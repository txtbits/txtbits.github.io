---
layout: post
title: "Hacer funcionar los puertos USB en las máquinas virtuales creadas con Virtual Box en Ubuntu 11.04,11.10,12.04 LTS, 12.10, 13.04, 13.10"
date: 2013-10-16 13:58:00 +0200
categories: Sistemas
---
Debido al comienzo de mi F.P.G.S en Desarrollo de Aplicaciones Multiplataforma, me he visto en la obligación para ciertas asignaturas de volver al ~~incomparable~~ Microsoft Windows.  
Por supuesto, como no quería tener que instalarlo de forma nativa, lo he instalado en una máquina virtual con el programa [Virtual Box](https://www.virtualbox.org/) de Oracle.

Tras instalar Microsoft Windows 7 en la misma, mi sorpresa fue que al intentar conectar un dispositivo USB (de almacenamiento en este caso, pero de cualquier tipo), la instalación del driver en la maquina virtual fallaba.

Tras buscar un poco, he visto que el problema no lo tenía la máquina virtual en sí, si no que no disponía de permisos en el grupo *vboxusers* de Ubuntu.

Los pasos a seguir son los siguientes (desde un terminal):

{% highlight sh %}
sudo adduser miusuario vboxusers

sudo usermod -aG vboxusers miusuario
{% endhighlight %} 

**Nota:** Véase que en donde pone *miusuario* hay que modificarlo por el propio de cada uno.

Otras de las cosas que me he preocupado, es en verificar que en la configuración de la propia máquina virtual tenga en la pestaña USB, la opción de Habilitar controlador 2.0 (EHCI) marcada, para habilitar el soporte para usb 2.0

Por otro lado, también tener instaladas las VirtualBox Guest Additions, para soporte gráfico, integración del puntero del ratón, carpetas compartidas, etc.