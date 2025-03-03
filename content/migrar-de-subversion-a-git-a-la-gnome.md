Title: migrar de subversion a git a-la-GNOME
Date: 2010-03-30 14:25
Author: admin
Category: General
Tags: feina, git, GNOME, svn
Slug: migrar-de-subversion-a-git-a-la-gnome
Status: published

[<img src="./wp-content/uploads/2009/03/git-logo.png" title="git-logo" class="alignright size-full wp-image-540" width="73" height="28" />](./wp-content/uploads/2009/03/git-logo.png)Avui al final m'he decidit a fer la migració d'algunes coses que tenim encara a la feina que estan amb [subversion](http://subversion.tigris.org/ "Lloc web del programa de control de versions subversion") i passar-les a [git](http://git-scm.com/ "Lloc web del programa de control de versions git").

Ja feia uns dies havia trobat una petita [guia per fer la migració](http://www.jonmaddox.com/2008/03/05/cleanly-migrate-your-subversion-repository-to-a-git-repository/ "Entrada en un bloc que parla sobre com fer una migració de subversion a git") ((De fet ja ho havia comentat per [identi.ca](http://identi.ca/gforcada "El meu compte d'identi.ca") :D)), però avui quan m'hi he posat m'he trobat que no em funcionava tal com jo volia.

No és que el repositori de git no el deixés funcionant correctament, sinó que com que tot i que sigui un scm descentralitzat tenim un servidor on hi ha el codi, etc etc no deixava el repositori en el mateix format.

Després de donar-hi unes quantes voltes m'he adonat que el que estava intentant fer era migrar de subversion a git amb els mateixos propòsits i casos d'ús que el GNOME, així que després de buscar una mica he arribat a [la guia de migració del GNOME](http://live.gnome.org/GitMigration "Guia de migració del GNOME de subversion a git") que m'ha portat a [una pàgina personal en el wiki del GNOME](http://live.gnome.org/JohnCarr/Git "Pàgina personal en el wiki del GNOME amb informació sobre la conversió de repositoris de subversion a git") on s'explica com fer el canvi de format dels repositoris.

I ara sí, ja puc clonar els repositoris del servidor amb total llibertat :)

Pels curiosos, aquest és l'*script* que he utilitzat (un mix de les dues solucions apuntades abans):

> mkdir *NOM-REPOSITORI*.git  
> cd *NOM-REPOSITORI*.git  
> git --bare init  
> git --bare svn init *https://servidor.codi.org/subversion/REPOSITORI* --no-metadata  
> git config svn.authorsfile /git/users.txt**\***  
> git --bare svn fetch

**\*** S'ha de crear un fitxer amb una línia per autor a l'estil: nom.usuari = Nom Real \<correu@electronic.org\>

P.D. Tot buscant informació sobre la migració i tot plegat he arribat a una entrada d'un bloc on hi havia la frase *"You don't branch because you don't use git"* ((No crees branques perquè no utilitzes git)) i la veritat és que té molta raó la frase, el canvi de subversion a git, entre moltes d'altres millores és que hi ha gestió de branques i no una simple recreació d'arbres de directoris sense cap mena de control per part del sistema de control de versions, a veure com em va!
