con información resumida de los libros de Ingeniería de Software: Un enfoque práctico de Roger R. Pressman e Ingeniería de Software de Ian Sommerville. Apoyado por la herramienta RAG Notebooklm,  https://notebook.google.com/notebook/e54ad0d3-6fb9-4e5e-b477-96915c1a5f81


2.1 Plan de calidad del software

El **plan de calidad del proyecto** se elabora durante la fase de planificación e identifica las metas, estándares, procedimientos y atributos de calidad más importantes para el sistema.

- **Estructura principal de un plan de calidad:**
    1. **Introducción del producto:** Descripción del sistema, ámbito de mercado y expectativas de calidad.
    2. **Planes del producto:** Fechas clave de entrega, asignación de responsabilidades y planes de distribución o servicio.
    3. **Descripciones de procesos:** Definición de los procesos de desarrollo y estándares aplicables a la arquitectura, diseño y código.
    4. **Metas de calidad:** Justificación de los atributos de calidad esenciales (ej. fiabilidad, mantenibilidad, usabilidad) y cómo se evaluarán.
    5. **Gestión de riesgos:** Riesgos principales que pueden degradar la calidad y acciones preventivas.
- **Criterios prácticos:** El plan debe ser lo más breve y conciso posible para garantizar que el equipo realmente lo lea y aplique. Además de la documentación formal, busca institucionalizar una "cultura de calidad" en todo el equipo de desarrollo.

---

2.2 La gestión de proyectos usando un marco de calidad

Integrar un marco de calidad en la dirección de proyectos permite estructurar el desarrollo de forma predecible y controlar las variaciones en costos, tiempos y defectos.

- **Niveles de aplicación:**
    - **Nivel organizacional:** Define el marco general de procesos, manuales de calidad y políticas globales de la empresa.
    - **Nivel de proyecto:** Adapta el marco general mediante el plan de calidad del proyecto y verifica que las entregas cumplan con los estándares.
- **Aseguramiento de Calidad (SQA) independiente:** El grupo de SQA realiza auditorías y revisiones periódicas sobre los procesos y productos del trabajo, reportando directamente a la alta dirección para evitar presiones sobre el calendario o presupuesto.
- **Equilibrio entre procesos y personas:** Los marcos formales garantizan consistencia en proyectos grandes, pero deben complementarse con la motivación, profesionalismo y juicio del equipo.

---

2.3 Estándares y Métricas de calidad en la ingeniería de software

Los estándares y las métricas proporcionan la base objetiva para evaluar si el software satisface las expectativas del cliente y los requisitos técnicos.

- **Estándares de software:**
    - **Estándares de producto:** Se aplican a los entregables directos (ej. guías de estilo de código, formatos de comentarios en encabezados, estructura de la especificación de requerimientos).
    - **Estándares de proceso:** Definen las actividades y pasos a seguir en el flujo de trabajo (ej. procedimientos de revisión de diseño, control de cambios, protocolos de prueba).
- **Métricas de calidad:**
    - **Métricas de proceso (o control):** Miden el desempeño de las actividades de desarrollo (ej. tiempo medio para corregir fallos, eficacia en la eliminación de defectos).
    - **Métricas de producto (o predicción):** Miden propiedades internas del sistema (ej. líneas de código, complejidad ciclomática, acoplamiento) para inferir atributos externos como la mantenibilidad o la propensión a errores.
    - **Enfoque GQM / OPM (Meta-Pregunta-Métrica):** Metodología que deriva métricas específicas a partir de los objetivos de negocio y preguntas cuantitativas del proyecto.

2.3.1 CMMI (Capability Maturity Model Integration)

Creado por el _Software Engineering Institute_ (SEI), es un marco de trabajo integrado para la mejora y evaluación de la capacidad de los procesos de software.

- **Áreas de proceso:** Organiza 22 áreas de proceso en cuatro categorías: Gestión de Procesos, Gestión de Proyectos, Ingeniería y Soporte.
- **Dos representaciones del modelo:**
    1. **Modelo en etapas (****Staged****):** Evalúa la madurez de la organización como un todo en **5 niveles**:
        - _Nivel 1 (Inicial):_ Proceso informal o caótico.
        - _Nivel 2 (Gestionado):_ Procesos básicos de gestión de proyectos y requerimientos.
        - _Nivel 3 (Definido):_ Procesos estandarizados e integrados a nivel organizacional.
        - _Nivel 4 (Gestionado cuantitativamente):_ Control estadístico y cuantitativo del proceso.
        - _Nivel 5 (Optimizado):_ Mejora continua mediante retroalimentación cuantitativa e innovación.
    2. **Modelo continuo (****Continuous****):** Permite evaluar la madurez de áreas de proceso individuales en una escala de 0 a 5, generando un **perfil de capacidad** flexible según las necesidades de la empresa.




