Title: consell: redireccions amb l'apache
Date: 2009-10-25 08:58
Author: admin
Category: General
Tags: apache, consells, programari lliure
Slug: consell-redireccions-amb-lapache
Status: published

Estic muntant un [cgit](http://hjemli.net/git/cgit/ "Lloc web del projecte cgit, un visualitzador web de dipòsits de git") al [servidor](http://badall.net "Servidor de badall.net") i m'he estat com dos dies intentant que en entrar a [git.badall.net](http://git.badall.net "Interfície web dels dipòsits de git que estan allotjats a badall.net") ((de moment demana usuari i contrasenya perquè hi estic fent proves :) )) s'executés el cgi que genera el cgit.

Al cap i a la fi era un alias no? Així que vaig anar a la documentació de [l'Apache](http://httpd.apache.org/ "Lloc web del servidor web Apache") a buscar informació sobre el [mod_alias](http://httpd.apache.org/docs/2.2/mod/mod_alias.html "Documentació sobre el mòdul d'alias de l'Apache") sense cap solució que funcionés ... llavors vaig pensar que seria una modificació de l'URL, així que cap a la documentació sobre el [mod_rewrite](http://httpd.apache.org/docs/2.2/mod/mod_rewrite.html "Documentació sobre el mòdul de reescriptura dels URL de l'Apache"). De nou sense cap resultat útil.

Finalment ((a la tercerca sempre va a la vençuda no?)) en [uns fòrums](http://fixunix.com/mozilla/408847-attempt-invoke-directory-script.html "Fòrum on he trobat la solució") he trobat la solució:

>     DirectoryIndex cgit.cgi

Només feia falta que en el directori del servidor virtual hi posés que l'índex del directori sigués l'script que s'havia d'executar!
