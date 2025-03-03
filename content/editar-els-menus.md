Title: editar els menús
Date: 2007-03-26 16:05
Author: admin
Category: General
Tags: alacarte, especificacions, estandards, freedesktop, GNOME, kde, sílvia
Slug: editar-els-menus
Status: published

ja fa uns dies la <a href="http://silviamira.sytes.net/" target="_blank" rel="noopener">Sílvia</a> tenia problemes al editar la disposició del seu menú, ja que tot i que havia eliminat molts programes (la majoria de <a href="http://www.kde.org" target="_blank" rel="noopener">KDE</a>, tot i que alguns de <a href="http://www.gnome.org" target="_blank" rel="noopener">GNOME</a> diria que també) li continuaven sortint en el menú i des de l'editor de menús del GNOME (l'<a href="http://www.realistanew.com/projects/alacarte" target="_blank" rel="noopener">Alacarte</a>) no els podia eliminar de cap manera

així que investigant una mica vaig anar a parar a l'<a href="http://standards.freedesktop.org/menu-spec/1.0/" target="_blank" rel="noopener">especificació</a> de <a href="http://www.freedesktop.org" target="_blank" rel="noopener">freedesktop.org</a> sobre la disposició de menús

el menú, com sembla que sigui norma, cosa que no em sembla malament, es desa en un fitxer <a href="http://en.wikipedia.org/wiki/Xml" target="_blank" rel="noopener">xml</a> força *espagueti-western* (és mooolt llarg), i des d'allà manualment vaig anar suprimint les entrades que no volia

tot i així l'Alacarte anava mostrant el mateix (vaig editar l'*applications.menu*, en principi el *settings.menu* diria que és per a l'altre menú), ho vam deixar estar perquè altres coses més importants havíem de fer, apart que una sol·lució parcial és la d'amagar les entrades que no vols

però el que em va sorprendre més de tot és que en el directori es es desen les definicions dels menús (~/.config/menus) no només es desen els menús, sinó que també es desen uns fitxers *nom_menu*.undo-*numero_incremental* que pel que ara veig es van crear tots fa uns quants mesos, no se si atribuir-ho a l'especificació que especifiqui (valgui la redundància) com desar les disposicions anteriors per tornar a l'estat anterior, o bé, que sigui per culpa de l'Alacarte
