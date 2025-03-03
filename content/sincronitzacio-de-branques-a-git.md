Title: Sincronització de branques a git
Date: 2010-08-16 06:58
Author: admin
Category: General
Tags: consells, git, programació
Slug: sincronitzacio-de-branques-a-git
Status: published

[<img src="./wp-content/uploads/2009/03/git-logo.png" title="git-logo" class="alignright size-full wp-image-540" width="73" height="28" />](http://gil.badall.net/wp-content/uploads/2009/03/git-logo.png)És *box-populi* que treballar amb branques amb [git](http://git-scm.com/ "Lloc web del programa de control de versions git") és una delícia ja que ho facilita moltíssim: és molt ràpid i les eines que et posa a disposició per treballar-hi fan que sigui molt recomanable fer-ho per a qualsevol canvi que es vulgui fer en el codi d'una aplicació.

Ara bé, quan ja has fet els canvis que volies fer-hi com els sincronitzes cap a la branca master ((Així és com es diu la branca principal a git.)) ?

Tens dues opcions, la que utilitzava jo fins ara:

> git checkout master  
> git diff --stat master..*BRANCA_DEV*  
> git merge master..*BRANCA_DEV*  
> git push

Amb això el que obtenim és que agafem tots els canvis que hi ha a *BRANCA_DEV* respecte de master i els mescla. A més a més per deixar-ne constància en fa un commit final amb la típica frase ((Com tot en el git es pot canviar)) "*Merge branch 'BRANCA_DEV' into master*".

Ara bé, hi ha una manera més bonica i més elegant de fer-ho, rebase:

> git checkout master  
> git rebase *BRANCA_DEV*  
> git pull  
> git push

Amb això el que estem fent és agafar els canvis de la branca *BRANCA_DEV* i els col·loca, en bloc, abans dels canvis que tinguem fets a la branca master. Això vol dir que si partim d'un commit X i fem tres canvis a la branca *BRANCA_DEV* i dos canvis a la branca master, quan executem les ordres de sobre el farà el git és reiniciar els commits fins al commit X, aplicar consecutivament els 3 commits de *BRANCA_DEV* i finalment un cop fet això aplicarà els nostres dos canvis a la pròpia branca master.

D'aquesta manera, sigui quin sigui el mètode utilitzat per sincronitzar les branques ja tindreu una manera molt fàcil de treballar amb diverses branques alhora, etc etc
