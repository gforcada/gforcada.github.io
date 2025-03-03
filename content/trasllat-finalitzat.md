Title: trasllat finalitzat
Date: 2007-05-25 20:25
Author: admin
Category: General
Tags: bloc
Slug: trasllat-finalitzat
Status: published

doncs ja està: ja tinc el bloc mogut al servidor nou (més d’això en un altre moment)

el canvi, com sempre no ha sigut fàcil, apart de que ara funcionarà amb *virtualhosts*, els servidors són diferents, l’URL també, etc etc resulta que el *\[inseriu els renecs preferits\]* del <a href="http://www.wordpress.org" target="_blank" rel="noopener">Wordpress</a> deixa els camins complets a les imatges!

o sigui que si un dia teniu el bloc a /var/www/bloc i després el poseu a qualsevol altre lloc, per exemple /home/gil/bloc ja l’heu cagat, el wordpress ho continuarà buscant a /var/www/bloc, suposava que un sistema de bloc tan utilitzat utilitzaria una variable d’entorn a l’estil \$base_path on tenir-hi el camí base al bloc, i a partir d’aquí reconstruir tots els fitxers

a per cert, l’URL del bloc a partir d’ara serà **http://gil.badall.net** \[1\]

\[1\] el nom del domini es va escollir tot anant cap a la trobada de Softcatalà a les terres de l’Ebre
