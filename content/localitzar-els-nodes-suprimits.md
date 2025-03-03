Title: localitzar els nodes suprimits
Date: 2008-03-19 00:10
Author: admin
Category: General
Tags: consells, guifi, sql
Slug: localitzar-els-nodes-suprimits
Status: published

<img src="./wp-content/uploads/2007/10/logo-guifi.png" data-align="right" alt="logo guifi" />a la barra lateral de l'esquerra de la pàgina de <a href="http://guifi.net" target="_blank" rel="noopener">guifi.net</a> es mostren les estadístiques dels nodes (totals, projectats, funcionant ...) i com que m'atabala molt veure'n que n'hi ha de suprimits però que només és l'estat i que per tant, o bé s'han de suprimir del tot o només deixar-los com a projectats hi ha una petita consulta amb sql que ens resol el dubte de quin node en concret són:

    SELECT id FROM guifi_location WHERE status_flag='Dropped';

Amb això ja sabrem els número de node que ens fa falta posar a http://guifi.net/ca/node/XXX per després suprimir-lo definitivament, canviar-li l'estat o contactar amb el seu creador o últim actualitzador

:)
