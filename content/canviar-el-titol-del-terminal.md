Title: canviar el títol del terminal
Date: 2010-07-18 10:01
Author: admin
Category: General
Tags: centos, consells, debian, terminal
Slug: canviar-el-titol-del-terminal
Status: published

Resulta que a la feina tenim uns quants servidors virtuals per a diferents propòsits i com que un era amb [CentOS](http://centos.org/ "Pàgina de la distribució GNU/Linux CentOS") i d'altres amb [Debian](http://www.debian.org/ "Pàgina de la distribució GNU/Linux Debian") un dia vaig adonar-me que quan em connectava al CentOS se'm canviava el títol del terminal però en canvi en connectar-me als Debian no.

Així que investigant una mica he descobert que hi ha la variable **PROMPT_COMMAND** que et permet canviar el títol, de manera que per exemple si poses al ~/.bashrc:

> PROMPT_COMMAND='echo -ne "\033\]0;\${USER}@\${HOSTNAME%%.\*}:\${PWD/\$HOME/~}\007"'

Et posarà com a títol el nom d'usuari, l'ordinador on estàs i el camí on estàs actualment.
