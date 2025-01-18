# Expansion-Estrategica-de-Laboratorios-para-Investigacion-y-Vacunacion-de-Covid-19
Análisis exhaustivo de los datos de COVID-19 y otros indicadores relevantes en seis países de América Latina. Para el análisis, se emplearon las bibliotecas de Python: pandas, numpy, seaborn y matplotlib. A lo largo del proceso, se realizaron limpiezas, filtrados y cálculos estadísticos para obtener conclusiones sobre la evolución del virus, el impacto de las vacunaciones, y la relación de ciertas condiciones con la mortalidad. Posteriormente, el dataset filtrado y limpio se cargó en Power BI, donde se desarrolló un dashboard interactivo para visualizar los hallazgos.
Desarrollo del proyecto
Paso 1: Configuración del Entorno
Para empezar, se creó un entorno virtual donde se instalaron las bibliotecas necesarias. Esto permitió mantener la consistencia y compatibilidad de los paquetes.
Paso 2: Carga y Filtrado de Datos
El dataset inicial fue cargado usando pandas. La estructura general de los datos se revisó para identificar la cantidad de columnas y tipos de datos. Se seleccionaron solo las filas correspondientes a los países de interés.
Paso 3: Limpieza y Preprocesamiento
Se realizó un análisis de los valores nulos para cada columna. Como resultado:
Se utilizaron distintos métodos para imputar valores nulos, basándose en la media de cada país para las columnas de casos confirmados, fallecidos, temperaturas, y precipitación.
Las columnas de fecha se convirtieron al formato datetime, y se estableció la fecha como índice para facilitar la organización temporal.
Las columnas correspondientes a dosis de vacunas administradas y recuperados acumulados se trataron para llenar valores nulos.
Paso 4: Análisis Estadístico Descriptivo
Para entender mejor el dataset, se calcularon estadísticas descriptivas como la media, mediana, desviación estándar, valor mínimo y máximo para cada columna numérica. Además, se generó una matriz de correlación para identificar la relación entre variables, mostrando relaciones como la densidad poblacional y el número de casos confirmados.
Paso 5: Visualización de Datos
Gráficos de Barras y Distribuciones
Se desarrollaron gráficos de barras para comparar las variables clave por país, incluyendo:
Casos confirmados y fallecidos: Se mostró la evolución mensual y semanal de estos valores en 2021.
Distribución de la población por grupos de edad: Este análisis permitió ver la estructura etaria en cada país.
Gráficos de Dispersión y Correlación
Se emplearon gráficos de dispersión para evaluar la relación entre temperatura promedio y casos confirmados. También se analizaron factores de como (diabetes y prevalencia de fumadores) en relación con la tasa de mortalidad.
Análisis de la Vacunación
Se estudió el progreso de la vacunación por país y grupo de edad. Los gráficos reflejaron la proporción de dosis administradas por grupo etario, lo que permitió evaluar la cobertura de vacunación en cada país.
Análisis de Mortalidad
Gráficos de barras compararon la tasa de mortalidad entre géneros, observando que la mortalidad masculina superaba a la femenina en todos los países. Los resultados indicaron que el tabaquismo y la diabetes mostraban una fuerte relación con la mortalidad.
Paso 6: Generación del Dashboard en Power BI
El dataset procesado y filtrado fue exportado y cargado en Power BI mediante un script de Python. Con estos datos, se desarrolló un dashboard interactivo que incluye:
Gráficos de línea y de barras para visualizar la evolución de casos y muertes por país y grupo etario.
Gráficos de dispersión que muestran relaciones como la temperatura y el número de casos, y la prevalencia de ciertas enfermedades con la mortalidad.
Filtros interactivos que permiten analizar los datos por año y categoría.
EDA e insights
1. Evolución Temporal de Casos y Muertes
Descenso gradual: Se observó un descenso en el número de casos y muertes a medida que avanzaba el 2021, probablemente asociado al incremento en la cobertura de vacunación.
Picos significativos: Hubo un pico de casos confirmados en febrero de 2021, seguido de una rápida disminución. Este patrón sugiere el efecto de intervenciones sanitarias o el impacto de restricciones temporales.
2. Cobertura de Vacunación y Reducción de Casos
Chile como líder en vacunación: Chile mostró una alta cobertura de vacunación en comparación con otros países de la región, lo cual se reflejó en una reducción más acelerada en los casos y muertes.
Desigualdad en cobertura por país: Otros países, como Brasil y Colombia, presentaron menor cobertura de vacunación, lo que podría explicar una mayor persistencia en el número de casos y muertes.
3. Comorbilidades y Mortalidad
Tabaquismo y diabetes: Estas comorbilidades mostraron una correlación positiva con la tasa de mortalidad en varios países. La alta prevalencia de estas condiciones aumenta la vulnerabilidad de la población, lo que sugiere la necesidad de campañas de salud preventiva.
Mayor mortalidad en hombres: En todos los países estudiados, la tasa de mortalidad masculina fue superior a la femenina. Este hallazgo sugiere que existen factores de riesgo adicionales entre la población masculina que deberían ser estudiados y abordados.
4. Impacto de la Urbanización en la Propagación del COVID-19
Alta densidad poblacional asociada a mayor propagación: Los países con mayor densidad y población urbana mostraron un número de casos confirmados proporcionalmente mayor, lo que indica que la urbanización es un factor clave en la propagación del virus.
Distribución desigual en zonas rurales y urbanas: Países con alta proporción de población urbana, como Brasil, tendieron a tener una tasa de propagación más rápida en comparación con otros con menor densidad.

