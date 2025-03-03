Title: git stash
Date: 2010-04-19 13:34
Author: admin
Category: General
Tags: consells, git, terminal
Slug: git-stash
Status: published

[<img src="./wp-content/uploads/2009/03/git-logo.png" title="git-logo" class="alignright size-full wp-image-540" width="73" height="28" />](http://gil.badall.net/wp-content/uploads/2009/03/git-logo.png)Una de les primeres coses que descobreixes quan utilitzes git és que de la mateixa manera que un mediawiki, per posar un exemple, hi ha mil i una maneres de treballar-hi:

Tot amb branques, arbres remots a github, via pedaços (com se solia anar amb subversion i cvs) ...

De manera que igual com amb un mediawiki el més important és definir una bona guia d'estil, les plantilles i el sistema de categorització, treballant amb el git, el més important és definir dintre de l'equip de treball un bon cicle de treball per tal que no hi hagi *diverges* ...

I és aquí on entra l'ordre **git stash**.

Un exemple ben fàcil: tens canvis a 5 fitxers diferents, fas un commit per a tres d'ells perquè els altres dos encara no estan llestos per enviar.  Si en aquell moment vols fer un *git pull --rebase* perquè el servidor de git és un servidor central i vols agafar els últims canvis i aplicar-hi els teus commits locals a sobre de les últimes actualitzacions, el git no et deixarà fer-ho, ja que hi ha canvis sense estar en un commit.

No pots fer-ne un commit perquè no estan acabats, de manera que el que pots fer és un git stash, que senzillament desa els canvis que no estan a cap commit i et deixa l'arbre sense cap fitxer que no estigui en un commit, de manera que ja pots fer un *git pull --rebase* i si tot va bé un *git push* per enviar els teus commits locals.

Ja només et queda fer un *git stash pop* per recuperar els canvis que tens que no estan a cap commit i continuar treballant tranquilament :)

Evidentment, com tota eina de git, el git stash et permet fer moltíssimes coses més, de fet per tal com es recupera la sessió desada (git stash pop) ja podeu veure que el git stash funciona com una pila, de manera que pots tenir tants stash com necessiteu ((No exempt de perill que després no funcionin sobre el commit en el que esteu treballant)) i aplicar-los a altres branques, o crear branques a partir dels stash, etc etc ...
