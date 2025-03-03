Title: pas d'arguments amb Python
Date: 2008-12-05 21:39
Author: admin
Category: General
Tags: consells, programació, python
Slug: pas-darguments-amb-python
Status: published

<img src="http://gil.badall.net/wp-content/uploads/2008/07/python_logo.png" title="Logotip del Python" class="alignright size-full wp-image-377" width="110" height="110" />  
Per pas d'arguments s'entén que quan crides una funció li dius amb quins valors vols que faci la seva funció.

Per exemple:

> suma(3,4) \# retorna 7  
> suma(4,5) \# retorna 9

El problema pot passar (com m'acabo de trobar i solucionar) en que si haig de passar força arguments (6 en concret) i a més els haig de redirigir es fa pesat mantenir les llistes d'arguments sincronitzades, per exemple si tenim un parell de classes que una hereda (Secundaria) de l'altre (Principal) i volem cridar el constructor de Principal des del constructor de Secundaria haurem de fer una cosa per l'estil:

> class Principal():  
> def \_\_init\_\_(self, primer, segon, tercer, quart, cinquè, sisé):  
> /\* ... operem amb ells ...\*/  
> class Secundaria (Principal):  
> def \_\_init\_\_(self, primer, segon, tercer, quart, cinquè, sisé):  
> Principal.\_\_init\_\_(primer, segon, tercert, quart, cinquè, sisé)

Per a simplificar-ho [Python](http://www.python.org/ "Lloc web del llenguatge de programació Python") ens permet diverses coses:

- valors predeterminats: Si sabem que un valor serà gairebé sempre el mateix i en contades vegades un de diferent podem fer que sigui opcional donant-li un valor des de la declaració de la funció
- llista d'arguments: Si no sabem quants arguments (o no ens importa) podem dir que els agafi tots
- diccionari d'arguments: Si el que volem es enviar les dades però no ens recordem de l'ordre en que estan posats en la declaració (per exemple si fem taula_multiplicar(3,5,7) però volíem la taula del 7 del 3 al 5 ens trobarem amb la taula del 3 del 5 al 7) podem fer servir els noms dels arguments

També es poden fer coses més sofisticades i complicades com barrejar llistes, diccionaris, valors predeterminats i paràmetres normals, per exemple:

> def funcio_estranya( valor_posicional, valor_predeterminat=5, \*resta_arguments): \# amb aixo creem una funció que el primer paràmetre es un de normal, després en bé un d'opcional i la resta hauran de ser una llista d'arguments variable

No està malament eh :)
