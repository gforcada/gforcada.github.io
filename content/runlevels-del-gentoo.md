Title: runlevels del gentoo
Date: 2007-03-06 19:45
Author: admin
Category: General
Tags: gentoo, programari lliure, runlevels
Slug: runlevels-del-gentoo
Status: published

com que els blocs serveixen, sovint, com a notes per a un mateix, aquí va la primera meva :)

els *runlevels* (o nivells d'execució) serveixen per dir-li al S.O. que engegui els serveis que volem, per exemple, podem tenir el runlevel de servidor, el d'escriptori, el de manteniment, etc etc

de manera que amb el nivell de servidor hi hauria els serveis de base de dades, web, etc etc en el d'escriptori no hi hauria servidors, en el de manteniment hi hauria, per exemple els mínims dels mínims serveis, per assegurar-nos que així tot està parat i es pot remenar les configuracions de qualsevol servei, actualitzar-lo, etc etc

i anant al tema, a <a href="http://www.gentoo.org" target="_blank" rel="noopener">gentoo</a>, a diferència d'altres distribucions que els nivells d'execució estan a **/etc/rc\*.d** (on l'\* va de 0 a 6, tot i que se'n poden posar tants com un vulgui) estan a **/etc/runlevels/\*** (on aquí l'\* pot ser qualsevol nom, el per defecte és *default*)

per gestionar els nivells tenim l'eina rc-update que bàsicament el que fa és 3 coses, mostrar els serveis d'un nivell, afegir-hi serveis i suprimir-ne:

    # llistem els serveis del runlevel default
    rc-update show default
    # afegim l'apache2 als runlevels servidor i default
    rc-update add apache2 servidor default
    # suprimim l'apache2 del runlevel default
    rc-update del apache2 default

tot i que a gentoo es canvii l'esquema dels noms de les carpetes dels *runlevels*, al igual com en la pràctica totalitat de les distribucions, tot el que hi ha en aquestes carpetes són enllaços simbòlics cap a **/etc/init.d**
