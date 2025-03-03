Title: lsof
Date: 2009-02-13 11:17
Author: admin
Category: General
Tags: consells, terminal
Slug: lsof
Status: published

Si algun procés que utilitzi ports de la xarxa es penja i no el sabeu trobar amb un «*ps -aux*» i llavors al tornar a arrancar el procés uns dóna error perquè el port encara està ocupat podeu fer un «*lsof -i PROTOCOL: PORT*» canviant PORT per el número de port i PROTOCOL pel tipus de protocol que utilizi (majoritàriament TCP o UDP  segurament).

Amb això veureu quin és el procés que us està ocupant el port i després ja li podreu fer tranquilament un «*kill -9 PROCES*» i voilà, el port ja està lliure :)
