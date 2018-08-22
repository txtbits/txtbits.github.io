---
post: layout
title: "Texto vertical con CSS (cross-browser)"
date: 2014-04-03 19:44:03 +0200
categories: [Desarrollo, Diseño]
---
El otro día haciendo unos ajustes en un proyecto, sé me presentó la necesidad de tener que mostrar un texto orientado de forma vertical. Como soy un poco reacio a utilizar imágenes para estas cosas, prefiero buscar soluciones CSS que en la mayoría de casos de este tipo suelen existir.

Si queremos mostrar un texto vertical con css, basta con añadir al elemento html (p,  div..) una clase con los siguientes estilos:

{% highlight css %}
-webkit-transform: rotate(-90deg);
-moz-transform: rotate(-90deg);
-ms-transform: rotate(-90deg);
-o-transform: rotate(-90deg);
transform: rotate(-90deg);
filter: progid:DXImageTransform.Microsoft.BasicImage(rotation=3);
{% endhighlight %} 

Los grados por supuesto, podemos ajustarlo a nuestras necesidades.

Si quieres ampliar información visita [stackoverflow](http://stackoverflow.com/questions/1080792/how-can-i-draw-vertical-text-with-css-cross-browser).