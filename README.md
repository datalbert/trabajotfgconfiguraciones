
# Configuracion proyecto TFG

Este repositorio contiene las configuraciones necesarias para cada uno de los microservicios desarrollados en nuestro proyecto. La gestión y carga de estas configuraciones se realiza a través de un servidor de configuración (ConfigServer), que se encarga de importar los archivos de configuración adecuados según el entorno de despliegue.

## Entornos de Despliegue

Las configuraciones están organizadas en función de tres ambientes de trabajo distintos:

- Desarrollo
- Pruebas
- Producción

### Desarrollo de cada entorno

1. **Desarrollo**
- Descripción: En el entorno de desarrollo, cada microservicio y sus bases de datos asociadas se ejecutan de forma independiente. Las bases de datos están contenidas en contenedores Docker separados, lo que permite aislar y gestionar cada uno de ellos de manera individual.
- Configuración: Cada microservicio se lanza por separado desde Visual Studio Code, facilitando así la depuración y el desarrollo individual. Esto permite a los desarrolladores probar y depurar cada componente de manera aislada antes de integrarlo con otros servicios.
- Contenedor: Docker se usa para contener las bases de datos, mientras que Visual Studio Code es la herramienta principal para iniciar y depurar los microservicios.
2. **Pruebas**
- Descripción: En el entorno de pruebas, se utiliza un archivo docker-compose.yml que engloba todos los microservicios y las bases de datos necesarias para las pruebas. Esto facilita la integración y validación del sistema en su totalidad.
- Configuración: El entorno se inicia mediante Docker, lo que permite configurar y lanzar todos los servicios necesarios de forma conjunta, simulando un entorno de integración más cercano al de producción. Esto es ideal para pruebas de integración y verificación de que todos los componentes funcionan correctamente juntos.
- Contenedor: Docker Compose se encarga de la orquestación de los contenedores, simplificando el proceso de configuración y ejecución del entorno de pruebas.
3. **Producción**
- Descripción: El entorno de producción es el entorno final donde se despliega la aplicación para su uso en vivo. En este entorno, los microservicios y sus bases de datos se gestionan mediante Kubernetes, lo que ofrece una solución robusta y escalable para la orquestación y gestión de los contenedores.
- Configuración: La configuración y el despliegue se realizan a través de Kubernetes, proporcionando una plataforma de orquestación que asegura alta disponibilidad, escalabilidad y gestión eficiente de los recursos.
- Contenedor: Kubernetes gestiona la implementación y el ciclo de vida de los contenedores, facilitando la administración de la infraestructura en producción.





