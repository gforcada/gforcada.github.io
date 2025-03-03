Title: llenguatge de gràfics
Date: 2010-01-03 20:39
Author: admin
Category: General
Tags: consells, gràfics, inkscape, llenguatge dot, programació, programari lliure
Slug: llenguatge-de-grafics
Status: published
Attachments: wp-content/uploads/2010/01/dependencies.png

Llegint [la documentació](http://library.gnome.org/devel/jhbuild/unstable/command-reference.html.en "Documentació del JHBuild a library.gnome.org") del [JHBuild](http://live.gnome.org/Jhbuild "Pàgina al wiki del GNOME sobre el JHBuild") ((Programa per a compilar el [GNOME](http://www.gnome.org "Pàgina web del projecte d'escriptori lliure GNOME") des dels dipòsits de codi font)) he vist que pots mirar les dependències que tenen cada programa des del propi terminal o generar un gràfic que ho mostri, per exemple les dependències de l'[Epiphany](http://projects.gnome.org/epiphany/ "Pàgina web del navegador web específic pel GNOME Epiphany") són:[<img src="http://gil.badall.net/wp-content/uploads/2010/01/dependencies-240x300.png" title="dependencies" class="aligncenter size-medium wp-image-781" width="240" height="300" />]({static}wp-content/uploads/2010/01/dependencies.png)

Resulta que aquest gràfic tant ben fet es fa amb un llenguatge de programació anomenat [DOT](http://en.wikipedia.org/wiki/DOT_language "Entrada a la wikipedia anglesa sobre el llenguatge de generació de gràfics DOT"). La sintaxi és ben senzilla i la facilitat de creació de gràfics és impresionant (només cal mirar els exemples de la Wikipedia).

La genialitat de la implementació que en fa el [Graphviz](http://en.wikipedia.org/wiki/Graphviz "Entrada a la wikipedia sobre el Graphviz") és que no només et treu .jpg o .png sinó que a més a més et pot treure .svg de manera que amb dos minuts pot definir el gràfic amb llenguatge DOT i després et pots estar l'estona que faci falta retocant-lo amb l'[Inkscape](http://www.inkscape.org/ "Pàgina web del projecte de creació d'un editor de gràfics vectorials Inkscape").

Em sembla que a partir d'ara quan hagi de fer gràfics obriré el terminal en comptes d'un editor d'imatges o de vectors :D
