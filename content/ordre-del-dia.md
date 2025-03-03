Title: ordre del dia
Date: 2008-02-19 00:04
Author: admin
Category: General
Tags: consells, terminal, xargs
Slug: ordre-del-dia
Status: published

una de tapes ... vull dir <a href="http://en.wikipedia.org/wiki/Xargs" target="_blank" rel="noopener"><strong>xargs</strong></a>!

no us heu trobat mai amb la necessitat de passar-li a una ordre el resultat d'una altra? i és que l'xargs l'únic que fa és passar com a arguments el que rep per l'entrada

a vegades amb l'accent tancat en teniu prou, però si no és el cas teniu l'xargs :)

amb aquesta ordre podeu, per exemple, seleccionar totes les imatges que acabeu d'importar i que estan en un directori per moure-les a un altre:

ls DCIM00\*.jpg \| xargs mv {} ~/Imatges/carpeta_nova

aquí seleccionem les imatges que volem amb *ls DCIM00\*.jpg*, redirigim la sortida de l'*ls* a l'entrada de l'*xargs* que al seu moment ho reenvia com a arguments de l'ordre *mv* que mourà *{}* (que és el que ens envia l'xargs) a *~/Imatges/carpeta_nova*

el {} a vegades no cal, si les volguéssim suprimir només ens hauria calgut fer *ls \*.jpg \| xargs rm* , però l'xargs ens dóna la possibilitat d e poder ubicar els paràmetres que volem passar a l'ordre de la manera que volem

fins i tot és tant intel·ligent que si la llista d'arguments és massa llarga la parteix a trossos perquè així no peti l'ordre!
