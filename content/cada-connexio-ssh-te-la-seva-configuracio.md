Title: cada connexió (ssh) té la seva configuració
Date: 2010-05-28 12:12
Author: admin
Category: General
Tags: consells, ssh
Slug: cada-connexio-ssh-te-la-seva-configuracio
Status: published

[<img src="http://gil.badall.net/wp-content/uploads/2007/11/openssh_logo.png" title="logotip de l&#39;Openssh" class="alignright size-full wp-image-225" width="194" height="191" />](http://gil.badall.net/wp-content/uploads/2007/11/openssh_logo.png)No us heu cansat mai de teclejar ssh *usuari@nom-interminable-de-la-maquina-hi-ha-sobre.domini* ?

Doncs com en tot en el món linux té el seu fitxer de configuració: **~/.ssh/config** (man ssh_config).

És tan senzill com tres línies:

Host *nom-curt*

HostName *nom-del-servidor.com*

User *usuari*

Un cop escrit això de sobre (canviant les cursives clar) ja podreu teclejar *ssh nom-curt* quan en realitat estaríeu teclejant *ssh usuari@nom-del-servidor.com*.

Sembla una petita diferència oi? Però penseu en els casos en que teniu més d'una clau pública (( La de la feina, la del servidor de casa, la del projecte on esteu col·laborant, la d'accés a repositoris de codi ... )) o qualsevol altre opció que heu d'especificar per connexió!

No hi ha dia que em deixi de sorprendre i trobar encara més útil l'[OpenSSH](http://en.wikipedia.org/wiki/OpenSSH "Article de la wikipedia anglesa sobre el programari OpenSSH")!
