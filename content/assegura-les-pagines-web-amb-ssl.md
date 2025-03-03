Title: Assegura les pàgines web amb SSL
Date: 2011-02-12 11:09
Author: admin
Category: General
Tags: consells, servidors, ssl
Slug: assegura-les-pagines-web-amb-ssl
Status: published

Cada vegada que envies dades per Internet, l'URL d'una pàgina web, un comentari, l'autenticació a una pàgina web... aquestes dades s'estan enviant sense encriptar, de manera que tothom que estigui entre el servidor on et connectes i el teu ordinador **amb molt poc esforç pot veure què fas o quin usuari i contrasenya tens**.

Per això es van inventar ja fa anys l'[SSL](http://en.wikipedia.org/wiki/Secure_Sockets_Layer "Article de la wikipedia anglesa sobre l'SSL"), un protocol que funciona sobre HTTP que permet fer comunicacions xifrades d'exterm a extrem de manera que per moltes persones que estiguin pel mig de la comunicació entre el servidor i el vostre ordinador, no podran saber què es comunica.

Per tal de configurar un servidor web perquè enviï les pàgines amb SSL ens fa falta un certificat. Hi ha dues maneres d'aconseguir-lo, o bé pagant a una entitat certificadora perquè ens doni un certificat que tots els navegadors reconeixeran com a segur, o bé, fer-los nosaltres mateixos. Els navegadors no el reconeixeran directament com a segur, però si nosaltres sabem on ens connectem no hi ha problema.

Aquí va la recepta per al segon mètode: fer-ho nosaltres mateixos ((L'única diferència amb fer-ho amb un de pagament és que en comptes de generar el certificat nosaltres ens el dóna l'entitat certificadora)).

- Instal·lem l'[OpenSSL](http://www.openssl.org/ "Pàgina web del projecte OpenSSL") a la nostra màquina (ha de ser al propi servidor per facilitar-ho tot)
- Creem la clau del servidor: **openssl genrsa 2048 \> server.key** ((Com sempre hi ha mil i un paràmetre per jugar-hi si us hi voleu entretenir))
- Creem el certificat: **openssl req -new -x509 -nodes -sha1 -days 365 -key server.key \> server.crt**
  - Responem totes les preguntes que ens fa l'auxiliar (són força fàcils :) )
- Activem el mòdul d'SSL de l'Apache ((ada distribució és diferent però normalment instal·lant el mòdul mod_ssl des del gestor de paquets ja l'habilita))
- Ja podem editar la màquina virtual de l'Apache per afegir-li la configuració per SSL. Vindria a ser una cosa a l'estil:

<!-- -->

    <VirtualHost *:443>
    ServerName servidor.guifi.net
    ServerAdmin admin@guifi.net
    SSLEngine on
    # Change the next two lines according to where you've actually
    # stored the certificate and key files.
    SSLCertificateFile /etc/ssl/apache2/server.crt
    SSLCertificateKeyFile /etc/ssl/apache2/server.key

    ServerName domain.tld
    SSLOptions StrictRequire
    SSLProtocol all -SSLv2

    DocumentRoot /path/to/ssl/enabled/site
    <Directory /path/to/ssl/enabled/site/>
    SSLRequireSSL
    Order Deny,Allow
    Allow from All
    </Directory>

Aquí sí que ja serà cada màquina virtual i cada domini que s'haurà de configurar com a un millor li sembli, i sobretot les necessitats que tingui. Els paràmetres clau són els del certificat i clau (SSLCertificateFile i SSLCertificateKeyFile).

Ara ja només us queda fer proves al servidor abans de donar-lo per definitiu. En aquesta fase de proves, i també en producció, us pot ser molt útil tenir fitxers de registres (els famosos logs) diferents si es per SSL o per text pla.

Si voleu per exemple que tot el trànsit sigui per SSL podeu fer un redireccionament de tot el trànsit per text pla a SSL amb:

    <VirtualHost *:80>
    ServerName servidor.guifi.net
    ServerAdmin admin@guifi.net

    RewriteEngine On
    Redirect permanent / https://servidor.guifi.net
    </VirtualHost>
