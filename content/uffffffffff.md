Title: uffffffffff
Date: 2007-03-16 18:52
Author: admin
Category: General
Tags: bloc, gentoo, php, phpmyadmin, servidor badall, wordpress
Slug: uffffffffff
Status: published

per si no us en havíeu adonat el <a href="http://gil.badall.net" target="_blank" rel="noopener">bloc</a> havia estat inaccessible des de feia com a mínim 24h

i d'aquestes 24h me n'h estat com a mínim 14 per trobar-hi l'entrellat, ja que la sol·lució ni molt menys era òbvia...

els fets:

després de remenar molt el bloc ahir tot funcionava perfectament

tot mirant els *<a href="http://en.wikipedia.org/wiki/Data_logging" target="_blank" rel="noopener">logs</a>* de l'<a href="http://httpd.apache.org" target="_blank" rel="noopener">apache</a> (a saber perquè em va picar mirar-los) vaig veure que un *<a href="http://en.wikipedia.org/wiki/Vhost" target="_blank" rel="noopener">vhost</a>* que havia creat feia molt temps donava problemes, així que vaig esborrar el fitxer de la configuració del *vhost* i vaig reiniciar l'apache, que com que em va donar problemes i no es va iniciar del tot correctament vaig decidir reiniciar el servidor

a partir de reiniciar ja no funcionava el bloc! però el més estrany de tot, el <a href="http://www.phpmyadmin.net" target="_blank" rel="noopener">phpmyadmin</a> que tinc instal·lat tampoc funcionava i li faltaven MOLTS fitxers (no era el cas del <a href="http://www.wordpress.org" target="_blank" rel="noopener">wordpress</a>), després de barallar-me molt amb el bloc, vaig copiar de nou els fitxers del phpmyadmin i aquest ja funcionava bé, però el bloc quan entraves a la seva pàgina principal no mostrava res, ni títol, ni missatges d'error, res de res, el codi font era zero, entrant-hi amb el <a href="http://links.twibright.com/" target="_blank" rel="noopener">links2</a> (navegador web per terminal) donava un error de <a href="http://en.wikipedia.org/wiki/Internet_socket" target="_blank" rel="noopener">socket</a> ...

per acabar d'embolicar que fa fort si entrava a la secció d'administració del bloc SÍ que funcionava aquest, però tornant a la pàgina inicial o qualsevol visualització de les entrades escrites tornava una pàgina amb blanc

més problemes, si baixava al portàtil el .zip del wordpress des del navegador web o ho feia amb el <a href="http://wget.sunsite.dk/" target="_blank" rel="noopener">wget</a> des del servidor donaven un md5sum diferent! cada vegada que entrava a la portada a al log d'errors de l'apache sortia

    [Fri Mar 16 17:52:48 2007] [notice] child pid 6278 exit signal Segmentation fault (11)

havia provat de tot, canviar la base de dades del wordpress, canviar-li el <a href="http://en.wikipedia.org/wiki/Path_%28computing%29" target="_blank" rel="noopener"><em>path</em></a> diverses vegades, fer una instal·lació completament nova del wordpress, recompilar l'apache i el php (el <a href="http://www.mysql.com" target="_blank" rel="noopener">mysql</a> no podia ser perquè no em donava cap problema) i res

buscant al <a href="http://www.google.com" target="_blank" rel="noopener">google</a> informació sobre pàgines en blanc del wordpress o als <a href="http://forums.gentoo.org" target="_blank" rel="noopener">fòrums de gentoo</a> sobre el wordpress tampoc donaven cap resultat

buscar l'error de l'apache m'enviava a <a href="http://httpd.apache.org/dev/debugging.html#crashes" target="_blank" rel="noopener">una pàgina de la documentació de l'apache</a> que em deia que recompilés l'apache amb no se quines opcions i fes una depuració complicadíssima

al <a href="http://bugzilla.gentoo.org" target="_blank" rel="noopener">bugzilla del gentoo</a> tan per l'apache com pel php no hi havia res que s'assemblés al meu problema i tan el php com l'apache són estables en la versió que els tinc, però <a href="http://bugs.gentoo.org/show_bug.cgi?id=170521" target="_blank" rel="noopener">un informe d'error</a> referint-se al mediawiki que no funcionava bé l'última <a href="http://packages.gentoo.org/packages/?category=dev-lang;name=php" target="_blank" rel="noopener">versió estable del php</a> però que l'anterior (el canvi de php5.2 a php5.1) ho arreglava, així que he recompilat una versió menys nova del php i ...

voilà, de moment funciona!!
