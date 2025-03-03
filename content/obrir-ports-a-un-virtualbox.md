Title: obrir ports a un Virtualbox
Date: 2009-12-27 17:28
Author: admin
Category: General
Tags: consells, virtualbox
Slug: obrir-ports-a-un-virtualbox
Status: published

*[<img src="./wp-content/uploads/2008/03/vbox.png" title="logo del virtualbox" class="alignright size-full wp-image-314" width="140" height="151" />](./wp-content/uploads/2008/03/vbox.png)Long time no blogging ... anyway!*

Ja fa temps ((De fet ho vaig descobrir a [Openbravo](http://www.openbravo.com "Lloc web d'Openbravo un ERP open source") quan utilitzava les màquines virtuals per fer coses de la feina)) que feia servir unes opcions no tant conegudes del [Virtualbox](http://www.virtualbox.org "Lloc web del projecte Virtualbox una eina per a crear i gestionar màquines virtuals") i que permeten interactuar molt més fàcilment amb la màquina virtual, aquí va l'explicació:

**Problema**: Tinc una màquina virtual amb Virtualbox i vull accedir a algun dels serveis que hi ha en algun port en concret d'aquesta màquina virtual.

**Sol·lució**: Són tres senzilles línies que només has d'anar copiant i enganxant en un terminal cada vegada que facis una màquina virtual nova.

> ﻿# VBoxManage setextradata *NOM_MAQUINA_VIRTUAL* "VBoxInternal/Devices/pcnet/0/LUN#0/Config/guesthttpd/HostPort" 8000  
> \# VBoxManage setextradata *NOM_MAQUINA_VIRTUAL* "VBoxInternal/Devices/pcnet/0/LUN#0/Config/guesthttpd/GuestPort" 80  
> \# VBoxManage setextradata *NOM_MAQUINA_VIRTUAL* "VBoxInternal/Devices/pcnet/0/LUN#0/Config/guesthttpd/Protocol" TCP

Canvieu el "*NOM_MAQUINA_VIRTUAL*" pel nom que li hagueu posat a la màquina virtual. Recordeu que després d'executar aquestes tres ordres haureu d'apagar i tornar a engegar la màquina virtual (no n'hi ha prou en reiniciar-la).

Un cop fet això i amb la màquina engegada de nou només cal que aneu al vostre navegador de l'ordinador amfitrió i poseu la direcció http://localhost:8000 i estareu veient l'Apache de la màquina virtual!

El mateix podeu fer amb l'ssh:

> ﻿# VBoxManage setextradata *NOM_MAQUINA_VIRTUAL* "VBoxInternal/Devices/pcnet/0/LUN#0/Config/ssh/HostPort" 2222  
> \# VBoxManage setextradata *NOM_MAQUINA_VIRTUAL* "VBoxInternal/Devices/pcnet/0/LUN#0/Config/ssh/GuestPort" 22  
> \# VBoxManage setextradata *NOM_MAQUINA_VIRTUAL* "VBoxInternal/Devices/pcnet/0/LUN#0/Config/ssh/Protocol" TCP

Després de apagar i tornar a engegar ja podreu fer un ssh ((ssh -l *USUARI* -p 2222 localhost)) a la màquina virtual.

Entenc que es pot fer amb qualsevol port i que en la cadena "VBoxInternal/Devices/pcnet/0/LUN#0/Config/ssh/\*" només cal canviar l'ssh per ftp o per qualsevol nom arbitrari no repetit, no he trobat cap guia que ho expliqui amb detall (tampoc he buscat molt :D)

Espero que sigui útil!
