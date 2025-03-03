Title: Millorar el temps d'engegada de l'Ubuntu
Date: 2008-07-24 22:14
Author: admin
Category: General
Tags: consells, optimització, ubuntu
Slug: millorar-el-temps-dengegada-de-lubuntu
Status: published

Si esteu cansats d'esperar prop d'un minut a que s'engegui l'<a href="http://www.ubuntu.com" target="_blank" rel="noopener">Ubuntu</a> i no enteneu perquè coi li costa tant mostrar la pantalla d'inici, avui seguint <a href="http://www.tuxpan.com/fcatrin/es/comments.php?guid=20080722" target="_blank" rel="noopener">una marevallosa guia</a> he fet que l'Ubuntu del meu portàtil passi d'**engegar-se d'uns <a href="http://galeria.badall.net/main.php?g2_itemId=2222" target="_blank" rel="noopener">50</a> \[1\] segons a només <a href="http://galeria.badall.net/main.php?g2_itemId=2226" target="_blank" rel="noopener">26</a> segons**!

Em falta comprovar si treient l'usplash (la cosa gràfica aquesta tant bonica que mostra una barra de progrés i el logo d'Ubuntu) encara millora una mica. I si sapigués esbrinar que coi fa el modprobe \[2\] i el setkey segurament podria tenir la pantalla del <a href="http://www.gnome.org/projects/gdm/" target="_blank" rel="noopener">GDM</a> amb menys de 25 segons :)

\[1\] Abans de fer la primera comprovació ja havia suprimit uns quants serveis que no necessitava, de manera que enlloc dels 42 que marca el gràfic en serien uns quants més.

\[2\] D'acord, carrega mòduls del kernel, però necessita tant de temps i n'ha de carregar tants?! \[3\]

\[3\] Hauré de fer proves de compilar el <a href="http://kernel.org" target="_blank" rel="noopener">kernel</a> jo mateix amb tot a dintre i amb el mínim de mòduls possibles (i sense la quantitat de mòduls que hi deu haver i que no necessito) a veure si hi ha cap diferència :)
