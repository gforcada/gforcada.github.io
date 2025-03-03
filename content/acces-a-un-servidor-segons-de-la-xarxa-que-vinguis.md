Title: Accés a un servidor segons de la xarxa que vinguis
Date: 2010-05-15 14:06
Author: admin
Category: General
Tags: servidor badall, ssh
Slug: acces-a-un-servidor-segons-de-la-xarxa-que-vinguis
Status: published

[<img src="./wp-content/uploads/2007/11/openssh_logo.png" title="logotip de l&#39;Openssh" class="alignright size-full wp-image-225" width="194" height="191" />](http://gil.badall.net/wp-content/uploads/2007/11/openssh_logo.png)Si tens un servidor que està a la xarxa local amb alguns serveis a Internet evidentment el primer que has de fer és no permetre que l'usuari root es connecti per ssh de manera que el més còmode és anar al fitxer /etc/ssh/sshd_config i afegir-hi la línia ((També és molt útil afegir la línia "PasswordAuthentication no" per no permetre connexions que s'autentiquin amb contrasenya, sinó que ho hagin de fer per clau pública-privada)):

> PermitRootLogin no

Que és força explicativa per si mateixa :D

Ara bé, si com deia el servidor és en una xarxa local i vols connectar-t'hi com a root directament (per exemple per fer una còpia de fitxers) la línia de sobre no ens ho permet.  En aquest cas la línia següent és la útil:

> AllowUsers root@192.168.1.\* USUARI1@\* USUARI2@\*

D'aquesta manera root només podria accedir des de la xarxa local (qualsevol IP de la xarxa *192.168.1.\**) i només els usuaris *USUARI1* i *USUARI2* podrien accedir des de qualsevol IP.

Realment els de [OpenSSH](http://www.openssh.com/ "Pàgina oficial del programa OpenSSH") han fet (i estant millorant) un programa excel·lent!
