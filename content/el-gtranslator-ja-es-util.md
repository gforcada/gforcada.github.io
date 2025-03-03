Title: el gtranslator ja és útil!
Date: 2008-01-10 14:25
Author: admin
Category: General
Tags: consells, GNOME, GNOME traduccions, gtranslator, Softcatalà, svn, vim
Slug: el-gtranslator-ja-es-util
Status: published
Attachments: wp-content/uploads/2008/01/gtranslator-logo.png, wp-content/uploads/2008/01/gtranslator.png

<img src="{static}wp-content/uploads/2008/01/gtranslator-logo.png" data-align="right" alt="logotip del gtranslator" />ara mateix estic fent la traducció del manual de la miniaplicació de l'indicador de teclat i com que he trobat una cadena de la interfície que era errònia m'he baixat el codi font del gnome-applets per a poder mirar la cadena i arreglar-la (que també m'ha costat lo seu trobar-la)

com que he vist que li quedaven poques cadenes m'he decidit a acabar-lo, així ja faltarà menys per estar al 100% de cara a d'aquí 2 mesos i 1 dia que sortirà el <a href="http://www.gnome.org" target="_blank" rel="noopener">GNOME</a> 2.22 però m'he trobat amb un problema i es que estava editant amb el <a href="http://www.vim.org/" target="_blank" rel="noopener">vim</a> el fitxer de traducció hi he vist que hi havia els caràcters dels símbols de temperatura per a graus <a href="http://ca.wikipedia.org/wiki/Celsius" target="_blank" rel="noopener">celsius</a> i <a href="http://ca.wikipedia.org/wiki/Fahrenheit" target="_blank" rel="noopener">farenheit</a> i com que no ser com copiar i enganxar (des de teclat) amb el vim ho he deixat en primera instància però després m'he recordat que hi ha uns gallecs (diria) que estan tornat a treballar amb el <a href="http://gtranslator.sourceforge.net/" target="_blank" rel="noopener">gtranslator</a>

una de les novetats que hi ha ara mateix a la branca <a href="http://svn.gnome.org/viewvc/gtranslator/branches/GOBJECT_WORK/" target="_blank" rel="noopener">GOBJECT_WORK</a> és una paleta de caràcters:

[]({static}wp-content/uploads/2008/01/gtranslator.png "gtranslator en funcionament")

[![gtranslator en funcionament](http://gil.badall.net/wp-content/uploads/2008/01/gtranslator.thumbnail.png)]({static}wp-content/uploads/2008/01/gtranslator.png "gtranslator en funcionament")

els observadors també hauran vist que hi ha una pestanya a sota de la llista de cadenes que posa «alternate language» que serveix per tenir un alter fitxer po obert, en principi el mateix que s'està traduint però en un altre idioma, o per exemple, una memòria de traducció (com la de <a href="http://www.softcatala.org/projectes/eines/mt/" target="_blank" rel="noopener">Softcatalà</a>)

encara no n'han fet cap llançament però una de les altres novetats importants (i que en principi ja hi ha a la branca GOBJECT_WORK tot i que no l'he sabut veure com s'activa) és la possibilitat de fer consultes a <a href="http://www.open-tran.eu" target="_blank" rel="noopener">open-tran.eu</a>, un lloc web on es poden consultar <a href="http://open-tran.eu/db.html" target="_blank" rel="noopener">traduccions de diferents projectes de programari</a> lliure (de moment <a href="http://www.gnome.org" target="_blank" rel="noopener">GNOME</a>, <a href="http://www.mozilla.com" target="_blank" rel="noopener">Mozilla</a>, <a href="http://www.kde.org" target="_blank" rel="noopener">KDE</a>, <a href="http://www.debian.org" target="_blank" rel="noopener">Debian</a> i Cor Jousma)

també s'està treballant en un connector a l'estil al que acabo de comentar per al <a href="http://live.gnome.org/TranslationProject/NewStatusPages" target="_blank" rel="noopener">damned-lies</a> (el programari que hi ha darrere <a href="http://l10n.gnome.org" target="_blank" rel="noopener">l10n.gnome.org</a>) la qual cosa permetrà fer consultes només a cadenes del GNOME

el títol de l'entrada tot i així no és per res del que acabo de comentar, sinó que com que un dels motius pels que quan tradueixo ho faig amb el <a href="http://www.gnome.org/projects/gedit/" target="_blank" rel="noopener">Gedit</a> o el vim és que tant el gtranslator o el poedit sempre s'entesten a modificar les referències al codi font de manera que quan acabes de traduir un programa i li fas un *diff* amb la versió anterior per enviar-la a les llistes de <a href="http://www.softcatala.org" target="_blank" rel="noopener">Softcatalà</a> et trobes que el *diff* no serveix per res precisament perquè hi ha tants canvis que no es poden arribar a veure a simple vista els canvis que hagis pogut fer

però almenys amb les quatre cadenes que hi he canviat aquesta vegada ho he comprovat i no ha canviat res de res :)
