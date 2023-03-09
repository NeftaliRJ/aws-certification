## Almacenamiento de instancias de EC2

### Volumen EBS

Principales caracteristicas: 

-   Elastick Block Store es una unidad de red que puede adjuntar a las instancias mientras se ejecutan
-   Permite que las instancias persistan los datos, incluso despues de su finalizacion ademas SOLO pueden montarse en UNA instancia a la vez.
-   Estan vinculadas a una zona de disponibilidad especifica
-   Nivel Gratuito: 30 GB de almacenamiento EBS gratuito de tipo Proposito general (SSD)

Consideraciones:

-   Es una unidad de Red (es decir, no es una unidad fisica)
    -   Utiliza la red para comunicar la instancia, lo que significa que puede haber un poco de latencia
    -   Se puede separar de una instancia EC2 y conectarla a otra rapidamente
-   Esta bloqueado en una zona de disponibilidad
    -   Un volumnen EBS en us-east-1a no puede adjuntarse a us-east-1b
    -   Para trasladar un volumen, primero hay que hacer un snapshot del mismo

El atributo "Delete on Termination"
-   Por defecto, se elimina el volumen EBS root (check marcado)
-   Por defecto, cualquier otro volumne EBS adjunto no se elimina (check no marcado)

## Snapshot

Haz una copia de seguridad de tu volumen EBS en un momento dado
No es necesario separar el volumen para hacer la instantania, pero se recomienda
Puedes copiar la instantaneas a traves de AZ o region

Archivo de Snapshots de EBS
-   Mover un snapshot a un "nivel de archivo" es un 75% mas barato
-   La restauracion del archivo tarda entre 24 y 72 horas

Papelera de reciclaje para Snapshots EBS
-   Configura reglas para retener los snapshots eliminados para poder recuperarlos despues de un borrado accidental
-   Especifica retencion (1 dia a 1 año)

## AMI

Amazon Machine Image

Las AMI son una personalizacion de una instancia EC2:
-   Añades tu propio SW, configuracion, etc...
-   Tiempo de arranque/configuracion mas rapido porque todo el SW esta preempaquetado
Las AMI se contruyen para una region especifica
Puedes lanzar instancias EC2 desde:
-   Una AMI publica: proporcionada por AWS
-   propia AMI: la crear y la mantienes tu

## EC2 Instance Store

Los volumenes EBS son unidades de red con un rendimiento bueno pero "limitado"
Si necesitas un disco de HW de alto rendimiento, utilizas EC2 Instance Store

- Mejor Rendimiento de E/S
- Los almacenes de instancias EC2 pierden su almacenamiento si se detienen
- Bueno para el buffer/cache/datos de memoria vitual/contenido temporal
- Riesgo de perdida de datos si el HW falla

## EFS Elastic File System

-   NFS gestionado que puede montarse en 100 Ec2s
-   EFD funciona con instancias EC2 de Linux en multi-AZ
-   Alta disponibilidad, escalable, caro, pago por uso, sin planificacion de capacidad

### EFS Infrequent Access

Clase de almacenamiento con costes optimizados para los archivos a los que no se accede a diario
EFS movera automaticamente tus archivos a EFS-IA basandose en la ultima vez que se accedio a ellos

## Resumen

![Resumen](/cloud-practicioner/images/ec2-storage-brief.png "Resumen").