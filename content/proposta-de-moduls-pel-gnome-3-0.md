Title: Proposta de mòduls pel GNOME 3.0
Date: 2010-10-08 06:06
Author: admin
Category: General
Tags: GNOME, GNOME-3
Slug: proposta-de-moduls-pel-gnome-3-0
Status: published

[<img src="./wp-content/uploads/2008/01/gnomefoot.png" title="logotip del GNOME" class="alignright size-full wp-image-274" width="122" height="150" />](http://gil.badall.net/wp-content/uploads/2008/01/gnomefoot.png)Avui s'acaba d'anunciar la [proposta nova de distribució de mòduls](http://mail.gnome.org/archives/devel-announce-list/2010-October/msg00001.html "Correu a la llista anunciant la nova proposta de mòduls") del que serà el **GNOME 3.0**.

Fins ara el GNOME tenia els conjunts de mòduls: d'administració, les eines de desenvolupament, la plataforma i l'escriptori.

Aquest últim (l'escriptori) és el que provocava més *tensions*, ja que pel fet de ser un conjunt de mòduls únics si s'afegia un reproductor de música (el [Rhythmbox](http://projects.gnome.org/rhythmbox/ "Pàgina web del reproductor de música Rhythmbox") per exemple) s'estava donant el missatge que el [Banshee](http://banshee.fm/ "Pàgina web del reproductor de música Banshee") no era recomanat pel [GNOME](http://www.gnome.org "Pàgina web del projecte d'escriptori lliure GNOME").

Amb la proposta nova s'han ampliat els conjunts de mòduls i es serà més inclusiu (sol·lucionant així el debat Rhythmbox/Banshee) i també es posarà l'accent en tot el que és la plataforma.

Els conjunts de mòduls nous seran:

- **Plataforma del sistema:** projectes a una capa inferior a l'escriptori i que no són part del GNOME, el NetworkManager, bluez (per Bluetooth), cairo (per gràfics), libxml (per processar xml) etc etc
- **Plataforma estable:** el que fins ara era plataforma, és a dir, les biblioteques bàsiques perquè funcioni el GNOME, Gtk+, GLib, etc etc. A més a més aquest conjunt donarà estabilitat API/ABI.
- **Plataforma estesa:** tots aquells mòduls que en un futur podran ser part de la plataforma estable però que encara no són prou madurs per ser estables del tot en períodes de temps llargs, per exemple el GStreamer, webkitgtk ... Així es dóna un missatge als desenvolupadors de quines eines han de fer servir.
- **Nucli de l'escriptori:** aquí ja entrem a l'escriptori com a tal, en aquest conjunt hi haurà tot el que es considera indispensable per poder fer funcionar una sessió, el centre de control, el Nautilus, etc etc
- **Aplicacions:** per sol·lucionar el debat Rhythmbox/Banshee aquest últim conjunt serà una recopil·lació d'aplicacions que respecten uns barems de qualitat i que per tant poden presentar-se juntament amb el GNOME. D'aquesta manera qualsevol aplicació que treballi sobre l'escriptori GNOME podrà ser elegible per entrar en aquest conjunt, però haurà de complir una sèrie de requisits, assegurant així la qualitat del que es presentarà a ulls de tothom el GNOME.

Personalment trobo que és una decisió molt bona sobretot per la part de plataforma, ara ja es donarà un missatge clar a qualsevol desenvolupador de quines eines ha d'utilitzar en tot el procés (des de baix nivell, a els mòduls bàsics i les eines més innovadores).

L'únic que em fa arrufar el nas és, com ja es diu en més d'una ocasió en el missatge d'anunci, com es gestionarà totes les traduccions, i sobretot l'increment d'aquestes pel fet que el conjunt Aplicacions passi a ser una recopil·lació de programari.

El que segur que serà és una molt bona oportunitat per fer avançar encara més el GNOME.
