Title: etiquetes a git
Date: 2010-03-31 13:59
Author: admin
Category: General
Tags: consells, git
Slug: etiquetes-a-git
Status: published

[<img src="./wp-content/uploads/2009/03/git-logo.png" title="git-logo" class="alignright size-full wp-image-540" width="73" height="28" />](http://gil.badall.net/wp-content/uploads/2009/03/git-logo.png)Això del git està molt bé, però com tot té la seva corba d'aprenentatge :)

Avui ha tocat indagar en les etiquetes (*tags*). N'hi ha de tres tipus:

- Senzilles
- Anotades
- Signades

Primer la versió ràpida i fàcil:

> \$ git tag NOM_ETIQUETA
>
> \$ git tag NOM_ETIQUETA *SHA1*

Creem una etiqueta amb el nom NOM_ETIQUETA i si es dóna el cas que no la volem fer en el commit en que està ara mateix el repositori local on estem treballant hi afegim el SHA1 del commit (amb un git log, o interfície web el trobem de seguida).

Per saber les etiquetes hi ha:

> \$ git tag -l -n1

Amb això mostrem totes les etiquetes, l'opció *-l*, i de pas també mostra el missatge del commit (en el cas de les etiquetes anotades també mostra l'anotació), l'opció *-n1*.

Un cop hem etiquetat tots els commits que ens sembli ja podem enviar els canvis (en cas que s'hagin d'enviar a algun lloc, estil git.gnome.org):

> \$ git push --tags

Fàcil eh :)

Si us equivoqueu també les podeu suprimir:

> \$ git tag -d NOM_ETIQUETA

I si ja l'havíeu enviat l'heu de suprimir en remot:

> \$ git push origin :refs/tags/NOM_ETIQUETA

Les etiquetes anotades tenen la particularitat que a més del nom que li donem a l'etiqueta també li afegim un comentari (l'anotació vaja).

Per crear-la:

> \$ git tag -a -m"ANOTACIÓ DE L'ETIQUETA" NOM_ETIQUETA

La resta funciona igual (enviar, llistar, suprimir, etc).

L'última opció de crear una etiqueta és la que en certs projectes té molt sentit. Les etiquetes signades permeten no només etiquetar un commit en concret de l'historial del repositori sinó que a més a més les pots signar amb una clau OpenPG, d'aquesta manera, si t'has de baixar el codi font del nucli de Linux i en vols estar 100% segur que ningú l'ha tocat ho pots saber comprovant que la signatura del commit de l'etiqueta signada correspon a en Linus Tolvards :)
