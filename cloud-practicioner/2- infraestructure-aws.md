
## Global infraestructure AWS

[Oficial Doc]([aws.amazon.com](https://aws.amazon.com/es/about-aws/global-infrastructure/?p=ngi&loc=1))

## AWS Regions

AWS tiene el concepto de una región, que es una ubicación física en todo el mundo donde agrupamos los centros de datos. AWS tiene regiones en todo el mundo. La mayoria de los servicios de AWS son de ambito regional.

### Como elegimos una region de AWS?

Consideraciones con la pregunta *Si necesitas lanzar una nueva applicacion, donde debes hacerlo?*

- Cumplimiento de los requisitos legales y de gobernanza de datos
- Proximidad a los clientes
- Servicios disponibles en una region
- Precios varian de una region a otra 


## AWS Availability Zones

Cada Region tiene muchas zonas de disponibilidad (normalmente 3, minimo 2 y maximo 6). Cada Zona de disponibilidad (AZ) es uno o varios centros de datos discretos con alimentacion, red y conectividad redundates.

Estan separadas unas de otras, de modo que estan aisladas a catastrofes y estan conectadas con redes de alto ancho de banda y latencia ultrabaja.

A pesar de tener un identificador por region y zona de disponibilidad como *us-east-1a* la asignacion de estas nomenclaturas se hara de forma **arbitraria** estos quiere decir que para dos usuarios diferentes la zona de disponibilidad *us-east-1a* puede no ser la misma.

## AWS Local Zones

Las zonas locales de AWS ubican el cómputo, el almacenamiento, la base de datos y otros servicios selectos de AWS más cerca de los usuarios finales. 

Cada ubicación de AWS Local Zone es una extensión de una región de AWS en donde puede ejecutar sus aplicaciones sensibles a la latencia con servicios de AWS.

Las zonas locales de AWS proporcionan una conexión segura con alto ancho de banda entre las cargas de trabajo locales y aquellas que ejecutan en la región de AWS.

## AWS Wavelength

AWS Wavelength permite a los desarrolladores crear aplicaciones que ofrecen latencias de milisegundos de un solo dígito a dispositivos móviles y usuarios finales. AWS Wavelength lleva los servicios de AWS al borde de la red 5G, lo que minimiza la latencia para conectarse a una aplicación desde un dispositivo móvil.

## AWS Outposts

AWS Outposts brinda servicios, infraestructura y modelos operativos nativos de AWS a prácticamente cualquier centro de datos, espacio de coubicación o instalación local. 

AWS Outposts está diseñado para entornos conectados y puede utilizarse para soportar cargas de trabajo que deben permanecer en las instalaciones debido a la baja latencia o las necesidades locales de procesamiento de datos.