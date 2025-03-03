Title: vim
Date: 2007-03-22 01:15
Author: admin
Slug: vi
Status: published

pàgina on aniré apuntant tot el que vaig aprenent d'aquest editor:

### fitxers de configuració:

**~/.vimrc**: fitxer en la teva carpeta personal on pots posar-hi coses com el tipus de sagnat que vols i moltíssimes altres coses

**/etc/vim/vimrc**: (en principi a totes les distribucions) fitxer general de configuració de les opcions del Vim

### canvis de mode

*ESC* per passar del mode d'edició al mode de control

*i* per passar del mode de control al mode d'edició

### en mode de control

*/alguna-cosa* per cercar alguna cosa (permet l'ús d'expressions regulars, cerca i reemplaç, etc etc)

- si prems la tecla *n* vas a la següent coincidència (bloquejant les majúscules i prement de nou *N* anem a l'anterior)

*d* o *dX* per suprimir la línia on tens el cursor (si escrius d10 suprimiràs a línia que estàs i 9 més tirant cap avall)

*p* o *P* per a enganxar de nou la línia que hem suprimit (minúscula per posar-la a sota del cursor i majúscula per posar-la a sobre)

*yy* per a copiar una línia (amb *yw* copies una paraula i *y2w* dues paraules - també s'utilitza per *p* o *d*)

*:w* per gravar

*:q!* per sortir sense gravar

*:wq* per sortir i gravar

*(esc) 1G* per anar a la primera línia

- *G* anem a l'última línia
- *nG* a la línia n

*(esc) u* per desfer l'últim canvi fet

*Ctrl+R* per a tornar a fer l'últim canvi desfet

*(esc) U* per desfer tots els canvis fets en la línia en que estem

*(esc) :s/text_vell/text_nou/* canviem «text_vell» per «text_nou» a la línia on estem (només la primera ocurrència de «text_vell» )

*(esc) :s/text_vell/text_nou/g* el mateix que abans però per totes les ocurrències

*(esc) :%s/text_vell/text_nou/g* totes les ocurrències que hi hagi de «text_vell» en el fitxer passaran a ser «text_nou»

*(esc) gf* quan estigueu a sobre un text a l'estil /etc/hostname editareu aquest fitxer (també funciona amb camins relatius init.d/sshd si esteu a /etc per exemple)

### ordres del mode de traducció (<a href="?p=250" target="_blank">+info</a>)

anar a la cadena no traduïda següent: \m  
anar a la cadena no traduïda anterior: \p  
copiar el msgid al msgstr: \c  
suprimir la cadena del msgstr: \d  
anar a la cadena dubtosa següent: \f  
anar a la cadena dubtosa anterior: \b  
marcar una cadena com a dubtosa: \z  
desmarcar una cadena com a dubtosa: \r  
mostra les estadístiques del fitxer: \s  
navegar pels errors del msgfmt: \e  
posar la informació del traductor a la capçalera: \t  
posar la informació de l'equip de traducció a la capçalera: \l

per posar la informació de l'equip de traducció i del traductor s'han d'omplir les variables següents al ~/.vimrc:  
let g:po_translator = 'Gil Forcada \<gilforcada guifi net\>'  
let g:po_lang_team = 'Catalan \<tradgnome softcatala org\>'

evidentment hi falta l'@ i els .

algunes cosetes més:

- <a href="http://www.nurdletech.com/vi.html" target="_blank">http://www.nurdletech.com/vi.html</a>
- <a href="http://www.yolinux.com/TUTORIALS/LinuxTutorialAdvanced_vi.html" target="_blank">http://www.yolinux.com/TUTORIALS/LinuxTutorialAdvanced_vi.html</a>
- <a href="http://www.vim.org/docs.php" target="_blank">http://www.vim.org/docs.php</a> òbviament aquí hi ha tot el que podeu necessitar :)
