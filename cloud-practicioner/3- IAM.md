## IAM

Con AWS Identity and Access Management (IAM), puede especificar quién o qué puede acceder a los servicios y recursos en AWS, administrar de forma centralizada los permisos específicos y analizar el acceso para perfeccionar los permisos en todo AWS.
IAM = Identity and Access Managment, sevicio global

- Cuenta root creada por defecto, no debe ser utilizada ni compartida
- Los usuarios son personas dentro de tu organizacion, y pueden ser agrupados
- Los grupos solo continen usuarios, no otros grupos
- Los usuarios no tienen que pertenecer a un grupos, y el usuario puede pertenecer a varios grupos

### Politica de contraseñas

- Contraseñas fuertes = mayor seguridad para tu cuenta
- En AWS, puedes configurar una politica de contraseñas:
  - Establecer una longitud minima de contraseña
  - Requerir tipos de caracteres especificos
    - Minusculas
    - Mayusculas
    - numeros
    - caracteres no alfanumericos
  - Permitir a todos los usuarios de IAM cambiar sus propias contraseñas
  - Requerir a los usuarios que cambien su contraseña despues de un tiempo
  - Impedir la reutilizacion de la contraseña

##  MFA

Los usuarios tienen acceso a tu cuenta y posiblemente pueden cambiar configuracion o eliminar recursos en tu cuenta de aws.
MFA = contraseña que conoces + dispositivo de seguridad que posees
Opciones:
-   Dispositivo virtual MFA
    -   Autenticador de Google (solo en dispositivo)
    -   Authy (multi-dispositivo)
-   Clave de seguridad del segundo factor universal (U2F)
    -   Yubikey
-   Dispositivo MFA de llavero por Hardware
-   Dispositivo MFA de llavero por Hardware por AWS 


## Permisos

- A los usuarios o grupos se les pueden asignar documentos JSON llamados politicas
- Estas politicas definen los permisos de los usuarios
- En AWS se aplica el principio minimo privilegio: no dar mas permisos de los que un usuario necesita

## Como acceder a AWS

Para acceder a AWS, tenemos 3 opciones:

-   Consola de administracion de AWS(protegida por contraseña + MFA)
-   Interfaz de linea de comandos de AWS(CLI): protegida por claves de acceso
-   AWS Software Developer Kit (SDK): para el codigo: protegido por claves de acceso
-   Las claves de acceso se generan a traves de la consola de AWS

Los usuarios gestionan sus propias claves de acceso

## CLI

-   Una herramienta que permite interactuar con los servicios de AWS mediante comando en tu shell de linea de comandos
-   Acceso directo a las API publicas de lso servicios de AWS
-   Puedes desarrollar scripts para gestionar tus recursos
-   Es de codigo de abierto

## SDK AWS

Kit de desarrollo de software de AWS(AWS SDK)
APIs especificas para cada lenguaje(conjunto de bibliotecas)
Permite acceder y administrar lso servicios de AWS mediante programacion
Integrado en la applicacion
Admite:
-   SDKs (JS, Python, PHP, .NET), SDKs para moviles, SDKs para dispositivos IoT

AWS CloudShell esta designado en base a regiones

## Roles IAM para los servicios

-   Algun servicio de AWS tendra que realizar acciones en tu nombre
-   Para ello, asignaremos permisos a los servicios de AWS con Roles IAM

## Herramientas de seguridad

IAM Credential Report
-   Un informe que enumera todos los usuarios de tu cuenta y el stado de tus diversas credencias

IAM Access Advisor
-   Muestra los permisos de servicio concedidos a un usuario y cuando se accedio a estos servicios por ultima vez


## Buenas practicas

-   No utilices la cuenta root excepto para la configuracion de la cuenta AWS
-   Un usuario fisico = un usuario AWS
-   asignar usuarios a grupos y asignar permisos a grupos
-   Crear una politica de Contraseñas fuerte
-   Crear y utilizar Roles para dar permisos a los servicios de AWS
-   Utilizar claves de acceso para el accesso programatico
-   Revisar los permisos de tu cuenta con el informe de credenciales de IAM
-   No compartir nunca los usuarios de IAM ni las claves de acceso