# Sistema-de-videovigilancia-incorporando-ESP32CAM

Sistema de videovigilancia con ESP32CAM en Arduino IDE, para este caso usaremos dos ESP32CAM (se pueden implementar más), una de ellas la cual es para detección de movimiento y la otra como webserver.

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

Esta liga la pegaras en el apartado  File > Preferences > Additional Boards Manager URLs;
Con esta liga podras acceder a las librerias necesarias para la utilización de ESP32CAM

ESP32CAM detección de movimiento:
* **EloquentSurveillance** by Simone Salerno
* **UniversalTelegramBot** by Brian Lough


**********************************************************************************

# Motion Detection CAM

Para acceder al codigo deberas ir al apartado File > Examples > EloquentSurveillance > *MotionDetectionTelegramExample*;
Dentro del codigo modificaras con tu propia información:
* WIFI_SSID
* WIFI_PASS
* BOT_TOKEN
* CHAT_ID
  
Dentro del codigo en la linea 30 cambiar **camera.mswide();** por **camera.aithinker();** ya que el modelo de nuestra camara es AI Thinker ESP32-CAM.
Para crear un bot en telegram usa BotFather (al crear un Bot te dara tu Bot token), y para obtener tu chat ID usa IDBot.

********************************************************************************

Este proyecto fue realizado en el marco del curso IoT Essentials Developer impartido por [Codigo IoT ](https://www.codigoiot.com/) y organizado por la [Asociación Mexicana del Internet de las Cosas](https://www.asociacioniot.org/).


