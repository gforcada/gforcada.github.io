Title: mostrar o amagar les traduccions
Date: 2008-02-17 02:23
Author: admin
Category: General
Tags: damned-lies, expressions regulars, GNOME traduccions, javascript, programació
Slug: mostrar-o-amagar-les-traduccions
Status: published

<img src="./wp-content/uploads/2008/01/gnomefoot.png" data-align="right" alt="logotip del GNOME" />després de dinar no sabia què fer i m'ha picat el cuc *hacker* i m'he decidit a tancar el l'errada <a href="http://bugzilla.gnome.org/show_bug.cgi?id=106779" target="_blank" rel="noopener">#106779</a> :)

moltes, moltes, moltes hores després he aconseguit que totes les peces encaixin i ara per fi ja he pogut enviar un <a href="http://bugzilla.gnome.org/attachment.cgi?id=105411&amp;action=view" target="_blank" rel="noopener">pedaç</a> que afegeix la funcionalitat d'amagar o mostrar les traduccions que ja estan al 100%

per fer-lo m'he basat en <a href="http://www.dustindiaz.com/seven-togglers/" target="_blank" rel="noopener">l'enllaç</a> que hi havia en l'últim comentari de l'errada, però el problema era que no s'havia de commutar un o tots els elements de les llistes, sinó que uns i prou

de manera que m'he tirat dels cabells navegant per Internet fins que he trobat una manera fàcil i còmode:

- primer de tot es defineix un identificador a cada una de les dues taules (la de documentació i la de interfície gràfica \[1\])
- seguidament a partir d'aquests identificadors agafes els elements *tr* d'aquestes taules i els passes per un bucle
- en el bucle l'únic que has de fer es comprovar si tenen un identificador que acabi amb -complete\[2\] i si es dóna el cas fer un (obj).style.display = 'none' o (obj).style.display = ''
- evidentment, perquè això funcioni, fa falta posar-hi els identificadors quan es generen les pàgines

tot i que és molt millorable, si s'aplica aviat i es posa en els servidor en producció (el <a href="http://l10n.gnome.org" target="_blank" rel="noopener">l10n.gnome.org</a>) anirà que ni pintat ara que ja falta menys d'un mes per al llançament del <a href="http://live.gnome.org/TwoPointTwentyone" target="_blank" rel="noopener">GNOME 2.22</a> :D

\[1\] realment no caldria fer-ho així i es podria fer directament amb tot el document de cop, però com que les pàgines son prou grosses així la consulta al <a href="http://en.wikipedia.org/wiki/Document_object_model" target="_blank" rel="noopener">DOM</a> es més curta

\[2\] i això és possible gràcies a que disposem d'expressions regulars a <a href="http://en.wikipedia.org/wiki/Javascript" target="_blank" rel="noopener">Javascript</a>!
