## CloudFormation

Es una forma declarativa de esbozar tu infraestructura de AWS, para la mayoria de recursos, CloudFormation los crea por ti, en el **orden correcto** con la **configuracion exacta**.

### Ventajas

-   Infraestructura como codigo
    -   no se crean recursos manualmente
    -   Los cambios en la infraestructura se revisan atraves del codigo
-   Coste:
    -   Cada recurso dentro de la pila esta etiquetado para que veas su costo
    -   Puedes estimar recursos con la plantilla de CloudFormation
    -   Estrategias de Ahorro: En Dev, podrias automatizar la eliminacion de plantillas a una hora y crearlas a otra
-   Productividad:
    -   Posibilidad de destruir y volver a crear una infraestructura en Cloud
    -   Generacion automatizada de diagramas para plantillas
    -   Programacion declarativa
-   Soporta la mayoria de recursos

## AWS Cloud Development Kit (CDK)

-   Define tu insfraestructura de Cloud usando un lenguaje conocido:
-   El codigo se compila en una plantilla de CloudFormation
-   Por lo tanto, puedes desplegar juntos a la infraestructura y el codigo de ejecucion de la aplicacion

## AWS Elastic Beanstalk

### Problematica que resuelve

-   Gestion de infraestrcutura
-   Desplegar codigo
-   Configurar todas las bases de datos
-   Problemas de escalado
-   La mayoria de las aplicaciones tienen la misma arquitectura (ALB + ASG)

### Overview

Es una vision centrada en el desarrollo de la implementacion de una aplicacion en AWS ademas utiliza todos los componentes (EC2,ASG,ELB,RDS) y los agrupa en una sola vista teniendo un control total sobre la configuracion y gratuito pero pagas por las instancias subyacentes.

**Beanstalk = PaaS**

Servicio gestionado:

-   configuracion de instancia
-   Estrategia de despliegue es configurable pero la realiza Elastic Beanstalk
-   Aprovisionamiendo de capacidad
-   Equilibrio de carga y autoescalado
-   Modelos de arquitectura:
    -   Despliegue de una instancia
    -   LB + ASG
    -   Solo ASG


## AWS CodeDeploy

Desplegar applicacion automaticamente
Funciona con instancias EC2, servidores locales y servidores hibridos.
Los servidores/instancias deben ser aprovisionados y configurados de antemano con el agente de CodeDeploy

## AWS CodeCommit

Producto competidor de Github
Servicio de control de fuentes que aloja repositorios basados en Git, ademas de facilitar la colaboracion con otros en el codigo y los cambios en el codigo se versionan automaticamente

Ventajas:

-   Totalmente gestionado
-   Escalable y de alta disponibilidad
-   Privado, seguro, integrado con AWS

## AWS CodeBuild

Servicio de construccion de codigo en el Cloud
Compila el codigo fuente, ejecuta las pruebas y produce paquetes que estan listos para ser desplegados(ejemp. CodeDeploy)

Ventajas:

-   Totalmente gestionado, sin servidor
-   Continuamente escalable y altamente disponible
-   Seguro

## AWS CodePipeline

Orquestar los diferentes pasos para que el codigo sea empujado automaticamente a produccion
Codigo => Construir => Probar => Desplegar

Ventajas:

-   Totalmente gestionado
-   Entrega rapida y actualizaciones rapidas


## AWS Code Artifact

Los paquetes de sw dependen unos de otros para ser construidos
Almacenar y recuperar estas dependencias se llama gestion de artefactos
CodeArtifact es una gestion de artefactos segura, escalable y rentable para el desarrollo de SW

## AWS CodeStar

Interfaz de usuario unificada para gestionar facilmente las actividades de desarrollo de SW en un solo lugar
"Forma rapida" de empezar a configurar correctamente varios servicios de codigo

## AWS Cloud9

Es un IDE en la nube para escribir, ejecutar y depurar codigo
Un IDE en la nube se puede utilizar dentro de un navegador web
AWS Cloud9 permite colaboracion de codigo en tiempo real

## AWS Systems Manager

-   Apoya con la gestion de sistemas EC2 y On-premises a escala
-   Servicio hibrio de AWS
-   Automatizacion de parches para mejorar normativa
-   Ejecuta comandos en toda una flota de servidores
-   Almacena la condiguracion de los parametros con el almacen de parametros SSM

Se necesita un agente SSM en los sistemas que controlamos, estos agentes vienen por defecto en las AMI de Amazon Linux y en algunas AMI de ubuntu

### Session Manager

Te permite iniciar un shell seguro en tus servidores EC2 y locales

No se necesita accesso SSH ni claves SSH
No se necsita puerto 22

```mermaid
  flowchart LR;
      InstanciaEC2-->|ejecuta comandos| SessionManager;
      SessionManager-->|Permisos IAM| User;
```

## OpsWork

Chef y Puppet te ayudan a realizar la configuracion del servidor de forma automatica, o acciones repetitivas
Alternativa a SSM

## Resumen 

![Infraestructure Deploy Resumen](/cloud-practicioner/images/infraestructure-deploy.png "Infraestructure Deploy Resumen").
![Infraestructure Development Resumen](/cloud-practicioner/images/infraestructure-development.png "Infraestructure Development Resumen").