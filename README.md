# Sistema-de-videovigilancia-incorporando-ESP32CAM

Sistema de videovigilancia con ESP32CAM en Arduino IDE, para este caso usaremos dos ESP32CAM (se pueden implementar mas), una de ellas la cual es para detección de movimiento y la otra como webserver.

*************************************************************************************
# Objetivo
Crear un sistema de vigilancia de la cual podemos acceder en tiempo real que es lo que esta pasando en un lugar determinado, notificandonos mediante Telegram si alguien entra a un cuarto o no, al momento de detectar **movimiento** notificar de inmediato y grabar todos los movimientos/acciones que haga.
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

<img src="extras/WEBSERVER.png" width="500" height="400">

Dentro del código selecciona la placa ESP-CAM requerida usando `CAMERA_MODEL_` en `appGlobals.h` a menos que uses la predeterminada:
* Tarjeta ESP32 Cam - `CAMERA_MODEL_AI_THINKER`.

De la misma manera, dentro de `utils.cpp` modificaremos el código con la información de nuestra red, esto es:
* WIFI_SSID
* WIFI_PASS
