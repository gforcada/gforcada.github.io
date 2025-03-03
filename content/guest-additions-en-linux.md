Title: Guest Additions en Linux
Date: 2008-05-29 01:22
Author: admin
Category: General
Tags: consells, linux, virtualbox
Slug: guest-additions-en-linux
Status: published

<img src="./wp-content/uploads/2008/03/vbox.png" data-align="right" alt="logo del virtualbox" />Fa uns dies comentava que per <a href="?p=327" target="_blank" rel="noopener">compartir carpetes</a> i tenir <a href="?p=330" target="_blank" rel="noopener">integració de finestres</a> calia instal·lar les *Guest Additions* al Windows.

Doncs bé, per fer-ho a Linux no es gaire més complicat :)

Només hem de muntar la ISO de les Guest Additions al Linux i (almenys a mi no m'ha funcionat) ignorar l'avís d'arrencada automàtica.

Naveguem pel disc que acabem de muntar i executem en un terminal el fitxer VBoxLinuxAdditions.run.

Un cop ho ha instal·lat tot podeu afegir línia al fitxer ~/.xinitrc que posi:

98vboxadd-xclient

Ara ja podeu reiniciar i podreu redimensionar la pantalla a gust i tindreu la integració de ratolí.

Per a compartir carpetes entre dos Linux <a href="http://virtualbox.org/wiki/Sharing_files_on_OSE" target="_blank" rel="noopener">hi ha un document</a>\[1\] a la pàgina oficial del <a href="http://www.virtualbox.org" target="_blank" rel="noopener">Virtualbox</a>, encara no ho he investigat tot i així :)

\[1\] També hi ha un <a href="http://virtualbox.org/download/1.6.0/UserManual.pdf" target="_blank" rel="noopener">manual complet</a> de 211 pàgines que deu explicar-ho també, però tampoc me l'he mirat del tot encara
