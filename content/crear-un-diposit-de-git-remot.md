Title: crear un dipòsit de git remot
Date: 2009-10-25 10:19
Author: admin
Category: General
Tags: consells, git, servidor badall
Slug: crear-un-diposit-de-git-remot
Status: published

<img src="./wp-content/uploads/2009/03/git-logo.png" title="git-logo" class="alignright size-full wp-image-540" width="73" height="28" alt="git-logo" />Ara que el [git](http://git-scm.com/ "Lloc web del projecte git, un sistema de control de revisions de fitxers distribuït") s'utilitza [a](http://git.kernel.org "Lloc web pel servidor de git per al sistema operatiu Linux") [molts](http://git.gnome.org "Lloc web pel servidor de git per al projecte GNOME") [projectes](http://cgit.freedesktop.org/ "Lloc web pel servidor de git per als projecte de Freedesktop") [importants](http://git.debian.org/ "Lloc web pel servidor de git per als projecte de Debian") va bé saber com muntar-se el teu propi servidor de git.

A grans trets són 3 pasos diferenciats: crear el dipòsit en el servidor, iniciar el dipòsit en el servidor local i finalment com s'utilitza en un ordinador qualsevol.

## Crear el dipòsit en el servidor

Creem un directori ((a on ens sembli del sistema de fitxers, l'únic en que afecta és en l'URL que ens quedarà pera  poder-hi accedir)) i hi entrem:

>     mkdir /home/git/DIPOSIT.git
>     cd /home/git/DIPOSIT.git

Iniciem el dipòsit de git:

>     git --bare init

Amb això ja tenim creat un dipòsit de git apunt per a que s'hi enviïn els primers canvis

## Crear un dipòsit local per a iniciar el dipòsit del servidor

Creem un directori on  ens sembli i hi entrem:

>     mkdir ~/Escriptori/DIRECTORI
>     cd ~/Escriptori/DIRECTORI

Iniciem el dipòsit:

>     git init

Afegim els fitxers que volem que estiguin en el dipòsit i un cop ja hi són tots:

>     git add -A ((fins ara no m'havia adonat que era en majúscula))
>     git commit -a -m"Primer commit"

Un cop ja tenim els fitxers li diem quin és el dipòsit remot on s'hauran d'enviar:

>     git remote add origin ssh://USUARI@servidor/home/git/DIPOSIT.git

Enviem els canvis que ja hem fet:

>     git push origin master

I amb això ja tenim un dipòsit de git iniciat en el servidor i amb els continguts que hi acabem d'enviar. Aquest directori que hem creat en aquest segon pas es pot esborrar.

## Clonar el dipòsit en remot

El pas més curt i més coneguts per tothom:

>     git clone ssh://USUARI@servidor/home/git/DIPOSIT.git

I ja podem fer públic l'URL per a accedir als dipòsits a qualsevol que tingui accés ((em falta mirar com s'ha de fer per permetre també l'accés a través d'HTTP sense necessitar un usuari en el servidor, alguna idea/web on s'expliqui?)).
