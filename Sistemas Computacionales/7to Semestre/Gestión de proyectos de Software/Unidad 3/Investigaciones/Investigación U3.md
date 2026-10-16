
Sacado del libro: Ingeniería de Software un enfoque desde la guía SWEBOK. Salvador Sanchez.



Estimación: Proceso de determinar una variable no conocida a partir de otras conocidas. 

La estimación de coste, plazos y esfuerzo es parte esencial de la planificación de cualquier tipo de proyectos.

La correcta estimación del coste y el esfuerzo es una tarea crítica. Subestimar supondrá casi con seguridad que el proyecto se llevará a cabo con pérdidas para la organización, pues al no poder deidcarle los recursos necesarios, es muy posible que el proyecto se retrase, que el producto resultante sea de una calidad inferior a la requerida y que el personal tenga que hacer horas extra (a costo de la propia moral del equipo). En un caso extremo, el proyecto tendrá que ser cancelado.

Una sobreestimación, por el contrario, lleva a lo que se conoce humorisiticamente como la "Ley de Parkinson" el trabajo se expande hasta rellenar todo el volumen disponible. Suele ser visto comunmente en tecnicas como el coste ganador en licitaciones publicas. Según esta técnica, lo que se estima fundamentalmente es un presupuesto que supere al de los competidores para después ajustar el resto de parámetros que permitirán llevar a cabo el proyecto en función de dicho presupuesto.

Para realizar una correcta estimación de coste y esfuerzo, evitando los problemas asociados a una estimación inadecuada, es necesario establecer con claridad los objetivos de proyecto, procurar que los requisitos estén bien especificados y recabar toda la información disponible en el momento. Todo ello debería realizarse varias veces durante el desarrollo, pues segun avanza el proyecto tendremos más información disponible: si las nuevas estimaciones varían mucho de las originales, deberán tomarse medidas correctivas.

En cuanto a los métodos de estimación, existen varios, y no puede decirse que unos ean mejores que otros , o que haya uno que aporte los mejores resultados. Resulta habitual, en consecuencia, aplicar más de uno en un mismo proyecto, pues unos métodos pueden complementar a otros como forma de verificar las estimaciones.

A continuación se describen brevemente algunas categorías en las que se pueden agrupar las técnicas de estimación:

- Estimación basada en el juicio (experiencia) de expertos. Técnica basada simplemente en la experiencia y conocimiento de las personas que han hecho un cierto número de estimaciones en el pasado.
- Modelos algorítmicos o paramétricos. El coste y esfuerzo se calcula mediante ecuaciones que tienen en cuenta distintas variables de un proyecto. La técnica de los puntos de función pertenece a este categoría.
- Otros modelos. Principalmente aquellos basados en técnicas de inteligencia artificial y minería de datos.



---

## Estimación mediante juicio de expertos 

Basada en el conocimiento y experiencia de proyectos similares.
Entre las técnias más conocidas de este tipo destacan el método Delphi  y la estimación por analogía. 

### Método Delphi

Se trata de una técnica en la que existe un coordinador que proporciona a cada experto una especificación y un formulario. El coordinador reúne a los expertos para intercambiar opiniones sobre la estimación y al final de la reunión, cada experto rellena su formulario de forma anónima. A continuación, el coordinador proporciona a los expertos un resumen de la estimación y se organizan nuevas reuniones para debatir las estimaciones de la ronda anterior hasta el punto donde ya no sean necesarias más revisiones. 

### Estimación de expertos por analogia

Consiste en realizar la estimación del proyecto actual comparando dichos proyectos con otros anteriores, de características y ámbitos similares. Se presupone que la organización mantiene una base de datos con proyectos realizados, o utiliza algún repositorio disponible, tal como el ISBSG "International Software Benchmarking Group, un repositorio de métricas de gestión de proyectos de diferentes sectores donde se puden encontrar proyectos similares al que queremos estimar en base a nuestro proyecto.


## ONSET  

**Dagnino, A.** (2013). "Estimating software-intensive projects in the absence of historical data." _Proceedings of the 35th International Conference on Software Engineering (ICSE 2013)_, pp. 941–950. IEEE.
[10.1109/ICSE.2013.6606643](https://doi.org/10.1109/ICSE.2013.6606643)

La técnica ONSET, por sus siglas (ONe Software Estimation Tool-kit) es una técnica realizada por Dagnino, A. que recopila 3 técnicas de estimación de costos y tiempo para casos en donde no se cuente con datos ni experiencia respaldada. 

1. **Planning Poker** (estimación relativa ágil)
    
2. **Modified Wideband Delphi** (convergencia de opiniones)
    
3. **Simulación Monte Carlo** (propagación de incertidumbre)

Pasos para la realización de la estimación:

1. Desglosar en tareas ≤ 1-2 días 
2. Para cada tarea: O, M, P → PERT 
3. Sumar totales → aplicar ×3 (inexperience) 
4. Sanity-check contra benchmark externo (tasas de mercado, SLOC × horas/SLOC, proyectos similares) 
5. Documentar supuestos y riesgos 
6. Registrar estimado vs. real en cada tarea 
7. Al terminar: calcular factor de error personal


La estimación PERT denotada con la formula:

- **O** (optimista): "todo sale perfecto"
- **M** (más probable): "lo más realista"
- **P** (pesimista): "algo sale mal"
$$
Tesperada​=(O+4M+P)/2
$$

Permite desglosar el tiempo estimados de las actividades con un previo WBS.

>  **Work Breakdown Structure (WBS)**, conocida en español como **Estructura de Desglose del Trabajo** (EDT), es una herramienta fundamental de la gestión de proyectos que consiste en la **descomposición jerárquica orientada a entregables** del trabajo a realizar. 


El cual mediante 3 variables podemos clasificar las actividades en base a su complejidad.

**Ejemplo Práctico:**  
Si una tarea tiene una duración optimista de 3 días, la más probable de 5 días y la pesimista de 9 días:

- **Duración esperada:** (3+4(5)+9)/6=5.66 días.
    
- **Desviación estándar:** (9−3)/6=1 día.
    

Este enfoque permite gestionar riesgos y estimaciones más realistas que el método determinista, especialmente cuando hay poca información histórica disponible.

Proyecto: App web de e-commerce (catálogo, carrito, pagos) 1. Esfuerzo estimado (WBS + PERT × 3): 480 horas 2. Tasa horaria (desarrollador full-stack, MX): $25 USD/hr → Costo de mano de obra: 480 × $25 = $12,000 3. Costos no laborales: - Hosting (Vercel/AWS): $200/mes × 3 meses = $600 - API de pagos (Stripe): 2.9% por transacción (recurr.) - Dominio + SSL: $50 - Herramientas (Figma, etc.): $200 → Total no laboral: ~$850 4. Contingencia (30%, primer proyecto): ($12,000 + $850) × 0.30 = $3,855 COSTO TOTAL ESTIMADO: ~$16,700 USD Rango (con incertidumbre): $12,000 – $22,000

## Puntos de función





