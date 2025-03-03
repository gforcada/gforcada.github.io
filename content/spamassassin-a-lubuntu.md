Title: spamassassin a l'ubuntu
Date: 2007-07-19 14:44
Author: admin
Category: General
Tags: evolution, spamassassin, ubuntu
Slug: spamassassin-a-lubuntu
Status: published

des de que vaig actualitzar a l'última versió d'<a href="http://www.ubuntu.com" target="_blank" rel="noopener">Ubuntu</a> (i d'això ja en fa uns quants dies) havia detectat que no funcionava però com que tampoc m'importava massa anar suprimint els 5 o 10 correus d'spam que rebia

però aquests dies que miro el correu un cop ves a saber quan si que comença a molestar trobar una trentena de correus d'<a href="http://ca.wikipedia.org/wiki/Correu_brossa" target="_blank" rel="noopener">SPAM</a> cada vegada

o sigui que m'ho he tornat a mirar, em sonava que algú havia comentat que s'havia d'iniciar el servei, així que:

/etc/init.d/spamassassin start

però em deia que no s'activava perquè estava definit així a /etc/default/spamassassin de manera que he canviat la variable ENABLED=0 a ENABLED=1 i ja el podia iniciar :)

el que no entenc és perquè l'han desactivat d'una versió a l'altra i potser fins i tot més important, per què l'Evolution no diu res si no està funcionant si el tens habilitat a la llista de connectors? (me'n vaig al <a href="http://bugzilla.gnome.org" target="_blank" rel="noopener">b.g.o</a> em sembla :)
