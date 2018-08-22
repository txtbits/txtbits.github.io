---
layout: post
title: "Trabajar con reStructuredText: Docutils y rst2pdf"
date: 2011-10-28 18:53:00 +0200
categories: [Desarrollo, Ofimática]
---
Hace unos años, era habitual al realizar trabajos, escribir cartas, o documentos, utilizar ~~MS Office~~ un procesador de textos. En la actualidad, nos encontramos que la información se presenta en la mayoria de los casos en formato PDF, o incluso directamente documentos web en HTML.

Desde hace poco, vengo utilizando una herramienta que de forma sencilla, puedes obtener un documento en PDF/HTML de un simple documento de texto (.txt) siguiendo unas simples pautas con la información.

Este modo de estructurar la información se llama [reStructuredText](http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html).

## ¿Qué es?
> reStructuredText es un lenguaje de marcas ligero, de fácil lectura en su formato de fuente pero muy versátil para producir documentos complejos.

## ¿Qué puedo hacer?
> * Escribo la documentación en texto plano y después la convierto a distintos formatos.
* Soporta versionado porque es texto.
* Se puede leer con cualquier editor.
   
Los documentos se puede convertir a muchos formatos diferentes, a destacar: PDF y HTML.
  
Además, permite utilizar hojas de estilos predeterminadas para incluir en la conversión, lo cual hace que puedas crear un documento PDF o HTML "curioso" con unos sencillos pasos.

A continuación detallo las instrucciones para instalar esta aplicación en Windows:

* Instalo [Python](http://www.python.org/download)
* Instalo setuptools
  * Descargar y ejecutar el archivo peak.telecommunity.com/dist/ez_setup.py desde el intérprete de comandos (**cmd**).
  ```
  C:\Python27\python.exe ez_setup.py
  ```
* Instalo docutils
  * Descargar y descomprimir [docutils](http://docutils.sourceforge.net/docutils-snapshot.tgz)
  * Ejecutar el archivo setup.py dentro de la carpeta descomprimida o:
    ```
    C:\Python27\python.exe setup.py install
    ```
* Descargar e instalar Reportlab:
  * Para 32 bits: [reportlab-2.5.win32-py2.7.exe](http://www.reportlab.com/ftp/reportlab-2.5.win32-py2.7.exe)
  * Para 64 bits: [reportlab-2.5.win-amd64-py2.7.exe](http://www.reportlab.com/ftp/reportlab-2.5.win-amd64-py2.7.exe)
* Instalo rst2pdf
  * Descargar [rst2pdf](http://code.google.com/p/rst2pdf/source/checkout)
  * Hace falta un cliente de subversión para descargarlo (como [tortoiseSVN](http://tortoisesvn.tigris.org/)).

Para Linux, es bastante sencillo, simplemente hace falta instalar Python, y posteriormente docutils y rst2pdf.
  
### Ejemplos de utilización desde intérprete de comandos (**cmd**):
    
```
C:\Python27\scripts\rst2html origen.rst destino.html
C:\Python27\scripts\rst2pdf origen.rst -o destino.pd
C:\Python27\scripts\rst2pdf origen.rst -s estilo.style -o  destino.pdf
```

### Enlaces de interés:
* [http://sphinx.pocoo.org/rest.html](http://sphinx.pocoo.org/rest.html)
* [http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html](http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html)
* [http://people.ee.ethz.ch/~creller/web/tricks/reST.html](http://people.ee.ethz.ch/~creller/web/tricks/reST.html)
* Manual de rst2pdf (y rst en general):  
  [http://lateral.netmanagers.com.ar/static/manual.pdf](http://lateral.netmanagers.com.ar/static/manual.pdf)
* Presentación rst:  
  [http://catherinedevlin.pythoneers.com/presentations/rst/olf.html](http://catherinedevlin.pythoneers.com/presentations/rst/olf.html)
* Tutorial en francés:  
  [http://culot.org/public/Docs/documentation_rest.html](http://culot.org/public/Docs/documentation_rest.html)