Title: it works!
Date: 2008-02-13 03:00
Author: admin
Category: General
Tags: apache, debian, guifi, problemes, sant ferriol, webmin, zyxel
Slug: it-works
Status: published

el que m'ha costat que sortís en el <a href="http://guifi.net/guifi/device/6527" target="_blank" rel="noopener">proxy</a> de <a href="http://guifi.net/ca/node/9525" target="_blank" rel="noopener">Sant Ferriol</a> <a href="http://ferriol.badall.net/" target="_blank" rel="noopener">aquesta frase</a>!

la cosa no era fàcil de deduir:

\- vaig instal·lar, com tants, un servidor amb <a href="http://www.debian.org/" target="_blank" rel="noopener">Debian</a>

\- li vaig instal·lar l'<a href="http://httpd.apache.org/" target="_blank" rel="noopener">apache</a> i no en vaig tocar ni una sola coma de la configuració

\- un cop tot instal·lat se'l van emportar a <a href="http://ca.wikipedia.org/wiki/Sant_Ferriol" target="_blank" rel="noopener">Sant Ferriol</a> (<a href="http://ca.wikipedia.org/wiki/Garrotxa" target="_blank" rel="noopener">Garrotxa</a>)

\- després de moltes setmanes per fi van poder canviar obrir els ports 22 (ssh), 80 (web) i 10000 (<a href="http://www.webmin.com/" target="_blank" rel="noopener">webmin</a>) perquè pogués fer-hi els últims ajustaments des de casa a través d'Internet

\- des del mateix moment que m'ho van dir vaig poder entrar per tant ssh com per webmin, però per web no es podia, l'Epiphany es quedava pensant i pensant fins que algun *time out* (la revista no eh!) n'aturava l'espera

\- després de provar i provar coses (un *wget http://localhost* des del propi servidor funcionava perfectament) vaig demanar la contrasenya del router per veure si era allà el problema

\- en principi no ho semblava, ja que la taula de direccionament de ports no hi havia res estrany, els tres ports estaven redireccionats cap a la mateixa ip de la mateixa manera

\- avui finalment, després de donar-hi voltes i voltes m'he mirat una per una les opcions del router (un <a href="http://www.zyxel.com/" target="_blank" rel="noopener">zyxel</a>, no en ser el model) resulta que hi ha uns filtres predeterminats per a uns quants ports, entre els quals el 80 que fa que tot el que es rebi s'enviï cap a 0.0.0.0 (o sigui com enviar-ho a */dev/null* pràcticament)

així que ja ho sabeu, si teniu algun zyxel aprop reviseu-ne bé les opcions no sigui cas que hi hagi algun filtre que us faci males jugades!
