Title: afegir mètodes a classes ja existents (objective-c)
Date: 2010-04-27 07:14
Author: admin
Category: General
Tags: iphone, objective-c, programació
Slug: afegir-metodes-a-classes-ja-existents-objective-c
Status: published

**Introducció**

Amb l'[Objective-C](http://en.wikipedia.org/wiki/Objective-c "Entrada a la wikipedia anglesa sobre el llenguatge de programació Objective-c") tens classes, categories i protocols.

Les classes implementen un seguit de protocols (un llistat de mètodes, una interfície vaja) i per facilitar la lectura i manteniment del codi, aquestes classes es poden separar en diversos fitxers (cada un d'ells una categoria) que haurien d'implementar un subconjunt de les funcions que es vol que faci la classe.

Així per exemple la classe *String* compleix amb el protocol *Copy*, per tant es poden copiar strings i una de les categories de funcions és la de *spellChecking*.

**Problema**

Si tenim un classe que ja ens ve del sistema (la classe String per exemple) i n'hem creat sub-classes (StringA, StringB, StringC) que totes tenen un mètode en comú (markSpell), quan creem instàncies de les subclasses ho podem fer amb un punter a la classe String però quan s'executa el codi ens dóna un avís de que la classe String podria no respondre ((A Objective-C les crides a mètodes en diuen enviament de missatges)) al missatge markSpell.

**Solució**

Crees un protocol que contingui aquest mètode ((Sí, la sintaxi és una mica estranya, però al final t'hi acostumes)):

> @protocol MarkSpell
>
> \- (void) markSpell
>
> @end

I quan crees el punter genèric de la classe Spell li dius que la variable compleix el protocol anterior:

> String \<MarkSpell\> \*myString = \[\[String alloc\] init\];

I amb això el compilador de l'[Xcode](http://en.wikipedia.org/wiki/Xcode "Entrada a la wikipedia anglesa sobre l'EID Xcode") ja no es queixarà més :)
