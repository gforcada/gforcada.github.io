Title: versionat de l'Ubuntu
Date: 2007-03-26 14:08
Author: admin
Category: General
Tags: gentoo, GNOME, linus, números de versions, ubuntu
Slug: versionat-de-lubuntu
Status: published

si normalment en el programari es fa servir els <a href="http://en.wikipedia.org/wiki/Version_number" target="_blank" rel="noopener">números de versions</a> de manera incremental per denotar que s'ha avançat des de la versió anterior, en el programari lliure en particular es fa servir força la descomposició de <a href="http://www.kernel.org" target="_blank" rel="noopener">Linux</a>\[0\] que consisteix en que el nombre major és per els canvis MOLT importants (canvis en l'<a href="http://en.wikipedia.org/wiki/Api" target="_blank" rel="noopener">API</a> per exemple), les versions x.senars són per a versions no estables que quan siguin estables es convertiran al següent nombre parell (o sigui les versions de prova 2.17 en ser estables seran la <a href="http://www.gnome.org/start/2.18/notes/ca/" target="_blank" rel="noopener">2.18</a>, com el <a href="http://www.gnome.org" target="_blank" rel="noopener">GNOME</a> per exemple)

per a revisions més menors, de manteniment, depuració d'errors o d'altres canvis poc importants es fa servir un tercer dígit (x.y.z, com el GNOME 2.16.3 que és la tercera versió estable del <a href="http://www.gnome.org/start/2.16/notes/ca/" target="_blank" rel="noopener">GNOME 2.16</a>)f

finalment, a vegades quan es fa un llançament hi ha algun petit problema que es resol amb una simple modificació, llavors s'afegeix encara un altre dígit, per exemple 3.2.0.1

però anant al gra, les versions d'<a href="http://www.ubuntu.com" target="_blank" rel="noopener">Ubuntu</a> em desconcertaven, 6.06, 6.10, 7.04 ...

fins que l'altre dia ho vaig trobar a l'ajuda de l'Ubuntu (tot i que no ho estava buscant), l'explicació és ben senzilla, el nombre major és la unitat de l'any en que estem (200**5**, 200**6**, 200**7** ...) i el nombre menor és el número de mes en que s'allibera la versió (juny→06, abril→04, octubre→10, etc etc)

un altre esquema semblant a aquest és el que fa servir <a href="http://www.gentoo.org" target="_blank" rel="noopener">Gentoo</a> per exemple, que tot i que no fan mai noves versions (degut a l'estructura de la distribució que només et cal anar actualitzant els *ebuilds* que tens instal·lats) sí que fan com unes marques en el temps volent dir: "ara està força estable"\[1\]

el seu esquema és tan senzill com el número de l'any i el número de marca d'estabilitat, o sigui 2007.1 és la segona (és comença per 0) marca d'estabilitat, per dir-ho d'alguna manera

\[0\] que jo sàpiga el parell-senar ho va començar a fer servir en <a href="http://en.wikipedia.org/wiki/Linus_Torvalds" target="_blank" rel="noopener">linus</a>

\[1\] bé, de fet és l'estabilització del que són els components del nucli que formen la distribució Gentoo, que cada vegada que tots s'han actualitzat a noves versions i s'han estabilitzat en els dipòsits de Gentoo es fa la versió, pot haver-hi vegades que no en facin ni en un any, ja que els components bàsics del Gentoo són tan mínims que si no hi ha gaires millores en els components o en la manera d'instal·lar la distribució, com que igualment després de tenir-ho tot instal·lat pots actualitzar a l'última versió disponible no hi ha pèrdua de funcionalitat
