---
layout: post
title: "Google Chrome y los acentos en Linux Mint (Ubuntu y derivadas). IBus en Gtk+ y Qt"
date: 2014-11-29 19:48:00 +0200
categories: [Google, Linux, Navegadores Web]
---
Hace algunas semanas me percaté que nuestro navegador favorito, **Google Chrome**, no reconocía los acentos en Linux Mint, distribución basada en Ubuntu, por lo que esta última es la causante del problema. A la hora de escribirlos, y pulsar la tecla del acento, no se asociaba a la tecla que pulsabas posteriormente, un problema de codificación.

En un principio pensé que el problema derivaba de la configuración del lenguaje del teclado, pero me sorprendió ver que en cualquier editor de texto local no me ocurría.

Tal vez puedas pensar que para búsquedas en Google, no es un problema grave, pero si eres asiduo a utilizar la suite ofimática en la nube [Google Drive](https://www.google.com/drive/) para realizar documentos formales, es imposible trabajar.

### IBus y los acentos

[IBus](https://help.ubuntu.com/community/ibus) es el método de entrada que interpreta lo que escribimos y lo _traduce_ en los caracteres que queremos ver, es decir, cuando tecleamos _‘a_ lo que realmente queremos ver es _á_. **IBus** es la aplicación que se encarga de realizar esta operación en **Ubuntu **desde la versión **9.10** ya que en versiones anteriores utilizaba **SCIM**.

Ahora bien, llegados a este punto nos encontramos que para relacionarse con **IBus** los dos grandes sistemas para crear interfaces gráficas como son [Gtk+](http://www.gtk.org/) y [Qt](http://qt-project.org/) necesitan de sus particulares bibliotecas como son _ibus-gtk_ y su homóloga _ibus-qtk_ respectivamente.

### Solución

**Google Chrome** utiliza Qt, por lo que basta con instalar el paquete correspondiente para solucionarlo:

{% highlight sh %}
sudo apt-get install ibus-qt4
{% endhighlight %}

#### Más información:
* [IBus](https://code.google.com/p/ibus/)
* [Ubuntu](https://help.ubuntu.com/community/ibus)