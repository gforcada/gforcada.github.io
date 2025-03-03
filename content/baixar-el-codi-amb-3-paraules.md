Title: baixar el codi amb 3 paraules
Date: 2008-02-19 14:20
Author: admin
Category: General
Tags: consells, GNOME, svn, terminal
Slug: baixar-el-codi-amb-3-paraules
Status: published

<img src="./wp-content/uploads/2008/01/subversion.png" data-align="right" alt="logotip del Subversion" />cansat d'haver d'escriure cada dia el *svn co svn+ssh://gforcada@svn.gnome.org/svn/\$mòdul/\$branca \$directori* avui per fi <a href="./wp-content/uploads/2008/02/svnco.sh" target="_blank" rel="noopener">m'he fet un script</a> que només li has de dir el mòdul, la branca i opcionalment el directori (sinó agafa el mateix valor que el mòdul) i llestos ja t'ho baixa :)

exemple de crida:

svnco.sh NetworkManager trunk nm

a més ja hi he posat l'usuari i servidor com a variables al principi de tot perquè si algú el vol utilitzar li sigui ben fàcil canviar-ho :)

per a poder-lo cridar d'aquesta manera s'ha d'editar el fitxer *~/.bashrc* i dir-li que afegeixi en el *PATH* el directori on deixeu l'script (normalment si sou usuari normal i no teniu permís de sistema seria a *~/.bin*), de manera que si editeu el *~/.bashrc* hi hauria d'haver una línia a l'estil:

export PATH=\$PATH:~/.bin

i llestos, a baixar codi que falta poc pel <a href="http://live.gnome.org/TwoPointTwentyone" target="_blank" rel="noopener">GNOME 2.22</a>!
