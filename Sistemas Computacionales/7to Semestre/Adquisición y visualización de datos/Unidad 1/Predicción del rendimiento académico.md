+Una universidad desea identificar factores relacionados con el rendimiento académico de sus estudiantes y determinar si es posible predecir si un alumno aprobará una determinada asignatura.

# Pautas generales de la investigación

Para dar una mejor respuesta sobre que tipo de estadísticas y gráficas hay me apoye del modelo de IA generativa Claude Sonnet 5.

Por cuestiones de practicidad se omitió el prompt, el contexto utilizado y la respuesta. Pero se puede encontrar desde aquí [[Contexto y respuesta para la actividad 08-09-26 Ciencia de Datos]].

# Preguntas 

## 1. Problema: ¿Qué queremos conocer?

Principalmente lo que buscamos es conocer factores socioeconómicos del alumno así como el rendimiento académico del estudiante para dar una estimación de si alumno será capaz de poder aprobar una asignatura y de esta forma tomar decisiones o medidas preventivas. 

## 2. Datos: ¿Qué variables necesitaríamos? 

Algunos de las variables que debemos de tomar en cuenta se basan bajo mi opinión en 3 bases, **factores socioeconómicos, factores académicos y factores interpersonales - profesionales**. Algunos de las variables socioeconómicas podrían ser como los ingresos estimados en el domicilio del estudiante, contar con equipo de computo, contar con electricidad e internet, numero de familiares que viven en su domicilio, cuantas son las personas que tienen la posibilidad de trabajar dentro de su domicilio, si reside dentro de la ciudad o es foráneo y demás factores de catalogación.

Para los factores académicos serían el promedio general, el avance reticular, el tipo de aprendizaje que el estudiante esté más cómodo … y para los factores interpersonales - profesionales serían por ejemplo las habilidades blandas y técnicas que el alumno tenga, el número de participaciones, certificados, etc. que el alumno esté involucrado. Estos pueden ser algunos de las variables que se deben de tomar en cuenta.

## 3. Análisis: ¿Qué estadísticas y gráficas utilizarían? 

De acuerdo con la información obtenida por Anthropic (2026) nos ofrece una respuesta vasta fundamentada en el proceso de "análisis exploratorio de datos (EDA)" para determinar las variables utilizadas, sus relaciones y su visualización hacía una variable objetivo. Principalmente me quedó con lo mencionado en la **estadística descriptiva**, es decir en la forma en como determinaríamos individualmente cada variable, por **numéricas continuas o categóricas**. Además de lo comentado en la **estadística relacional**, es decir, relacionar los 2 tipos de variables que podemos encontrar. Bajo este fundamento, podemos darnos cuenta que el hecho de haber catalogado las 3 variables (factores socio-económicos, factores académicos y factores interpersonales - profesionales) caen dentro de la clasificación propia. Ahora, de acuerdo con cada categoría podemos utilizar de un conjunto de gráficas como **histogramas para representar a los factores académicos, gráficas de barras o gráfica circular para representar a los factores socio-económicos.** Y para complementarlos se utilizaría la estadística relacional con los factores interpersonales - profesionales para realizar relaciones entre variables, **utilizando ciertas gráficas como de dispersión o mapa de calor.** 

## 4. Modelo: ¿Qué algoritmos podrían usar?

Basado en las respuestas obtenidas por Anthropic (2026) puedo resumir que para el tipo de caso que estamos llevando a cabo con una clasificación binaría entre dos condiciones "Aprobará" o "No aprobará" se comenta que podemos utilizar un conjunto de diversos algoritmos de Machine Learning tales como los árboles de decisión o Random Forest, los K-Nearest Neighbors, Regresión Logística o Redes neuronales. Sin entrar tanto en materia con cada uno de ellos, cualquiera puede ser optable para poder ser utilizado mientras el conjunto de datos utilizados sean adecuados para cada algoritmo, es decir, tenemos ciertos algoritmos que obtienen buen desempeño con conjunto de datos pequeños pero que quizás no pueden ser tan confiables para ciertos modelos que requieren de un conjunto de datos más grandes. Principalmente deberíamos de evaluar cuál es el tipo de algoritmo que utilizaremos dependiendo de la población estudiantil que será estudiada.

## 5. Evaluación: ¿Cómo determinar si el modelo funciona?
De acuerdo por Anthropic (2026), podemos realizar diferentes de tipos de pruebas tales como una Matriz de confusión, Exactitud (Accuracy), Validación cruzada o comparar una baseline simple, principalmente veo más relevantes unos u otros dependiendo del resultado que obtengamos , ya que por el caso de la prueba de Exactitud, podemos obtener información certera si los datos son balanceados ( es decir que tengamos un número similar de "aprobaciones" vs "no aprobaciones"). O podemos llegar hasta soluciones simples como una baseline, es decir, proporcionando una preferencia hacia un tipo de clase. 

Hago mención en que tampoco no quiero concluir y dar una respuesta certera para determinar en cómo sabremos si el modelo funcionará . A manera práctica independientemente de la teoría, empíricamente podríamos observar estos resultados en los algoritmos si nos damos cuenta que el resultado obtenido por el modelo representa a esa población estudiada. Es decir, si en el tec nos damos cuenta que los números de predicciones de "no aprobaciones" es mayor a las de "aprobaciones". Podría ser prudente evaluar a esa población que se encuentra entre las "aprobaciones" y evaluar los 3 tipos de variables que había mencionado anteriormente.
## 6. Comunicación: ¿Cómo presentarían los resultados al director? 

Los resultados al director llegarían con un informe de los resultados del proyecto dado, dando por sentado que anteriormente ya habríamos presentado la propuesta del proyecto, haber obtenido las ciertas autorizaciones entre los directivos para su desarrollo, y haber dado informes durante el transcurso de este. El objetivo principal de la presentación de los resultados está en clarificar y dar una visión a la realidad de la dirección escolar basado en las predicciones de los modelos, para de esta forma dar un enfoque introspectivo que permita realizar cambios o medidas preventivas entre la población en riesgo, los cuales serían "no aprobaciones".

## 7 . Ética: ¿Debería utilizarse el modelo para predecir automáticamente quien puede seguir estudiando?

A mi parecer no. Me quedó con un enunciado que me comenta Anthropic (2026) al respecto.

"Los modelos predictivos en educación **pueden introducir o amplificar sesgos existentes**. Un estudio de Cornell encontró que un modelo de éxito estudiantil mostraba sesgo de género y raza en dos de tres medidas de equidad consideradas. [arxiv](https://arxiv.org/pdf/2007.00088)". Antropic (2026).

Creo que al momento de aplicar modelos predictivos en este estudio puede adjudicarnos a problemas que deberíamos de estar previniendo y no agravando, como es el sesgo existente a la educación. Aunque creo que también deberíamos de tomarlo con cuidado, ya que dependiendo del objetivo del proyecto, esto puede ayudarnos a disminuir el sesgo educativo o agrandarlo. Si este modelo lo utilizamos como una herramienta para prevenir posibles abandonos estudiantiles aplicando medidas, estaríamos teniendo una mayor visualización sobre esa población y por ende tomar medidas educativas hacia esa población especifica.

Referencias: 

Anthropic. (2026). Claude (Versión Sonnet 5) [Modelo de lenguaje grande]. https://claude.ai/share/41bbfde6-2644-49a2-b88e-e2e270c9cc09


