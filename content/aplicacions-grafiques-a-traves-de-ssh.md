Title: aplicacions gràfiques a través de ssh
Date: 2007-12-16 00:18
Author: admin
Category: General
Tags: consells, programari lliure, ssh
Slug: aplicacions-grafiques-a-traves-de-ssh
Status: published

<img src="./wp-content/uploads/2007/11/openssh_logo.png" data-align="right" alt="logotip de l’Openssh" />ja fa temps que sabia que es podia fer, però pensava que seria quelcom complicat, que requerís editar un bon grapat de fitxers de configuració, saber com funcionen ben bé totes les parts i buscar molt per Internet, però resulta que és tan simple com:

    ssh -X usuari@màquina

ull que ha de ser x majúscula

un cop us heu autenticat a la màquina ja podeu cridar les aplicacions gràfiques des del terminal que es crearà una finestra nova amb el programa en concret :D

podeu aprofitar l'avinentesa per a passar-vos fitxers d'un directori local a un remot (o viceversa) etc etc
