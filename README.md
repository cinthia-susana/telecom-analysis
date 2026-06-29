### Análisis de Comportamiento de Usuarios (ConnectaTel)
El objetivo principal de este proyecto es analizar los patrones de consumo de los clientes de ConnectaTel para identificar oportunidades de optimización en la oferta actual de planes. A través del análisis de datos, se segmentó a la población por edad, volumen y duración de llamadas y mensajes para fundamentar decisiones estratégicas de negocio basadas en datos reales.

El análisis se basó en las siguientes bases de datos estructuradas:
-plans.csv: Catálogo de planes con sus precios y beneficios. 

-user_profile.csv: Contiene la información de los usuarios, incluyendo ID único, edad y el tipo de plan actual (Básico / Premium).

-usage.csv: Contiene el registro histórico de las interacciones de los usuarios. Incluye duración de las llamadas en minutos y la cantidad de los mensajes enviados.

##Etapas de análisis

El flujo de trabajo se desarrolló de la siguiente manera:

Exploración inicial e imputación de nulos: Exploración de los datos. Se trataron nulos críticos preservando la consistencia del negocio (imputación lógica con 0 para ausencias de consumo y eliminación del 1% de registros sin fecha).

Procesamiento y optimización de código: Limpieza de duplicados, corrección de tipos de datos y creación de nuevas variables categóricas (grupo_uso y grupo_edad)

Análisis exploratorio de datos: Generación de distribuciones visuales (histogramas y diagramas de caja) para identificar sesgos y detectar outliers extremos en la duración de las llamadas.

Segmentación y conclusiones de negocio: Cruce de edad con variables de consumo para proponer el rediseño de planes comerciales y estrategias de control de fraude.

##Guía de Reproducción Básica
Para replicar los resultados y gráficas de este análisis, se recomienda seguir los siguientes pasos:

-Ejecuta la primera celda de código para importar las librerías esenciales (pandas, numpy, seaborn y matplotlib.pyplot).

-Verifica que las rutas de lectura en pd.read_csv() apunten correctamente al nombre de los archivos cargados en el entorno.

-Corre las celdas de forma secuencial de arriba hacia abajo. Asegúrate de no alterar el orden de ejecución de las celdas de limpieza, ya que los análisis visuales posteriores dependen estrictamente de que las columnas hayan sido preprocesadas correctamente.
