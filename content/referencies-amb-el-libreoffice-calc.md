Title: Referències amb el LibreOffice calc
Date: 2011-09-30 05:02
Author: admin
Category: General
Tags: consells, libreoffice
Slug: referencies-amb-el-libreoffice-calc
Status: published

No us heu trobat mai amb la situació de que teniu un llibre de càlcul amb un full amb moltes dades tabulades i que des d'un altre full hi voleu accedir-hi?

## Eus aquí la sol·lució:

> =INDIRECTE(ADREÇA(G12;G13;1;1;"Full4"))

La funció ADREÇA genera una adreça (estil A1 o fullX.\$B\$1) amb els paràmetres que li passem, de manera que els podem generar dinàmicament, en l'exemple heu d'emplenar els camps G12 i G13 amb els nombres de la fila (G12) i la columna (G13, **també com a nombre!**).

La funció INDIRECTE agafa una adreça, en aquest cas prèviament generada amb la funció ADREÇA, i ens retorna el seu valor, de manera que si a G12 i G13 i tenim els valors 2 i 3, el resultat d'aquesta fórmula serà el valor que hi ha a la fila 2 columna C (columna 3) del full "Full4".

**Molt útil si teniu un full ple de dades i hi voleu fer càlculs des d'altres fulls.**
