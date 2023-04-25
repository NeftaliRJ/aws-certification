## AWS Organizations

Servicio global, permite **gestionar varias cuentas de aws**
La cuenta principal es el master account
Beneficios de costes:
-   Facturacion sonsolidad en todas las cuentas: metodo de pago unico
-   Agrupacion de instancia EC2 reservadas
-   La api esta disponible para automatizar la creacion de cuentas
-   Restringir los privilegios de las cuentas mediante Politicas de Control de Servicios (SCP)

Estrategias multicuenta

Crear cuentas por departamento, por centro de costes en funcion de las restricciones normativas para un mejor aislamiento de los recursos para tener limites de servicio separados por cuentas

### Unidades organizativas (UO)

Unidad de negocio, ciclo de vida medioambiental, basado en proyectos

### Service Control Policies (SCP)

Lista blanca o negra de acciones IAM
Se aplica a nivel de OU o de cuenta
No se aplica a la cuenta maestra
El SCP se aplica a todos los Usuario y Roles de la cuenta
El SCP debe tener un Permitir explicito (no permite nada por defecto)

Casos de uso:

Restringir el acceso a determinado servicios

### Jerarquia SCP

El grupo padre sera el encargado de proveer en cascada la jerarquia que se respetara para las SCP

### Facturacion Consolidada

proporciona:

-   Uso combinado, combina el uso en todas la cuentas de AWS Organizations para compartir los precios por volumen
-   Una factura

### AWS Control Tower

Forma facil de configurar y gobernar un entorno AWS multicuenta seguro y con las mejores practicas, se ejecuta sobre las organizaciones de AWS

## Modelos de precios

-   Paga por lo que usas
-   Ahorra cuando reserves
-   Paga menos usando mas - paga por volumen
-   Paga menos al crecer AWS

### Precio de computacion Lambda y ECS

Lambda

-   Pago por llamada
-   Pago por duracion

## Saving plans

Comprometete a pagar una determinada cantidad de dolares por hora durante 1 o 3 años
La forma mas facil de establecer compromisos a largo plazo en AWS

### AWS Compute optimizer

Reduce el costes y mejora el rendimiento recomendado los recursos de AWS optimos para tus cargas de trabajo.
Ayuda a elegir las configuraciones optimas y a dimensionar correctamente tus cargas de trabajo (Sobre/subprovisionamiento)
Utiliza ML para anlizar las configuraciones de tus recursos y sus metricas de utilizacion CloudWatch

## Herramientas de facturacion y calculo de coste

Estimacion de costes en el Cloud:
-   Calculadora de precios

Seguimiento de los costes en el Cloud
-   Dashboard de facturacion
-   Etiquetas de asignacion

## AWS Pricing Calculator

Calcula el coste de la arquitectura de tu solucion

## Alarmas de facturacion en CloudWatch

**La metrica de los datos de facturacion se almacena en CloudWatch us-east-1**
Los datos de facturacion son los costes globales de AWS en todo el mundo

Pretende ser una simple alarma(no tan potente como AWS Budgets)

## AWS Budgets

Crea un presupuesto y envia alarmas cuando los costes superen el presupuesto
3 tipos de presupuestos: Uso, Coste, Reserva
Hasta 5 notificaciones SNS por presupuesto

2 presupuesto son gratuitos despues se cobra

## AWS Trusted Advisor

Sin necesidad de instalar nada - evaluacion de alto nivel de la cuenta de AWS
Analiza tus cuentas de AWS y proporciona recomendaciones

-   Optimizacion de coste
-   Rendimiento
-   Seguridad
-   Limites del servicio
-   Tolerancia a fallos

Planes de soporte

-   7 Core Checks
-   Full Checks

## Resumen

![Account](/cloud-practicioner/images/account.png "Account").
![Billing](/cloud-practicioner/images/billing.png "Billing").