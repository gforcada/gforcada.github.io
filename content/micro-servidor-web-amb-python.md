Title: Micro servidor web amb Python
Date: 2011-06-16 06:46
Author: admin
Category: General
Tags: consells, php, programació web, python
Slug: micro-servidor-web-amb-python
Status: published

[<img src="./wp-content/uploads/2008/07/python_logo.png" title="Logotip del Python" class="alignright size-full wp-image-377" width="110" height="110" />](./wp-content/uploads/2008/07/python_logo.png)Tot i que el llenguatge més utilitzat (o en el que pensa gairebé tothom) quan parla de pàgines web és [PHP](http://php.net "Pàgina web del llenguatge de programació PHP"), amb [Python](http://python.org "Pàgina web del llenguatge de programació Python") també es poden fer pàgines web :D

Un dels grans *què* del PHP és que engegues el servidor ([Apache](http://httpd.apache.org/ "Pàgina web del servidor HTTP Apache") normalment), poses un fitxer php en algun lloc accessible i *boom!* ja tens la pàgina funcionant al navegador.  
No se si existeix alguna cosa semblant, però amb Python encara ho pots fer més senzill (a mode de test i MAI en producció quedi clar):

    from wsgiref.simple_server import make_server

    def simple_app(environ, start_response):
        status = '200 OK'
        response_headers = [('Content-type','text/plain')]
        start_response(status, response_headers)
        return ['Hello world!\n']

    # run the server
    port = 8000
    httpd = make_server('', port, simple_app)
    print "Serving on port %i..." % port
    httpd.serve_forever()

 

Amb el codi d'aquí sobre en teniu prou d'anar canviant el que hi ha dintre la funció per tenir ja alguna cosa que es mostri en el navegador :)
