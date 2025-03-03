Title: Algú coneix en Joan Carles Soler?
Date: 2009-06-03 11:08
Author: admin
Category: General
Tags: bugs, gentoo, glibc, locale
Slug: algu-coneix-en-joan-carles-soler
Status: published

Ahir per fi vaig tenir els 5 minuts que no tens res a fer i penses en emplenar informes d'errades i vaig emplenar el de que el locale ca_ES comença les setmanes en diumenge en comptes de dilluns.

Resulta que els de [Gentoo](http://bugs.gentoo.org/show_bug.cgi?id=272297 "Informe d'error en el bugzilla de Gentoo sobre el dia d'inici de la setmana en el locale ca_ES") m'han dit que això s'ha d'informar *upstream* i cap allà me n'he anat.

Per sorpresa meva ja hi havia [un informe](http://sources.redhat.com/bugzilla/show_bug.cgi?id=6770 "Informe d'errada al bugzilla de la glibc") (des del juliol de l'any passat) i en el qual es demana que per fer el canvi esmentat es tingui consentiment de l'autor original, i aquí és on ve la meva crida:

**Algú coneix en Joan Carles Soler (amb adreça joan.carles *arroba* uv *punt* es)?**

Avui al matí he enviat un correu en aquest correu electrònic però encara sense resposta.

Cercant per Google sembla que col·laborava a Debian i fins i tot a traduir el [KDE](http://cat.kde.org "Pàgina web del KDE al català") al català, a veure si així resulta més fàcil arribar a ell i solucionar-ho.

Mirant el portàtil de la Sílvia he vist que el seu locale ca_ES ja estava arreglat amb un comentari FIXME i mirant els diff.gz de [Debian](http://packages.debian.org/sid/libc6-dev "Detalls del paquet libc6-dev a Debian") i [Ubuntu](https://launchpad.net/ubuntu/jaunty/+source/glibc/2.9-4ubuntu6 "Detalls del paquet glibc a Ubuntu") tots dos porten el pedaç que fa que el dilluns sigui el primer dia de la setmana.
