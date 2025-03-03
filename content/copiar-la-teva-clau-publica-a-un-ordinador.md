Title: copiar la teva clau pública a un ordinador
Date: 2007-11-02 17:50
Author: admin
Category: General
Tags: consells, gentoo, programari lliure, ssh
Slug: copiar-la-teva-clau-publica-a-un-ordinador
Status: published
Attachments: wp-content/uploads/2007/11/glogo-small.png, wp-content/uploads/2007/11/openssh_logo.png

<img src="{static}wp-content/uploads/2007/11/openssh_logo.png" data-align="right" alt="logotip de l’Openssh" />si us heu trobat que heu d'administrar diversos servidors i n'esteu farts de teclejar les contrasenyes de segur que heu descobert el sistema d'autenticació basat en claus públiques i claus privades, amb les quals a partir d'aquell moment en que tot el sistema està apunt ja no hauràs de teclejar mai més la contrasenya de l'usuari de la màquina remota a la que et connectaràs

doncs bé, com que per fer el procés has de copiar un fitxer (la clau pública) que tens localment a l'altre màquina es una mica rollo i tal, per sort hi ha gent que s'ho curra molt i avui hi he trobat una sol·lució molt ràpida i bona:

    ssh-copy-id -i ~/.ssh/id_dsa.pub usuari@màquina

i amb això ja tindrem copiada la nostra clau pública per poder entrar en aquella màquina com a l'usuari que hem especificat

llegit a <a href="http://gentoo-wiki.com/SECURITY_SSH_without_a_password" target="_blank" rel="noopener">Gentoo-wiki</a>
