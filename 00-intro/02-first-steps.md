# Primeros pasos con Docker

## Verificar la instalación

Ejecutar: 

```docker ps```

## Imagenes y contenedores

En Docker, el concepto de "contenedor" se refiere a una unidad estándar de software que encapsula el código y todas sus dependencias, 
permitiendo que la aplicación se ejecute de manera rápida y confiable en diferentes entornos informáticos. Los contenedores son ligeros, 
eficientes y proporcionan un aislamiento consistente del sistema subyacente.

Por otro lado, una "imagen" en Docker es una plantilla ligera y portátil que contiene instrucciones para crear un contenedor.
Las imágenes son inmutables y actúan como una base para instanciar contenedores, asegurando así que la aplicación se comporte de la 
misma manera en cualquier lugar donde se despliegue.

## Ciclo de vida de un contenedor

Un contenedor se lanza y termina de forma similar a cualquier proceso del sistema operativo. El contenedor tiene un "entrypoint",
un binario dentro del contenedor que controla el inicio y el final del contenedor. Cuando el entrypoint finaliza, el contenedor finaliza.

Los entrypoints no suelen ser binarios interactivos, sino procesos tipo servidor, ya sean bases de datos o servidores web.

## Hello World en Docker !

Ejecutar:

```docker run hello-world```

Salida esperada:

```
carlos@jordan:~$ docker run hello-world

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/

```

## Contenedores e imagenes

### Listar contenedores e imàgenes: 

Ejecutar:

1. ```docker ps```
2. ```docker ps -a```
3. ```docker images```

### Bajar imagenes

Ejecutar:

1. ```docker pull alpine```
2. ```docker pull ubuntu```
3. ```docker images```

## Instanciar una imagen

1. Ejecutar ```docker run -ti ubuntu bash```
2. Ejecutar ```apt get update && apt install inetutils-ping```
3. Ejecutar ```ping 1.1.1.1```
4. Ejecutar ```exit```
5. Ejecutar ```docker run -ti ubuntu bash```
   - ¿esta presente el binario ping? 
