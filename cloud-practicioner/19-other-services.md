## Amazon WorkSpaces

Solucion de escritorio gestionado como servicio DaaS para aprovisionar facilmente escritorios Windows o Linux
Genial para eliminar la gestion de la VDI(Infraestructura de Escritorio Virtual) local
Rapidamente escalable a miles de usuarios
Servicio de pago por uso con tarifas mensuales o por hora

WorkSpaces puede integra multiples regiones

## Amazon AppStream 2.0

Servicio de streaming de aplicaciones de escritorio para usuarios
Entrega a cualquier ordenador, sin adquirir, infraestructura
**La aplicacion se entrega de un navegador web**

### WorkSpaces vs AppStream 2.0

WorkSpaces

-   Dispones de una VDI y un escritorio totalmente gestionado
-   Los usuarios se conectan a la VDI y abren aplicaciones nativas o WAM
-   Los espacios de trabajo estan bajo demanda o siempre encendidos

AppStream

-   Transmite una aplicacion de escritorio a los navegadores web (sin necesidad de conectarse a una VDI)
-   Funciona con cualquier dispositivo con navegador web

## AWS Sumerian

Crea y ejecuta aplicaciones de realidad virtual (RV), realidad aumentada (RA) y 3D
Se puede utilizar para crear rapidamente modelos 3D

## AWS IoT Core

El nucleo de AWS IoT te permite conectar facilmente los dispositivos IoT a la nube de AWS
Sin servidor, seguro y escalable a miles de millones de dispositivos y billones de mensajes
Tus aplicaciones pueden comunicarse con tus dispositivos incluso cuando no estan conectados
Se integran con muchos servcios de AWS

## AWS Elastic Transcoder

Se utiliza para convertir los archivos multimedia almacenados en S3 en archivos multimedia en los formatos requeridos por los dispositivos de reproduccion de los consumidores

```mermaid
  flowchart LR;
      BucketS3Entrada--> TranscodingPipeline;
      TranscodingPipeline--> BucketS3Salida;
      BucketS3Salida--> Dispositivos;
```

## AWS AppSync

Almacena y sincroniza los datos entre las aplicaciones moviles y web en tiempo real
Utiliza GraphQL
El codigo del cliente se puede generar automaticamente
Suscripciones en tiempo real

## AWS Amplify

AWS Amplify es un conjunto de herramientas y servicios que permite a los desarrolladores front-end y back-end crear aplicaciones web y móviles de manera fácil y rápida
Autenticacion, almacenamiento, API(REST, GraphQL), CI/CD

## AWS Device Farm

Servicio totalmente gestionado que prueba tus aplicaciones web y moviles en navegadroes de escritorio, dispositivos moviles reales y tablesta
Ejecuta pruebas simultaneamente en varios dispositivos ademas de poder configurarlos

## AWS Backup

Servicio totalmente gestionado para administrar y automatizar centralmente las copias de seguridad en todos los servicios de AWS
Copias de seguridad bajo demanda y programadas
Soporta PITR (Point in time Recovery)

## AWS Elastic Disaster Recovery (DRS)

Recupera rapida y facilmente tus servidores fisicos, virtuales y en la nube de AWS
Replicacion continua a nivel de bloque para tus servidores

## AWS DataSync

Mueve una gran cantidad de datos de las instalaciones a AWS
Puedes sincronizar a: Amazon S3, Amazon EFS, Amazon Fsx

Las tareas de replicacion se pueden programar cada hora, cada dia, cada semana
Las tareas de replicacion son **incrementales** despues de la primera carga completa

## AWS Application Discovery Service

Planificar los proyectos de migracion recopliando informacion sobre los centros de datos locales
Los datos de utilizacion de los servidores y la asignacion de dependencias son importantes para las migraciones 

Puede utilizarse mediante un agente de AWS o sin el y este determinara ciertas limitantes en cuando a la informacion que accesa

## AWS Application Migration Service (MGN)

Solucion Lift-and-shift que simplifica la migracion de aplicaciones a AWS
Convierte tus servidores fisicos, virtuales y basados en la nube para que se ejecuten de forma nativa en AWS

## AWS Faul Inject Simulator (FIS)

Un servicio gestionado para ejecutar experimentos de inyeccion de fallos en la cargas de trabajo de AWS
Basado en la **ingenieria del caos**: estresar una aplicacion creando eventos pertubadores 
Te ayuda a descubrir fallos ocultos y cuellos de botella en el rendimiento
Utiliza plantillas preconstruidas que generan las interrupciones deseadas

## AWS Step Functions

Contruye un flujo de trabajo visual sin servidor para orquestar tus funciones Lambda
Caracteristicas: secuencia, paralelo, condiciones

## AWS Ground Station

Servicio totalmente gestionado que te permite controlar las comunicaciones por satelite, procesar los datos y escalar tus operaciones por satelite
Proporciona una red global de estaciones terrestres de satelites cerca de las regiones de AWS
Te permite descargar los datos de los satelites a tu VPC de AWS en cuestion de segundos
Envia los datos de los satelites a una instancia S3 o EC2

## AWS PinPont

Servicio escalable de comunicaciones de marketing (bidireccional)
Soporta correo electronico, SMS, push, voz y mensaria in-app
Posibilidad de segmentar y personalizar los mensajes con el contenido adecuado para los clientes
Posibilidad de recibir respuestas y enviar todo mediante SMS

Frente a Amazon SNS o Amazon SES

-   En SNS y SES gestionas la audencia, el contenido y el calendario de entrega de cada mensaje
-   En amazon Pinpoint, creas plantillas de mensajes, horarios de entrega, segmentos altamente segmentados y campañas completas