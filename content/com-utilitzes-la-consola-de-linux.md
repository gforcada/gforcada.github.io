Title: com utilitzes la consola de Linux?
Date: 2007-06-26 22:36
Author: admin
Category: General
Tags: guifi, linux, meme, terminal
Slug: com-utilitzes-la-consola-de-linux
Status: published

seguint el meme d'en Xavi Ivars, aquí la meva sortida a l'ordre:

    history | awk '{print $2}' | awk 'BEGIN {FS="|"} {print $1}' | sort | uniq -c | sort -rn | head -10

114 ./winbox.exe  
95 exit  
63 sudo  
38 ping  
34 ssh  
26 iwlist  
24 cd  
22 ifconfig  
11 route  
11 ls

i si mirem l'usuari root:

129 ping  
91 ifconfig  
78 iwlist  
54 dhclient  
26 telnet  
26 exit  
21 route  
14 iwconfig  
10 cat  
8 ./winbox.exe

suposo que es nota que formo part de <a href="http://guifi.net" target="_blank" rel="noopener">guifi.net</a> amb totes les ordres de root :)
