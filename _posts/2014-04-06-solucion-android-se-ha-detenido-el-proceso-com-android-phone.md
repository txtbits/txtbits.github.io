---
layout: post
title: "[SOLUCIÓN] Se ha detenido el proceso com.android.phone - Android"
date: 2014-04-06 12:35:13 +0200
categories: Android
---
En esta entrada os voy a contar un problema con el que tuve que lidiar hace bastante tiempo, cuando mi Nexus 4, sé actualizó a la versión 4.3 de Android sufriendo el fatídico error.

![Interfaz de Google Docs]({{"/assets/img/posts/2014/04/com.android.phone.png" | absolute_url }}){: .img-responsive .pull-right }

Sí, es cierto que vamos por versión 4.4.2, y que la versión 4.4.3 no faltará mucho para que sea lanzada, pero este problema por lo que he podido ver en blogs y foros, puede ocurrir al actualizar cualquier versión, no es especifica de la actualización a 4.3

Al actualizar de versión mediante OTA, todos nuestros datos, configuraciones y aplicaciones se mantienen "intactas" (cierto, lamentablemente no siempre es así) por lo que la nueva actualización en definitiva lo que hace es modificar los ficheros antiguos por los nuevos. En este proceso, a veces se genera un error al machacar los datos que tiene el teléfono para las teleoperadoras, es decir, para conectarnos a nuestra teleoperadora, y poder recibir señal para llamadas y datos.

Nos ponemos en situación:
  
Actualizo mi dispositivo Android a la nueva versión, finaliza la instalación de la nueva versión, sé reinicia el terminal y a partir del momento en el que vuelvo a introducir el PIN, constantemente y cada pocos segundos aparece un mensaje diciendo:

```
Se ha detenido el proceso com.android.phone
```

Si, si... Constamente, cada vez que aceptamos el error, sé vuelve a reproducir a los pocos segundos...

## Solución:

1. Debemos ser raudos y veloces, para que entre los segundos de margen que nos deja tras aceptar el mensaje de error, entrar en la configuración de APN, y seguidamente poner nuestro dispositivo en Modo Avión.  
Es complicado, pero con unos cuantos intentos sé puede conseguir, nos metemos en el menú de configuración de APN, desplegamos los Ajustes Rápidos (el menú derecho del desplegable de las notificaciones) y pulsamos en Modo Avión.  
Hay que hacerlo en este orden, puesto que si ponemos el Modo Avión primero, el sistema no nos deja acceder a la configuración de APN.
2. Una vez aquí, ya no saltará el mensaje de error. Por lo que podemos descansar unos segundos. 🙂
3. Tenemos que eliminar **todas** las APN de operadoras que tengamos guardadas.
4. Buscar la información que nos ofrece nuestra operadora para crear un nuevo APN de forma manual e insertarlo. En la página web de la operadora os ofrecerá información sobre estos datos, incluso podéis llamar al número de atención al cliente y os lo dirán por teléfono). Nota: No os olvidéis de dar al botón inferior de guardar al insertar los datos.
5. Una vez estemos en este paso, ya sólo hace falta quitar el Modo Avión y ¡listo!. A los pocos segundos os cogerá cobertura y conexión de datos y no volverá a reproducirse el error.  
**Nota:** Si esto no ocurriera, revisad los datos de APN que habéis introducido porque seguramente sean incorrectos.

Genera bastante rechazo que encima que te ilusiona recibir una nueva actualización de tu sistema, sabiendo lo cotizadas que están en Android (dichosa fragmentación...) y que en el primer arranque, nos encontremos con este tipo de problemas, que directamente no dejan hacer absolutamente nada en nuestro terminal al mostrar el error en una notificación modal.

Con estas indicaciones, seguro que lo solucionáis, pero si no fuera así, no dudéis en comentarme y trataré de echaros una mano.

Información adicional en: <http://www.htcmania.com/showthread.php?t=651380>

**Actualización:** Parece ser que una alternativa que les está funcionando a muchos usuarios es desactivar la actualización automática de la fecha y hora desde Ajustes -> Fecha y Hora

¡Saludos!