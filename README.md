# Clasificación de imágenes (perros y gatos)

Este código representa el sitio web, una vez que se crea y se entrena el modelo de inteligencia artificial con Python y Tensorflow, se exporta a los archivos "json" y "bin".
Se puede utilizar en el celular, solo se necesita apuntar la cámara al perro o gato que se quiera clasificar.

### Iniciar un servidor en la carpeta
Este proyecto utiliza un modelo de Tensorflow.js, el cual para cargarse requiere que el acceso sea por medio de http/https. La forma de hacerlo es la sigueinte:
- Descargar Python en la computadora
- Abrir una línea de comandos o terminal
- Navegar hasta la carpeta donde se encuentra el código
- Ejecutar el comando `python -m http.server 8000`
- Abrir un explorador e ir a http://localhost:8000

### Utilizarlar en un celular
Si se desea abrir desde el celular, no se puede solo poner la IP local de la computadora y el puerto, ya que para usar la cámara se requiere HTTPS. Se debe hacer un túnel de HTTPS siguiendo los pasos que se muestran a continuación:
- Descargar ngrok en la computadora, y descomprimirlo
- Abrir una línea de comandos o terminal
- Navegar hasta la carpeta donde se descargo ngrok
- Ejecutar el comando `ngrok http 8000`
- Es importante tener activos el servidor de python, y el túnel de ngrok
- En la línea de comandos aparecerá un enlace HTTPS. De esa forma se puede entrar con el celular, no importa si no se esta en una red local.
- El túnel expira después de 2 horas, despues de eso solo se debe reiniciar ngrok
- Abrir un explorador en el celular e ir al enlace HTTPS indicado

### Uso
Se puede dar clic en el botón de "Cambiar camara" para utilizar la cámara delantera o trasera del celular. Solo se debe apuntar la cámara a un perro o gato, y abajo aparecerá la predicción.