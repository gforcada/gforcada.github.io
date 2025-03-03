Title: administració de servidors i git
Date: 2010-05-11 06:28
Author: admin
Category: General
Tags: consells, git
Slug: administracio-de-servidors-i-git
Status: published

[<img src="./wp-content/uploads/2009/03/git-logo.png" title="git-logo" class="alignright size-full wp-image-540" width="73" height="28" />](./wp-content/uploads/2009/03/git-logo.png)Fins que no proves les coses no te n'adones de lo difícil, o fàcil, que és fer-les...

Avui havia de fer uns canvis a un dels servidors de la feina i com que eren temes de configuració ... cd /etc

Però abans de prémer cap més tecla m'ho he pensat dues vegades i he teclejat unes quantes ordres ben senzilles i  molt útils de cara al futur:

**Control de versions de la configuració d'un servidor**

Sembla que pugui ser una cosa difícil, que requereixi molt de temps i que sigui complex de mantenir oi? Doncs res més senzill que fer:

>     cd /etc
>     git init
>     (opcionalment vim .gitignore per excloure els fitxers que no volem versionar)
>     git add -A
>     git commit -m"Configuració inicial que funciona del servidor"

Només amb aquestes senzilles ordres ja tenim tot el directori /etc versionat amb git. A partir d'ara qualsevol canvi a qualsevol fitxer que estigui dintre de /etc ens sortirà amb un *git status* i quan haguem fet les proves necessàries per assegurar que els canvis són correctes ja podrem fer un *git commit FITXER1 FITXER2 -m"Missatge"* per tenir controlada una nova revisió dels fitxers.

Ara ja no hi ha excusa per dir que s'ha perdut alguna configuració o que s'ha espatllat algun servei del servidor, sempre tindràs un *git checkout* o un *git reset --hard HEAD* per tornar a una versió dels fitxers de configuració correcta :)
