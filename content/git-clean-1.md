Title: git-clean (1)
Date: 2009-05-17 11:24
Author: admin
Category: General
Tags: consells, git
Slug: git-clean-1
Status: published

<img src="http://gil.badall.net/wp-content/uploads/2009/03/git-logo.png" title="git-logo" class="alignright size-full wp-image-540" width="73" height="28" alt="git-logo" />A vegades després de compilar un programa que t'has baixat per exemple de [git.gnome.org](http://git.gnome.org "Interfície web del sistema de control de versions distribuït del GNOME") vols tornar a deixar-ho tot tal com estava (o sigui una còpia igual del que hi ha publicat a git.gnome.org).

En aquestes ocacions, si el sistema de control de versions és el [git](http://en.wikipedia.org/wiki/Git_(software) "Article de la Wikipedia anglesa sobre el sistema de control de versions distribuït Git") només heu de fer:

    # per veure què es netejarà
    git clean -n
    # per eliminar aquests fitxers
    git clean -f
    # si també voleu eliminar els directoris que s'hagin pogut crear
    git clean -fd

I amb això ja estarà tot net com una patena :)
