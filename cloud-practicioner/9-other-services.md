## ECS

Elastic Container Service
Lanzar contenedores Docker en AWS
Debes aprovisionar y mantener la infraestructura (instancias EC2)
AWS se encarga de iniciar/parar los contenedores
Tiene integraciones con el Load Balancer

## Fargate

Lanza contenedores Docker en AWS
No aprovisionas la infraestructura (no hay intancias EC2 que gestionar)
Oferta Serverless
AWS solo ejecuta los contenedores por ti en funcion de la CPU/RAM que necesites

## ECR

Elastic Container Registry
Registro privado de Docker en AWS
Aqui es donde almacenas tus imagenes Docker para que puedan ser ejecutadas por ECS o Fargate

## Serverless

Es un nuevo paradigma en el que los desarrolladores ya no tienen que gestionar servidores
Solo despliega codigo, solo despliega funciones

Ejemplos: S3, DynamoDb, Fargate, Lambda

## Lambda

### Diferencia con EC2

| Lambda      | EC2         |
| ----------- | ----------- |
| Funciones virtuales - no hay servidores que gestionar      | Servidores virtuales en el Cloud       |
| Limitado por el tiempo   | Limitado por la RAM y CPU        |
| Ejecucion bajo demanda   | Funcionamiento continuo        |
| Escalado automatizado   | Escalado significativo        |

Beneficios:

-   Pago por solicitud y tiempo de computacion
    -   Capa gratuita: 1M de solicitudes y 400GB de computacion
-   Integrado con todo el conjunto de servicios
-   **Dirigido por eventos**

## Amazon API Gateway

Servicio totalmente gestionado para los desarrolladores creen, publiquen, mantenga y supervisen facilmente API
Serverless y escalable
Soporta APIs RESTful y APIs WebSocket

## AWS Batch

Procesamiento por lotes totalmente gestionado a cualquier escala
Ejecuta eficientemente 100,00 trabajos de computacion por lotes en AWS
Batch lanzara dinamicamente instancias EC2 o Spot Instances, porporcionando la cantidad adecuada de computacion / memoria
Los trabajos por lotes se definen como **imagenes de Docker** y ejecutados en **ECS**

| Lambda      | Batch         |
| ----------- | ----------- |
| Limite de tiempo      | Sin limite de tiempo       |
| Tiempo de ejecucion limitado   | Depende de ECS        |
| Espacio de disco temporal limitado   | Depende de EC2        |
| Serverless   | Tiempo de ejecucion sin limite siempre que este empaquetado en una imagen de Docker        |

## Lightsail

Servidores Virtuales, almacenamiento DB y redes
Precios bajos y predecibles
Alternativa sencilla al uso de EC2,RDS,ELB
Ideal para personas para personas con poca experiencia
Casos de uso:
-   Aplicaciones web sencillas
-   Sitios web
-   Tiene alta disponibilidad pero no tiene escalado

## Resumen 

![Other services Resumen](/cloud-practicioner/images/other-services-overview.png "Other services Resumen").