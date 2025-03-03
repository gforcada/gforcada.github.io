Title: L'XSLT és útil: Deliverance
Date: 2009-11-24 10:46
Author: admin
Category: General
Tags: consells, Deliverance, xslt
Slug: lxslt-es-util-deliverance
Status: published

Des de que fa molt de temps es va començar a parlar de l'[XML](http://en.wikipedia.org/wiki/XML "Article de la Wikipedia anglesa sobre el format de fitxer XML") i l'[XSLT](http://en.wikipedia.org/wiki/XSLT "Article de la Wikipedia anglesa sobre el format de fitxer XSLT") com a la panacea de la descripció ordenada de contingut i una descripció ordenada de les transformacions d'aquests continguts respectivament que tot i veure aplicacions que utilitzaven XSLT mai no li havia acabat de trobar massa la gràcia.

Ara però, i gràcies a que estic treballant en un projecte amb [Plone](http://www.plone.org/ "Lloc web del projecte de gestor de continguts en línia Plone") que n'hi he vist el gran potencial: [**Deliverance**](http://deliverance.openplans.org "Lloc web del Deliverance un proxy que et permet aplicar transformacions XSLT a pàgines web").

El Deliverance, ras i curt és un *proxy* ((Servei intermediari en aquest cas? Ja que es tracta de programari i no maquinari)) que amb una colla de regles ((Molt poques realment, quatre contades)) li apliques transformacions a qualsevol pàgina web.

D'aquesta manera pots tenir un dissenyador que no sàpiga res ((Ni ho necessiti que és el més important)) sobre el [CMS](http://en.wikipedia.org/wiki/Content_management_system "Article a la Wikipedia anglesa sobre els sistemes gestors de continguts") en que estàs treballant. Llavors per unir el disseny en HTML del dissenyador i les personalitzacions i els continguts  que s'han creat dins del CMS s'ajunten amb el Deliverance. Amb unes quantes regles senzilles li vens a dir "aquest bloc que surt a la dreta posa'l a l'esquerra amb aquests estils".

A més a més, el Deliverance és independent del CMS en el que treballes, ja que el pots ficar enmig de l'usuari i el CMS de manera que els desenvolupadors no han de remenar res de disseny ni presentació i els dissenyadors només s'han de concentrar en fer els dissenys en HTML+CSS+JavaScript.