5. Estrategias de Vacunación y Eficacia
Vacunación temprana y descenso de casos: La correlación entre una mayor cobertura de vacunación y una disminución en el número de casos y muertes fue evidente, especialmente en Chile y Perú. Esto resalta la efectividad de una estrategia de vacunación temprana y amplia.
Retos en Colombia y Brasil: Estos países presentaron una menor proporción de vacunación y un mayor porcentaje de muertes, lo que sugiere áreas de mejora en sus estrategias de inmunización y en la infraestructura de salud pública.

Análisis del dashboard

Métricas Generales:
Esta página presenta una visión general de las principales métricas relacionadas con la pandemia. Las cuatro tarjetas en la parte superior muestran los valores acumulados más relevantes: infecciones, muertes, recuperaciones y dosis administradas.
Los gráficos de barras interactivos facilitan la comparación entre muertes acumuladas e infecciones y muestran cómo han variado estas métricas por mes, año y país. Además, el usuario puede aplicar filtros específicos de año y país o eliminarlos con el botón de reinicio.
Esta página ayuda a visualizar el impacto general de la pandemia en cada país y cómo el virus ha evolucionado a lo largo del tiempo. La comparación entre infecciones y muertes acumuladas es útil para identificar los países más afectados y evaluar la efectividad de las medidas sanitarias.
Análisis Geoespacial:
Presenta un mapa interactivo que permite visualizar la distribución de los principales indicadores de la pandemia (confirmados, fallecidos, vacunados y recuperados) por país en América Latina. El usuario puede seleccionar el indicador de interés mediante un segmentador, lo que actualiza automáticamente el mapa, mostrando los valores máximos acumulados por país. La representación geográfica facilita identificar patrones y diferencias regionales en la evolución de la pandemia, permitiendo un análisis visual claro y efectivo. Además, la página cuenta con filtros interactivos que permiten analizar los datos en periodos específicos, brindando mayor flexibilidad al usuario.
Análisis de Temperatura con mapas de dispersión:
Muestra la relación entre la temperatura promedio y los casos de COVID-19, permitiendo observar si existe alguna correlación entre el clima y la propagación del virus.
Esta información puede ayudar a diseñar estrategias de vacunación y medidas de prevención, especialmente en países con estaciones o climas variados.

Análisis temporal entre vacunación y muertes:
Esta página muestra la correlación entre la cobertura de vacunación y la reducción de casos de COVID-19, junto con un análisis de la evolución de la mortalidad.
Los datos refuerzan la eficacia de las vacunas, sugiriendo que un aumento en la cobertura de vacunación es una estrategia efectiva para disminuir la mortalidad y controlar la propagación.

Estrategias de vacunación
Muestra la efectividad de la vacunación en el control de la pandemia, tomando la población y la cantidad de vacunas aplicadas resaltando países con estrategias exitosas y aquellos que podrían mejorar sus programas de inmunización.

Mapas Informativos
Esta página utiliza mapas para representar visualmente los datos por ubicación geográfica, permitiendo una rápida identificación de los países más afectados.
La información geoespacial es clave para identificar regiones con alta demanda de recursos y establecer ubicaciones estratégicas para la expansión de laboratorios.
Conclusiones:
La última página del dashboard presenta un resumen de los hallazgos clave y recomendaciones estratégicas para la expansión de laboratorios.
Este resumen facilita una revisión rápida de los insights principales, proporcionando una base sólida para la toma de decisiones informadas sobre la ubicación de los laboratorios de investigación y vacunación.

