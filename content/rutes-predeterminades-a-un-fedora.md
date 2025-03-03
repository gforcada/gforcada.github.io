Title: rutes predeterminades a un Fedora
Date: 2007-10-16 00:13
Author: admin
Category: General
Tags: fedora, guifi, programari lliure, servidor proxy, xarxes
Slug: rutes-predeterminades-a-un-fedora
Status: published

resulta que un servidor (<a href="http://fedoraproject.org/" target="_blank" rel="noopener">fedora</a> 7) que havia configurat aquest estiu i que tenia dues interfícies de xarxa quan es reiniciava no tenia la ruta predeterminada que se li havia configurat, de manera que ho he mirat una mica hi he trobat <a href="http://www.redhat.com/docs/manuals/linux/RHL-8.0-Manual/ref-guide/s1-boot-init-shutdown-sysconfig.html" target="_blank" rel="noopener">un document</a> força vell però força bo\[1\]

així que només he hagut d'afegir un parell de línies:

    GATEWAY=ip_del_router_d'Internet
    GATEWAYDEV=nom_de_la_interfície

\[1\] una de les ventatges que ara mateix li veig al fedora és que com que està basat en el Red Hat de fa força temps, tot el que és aspecte gràfic i «parides» vàries s'ha modificat de dalt a baix, igual com la manera de treballar amb la comunitat, etc etc però per sort, en aquest cas, les coses bàsiques com la configuració de la xarxa es fa tot igual que abans (això si completament diferent que a totes les altres distribucions)

i jo em pregunto, per què coi una part tan important, sinó la que més, com és la connectivitat del servidor que estàs administrant no forma part de la <a href="http://www.linux-foundation.org/en/LSB" target="_blank" rel="noopener">LSB</a> ?

que per moltes <a href="http://en.wikipedia.org/wiki/Linux_Standard_Base#Criticism" target="_blank" rel="noopener">crítiques</a> que pugui tenir almenys ja es podrien posar d'acord amb això, que després s'hagués de canviar, doncs es fa, serà que no s'han fet canvis a la vida ...
