Title: entrar una sola vegada la frase de pas de la clau privada
Date: 2007-11-05 20:18
Author: admin
Category: General
Tags: consells, GNOME, gnome-session, seahorse, ssh
Slug: entrar-una-sola-vegada-la-frase-de-pas-de-la-clau-privada
Status: published
Attachments: wp-content/uploads/2007/11/seahorse.png, wp-content/uploads/2007/11/captura-edita-el-programa-dinici.png

<img src="{static}wp-content/uploads/2007/11/seahorse.png" data-align="right" alt="logotip del Seahorse" />si en <a href="?p=223" target="_blank" rel="noopener">l'apunt anterior</a> comentava com copiar la clau pública a d'altres ordinadors ara el que interessa és que no haguem d'escriure la frase de pas (*passprhase* en anglès) cada vegada que ens connectem, ja que el que havíem guanyat en seguretat i comoditat al fer el sistema de claus públiques i privades el perdem si igualment no entrem la contrasenya de l'usuari, però si la de la clau privada

de manera que el que hem de fer és instal·lar el <a href="http://www.gnome.org/projects/seahorse/index.html" target="_blank" rel="noopener">Seahorse</a>-agent si no el teniu instal·lat (per exemple en l'<a href="http://www.ubuntu.com" target="_blank" rel="noopener">Ubuntu</a> Gutsy a mi no me li deixava instal·lat) i afegir-lo en els programes d'inici a través de l'aplicació de configuració del *gnome-session*

![captura del gnome-session]({static}wp-content/uploads/2007/11/captura-edita-el-programa-dinici.png)

un cop fet això quan sortiu i torneu a entrar a la sessió veureu que no ha canviat res, però quan obriu un terminal i entreu a un ordinador remot on hi tingueu la clau pública us sortirà un diàleg en GTK+ perquè introduïu la frase de pas i seguidament us deixarà d'empipar

a partir d'aquest moment ja podeu entrar a tants llocs com vulgueu, que si hi ha la clau pública ja no us caldrà escriure mai més la frase de pas ni contrasenya fins que tanqueu la sessió o buideu la memòria cau del Seahorse

P.D. en principi hauria de sortir una parella de claus a l'àrea de notificació del <a href="http://www.gnome.org" target="_blank" rel="noopener">GNOME</a>, però almenys a mi no em surt

P.D. 2 és un bug del compiz que no surti les decoracions quan fas captures de pantalla?
