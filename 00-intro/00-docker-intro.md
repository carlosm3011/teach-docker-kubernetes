# Introducción a Docker

## VMs vs containers

- **Tipo de Aislamiento y Overhead**
  - VMs: Utilizan la virtualización del hardware para proporcionar un aislamiento completo del sistema operativo; esto conlleva un mayor uso de recursos.
  - Contenedores: Proporcionan aislamiento a nivel de sistema operativo, lo que significa menos sobrecarga y un uso más eficiente de los recursos del sistema.

- **Arranque y Escalabilidad**
  - VMs: Tienen tiempos de arranque más largos debido a la necesidad de cargar todo el sistema operativo y el hardware virtual.
  - Contenedores: Se inician rápidamente ya que comparten el kernel del sistema operativo del host y solo cargan la aplicación y sus dependencias.

- **Portabilidad de la Aplicación**
  - VMs: La portabilidad puede verse afectada por las dependencias del sistema operativo y el hardware virtual.
  - Contenedores: Son altamente portátiles, ya que encapsulan la aplicación y sus dependencias en un contenedor consistente.

- **Eficiencia del Almacenamiento**
  - VMs: Cada VM necesita una copia completa del sistema operativo, lo que aumenta el uso del almacenamiento.
  - Contenedores: Comparten el kernel del sistema operativo del host y pueden compartir capas, reduciendo significativamente el uso del almacenamiento.

- **Uso de Casos**
  - VMs: Adecuadas para ejecutar aplicaciones que necesitan sistemas operativos completos o para simular hardware específico.
  - Contenedores: Ideales para despliegues de microservicios, aplicaciones escalables y entornos de desarrollo y pruebas consistentes.

- **Herramientas y Ecosistemas**
  - VMs: Utilizan herramientas de virtualización como VMware, VirtualBox y Hyper-V.
  - Contenedores: Ampliamente apoyados por herramientas como Docker y Kubernetes en un ecosistema en constante crecimiento.
