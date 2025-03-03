Title: recuperar fitxers suprimits
Date: 2008-10-26 15:18
Author: admin
Category: General
Tags: consells, GNOME, svn
Slug: recuperar-fitxers-suprimits
Status: published

<img src="./wp-content/uploads/2008/01/subversion.png" data-align="right" alt="logotip del Subversion" />Per recuperar fitxers suprimits amb el <a href="http://subversion.tigris.org/" target="_blank" rel="noopener">Subversion</a>:

svn --verbose log (per a mirar en el registre quan es va suprimir i per tant saber la revisió anterior a la que es va suprimir per poder-lo recuperar)

svn copy svn+ssh://gforcada@svn.gnome.org/svn/damned-lies/trunk/po/POTFILES.in@1091 POTFILES.in

El URL del fitxer@revisió  i el nom del fitxer destí (per si el volem recuperar amb un nom diferent).

Resulta que fa un temps es feia servir una altra sintaxi que ara no serveix :S

Sort que hi ha el <a href="http://svnbook.red-bean.com/nightly/en/svn.ref.svn.c.copy.html" target="_blank" rel="noopener">llibre</a> :)

Hi ha algun llibre semblant per el <a href="http://git.or.cz/" target="_blank" rel="noopener">git</a>?
