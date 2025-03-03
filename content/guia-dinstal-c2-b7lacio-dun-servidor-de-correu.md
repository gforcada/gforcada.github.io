Title: Guia d'instal·lació d'un servidor de correu
Date: 2010-01-23 15:29
Author: admin
Category: General
Tags: centos, correu electrònic, gentoo, programari lliure, redhat, servidor de correu
Slug: guia-dinstal%c2%b7lacio-dun-servidor-de-correu
Status: published

Ja fa dies que li estic donant voltes a crear un servidor de correu ja que com que segurament a la feina el necessitarem tard o d'hora així vaig practicant :)

Per sort em vaig quedar marevallat amb [linuxmail.info](http://www.linuxmail.info/ "Pàgina web on expliquen tots els detalls per configurar un servidor de correu amb linux"). Ho té tot, des de l'SMTP a crear usuaris nous, passant per l'accés (IMAP i POP), la seguretat (SSL, antivirus i antispam), la configuració, etc etc

A més, si ho ajunto amb la guia que hi ha a la [wiki de Gentoo](http://en.gentoo-wiki.com/wiki/Mail_server_using_Postfix_and_Dovecot "Article al wiki de Gentoo on s'explica com configurar un servidor de correu") ((linuxmail.info sembla centrat a RHEL i CentOS)) suposo que me'n sortiré.

Algunes idees a tenir en ment? Creieu que la sol·lució proposada ([Postfix](http://www.postfix.org/ "Lloc web del projecte de servidor de correu Postfix") + [Dovecot](http://www.dovecot.org/ "Lloc web del servidor d'IMAP i POP3 Dovecot") + PostfixAdmin + [ClamAV](http://www.clamav.net/ "Lloc web de l'antivirus ClamAV") + [Spamassassin](http://spamassassin.apache.org/ "Lloc web del projecte de filtre d'SPAM SpamAssassin")) és correcte? Sembla que aquest Dovecot aquest és prou bo tot i que és la primera vegada que n'he sentit a parlar. Fins i tot ofereixen [una recompensa de 1000€](http://dovecot.org/security.html "Pàgina on explica com obtenir 1000€ dell projecte Dovecot") per qui trobi un error de seguretat.

Lo dit, si teniu alguna guia amagada per algun lloc o consells de bones pràctiques, etc etc relacionades amb configurar i administrar servidors de correu sóc tot orelles!
