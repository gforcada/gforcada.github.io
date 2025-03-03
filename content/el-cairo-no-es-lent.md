Title: el cairo no és lent!
Date: 2009-10-15 14:09
Author: admin
Category: General
Tags: benjamin otte, cairo, GNOME, gstreamer, xserver
Slug: el-cairo-no-es-lent
Status: published
Attachments: wp-content/uploads/2009/10/cairo-logo.png

<img src="{static}wp-content/uploads/2009/10/cairo-logo.png" title="cairo-logo" class="alignright size-full wp-image-674" width="370" height="81" alt="cairo-logo" />Un dels punts més forts del programari lliure és precisament la capacitat de poder analitzar i millor el codi que s'executa.

Agafant-se en aquest principi ja fa uns dies vaig llegir en el [planet GNOME](http://planet.gnome.org "Planeta on desenvolupadors i col·laboradors del GNOME tenen sindicats els seus blocs") que en [Benjamin Otte](http://blogs.gnome.org/otte/ "Blog d'en Benjamin Otte") havia decidit decidit [posar ordre](http://blogs.gnome.org/otte/2009/10/05/cairo-is-slow/ "Entrada al bloc d'en Benjamin Otte on demostra el resultat del seu treball") a tota la pila de programes que intervenen en la reproducció de vídeo per fer que funcioni molt millor.

Un intent de resum seria dir que ha modificat el [gstreamer](http://gstreamer.freedesktop.org/ "Lloc web del projecte GStreamer, un entorn de treball multimèdia"), el [cairo](http://cairographics.org/ "Lloc web del projecte Cairo, una biblioteca per generar gràfics en 2D"), el pixman i l'[xserver](http://www.x.org/ "Lloc web del projecte X.org") perquè el primer utilitzi el segon per a mostrar el vídeo i com que el segon utilitza el tercer i el quart, ha fet que entre tots quatre treballin amb el mateix format d'imatge (eliminant així els costosos canvis de format) i fent que tot aquesta poca feina que queda si eliminem els canvis de format el faci la pròpia targeta gràfica.

El vídeo que adjunta en el seu bloc en deixa prou constància de la impressionant millora ([enllaç al vídeo](http://people.freedesktop.org/~company/stuff/gst-cairo.ogv "Enllaç al vídeo que demostra la millora ostensible del rendiment de tot plegat")).

Però el millor no acaba aquí! Ja que gràcies al seu treball inicial en fer els pedaços per a cada un dels programes mencionats a sobre ha pogut captar l'atenció de les parts implicades (les comunitats i empreses al voltant dels projectes) i de resultes de tot plegat [es farà una hackfest](http://blogs.gnome.org/otte/2009/10/14/video-hackfest/ "Entrada al bloc d'en Benjamin Otte sobre la pròxima video hackfest a Barcelona") (una trobada de desenvolupadors per a centar-se en un tema en concret) a Barcelona amb alguns dels desenvolupadors de tots els projectes per a millorar encara més el que ja ha començat en Benjamin.

Pot semblar senzill tot plegat: agafar els programes que creus que es poden millorar, fer-ne les millores, publicar-les i que s'adopti el codi a cada projecte per tal que no sigui un *hack* que hagi fet un i prou sinó que en les pròximes versions estables s'incorpori el codi i així tothom pugui beneficiar-se del seu treball, però si us mireu els projectes, només per entendre bé el funcionament del GStreamer, el Cairo, el pixman i l'xserver s'ha d'estudiar molt detingudament cada codi per no trencar coses que ja funcionaven i a més a més entendre-ho tant i tant bé que els canvis que es fan millorin (i de quina forma!) el rendiment global de la reproducció de vídeos.

Si això ho ha pogut fer en Benjamin tot sol, m'agradarà veure què en sortirà d'aquí un mes i pocs dies (21-22 del mes que ve) en la hackfest que es farà!

A més a més no només beneficiarà a la reproducció de vídeo el fet que des del GStreamer fins a l'xserver es treballi de manera més conjunta i coordinada, sinó que tots els programes que requereixin capacitats gràfiques pel seu funcionament (Compiz, Clutter, etc) també en sortiran beneficiats!
