Title: directoris d'ús comú
Date: 2008-02-19 14:36
Author: admin
Category: General
Tags: consells, terminal
Slug: directoris-dus-comu
Status: published

avui estic automatitzador :)

si abans feia un <a href="?p=305" target="_blank" rel="noopener">script per a poder baixar el codi font</a> de manera més còmode i així escriure menys ara el que explicaré és pel següent cas:

normalment quan inicieu un terminal us deixa com a *pwd* a *~* però segur que allà no hi teniu directament tot el que voleu, en canvi teniu un altre directori (per exemple *~/gnome/codi*) on hi teniu tot el codi font dels mòduls que us heu baixat amb l'script d'abans :) i per accedir-hi sempre heu de fer un *cd gnome/codi*

doncs bé, hi ha una variable d'entorn que ens permet afegir tants directoris com vulguem en el camí de directoris, altrament dit, que si posem *export CDPATH=\$CDPATH:~/gnome/codi* al nostre *~/.bashrc* a partir de llavors, des de qualsevol directori podrem accedir directament a qualsevol directori de *~/gnome/codi* :)

en vaig sentir a parlar al <a href="http://planet.gnome.org" target="_blank" rel="noopener">planeta GNOME</a> i avui cercant he anat a parar a *<a href="http://www.caliban.org/bash/" target="_blank" rel="noopener">Working more productively with bash 2.x/3.x</a>*, no està gens malament :D
