# Detalle del procedimiento Extracción - Transformación - Carga (ETL)
![Diagrama_ETL.png](DiagramaProcesoETL_files/Diagrama_ETL.png)

## Carga

Se encarga de recopilar información de diversas fuentes, como archivos de texto, hojas de cálculo, bases de datos o sistemas de medición. Esta información puede presentarse en una variedad de formatos, y el proceso de extracción se encarga de interpretarla y organizarla para la siguiente etapa, que es la transformación.

### Detalle del proceso de extracción

1.	Identificar la Fuente de Datos: El primer paso es identificar la Fuente de Datos REST API que contendrá la información requerida. Esta fuente es proporcionada por XM SA ESP 
2.	Crear la Solicitud HTTP POST: Una vez localizamos la Fuente de Datos REST API, procedemos a crear una solicitud HTTP POST que contenga los parámetros necesarios, para la extracción de la información sobre energía eléctrica.
3.	Enviar la Solicitud y Recibir la Respuesta: Posteriormente, enviamos la solicitud a la Fuente de Datos REST API y aguardamos la respuesta, la cual se presentará en archivos tipo JSON.
4.	Almacenar la Información en Archivos JSON: Una vez obtenida la respuesta, organizamos y guardamos la información en archivos JSON, dado que esta estructura nos facilitará el acceso y la manipulación de los datos.
5.	Automatizar el Proceso con Prefect: Para simplificar la extracción de información, podemos emplear una herramienta como Prefect. Con Prefect, configuramos un flujo que maneje la solicitud HTTP POST, la recepción de la respuesta y la posterior almacenamiento en archivos JSON. Además, podemos programar la ejecución periódica del flujo, como diariamente o semanalmente.
6.	Cargar la Información en una Base de Datos en la Nube: Finalmente, una vez que los datos están en archivos JSON, podemos utilizar Prefect para cargarlos en una base de datos en la nube, la cual es DigitalOcean. Esto centralizará la información y simplificará su acceso para análisis y gestión de la información sobre energía eléctrica en Colombia.


## Transformación

La transformación es un proceso esencial que se encarga de otorgar un formato práctico y uniforme a la información obtenida durante la fase de extracción. Este procedimiento abarca diversas acciones, tales como la depuración de datos para eliminar registros duplicados o incorrectos, la conversión de unidades de medida, o incluso el enriquecimiento de la información con datos adicionales obtenidos de otras fuentes. La transformación desempeña un papel crucial en la garantía de la calidad y la utilidad de la información procesada.

### Detalle proceso de transformación 

1. Elegir las dimensiones de la base de datos extraída es el primer paso crucial en el proceso de transformación de la información. Estas dimensiones actúan como los cimientos que permiten describir de manera integral el sistema eléctrico y sus posibles eventualidades. 

2. Una vez que hemos definido las dimensiones de la base de datos extraída, es fundamental llevar a cabo la limpieza de los datos. Este proceso implica eliminar registros duplicados o erróneos, lo que asegura la coherencia y fiabilidad de la base de datos, proporcionando así una sólida base para análisis posterior, para este punto, es importante considerar la posibilidad de enriquecer los datos con información adicional que complemente la descripción del sistema eléctrico y sus eventualidades.

3. Análisis Exploratorio de Datos (EDA). Este proceso permite explorar y analizar la información transformada, proporcionando insights valiosos que facilitan la toma de decisiones informadas sobre el sistema eléctrico y sus eventualidades.

## Carga

Se carga la información transformada en el destino elegido, como una base de datos o un almacén de datos. Esto implica conectarse al destino, preparar la información, cargarla y verificar la carga para asegurar su integridad.

### Detalle proceso de carga

Se realiza la carga de la información en el destino deseado. A continuación, se detallan los pasos para la carga de la información en una base de datos en la nube de AWS, y el posterior análisis de la información con un procedimiento de machine learning y herramientas de BI (Business Intelligence):

1. Subimos la información transformada a una base de datos en la nube de AWS: Iniciamos cargando la información en una base de datos en la nube de AWS. Este paso centraliza los datos para un acceso fácil y efectivo, facilitando su análisis y gestión.

2. Prepararamos la información para el análisis: Una vez en la base de datos de AWS, se da el alistamiento de los datos para el análisis. Esto puede implicó la organización de los datos en un dataset de datos específico.

3. Realizamos el proceso de análisis con un procedimiento de machine learning: Con los datos preparados, procedemos al análisis mediante un proceso de machine learning. Este paso implica la utilización de machine learning para prever el precio de la energía eléctrica basado en diversas variables como pérdidas de energía, generación sistema ideal de energía electrica, Volumen Útil diario Energía por Embalse, Emisiones de CO2, entre otras.

4. Realizamos el proceso de analítica de BI con tableros descriptivos: Una vez obtenidos los resultados del análisis, procedemos a realizar la analítica de Business Intelligence (BI) utilizando tableros descriptivos. Estos tableros ofrecen una visión clara y comprensible de los datos, facilitando la toma de decisiones informadas sobre el sistema eléctrico y sus eventualidades.

