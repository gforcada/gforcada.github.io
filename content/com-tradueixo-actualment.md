Title: com tradueixo actualment
Date: 2010-09-24 11:27
Author: admin
Category: General
Tags: consells, GNOME traduccions, Softcatalà, traduccions
Slug: com-tradueixo-actualment
Status: published

Avui((Aprofitant que és festa major a Barcelona)) m'he posat a traduir els mòduls del GNOME en els quals estic com a últim traductor.

Després de fer ja uns quants mòduls he trobat que el cicle de treball que utilitzava m'era molt còmode i de nou((Ja vaig [parlar-ne fa un temps](http://gil.badall.net/2007/06/01/com-tradueixo/ "Entrada al bloc en que comentava quin cicle de treball utilitzar per ajudar en els projectes de traducció de Softcatalà") de com posar-se a traduir)) el documento a veure si algú en pot treure alguna cosa útil i aprofitar-ho i de pas a veure si [algú també s'anima](http://softcatala.cat/planeta "Planeta Softcatalà, on es publiquen les entrades al bloc de diversos membres de Softcatalà") a publicar el seu cicle.

**Disposició de treball**

Com em van dir fa un temps: això de treballar amb dues pantalles enganxa,  després de provar-ho ja no podràs tornar a treballar amb una sola!

Així que amb la pantalla del portàtil i l'externa tinc:

- Dos terminals (un per la traducció activa i l'altre per fer consultes a fitxers po d'altres mòduls o traduccions d'altres idiomes del mateix mòdul)
- Navegador amb diverses pestanyes obertes (el [Damned-Lies](http://l10n.gnome.org "Pàgina web del GNOME pensada per als traductors, amb estadístiques i diverses funcions que ajuden al cicle de treball de traducció"), [el recull de Softcatalà](http://www.softcatala.cat/recull.html "Pàgina del recull de termes de Softcatalà"), [Termcat](http://www.termcat.cat "Pàgina web del centre de terminologia de la Generalitat"), la [Wikipedia](http://www.wikipedia.org "Fa falta descripció? :)"), l'[Open-Tran](http://ca.en.open-tran.eu "Pàgina que permet fer cerques per parelles d'idiomes sobre traduccions de projectes lliures") i l'[Optimot](http://optimot.gencat.cat "Portal de la Generalitat que és un aglutinador de coneixement relacionat amb lingüística, criteris, diccionaris, recomanacions ..."))
- Nota del Tomboy amb un resum de les traduccions a fer i llistat de terminologia que vaig descobrint i establint

D'aquesta manera només haig de moure una mica al ratolí i ja tinc el focus en la finestra que vull utilitzar, en tot el matí no he fet servir l'Alt+Tab :)

**Forma de treball**

- Des del terminal actualitzo el git del mòdul que traduiré (canviar de branca si fa falta i tota la pesca)
- Actualitzo la traducció amb un [script](http://gil.badall.net/wp-content/uploads/2010/09/msgstatus "Script que faig servir per actualitzar la traducció") ("*msgstatus ca*")
- Faig la traducció (pas obvi :)
- Reviso els canvis amb el [Meld](http://meld.sourceforge.net/ "Magnífic programa que permet comparar dos o tres fitxers i fins i tot directoris i que permet enviar canvis cap a una o altra direcció") (entre el fitxer ca.git.po que em crea el msgstatus i el fitxer de la traducció acabada ca.po)
- Extrec totes les cadenes del català (amb un altre [script](http://gil.badall.net/wp-content/uploads/2010/09/msgstatus "Script que agafa un fitxer po i en crea un altre on només hi ha el text en català"))
- Amb el fitxer (ca.po.tmp) que em crea l'script anterior li passo el  el verificador ortogràfic ([Hunspell](http://en.wikipedia.org/wiki/Hunspell "Entrada a la wikipedia anglesa sobre el verificador ortogràfic Hunspell"))
- Finalment després de traduir, revisar i passar la verificació ortogràfica pujo el fitxer al Damned-Lies

Espero que us sigui útil!
