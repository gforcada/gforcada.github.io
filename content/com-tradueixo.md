Title: com tradueixo
Date: 2007-06-01 20:18
Author: admin
Category: General
Tags: bloc, gedit, manual, meld, Softcatalà, termcat, traduccions
Slug: com-tradueixo
Status: published

ja feia moltes setmanes que ho volia escriure això, a veure si me'n surto

això intenta ser una petita guia de com tradueixo jo ara mateix i també alguns consells o *trucs* que utilitzo per diverses coses, aquí va:

1.  primer de tot ens cal buscar un fitxer per traduir, les millors pràctiques per això són dues:
    1.  si hi ha un equip de traducció (com en el <a href="http://www.softcatala.org/projectes/gnome/" target="_blank" rel="noopener">GNOME</a>, l'<a href="http://softcatala.org/projectes/openoffice/index.htm" target="_blank" rel="noopener">OOo</a>, <a href="http://softcatala.org/projectes/mozilla/" target="_blank" rel="noopener">Mozilla</a>, etc etc) demanar-ho directament allà que us en assignin un, o bé si ja teniu prou confiança i rodatge agafar-ne un directament vosaltres dels dipòsits de traduccions
    2.  si no hi ha equip de traducció i el fitxer ja estava parcialment traduït, posar-se en contacte amb el traductor anterior sempre ajuda a no repetir esforços
    3.  òbviament si el fitxer és nou endavant les atxes, en cas que sigui nou però hi hagi equip de traducció notificar que el vas a fer sempre ajuda a no repetir esforços
2.  un cop tenim el fitxer per traduir, ens hem de documentar: <a href="http://www.softcatala.org/projectes/eines/guiaestil/guiaestil.htm" target="_blank" rel="noopener">llegir la guia d'estil</a>, tenir a mà el <a href="http://www.softcatala.org/projectes/eines/recull/recull.htm" target="_blank" rel="noopener">recull de termes</a>, el <a href="http://www.softcatala.org/wiki/Glossari_de_l%27OpenOffice.org" target="_blank" rel="noopener">glossari específic del projecte</a> o <a href="http://www.softcatala.org/projectes/eines/mt/" target="_blank" rel="noopener">una memòria de traducció</a> (o qualsevol altre document per a fixar criteris per mantenir una cohesió) seran els teus aliats per fer una traducció, no ja correcte, sinó també amb harmonia amb la resta del projecte
    1.  no cal que us llegiu tot el recull de termes (menys encara la memòria de traducció), a mesura que surtin dubtes els podeu anar consultant
3.  ara ja podem començar a editar el nostre fitxer: per fer-ho hi ha molts programes que ho faciliten, el <a href="http://gtranslator.sourceforge.net/" target="_blank" rel="noopener">gtranslator</a>, el <a href="http://www.poedit.net/" target="_blank" rel="noopener">poedit</a> (els dos per a <a href="http://www.gnome.org" target="_blank" rel="noopener">GNOME</a> i el poedit per Windows també), el <a href="http://kbabel.kde.org/" target="_blank" rel="noopener">kbabel</a> (per a <a href="http://www.kde.org" target="_blank" rel="noopener">KDE</a>). També tenim connectors per a editors de línia d'ordres com el <a href="http://www.vim.org/" target="_blank" rel="noopener">vim</a> o l'<a href="http://www.gnu.org/software/emacs/" target="_blank" rel="noopener">emacs</a> i en definitiva qualsevol editor de text pla (els editors de text formatat com l'<a href="http://www.openoffice.org/product/writer.html" target="_blank" rel="noopener">OOo Writer</a> o l'<a href="http://www.abisource.com/" target="_blank" rel="noopener">AbiWord</a> per exemple no serien els millors)
    1.  personalment faig servir el <a href="http://www.gedit.org/" target="_blank" rel="noopener">Gedit</a> per diverses raons:
        1.  permet veure unes quantes cadenes alhora, cosa que els altres editors no (gtranslator, poedit)
        2.  permet fer cerques *"vives"* (si premeu Ctrl+K i entreu algun text veureu què vull dir)
        3.  permet fer desplaçaments ràpids (premeu Ctrl+fletxa de la dreta i l'esquerra i veureu què passa) i seleccions ràpides (Ctrl+Alt+fletxa de la dreta o esquerra), fins i tot seleccionar des del lloc on esteu fins al principi o final (Ctrl+Alt+tecla d'amunt o d'avall)
        4.  et permet tenir diferents documents oberts en pestanyes i poder-hi accedir fàcilment (Alt+nº de la pestanya), per exemple tenir en una pestanya la traducció i amb les altres del costat la guia d'estil, el recull i la memòria de traducció on hi pots cercar fàcilment paraules amb el Ctrl+K
        5.  ressaltat de sintaxi que a més pots personalitzar i permet verificar l'ortografia
        6.  deixem-ho aquí que sembla una oda al Gedit :) que tot sigui dit no és perfecte, <a href="http://bugzilla.gnome.org/show_bug.cgi?id=389286" target="_blank" rel="noopener">li faltaria això</a>
4.  un cop acabat de traduir l'hem de repassar \[1\]:
    1.  torneu a mirar les cadenes una a una
    2.  passeu-li un corrector ortogràfic
    3.  comproveu alguns mots concrets amb traduccions de programes semblants (si esteu traduint un reproductor multimèdia us podeu mirar el banshee, el totem i d'altres)
    4.  consulteu el <a href="http://www.termcat.cat" target="_blank" rel="noopener">termcat</a>, el <a href="http://www.wordreference.com" target="_blank" rel="noopener">wordreference</a>, el <a href="http://www.dictionary.com" target="_blank" rel="noopener">dictionary.com</a>, el <a href="http://www.grec.cat/home/cel/dicc.htm" target="_blank" rel="noopener">gran diccionari de la llengua catalana</a>, el <a href="http://www.grec.cat/cgibin/mlt00.pgm" target="_blank" rel="noopener">diccionari de la llengua catalana multilingüe</a>, el <a href="http://www.translendium.com/" target="_blank" rel="noopener">translèndium</a>, el <a href="http://www.softcatala.org/traductor/" target="_blank" rel="noopener">traductor de Softcatalà</a> o qualsevol altra font enciclopèdica
5.  si el fitxer ja tenia una traducció anterior i l'heu d'enviar a una llista de correu de traducció (des d'on es coordinen les traduccions) és aconsellable fer un diff (o sigui la diferència entre el fitxer vell i el nou), no te sentit que s'hagin de mirar tot el fitxer sencer si la teva traducció nova només ha canviat 5 o 6 cadenes i el fitxer sencer en són 564
    1.  l'ordre del diff des de la línia d'ordres seria: *diff -u fitxer_vell.po fitxer_nou.po \> fitxer.diff*
6.  abans d'enviar el fitxer sencer i el diff a la llista de correu seria aconsellable que els comprimiu (un tar.bz2 o tar.gz mateix), d'aquesta manera ocuparan menys espai i faran més lleugera la càrrega del mailman quan hagi de reenviar els correus a tota la gent subscrita a la llista de correu
7.  **ja està!**

i un parell de bonus:

el <a href="http://meld.sourceforge.net/" target="_blank" rel="noopener">meld</a>, és un visualitzador de diferències, és perfecte per a treure la majoria de línies que innecessàriament se'ns afegeixen al diff, si us en mireu un veureu que hi ha moltíssims canvis que només són perquè s'ha canviat la línia de codi on estava la cadena, el meld facilita fer la fusió d'aquests canvis que són trivials, de manera que un diff que podria ser de més de 500 o 600 línies es redueix a unes 70 o 80 (i no exagero)

amb l'ordre *msgfmt --statistics nom_fitxer.po* podeu no només saber les estadístiques del fitxer, sinó també si hi ha errors en el fitxer i a quina línia es produeixen :)

\[1\] com que sóc força manta <a href="fitxers/revisio.sh" target="_blank" rel="noopener">m'he fet un script</a> que em permet (a partir del fitxer vell i el nou acabat de traduir) treure les cadenes que s'han afegit o modificat i d'aquesta manera poder revisar més còmodament el text (sense totes les cadenes en anglès o de format) i apart em treu el diff tradicional i em fa un fitxer .tar.bz2 amb la traducció i el diff, apunt per enviar-ho a la llista de traducció :)
