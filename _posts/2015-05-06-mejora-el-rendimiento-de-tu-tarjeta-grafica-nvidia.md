---
layout: post
title: "Mejora el rendimiento de tu tarjeta gráfica NVidia"
date: 2015-05-06 18:53:39 +0200
categories: [Trucos, Windows]
---
Os comparto un pequeño truco ~~ajuste~~ encontrado en [Reddit](http://www.reddit.com/r/GlobalOffensive/comments/343kmi/nvidia_users_how_to_turn_down_your_cpu_usage_and/) que mejora el rendimiento de tu **tarjeta gráfica NVidia** desactivando un servicio asociado al software de los drivers y que resulta innecesario en la mayoría de los casos.

![NVidia logo]({{"/assets/img/posts/2015/05/nvidia.png" | absolute_url }}){: .img-responsive .pull-right }

Se trata de una característica de la aplicación **GeForce Experience**, que supongo que tendrás instalado ya que NVidia prácticamente te obliga a instalarlo en cada actualización de los drivers.

El usuario _Anal-Cheese_ comenta que desactivando el **servicio de Windows** _"Nvidia Streamer Service"_ se consigue un ligero aumento de FPS. Este servicio, concretamente _"nvstreamsvc.exe"_, que está corriendo constantemente y se ejecuta al inicio, lo que hace es permitir el streaming al dispositivo Nvidia Shield, así que a no ser que tengas una de estas, no tiene sentido tenerlo constantemente en ejecución.

Tras realizar algunas pruebas con mi equipo (CPU i5 2500k + GTX560Ti), los resultados son un incremento de 200-220~ to 250-280~ FPS.

Es decir, no es un gran incremento pero siempre es bienvenido, sobre todo en tarjetas gráficas como la mía que ya tiene recorrido, o en tarjetas gráficas de gama media/baja.

![Servicio de Windows Nvidia Streamer Service]({{"/assets/img/posts/2015/05/nvidiastream.jpg" | absolute_url }}){: .img-responsive .margin-auto }

**NOTA:** En caso de que no uses GeForce Experience puedes obviar todo esto pues no tendrás el servicio corriendo.

[Post original](http://www.reddit.com/r/GlobalOffensive/comments/343kmi/nvidia_users_how_to_turn_down_your_cpu_usage_and/) en el subreddit de Counter Strike, [/r/GlobalOffensive](http://www.reddit.com/r/GlobalOffensive).