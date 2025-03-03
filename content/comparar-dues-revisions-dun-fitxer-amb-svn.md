Title: comparar dues revisions d'un fitxer amb svn
Date: 2008-11-28 14:08
Author: admin
Category: General
Tags: consells, svn
Slug: comparar-dues-revisions-dun-fitxer-amb-svn
Status: published

<img src="./wp-content/uploads/2008/01/subversion.png" title="logotip del Subversion" class="alignright size-full wp-image-271" width="88" height="64" />Quan encara no heu confirmat uns canvis en un fitxer que està versionat amb svn podeu utilitzar l'ordre *svn status* per saber quins fitxers estan modificats i un *svn diff \$nom_fitxer* per veure el canvis respecte l'última vegada que vau actualitzar el dipòsit amb un *svn up* (o un *svn co \$url*).

Ara bé, si acabeu de fer la confirmació (*commit*) i voleu agafar-ne el pedaç per aplicar-lo a una altra branca o enviar-lo a algú com ho podeu fer?

La resposta és senzilla un cop la saps, com de costum :)

Primer feu un *svn log \$nom_fitxer* i aquest us mostrarà les revisions en que heu modificat el fitxer de manera que si les revisions són la 35 i la 44 només heu de fer un:

> **svn diff \$url_fins_al_fitxer@35 \$url_fins_al_fitxer@44**

L'URL del fitxer el podeu trobar fàcilment si feu un *svn info* i afegiu el tros de camí (*path*) fins al fitxer.

Si fóssin dos fitxers diferents, que pel motiu que sigui els heu bifurcat en el propi dipòsit (per dir alguna cosa: script_v1.sh i script_v2.sh) en principi no caldria posar tot l'url, sinó que amb els camis en local i @REVISIÓ ja n'hi hauria prou.

Uff, fins a 6 ordres hem necessitat: svn {stats, diff, up, co, log, info}
