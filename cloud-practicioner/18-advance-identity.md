## AWS STS (Security Token Service)

Te permite crear credenciales temporales con privilegios limitados para acceder a tus recursos de AWS
Credenciales de corta duracion: configuras el periodo de caducidad
Casos de uso:

Federacion de identidades: Gestionar las identidades de los usuarios en sistemas externos y proporcionales token STS
Roles IAM para el acceso cruzado
Roles IAM para amazon EC2

## Amazon Cognito (simplificado)

Identidad para tus usuarios de aplicaciones web y moviles
En lugar de crear un usuario IAM, crea un usuario en Cognito

## Microsoft Active Directory(AD)

Base de datos de objetos - Gestion centralizada de la seguridad, creacion de cuentas, asignacion de permisos

Active Directory (AD) o Directorio Activo (DA) se pueden definir cómo los términos que utiliza Microsoft para referirse a su implementación de servicio de directorio en una red distribuida de computadoras. Utiliza distintos protocolos, principalmente LDAP, DNS, DHCP y Kerberos.

De forma sencilla se puede decir que es un servicio establecido en uno o varios servidores en donde se crean objetos tales como usuarios, equipos o grupos, con el objetivo de administrar los inicios de sesión en los equipos conectados a la red, así como también la administración de políticas en toda la red.

## AWS Single Sing-On (SSO)

Gestiona de forma centralizada el inicio de sesion unico para acceder a multiples cuentas y aplicaciones empresariales de terceros
Integrado con AWS Organizations
Soporta el Marcado SAML 2.0

## Resumen

![Advance identity](/cloud-practicioner/images/advance-identity.png "Advance identity").