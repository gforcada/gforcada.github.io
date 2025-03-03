Title: Configurar un servidor de correu
Date: 2010-06-25 13:00
Author: admin
Category: General
Tags: dovecot, gentoo, postfix, ssl
Slug: configurar-un-servidor-de-correu
Status: published

[<img src="./wp-content/uploads/2007/11/glogo-small.png" title="logotip de gentoo" class="alignright size-full wp-image-224" width="146" height="149" />](http://gil.badall.net/wp-content/uploads/2007/11/glogo-small.png)Avui per fi després de batallar molt he aconseguit fer funcionar el correu que he configurat en el servidor que tenim a casa.

Els programes són [Postfix](http://www.postfix.org "Lloc web del projecte d'SMTP Postfix") i [Dovecot](http://www.dovecot.org/ "Lloc web del projecte d'IMAP i POP Dovecot") (només IMAP). La complexitat ha estat en fer funcionar correctament tant el Postfix com el Dovecot amb SSL.

Com que el servidor corre amb Gentoo he utilitzat com a base les guies següents:

- [Configuració inicial del Postfix i el Dovecot](http://en.gentoo-wiki.com/wiki/Mail_server_using_Postfix_and_Dovecot "Entrada al wiki de Gentoo sobre com configurar el Postfix i el Dovecot")
- [Configuració del Dovecot i l'SSL](http://en.gentoo-wiki.com/wiki/Dovecot/TLS "Guia al wiki de Gentoo per configurar el Dovecot amb SSL")
- [Configuració del Postfix i l'SSL](http://en.gentoo-wiki.com/wiki/Postfix/TLS "Entrada a la wiki de Gentoo sobre com configurar el Postfix amb SSL") (obvien la part de la creació del certificat, per la resta tot és útil)

I finalment per fer que el Postfix funcioni correctament amb l'SSL he seguit [la guia de nixcraft.com](http://nixcraft.com/getting-started-tutorials/3075-postfix-mail-server-create-self-signed-ssl-certificates-cent-os-redhat-linux.html "Guia de com fer funcionar correctament el Postfix amb SSL"). M'ha calgut aquesta guia perquè com el certificat és auto-signat, per als que paguin un certificat no els caldrà entenc.

Amb tot això i una mica de paciència ja tindreu un servidor de correu casolà funcionant :)
