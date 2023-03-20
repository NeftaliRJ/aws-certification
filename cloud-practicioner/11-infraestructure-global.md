
## Por que hacer una solicitud global?

Una aplicacion global es una aplicacion despleagada en multiples geografias
Disminucion de latencia
-   Latencia es el tiempo que tarda un paquete en llegar a un servidor
-   Implementar applicacion mas cerca de usuarios para disminuir latencia
Recuperacion de desastres(DR)
Proteccion contra ataques

## Route 53

Es un DNS gestionado, DNS es una coleccion de reglas y registros que ayuda a los clientes a entender como llegar a un servidor a traves de las URL

Politicas de enrutamiento
-   Simple routing policy: no hay controles de salud
-   Weighted routing policy: distribucion de carga por instancias por peso (se le asigna a las insntacias)
-   Latency routing policy
-   Failover routing policy - recuperacion de desastres (control de salud)

## CloudFront

Red de entrega de contenidos (Content Delivery Network - CDN)
Mejora el rendimiento de lectura, el contenido se **almacena en cache en edge location**
Mejora la experiencia de los usuarios
Proteccion DDos, integracion con Shield
Es ideal para **contenidos estaticos**

**S3 Cross Region Replication (CRR)**: es ideal para **contenidos dinamicos** con baja latencia en pocas regiones

Bucket S3

-   Para distribuir archivos y almacenarlos en cache en el borde
-   Seguridad con CloudFront Origin Access Identity(OAI)
-   Puede utilizarse como entrada(subir archivos S3)

Origen personalizado (HTTP)

-   Application LoadBalancer
-   Instancias EC2
-   Sitios web S3

## S3 Transfer Accelaration

Aumenta la velocidad de transferencia transfiriendo el archvio a una ubicacion edge de AWS que reenviara los datos al bucket de S3 en la region de destino

## AWS Global Accelerator

Mejora la disponibilidad y el rendimiento global de la applicaicon a la red global de AWS
Aprovecha la red interna de AWS para optimizar la ruta hacia tu aplicacion
Se crean **2 IP AnyCast** para tu aplicacion y el trafico se envia a traves de los puntos de presencia (Edge Locations)

CloudFront vs AWS Global Accelerator

Cloudfront
-   Mejora el rendimiento de tu contenido almacenable en cache
-   El contenido se entrega en Edge Location

Global Accelerator
-   Sin almacenamiento en cache, proxy de paquetes en edge location a las aplicaciones que se ejecutan en una o mas regiones
-   Mejora el rendimiento en aplicaciones sobre TCP o UDP

## AWS Outposts

Cloud hibrido: empresas que mantenien una infraestructura local junto a una infraestructura en la nube

Los Outposts de AWS son "Racks de servidores" que ofrecen la misma infraestructura, servicios, API y herramientas de AWS para crear tus propias aplicaciones en las instalacioes al igual que en el Cloud

Aws configurara y administrara los "racks Outposts" dentro de una infraestructura local

Ventajas:
-   Acceso baja latencia a los sistemas locales
-   Procesamiento local de datos
-   Residencia de datos
-   Migracion mas facil
-   Servicios totalmente gestionado

## AWS WaveLenght

Son despliegues de infraestrctura incrustados en los centros de datos de los proveedores de telecomunicaciones de las redes 5G
Aplicaciones de latencia ultrabaja atraves de las redes 5G
Conexion sergura y de gran ancho de banda con la region AWS matriz

## AWS LocalZones

Coloca la informatica, el almacenamiento, la base de datos y otros servicios de AWS seleccionados mas cerca de los usuarios finales
Amplia tu VPC a mas ubicaciones "Extension de una region de AWS"

## Resumen 

![Infraestructure 1 Resumen](/cloud-practicioner/images/infra-global-1.png "Infraestructure 1 Resumen").
![Infraestructure 2 Resumen](/cloud-practicioner/images/infra-global-2.png "Infraestructure 2 Resumen").