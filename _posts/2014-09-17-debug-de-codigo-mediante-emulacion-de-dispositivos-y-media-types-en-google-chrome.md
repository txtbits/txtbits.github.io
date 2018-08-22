---
layout: post
title: "Debug de código mediante emulación de dispositivos y Media Types en Google Chrome"
date: 2014-09-17 09:54:11 +0200
categories: [Desarrollo, Diseño, Google]
---
Últimamente, en mi trabajo, el desarollo frontend se ha incrementado considerablemente, y me he encontrado en la situación de tener que realizar varios contenidos web con formato muy especifico para su visualización en versión web, como en versión impresa, como ya os imaginaréis es contenido con resultados estadísticos, e informes, por lo que la versión impresa de la web cobra un papel muy importante.

Hasta hace relativamente poco tiempo, este trabajo era bastante pesado, puesto que no había apenas herramientas de depuración de código CSS para los diferentes Media Types (y además, teniendo en cuenta de que la gran mayoría fueron implementandos en CSS2...).

Desde el primero momento, supuse que Google Chrome, con sus Developer Tools, tendría que tener algún as bajo la manga, para facilitarnos la tarea, pero me resulto curioso que no encontré dicha opción en las herramientas. Tras ponerme a indigar por Google descubrí no sólo tenía una herramienta que facilitaba la tarea, era un completo emulador de todos los Media Types y por supuesto incluyendo su completo set de herramientas como inspector de elementos HTML, modificación de estilos CSS en vivo, etc.

El problema de esto, es que los desarrolladores de Chromium (versión base de Google Chrome) han movido ~~escondido~~) en repetidas ocasiones esta funcionalidad, y han conseguido despistar a más de uno.

En este momento (Versión 37.0.2062.120 m) se encuentran en: 
![Google Dev Tools Emulation](http://txtbits.com/wp-content/uploads/2014/09/google-dev-tools-emulation.png){:class="img-responsive pull-right"}

1. Chrome Developer Tools 
  * Linux/Windows: ctrl + shift + j o F12
  * Mac: cmd + alt + j o F12
2. Si no se abre automáticamente el Drawer, apretamos ESC.
3. En el Drawer de la consola, veremos una pestaña que pone "Emulation", aquí es donde actualmente han centralizado la Emulación del navegador: 
  * Devices: Para emular dispositivos en función del modelo, resolución etc.
  * Media: Para emular Media Types.

Esta funcionalidad nos puede ahorrar un tiempo increíble a la hora de depurar código en desarrollo web, añadiendo toda la potencia que tiene el inspector de las Google Chrome Developer Tools, y su previsualizador en tiempo real.