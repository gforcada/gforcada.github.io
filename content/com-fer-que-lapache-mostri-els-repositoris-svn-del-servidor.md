Title: com fer que l'apache mostri els repositoris svn del servidor
Date: 2008-06-12 13:17
Author: admin
Category: General
Tags: apache, consells, gentoo, ssh, svn
Slug: com-fer-que-lapache-mostri-els-repositoris-svn-del-servidor
Status: published

<img src="./wp-content/uploads/2008/01/subversion.png" data-align="right" alt="logotip del Subversion" />Tinc un parell de repositoris subversion al <a href="http://badall.net:81" target="_blank" rel="noopener">servidor vell</a> i com que vull donar-hi accés a d'altres persones m'he decidit a fer el que diu el títol: permetre que es pugui accedir des de web i de forma anònima als repositoris.

Com que és en el servidor hi ha <a href="http://www.gentoo.org" target="_blank" rel="noopener">Gentoo</a> hi ha una guia que està molt bé: <a href="http://www.rockfloat.com/howto/gentoo-subversion.html" target="_blank" rel="noopener">Gentoo-Subversion</a>.

Fins al punt 11 m'ha anat perfecte, però aquí ha punxat :(

Per sort he trobat unes quantes guies que expliquen com configurar l'<a href="http://httpd.apache.org" target="_blank" rel="noopener">Apache</a>, i en concret <a href="http://svnbook.red-bean.com/en/1.1/ch06s04.html" target="_blank" rel="noopener">la guia</a> del <a href="http://svnbook.red-bean.com/" target="_blank" rel="noopener">llibre</a> del <a href="http://subversion.tigris.org/" target="_blank" rel="noopener">Subversion</a> està molt bé.\[1\]

Ja està tot configurat :)

De moment només n'he configurat l'accés a <a href="http://badall.net:81/svn/damn-ob/" target="_blank" rel="noopener">un</a> dels dos repositoris (l'altre quan tingui temps :)

Cosa que em recorda que hauria de mirar de fer servir subdominis per al servidor vell també, que ara mateix es un cacau si es vol accedir-hi :(

\[1\] Quant buscava un paràmetre en concret (AuthzSVNAccessFile) el primer resultat que m'ha sortit ha sigut <a href="http://www.comesfa.org/ca/node/1159" target="_blank" rel="noopener">un article</a> d'en <a href="http://www.majomo.com" target="_blank" rel="noopener">Marc</a> a <a href="http://www.comesfa.org" target="_blank" rel="noopener">Comesfa.org</a> :)
