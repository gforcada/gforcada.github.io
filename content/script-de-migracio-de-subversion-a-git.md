Title: Script de migració de Subversion a git
Date: 2011-03-07 18:05
Author: admin
Category: General
Tags: git, guifi, programari lliure, svn
Slug: script-de-migracio-de-subversion-a-git
Status: published

[<img src="http://gil.badall.net/wp-content/uploads/2009/03/git-logo.png" title="git-logo" class="alignright size-full wp-image-540" width="73" height="28" />](http://gil.badall.net/wp-content/uploads/2009/03/git-logo.png)Hi ha moltíssimes maneres de passar un repositori Subversion a git.

Ni molt menys és que sigui una tasca complexa, tot depèn de les bones pràctiques que s'hagin dut a terme en el Subversion.

A [guifi.net](http://guifi.net "Pàgina web del projecte guifi.net") hem decidit ((De fet jo ho vaig decidir i ningú s'hi ha oposat de moment)) **canviar del [monolític Subversion de lafarga.cat](http://projectes.lafarga.cat/projects/guifi/scm "Pàgina amb la informació d'accés al subversion de lafarga.cat pel projecte guifi.net") a [git](http://git-scm.com/ "Pàgina del programa de control de versions descentralitzat git")**. De moment ho enviarem a [gitorious.org](http://gitorious.org "Pàgina on es poden allotjar repositoris de git i col·laborar entre diverses persones") ((En concret al projecte [guifi de gitorious.org](http://gitorious.org/guifi "Projecte de guifi a gitorious.org"))), però això és el de menys. Al moment en que canvies a git, pots allotjar el codi allà on vulguis i canviar-ho els dies senars dels mesos parells si vols :)

Com que a lafarga.cat només teníem un sol repositori per el codi hi havia múltiples, **fins a 15!**, repositoris dins del mateix repositori i barrejats en diverses carpetes i demés.

Total, per sort l'historial en aquest cas no era crucial i amb [un script que he creat](http://gil.badall.net/fitxers/guifi_svn2git.sh "Script per clonar el repositori subversion de lafarga.cat, separar-lo per projectes i enviar-lo a gitorious.org") ja s'està pujant el codi a gitorious.org :)

**NOTA:** encara no s'ha decidit una data oficial per abandonar lafarga.cat i abraçar de totes totes el git, serà aviat, esperem.

Els que tingueu ganes de jugar amb el git ((Les [diapositives que vaig utilitzar](http://www.slideshare.net/gilforcada/com-funciona-el-git-guifi "Presentació a slideshare sobre git") l'últim cop que en vaig parlar)) ja no teniu excusa que no hi ha codi real.
