Title: Commits parcials amb git
Date: 2011-11-09 12:58
Author: admin
Category: General
Tags: consells, git, programació
Slug: commits-parcials-amb-git
Status: published

[<img src="http://gil.badall.net/wp-content/uploads/2009/03/git-logo.png" title="git-logo" class="size-full wp-image-540 alignright" width="73" height="28" />](http://gil.badall.net/wp-content/uploads/2009/03/git-logo.png)No us ha passat alguna vegada que mentre esteu escrivint alguna funció nova us adoneu que en una altra funció li falla alguna cosa? Llavors què feu? Un *git stash* abans de fer cap canvi a l'altre mètode i un cop el teniu arreglat un *git stash pop*?

**Ja no cal!**

Sabia que es podia fer però mai m'havia aturat a mirar com es feia:

    git add -p

Amb aquesta ordre (i si voleu el fitxer o fitxers) **afegireu a l'índex les parts del fitxer** que vulgueu. D'aquesta manera si teniu dues parts modificades del codi en un mateix fitxer (la funció que estàveu fent i les quatre línies per arreglar un altre funció) no us cal fer cap cosa estranya per afegir només una part del fitxer, res de fitxers temporals, ni branques, ni deixar coses al porta-retalls, etc etc, senzillament fer una addició de pedaços (d'aquí ve el -p) .

Senzill i MOLT útil. Més de dues, tres i quatre vegades m'hagués estalviat una bona estona d'anar creant fitxers, deixant coses sense desar, etc etc si hagués sabut aquesta opció del *git add* :)
