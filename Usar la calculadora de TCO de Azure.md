# Usar la calculadora de TCO de Azure


En este tutorial usará la Calculadora del coste total de propiedad (TCO) para generar un informe de comparación de costes para un entorno local.

**Nota**: En este tutorial, se proporcionan definiciones de ejemplo de la infraestructura local y las cargas de trabajo para un centro de datos típico. Para crear un informe de la Calculadora de TCO, use las definiciones de ejemplo o proporcione detalles de su infraestructura local y sus cargas de trabajo *reales*.

# Tarea 1: Configurar la calculadora de TCO

En esta tarea agregaremos información de infraestructura a la calculadora. 

1. En el explorador navegue hasta la página [Calculadora del coste total de propiedad (TCO)](https://azure.microsoft.com/es-es/pricing/tco/calculator/).

2. Para agregar detalles de su infraestructura de servidor local, haga clic en **+ Agregar carga de trabajo del servidor** en el panel **Definir cargas de trabajo**.

    | Configuración | Valor |
    | -- | -- |
    | Nombre | **Servidores: Máquinas virtuales Windows** |
    | Carga de trabajo | **Servidor Windows/Linux** |
    | Entorno | **Máquinas virtuales** |
    | Sistema operativo | **Windows** |  
    | Máquinas virtuales | **50** |
    | Virtualización | **Hyper-V** |
    | Núcleo(s) | **8**|
    | RAM (GB) | **16** |
    | Optimizar por | **CPU** |
    | Windows Server 2008/2008 R2 | **Apagado** |

3. Seleccione **+ Agregar carga de trabajo del servidor** para hacer una fila para una definición de cargas de trabajo del servidor nueva. 

    | Configuración | Valor |
    | -- | -- |
    | Nombre | **Servidores: Máquinas virtuales Linux** |
    | Carga de trabajo | **Servidor Windows/Linux** |
    | Entorno | **Máquinas virtuales** |
    | Sistema operativo | **Linux** |  
    | Máquinas virtuales | **50** |
    | Virtualización | **VMware** |
    | Núcleo(s) | **8**|
    | RAM (GB) | **16** |
    | Optimizar por | **CPU** |
    | Windows Server 2008/2008 R2 | **Apagado** |

4. En el panel **Almacenamiento**, haga clic en **Agregar almacenamiento**.

    | Configuración | Valor |
    | -- | -- |
    | Nombre | **Almacenamiento del servidor** |
    | Tipo de almacenamiento | **Disco local/SAN** |
    | Tipo de disco | **HDD** |
    | Capacidad | **60 TB** |  
    | Copia de seguridad | **120 TB** |
    | Archivo | **0 TB** |

5. En el panel **Redes**, agregue el ancho de banda. 

    | Configuración | Valor |
    | -- | -- |
    | Ancho de banda de salida | 15 TB|

6. Haga clic en **Siguiente**.

7. Explore las opciones y realice los ajustes que necesite. 

    | Configuración | Valor |
    | -- | -- |
    | Divisa | **Euro** |

8. Haga clic en **Siguiente**.

# Tarea 2: Revisar los resultados y guardar una copia

En esta tarea revisaremos las recomendaciones de ahorro de costes y descargaremos un informe. 

1. Revise las recomendaciones y visualizaciones de ahorro de Azure.

    | Configuración | Valor |
    | -- | -- |
    | Período| **3 años** |
    | Región | **Norte de Europa** |

2. Para modificar la información que proporcionó, vaya al final de la página y haga clic en **Atrás**. 

3. Para guardar o imprimir una copia en PDF del informe, haga clic en **Descargar**.

    ![Captura de pantalla del panel de informes de la calculadora de TCO en Azure. Los campos de entrada resaltados y completados indican cómo establecer el período de la calculadora de TCO en tres años y la región en el Norte de Europa. Un gráfico muestra el coste de la infraestructura local y las cargas de trabajo compensadas frente al coste reducido de usar Azure.](../images/2001.png)

¡Enhorabuena! Ha utilizado la Calculadora de TCO para generar un informe de comparación de costes para un entorno local.
