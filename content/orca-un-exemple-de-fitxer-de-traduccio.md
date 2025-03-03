Title: orca, un exemple de fitxer de traducció
Date: 2007-04-10 19:10
Author: admin
Category: General
Tags: disminució visual, firefox, GNOME traduccions, orca, traduccions
Slug: orca-un-exemple-de-fitxer-de-traduccio
Status: published

porto la traducció al català de l'<a href="http://l10n.gnome.org/module/orca" target="_blank" rel="noopener">Orca</a> pel <a href="http://www.gnome.org" target="_blank" rel="noopener">GNOME</a> i la sorpresa va ser majúscula quan vaig veure que pràcticament TOTES les cadenes del <a href="http://l10n.gnome.org/POT/orca.HEAD/orca.HEAD.pot" target="_blank" rel="noopener">fitxer de traducció</a> tenien unes quantes línies de comentaris explicant el context de cada cadena

a tall d'exemple:

    #. Translators: this represents the state of a node in a tree.

    #. 'expanded' means the children are showing.

    #. 'collapsed' means the children are not showing.

    #.

    #: ../src/orca/braillegenerator.py:1073 ../src/orca/J2SE-access-bridge.py:72

    #: ../src/orca/speechgenerator.py:1247 ../src/orca/where_am_I.py:555

    msgid "expanded"

    msgstr ""#. Translators: this represents the state of a node in a tree.

    #. 'expanded' means the children are showing.

    #. 'collapsed' means the children are not showing.

    #.

    #: ../src/orca/braillegenerator.py:1079 ../src/orca/J2SE-access-bridge.py:79

    #: ../src/orca/speechgenerator.py:1253 ../src/orca/where_am_I.py:561

    msgid "collapsed"

    msgstr ""

i així pràcticament totes les cadenes, la qual cosa facilita molt la feina de traducció, apart que en el cas concret de l'Orca, al ser un lector de pantalla i ampliador ajuda encara més, ja que el programa es per treballar sobre altres programes, amb la qual cosa no tens el context de l'aplicació (per exemple, si es un navegador web i parla de *link* sabràs que es refereix a un enllaç web)

a més per la gent amb disminucions visuals els serà tota una delícia el pròxim llançament de l'Orca, ja que aquest permetrà emprar el <a href="http://www.mozilla-europe.org/ca/products/firefox/" target="_blank" rel="noopener">firefox</a> amb l'Orca
