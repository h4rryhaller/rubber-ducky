# Rubber Ducky 
Following payload will grab saved Wifi password and will send them to your hosted webhook and hide the cmd windows by using technique mentioned in hak5darren
rubberducky wiki -- Payload hide cmd window [https://github.com/hak5darren/USB-Rubber-Ducky/wiki/Payload---hide-cmd-window]

## Hardware
Basado en la placa china DigiSpark ATTiny85 USB Modelo A

## Cambios
* Reemplazamos los ficheros de configuración de teclado americano por el español https://github.com/Dasor/digispark-keyboard-layout-Spanish
* Exfiltramos los datos en webhook.cool
* Encendemos el led rojo (pin 1) muy atenuado por discrección. Cuando la exfiltración finaliza se apaga el led.

## Instalación
Configura el archivo `config.h` con tu dirección de webhook, el pin de tu placa, nivel de atenuación del led, etc.

## Uso
Genera un identificador en https://webhook.cool 
Esa será la url donde hagas tus peticiones https://tu-identificador/webhook.cool
Tras la exfiltración puedes consultar tus datos en https://webhook.cool/at/tu-identificador
Los datos se borran tras 7 días sin uso de la cuenta. Para evitarlo puedes crear una cuenta en https://crontap.apihustle.com/crontap/ que, en mi caso, he configurado para que haga dos peticiones por semana. 
