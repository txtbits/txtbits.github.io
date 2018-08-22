---
layout: post
title: "Solución: error while loading shared libraries: libudev.so.0: cannot open shared object file:"
date: 2014-11-21 12:41:16 +0200
categories: Linux
---
Al instalar algunos programas en Linux, podemos encontramos con la sorpresa de que tras la instalación, la aplicación no arranca. Un primer paso para elaborar un diagnóstico es, a través de un terminal lanzar el ejecutable y ver si devuelve algún tipo de error.

Esto es lo que me pasó al instalar [IsoPlex](http://isoplex.isohunt.to/) (y algunos usuarios también lo han reportado con la instalación de [Popcorn Time](https://popcorntime.io/). Tras la instalación, no me arrancaba y probé por terminal, el error que me devolvía era:

{% highlight sh %}
error while loading shared libraries: libudev.so.0: cannot open shared object file: No such file or directory
{% endhighlight %}

Para resolver el problema, simplemente tienes que crear un enlace simbólico con el siguiente comando:

{% highlight sh %}
sudo ln -s /lib/x86_64-linux-gnu/libudev.so.1 /usr/lib/libudev.so.0
{% endhighlight %}

¡Y listo!, ya podéis arrancar la aplicación sin problemas.

¡Saludos!