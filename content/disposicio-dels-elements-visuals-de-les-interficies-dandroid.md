Title: Disposició dels elements visuals de les interfícies d'Android
Date: 2010-08-27 06:24
Author: admin
Category: General
Tags: android, disseny, disseny d'interfícies, glade, xml
Slug: disposicio-dels-elements-visuals-de-les-interficies-dandroid
Status: published
Attachments: wp-content/uploads/2010/08/Android-logo.jpg

[<img src="{static}wp-content/uploads/2010/08/Android-logo.jpg" title="Android-logo" class="alignright size-full wp-image-993" width="239" height="264" />]({static}wp-content/uploads/2010/08/Android-logo.jpg)Per dissenyar interfícies d'[Android](http://www.android.com/ "Pàgina web del projecte Android") has de fer-ho amb un [llenguatge](http://d.android.com/guide/topics/ui/index.html "Pàgina de la guia de desenvolupament per a Android sobre com crear interfícies") [XML](http://ca.wikipedia.org/wiki/XML "Entrada de la wikipedia catalana sobre el llenguatge de marcatge extensible (XML)") que s'han inventat aquests de [Google](http://www.google.com "Pàgina web prou coneguda"). A diferència per exemple de com ho fas a l'iPhone on ho fas, o bé amb un editor visual (estil [Glade](http://glade.gnome.org/ "Editor visual d'interfícies per a GTK+")), o bé directament des del codi. Amb l'Android pots fer-ho de dues maneres ((En realitat són tres, també hi ha un editor visual, però és menys que un *mal* intent de crear un editor d'interfícies)): o bé ho fas per codi, o ho fas amb el llenguatge aquest que comentava.

El fet és que com que és un XML hi pots treballar sense que t'hagis de tallar les venes, ja que entre altres coses et deixa separar tot el que és el estils del que és la declaració pròpiament dita de la interfície (molt a l'estil XHTML i CSS perquè ens entenguem).

Tot i així tampoc no és la panacea de l'edició d'interfícies, ja que si bé és molt senzill (i com a programador molt més amigable) poder treballar directament amb l'XML, el fet que l'Android estigui pensat per a una gran varietat de formats de sortida ((Des de pantalles de 2,5" fins a pantalles de 10" o més)) complia en certa manera com disposes els elements.

Per sort hi ha molta gent que escriu sobre com fer aquelles coses que se t'escapen a simple vista i avui he trobat un parell de blocs que valen molt la pena:

- [Una explicació bàsica de com funciona la gravetat](http://sandipchitale.blogspot.com/2010/05/linearlayout-gravity-and-layoutgravity.html "Entrada en un bloc on s'explica com funciona tot el tema de la gravetat en les interfícies d'Android")
- [Una altra explicació bàsica de com disposar elements en la interfície](http://mobiforge.com/designing/story/understanding-user-interface-android-part-1-layouts "Entrada en un bloc que parla sobre com es construeixen interfícies amb Android")
