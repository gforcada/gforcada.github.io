Title: en català, la setmana comença en dilluns
Date: 2012-04-22 16:46
Author: admin
Category: General
Tags: català, gentoo, glibc, programari lliure
Slug: en-catala-la-setmana-comenca-en-dilluns
Status: published

(anava a escriure sobre una altra cosa, però compartir l'alegria sempre és millor :D)

Sembla senzill oi?

Doncs bé, [**per fi!**](http://sourceware.org/bugzilla/show_bug.cgi?id=6770 "Informe d'errada a la glibc sobre la informació del locale català") ((Gràcies [Jordi!!!](http://oskuro.net/blog/ "Bloc d'en Jordi Mallach"))) tots els Linux, no importa la distribució, ja no tindran excuses per començar el dia de la setmana en diumenge!

Si ve els derivats de [Fedora](http://fedoraproject.org/ "Pàgina web de la distribució Fedora") i [Debian](http://www.debian.org/ "Pàgina web de la distribució Debian") ja feia anys i panys que tenien un pedaç que aplicaven, no totes les distribucions en tenien ([Gentoo](http://www.gentoo.org "Pàgina web de la distribució Gentoo") per exemple :)) i com sempre, com més *upstream* estiguin fets els canvis, menys manteniment s'ha de fer més avall a la cadena de distribució :)

Si en voleu saber més, podeu llegir l'article a [LWN](http://lwn.net/Articles/488778/ "Article a LWN.net sobre els canvis en el desenvolupament de la glibc"). No és sobre el català en concret però sí sobre allà on estava la informació errònia del català :)

Si a més a més voleu col·laborar-hi, seria bon moment ara per revisar el *locale* de dalt a baix i deixar-lo el més endreçat i net possible (una revisió dels pedaços que apliquen les distribucions segur que ja dóna pistes).

Ja no hauré de consultar [el meu propi apunt](http://gil.badall.net/2009/05/07/les-setmanes-comencen-dilluns/ "Apunt al meu bloc sobre com canviar el locale i que mostri els dilluns com a primer dia de la setmana") al bloc cada vegada que actualitzi la [glibc](http://www.gnu.org/software/libc/ "Pàgina web del programari glibc") :)
