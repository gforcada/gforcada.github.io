Title: Crear un dipòsit de Subversion amb accés per http i per ssh
Date: 2008-12-03 02:42
Author: admin
Category: General
Tags: gentoo, git, GNOME, pis de girona, ssh, svn, turing, UdG
Slug: crear-un-diposit-de-subversion-amb-acces-per-http-i-per-ssh
Status: published

<img src="http://gil.badall.net/wp-content/uploads/2008/01/subversion.png" title="logotip del Subversion" class="alignright size-full wp-image-271" width="88" height="64" />A la universitat hem de fer una [màquina de Turing](http://en.wikipedia.org/wiki/Turing_machine "Article de la Wikipedia anglesa on explica què es una màquina de Turing") ([català](http://ca.wikipedia.org/wiki/M%C3%A0quina_de_Turing "Article a la Wikipedia catalana on explica què es una màquina de Turing")) i com que l'hem de fer en grup crec que la millor manera és posar un servidor de [Subversion](http://subversion.tigris.org/ "Lloc web del projecte Subversion, un sistema de control de revisions de fitxers") (hi estic més acostumat, amb [git](http://en.wikipedia.org/wiki/Git_(software) "Article de la Wikipedia anglesa que explica el sistema de control de revisions distribuït git") només he fet "*git clone \$url*").

Així que "*dit i fet*":

- Com que el servidor és un [Gentoo](http://www.gentoo.org "Lloc web de la distribució GNU/Linux Gentoo") [aquesta guia](http://www.rockfloat.com/howto/gentoo-subversion.html "Guia de com instal·lar un servidor de Subversion a una màquina Gentoo") m'ha anat que ni pintat, et descriu els passos per tal de configurar un servidor Subversion a la màquina i com fer per permetre que es pugui accedir en mode lectura per web i els usuaris que vulguis en mode lectura i escriptura.
- Com que a més vull donar accés per [SSH](http://ca.wikipedia.org/wiki/SSH "Article de la Wikipedia anglesa on explica què és l'SSH") (ja que hi estic acostumat del [GNOME](http://www.gnome.org "Lloc web del projecte GNOME")) només m'ha fet falta seguir aquesta [altra guia](http://svn.haxx.se/dev/archive-2004-03/0253.shtml "Guia per a configurar l'accés a dipòsits Subversion amb ssh") que ho deixa força clar :)
- Però aquí no acaba tot, com que la xarxa que tinc muntada al pis de Girona és una mica peculiar, el port de l'SSH no és el predeterminat (22), de manera que aquesta [altra guia](http://articles.slicehost.com/2007/9/5/using-ssh-with-svnserve "Guia de com fer-ho per connectar-te per SSH a un dipòsit Subversion si no fa servir el port predeterminat") m'ha resolt els dubtes.

Ara sí, llestos :)
