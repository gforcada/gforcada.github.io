Title: Permisos per compartir un repositori de git
Date: 2010-04-09 10:48
Author: admin
Category: General
Tags: consells, git
Slug: permisos-per-compartir-un-repositori-de-git
Status: published

[<img src="./wp-content/uploads/2009/03/git-logo.png" title="git-logo" class="alignright size-full wp-image-540" width="73" height="28" />](http://gil.badall.net/wp-content/uploads/2009/03/git-logo.png)Un dels problemes de tenir un repositori en un servidor central és com de costum el tema dels permisos, per una banda has de tenir els usuaris creats en local, afegir-los en el mateix grup perquè cadascú pugui accedir als repositoris i finalment un cop està tot apunt tens el problema (amb solució!) de que quan algú fa un commit la resta no en poden fer ja que s'han canviat els permisos.

A primer cop d'ull penses que això amb un *hook* de git i un script que faci un *chown* ja n'hi pot haver prou, després ho rumies una mica més i penses que no hauria de ser tant complicat i arribes a la idea que l'*umask* serà el teu amic ... però al final cerques una mica per Internet i et [trobes amb una solució](http://moserei.de/index.php/58/shared-git-repo-ssh-umask-problems/comment-page-1 "Entrada d'un bloc on es comenta com resoldre el tema de permisos en un repositori git compartit") molt més elegant:

> \$ git repo-config core.sharedRepository true

Amb aquesta senzilla ordre executada per a tots i cadascun dels repositoris que vulguis compartir entre més d'un desenvolupador i llestos, a programar que és el que ens agrada.
