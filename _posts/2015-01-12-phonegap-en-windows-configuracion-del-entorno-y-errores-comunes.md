---
layout: post
title: "Phonegap en Windows. Configuración del entorno y errores comunes."
date: 2015-01-12 17:32:13 +0200
categories: [Android, Desarrollo]
---
El otro día me pidió ayuda un amigo el cual trataba de dar sus primeros pasos con el desarrollo de webapps para dispositivos móviles utilizando el Framework Phonegap. Se llevo algún que otro quebradero de cabeza en su configuración (y una pequeña "chapa" informativa por mi parte para que migrara a Linux Mint :P).

A continuación detallo las pautas a seguir para su configuración en Windows:

## Pasos estándar para preparar nuestro entorno de trabajo (en Windows):

1. Descargar e instalar [Java Development Kit (JDK)](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html?ssSourceSiteId=otnes)
2. Descargar [Ant](https://ant.apache.org/bindownload.cgi) y descomprimirlo en el disco duro.
3. Descargar el [SDK de Android](http://developer.android.com/sdk/index.html#Other) (nota: recomiendo solo el SDK)
4. Instalar [Node.js](http://nodejs.org/) (versión >=0.10.22) para utilizar su gestor de dependencias npm e instalar Phonegap.
5. Tras esto, en la consola de Windows escribir: 
  ```
  npm install -g phonegap
  ```
6. Configurar las variables de entorno: 
    * **JAVA_HOME** (_{path instalación JDK}_)
    * **ANT_HOME** (_{path instalación ant}_)
    * **ANDROID_HOME** (_{path instalación android/sdk}_)
7. Añadir esta configuración en la variable PATH: 
  ```
  ;%ANT_HOME%/bin;%ANDROID_HOME%\tools;%ANDROID_HOME%\platform-tools;%JAVA_HOME%\bin
  ```

## Errores, problemas y soluciones comunes en Windows.

* **Alguna de las variables de entorno no funciona. No encuentra las aplicaciones a través de la consola de Windows.**
  Alternativamente al punto 6 se puede escribir el **path absoluto** en la variable PATH a cada una de los 4 directorios anteriores (a veces %VARIABLE% no es comprendido bien por Windows).
* **Ant usa JRE en vez de JDK incluso con variables de entorno**
  Al ejecutar ant aparece un mensaje de error: 
  ```
  C:\Users\xxx>ant Unable to locate tools.jar. Expected to find it in C:\Program Files\Java\jre6\li b\tools.jar Buildfile: build.xml does not exist! Build failed
  ```
  Cuando aparece este error, es síntoma de que el sistema está utilizando JRE en vez de JDK (tienes los dos instalados sin saberlo). En este caso el paso 6 es obligatorio, y es necesario forzar la variable de entorno **JAVA_HOME** para que utilizar el JDK y muy importante: **el path no debe incluir el directorio /bin/**
  ```
  C:\Program Files\Java\jdk1.7.0_71
  ```
* **Versión correcta del SDK de Android no encontrada**
  Un error muy común al ejecutar una aplicación a través del comando: phonegap run android, es que aparezca en la ejecución el siguiente mensaje:
  ```
  [phonegap] detecting Android SDK environment...
  [phonegap] using the remote environment</pre>
  ```
  Este error es debido a que tú versión de Phonegap instalada utiliza una **versión del SDK de Android diferente** a la que tienes. Revisa la versión del API de Android que necesitas y descargala a través del SDK Manager.

Espero que con estas indicaciones no tengáis ningún problema, en caso contrario nos vemos en los comentarios.

¡Saludos!