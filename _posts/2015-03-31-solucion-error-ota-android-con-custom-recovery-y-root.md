---
layout: post
title: "[SOLUCIÓN] Error OTA Android con custom recovery y root"
date: 2015-03-31 18:37:22 +0200
categories: Android
---
**IMPORTANTE:** Este tema es para usuarios avanzados con conocimientos sobre Custom ROMs Android. He condensado los pasos a seguir para solucionar el error del título. No me hago responsable de posibles bricks, pero estoy abierto a cualquier petición de ayuda. 🙂

Hace un par de días me saltó la actualización vía **OTA de Android 5.1** en mi Nexus 10, la cual llevaba pensando en instalar de forma manual desde el día de publicación, pero por falta de tiempo no lo había hecho. Mi tablet estaba con **stock ROM Android 5.0** pero tenía modificado el stock recovery por **TWRP Recovery** y también con **permisos root** gracias a superSU.

**En este estado, es importante saber que la instalación de la OTA no se puede hacer mediante el método directo**, pulsando instalar mediante la notificación de "actualización disponible" y hacer una instalación limpia de fábrica supone el perder todos los datos de aplicaciones, así que intenté de forma manual a través de  TWRP Recovery.

Al tratar de instalar el update.zip me aparecían los siguientes errores:

{% highlight sh %}
script aborted: "/system/bin.install-recovery.sh" has unexpected contents.

script aborted: "/system/bin/app_process" has unexpected contents.
{% endhighlight %}

Mi primer paso ha sido volver a recuperar el stock recovery, para ello me he descargado la imagen de fabrica correspondiente a mi Nexus 10 desde la página de desarrolladores de Google donde se encuentran las imágenes de fabrica de todos los Nexus: [Factory Images for Nexus Devices](https://developers.google.com/android/nexus/images) y me he descargado la **nueva versión de Android** correspondiente a mi dispositivo a la que quiero actualizar.  Tras esto, los únicos ficheros que tienes que **flashear con fastboot** son los que describo a continuación:

{% highlight sh %}
fastboot flash system system.img
fastboot flash boot boot.img
fastboot format cache
fastboot reboot
{% endhighlight %}

** boot.img es necesario si deseas instalar la actualización OTA.

De este modo se os actualizará el dispositivo sin problemas y por supuesto, **sin perder los datos**.

Más información: [XDA-Developers](http://forum.xda-developers.com/showthread.php?t=2380113&page=41)

&nbsp;