Title: idioma predeterminat a un centOS
Date: 2007-12-27 13:43
Author: admin
Category: General
Tags: centos, debian, distribucions, dns, gentoo, guifi, i18n, problemes, redhat
Slug: idioma-predeterminat-a-un-centos
Status: published
Attachments: wp-content/uploads/2007/12/centos_icon_60.png

<img src="{static}wp-content/uploads/2007/12/centos_icon_60.png" data-align="right" alt="centos logo" />tot mirant com instal·lar un servidor de <a href="http://en.wikipedia.org/wiki/Dns" target="_blank" rel="noopener">DNS</a> a un servidor de <a href="http://guifi.net" target="_blank" rel="noopener">guifi.net</a> (<a href="http://guifi.net/guifi/device/4325" target="_blank" rel="noopener">elpipa</a> de <a href="http://guifi.net/ca/centelles" target="_blank" rel="noopener">Centelles</a> en concret) he tingut molts problemes, entre els quals que no podia canviar l'idioma predeterminat del sistema que estava a castellà i evidentment que el prefereixo tenir en català per molt que hi entri per ssh

com que la distribució és una <a href="http://www.centos.org" target="_blank" rel="noopener">CentOS</a> i no l'havia tocat mai he començat a buscar per Internet i al cap de força estona he desistit i m'he començat a mirar els fitxers que hi havia dintre */etc*

cap al final de la llista hi ha la carpeta de *sysconfig* i a dintre d'aquesta un fitxer força intuïtiu que és diu *i18n* on hi ha unes quantes variables per a configurar l'idioma i el tipus de lletra

a més hi ha les aplicacions *system-config-language* i *system-config-keyboard* per a configurar-ho

no he reiniciat el servidor per a provar-ho, però en sortir i tornar a entrar per *ssh* sí que funciona i quan faig un *locale* ja em mostra el ca_ES.UTF-8 :D

ara que hi penso suposo que si vaig a la documentació de la <a href="http://www.redhat.com/rhel" target="_blank" rel="noopener">RHEL</a> ho hauria trobat oi?

P.D. de nou a <a href="http://www.gentoo.org" target="_blank" rel="noopener">Gentoo</a> i <a href="http://www.debian.org" target="_blank" rel="noopener">Debian</a> es configura d'una manera, a <a href="http://www.redhat.com" target="_blank" rel="noopener">Red Hat</a> d'una altra, a saber a <a href="http://www.opensuse.org/" target="_blank" rel="noopener">Suse</a> i <a href="http://www.mandriva.com" target="_blank" rel="noopener">Mandriva</a> ... tampoc es tant difícil posar-se d'acord en temes com aquests no?
