Title: git show -3
Date: 2011-02-10 15:23
Author: admin
Category: General
Tags: consells, git, terminal
Slug: git-show-3
Status: published

[<img src="./wp-content/uploads/2009/03/git-logo.png" title="git-logo" class="alignright size-full wp-image-540" width="73" height="28" />](http://gil.badall.net/wp-content/uploads/2009/03/git-logo.png)L'opció *show* del [git](http://git-scm.com/ "Pàgina web del git, el programa de control de versions distribuït") serveix per, tal com indica el nom, mostrar diverses coses, entre elles, i en el 99% dels casos, serà veure els commits ja fets.

Per exemple amb "**git show**" es mostrarà el *diff* de l'últim *commit*.

Per sort, com totes les ordres de git tenen moltíssimes variants, de manera que per exemple amb el títol de l'entrada "**git show -3**" el que farem es veure els tres últims *commits* per ordre cronològic invers (l'últim primer).

També podem afegir-hi el paràmetre *--stat* que permet mostrar un llistat de quins fitxers s'han canviat, de manera que es te una visió molt més ràpida del que s'ha fet en el canvi sense entrar en els detalls del *diff* com a tal.

Amb **git show --help** teniu tota la resta d'informació per si necessiteu fer altres coses :)
