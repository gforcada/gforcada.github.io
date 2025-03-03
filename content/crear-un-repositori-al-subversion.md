Title: crear un repositori al subversion
Date: 2008-06-22 14:41
Author: admin
Category: General
Tags: consells, programació, svn, terminal
Slug: crear-un-repositori-al-subversion
Status: published

En el servidor executeu:

    repositori=NOM_PROJECTE

    svnadmin create /var/svn/repos/$repositori
    chown -R apache:svnusers /var/svn/repos/$repositori
    chown -R g-w /var/svn/repos/$repositori
    chown -R g+rw /var/svn/repos/$repositori/db
    chown -R g+rw /var/svn/repos/$repositori/locks

En el client (per ssh) \[1\]:

    svn import -m"comentari"  FITXERS_A_IMPORTAR svn+ssh://USUARI@MÀQUINA/var/svn/repos/$repositori

En el client (per http) \[2\]:

    svn import -m"comentari" FITXERS_A_IMPORTAR http://MÀQUINA/svn/$repositori

\[1\] \[2\] Evidentment, s'ha de configurar tant l'ssh com l'apache perquè ho permetin :)
