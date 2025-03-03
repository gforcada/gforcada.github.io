Title: instal·lació d'un SVN
Date: 2007-07-25 23:46
Author: admin
Category: General
Tags: damned-lies, GNOME, svn
Slug: instal%c2%b7lacio-dun-svn
Status: published

ja fa temps que vull posar un <a href="http://subversion.tigris.org/" target="_blank" rel="noopener">Subversion</a> al servidor on hi ha aquest bloc, el de la Sílvia i demés històries

en el servidor hi ha una <a href="http://www.gentoo.org" target="_blank" rel="noopener">Gentoo</a> i seguint la <a href="http://gentoo-wiki.com/SVN" target="_blank" rel="noopener">guia de la gentoo-wiki d'instal·lació d'un SVN</a> em quedo encallat en el moment de:

      3. check that

            ssh yourhost "which svnserve"

         returns /usr/local/bin/svnserve and not /usr/bin/svnserve. If the

         latter is the case, ssh does not search /usr/local/bin for the

         svnserve command.     To change that, you can use the PAM module pam_env.so which is usually

         included in /etc/pam.d/ssh via system-auth. pam_env's config file is

         /etc/security/pam_env.conf and by adding

            PATH OVERRIDE=/usr/local/bin:/usr/bin:/bin

         you instruct it to set this particular path for all system-auth services.

encara no he arribat a entendre això del PAM i on s'ha de posar tot plegat i demés ... alguna idea?

m'he començat a mirar <a href="http://svnbook.red-bean.com/nightly/en/index.html" target="_blank" rel="noopener">el llibre del subversion</a> a veure si em serveix, però essent com és el Gentoo que ho canvia tot de baix a dalt no se com anirà :(

segons la guia aquesta del gentoo-wiki.com hi ha 4 maneres de fer servir el svn, jo he triat la de svn+ssh perquè d'aquesta manera tens l'autenticació a través de ssh, que sempre va bé

és aquesta suposició correcte? quins avantatges i/o inconvenients tenen les quatre maneres?
