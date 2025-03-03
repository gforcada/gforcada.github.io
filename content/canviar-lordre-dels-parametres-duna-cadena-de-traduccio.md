Title: Canviar l'ordre dels paràmetres d'una cadena de traducció
Date: 2009-01-28 19:54
Author: admin
Category: General
Tags: C, GNOME traduccions, traduccions
Slug: canviar-lordre-dels-parametres-duna-cadena-de-traduccio
Status: published

A vegades hi ha cadenes en els fitxers po que tenen més d'un paràmetre (els %s, %d i d'altres per l'estil) i que si volem traduir la cadena i que no quedi forçada hem de canviar l'ordre en que apareixen els paràmetres.

Per exemple la cadena:

msgid "'%s' not found in '%s'!\n"

On el primer paràmetre és el nom d'un directori i el segon un fitxer el traduiríem:

msgstr "No s'ha trobat «(el fitxer)» a (el directori)\n"

Per a poder-ho indicar hem d'utilitzar una notació una mica diferent:

msgstr "No s'ha trobat «%2\$s» a «%1\$s»\n"

Això seria per programes que estan escrits en C i C++ (suposo), per a altres llenguatges estil Python normalment es posen noms a les variables de manera que és més explícit.
