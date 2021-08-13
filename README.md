##### :heavy_exclamation_mark: Estado :heavy_exclamation_mark:
Debería funcionar en todas las regiones siempre que se asignen los códigos de operación. Actualmente solo funciona en TERA Toolbox.

##### :heavy_exclamation_mark: Instalación :heavy_exclamation_mark:
1) Descargar Negociador: https://github.com/Loliconera/Negotiator/archive/refs/heads/master.zip
2) Extraiga el contenido del archivo zip en "\TeraToolbox\mods"
3) ¡Hecho! (el módulo se actualizará automáticamente cuando se lance una nueva versión)

# Negociador
Un módulo tera-proxy que acepta o rechaza automáticamente las negociaciones de Trade Broker.
Esta es una bifurcación del original Pinkie Pie's auto-negotiate.

![Screenshot](https://i.imgur.com/uB74X4o.png)

## Como usar
Hay varias opciones que puede cambiar en el archivo config.json:  
  
* "**AUTO_ACCEPT_THRESHOLD**" - Acepta automáticamente ofertas por *igual o mayor que* la cantidad especificada en % (0 para deshabilitar)
** Ejemplo: 99 aceptará ofertas por el 99% (o más) del precio de venta
* "**AUTO_REJECT_THRESHOLD**" - Rechaza automáticamente ofertas por *menos* que la cantidad especificada en % (0 para deshabilitar)
** Ejemplo: 75 rechazarán ofertas por menos del 75% del precio de venta
* "**UNATTENDED_MANUAL_NEGOTIATE**" - Configure en "true" para aceptar automáticamente las negociaciones después de hacer clic en el enlace "Accept" en el chat (¡así que tenga cuidado con lo que hace clic!)
* "**DELAY_ACTIONS**" - Establezca esto en "false" para manejar de inmediato las negociaciones en lugar de esperar un poco para simular un comportamiento similar al humano.
* "**log**" - Establezca esto en "true" para habilitar el registro de negociaciones en su consola
  
Mientras estás en el juego, abre una sesión de chat proxy escribiendo "/proxy" o "/8" en el chat y presionando la barra espaciadora. 
Esto sirve como interfaz de comandos del script.  
Se admiten los siguientes comandos:  
  
* **nego accept [x]** - cambiar el porcentaje mínimo para aceptar un trato, ej. "nego accept 100" [0 para inhabilitar]
* **nego reject [x]** - cambiar el porcentaje máximo para rechazar un trato, ej. "nego reject 75" [0 para inhabilitar]
* **nego unattended** - habilitar / deshabilitar la aceptación automática de ofertas después de hacer clic en el enlace "Accept" en el chat
* **nego delay** - cambiar entre el comportamiento humano y la negociación inmediata
* **nego log** - habilitar / deshabilitar el registro en la consola

## Seguridad
Todo lo que envíes al chat proxy en el juego se intercepta del lado del cliente. El chat NO se envía al servidor.
Este módulo utiliza retrasos aleatorios para simular un comportamiento similar al humano.

## Créditos
- Original de Pinkie Pie -> https://github.com/pinkipi
- Bifurcado de TeraProxy -> https://github.com/TeraProxy/Negotiator

## Cambios
<details>

### 1.1.0
* [~] Ahora extrae cadenas directamente de los archivos del juego (¡el módulo SIEMPRE estará actualizado!)
* [-] Se eliminaron los archivos y el directorio de "cadenas", ya que ya no son necesarios
### 1.0.2
* [+] Aviso agregado sobre negociación exitosa
### 1.0.1
* [*] Se corrigió un error al cambiar el umbral de aceptación y rechazo en el juego.
### 1.0.0
* [*] Compatibilidad BigInt
* [+] Se agregó soporte de actualización automática en el proxy de Caali
* [+] Se agregó un registro de negociación opcional a la consola.
* [+] Comandos agregados dentro del juego
* [+] Se agregó visualización de los nombres y la cantidad de los artículos.
* [~] Configuración movida al archivo de configuración

</details>