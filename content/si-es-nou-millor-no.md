Title: si és nou millor no?
Date: 2009-11-02 21:21
Author: admin
Category: General
Tags: controladors, nouveau, ubuntu, xorg
Slug: si-es-nou-millor-no
Status: published

La [Sílvia](http://silvia.badall.net "Bloc de la Sílvia") porta tot el dia batallant amb la targeta gràfica ((Una Nvidia GeForce FX 5700ve, força vella, res a veure amb GPU modernes)) del seu ordinador de sobretaula que no li dóna més de 800x600 o instal·lant els controladors directament des del web del fabricant 640x480 ((Sí, instal·lant uns controladors suposadament més nous fan que la resolució sigui pitjor!)).

Al final com que ja fa temps que sabia de l'esforç d'alguns hackers per a crear uns controladors lliures per a les targetes gràfiques d'aquesta marca, el [projecte nouveau](http://nouveau.freedesktop.org/wiki/ "Lloc web del projecte nouveau per a crear uns controladors lliures per a les targetes gràfiques de Nvidia"), he decidit provar-ho i ha sigut un plis.

Amb el Synaptic l'hi he instal·lat el controlador i he suprimit els controladors propietaris, he afegit una sola línia al xorg.conf, he reiniciat ((o podia haver matat el servidor d'X i tornar-lo a carregar, que a Linux no cal reiniciar per tot :D)) i amb el fantàstic editor de la configuració de la pantalla del GNOME li he posat la resolució a 1024x768 :)

Una demostració més de que per molt que sigui el maquinari vell i que hi hagi controladors disponibles des del fabricant, resulta que una colla de hackers ho poden (i en aquest cas ho fan) molt millor en quan a satisfacció de l'usuari final!

P.D. Al final entre tantes proves s'ha acabat instal·lant la versió 9.04 en comptes de la 9.10 :D

P.D.2 el comentari de l'entrada anterior ha sigut el nº 200! A veure què tardeu a doblar la xifra ;)
