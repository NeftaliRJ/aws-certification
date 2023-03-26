## Amazon CloudWatch

Proporciona metricas para todos los servicios de AWS
La metrica es una variable a monitorizar ademas de tener marcas de tiempo

### Amazon CloudWatch Metrics

-   CloudWatch proporciona metricas para todos los servicios de AWS
-   la **metrica** es una variable a monitorizar
-   las metricas tienen marca de tiempo


### Amazon CloudWatch Alarms

Se utilizan para activar las notificaciones de cualquier metrica
Acciones de las alarmas
-   Autoescalado
-   Acciones de EC2
-   Notificaciones SNS
Puedes elegir el periodo sobre el que evaluar una alarma

### Amazon CloudWatch Logs

Permite la monitorizacion de logs en tiempo real
Retencion de logs de CloudWatch ajustable
Funciona mediante la instalacion de un agente tanto para servicios de AWS como para servidores locales

### Amazon CloudWatch Events

Programar: Trabajos Cron
Patrones de eventos: Reglas de eventos para reaccionar ante un servicio que hace algo
Activar funciones lambdas

Servicios de comunicacion en Amazon EventBridge

-   Por defecto 
-   Socios
-   Apps personalizadas

### AWS CloudTrail

Proporciona gobernanza, normativa y auditoria para tu cuenta de AWS
CloudTrail esta activo por defecto
Obten un historial de eventos/llamadas a la API realazadas en tu cuenta de AWS
Un rastro puede aplicarse a todas las regiones(por defecto) o a una sola Region.

-   Eventos de gestion
    -   Operaciones que se realizan en los recursos de tu cuenta de AWS
    -   Los trails estan condiguradas para logs de ventos de gestion
    -   Puedes separar los Eventos de Lectura de los Eventos de Escritura
-   Eventos de datos
-   Por defecto los eventos de datos no se registran

### AWS CloudTrail Insights

Activa CloudTrail Insights para detectar actividad inusual en tu cuenta
Analiza los eventos de gestion normales para crear una linea de base
Luego analiza continuamente los eventos de escritura

Los eventos se almacenan durante 90 dias en CloudTrail, para conservar los eventos mas alla, debe registrarse en S3 y utilizar Athena

### AWS X-Ray

Resolucion de problemas de rendimiento
Comprender las dependencias en una arquitectura de microservicios
Identificar los problemas del servicio
Entrontrar errores y excepciones

### AWS CodeGuru

Un servicio con tecnologia ML para revisiones de codigo automatizadas y recomendaciones sobre el rendimiento de las aplicaciones
Funcionalidades:
-   CodeGuru Reviewer: reivisones de codigo automatizadas para el analisis estatico
-   CodeGuru Profiler: visibilidad/recomendaciones sobre el rendimiento de la aplicacion durante el tiempo de ejecucion

## AWS Status

Muestra todas las regiones, todos los servicios de salud
Muestra la informacion historica de cada dia

### AWS Personal Health Dashboard

El AWS Personal Health Dashboard proporciona alertas y orientacion para solucionar problemas cuando AWS esta experimentando eventos que pueden afectarte.
Este te ofrece una vision personalizada del rendimiento y la disponibilidad de los servicios de AWS subyacentes a tus recursos de AWS.

## Resumen 

![Monitoring Resumen](/cloud-practicioner/images/monitoring.png "Monitoring Resumen").