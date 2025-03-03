Title: UUID al /etc/fstab
Date: 2008-06-30 23:13
Author: admin
Category: General
Tags: consells, sistemes de fitxer, UUID
Slug: uuid-al-etcfstab
Status: published

Preocupats perquè la vostra distribució fa servir noms estranys (<a href="http://en.wikipedia.org/wiki/UUID" target="_blank" rel="noopener">UUID</a>) per a emplenar la informació del <a href="http://en.wikipedia.org/wiki/Fstab" target="_blank" rel="noopener">/etc/fstab</a>? O el contrari, voleu afegir-hi alguna nova partició (segurament algun disc usb extraïble) i voleu que sempre es munti al mateix lloc?

Per a saber l'UUID d'una partició, res més senzill que teclejar en un terminal:

    vol_id -u /dev/sdX

Vist a <a href="http://dev.osso.nl/herman/blog/2007/05/20/got-to-love-uuid-fstab-entries/" target="_blank" rel="noopener">Herman Bos</a>

Personalment no em va alegrar gaire el primer dia que vaig veure que tenia l'/etc/fstab omplert amb números llargs i estranys, però ben pensat, sobretot per el cas dels dispositius extraïbles amb caràcter permanent (discs durs muntats per usb que sempre estaran connectats o que sempre els vols tenir connectats al mateix punt) és la millor solució.
