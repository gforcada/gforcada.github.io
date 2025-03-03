Title: eina del dia: cdrecord
Date: 2009-11-02 09:17
Author: admin
Category: General
Tags: consells, gentoo, Softcatalà, terminal, ubuntu
Slug: eina-del-dia-cdrecord
Status: published

Sembla que el [Brasero](http://en.wikipedia.org/wiki/Brasero_(software) "Article de la wikipedia anglesa sobre el programa de enregistrament de CD/DVD Brasero") no em funciona massa bé de manera que per esborrar el CD-RW que tinc per a enregistrar-hi l'[Ubuntu 9.10](http://www.ubuntu.com/products/whatisubuntu/910features "Tour sobre l'Ubunut 9.10") ((És per la [Sílvia](http://silvia.badall.net "Bloc de la Sílvia") eh, no us preocupeu, no abandono [Gentoo](http://www.gentoo.org "Lloc web de la distribució Gentoo") de moment :D )) he decidit fer-ho fàcil i teclejar quatre ordres des del terminal:

> mount *\# per veure el punt de muntatge del CD-RW*
>
> umount **/dev/XXX** *\# desmuntem la unitat*
>
> cdrecord blank=all **/dev/XXX** *\# esborrem la unitat*
>
> cdrecord **/dev/XXX** **/RUTA/FINS/AL/FITXER/ISO** *\# enregistrem el fitxer ISO*
>
> eject **/dev/XXX** *\# expulsem la unitat*

I llestos ja tinc l'Ubuntu 9.10 enregistrat al CD-RW. ((Baixat des de [Softcatalà](http://www.softcatala.cat "Lloc web del projecte de traducció de programari al català Softcatalà") perquè no hi havia manera que els miralls d'Ubuntu.com funcionèssin))
