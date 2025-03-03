Title: suprimir els fitxers que no són d'un dipòsit
Date: 2008-03-12 13:06
Author: admin
Category: General
Tags: consells, svn, terminal, xargs
Slug: suprimir-els-fitxers-que-no-son-dun-diposit
Status: published

<img src="http://gil.badall.net/wp-content/uploads/2008/01/subversion.png" data-align="right" alt="logotip del Subversion" />Es veu que m'ha agafat la dèria de fer-me scripts per a tot :)

El d'avui és per el típic cas en que estem treballant amb un dipòsit i per poder fer comparacions i tot plegat ens queden la tira de fitxers temporals repartits per tot arreu i que un cop acabada la feina i confirmada (*commit* en anglès) només fan nosa, així que anem a suprimir-los:

svn status \| grep ? \| cut -d" " -f7 \| xargs rm

amb *svn status* ens dirà quins fitxers hi ha diferents dels que estan actualment al dipòsit <a href="http://subversion.tigris.org/" target="_blank" rel="noopener">SVN</a>, amb el *grep* agafem els que es desconeix (normalment seran aquests els que volem suprimir), seguidament agafem només el nom del fitxer amb el *cut* i per acabar amb l'*<a href="?p=304" target="_blank" rel="noopener">xargs</a>* i un simple *rm* els eliminem tots :D
