Title: mètodes virtuals? polimorfisme? delegació? herència?
Date: 2008-11-28 00:06
Author: admin
Category: General
Tags: dubtes, programació, python
Slug: metodes-virtuals-polimorfisme-delegacio-herencia
Status: published

<img src="./wp-content/uploads/2008/07/python_logo.png" title="Logotip del Python" class="alignright size-full wp-image-377" width="110" height="110" />Aquest tros de codi amb [Python](http://www.python.org/ "Lloc web del llenguatge de programació Python"):

>     #!/usr/bin/env python
>     # -*- encoding: utf-8 -*-
>
>     class main():
>        def laptop(self):
>           self.p()
>
>     class one(main):
>        def p(self):
>           print "Lenovo"
>
>     class two(main):
>        def p(self):
>           print "Asus"
>
>     # Creem un parell d'instàncies
>     i_one = one()
>     i_two = two()
>
>     i_one.laptop() # mostra "Lenovo"
>     i_two.laptop() # mostra "Asus"

El que fa bàsicament és crear 3 classes (dues d'elles -*one* i *two*- hereden de la primera -*main*-) de manera que totes les instàncies que es facin de les classes filles tindran els mètodes de la classe mare (el mètode *laptop* en aquest cas).

A més cada classe filla defineix una mateixa funció (la funció *p*).

La gràcia d'aquest disseny és que et permet definir una especialització de comportament de manera que per exemple, si tens una col·lecció d'instàncies de *one* i *two* barrejades però vols saber-ne quin portàtil tenen, només cal que executis el mètode *laptop* a tota la col·lecció que sense cap problema ens dirà per a cada un d'ells quin portàtil té.

El dubte que em queda ara és: quin nom rep aquesta tècnica? Perquè he estat buscant en el llibre de Python que tinc ([Learning Python](http://oreilly.com/catalog/9780596513986/ "Llibre Learning Python d'O'Reilly") d'[O'Reilly](http://www.oreilly.com "Lloc web de l'editorial de llibres O'Reilly")) d'on he recordat aquesta possibilitat del Python i no he aconseguit trobar-la ni a l'índex del principi (per temes) ni  el del final (per nom).
