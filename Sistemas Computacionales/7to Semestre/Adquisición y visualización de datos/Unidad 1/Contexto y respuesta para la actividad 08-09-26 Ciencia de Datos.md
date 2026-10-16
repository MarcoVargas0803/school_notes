

> [!NOTE] Prompt Utilizado 1
> Hola Claude buenas noches. A partir de este momento eres un experto en la Materia de la Ciencia de Datos. Estoy buscando apoyo entre fuentes confiables para realizar una tarea de ejercicio de mi materia "Adquisición y Visualización de Datos" de mi especialidad "Inteligencia Artificial Aplicada a la Ciencia de Datos". Este ejercicio nos permite identificar y razonar sobre como podemos plantear la respuesta para un dado caso. A continuación te pasaré el contexto...

# Contexto 
Estudio: Predicción del rendimiento académico

Una universidad desea identificar factores relacionados con el rendimiento académico de sus estudiantes y determinar si es posible predecir si un alumno aprobará una determinada asignatura.

1. Problema: ¿Qué queremos conocer? Principalmente lo que buscamos es conocer factores socioeconómicos del alumno así como el rendimiento académico del estudiante para dar una estimación de si alumno será capaz de poder aprobar una asignatura, digamos que queremos saber de antemano cuáles son los estudiantes que probablemente tendrán dificultades en ciertas materias.
2. Datos: ¿Qué variables necesitaríamos? Algunos de las variables que debemos de tomar en cuenta se basan bajo mi opinión en 3 bases, factores socioeconómicos, factores académicos y factores interpersonales - profesionales. Algunos de las variables socioeconómicas podrían ser como los ingresos estimados en el domicilio del estudiante, contar con equipo de computo, contar con electricidad e internet, numero de familiares que viven en su domicilio, cuantas son las personas que tienen la posibilidad de trabajar dentro de su domicilio, y demás factores de catalogación. Para los factores académicos serían el promedio general, el avance reticular, el tipo de aprendizaje que el estudiante esté más comodo... y para los factores interpersonales - profesionales serían por ejemplo las habilidades blandas y técnicas que el alumno tenga, el número de participaciones, certificados, etc. que el alumno esté involucrado. Estos pueden ser algunos de las variables que se deben de tomar en cuenta.
3. Análisis: ¿Qué estadísticas y gráficas utilizarían? Principalmente se tendría que evaluar cuál sería la estadística adecuada, pero por el tipo de variables y datos, debemos de tomar en cuenta muchos factores, aunque debemos simplificarlos a ciertas materias con 2 estatus (Aprobará o No aprobará). Así que una gráfica circular o con una gráfica de barras por materia podría ser lo adecuado.
4. Modelo: ¿Qué algoritmos podrían usar? Principalmente los modelos de ordenamiento clásicos para agrupar los... (aqui me quedé sin inspiración ni información confiable para dar una respuesta certera).
5. Evaluación: ¿Cómo determinar si el modelo funciona? Se
6. Comunicación: ¿Como presentarían los resultados al director?
7. Ética: ¿Debería utilizarse el modelo para predecir automáticamente quien puede seguir estudiando?


# Respuesta

### 4. Modelo: ¿Qué algoritmos podrían usar?

Al tratarse de un problema de **clasificación binaria** (Aprobará / No aprobará), los estudios sobre predicción de rendimiento académico coinciden en un conjunto bastante estable de algoritmos clásicos de machine learning:

