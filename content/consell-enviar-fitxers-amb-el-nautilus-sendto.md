Title: consell: enviar fitxers amb el nautilus-sendto
Date: 2007-08-04 17:41
Author: admin
Category: General
Tags: consells, evolution, GNOME, nautilus-sendto, Softcatalà
Slug: consell-enviar-fitxers-amb-el-nautilus-sendto
Status: published
Attachments: wp-content/uploads/2007/08/nautilus-sendto.png, wp-content/uploads/2007/08/envia-a.png

com a membre del <a href="http://www.softcatala.org/wiki/GNOME" target="_blank" rel="noopener">projecte de traducció</a> del <a href="http://www.gnome.org" target="_blank" rel="noopener">GNOME</a> al català envio traduccions o revisions de traduccions a la <a href="http://llistes.softcatala.org/mailman/listinfo/gnome" target="_blank" rel="noopener">llista de coordinació</a>, de manera que cada vegada que haig d'enviar una traducció haig d'anar a l'<a href="http://www.gnome.org/projects/evolution/" target="_blank" rel="noopener">Evolution</a>, escriure el correu, obrir el diàleg de selecció de fitxers i anar per sistema de fitxers a buscar la traducció

però hi ha una manera molt més ràpida i còmode :)

l'únic que heu de fer és instal·lar el <a href="http://www.gnomefiles.org/app.php/Nautilus-SendTo" target="_blank" rel="noopener">nautilus-sendto</a> al vostre sistema: sudo apt-get install nautilus-sendto (a <a href="http://www.debian.org" target="_blank" rel="noopener">Debian</a> i derivats - entre ells <a href="http://www.ubuntu.com" target="_blank" rel="noopener">Ubuntu</a>) o emerge -va nautilus-sendto (a <a href="http://www.gentoo.org" target="_blank" rel="noopener">Gentoo</a> i derivats - si es que n'hi ha)

un cop fet això quan seleccioneu un fitxer, en el seu menú contextual us apareixerà això:

![menú contextual del nautilus-sendto]({static}wp-content/uploads/2007/08/nautilus-sendto.png)

un cop ho seleccioneu podeu triar a través de quin mètode voleu enviar el(s) fitxer(s) seleccionat(s):

![finestra del nautilus-sendto]({static}wp-content/uploads/2007/08/envia-a.png)

si trieu amb l'Evolution, us obrirà una finestra d'escriure correus amb l'adreça que heu posat en el diàleg anterior i els fitxers ja adjuntats, només us farà falta escriure el títol i el cos del correu :)
