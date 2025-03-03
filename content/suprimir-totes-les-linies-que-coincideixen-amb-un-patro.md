Title: suprimir totes les línies que coincideixen amb un patró
Date: 2008-01-18 23:12
Author: admin
Category: General
Tags: expressions regulars, GNOME traduccions, terminal, turc, vim
Slug: suprimir-totes-les-linies-que-coincideixen-amb-un-patro
Status: published

<img src="http://gil.badall.net/wp-content/uploads/2007/12/vimlogo.png" data-align="right" alt="logotip del vim" />tot editant fitxers turcs\[1\] tenia la necessitat de suprimir totes les línies que comencessin per msgstr\[1\] així que he anat a buscar per Internet i al final he trobat que amb el <a href="http://www.vim.org" target="_blank" rel="noopener">vim</a> pots fer:

    :%g/^msgstr\[1/d

i amb això suprimiràs en tot el fitxer totes les línies que comencin per msgstr\[1

\[1\] : l'altre dia actualitzant la <a href="http://badall.net:81/damned-lies/" target="_blank" rel="noopener">meva còpia</a> del <a href="http://l10n.gnome.org" target="_blank" rel="noopener"></a> que tinc a un dels servidors vaig veure que hi havia alguns mòduls que amb turc no passaven la comprovació *msgfmt -cv* així que li vaig demanar a en Baris si li feia res que ho arreglés i com que m'ha dit que sí és el que estic fent ara mateix :)
