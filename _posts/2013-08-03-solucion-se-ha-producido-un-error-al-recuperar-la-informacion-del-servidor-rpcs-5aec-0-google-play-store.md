---
layout: post
title: "[SOLUCIÓN] \"Se ha producido un error al recuperar la información del servidor. [RPC:S-5:AEC-0]\" Google Play Store"
date: 2013-08-03 12:20:00 +0200
categories: Android
---
Hoy escribo estas líneas para tratar de solucionar este error repentino que me surgió en mi tablet Nexus 10 y que puede traer algún que otro dolor de cabeza.

El problema apareció de repente, al tratar de actualizar (y también instalar) aplicaciones de Google Play Store. En todo momento me aparecía en la barra de notificaciones el siguiente mensaje:

```
"Se ha producido un error al recuperar la información del servidor. [RPC:S-5:AEC-0]"
```

Tengo que decir, que este problema es posible que sea raíz de que intente forzar la actualización OTA (Over The Air) de mi Nexus 10 a Android 4.3 eliminando los datos de aplicación del Marco de Aplicaciones de Google.

Existen varias posibilidades de solución, por lo que he leído a unos les ha funcionado una, y otros otra, entiendo que será a raíz de que el problema se reproduce de diferentes formas y/o acciones.

Por este motivo, voy a listar las opciones y la cosa es ir probando a ver cual os soluciona el problema.

Voy a ponerlas de mayor a menor prioridad.

* **Opción 1: Borrar los datos del Marco de Aplicaciones de Google**
  Entrando en Ajustes -> Aplicaciones -> Todas -> Marco de Aplicaciones de Google.
  Forzamos cierre de la aplicación y borramos datos (hasta que eliminé completamente los datos y desactive el botón, recalco esto porque a veces no se eliminan todos los datos a la primera).
* **Opción 2: Eliminar la cuenta de Google del teléfono**
  Entrando en Ajustes -> Cuentas -> [Cuenta de Google] -> Eliminar cuenta.
  <span style="color: red;">**OJO:**</span> Te aparece un aviso de que se pueden perder algunos datos ¡Tenlo en cuenta! (las apps no se pierden).
* **Opción 3: Restablecer datos de fábrica**
  Entrando en Ajustes -> Copia de seguridad -> Restablecer datos de fábrica.
  De este modo borramos <span style="color: red;">**TODO**</span> el contenido del télefono, dejandolo en un estado como cuando lo desempaquetamos por primera vez de la caja al adquirirlo (claramente no se haya desbloqueado el terminal e instalado una Custom ROM)
* **Opción 4: Instalar Imagen de Fabrica de nuestro terminal, o en su defecto una Custom ROM.**
  Como ultima alternativa, aunque os aseguro que no vais a llegar a esta ultima opción, se puede reinstalar por completo el sistema operativo Android en vuestro terminal.
  Añado esta opción puesto que si elegís instalar una Custom ROM, en la mayoría de los casos experimentaries como la potencia, usabilidad y calidad de vuestro terminal aumenta exponencialmente. Pero esto, ya lo dejo para otro post o para que busquéis por red de redes.
    
Espero que os sirva de ayuda.

¡Un saludo!    