- **Árboles de decisión (Decision Tree / C4.5)** y **Random Forest**: muy usados porque son interpretables (importante si luego hay que explicarle al director o a un profesor por qué se predijo algo) y suelen tener buen desempeño. En un estudio con 8000 muestras y 22 atributos, el clasificador Random Forest superó a SVM en un 15% de precisión. [academia](https://www.academia.edu/68211069/Machine_Learning_Approach_for_Student_Academic_Performance_Prediction)
- **K-Nearest Neighbors (KNN)**: clasifica midiendo la distancia entre las características de un nuevo estudiante y sus vecinos más cercanos; es rápido de entrenar y poco sensible a valores atípicos. [arxiv](https://arxiv.org/pdf/2502.03143)
- **Naive Bayes**: técnica probabilística basada en el teorema de Bayes que asume independencia condicional entre variables; funciona bien con conjuntos de datos pequeños. [arxiv](https://arxiv.org/pdf/2502.03143)
- **Support Vector Machine (SVM)**: busca el hiperplano que separa las clases maximizando el margen geométrico entre ellas. [arxiv](https://arxiv.org/pdf/2502.03143)
- **Regresión Logística**: es el modelo base más simple para clasificación binaria; en un estudio con 480 registros y 17 columnas alcanzó puntajes de entrenamiento y prueba de 87.20% y 86.81% respectivamente. [academia](https://www.academia.edu/67660461/Student_Academic_Performance_Prediction_under_Various_Machine_Learning_Classification_Algorithms)
- **Redes neuronales (MLP)**: se usan cuando hay más datos disponibles; en un estudio superaron a la clasificación bayesiana cuando los datos eran continuos, aunque para bases de datos pequeñas o de un solo semestre los métodos clásicos suelen ser más apropiados. [academia](https://www.academia.edu/102512528/Student_Performance_Prediction_using_Machine_Learning)

Para tu caso (dado que combinas variables socioeconómicas, académicas e interpersonales, probablemente con pocos cientos de registros), lo razonable es plantear una comparación de al menos 3-4 modelos clásicos (Regresión Logística como línea base, Árbol de Decisión / Random Forest por interpretabilidad, y SVM o KNN como contraste) y quedarte con el que tenga mejor desempeño.

### 5. Evaluación: ¿Cómo determinar si el modelo funciona?

Para un problema de clasificación binaria, las métricas estándar son:

- **Matriz de confusión** (verdaderos/falsos positivos y negativos).
- **Exactitud (Accuracy)**: útil solo si las clases están balanceadas (similar número de "aprobará" vs "no aprobará"); si hay desbalance (por ejemplo, muchos más aprobados que reprobados), esta métrica puede engañar.
- **Precisión, Recall (sensibilidad) y F1-score**: especialmente el **recall de la clase "no aprobará"** es crítico aquí, porque el objetivo es detectar a tiempo a los estudiantes en riesgo — un falso negativo (decir que aprobará cuando en realidad no) tiene mayor costo que un falso positivo.
- **Curva ROC y AUC**: para comparar modelos de forma global.
- **Validación cruzada (k-fold cross-validation)**: para asegurar que el modelo generaliza y no solo memoriza los datos de entrenamiento.
- Comparar contra un **baseline simple** (por ejemplo, predecir siempre la clase mayoritaria) para verificar que el modelo realmente aporta valor.

### 6. Comunicación: ¿Cómo presentarían los resultados al director?

Aquí la clave es traducir resultados técnicos en información accionable:

- Evitar jerga estadística; hablar en términos de "de cada 10 estudiantes que el modelo marca en riesgo, X realmente reprueban" (esto es simplemente explicar la precisión en lenguaje natural).
- Usar visualizaciones simples: gráficas de barras por materia con el número/porcentaje de estudiantes en riesgo, un mapa de calor con los factores más influyentes (por ejemplo, importancia de variables del Random Forest), y una tabla resumen con las métricas clave.
- Presentar el modelo como una **herramienta de apoyo a la decisión** (para orientar tutorías, becas, asesorías) y no como una sentencia definitiva.
- Incluir las limitaciones del modelo (tamaño de muestra, posibles sesgos, incertidumbre) para que el director tome decisiones informadas, no ciegas al modelo.

### 7. Ética: ¿Debería usarse el modelo para predecir automáticamente quién puede seguir estudiando?

Esta es la pregunta más delicada, y la literatura es bastante clara en su cautela:

- Los modelos predictivos en educación **pueden introducir o amplificar sesgos existentes**. Un estudio de Cornell encontró que un modelo de éxito estudiantil mostraba sesgo de género y raza en dos de tres medidas de equidad consideradas. [arxiv](https://arxiv.org/pdf/2007.00088)
- El riesgo principal es que variables como raza, etnicidad o nivel socioeconómico suelen estar correlacionadas con el estatus de "riesgo", por lo que estudiantes de ciertos grupos podrían ser marcados desproporcionadamente como en riesgo o como carentes de las capacidades para cierta carrera. [newamerica](https://www.newamerica.org/education-policy/in-the-news/mathematician-brought-big-data-advising-then-deeper-questions-emerged/)
- Hay también un argumento filosófico de fondo: el problema ético central de usar analítica de aprendizaje para clasificar el riesgo de los estudiantes es que falla en reconocerlos como individuos, lo que puede afectar su capacidad de agencia — es decir, reducir a una persona a una probabilidad estadística tiene un costo moral, incluso si el modelo es técnicamente preciso. [springer](https://link.springer.com/doi/10.1007/s11423-016-9458-1)
- Por otro lado, hay beneficios reales: la analítica predictiva en educación superior ofrece la posibilidad de intervención temprana para estudiantes en riesgo, optimización de recursos y mejor toma de decisiones institucionales, siempre que se implemente con responsabilidad. [vktr](https://www.vktr.com/ai-ethics-law-risk/higher-educations-ai-dilemma-powerful-tools-dangerous-tradeoffs)

---


> [!NOTE] Prompt Utilizado 2
> Puedes ayudarme a complementar la respuesta en la pregunta 3. Me gustaría poder entrar más a detalle. Vamos a apoyarnos de las fuentes confiables para dar una respuesta fundamentada.

# Respuesta 

Claro, vamos a desglosarlo. La confusión es normal: la pregunta 3 no se trata solo de "qué gráfica hacer al final", sino de todo el proceso de **análisis exploratorio de datos (EDA)** que haces _antes_ de meter todo a un modelo. Se divide en tres niveles, y cada uno responde una pregunta distinta:

### Nivel 1 — Estadística descriptiva (entender cada variable por separado)

Antes de relacionar variables, necesitas saber cómo se comporta cada una individualmente. Aquí depende del **tipo de variable**:

- **Variables numéricas continuas** (ingresos estimados, promedio general, número de participaciones): media, mediana, desviación estándar, mínimo/máximo. Gráfica: **histograma** o **boxplot** (diagrama de caja) para ver la distribución y detectar valores atípicos (ej. un estudiante con un promedio anómalamente bajo o alto).
- **Variables categóricas** (cuenta con internet: sí/no, tipo de aprendizaje, aprobará/no aprobará): frecuencias y porcentajes. Gráfica: **gráfica de barras** o **gráfica circular** (esta última solo si son pocas categorías, 2-4 máximo, porque con más categorías se vuelve ilegible).

### Nivel 2 — Estadística relacional (cómo se relacionan las variables entre sí y con la variable objetivo)

Esto es lo más importante para tu pregunta 4 (modelado), porque aquí es donde empiezas a ver **qué variables realmente importan** para predecir si un alumno aprueba o no:

- **Numérica vs. numérica** (ej. promedio general vs. ingresos del hogar): **matriz de correlación** visualizada como **mapa de calor (heatmap)**, y **gráfica de dispersión (scatter plot)** para pares específicos.
- **Numérica vs. categórica** (ej. promedio general según si el alumno aprobó o no): **boxplot comparativo** (un boxplot de "promedio" separado por la categoría "aprobó/no aprobó") — esto te deja ver de un vistazo si los que aprueban tienen, en promedio, mejor rendimiento previo.
- **Categórica vs. categórica** (ej. tener computadora en casa vs. aprobar/no aprobar): **tablas de contingencia** y **gráficas de barras agrupadas o apiladas**.

### Nivel 3 — Visualización orientada a la variable objetivo

Como bien intuiste, cuando ya llegas al resultado final (aprobará/no aprobará por materia), una **gráfica de barras por materia** (mostrando cuántos/qué % aprobarán vs no) es adecuada. La gráfica circular funciona solo si estás mostrando la proporción para _una sola_ materia a la vez, no varias juntas.

Aplicado a tus variables concretas:

| Variable                         | Tipo                                   | Estadística                                      | Gráfica                                  |
| -------------------------------- | -------------------------------------- | ------------------------------------------------ | ---------------------------------------- |
| Ingresos estimados del hogar     | Numérica continua                      | Media, mediana, boxplot por resultado            | Histograma / Boxplot                     |
| Acceso a computadora/internet    | Categórica binaria                     | Frecuencias, tabla de contingencia con resultado | Barras                                   |
| Promedio general                 | Numérica continua                      | Media, correlación con resultado                 | Boxplot comparativo, scatter             |
| Habilidades blandas/certificados | Numérica (conteo) o categórica ordinal | Frecuencias, correlación                         | Barras, boxplot                          |
| Aprobará/No aprobará (objetivo)  | Categórica binaria                     | Proporción por materia                           | Barras por materia, circular por materia |
