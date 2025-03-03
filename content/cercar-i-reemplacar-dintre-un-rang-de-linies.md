Title: cercar i reemplaçar dintre un rang de línies
Date: 2009-07-25 22:50
Author: admin
Category: General
Tags: consells, terminal, vim
Slug: cercar-i-reemplacar-dintre-un-rang-de-linies
Status: published

<img src="./wp-content/uploads/2007/12/vimlogo.png" title="logotip del vim" class="alignright size-full wp-image-251" width="48" height="48" alt="logotip del vim" />El [Vim](http://www.vim.org/ "Pàgina web del Vim") et permet entre moltes altres coses fer cerques i reemplaçaments:

>     :s/cerca/reemplaç/g

Si volem fer el canvi a tot el fitxer només hem d'afegir un % al principi:

>     :%s/cerca/reemplaç/g

Però si el que volem és fer-ho dintre un rang de línies només cal que les especifiquem:

>     :8,19s/cerca/reemplaç/g

Ja feia dies que l'havia trobat i utilitzat, però avui l'he tornat a necessitar i ja no me'n recordava, de manera que a veure si escrivint-ne una entrada al bloc se'm queda més :)
