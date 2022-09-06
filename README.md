# DOCKER
Docker le proporciona una manera estándar de ejecutar su código. Docker es un sistema operativo para contenedores. De manera similar a cómo una máquina virtual virtualiza (elimina la necesidad de administrar directamente) el hardware del servidor, los contenedores virtualizan el sistema operativo de un servidor.

## ARQUITECTURA
La arquitectura Docker es una arquitectura cliente-servidor, dónde el cliente habla con el servidor (que es un proceso daemon) mediante un API para poder gestionar el ciclo de vida de los contenedores y así poder construir, ejecutar y distribuir los contenedores.

El hecho de que el cliente se comunique con el servidor mediante el API hace que el cliente y servidor puedan estar en la misma máquina comunicándose mediante sockets de UNIX o bien en máquinas diferentes comunicándose mediante un end-point en la red.

Cuando trabaja con Docker, usa imágenes, contenedores, volúmenes, redes; todos estos son objetos de Docker.

#### Traditional vs. New-Generation Virtualization

Anteriormente, solíamos crear máquinas virtuales, y cada VM tenía un sistema operativo que ocupaba mucho espacio y lo hacía pesado.

Ahora, en el caso del contenedor de la ventana acoplable, tiene un solo sistema operativo y los recursos se comparten entre los contenedores. Por lo tanto, es ligero y arranca en segundos.

![image](https://user-images.githubusercontent.com/101889445/188665474-585b244a-534b-4e88-b708-7a1cc65e02e0.png)

#### Docker Engine
Es la parte central de todo el sistema Docker. Docker Engine es una aplicación que sigue arquitectura cliente-servidor. Está instalado en la máquina host. Hay tres componentes en Docker Engine:

-Servidor: Es el demonio de la ventana acoplable llamado Dockerd. Puede crear y administrar imágenes de la ventana acoplable. Contenedores, redes, etc.

-API de descanso: Se utiliza para indicar al demonio de la ventana acoplable qué hacer.

-Interfaz de línea de comandos (CLI): Es un cliente que se usa para ingresar comandos de docker.

#### Imágenes
Las imágenes de Docker son plantillas de solo lectura con instrucciones para crear un contenedor de Docker. La imagen de Docker puede extraerse de un concentrador de Docker y usarse tal como está, o puede agregar instrucciones adicionales a la imagen base y crear una imagen de Docker nueva y modificada. Puede crear sus propias imágenes de la ventana acoplable también utilizando un archivo acoplable. Cree un dockerfile con todas las instrucciones para crear un contenedor y ejecutarlo; creará su imagen de ventana acoplable personalizada.

La imagen de Docker tiene una capa base que es de solo lectura y la capa superior se puede escribir. Cuando edita un archivo docker y lo reconstruye, solo la parte modificada se reconstruye en la capa superior.

#### Contenedores
Después de ejecutar una imagen de la ventana acoplable, crea un contenedor de la ventana acoplable. Todas las aplicaciones y su entorno se ejecutan dentro de este contenedor. Puede usar la API o la CLI de Docker para iniciar, detener y eliminar un contenedor de Docker.

A continuación se muestra un comando de muestra para ejecutar un contenedor docker de ubuntu:

docker run -i -t ubuntu /bin/bash

#### Volúmenes
Los datos persistentes generados por Docker y utilizados por los contenedores de Docker se almacenan en Volumes. Están completamente administrados por Docker a través de Docker CLI o Docker API. Los volúmenes funcionan en contenedores de Windows y Linux. En lugar de conservar los datos en la capa de escritura de un contenedor, siempre es una buena opción utilizar volúmenes para ello. El contenido del volumen existe fuera del ciclo de vida de un contenedor, por lo que usar el volumen no aumenta el tamaño de un contenedor.

Puede usar el indicador -v o –mount para iniciar un contenedor con un volumen. En este comando de muestra, está usando geekvolume volume con el contenedor geekflare

docker run -d --name geekflare  -v geekvolume:/app nginx:latest

![image](https://user-images.githubusercontent.com/101889445/188667211-163fe4d7-0496-42fd-8e3e-d74ca763b2e7.png)