2.3.2 MoProSoft

En el ámbito general de la industria, **MoProSoft** (Modelo de Procesos para la Industria de Software) es un estándar enfocado en las micro, pequeñas y medianas empresas de desarrollo de software (desarrollado en México), que simplifica las mejores prácticas de CMMI e ISO 9000 para adaptarlas a organizaciones pequeñas con recursos limitados.

Caracteristicas

- Es específico para el desarrollo y mantenimiento de software.
- Facilita el cumplimiento de los requisitos de otros modelos como ISO/IEC 29110, ISO 9001:2008, ISO/IEC 15504, CMMI-DEV e ISO/IEC 12007.
- Es sencillo de entender y adoptar.
- Es práctico en su aplicación.
- Comprende un documento de menos de 200 páginas que al compararlo con otros modelos y estándares, lo hace bastante práctico.
- Resulta acorde con la estructura de las organizaciones mexicanas con desarrollo o mantenimiento de software.
- Está orientado a mejorar los procesos, para contribuir a los objetivos de la organización, y no simplemente ser un marco de referencia o dictaminación.
- Tiene un bajo costo, tanto para su capacitación, adopción como para su evaluación.

A quien va dirigido

- El Modelo MoProSoft está dirigido a las empresas o áreas internas dedicadas al desarrollo y/o mantenimiento de software.
- Agrupa los procesos en tres categorías principales: Alta Dirección, Gerencia y Operación. Esta división de procesos se ajusta a la estructura funcional de una organización.
- Las organizaciones que no cuentan con procesos establecidos, pueden usar el modelo como la primera versión de sus procesos e ir ajustándolos de acuerdo a sus necesidades y experiencia adquirida.
- Las organizaciones, que ya tienen procesos establecidos, pueden usarlo como punto de referencia para identificar los elementos que les hace falta cubrir.

Servicios Adicionales sobre dicha norma

- Preverificaciónes (Diagnostico)
- Verificaciones Formales
- Verificaciones Correctivas
- Herramienta de Gestión KWE 2.0 (Base de Conocimiento)
- Venta de la Norma NMX-I-059-NYCE
- Venta de la Guía de Implantación de los Requisitos de la Norma NMX-I-059-NYCE (MoProSoft) a Nivel 1 y 2.

https://www.sige.org.mx/verificacion-moprosoft/

---

2.4 Impacto de la calidad en tiempo, costo y alcance del proyecto

La calidad no es un costo adicional, sino una inversión que afecta directamente el triángulo de gestión de proyectos (tiempo, costo y alcance):

- **Efecto multiplicador del costo por detección tardía:** Corregir un error durante las fases iniciales (requisitos o diseño) tiene un costo unitario, mientras que corregir ese mismo error en la fase de pruebas o tras la entrega al cliente cuesta entre **15 y 100 veces más**.
- **Impacto en tiempo y costo:** La aplicación de técnicas de prevención y verificación (como inspecciones) reduce el volumen de trabajo rehecho (_rework_), lo que disminuye tanto la duración total como el costo final del proyecto.
- **Impacto en el mantenimiento a largo plazo:** Invertir esfuerzo durante el desarrollo para producir código mantenible incrementa ligeramente el costo inicial, pero genera reducciones drásticas en los costos de evolución y mantenimiento durante el ciclo de vida del producto.
- **Compromiso del alcance:** Trabajar con presupuestos o calendarios poco realistas obliga a reducir el alcance, recortar pruebas o entregar software con menor fiabilidad y rendimiento.

---

2.5 Control del cambio

Dado que los cambios durante el desarrollo son inevitables, la **Gestión de la Configuración del Software (GCS)** establece procesos para controlar las modificaciones sin causar caos ni introducir defectos.

- **Líneas base (****Baselines****):** Colección de elementos de configuración (código, documentos) aprobados formalmente; una vez establecida una línea base, cualquier modificación requiere aprobación formal.
- **Comité de Control de Cambios (CCB / ACC):** Autoridad encargada de analizar las peticiones de cambio (_Change Requests_) desde el punto de vista estratégico, evaluando su impacto en costo, tiempo, arquitectura y riesgos.
- **Flujo formal del proceso de cambio****:**
    1. **Solicitud:** El cliente o desarrollador envía una Petición de Cambio (_CR_).
    2. **Verificación y análisis:** Se comprueba que la petición sea válida y el equipo técnico evalúa los módulos afectados y el esfuerzo necesario.
    3. **Evaluación costo-beneficio:** El CCB decide si aprueba, rechaza o pospone el cambio para una versión futura.
    4. **Implementación controlada:** Se extrae el objeto de la base de datos (_check-out_), se realiza la modificación, se ejecutan las pruebas de SQA y se reingresa (_check-in_).
    5. **Nueva línea base:** Se crea la nueva versión del producto y se notifica a los involucrados.