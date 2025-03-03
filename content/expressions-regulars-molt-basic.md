Title: expressions regulars (molt bàsic)
Date: 2007-11-24 03:20
Author: admin
Category: General
Tags: awk, expressions regulars, GNOME traduccions, sed, vim
Slug: expressions-regulars-molt-basic
Status: published

estic traduint el <a href="http://l10n.gnome.org/module/goffice" target="_blank" rel="noopener">goffice</a> (o almenys intentant-ho :) i com que hi havia algunes cadenes de comentaris que em molestaven i el fitxer era molt llarg és difícil fer-ho a mà anar repassant visualment el fitxer

de manera que m'he recordat que hi ha les <a href="http://ca.wikipedia.org/wiki/Expressions_regulars" target="_blank" rel="noopener"><em>expressions regulars</em></a>! així que com que la meva memòria és molt molt dolenta he buscat per Internet fins que he arribar a un <a href="http://www.grymoire.com/Unix/Regular.html#uh-2" target="_blank" rel="noopener">quadre resum</a> que m'ha dit tot el que necessitava:

**^#\$**

i amb això el que fem és buscar totes les línies en que comencin (ho indica el ^) per \# i acabin (ho indica el \$) també amb \#

així que he obert el <a href="http://www.vim.org" target="_blank" rel="noopener">vim</a>, li he posat l'expressió regular i després d'una combinació de *dd* (eliminar la línia on estàs) i *n* (anar a la pròxima ocurrència de la cerca) ja tenia el fitxer net :D

suposo que això també es podia haver fet amb el <a href="http://en.wikipedia.org/wiki/Sed" target="_blank" rel="noopener">sed</a> o l'<a href="http://en.wikipedia.org/wiki/Awk" target="_blank" rel="noopener">awk</a> (encara no entenc quina diferència hi ha entre l'un i l'altre però vaja)
