Title: Tirar enrere commits locals en git
Date: 2009-08-09 21:47
Author: admin
Category: General
Tags: git, GNOME traduccions
Slug: tirar-enrere-commits-locals-en-git
Status: published

<img src="./wp-content/uploads/2009/03/git-logo.png" title="git-logo" class="alignright size-full wp-image-540" width="73" height="28" alt="git-logo" />Quan esteu treballant en una traducció i potser esteu a mig fer-la potser us ha passat que us comenten o us adoneu de la manera que sigui que hi ha noves cadenes o se n'han canviat algunes, de manera que us cal actualitzar el codi per a poder després actualitzar la traducció.

Si esteu amb [Git](http://en.wikipedia.org/wiki/Git_(software) "Pàgina a la Wikipedia sobre Git") com a control de versions el que aniríeu a fer és fer un **git pull** per a actualitzar el codi, però ràpidament us adonareu que no podeu, ja que us dirà que hi ha fitxers els canvis dels quals no estan registrats (no s'ha fet el commit) en el git.

Al tractar-se d'una traducció, la qual no té massa sentit fer-ne diferents commits per fer-ne la traducció sembla que perdem flexibilitat ...

Doncs per sort no! (i perdó per la llarga introducció :D

El truc està en que es fa un commit local (sense enviar-lo al servidor central), després actualitzem normalment amb git pull i finalment fem:

> git reset --mixed HEAD^

Amb el git reset podem canviar l'estat del cap actual, d'aquesta manera amb l'ordre de sobre aquesta línia el que li estem dient és que desfaci el commit però que deixi aplicats els canvis de manera que només haguem de fer el commit de nou i pujar-ho.
