---
layout: post
title: "Bootstrap Framework: anchos de columna personalizados en tablas."
date: 2015-07-09 19:39:14 +0200
categories: Diseño
---
En la versión 3 de [Bootstrap](https://getbootstrap.com/docs/3.3/) apareció la posibilidad de hacer las tablas responsive y adaptar de forma dinámica el contenido. Sin embargo, no hay mayor flexibilidad en cuanto a la manipulación de tamaño de las columnas. A continuación, explico un truco muy simple para los que se han topado con el problema de querer tener anchos de columna personalizados en tablas en Bootstrap.

Partimos del siguiente ejemplo de tabla:

{% highlight html %}
<table class="table table-condensed table-striped">
    <thead>
        <tr>
            <th>Id</th>
            <th>Nombre</th>
            <th>Descripcion</th>
        </tr>
    </thead>
    <tbody>
        {%raw%}{% for elem in elementos %}
            <tr>
                <td>{{elem.id}}</td>
                <td>{{elem.nombre}}</td>
                <td>{{elem.descripcion}}</td>
            </tr>
        {% endfor %}{%endraw%}
    </tbody>
</table>
{% endhighlight html %}

Digamos que una vez que se procesa la tabla, el campo _descripción_ es demasiado grande y empuja el resto de columnas haciéndolas más pequeñas de lo que deberían ser. La forma más rápida de solucionar este problema es simplemente dar tamaños de las columnas de los encabezados de la tabla. Para ello, podemos aprovecharnos de las clases que nos proporciona el grid de Bootstrap:

{% highlight html %}
<table class="table table-condensed table-striped">
    <thead>
        <tr>
            <th class="col-sm-2">Id</th>
            <th class="col-sm-4">Nombre</th>
            <th class="col-sm-6">Descripcion</th>
        </tr>
    </thead>
    <tbody>
        {%raw%}{% for elem in elementos %}
            <tr>
                <td>{{elem.id}}</td>
                <td>{{elem.nombre}}</td>
                <td>{{elem.descripcion}}</td>
            </tr>
        {% endfor %}{%endraw%}
    </tbody>
</table>
{% endhighlight html %}

Sea cual sea el ancho de la tabla de cabeceras tus datos de la tabla se ajustarán a ese tamaño.

Muy sencillo y funciona a la perfección.

**Bonus:** Esto funciona también en Bootstrap 2, usando las clases span* en su defecto (para los que como yo, sigan desarrollando en sitios web que necesiten un extra de compatibilidad con navegadores antiguos).