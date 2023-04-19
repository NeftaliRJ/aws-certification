## Modelo de responsabilidad compartida de AWS

Responsabilidad de AWS - Seguridad **del** Cloud
Responsabilidad del Client - Seguridad **dentro del** Cloud

Controles compartidos:

- Gestion de parches, gestion de configuracion

## WAF y Shield

Proteccion DDos en AWS
DDos: Distributed Denial-of-Service

AWS Shield Standard: Protege contra ataques DDoS a tu sitio web y aplicaciones para todos los clientes sin coste adicional
AWS Shield Advanced: Proteccion DDoS premium 24/7
AWS WAF:

- Filtra solicitudes especificas basadas en reglas
- Protege tus aplicaciones web de las vulnerabilidades web mas comunes
- La capa es  HTTP
- Define la ACL(Lista de control de acceso a la web)

CloudFront y Route 53:

- Proteccion de la disponibilidad mediante una red de borde global
- Combinado con AWS Shield, proporciona mitigacion de ataques en el borde

## Encriptacion

Datos en reposo: datos almacenados o archivados en un dispositivo
Datos en transito: Datos que se trasladan de un lugar a otro, significa que lso datos se transfieren en la red

### Amazon KMS (Key Managment service)

Gestiona las claves de cifrado por nosotros

Cifrado opcional
Cifrado activado automaticamente

### CloudHSM

AWS proporciona el hardware de encriptacion
Hardware dedicado
Grationas por completo tus propias claves de cifrado (no AWS)

Tipos de Customer Master Keys:

- Gestionado por el cliente
- Gestionada por AWS
- Propiedad de AWS
- CloudHSM(Almacen de claves personalizadas)

### AWS Certificate Manager (ACM)

Te permite aprovisionar, gestionar y desplegar facilmente los certificados SSL/TLS
Se utiliza para proporcionar encriptacion en vuelo para los sitios web(HTTPS)

### AWS Secrets Manager

- Capacidad para forzar la rotacion de secretos cada dia
- Los secretos se encriptan mediante KMS
- Automatizar la generacion de secretos en la rotacion(Utilizacion Lambda)

### AWS Artifact (no es realmente un servicio)

Portal que proporciona a los clientes acceso bajo demanda a la documentacion de conformidad de AWS y a los acuerdo de AWS. Puede apoyar la auditoria interna o la normativa.

Artifacts Reports - Te permite descargar los documentos de seguridad y conformidad de AWS de auditores externos como ISO, PCI, SOC

Artifacts Agreements - Te permite revisar, aceptar y hacer un seguimiento del estado de los acuerdo de AWS, como el BAA, HIPAA

## AWS Guard Duty

Descubrimiento inteligente de amenzas para proteger la cuenta de AWS
Utiliza algoritmos de Machine Learning, deteccion de anomalias y datos de terceros
Los datos de entrada incluyen:

- Log de Eventos de CloudTrail

## Amazon Inspector

Evaluaciones de seguridad automatizadas

Para instancias EC2

- Aprovechando el agente de AWS System Manager(SSM)
- Analiza contra la accessibilidad a la red no intencionada

Para contenedores registran en Amazon ECR

- Evalua los contenedores a medida que se registran

**Solo para instancias EC2 e infraestructura de contenedores**

## AWS Config

Ayuda a auditar y registrar la normativa de tus recursos de AWS
Ayuda a registrar las configuraciones y los cambios a lo largo del tiempo
Posibilidad de almacenar datos de Configuracion en S3
Preguntas que se puedne resolver con AWS Config:

- Hay acceso SSH sin restricciones a mis grupos de seguridad?
- Tengo buckets publicos?

Puede recibir alertas

## Macie

Es un servicio de seguridad y privacidad de datos totalmente gestionado que utiliza el machine learning y la concordancia de patrones para descubrir y proteger tus datos sensibles en AWS.
Macie te ayuda a identificar y alertar sobre los datos sensibles, como la informacion personal identificable(PII)

## Security Hub

Herramienta de seguridad central para gestionar la seguridad en varias cuentas de AWS y automatizar las comprobaciones de seguridad. Recoge (herramienta de integracion) los posibles problemas y hallazgos de diversos servicios como (Macie, GuardDuty, Inspector).


## Amazon Detective

GuardDuty, Macie y Security Hub se utilizan para identificar posibles problemas de seguridad, o hallazgos
Amazon Detective analiza, investiga e identifica rapidamente la causa raiz de los problemas de seguridad o las actividades sospechosas.
Recoge y procesa automaticamente los eventos.

## AWS Abuse

Informar de la sospecha de que los recursos de AWS se utilizan con fines abusivos o ilegales
Algunos:
-   Spam: revisar correos proveniente de una ip propiedad de AWS
-   Escaneo de puertos
-   Ataques DoS o DDoS
-   Intentos de intrusion
-   Distribucion de malware
-   Alojar contenido censurable

## Resumen

![Security Normative](/cloud-practicioner/images/sec-normative-1.png "Security Normative").
![Security Normative](/cloud-practicioner/images/sec-normative-2.png "Security Normative").
