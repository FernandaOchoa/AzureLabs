---
wts:
    title: 'Cálcular el Acuerdo de nivel de servicio compuesto'
    module: 'Módulo 06: Descripción de los acuerdos de nivel de servicio y Azure Cost Management'
---
# Calcular acuerdos de nivel de servicio compuestos 

En este tutorial determinaremos el Acuerdo de nivel de servicio disponible de los servicios de Azure y luego calcularemos la disponibilidad basada en el Acuerdo compuesto de la aplicación esperada.

Nuestra aplicación de ejemplo consta de estos servicios de Azure. No entraremos en configuraciones ni consideraciones arquitectónicas en detalle. La intención aquí es dar un ejemplo de alto nivel.

+ **App Service**: Para hospedar la aplicación.
+ **Azure AD B2C**: Para autenticar inicios de sesión de usuarios y administrar perfiles.
+ **Application Gateway**: Para administrar el acceso a la aplicación y la escala. 
+ **Azure SQL Database**: Para almacenar datos de la aplicación. 

# Tarea 1: Determinar los valores de porcentaje de tiempo de actividad del Acuerdo de nivel de servicio para nuestra aplicación

1. En un explorador, vaya a la página [Resumen de SLA para los servicios de Azure](https://azure.microsoft.com/es-es/support/legal/sla/summary/).

2. Localice el valor de tiempo de actividad del Acuerdo de nivel de servicio de **App Service**, **99,95 %**. Haga clic en **Ver detalles completos** y luego expanda los **detalles del SLA**. Observe los **Porcentajes mensuales del tiempo de actividad** y los **Créditos de servicio**.

3. Regrese a la página web del Acuerdo de nivel de servicio, localice el servicio **Azure Active Directory B2C** y determine el valor de tiempo de actividad del acuerdo (SLA), **99,9 %**. 

4. Localice el valor de tiempo de actividad del Acuerdo de nivel de servicio de **Application Gateway**, **99,95 %**. 

5. La base de datos de Azure SQL usa niveles premium, pero no está configurada para implementaciones con redundancia de zona. Localice el valor de tiempo de actividad del SLA de **Azure SQL Database**, **99,99%**. 

    **Nota**: Existen diferentes valores de tiempo de actividad para diferentes configuraciones e implementaciones de Azure SQL Database. Es importante que tenga claros los valores de tiempo de actividad requeridos al planificar y calcular el coste de su implementación y configuración. Pequeños cambios en el tiempo de actividad pueden tener un impacto en los costes del servicio, así como aumentar potencialmente la complejidad en la configuración. Otros servicios que pueden ser de interés en la página web de resumen del Acuerdo de nivel de servicio de Azure incluirían las **Maquinas virtuales**, **Cuentas de almacenamiento** y **Cosmos DB**.

# Tarea 2: Calcular el tiempo de actividad del porcentaje del Acuerdo de nivel de servicio compuesto de la aplicación

1. Si alguno de los servicios que comprende nuestra aplicación no está disponible, tampoco lo estará la aplicación para que los usuarios inicien sesión y la usen. Como tal, el tiempo de actividad total para nuestra aplicación consiste en lo siguiente:

    **% de tiempo de actividad de App Service** X **% de tiempo de actividad de Azure AD B2C** X **% de tiempo de actividad de Azure Application Gateway** X **% de tiempo de actividad de Azure SQL Database** = **% de tiempo de actividad total**

    que en términos de porcentaje es:

    **99,95 %** X **99,9 %** X **99,95 %** X **99,99 %** = **99,79 %**

    Esta es la disponibilidad esperada basada en el Acuerdo de nivel de servicio (SLA) de nuestra aplicación con los servicios y la arquitectura actuales.

¡Enhorabuena! Ha determinado el tiempo de actividad basado en el Acuerdo de nivel de servicio (SLA) para cada uno de los servicios en nuestra aplicación de muestra y luego ha calculado la disponibilidad esperada compuesta basada en el Acuerdo de nivel de servicio para la aplicación.