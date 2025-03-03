Title: múltiples constructors en php
Date: 2007-06-18 21:55
Author: admin
Category: General
Tags: php, programació, programació web
Slug: multiples-constructors-en-php
Status: published

doncs es veu que no es pot, així de ras i curt

la idea dels <a href="http://en.wikipedia.org/wiki/Constructor_overloading" target="_blank" rel="noopener">constructors múltiples</a> és que quan construeixes un objecte, el puguis construir a partir de diferents (o cap valors), per exemple es podria construir l'objecte triangle a partir de la longitud de dos costats i un angle, o a partir de les tres longituds, etc etc

pel que ser, com a mínim el [c++](http://en.wikipedia.org/wiki/C%2B%2B) ho permet i pel cas concret que estic fent a la feina m'aniria de perles poder-ho utilitzar

al final ho he solucionat passant un *array* amb les dades que necessito a l'únic constructor que et permet el <a href="http://www.php.net" target="_blank" rel="noopener">php</a> i dins d'aquest cridar una o altre funció segons les dades que conté l'*array* :)
