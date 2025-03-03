Title: compartir música a través de la xarxa local
Date: 2007-11-14 01:18
Author: admin
Category: General
Tags: amarok, apple, avahi, banshee, música, programari lliure, rhythmbox, tangerine, zeroconf
Slug: compartir-musica-a-traves-de-la-xarxa-local
Status: published
Attachments: wp-content/uploads/2007/11/tangerine-48.png, wp-content/uploads/2007/11/avahi.png

com força gent es troba habitualment que té diversos ordinadors a casa seva, acabes tenint tota la música en un ordinador perquè era el que feies servir abans, però des de que tens el portàtil o l'ordinador nou que ja no el fas servir per res, però fa molta mandra anar movent la música d'una banda cap a l'altre, etc etc

però per sort des de fa temps hi ha una tecnologia que s'anomena de "*configuració zero*" que es va inventar <a href="http://www.apple.com/" target="_blank" rel="noopener">Apple</a> per al seu reproductor de música <a href="http://www.apple.com/itunes/" target="_blank" rel="noopener">iTunes</a>\[1\] per a compartir música a través de la xarxa local, de manera que si dues persones tenien l'iTunes engegat i estaven a la mateixa xarxa local podien veure i escoltar la música de l'altre

<img src="{static}wp-content/uploads/2007/11/avahi.png" data-align="right" alt="icona de l’avahi" />

**el programari lliure**

com de costum no es va quedar enrere i va sortir l'<a href="http://avahi.org" target="_blank" rel="noopener">avahi</a>\[2\] que no només permet compartir música sinó que directament va un pas més enllà i es tot un servei integral de descoberta de serveis que s'autopubliquin per la xarxa local: si algú té la impressora compartida la pots veure a través de l'avahi (llavors falta que els programes ho implementin com de costum, però amb el temps ...) o si tens carpetes compartides, si hi ha servidors de ssh o ftp ...

per a l'avahi hi ha un programa força interessant que es una espècie de navegador amb el que pots veure tots els serveis que l'avahi es capaç de veure (s'anomena *avahi zeroconf browser*)

**tangerine**

però al que anava, si l'ordinador aquell que tens abandonat no el fas servir ni tan sols amb la pantalla llavors resulta difícil poder engegar els programes com el <a href="http://www.gnome.org/projects/rhythmbox/" target="_blank" rel="noopener">Rhythmbox</a>, <a href="http://banshee-project.org" target="_blank" rel="noopener">Banshee</a> o <a href="http://amarok.kde.org" target="_blank" rel="noopener">amaroK</a> (per dir-ne alguns), ja que t'obliga a tenir un usuari amb la sessió oberta, fer-ho manualment cada vegada, etc etc

<img src="{static}wp-content/uploads/2007/11/tangerine-48.png" data-align="right" alt="icona del tangerine" />així que per a respondre a aquestes necessitats tenim el <a href="http://www.snorp.net/log/tangerine" target="_blank" rel="noopener">tangerine</a>, un programa que amb un simple fitxer de text com a fitxer de configuració ens permet tenir un servidor de música ben ràpid i fàcil de fer servir :) fins i tot proporciona una interfície gràfica per a configurar-lo si algú el fa servir en ordinadors amb pantalla

el fitxer en concret ha d'estar a ~/.tangerine i més o menys hauria de ser una cosa per l'estil:

    [Tangerine]
    name = servidor de so
    password_file = /root/.tangerine-passwd
    debug = True
    max_users = 0
    log_file = /root/.tangerine-log
    port = 0
    publish = True
    plugins = file,session
    [FilePlugin]
    directories = /arx_petit/musica

el que em falta acabar de mirar és com posar-lo com a dimoni i que pugui estar en els runlevels com li pertocaria a un servei com al cap i a la fi és

apart, que al ser un programet petit no està ara mateix en el portage del <a href="http://www.gentoo.org" target="_blank" rel="noopener">Gentoo</a>, tot i que si que hi ha un <a href="http://bugs.gentoo.org/attachment.cgi?id=124277" target="_blank" rel="noopener">ebuild</a> en el [bugzilla del Gentoo](http://bugs.gentoo.org) (bug [\#147053](http://bugs.gentoo.org/show_bug.cgi?id=147053))

algú sap com s'han de crear els fitxers que han d'anar a */etc/init.d* i als diferents *runlevels*? algun punter a documentació estaria molt bé :)

\[1\] que tot sigui dit, el fet de compartir música per la xarxa local amb l'iTunes els va portar molts problemes als senyors d'Apple, perquè les grans discogràfiques hi estaven totalment en contra i a cada nova versió de l'iTunes les capacitats de compartir anaven a menys

\[2\] encara no havia vist el seu logotip però realment els falta algun dissenyador inspirat a aquesta gent :)
