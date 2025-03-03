Title: instal·lar un servidor de jabber a Debian
Date: 2007-10-26 21:32
Author: admin
Category: General
Tags: debian, guifi, jabber, servidor proxy
Slug: instal%c2%b7lar-un-servidor-de-jabber-a-debian
Status: published

no ho he fet mai, així que segurament qualsevol que ho hagi fet em dirà que ho faig malament (o sigui, comenteu les errades si us plau)

introducció:

el <a href="http://www.jabber.org" target="_blank" rel="noopener">jabber</a> és un protocol de missatgeria instantània lliure que a més a més és fàcilment replicable (amb lo que pots tenir el teu propi servidor de missatgeria) i a més és altament configurable i pot fer de passarel·la cap a altres servidors amb el qual no et quedes aïllat (això no se si m'ho he tret de la màniga però diria que sí oi?) així que com que és útil el posaré a un dels molts servidors de <a href="http://guifi.net" target="_blank" rel="noopener">guifi</a> (de fet ja hi ha altres servidors de jabber a guifi)

comencem:

- instal·lem el <a href="http://www.debian.org" target="_blank" rel="noopener">Debian</a>
- obrim el <a href="http://www.nongnu.org/synaptic/" target="_blank" rel="noopener">Synaptic</a> o des del terminal i instal·lem el paquet «jabber» i les seves dependències
- editem el fitxer principal de configuració del jabber que es troba a /etc/jabber/jabber.xml
  - busquem on posa \<host\> i posem el nom que volguem al servidor (estil jabber.badall.net)
- en <a href="http://crysol.inf-cr.uclm.es/node/558" target="_blank" rel="noopener">aquesta pàgina</a> ens diuen que hem de crear el directori /var/lib/jabber/\<host\> (on \<host\> és el host que hem posat abans)
- l'engeguem amb */etc/init.d/jabber start*

i ja està! en principi no fa falta res més :) ja tindreu un servidor de missatgeria funcionant i a més lliure :)

en la mateix pàgina que he comentat abans expliquen com afegir-hi SSL (seguretat) al jabber, així que si sabeu llegir la llengua de Cervantes ho podreu fer :)

nota: no he pogut fer tots els passos jo mateix perquè no ser el domini que tindrà aquest servidor, de manera que espero que això funcioni quan estigui tot fet i així em servirà per a configurar-lo quan estigui en el seu lloc definitiu i amb el domini concretat :)
