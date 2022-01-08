---
título: WSL-Python http.server
publicado: true
---


# Iniciar un servidor http en mi WSL con Pyton3

## Configurar la red del subsistema linux de windows.


Para configurar la red de nuestra distribucón linux instalada en nuestro sistema WindowsÂ®
tendremos que acceder a la consola de administracion de Hyper-V. Se debería correr con  *privilegios de administrador*.
Una vez conectado al servidor, que debe ser nuestra máquina local, vamos al menú ***Administrador de comuntadores virtuales*** .
 Allí elegimos la NIC denominada **WSL**.
Basta con poner el modo en ***Red Interna*** y elegir la tarjeta de red local por la que queramos conectarnos.

![red_screen](../assets/wsl_red_externa.png)

## Ejecutar Python para inciar un servidor HTTP.

Si necesitamos compartir archivos, este tipo de servicio puede resultar util. Es una forma rápida y sencilla de acceder via http a un directorio dado.
``` js
\# python -m http.server --bind 127.0.0.1 --directory /home/antonio/Documents 8080
```
![Windows](../assets/wsl_puerto_direcciorio_direccion.png)

Una vez arrancado el servidor podemos acceder a el desde un navegador, indicando el puerto por el que hemos arrancado el servicio, y obtendremos un lista de enalces a los ficheros ubicados en el directorio que se pasa como parámetro del comando de inicio del servicio.

![directorios](../assets/directorio_navegador.png)


>
>
> Fin del articulo
>
