# Instalación de Docker

Instalación de Docker en Ubuntu y Windows.

## Instalación en Ubuntu

- **Actualizar el Índice del Paquete**
  - Ejecutar `sudo apt-get update` para actualizar el índice de paquetes del sistema.

- **Instalar Paquetes para Permitir el Uso de un Repositorio sobre HTTPS**
  - Ejecutar `sudo apt-get install apt-transport-https ca-certificates curl software-properties-common`.

- **Agregar la Clave GPG Oficial de Docker**
  - Usar `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`.

- **Agregar el Repositorio de Docker a APT**
  - Ejecutar `sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"`.

- **Actualizar el Índice del Paquete (de nuevo)**
  - Ejecutar `sudo apt-get update`.

- **Instalar Docker CE**
  - Ejecutar `sudo apt-get install docker-ce`.

- **Verificar que Docker Está Corriendo**
  - Usar `sudo systemctl status docker`.

## Instalación en Windows

- **Requisitos Previos para Windows 10**
  - Asegurarse de estar ejecutando Windows 10 Pro, Enterprise, o Education.
  - Habilitar la virtualización en la BIOS.

- **Descargar Docker Desktop para Windows**
  - Visitar la [página oficial de Docker](https://www.docker.com/products/docker-desktop) y descargar Docker Desktop para Windows.

- **Instalar Docker Desktop**
  - Abrir el instalador descargado y seguir las instrucciones de instalación.

- **Reiniciar el Sistema (si es requerido)**
  - Puede ser necesario reiniciar el sistema para completar la instalación.

- **Iniciar Docker Desktop**
  - Después del reinicio, abrir Docker Desktop desde el menú de inicio.

- **Verificar la Instalación**
  - Abrir una terminal (por ejemplo, PowerShell) y ejecutar `docker --version` para verificar que Docker se haya instalado correctamente.

