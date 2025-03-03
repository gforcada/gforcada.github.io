Title: tree
Date: 2008-06-12 01:53
Author: admin
Category: General
Tags: consells, terminal
Slug: tree
Status: published

Aquesta ordre no planta arbres (per desgràcia) però si que fa uns llistats molt bonics:

  
`xurrasco svn # tree -a`  
`.`  
`|-- conf`  
`` `-- repos ``  
`` `-- damn-ob ``  
`|-- README.txt`  
`|-- conf`  
`| |-- authz`  
`| |-- passwd`  
`` | `-- svnserve.conf ``  
`|-- dav`  
`|-- db`  
`| |-- current`  
`| |-- format`  
`| |-- fs-type`  
`| |-- revprops`  
`` | | `-- 0 ``  
`| |-- revs`  
`` | | `-- 0 ``  
`| |-- transactions`  
`| |-- uuid`  
`` | `-- write-lock ``  
`|-- format`  
`|-- hooks`  
`| |-- post-commit.tmpl`  
`| |-- post-lock.tmpl`  
`| |-- post-revprop-change.tmpl`  
`| |-- post-unlock.tmpl`  
`| |-- pre-commit.tmpl`  
`| |-- pre-lock.tmpl`  
`| |-- pre-revprop-change.tmpl`  
`| |-- pre-unlock.tmpl`  
`` | `-- start-commit.tmpl ``  
`` `-- locks ``  
`|-- db-logs.lock`  
`` `-- db.lock ``

Gens malament per ser un terminal, a més si teniu habilitats els colors, us marca els directoris i d'altres (diria que deu fer servir els colors de l'ls) :)

**EDICIÓ**: realment és veu millor, ja que pel que veig el WordPress li agrada menjar-se les tabulacions ... proveu-ho en el vostre propi terminal a veure què surt ;)
