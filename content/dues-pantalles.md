Title: dues pantalles
Date: 2009-09-18 15:01
Author: admin
Category: General
Tags: consells, GNOME, xrandr
Slug: dues-pantalles
Status: published
Attachments: wp-content/uploads/2009/09/pantalla-externa.jpg

Ja fa molt de temps que treballo únicament amb portàtil i tenia l'ordinador que utilitzava abans abandonat, però des de fa un temps que el vaig moure a la taula on tinc normalment el portàtil que anava veient la pantalla de l'ordinador que estava tancada i cobrint-se de pols perquè no la feia servir.

Després d'algun intent frustat d'intentar fer-la funcionar correctament (el GNOME ja detectava la pantalla externa però només a 800x600) avui finalment he aconseguit que funcioni correctament a 1024x768 :D

Així que aquí va la recepta pels que tingueu una pantalla externa velleta. La pantalla (una Acer AL512 vegeu la foto) deu tenir uns  6 o 7 anys tranquilament i suposo que és per aquest motiu que el xrandr no em detectava aquest mode de 1024x768 i es quedava amb els 800x600 i 640x480.

<p>

<figure>
<img src="http://gil.badall.net/wp-content/uploads/2009/09/pantalla-externa-300x290.jpg" title="pantalla-externa" class="size-medium wp-image-657" width="300" height="290" alt="La meva pantalla externa" />
<figcaption aria-hidden="true">La meva pantalla externa</figcaption>
</figure>

</p>

Si com a mi us passa que al fer un ***xrandr -q*** no us mostra el mode de resolució que vosaltres voleu haureu de fer aquests passos:

Amb l'ordre **gtf** li dieu les mides i la velocitat de refresc que voleu, per exemple:

    $ gtf 1024 768 60
    # 1024x768 @ 60.00 Hz (GTF) hsync: 47.70 kHz; pclk: 64.11 MHz
     Modeline "1024x768_60.00"  64.11  1024 1080 1184 1344  768 769 772 795  -HSync +Vsync

Agafeu tot el que hi ha després de *Modeline* en aquesta última línia i li passeu a l'xrandr:

    $ xrandr --newmode Modeline

Ja només us queda afegir el nou mode a la pantalla que volgueu (en el meu cas la VGA externa):

    $ xrandr --addmode VGA 1024x768_60.00

*(Podeu veure que el segon text de la sortida del gtf és el nom que li dóna al mode, podeu canviar-lo si voleu)*

Finalment només us falta aplicar el mode a la pantalla:

    $ xrandr --output VGA --mode 1024x768_60.00

I llestos, ja teniu la pantalla a la mida que us ve més de gust :)

Per a més comoditat podeu moure les pantalles (si estan de costat, una sobre de l'altra i en quin ordre) des de l'aplicació de configuració del propi GNOME que va molt bé, l'únic que li manca és poder afegir nous modes :(

Si a més també utilitzeu molt els espais de treball us pot interessar l'informe de millora que he enviat avui al bugzilla del GNOME: [595562 - Allow to stick a workspace to a monitor](https://bugzilla.gnome.org/show_bug.cgi?id=595562 "Informe de millora enviat al bugzilla del GNOME per permetre que en una pantalla es mostri permanentment un sol espai de treball").
