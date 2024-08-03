# Sistema-de-videovigilancia-incorporando-ESP32CAM

Sistema de videovigilancia con ESP32CAM en Arduino IDE, para este caso usaremos dos ESP32CAM (se pueden implementar mas), una de ellas la cual es para detección de movimiento y la otra como webserver.

<img src="Extras/GRAB.jpg" width="500" height="400">

<img src="Extras/TEL.jpg" width="500" height="400">
*************************************************************************************
# Objetivo
Crear un sistema de videovigilancia que permita el acceso en tiempo real para monitorear lo que ocurre en un lugar específico. El sistema enviará notificaciones a través de Telegram cuando se detecte la entrada de una persona en una habitación. Al detectar **movimiento**, el sistema notificará de inmediato y grabará todas las acciones y movimientos realizados.
*************************************************************************************************

# Componentes
* ESP32 CAM OV2640
* FTDI TTL USB Serial Converter
* Cables Macho-Hembra
* Cable USB to Mini USB
* Tarjeta MicroSD 4 GB



******************************************************************************************
# Librerias
Para las dos ESP32CAM necesitaras ArduinoJSON:

https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_dev_index.json

Esta liga la pegaras en el apartado  `File` > `Preferences` > `Additional Boards Manager URLs`;
Con esta liga podras acceder a las librerias necesarias para la utilización de ESP32CAM

ESP32CAM detección de movimiento:
* **EloquentSurveillance** by Simone Salerno
* **UniversalTelegramBot** by Brian Lough


**********************************************************************************

# Motion Detection CAM

Para acceder al codigo deberas ir al apartado `File` > `Examples` > `EloquentSurveillance` > `MotionDetectionTelegramExample`;
Dentro del codigo modificaras con tu propia información:
* WIFI_SSID
* WIFI_PASS
* BOT_TOKEN
* CHAT_ID
  
Dentro del codigo en la linea 30 cambiar **camera.mswide();** por **camera.aithinker();** ya que el modelo de nuestra camara es AI Thinker ESP32-CAM.
Para crear un bot en telegram usa BotFather (al crear un Bot te dara tu Bot token), y para obtener tu chat ID usa IDBot.

***********************************************************************************

# Web Server CAM
Para el correcto funcionamiento del sistema de videovigilancia será necesario programar y posteriormente confirgurar el dispositivo con el código correspondiente.

*ESPCAM WEBSERVER*
* **ESP32-CAM_MJPEG2SD** by s60sc.

Lo puedes encontrar en el siguiente enlace:

[ESP32-CAM_MJPEG2SD](https://github.com/s60sc/ESP32-CAM_MJPEG2SD)

**Instalación y configuración**

Descargue los archivos de github en la carpeta de bocetos de Arduino IDE.

<img src="Extras/WEBSERVER.png" width="500" height="400">

Dentro del código selecciona la placa ESP-CAM requerida usando `CAMERA_MODEL_` en `appGlobals.h` a menos que uses la predeterminada:
* Tarjeta ESP32 Cam - `CAMERA_MODEL_AI_THINKER`.

 <img src="Extras/APP.png" width="500" height="400"> 

De la misma manera, dentro de `utils.cpp` modificaremos el código con la información de nuestra red, esto es:
* WIFI_SSID
* WIFI_PASS

<img src="Extras/INT.png" width="500" height="400"> 


Después de programar y configurar la ESP32CAM con los pasos anteriores es necesario insertar una tarjeta memoria micro SD (preferentemente de 8 GB de capacidad o superior) configurada de la siguiente manera:

* Del código anteriormente descargado, localizar la carpeta `data` y copiarla a la tarjeta de memoria micro SD.
***************************************************************************************************************************

Este proyecto fue realizado en el marco del curso IoT Essentials Developer impartido por [Codigo IoT](https://www.codigoiot.com/) y organizado por la [Asociación Mexicana del Internet de las Cosas](https://www.asociacioniot.org/).

