Title: Introspecció a Python
Date: 2008-12-08 12:29
Author: admin
Category: General
Tags: consells, programació, python
Slug: introspeccio-a-python
Status: published

<img src="http://gil.badall.net/wp-content/uploads/2008/07/python_logo.png" title="Logotip del Python" class="alignright size-full wp-image-377" width="110" height="110" />Per tenir les dades que genera una aplicació que estic fent amb [Python](http://www.python.org "Lloc web del llenguatge de Programació Python") he escrit un parell de funcions que em permeten tenir un document estructurat (en xml) de totes les dades que es generen\[1\].

La tècnica de introspecció es basa en aprofitar les meta-dades (per dir-ho d'alguna manera) que tens sobre els objectes que has anat construint en l'aplicació per (dinàmicament) poder-ho formatar d'alguna manera.

Amb Python tenim algunes propietats, com molt bé es descriuen en [un article d'IBM](http://www.ibm.com/developerworks/library/l-pyint.html "Pàgina d'IBM sobre la introspecció a Python") \[2\]:

- objecte.\_\_dict\_\_ : Ens retorna una llista amb els elements que formen part de l'objecte. Així per mostrar els elements faríem:
- Si volem refinar el que volem mostrar tenim tot un seguit de funcions que ens diuen quin tipus de variable estem tractant: les comparacions amb el comparador [*is*](http://docs.python.org/library/stdtypes.html?highlight=membership#comparisons "Referència al mètode de comparació is") (exemple: if x is dict ....) per als tipus bàsics, [callable](http://docs.python.org/library/functions.html?highlight=callable#callable "Referència a la funció callable") per saber si és tracta d'un mètode, i per a objectes i classes [*isinstance*](http://docs.python.org/library/functions.html?highlight=isinstance#isinstance "Referència a la funció isinstance")(objecte, classe-o-llista-de-classes) i *[issubclass](http://docs.python.org/library/functions.html?highlight=isinstance#issubclass "Referència a la funció isinstance")*(classe, info-de-classe).

Només amb això podem treure molt suc a la informació que tenim ara mateix a les estructures de dades que estem muntant i si es fa el més genèric possible, no caldrà tocar ni una coma quan afegim més dades o hi encadenem alguna altra estructura.

\[1\] En certa manera hi ha truc perquè el sistema són classes que tenen diccionaris de classes a dintre fins a 5 nivells de manera que la introspecció és recursiva per naturalesa.

\[2\] És una mica vell, del 2002, però pels meus objectius n'he tingut ben prou :)
