Title: com instal·lar un SAI riello-ups a linux
Date: 2008-01-24 19:35
Author: admin
Category: General
Tags: centos, consells, linux, problemes, SAI
Slug: com-instal%c2%b7lar-un-sai-riello-ups-a-linux
Status: published

l'altre dia em van encarregar d'instal·lar i configurar l'aplicació de control d'un <a href="http://ca.wikipedia.org/wiki/SAI" target="_blank" rel="noopener">SAI</a> \[0\] (marca <a href="http://www.riello-ups.com/" target="_blank" rel="noopener">Riello-UPS</a> \[1\]) a un servidor

el model en concret importa poc perquè mentre sigui de la mateixa marca tots van amb el mateix programa, el <a href="http://www.riello-ups.com/downloadDettaglio.asp?language=eng&amp;dwns=22" target="_blank" rel="noopener">PowerShield</a>

per començar el primer problema que hi havia és que en el CD que m'havien donat hi havia la tira de directoris per a diferents sistemes operatius i l'únic que hi havia per Linux era per a una versió 2.4 del nucli

per sort, al seu lloc web ja et deixen baixar la versió nova (tenia la versió 2 i ara ja van per la 3) i aquesta sí que estava compilat per a nuclis 2.6 :)

s'instal·la ben fàcilment, és un rpm, ja que la distribució que hi ha en el servidor és un <a href="http://www.centos.org/" target="_blank" rel="noopener">CentOS</a>, però si mireu la pàgina de baixades hi ha paquets per a Gentoo, Debian, Solaris, Novell, Suse, Mac OS X, \*BSD entre d'altres, vaja que és difícil no tenir un paquet per al servidor que tinguis :)

a la mateixa pàgina del programa hi ha un manual (en <a href="http://extranet.riello-ups.com/areaftp/Manuals/Users%20Manual%205.0B.pdf" target="_blank" rel="noopener">anglès</a> i <a href="http://extranet.riello-ups.com/areaftp/Manuals/Manuale%20Utente%205.0B.pdf" target="_blank" rel="noopener">italià</a>) amb tota la documentació del programa

només heu de tenir el codi del SAI per a poder començar a configurar-lo i la resta és anar seguint el manual

per no canviar la tradició, per a Windows i Mac (no tinc clar si la versió de Mac és nadiua o bé a través de Java, ja que en el manual van junts) hi ha interfície gràfica i per a la resta tenim interfície de terminal

el programa en sí et permet fer de tot i més, gestionar molts SAI, posar-hi alarmes molt personalitzades, etc etc

per exemple (el que havia de fer-hi jo vaja) és que enviï un correu electrònic quan marxi la corrent, doncs per aquest propòsit, que ja està contemplat en el programa et diuen que directament agafis un fitxer que ja hi ha al mateix directori on s'instal·la tot (com a mínim per al paquet de Red Hat era /opt/upsmon) perquè hi fiquis el que et sembla, jo en el meu cas hi vaig posar:

    mail correu_a_qui_vulguis_que_avisi -s "Que això s'apaga!" < $1

on a \$1 en principi hi va un missatge del propi programa (que també pots canviar però no ho recomanen)

un cop ja està configurat només s'ha de iniciar el dimoni /etc/init.d/upsmon start i a tirar milles \[2\]

tot i així em vaig trobar amb que no es volia engegar, s'entestava a dir-me:

    Cannot allocate memory for shared data !

així que els vaig enviar un missatge <a href="http://www.riello-ups.com/contatti.asp?language=eng" target="_blank" rel="noopener">a través del seu lloc web</a> i avui molt amablement m'han respost amb:

    it means that shared is busy for 33000 (0x80E8) key
    So you have to:

    ipcs
    ipcrm -m <key ID>

    example:
    ipcs (enter)
    0x000080e8 4521990    root      666        76899      0
    ipcrm -m 4521990

    After this restart upsagent

i voilà ja funciona :)

P.D. ara no feu com he fet jo que he reiniciat el servidor per a comprovar que tot funcioni bé, que arrenqui, etc etc i resulta que el servidor es penja :(

\[0\] ara entenc l'*UPS* en el nom de l'empresa, fins ara no sabia que SAI en anglès és <a href="http://en.wikipedia.org/wiki/Uninterruptible_power_supply" target="_blank" rel="noopener">UPS</a> :)  
\[1\] no és per fer publicitat, sinó que com que tenen programari propi per un altre SAI no serveix de massa  
\[2\] per què diem *tirar milles* si a Catalunya sempre hem fet servir quilòmetres?
