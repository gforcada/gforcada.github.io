Title: mida personalitzada al gnome-terminal
Date: 2008-12-16 15:53
Author: admin
Category: General
Tags: consells, GNOME, terminal
Slug: mida-personalitzada-al-gnome-terminal
Status: published

<img src="http://gil.badall.net/wp-content/uploads/2007/12/gnomelovelogo.png" title="logotip del GNOME Love" class="alignright size-full wp-image-259" width="150" height="150" alt="logotip del GNOME Love" />Com que tinc una pantalla de 15,4 polzades els terminals de 80x24 no em coincideixen massa bé a la pantalla si en vull tenir uns quants d'oberts alhora (normalment 4 formant una graella de 2x2), de manera que sempre acabo redimensionant els terminals a 87x23 enlloc del 80x24 que és el predeterminat.

De manera que per a canviar-ho i fer que els 87x23 siguin els valors predeterminats he buscat una mica i ja hi he trobat la solució :)

Es pot cridar el [gnome-terminal](http://en.wikipedia.org/wiki/GNOME_Terminal "Article a la Wikipedia anglesa sobre el GNOME Terminal, el terminal del GNOME") amb l'opció **--geometry=*files*x*columnes***.

De manera que només cal canviar el terminal predeterminat del sistema a (Sistema → Preferències → Aplicacions Preferides) i posar-hi l'ordre: gnome-terminal --geometry=87x23 :D
