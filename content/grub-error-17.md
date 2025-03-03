Title: grub error 17
Date: 2007-11-18 23:11
Author: admin
Category: General
Tags: bios, debian, grub, guifi, mont-rodon, problemes, servidor proxy, ubuntu
Slug: grub-error-17
Status: published

<img src="http://gil.badall.net/wp-content/uploads/2007/10/logo-guifi.png" data-align="right" alt="logo guifi" />acabo d'instal·lar el que serà el servidor de Mont-rodon (el <a href="http://guifi.net/ca/guifi/device/6748" target="_blank" rel="noopener">Gurri</a>), però m'he trobat que just després d'acabar la instal·lació d'una <a href="http://www.debian.org" target="_blank" rel="noopener">Debian</a> estable i reiniciar el <a href="http://www.gnu.org/software/grub" target="_blank" rel="noopener">Grub</a> em donava l'error número 17

segons <a href="http://www.gnu.org/software/grub/manual/grub.html" target="_blank" rel="noopener">el manual del grub</a> això és perquè tot i que existeixi la partició el grub no sap de quin tipus és

després d'iniciar amb un cd autònom d'<a href="http://www.ubuntu.com" target="_blank" rel="noopener">Ubuntu</a> he vist que ni el *menu.lst* ni la partició semblaven malmeses, així que buscant una mica per Internet m'he trobat amb la sol·lució: resulta que en els ordinadors vells (com en el meu cas) remenant la <a href="http://ca.wikipedia.org/wiki/BIOS" target="_blank" rel="noopener">BIOS</a> en pots tenir prou, i efectivament, el canal màster del primer <a href="http://en.wikipedia.org/wiki/Integrated_Drive_Electronics" target="_blank" rel="noopener">IDE</a> de l'ordinador estava fixat que es detectés com a LBA (ni idea què vol dir això), però com que tenia el mode automàtic, li he posat i llestos, ja s'engega al Debian :)

a instal·lar i configurar <a href="http://guifi.net/ca/guifi/device/6748/view/services" target="_blank" rel="noopener">tots els serveis</a> que ja li he configurat en la pàgina de <a href="http://guifi.net" target="_blank" rel="noopener">guifi</a>
