Title: les setmanes comencen dilluns
Date: 2009-05-07 10:27
Author: admin
Category: General
Tags: evolution, gentoo, GNOME, locale
Slug: les-setmanes-comencen-dilluns
Status: published

<img src="./wp-content/uploads/2007/11/glogo-small.png" title="logotip de gentoo" class="alignright size-full wp-image-224" width="146" height="149" alt="logotip de gentoo" />Des de que tinc el portàtil nou i que hi vaig posar [Gentoo](http://www.gentoo.org/ "Lloc web de la distribució Linux Gentoo") tot ha anat força bé, almenys amb temps i una canya havia aconseguit que el servidor d'X funcionés (com que el portàtil porta una de les targetes gràfiques d'Intel noves no hi havia els drivers en el [Portage](http://en.wikipedia.org/wiki/Portage_(software) "Article de la Wikipedia sobre el Portage") normal).

L'únic defecte que no havia aconseguit solucionar era que tot i que el calendari de l'[Evolution](http://projects.gnome.org/evolution/ "Pàgina web del projecte de suite de correu i calendari Evolution") ja em marcava correctament com a inici de setmana el dilluns (es pot configurar a través de les preferències) el calendari del quadre (el que et surt quan fas clic a l'hora) em continuava mostrant el diumenge com a dia d'inici.

Tot i que en principi pels [fòrums de Gentoo](http://forums.gentoo.org/ "Fòrums de la distribució Gentoo Linux") es deia que el quadre feia cas a la configuració de l'Evolution resulta que no (pendent d'emplenar un bug per això).

De manera que avui, cansat de veure els diumenges al principi he agafat el toro per les banyes, m'he desplaçat amb un terminal fins a */usr/share/i18n/locales* i allà ho he solucionat :)

El problema és que el locale ca_ES li faltaven les línies (tretes del locale fr_FR):

    first_weekday 1
    first_workday 1
    week 7;19971201;4

Un cop posat això només ha fet falta fer un *locale-gen* (com a root) i reiniciar, ja que tancar la sessió i tornar-la a iniciar sembla que no ha tingut prou efecte (els locales es carreguen a memòria en la seqüència d'iniciació de l'ordinador).

També haig d'emplenar un bug per això :)
