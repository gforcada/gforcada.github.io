Title: rebre notificacions del cron al teu client de correu preferit
Date: 2010-08-18 13:45
Author: admin
Category: General
Tags: consells, debian, dovecot, programari lliure
Slug: rebre-notificacions-del-cron-al-teu-client-de-correu-preferit
Status: published
Attachments: wp-content/uploads/2010/08/debian.png

[<img src="{static}wp-content/uploads/2010/08/debian.png" title="Debian" class="alignright size-full wp-image-983" width="70" height="80" alt="Logo del projecte Debian" />]({static}wp-content/uploads/2010/08/debian.png)A la [feina](http://www.usecm.com "Pàgina web de l'empresa on treballo") ((Perdó per l'SPAM :D )) tenim un parell de servidors ((El típic escenari de producció i desenvolupament/test)) que corren amb [Debian](http://www.debian.org/ "Pàgina web de la distribució GNU/Linux Debian") on entre moltes altres coses hi tinc alguns processos amb cron i tal.

Com que des que [vaig configurar](http://gil.badall.net/2010/06/25/configurar-un-servidor-de-correu/ "Entrada del bloc on parlo sobre com configurar el servidor de correu a Gentoo") un servidor de correu al servidor de casa estic rebent la sortida de l'execució dels processos que tinc en el cron per correu electrònic i trobo que és molt útil avui he fet el mateix a la feina, i la veritat és que ha sigut la cosa més senzilla del món!

**Nota:** amb aquesta configuració només rebreu els correus interns del propi servidor, no tindreu un servidor de correu completament funcional ni molt menys!

## Passos per fer-ho:

1.  Configurar un registre MX d'un domini que tingueu al vostre abast per poder adreçar-vos-hi per recollir el correu.
2.  Deixar tal qual està l'exim4 tal com ve per defecte a Debian (o sigui no fer res :D).
3.  Instal·lar el dovecot-imap (apt-get install dovecot-imapd) ((Si voleu també podeu instal·lar el dovecot-pop3d per accedir a través de POP)).
4.  **Llestos!**

Ara l'únic que heu de fer és configurar el vostre client de correu perquè vagi a recollir a través d'IMAP els correus en el vostre servidor i d'aquesta manera tindreu puntualment la sortida de les execuccions dels processos del cron al vostre client de correu :D

## Punts extra

- Per si no us n'adoneu quan instal·leu el dovecot-imapd: el propi dovecot crea un certificat auto-generat de manera que només fent els 4 passos de sobre ((Realment dos: el primer i el tercer,  i un només en el propi servidor.)) teniu xifratge de la connexió gratuïtament :D

<!-- -->

- Per no haver de tenir 40.000 comptes en el client de correu que utilitzeu podeu afegir la següent línia al crontab de tots els usuaris que tinguin cron:

> MAILTO=jordi@localhost

D'aquesta manera tots els usuaris que en el seu crontab tinguin aquesta línia enviaran el correu a l'usuari *jordi*, de manera que l'únic compte que haureu de tenir en el vostre client de correu és el de l'usuari jordi.
