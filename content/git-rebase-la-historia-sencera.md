Title: git rebase: la història sencera
Date: 2010-10-06 20:13
Author: admin
Category: General
Tags: consells, git
Slug: git-rebase-la-historia-sencera
Status: published

## [<img src="./wp-content/uploads/2009/03/git-logo.png" title="git-logo" class="alignright size-full wp-image-540" width="73" height="28" />](./wp-content/uploads/2009/03/git-logo.png)Introducció

Si treballeu amb [git](http://en.wikipedia.org/wiki/Git_%28software%29 "Article de la wikipedia anglesa sobre el sistema de control de versins distribuït Git") ja haureu sentit a parlar de l'ordre *rebase*. Per intentar-ho resumir (( [Hi](http://book.git-scm.com/4_rebasing.html) [ha](http://darwinweb.net/articles/the-case-for-git-rebase) [moltíssima](http://www.eecs.harvard.edu/~cduan/technical/git/git-5.shtml) [lectura](http://www.kernel.org/pub/software/scm/git/docs/git-rebase.html) )):

Suposem que has començat una branca de desenvolupament paral·lela a la branca principal, has fet uns quants commits i al mateix temps la branca principal també evoluciona amb uns quants commits.

En aquell moment les dues branques han divergit (tenen commits diferents) de manera que no pots enviar els canvis d'un  a l'altre de manera automàtica que sinó es perdrien els canvis que ja hi ha fets en l'altre branca.

Si vols integrar els canvis d'una branca a l'altre tens dues sol·lucions:

- merge: **combinar en un sol commit** tots els canvis d'una branca per integrar-los en l'altra.
  - problema: s'ajunta en un sol commit tots els canvis de la branca, de manera que si els canvis són molt invasius és perjudicial a la llarga ja que no tens l'historial real dels commits que van portar a aquest super-commit.
- rebase: *actualitzar* tots els commits de la teva branca perquè utilitzin la nova base de l'altra branca de manera que llavors sí que es puguin aplicar els canvis de forma directe
  - problema: **es reescriu la història** dels commits, ja que si els canvis que comporten la nova base a partir de la qual aplicar els commits toca els mateixos fitxers que els que un ha canviat en la seva branca es modifiquen els commits automàticament.

Una mica enrevessat oi? Mireu [la documentació oficial del git](http://www.kernel.org/pub/software/scm/git/docs/git-rebase.html "Pàgina de la documentació del Git sobre el rebase") sobre el rebase amb tots els dibuixets.

## L'important, el codi

Ara bé, m'he trobat moltíssima documentació explicant **el què**, però no **el com**, així que aquí va una guia ràpida de les ordres per tal de fer un rebase:

    git checkout BRANCH # anem a la branca que volem passar a master
    git rebase MASTER # fem el rebase (si trobem conflictes els anem sol·lucionant)
    git push -f # envies els canvis al servidor (el -f és degut a que forces el push)
    git checkout MASTER # tornem a la branca master
    git pull origin BRANCH # ara ja podem agafar els canvis de la branca BRANCH sense cap problema
    git push # enviem al servidor la branca master amb tots els canvis de la branc BRANCH aplicats

I amb això ja teniu tot el necessari per poder treballar amb branques i fer-ne després *rebase* d'aquestes.

Tingueu en compte el fet aquest de la reescriptura de la història. De per si no és dolent, el principal problema és que si la branca en la que estàs treballant també l'utilitza algú altre, aquest altre tindrà problemes quan torni a fer una actualització del codi.

Si pel contrari treballeu amb aquesta branca únicament vosaltres no tindreu absolutament cap problema i, sens dubte, serà la millor manera de preservar tot els commits i per tant molt més senzill de navegar per l'historial.
