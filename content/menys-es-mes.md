Title: Menys és més
Date: 2011-01-30 15:40
Author: admin
Category: General
Tags: consells, programari lliure, xorg, xrandr
Slug: menys-es-mes
Status: published

I mai millor dit!

Avui he actualitzat el nucli i després de reiniciar per arrencar amb el nucli nou em trobo que la pantalla es mostra a 800x600 en comptes de 1280x800.

Començo a remenar opcions i veig que sí que puc tornar als 1280x800 amb l'xrandr ((M'ha anat molt bé [una meva entrada al bloc](http://gil.badall.net/2009/09/18/dues-pantalles/ "Entrada al bloc sobre com configurar la resolució de les pantalles des del terminal"))), però després de reiniciar sempre tornava als 800x600.

Després d'examinar el /var/log/Xorg.0.log semblava que era algun tema de configuració... "Doncs res" m'he dit, a tocar el /etc/X11/xorg.conf a veure què hi passa.

El primer que se m'ha acudit es esborrar el fitxer (fent una còpia abans!) i reiniciar, i voilà! Ja funciona a1280x800 i a més a més, quan connecto la pantalla externa de casa ja me la detecta bé i a més a més a la resolució que toca i tot ((M'havia fet un script per la pantalla de casa i de la feina :D))!
