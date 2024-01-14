# Levantar un wordpress con mysql

## ¿Que es docker compose?

Docker Compose es una herramienta de Docker que facilita la definición y ejecución de aplicaciones multi-contenedor. Utiliza un archivo YAML para configurar los servicios de la aplicación, lo que permite definir, por ejemplo, bases de datos, aplicaciones backend, front-end, y cualquier otro servicio que la aplicación requiera, junto con sus respectivas configuraciones, como puertos, volúmenes, y dependencias entre ellos.

Docker Compose simplifica el proceso de despliegue y gestión de estos servicios, permitiendo lanzar y detener toda la aplicación con unos pocos comandos, asegurando la coherencia en diferentes entornos de desarrollo, pruebas y producción. Es especialmente útil en el desarrollo de aplicaciones basadas en microservicios y en entornos donde la integración y la automatización son críticas.

## Comandos básicos de docker compose

### Comandos de Docker Compose

1. **Levantar la Aplicación**
   - Para iniciar todos los servicios:
     ```bash
     docker-compose up
     ```
   - En modo "detached":
     ```bash
     docker-compose up -d
     ```

2. **Bajar la Aplicación**
   - Detener todos los servicios y mantener los datos:
     ```bash
     docker-compose down
     ```

3. **Borrar la Aplicación y sus Datos**
   - Detener servicios y borrar todos los datos y volúmenes:
     ```bash
     docker-compose down --volumes
     ```


## Receta de compose para levantar un wordpress con mysql

```
version: '2'

services:
  db:
    image: mysql:5.7
    volumes:
      - db_data:/var/lib/mysql
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: somewordpress
      MYSQL_DATABASE: wordpress
      MYSQL_USER: wordpress
      MYSQL_PASSWORD: wordpress

  wordpress:
    depends_on:
      - db
    image: wordpress:latest
    ports:
      - "8000:80"
    restart: always
    environment:
      WORDPRESS_DB_HOST: db:3306
      WORDPRESS_DB_USER: wordpress
      WORDPRESS_DB_PASSWORD: wordpress
volumes:
    db_data:

```
