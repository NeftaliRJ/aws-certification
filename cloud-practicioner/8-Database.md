## Bases de datos

Aws ofrece el uso para gestionar diferentes bases de datos
Beneficios:

-   Aprovisionamiento rapito, alta disponibilidad
-   Copia de seguridad
-   Parcheo del SO
-   Monitorizacion, alertas

Ventaja sobre el uso de RDS frente el despliegue de la BD en EC2:

-   Monitorizacion
-   Replicas de lectura para mejorar el rendimiento de lectura
-   Configuracion multi AZ
-   Ventanas de mantenimiento
-   No puedes acceder por SSH


## Amazon Aurora

-   Aurora es una tecnologia propietaria de AWS
-   Postgrest y MySQL son compatibles
-   Optimizada para AWS Cloud y afirma que mejora 5 veces el rendimiento de MySQL en RDS y 3 veces el rendimiento en Postgrest
-   Almacenamiento crece automaticamente en incrementos de 10 GB
-   Aurora cuesta mas que RDS (20% mas) pero es mas eficiente
-   No esta a nivel gratuito

## Replicas

-   Escala la carga de trabajo de lectura de tu BD
-   Puedes crear hasta 5 replicas de lectura
-   Los datos solo se escriben en la BD principal

## Multi-AZ

-   Recuperacion en caso de caida de la AZ (alta disponibilidad)
-   Los datos solo se leen/escriben en la base de datos principal
-   Solo se puede tener otra AZ como conmutacion por error

## Multi-region

-   Recuperacion de desastres en caso de problema de region
-   Rendimiento local para lecturas globales
-   Coste de replicacion

## Amazon ElasticCache

-   ElastiCache es para conseguir Redis o Memcached gestionados
-   Cache = bases de datos en memoria de alto rendimiento y baja latencia
-   Ayuda a reducir la caga de las bases de datos para cargas de trabajo de lectura intensiva

AWS se encarga del mantenimiento /parche del SO, optimizaciones, instalacion, configuracion etc..

## DynamoDB

Totalmente gestionado con replicacion a traves de 3 AZ
Base de datos NoSQL
Escala a cargas de trabajo masicas
Latencia de un milisegundo: recuperacion de baja latencia

Usa de tipo de dato Clave/valor

### DynamoDB Accelarator - DAX

Cache en memoria totalmente gestionada para DynamoDB
Mejora el rendimiento x10
Seguridad, alta escalabilidad y alta disponibilidad
Diferencia con ElastiCache a nivel de CCP: DAX solo se utiliza y se integra con DynamoDB, mientras que ElastiCache puede utilizarse para otras bases de datos

## Redshift

-  Basado en PostgrestSQL, pero no se utiliza para OLTP
-  Es OLAP - **procesamiento analitico en linea** (analisis y almacenamiento de datos)
-  Carga los datos una vez cada hora, no cada segundo
-  Rendimiento **10 veces superior** al de otros almacenes de datos
-  Almacenamiento de datos en columnas

## EMR

-   Elastic MapReduce
-   Ayuda a crear **clusters Hadoop** (Big Data) para **analizar y procesar una gran cantidad de datos**
-   Los clusters pueden estar formados por cientos de instancias EC2
-   Autoescalado e integrado con instancias Spot
-   Caso de uso: **procesamiento de datos**, machine learning, indexacion web ...

## Athena

-   Servicio de consulta sin servidor para analizar los datos almacenados en Amazon S3
-   Utiliza SQL estandar para consultar los archivos
-   Precio: 5 USD por TB de datos analizados
-   Caso de uso: Inteligencia empresarial/analisis/informes etc..
-   Examen: **analiza los datos en S3 usando SQL sin servidor**

## QuickSight

-   Servicio de inteligencia empresarial impulsado por Machine Learning **sin servidor** para crear **Dashboard** interactivos
-   Rapido, escalable automaticamente, integrable
-   Casos de uso
    -   Analisis empresarial
    -   Construir visualizacion
    -   Realizar analisis adhoc

## DocumentDB

-   DocumentDB es lo mismo que **MongoDB**
-   Totalmente gestionado, de alta disponibilidad con replicacion a traves de 3 AZ
-   Escala automaticamente a cargas de trabajo con millones de peticiones por segundo

## Neptune

-   Base de datos **grafica** totalmente gestionado
-   Un **conjunto de datos de grafos** podria ser una red social
-   Alta disponibilidad en 3 AZ, con hasta 15 replicas de lectura
-   Construye y ejecuta aplicacion que trabajen con conjuntos de datos altamente conectados

## QLDB

-   Quantum Ledger Database (base de datos de libros contables)
-   Un libro de contabilidad es un libro que registra las **transacciones financieras**
-   Totalmente gestionada, sin servidor, de alta disponibilidad, con replicacion en 3 AZ
-   Se utiliza para **revisar el historial de todos los cambios** realizados en los datos de la applicacion
-   Sistema **inmutable**: ninguna entrada  puede ser elimianda
-   **Rendimiento 2-3 veces mejor** que lso marcos de blockchain
-   Diferencia con Amazon Managed Blockchain: **no hay componente de descentralizacion**

## Amazon Managed Blockchain

-   Permite crear aplicaciones en las que se pueden **ejecutar transacciones sin necesidad de una autoridad central** de confianza
-   Servicio gestionado para:
    -   Unirte a redes publicas de blockchain
    -   crear propia red privada escalable
-   Compatible con los marcos Hyperledfer y Ethereum

## AWS Glue

-   Servicio gestionado de **extraccion, transformacion y carga** (ETL)
-   Util para preparar datos para la analitica
-   Servicio totalmente serverless

## DMS - Database Migration Service

-   Migra de fomra rapida y segura las bases de datos a AWS, con capacidad de recuperacion y autocuracion
-   Las bases de datos de origen sigue disponible durante la migracion

## Resumen 

![Database Resumen](/cloud-practicioner/images/database-overview.png "Database Resumen").
