Title: com enganxar al Vim sense que es re-formati
Date: 2010-07-04 09:27
Author: admin
Category: General
Tags: consells, terminal, vim
Slug: com-enganxar-al-vim-sense-que-es-re-formati
Status: published
Attachments: wp-content/uploads/2010/07/codi-exemple.png, wp-content/uploads/2010/07/vim-abans-paste.png, wp-content/uploads/2010/07/vim-despres-paste.png

Segur que els que utilitzeu el [Vim](http://en.wikipedia.org/wiki/Vim_%28text_editor%29 "Entrada a la wikipedia anglesa sobre l'editor de text de terminal Vim") ja n'heu buscar la solució ja que realment és molt molest.

Si aneu a una pàgina web i en copieu el codi font d'un tros de programa, per exemple:

[<img src="http://gil.badall.net/wp-content/uploads/2010/07/codi-exemple-280x300.png" title="codi-exemple" class="aligncenter size-medium wp-image-935" width="280" height="300" />]({static}wp-content/uploads/2010/07/codi-exemple.png)

Us trobareu que un cop enganxat al terminal queda tot el codi reformatat:

[<img src="http://gil.badall.net/wp-content/uploads/2010/07/vim-abans-paste-300x220.png" title="vim-abans-paste" class="aligncenter size-medium wp-image-936" width="300" height="220" />]({static}wp-content/uploads/2010/07/vim-abans-paste.png)

Per sort amb el Vim li pots dir que no reformati el codi:

[<img src="http://gil.badall.net/wp-content/uploads/2010/07/vim-despres-paste-300x220.png" title="vim-despres-paste" class="aligncenter size-medium wp-image-937" width="300" height="220" />]({static}wp-content/uploads/2010/07/vim-despres-paste.png)

El truc està en que abans d'enganxar al terminal ens posem en mode control i establim l'opció **paste**) o sigui, la seqüència és:

- *(obres el fitxer)*
- Passes a mode ordre (amb la tecla Esc)
- escrius **:set paste**
- tornes a mode edició (amb la tecla i)
- ja pots fer un Ctrl+Maj+V per enganxar el que tinguis al porta-retalls

Llestos ja tenim un bon tros de codi que no hem de picar i que a més continua ben formatat :)

*  
*
