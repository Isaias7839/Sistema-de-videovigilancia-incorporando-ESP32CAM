# Sistema-de-videovigilancia-incorporando-ESP32CAM

Sistema de vigilancia con ESP32CAM en Arduino IDE, para este caso usaremos dos ESP32CAM (se pueden implementar más), una de ellas la cual es para detección de movimiento y la otra como webserver.

# Objetivo
Crear un sistema de vigilancia la cual nos notifique mediante Telegram si alguien entra en un cuarto o no, al momento de detectar un "intruso" notificar de inmediato y grabar todos los movimientos/acciones que haga.


# Componentes
* ESP32 CAM OV2640
* FTDI TTL USB Serial Converter
* Cables Macho-Hembra
* Cable USB to Mini USB




# Librerias
Para las dos ESP32CAM necesitaras ArduinoJSON:

https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_dev_index.json

Esta liga la pegaras en el apartado  File > Preferences > Additional Boards Manager URLs.

ESP32CAM detección de movimiento:
* **EloquentSurveillance** by Simone Salerno
* **UniversalTelegramBot** by Brian Lough
