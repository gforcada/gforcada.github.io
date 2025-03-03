Title: virtualbox - compartir carpetes
Date: 2008-05-20 02:51
Author: admin
Category: General
Tags: consells, virtualbox
Slug: virtualbox-compartir-carpetes
Status: published

<img src="http://gil.badall.net/wp-content/uploads/2008/03/vbox.png" data-align="right" alt="logo del virtualbox" /><a href="?p=313" target="_blank" rel="noopener">Ja fa temps</a> que el vaig començar a fer servir per virtualitzar el Windows. És molt senzill i ràpid, es segueix un petit auxiliar i ja està tot apunt. Poses el cd (o seleccionar una imatge ISO que ja tinguis al disc dur) i comences a instal·lar el sistema operatiu.

 

Ara bé, amb això no en tenia prou, necessitava poder compartir documents entre el sistema operatiu amfitrió i el virtualitzat, així que vaig buscar una mica per Internet i resulta que és igual de fàcil:

 

- Un cop tens la màquina engegada vas al menú Dispositius → Instal·la les Guest Additions
- Es baixarà una petita imatge ISO que després es muntarà al Windows\[1\] i s'obrirà l'instal·lador
- Segueixes l'auxiliar i reinicies \[2\]
- Abans de tornar a engegar la màquina vas a les opcions de la màquina virtual i li dius les carpetes que vols compartir
- Engeges la màquina virtual i un cop està engegat vas al terminal i hi escrius: "net use x: \\vboxsvr\\carpeta" on \$carpeta és el nom de la carpeta que li has donat en el punt anterior\[3\]

Fent-ho així tindreu una unitat de xarxa muntada a la lletra x: si voleu compartir més carpetes repetiu els dos últims punts tantes vegades com faci falta, canviant el \$carpeta i la x: per el nom de la carpeta i una lletra d'unitat lliure clar.

 

\[1\] Diria que només es per Windows les Guest Additions. Les distribucions de Linux que he provat no m'hi he entretingut a mirar com compartir carpetes

\[2\] No n'estic segur si cal reiniciar, però sent Windows segurament serà que si :)

\[3\] Sobretot poseu l'espai entre x: i \\vboxsrv... que sinó no funcionarà
