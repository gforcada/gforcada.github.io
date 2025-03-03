Title: Ara és el millor moment per construir el GNOME 3.0
Date: 2011-02-20 17:05
Author: admin
Category: General
Tags: consells, GNOME, GNOME Shell, jhbuild, programari lliure
Slug: ara-es-el-millor-moment-per-construir-el-gnome-3-0
Status: published
Attachments: wp-content/uploads/2011/02/Screenshot.png

[<img src="./wp-content/uploads/2008/01/gnomefoot.png" title="logotip del GNOME" class="alignright size-full wp-image-274" width="122" height="150" />](./wp-content/uploads/2008/01/gnomefoot.png)Si sou impacients, o senzillament us agrada provar novetats, ja estareu al cas que [d'aquí poc](http://live.gnome.org/TwoPointNinetyone "Calendari de llançament del GNOME 3 previst pel 6 d'abril") sortirà el [GNOME 3](http://www.gnome3.org "Pàgina de promoció del GNOME3") amb el [GNOME Shell](http://live.gnome.org/GnomeShell "Pàgina principal del projecte GNOME Shell a la wiki del GNOME") i tot el que això implica.

Mentre les distribucions no empaqueten tots els mòduls que fan falta pel GNOME 3 sempre ens queda l'opció d'utilitzar el [JHBuild](http://library.gnome.org/devel/jhbuild/stable/ "Documentació del JHBuild, l'eina de compilació del GNOME"), un sistema d'automatització de seguiment de dependències, de la compilació dels paquets i de la instal·lació d'aquests.

Teniu una [secció específica a la pàgina del GNOME Shell](http://live.gnome.org/GnomeShell#Building "Secció de la pàgina principal del projecte GNOME Shell a la wiki del GNOME on s'explica com compilar el GNOME Shell") on s'explica tots els pocs passos que cal seguir perquè tingueu l'entorn del JHBuild .

**I per què ara és el millor moment?** Molt senzill, el GTK+3 ja ha sortit i des de fa ja uns dies/setmanes que tot el codi que s'envia als components principals del GNOME 3 només es permet que siguin pedaços que arreglin coses, no es permet afegir funcions noves, de manera que cada dia que passa la plataforma és més i més estable. Resultat: compilar a partir del codi font és molt més factible i no has de ser cap gurú per poder deixar l'ordinador compilant tots els mòduls necessaris. De fet és tant senzill que el fitxer de configuració del JHBuild que faig servir jo és tant simple com això:

    # Directory where to check sources out
    checkoutroot = '/opt/gnome-gil/source'

    # Directory where to install
    prefix = '/opt/gnome-gil/install'

    skip = [ ]
    skip.extend ([ 'mozilla', 'firefox', 'dbus', 'hal',
     'NetworkManager', 'PolicyKit', 'PolicyKit-gnome',
     'libgdiplus', 'mono', 'monodoc', 'nss', 'nspr',
     'sqlite3', 'pulseaudio', 'pysqlite2', 'mono-addins',
     'polkit', 'DeviceKit', 'DeviceKit-disks',
     'DeviceKit-power', 'libxml2', 'libxslt', 'libgpg-error',
     'libgcrypt', 'expat', 'libtasn1', 'gnutls',
     'libvolume_id', 'udisks', 'UPower', 'upower', 'evolution-exchange', 'evolution-mapi'
    ])

Amb això al fitxer ~/.jhbuildrc ja en tindreu prou per començar a compilar el GNOME 3.0.

Aquí us deixo una captura de pantalla ((Sí tinc un usuari que es diu jou per fer-lo servir per fer proves)) a mode de fer-vos dentetes a veure si us animeu a compilar-lo:

[<img src="./wp-content/uploads/2011/02/Screenshot-300x187.png" title="Screenshot" class="size-medium wp-image-1192 aligncenter" width="300" height="187" />]({static}wp-content/uploads/2011/02/Screenshot.png)
