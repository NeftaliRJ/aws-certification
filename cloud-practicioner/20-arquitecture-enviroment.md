## AWS Well-arquitecture
Principios generales de orientacion

Ayuda a los arquitectos de la nube a crear una infraestructura segura

-   Deja de adivinar tus necesidades de capacidad
-   Prueba los sistemas a escala de produccion
-   Automatizar para facilitar la experimentacion arquitectonica
-   Permitir arquitectura evolutivas
    -   Diseña en funcion de los requisitos cambiantes
-   Impulsar las arquitecturas utilizando datos

Principios de diseño

-   Escalabilidad: vertical y horizontal
-   Recursos desechables: los servidores deben ser desechable y facilmente configurables
-   Automatizacion: Sin servidor, infraestructura como servicio, autoescalado
-   Acoplamiento
    -   Los monolitos son aplicaciones que crecen mas y mas 
    -   Dividela en componentes mas pequeños y debilmente acoplados
-   Servicios, no servidores
    -   No utilices solo EC2
    -   Utiliza servicios gestionados, base de datos, serverless etc.

6 Pilares

-   Excelencia operativa
-   Seguridad
-   Fiabilidad
-   Eficacia de rendimiento
-   Optimizacion del rendimiento
-   Optimizacion de costos
-   Sostenibilidad

## Excelencia operativa

Incluye la capacidad de ejecutar y supervisar los sistemas para aportar valor al negocio y mejorar continuamente los procesos y procedimientos de soporte
Principios de diseño:
-   Realiza operaciones como codigo - Infraestructura como codigo
-   Anotar la documentacion - Automatizar la creacion de documentos anotada despues de cada construccion
-   Realiza cambios frecuentes, pequeños y reversibles - para que en caso de cualquier fallo, puedes revertirlo
-   Perfecciona los procedimientos de las operaciones con frecuencia - asegurate de que los miembros del equipo esten familiarizados con ellos
-   Anticipa los fallos
-   Aprende de todos los fallos operativos

Servicios

Prepara
-   AWS CloudFormation, AWS Config
Operar
-   AWS CloudTrail, Amazon CloudWatch, AWS X-Ray
Evolucionar
-   AWS CodeBuild, AWS CodeCommit, AWS CodeDeploy, AWS CodePipeline

## Seguridad

Incluye la capacidad de proteger la informacion, los sistemas y los activos a la vez que se proporciona valor empresarial mediante evaluaciones de riesgo y estrategias de mitigacion

Principios de diseño:
-   Implementar una base solida de identidad - centralizar la gestion de privilegios y reducir la dependencia de las credenciales a largo plazo
-   Habilitar la trazabilidad - Integrar logs y metricas con los sistemas para responder y actuar automaticamente
-   Aplicar la seguridad en todas las capas
-   Automatizar las mejores practicas
-   Protege los datos en transito y en reposo
-   Manten a las personas alejadas de los datos
-   Preparate para los eventos de seguridad
-   Modelo de responsabilidad compartida

Servicios

Gestion de identidades y accesos
-   IAM, AWS STS, MFA Token, AWS Organizations
Controles de deteccion
-   AWS Config, AWS  CloudTrail, AWS CloduWatch
Proteccion de la infraestructura
-   AWS CloudFront, Amazon VPC, AWS Shield
Proteccion de datos
-   KMS, S3, ELB, Amazon EBS

## Fiabilidad

Capacidad de un sistema para recuperarse de las interrupciones de la infraestructura o del servicio, adquirir dinamicamente recursos informaticos para satisfacer la demanda y mitigar las interrupciones

Principios de diseño
-   Prueba los procedimientos de recuperacion - Utiliza la automatizacion para simular diferentes fallos o para recrear escenarios que hayan provocado fallos anteriores
-   Repurate automaticamente de los fallos
-   Escala horizontalmente para aumentar la disponibilidad agregada del sistema
-   Deja de advinar la capacidad
-   Gestiona el cambio en la automatizacion

Servicios

Fudamentos
-   IAM, Amazon VPC, AWS Trusted Advisor
Gestion del cambio
-   AWS Auto Scaling, AWS Config, AWS CloudTrail
Gestion del fracaso
-   Backups, AWS CloudFormation

## Eficiencia del rendimiento

Incluye la capacidad de utilizar los recursos infromaticos de forma eficiente para satisfacer los requisitos del sistema, y de mantener esa eficiencia a medida que cambia la demanda y evolucionan tecnologias.

Principios de diseño:
-   Democratizar las tecnologias avanzadas - Las tecnologias avanzadas se convierten en servcios y, por tanto, puedes centrarte mas en el desarrollo de productos
-   Hazte global en minutos - Despliegue facile en multiples regiones
-   Utiliza arquitectura sin servidor
-   Experimenta mas a menudo
-   Simpita mecanica

Servicios

Seleccion
-   AWS Auto Scaling Group, AWS Lambda, EBS, S3, Amazon RDS
Revisar
-   AWS CloudFormation, AWS News Blog
Monitorizacion
-   Amazon CloudWatch, AWS Lambda

## Optimizacion de costes

Incluye la capacidad de ejecutar sistemas para ofrecer valor empresarial al precio mas bajo

Principios de diseño
-   Adopta un modo de consumo - Paga solo por lo que usas
-   Medir la eficiencia global
-   Deja de gastar dinero en las operaciones del centro de datos
-   Analiza y atribuye el gasto

Servicios

Conciencia del gasto
-   AWS Budgets, AWS Cost and Usage Report, AWS Cost Explorer
Recursos rentables
-   Spot Instance, Reserved Instance
Adecuacion de la oferta y la demanda
-   AWS Auto Scaling, AWS Lambda
Optimizacion en el tiempo
-   AWS Trusted Advisor

## Sostenibilidad

Este pilar se centra en minimizar el impacto medioambiental de la ejecucion de cargas de trabajo en el cloud

Princiios de diseño
-   Comprende tu impacto
-   Establece objetivos de sostenibilidad
-   Maximizar la utilizacion
-   Anticipa y adopta nuevas ofertas de HW
-   Utilizar servcios gestionados

Servicios

-   Autoescalado de EC2
-   Explorador de costes, Amazon S3 Glacier
-   Lectura local, escritura global RDS y multiples bases de datos

## Herramienta AWS Well-Architected

Herramienta gratuita para revisar tus arquitecturas con respecto al Marco de los 6 pilares de la buena arquitectura y adoptar las mejores practicas de arquitectura.

## Dimensionamiento correcto de AWS

EC2 tiene muchos tipos de instancia, pero elegir el tipo de instancia mas potente no es la mejor opcion.
El dimensionamiento correcto es el proceso de adecuar los tipos y tamaños de instancia a los requisitos de rendimiento y capacidad de tu carga de trabajo al menor coste posible.

## AWS Support

Developer - Orientacion general, Acceso por correo electronico en horario laboral
Bussiness - Chat 24x7, sistema de produccion deteriorado
Enterprise - Acceso a un Gestor Tecnico de Cuentas (TAM)

## AWS re:Post

Servicio de preguntas y respuestas gestionado por AWS que ofrece respuestas a tus preguntas tecnicas sobre AWS, revisadas por expertos y que sustituye a los fores orignales de AWS