Conclusiones y Recomendaciones
El análisis demostró que la densidad poblacional, la proporción de población urbana y la prevalencia de enfermedades, como diabetes y tabaquismo, son factores clave que influyen en la tasa de propagación y mortalidad del COVID-19 en estos países. Además, los resultados de la vacunación variaron significativamente entre países, con estrategias más efectivas en Chile y Perú, que experimentaron una reducción más acelerada en los casos confirmados y muertes.
Los hallazgos sugieren que una estrategia de vacunación eficiente, combinada con inversiones en infraestructura de salud y campañas de prevención de comorbilidades, es crucial para mejorar la resiliencia ante futuras pandemias.
Ubicaciones Óptimas para la Expansión de Laboratorios Farmacéuticos
Considerando todos los factores analizados (densidad poblacional, infraestructura de salud, capacidad de distribución, necesidades sanitarias y la alta demanda de vacunas), se identificaron las siguientes ubicaciones óptimas para la expansión de laboratorios farmacéuticos:
Brasil: presenta una alta densidad poblacional y una gran necesidad de infraestructura sanitaria adicional. La concentración urbana en estas áreas también facilitaría la distribución de productos farmacéuticos y vacunas, maximizando el alcance de los nuevos laboratorios.
México: La Ciudad de México es altamente poblada y tiene un nivel de urbanización elevado, lo que la convierte en un lugar ideal para la expansión de laboratorios farmacéuticos que puedan atender la demanda de la región. Monterrey, por su ubicación estratégica cerca de la frontera, facilitaría la distribución tanto a nivel nacional como hacia los Estados Unidos.
Colombia (Bogotá): Bogotá cuenta con una alta densidad poblacional y presenta una infraestructura en desarrollo para la distribución farmacéutica. La expansión de laboratorios aquí permitiría mejorar la disponibilidad de vacunas y medicamentos en toda la región andina.

Perú (Lima): La capital peruana es un centro estratégico para la distribución a diversas áreas, incluidas las rurales, que necesitan mayor apoyo en infraestructura sanitaria. La apertura de laboratorios en Lima facilitaría el acceso a vacunas y medicamentos en el país.
 
Reflexión personal
Durante el desarrollo de este proyecto, he profundizado mis conocimientos en programación y aprendí a crear códigos que automatizan procesos de limpieza y procesamiento de datos. La combinación de bibliotecas como Numpy, Pandas, Seaborn y Matplotlib me permitió no solo manipular archivos CSV de forma eficiente, sino también acceder a bases de datos SQL para extraer datos, lo cual amplía significativamente el alcance de cualquier análisis. Además, comprendí cómo usar estas herramientas para procesar grandes volúmenes de datos (más de 13 millones de registros) de manera ágil y sin comprometer el rendimiento, lo cual es esencial en el análisis de datos a gran escala.
Otro aprendizaje importante fue el flujo de trabajo entre Python y Power BI. Una vez que los datos fueron procesados y limpiados en Python, la integración con Power BI fue fluida, y el resultado fue un dashboard interactivo y estético que permitió comunicar los insights de manera accesible y visual. Este flujo me enseñó a combinar las capacidades analíticas de Python con la visualización avanzada de Power BI, logrando un enfoque completo que permite tanto el análisis como la presentación de resultados en un entorno empresarial.

Reflexión sobre el Enfoque en el Proyecto
Si tuviera que volver a empezar este proyecto, sin duda utilizaría las mismas herramientas y enfoques, ya que han demostrado ser sumamente versátiles y eficaces. El uso de Numpy, Pandas, Seaborn y Matplotlib permitió un análisis profundo y rápido, y la conexión a Power BI dio lugar a visualizaciones interactivas que enriquecieron el entendimiento de los datos.
¿Cambiaría algo? Quizás exploraría una mayor optimización del código para hacer el proceso aún más rápido y eficiente, sobre todo si trabajara con datasets aún más grandes o en entornos de colaboración. También podría considerar el uso de técnicas de procesamiento en la nube para manejar datos en paralelo, si fuera necesario analizar datasets de un tamaño significativamente mayor.

Conclusión
Este proyecto no solo me permitió consolidar mis habilidades técnicas como Analista de Datos, sino también ver la importancia de una buena planificación y estructura en el código para llevar a cabo análisis de datos efectivos y presentar resultados que generen valor. Además, trabajar con herramientas de Python junto con Power BI me dio una visión completa del proceso, desde la limpieza y transformación de datos hasta la creación de dashboards interactivos para la toma de decisiones.



