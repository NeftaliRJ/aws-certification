## SQS

Simple Queue Service

-   Es la oferta mas antigua de AWS
-   Servicio totalmente gestionado utilizado para desacoplar aplicaciones
-   Por defecto 4 dias hasta max. 14 dias
-   No hay limite en el numero de mensajes
-   **Los mensajes se elimann despues de ser leidos por consumidores**
-   Baja latencia

## SNS

Y si queremos enviar un mensaje a muchos receptores?

**Pub/Sub**

Los publicadores de eventos, solo envian mensajes a un SNS Topic
Tantos suscriptores de eventos como queremos escuchar las notificaciones del SNS Topic
Cada susbcriptro **recibira todos los mensajes**
Hasta 12.5M de subscriptores limite de 100k Topics

## Amazon Kinesis

Kinesis = streaming big data en tiempo real

Servicio gestionado para recopilar, procesar y analizar datos de streaming en tiempo real a cualquier escala

## Amazon MQ

SQS, SNS son servicios nativos del Cloud, y utilizan protocolos propietarios de AWS
Las aplicaciones tradicionales que se ejecutan desde las instalaciones
Al migrar a el Cloud de rediseñar la aplicacion ara utilizar SQS y SNS
Amazon MQ = managed Apache ActiveMQ

## Resumen 

![Integration Resumen](/cloud-practicioner/images/integrations.png "Integration Resumen").