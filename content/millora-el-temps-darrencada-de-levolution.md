Title: Millora el temps d'arrencada de l'Evolution
Date: 2011-10-02 12:42
Author: admin
Category: General
Tags: consells, evolution, GNOME
Slug: millora-el-temps-darrencada-de-levolution
Status: published

[<img src="http://gil.badall.net/wp-content/uploads/2008/07/evo.png" title="Logotip de l&#39;Evolution" class="alignright size-full wp-image-382" width="100" height="93" />](http://gil.badall.net/wp-content/uploads/2008/07/evo.png)Si utilitzeu l'[Evolution](http://projects.gnome.org/evolution/ "Pàgina del programa de correu, contactes, calendari i notes Evolution"), el gestor de correu del [GNOME](http://gnome.org "Pàgina web del projecte GNOME") i us sembla que tarda una mica massa en obrir-se proveu aquest consell que comenta en [Pacho Ramos al seu bloc](http://my.opera.com/pacho/blog/2011/09/18/reviving-completely-messed-up-evolution "Entrada al bloc d'en Pacho Ramos on comenta com millorar el temps d'arrencada de l'Evolution"):

> cd ~/.local/share/evolution
>
> for i in \`find . -name folders.db\`; do echo "Rebuilding Table \$i"; sqlite3 \$i "vacuum;" ; done

Només he fet servir la segona part, no tenia ganes de fer un còpia de seguretat per si les mosques :)
