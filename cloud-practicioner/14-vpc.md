## VPC

Para la certificacion se debe conocer

- VPC, subredes puertas de enlace de internet y puertas de enlace NAT
- Grupos de seguridad, ACL de red
- VPC Peering, VPC Endpoints
- Site to Site VPN y Direct Connect
- Transit Gateway

Virtual Private Cloud - Red privada para desplegar tus recursos

Las subredes te permiten particionar tu red dentro de tu VPC (Recurso de Zona de disponibilidad)

- Subred publica es una subred accesible desde internet
- Subred privada es una subred que no se puede acceder desde internet
- Para definir el acceso a internet y entre subredes, utilizamos las **tablas de ruta**

Los **Gateways** de internet ayudan a nuestras instancias de la VPC a conectarse con Internet

Los **Gateways NAT** (gestionados por AWS) y las Instancias NAT(autogestionadas) permiten que tus instancias en tus **subredes privadas** accedan a internet sin dejar de ser privadas

## ACL de red

NACL (ACL de Red) y grupos de seguridad

NACL

- Firewall que controla el trafico desde y hacia la subred
- Puede tener reglas ALLOW y DENY
- Se adjuntan a nivel de subred
- Las reglas incluyen direcciones IP
- **Sin estado** esto quiere decir que no maneja si una instancia acepta o no trafico entrante se limita a ser un grupo de reglas

Grupos de Seguridad

- Un firewall que controla el trafico hacia y desde una instancia EC2
- Puede tener solo reglas ALLOW
- Las reglas incluyen direcciones IP y otros grupos de seguridad
- Es con estado

### Logs de flujo de la VPC

Captura informacion sobre el trafico IP que entra en tus interfaces
Ayuda a supervisar y solucionar problemas de conectividad
Captura tambien la informacion de red  de las interfaces gestionadas

### VPC Peering

Conectar dos VPC, de forma privada utilizando la red de AWS
Haz que se comporten como si estuvieran en la misma red
No es transitiva (debe establecerse para cada VPC que necesite comunicarse entre si)

### VPC Endpoints

Los endpoints te permiten conectarte a los servciios de AWS utilizando una red privada en lugar de la red www publica
Esto te proporciona mayor seguridad y menor latencia para acceder a los servicios de AWS

VPC Endpoint Gateway: S3 y DynamoDB
VPC Endpoint Interface: el resto

## AWS PrivateLink

La forma mas segura y escalable de exponer un servicio a miles de VPCs
No require peering de VPC, gateway, etc...
Requiere un Network Load Balancer y un ENI (VPC cliente)

### Site to Site VPN

Conecta una VPN on-premise a AWS
La conexion se encripta automaticamente
Pasa por la internet publica

### Direct Connect (DX)

Estableceuna conexion fisica entre las instalaciones y AWS
la conexion es privada, segura, y rapida
Pasa por una red privada
Tardar al menos un mes en establecerse

### Cliente VPN

Conectar desde tu ordenador mediante OpenVPN a tu red privada en AWS y en las instalaciones

### Transit Gateway

Para tener peering transitivo entre miles de VPC y locales, conexion hub-and-spoke(estrella)

## Resumen

![VPC Resumen](/cloud-practicioner/images/vpc-1.png "VPC Resumen").
![VPC Resumen](/cloud-practicioner/images/vpc-2.png "VPC Resumen").
