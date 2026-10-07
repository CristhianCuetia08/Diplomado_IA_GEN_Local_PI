# PLANTEAMIENTO Y ANÁLISIS INICIAL DE UN ASISTENTE DOCUMENTAL LOCAL PARA LA ORGANIZACIÓN Y CONSULTA DE NORMATIVA PÚBLICA EN UNA ENTIDAD TERRITORIAL

## PROYECTO INTEGRADOR

### Diplomado en Inteligencia Artificial Generativa Local, Agentes Autónomos y Sistemas Multimodales – IA 5.0 Lab

---

## PORTADA ACADÉMICA

**Nombre de la institución:** [Nombre de la institución]

**Programa académico:** [Programa académico]

**Diplomado:** Diplomado en Inteligencia Artificial Generativa Local, Agentes Autónomos y Sistemas Multimodales – IA 5.0 Lab

**Título del proyecto:**
**Planteamiento y análisis inicial de un asistente documental local para la organización y consulta de normativa pública en una entidad territorial**

**Autores:** [Nombres de los autores]

**Docente o asesor:** [Nombre del docente o asesor]

**Municipio:** [Municipio o departamento]

**Fecha:** [Fecha de entrega]

---

# 1. INTRODUCCIÓN

Las entidades territoriales gestionan diferentes tipos de documentos asociados con sus funciones administrativas, jurídicas y operativas. Dentro de este conjunto se encuentran normas, decretos, acuerdos, resoluciones, circulares, conceptos, manuales, procedimientos y comunicaciones oficiales. La consulta adecuada de esta información constituye una actividad relevante para apoyar la elaboración de documentos institucionales, la revisión de antecedentes y la atención de requerimientos internos o externos. Sin embargo, la utilidad de un repositorio documental no depende únicamente de conservar los archivos, sino también de contar con mecanismos que permitan localizar, relacionar y consultar información de manera controlada, contextualizada y verificable.

En contextos donde existen documentos producidos en diferentes momentos, formatos y dependencias, puede presentarse la necesidad de mejorar los mecanismos de organización y recuperación de información. Para una entidad territorial, esta necesidad debe analizarse considerando sus capacidades reales de infraestructura, conectividad, presupuesto, talento humano y gestión documental. En particular, antes de adoptar herramientas de inteligencia artificial resulta necesario conocer qué información será procesada, quién podrá acceder a ella, cuáles son sus niveles de sensibilidad, cómo se verificará su procedencia y qué responsabilidades conservarán las personas encargadas de utilizar y aprobar los resultados.

La inteligencia artificial generativa ofrece posibilidades para apoyar tareas de búsqueda, síntesis y elaboración preliminar de textos. En este contexto, los sistemas de generación aumentada por recuperación —Retrieval-Augmented Generation, RAG— permiten plantear un mecanismo en el cual las respuestas del modelo se apoyen en información previamente recuperada desde una base documental. Esta aproximación resulta pertinente para un asistente que requiera mostrar las fuentes utilizadas y reducir la generación de respuestas sin evidencia documental. No obstante, RAG no equivale al entrenamiento o ajuste fino del modelo y tampoco garantiza por sí mismo que las respuestas sean jurídicamente correctas o que las fuentes recuperadas sean las más actualizadas.

El enfoque **local-first** propuesto en este proyecto busca que los documentos y componentes de información institucional permanezcan, preferiblemente, dentro de infraestructura controlada por la entidad. Esta decisión puede contribuir a fortalecer el control técnico sobre los datos, disminuir la dependencia de servicios externos y facilitar determinados escenarios de operación con conectividad limitada. Sin embargo, la ejecución local de modelos no elimina las obligaciones relacionadas con protección de datos personales, seguridad de la información, gestión documental, propiedad intelectual, control de acceso o responsabilidad institucional. La Ley 1581 de 2012 establece disposiciones generales para la protección de datos personales y contempla principios y obligaciones que deben ser considerados cuando información personal sea objeto de tratamiento.

El presente documento corresponde exclusivamente al **Módulo 1: Fundamentos, soberanía tecnológica y gobernanza de IA** del Diplomado en Inteligencia Artificial Generativa Local, Agentes Autónomos y Sistemas Multimodales – IA 5.0 Lab. Por esta razón, su propósito no es demostrar una implementación terminada, sino caracterizar el problema, los actores, los datos, los riesgos, los requisitos y las alternativas arquitectónicas que deberán orientar las etapas posteriores. La propuesta se formula como un anteproyecto técnico-académico y deberá ser validada posteriormente con usuarios, responsables de información, personal jurídico, responsables tecnológicos y demás actores de la entidad territorial objeto de estudio.

---

# 2. CONTEXTO INSTITUCIONAL Y TERRITORIAL

El proyecto se plantea para **[entidad territorial objeto de estudio]**, ubicada en **[Municipio o departamento]**, entendida para efectos de esta formulación como una organización pública que produce, recibe, conserva y consulta documentación relacionada con sus funciones institucionales. En esta etapa no se dispone de información suficiente para afirmar características específicas de una entidad determinada, por lo que aspectos como su estructura organizacional, volumen documental, infraestructura tecnológica, políticas internas y responsables deberán ser confirmados mediante un diagnóstico institucional.

Las áreas potencialmente relacionadas con el caso de uso pueden comprender dependencias jurídicas, administrativas, secretarías productoras de documentos, áreas de archivo o gestión documental, tecnologías de la información y niveles directivos responsables de la aprobación de documentos. La participación concreta de cada dependencia deberá definirse a partir del levantamiento de procesos y entrevistas con los responsables institucionales.

Desde la perspectiva territorial, el proyecto considera pertinente un escenario correspondiente al Cauca o a otra región donde puedan coexistir diferentes niveles de capacidad tecnológica. Esta consideración no supone que todas las entidades de la región presenten las mismas condiciones. Por el contrario, constituye un supuesto de diseño que deberá ser contrastado con información real sobre conectividad, disponibilidad de servidores, características del hardware, conocimientos técnicos del personal y presupuesto disponible.

Una solución de estas características debe ser reproducible y proporcional a las capacidades de la organización. No resultaría adecuado plantear desde el inicio una infraestructura que requiera recursos computacionales que la entidad no pueda mantener. Por ello, la selección futura de modelos deberá considerar factores como tamaño del modelo, memoria requerida, latencia, calidad esperada, licencia, facilidad de operación y costo computacional.

El contexto institucional también hace necesario diferenciar entre **modelo, aplicación, agente, sistema RAG y flujo de trabajo**. El modelo de lenguaje constituye un componente de inferencia; la aplicación integra interfaces, reglas y servicios; el RAG proporciona recuperación de información para contextualizar las respuestas; y un agente, si posteriormente se incorpora, implicaría capacidades adicionales de planificación, uso de herramientas y ejecución controlada de acciones. En consecuencia, no se debe considerar que la simple incorporación de un modelo de lenguaje constituye por sí misma un sistema inteligente institucional.

En este proyecto se propone inicialmente un asistente documental de alcance controlado. El sistema deberá consultar fuentes autorizadas y apoyar la generación de borradores, pero las decisiones administrativas, jurídicas y de aprobación permanecerán bajo responsabilidad humana.

---

# 3. PLANTEAMIENTO DEL PROBLEMA

## 3.1 Situación problemática

La gestión de normativa pública requiere localizar información confiable, identificar documentos pertinentes y comprender su relación con otros documentos institucionales. Cuando la documentación se encuentra distribuida en diferentes carpetas, sistemas, formatos o dependencias, aumenta la necesidad de establecer mecanismos adecuados de clasificación, búsqueda y trazabilidad. Esta situación no debe interpretarse como una falla comprobada de **[entidad territorial objeto de estudio]**, dado que todavía no se cuenta con un diagnóstico institucional completo. Se plantea, por tanto, como una condición potencial que deberá ser evaluada mediante el levantamiento de información.

La heterogeneidad documental puede involucrar archivos PDF, documentos ofimáticos, documentos digitalizados mediante OCR y archivos con diferentes estructuras de metadatos. Además, la información puede estar asociada con fechas, entidades emisoras, tipos documentales, temas, estados y relaciones con otros documentos. En un escenario de consulta manual, la eficiencia de recuperación dependerá, entre otros factores, de la organización del repositorio y del conocimiento de los funcionarios que realizan la búsqueda.

Otro elemento relevante corresponde a la actualización y vigencia de la información. Una respuesta construida a partir de un documento desactualizado, modificado o que posteriormente haya sido sustituido puede generar una interpretación inadecuada. Por esta razón, el asistente propuesto no deberá limitarse a recuperar texto, sino que deberá conservar metadatos, versiones y evidencia de las fuentes utilizadas. La determinación de vigencia jurídica, sin embargo, deberá permanecer bajo responsabilidad de los funcionarios competentes.

La incorporación de inteligencia artificial generativa introduce riesgos adicionales. Un modelo puede generar información que no se encuentre respaldada por los documentos recuperados, combinar incorrectamente fragmentos de diferentes fuentes o producir una respuesta con apariencia de certeza cuando la evidencia disponible sea insuficiente. El uso de RAG puede contribuir a reducir este problema al proporcionar contexto documental, pero no elimina el riesgo de alucinación ni sustituye la evaluación humana.

También existe una dimensión relacionada con privacidad y seguridad. Algunos documentos públicos pueden contener datos personales, mientras que otros documentos institucionales pueden ser de uso interno o estar sometidos a restricciones. La Ley 1581 de 2012 establece, entre otros elementos, principios relacionados con finalidad, libertad, veracidad o calidad, transparencia y confidencialidad en el tratamiento de datos personales. Por ello, el proyecto deberá establecer controles de acceso y reglas de tratamiento antes de permitir que determinados documentos sean utilizados por el asistente.

El traslado de documentos a servicios externos puede generar dependencias técnicas y organizacionales adicionales. La utilización de una API externa, por ejemplo, puede implicar enviar contenido fuera de la infraestructura institucional. En consecuencia, deberá evaluarse previamente qué información puede salir de la organización, bajo qué autorización y con qué garantías. El enfoque local-first se plantea precisamente como una estrategia para conservar mayor control sobre la información, aunque no debe interpretarse como una garantía automática de cumplimiento normativo.

En este contexto aparece una oportunidad para formular una arquitectura de asistente documental que combine repositorio controlado, clasificación documental, recuperación semántica, generación asistida, citas verificables, control de acceso y revisión humana. La finalidad no consiste en automatizar la responsabilidad jurídica o administrativa, sino en proporcionar una herramienta de apoyo que permita mejorar el acceso al conocimiento documental y conservar evidencia de las fuentes utilizadas.

## 3.2 Pregunta del proyecto

**¿Cómo formular una arquitectura de asistente documental local que permita organizar y consultar normativa pública, generar borradores preliminares con citas verificables y conservar el control institucional sobre los documentos, incorporando trazabilidad, privacidad, supervisión humana, seguridad y viabilidad operativa para [entidad territorial objeto de estudio]?**

---

# 4. JUSTIFICACIÓN

## 4.1 Dimensión institucional

El proyecto resulta pertinente porque propone analizar una necesidad relacionada con la gestión y consulta de información institucional. La organización de documentos y la recuperación de evidencia pueden apoyar diferentes procesos administrativos y jurídicos, siempre que la herramienta se mantenga dentro de límites claramente definidos.

El valor institucional no se plantea como sustitución de las funciones de los servidores públicos, sino como apoyo para localizar información y preparar borradores que posteriormente sean revisados. Esta distinción resulta fundamental para evitar que una herramienta generativa sea utilizada como autoridad jurídica o administrativa.

## 4.2 Dimensión técnica

Desde la perspectiva de Ingeniería de Sistemas, el proyecto permite integrar gestión documental, procesamiento de lenguaje natural, recuperación de información, modelos de lenguaje, control de acceso, auditoría y gestión de riesgos.

La arquitectura local-first ofrece además un escenario para estudiar la ejecución de modelos de lenguaje bajo restricciones reales de hardware. La selección futura del modelo deberá realizarse con base en pruebas y no únicamente en su tamaño o popularidad.

## 4.3 Dimensión operativa

Un sistema que permita localizar documentos y mostrar evidencia recuperada puede contribuir potencialmente a disminuir tareas repetitivas de búsqueda. Sin embargo, cualquier beneficio operativo deberá ser medido posteriormente mediante una línea base y un conjunto de pruebas.

## 4.4 Dimensión académica

El proyecto permite aplicar conceptos del diplomado en un caso concreto de Ingeniería de Sistemas, pasando de la discusión conceptual sobre IA generativa a la formulación de una solución gobernable y evaluable.

## 4.5 Dimensión territorial

El enfoque es pertinente para analizar escenarios donde las capacidades tecnológicas pueden ser heterogéneas. Una arquitectura local-first puede plantearse de manera gradual y adaptarse al hardware disponible, evitando asumir desde el inicio que la organización posee infraestructura de alto desempeño.

## 4.6 Dimensión ética

El sistema debe incorporar desde su formulación límites de uso, mecanismos de supervisión y advertencias sobre las limitaciones de los modelos generativos. El principio central será que la generación automática constituye apoyo y no autoridad.

## 4.7 Privacidad y seguridad

La protección de datos debe considerarse desde la arquitectura y no como una actividad posterior. La Ley 1581 de 2012 contempla disposiciones aplicables al tratamiento de datos personales por entidades públicas y privadas. Por ello, el sistema deberá incorporar clasificación de información, mínimo privilegio, control de acceso, trazabilidad y procedimientos para incidentes.

## 4.8 Soberanía tecnológica

El enfoque local-first busca disminuir dependencias innecesarias de proveedores externos y mantener bajo control institucional los documentos y componentes críticos. Sin embargo, soberanía tecnológica no significa aislamiento absoluto. La entidad deberá valorar licencias, actualizaciones, dependencias de software, disponibilidad de soporte y capacidad interna de mantenimiento.

## 4.9 Sostenibilidad

La solución deberá ser proporcional a los recursos disponibles. El uso de modelos pequeños o medianos, cuando sean suficientes para la tarea, puede ser más sostenible desde el punto de vista computacional que adoptar modelos de gran tamaño sin justificación técnica. Esta hipótesis deberá validarse posteriormente mediante benchmarking.

---

# 5. OBJETIVO GENERAL

**Formular el planteamiento, alcance, requisitos iniciales, alternativa arquitectónica y esquema de gestión de riesgos para un asistente documental local orientado a la organización y consulta de normativa pública en una entidad territorial, incorporando mecanismos de trazabilidad, generación de borradores con citas verificables, control de acceso y supervisión humana.**

---

# 6. OBJETIVOS ESPECÍFICOS

1. **Caracterizar** el problema asociado con la organización, consulta y recuperación de documentación normativa en el contexto de [entidad territorial objeto de estudio].

2. **Identificar** los usuarios, actores, partes interesadas, procesos y responsabilidades relacionados con la gestión y consulta de los documentos que serían utilizados por el asistente.

3. **Clasificar** preliminarmente los tipos de documentos, metadatos y categorías de información involucradas, considerando niveles de sensibilidad, procedencia, acceso y tratamiento.

4. **Analizar** las alternativas de arquitectura local, híbrida y principalmente externa, considerando privacidad, control de datos, costos, conectividad, rendimiento, mantenimiento, escalabilidad y dependencia tecnológica.

5. **Definir** los requisitos funcionales y no funcionales iniciales de un asistente documental con recuperación aumentada por generación, citas verificables y supervisión humana.

6. **Identificar y priorizar** los principales riesgos tecnológicos, documentales, de seguridad, privacidad y gobernanza utilizando como referencia las funciones Govern, Map, Measure y Manage del NIST AI RMF. El NIST AI RMF organiza la gestión de riesgos de IA precisamente alrededor de estas cuatro funciones y plantea su aplicación como un proceso continuo.

7. **Establecer** criterios de éxito, supuestos, restricciones y condiciones preliminares de validación que orienten los módulos posteriores del proyecto.

---

# 7. USUARIOS, ACTORES Y PARTES INTERESADAS

| Actor o usuario                         | Rol en el proceso                                        | Necesidades                                          | Nivel de interacción | Riesgos o responsabilidades                                   |
| --------------------------------------- | -------------------------------------------------------- | ---------------------------------------------------- | -------------------- | ------------------------------------------------------------- |
| Funcionarios jurídicos                  | Consultan normativa y revisan borradores                 | Fuentes confiables, citas, contexto y trazabilidad   | Alto                 | Deben validar interpretaciones y documentos generados         |
| Funcionarios administrativos            | Consultan información y elaboran documentos              | Búsqueda sencilla y resultados comprensibles         | Medio/alto           | Pueden interpretar incorrectamente una respuesta sin revisión |
| Secretarías o dependencias productoras  | Generan y aportan documentos                             | Organización, clasificación y control de versiones   | Medio                | Deben garantizar procedencia y actualización                  |
| Directivos o responsables de aprobación | Revisan resultados institucionales                       | Evidencia, trazabilidad y control                    | Medio                | Conservan responsabilidad de aprobación                       |
| Archivo o gestión documental            | Administra documentación                                 | Metadatos, versiones, conservación y procedencia     | Alto                 | Debe definir reglas documentales                              |
| Tecnología de la información            | Administra infraestructura                               | Seguridad, mantenimiento, disponibilidad y monitoreo | Alto                 | Debe controlar infraestructura y accesos                      |
| Ciudadanía                              | Puede ser usuaria indirecta o directa cuando corresponda | Acceso a información pública pertinente              | Bajo/variable        | No debe acceder a información restringida                     |
| Administradores del sistema             | Gestionan usuarios y configuración                       | Gestión de permisos y auditoría                      | Alto                 | Deben aplicar mínimo privilegio                               |
| Responsables de protección de datos     | Supervisan tratamiento de información personal           | Clasificación, privacidad y controles                | Medio                | Deben validar tratamiento de datos personales                 |
| Órganos de control o auditoría          | Revisan cumplimiento y trazabilidad                      | Evidencia, registros y documentación                 | Bajo/periódico       | Pueden requerir evidencia de operaciones                      |

Los usuarios directos serían principalmente funcionarios autorizados que consulten documentos o utilicen la generación de borradores. Los usuarios indirectos corresponden a personas que reciban resultados producidos con apoyo del sistema. Los administradores tendrán capacidades técnicas superiores, pero deberán estar sujetos al principio de mínimo privilegio. Los responsables de aprobación conservarán la decisión final sobre los documentos institucionales.

---

# 8. DESCRIPCIÓN PRELIMINAR DE LA SOLUCIÓN

La solución se plantea como un **asistente documental local-first**, compuesto por diferentes capas técnicas y organizacionales.

### 8.1 Repositorio local o institucional

Constituirá el almacenamiento de documentos autorizados. Deberá conservar identificación, procedencia, fecha, versión y demás metadatos definidos por la entidad.

### 8.2 Clasificación documental

Los documentos deberán organizarse según categorías previamente establecidas, tales como tipo documental, fecha, entidad emisora, tema, estado y nivel de acceso.

### 8.3 Extracción de texto y metadatos

Los documentos serán procesados para extraer texto y metadatos. Cuando existan documentos escaneados, podrá ser necesario aplicar OCR. Esta etapa deberá incluir mecanismos para detectar errores de extracción.

### 8.4 Fragmentación o *chunking*

Los documentos podrán dividirse en fragmentos para facilitar la recuperación. La estrategia deberá conservar suficiente contexto para que cada fragmento pueda ser interpretado correctamente.

### 8.5 Embeddings

Los fragmentos podrán representarse mediante vectores para permitir búsqueda semántica. La selección del modelo de embeddings deberá considerar idioma, calidad, consumo de recursos y compatibilidad con la infraestructura.

### 8.6 Índice o base de conocimiento local

Los embeddings y metadatos podrán almacenarse en una solución local de búsqueda vectorial. La tecnología específica deberá seleccionarse durante los módulos posteriores.

### 8.7 Modelo de lenguaje

Se plantea utilizar un modelo local o autoalojado compatible con el hardware disponible. La elección deberá considerar memoria, latencia, calidad, licencia y costo computacional.

### 8.8 Mecanismo RAG

El mecanismo RAG deberá recuperar fragmentos relevantes antes de solicitar al modelo la generación de una respuesta. El sistema deberá identificar las fuentes utilizadas y permitir verificar el contenido recuperado.

### 8.9 Respuestas con citas

Las respuestas deberán incorporar referencias a los documentos utilizados. Cuando la evidencia recuperada sea insuficiente, el sistema deberá evitar presentar una respuesta como concluyente.

### 8.10 Generación de borradores

El sistema podrá generar borradores preliminares de oficios, informes, respuestas o documentos de trabajo. Estos productos no tendrán carácter oficial hasta que sean revisados y aprobados por los responsables correspondientes.

### 8.11 Revisión y aprobación humana

Los borradores deberán pasar por una etapa explícita de revisión. El usuario responsable deberá poder aceptar, modificar, rechazar o solicitar una nueva generación.

### 8.12 Registro de trazabilidad

Se deberá registrar, según las políticas institucionales, la consulta, usuario, fecha, documentos recuperados, versión del modelo, parámetros relevantes y resultado generado.

### 8.13 Control de acceso

Los usuarios deberán acceder únicamente a las fuentes que correspondan con sus funciones.

### 8.14 Copias de seguridad y versiones

El repositorio deberá disponer de mecanismos para recuperar información ante pérdida o corrupción y conservar versiones de documentos relevantes.

## Funciones fuera de la solución

La propuesta excluye expresamente:

* Decisiones jurídicas automáticas.
* Firma o aprobación automática de actos administrativos.
* Modificación autónoma del repositorio oficial.
* Acceso irrestricto a sistemas institucionales.
* Uso de documentos sensibles en servicios externos sin autorización.
* Sustitución del criterio profesional de funcionarios.
* Emisión de conceptos jurídicos definitivos.
* Determinación automática e infalible de vigencia jurídica.

---

# 9. ALCANCE

## 9.1 Alcance funcional

En una primera versión conceptual o prototipo se proyecta que el sistema pueda:

* Ingerir documentos autorizados.
* Registrar metadatos.
* Organizar documentos por tipo, fecha, entidad emisora, tema y estado.
* Controlar versiones.
* Realizar búsquedas por palabras clave.
* Realizar búsquedas semánticas.
* Recuperar fragmentos relevantes.
* Responder preguntas sobre el contenido disponible.
* Presentar citas y fuentes.
* Generar borradores preliminares.
* Mostrar evidencia documental.
* Registrar consultas y resultados.
* Aplicar controles de acceso según roles.
* Permitir revisión y aprobación humana.

## 9.2 Alcance técnico

La solución se orientará bajo una arquitectura local-first, con posibilidad de utilizar modelos pequeños o medianos compatibles con el hardware institucional.

Se contempla conceptualmente:

* Repositorio documental local.
* Motor de extracción de texto.
* Base de conocimiento local.
* Modelo de embeddings.
* Motor de recuperación.
* Modelo de lenguaje local o autoalojado.
* API local cuando sea pertinente.
* Interfaz web institucional.
* Registro de auditoría.
* Gestión de versiones.

La operación podrá diseñarse de manera que, después de preparar el entorno, las consultas no dependan permanentemente de una conexión externa.

## 9.3 Alcance organizacional

Se deberá determinar:

* Qué áreas participarán.
* Quién validará documentos.
* Quién administrará usuarios.
* Quién aprobará borradores.
* Quién administrará infraestructura.
* Quién supervisará protección de datos.
* Qué capacitación necesitarán los usuarios.
* Cómo se actualizará el repositorio.

## 9.4 Exclusiones

El proyecto no contempla:

* Reemplazar asesoría jurídica.
* Sustituir funcionarios.
* Garantizar automáticamente la vigencia jurídica de la normativa.
* Producir decisiones definitivas sin revisión humana.
* Entrenar un modelo fundacional desde cero.
* Migrar toda la infraestructura de la entidad.
* Conectar de manera irrestricta el asistente a sistemas institucionales.
* Presentar resultados generados como actos administrativos oficiales.

---

# 10. REQUISITOS DEL SISTEMA

## 10.1 Requisitos funcionales

| Código | Requisito                                      | Prioridad  | Criterio de aceptación preliminar                                                 |
| ------ | ---------------------------------------------- | ---------- | --------------------------------------------------------------------------------- |
| RF-01  | Permitir la carga de documentos autorizados    | Alta       | Un usuario autorizado puede incorporar un documento y registrar su procedencia    |
| RF-02  | Registrar metadatos documentales               | Alta       | Cada documento posee los metadatos definidos institucionalmente                   |
| RF-03  | Clasificar documentos                          | Alta       | Los documentos pueden asociarse con categorías predefinidas                       |
| RF-04  | Gestionar versiones                            | Alta       | El sistema conserva identificación de versiones                                   |
| RF-05  | Indexar documentos                             | Alta       | Los documentos autorizados pueden ser incluidos en el índice                      |
| RF-06  | Permitir búsqueda literal                      | Alta       | Una consulta devuelve coincidencias textuales pertinentes                         |
| RF-07  | Permitir búsqueda semántica                    | Alta       | Una consulta puede recuperar fragmentos relacionados por significado              |
| RF-08  | Recuperar fragmentos relevantes                | Alta       | El sistema presenta evidencia documental asociada a la consulta                   |
| RF-09  | Generar respuestas con citas                   | Alta       | Las respuestas muestran las fuentes recuperadas                                   |
| RF-10  | Generar borradores preliminares                | Alta       | El sistema produce un borrador claramente identificado como no oficial            |
| RF-11  | Mostrar fuentes utilizadas                     | Alta       | El usuario puede identificar los documentos empleados                             |
| RF-12  | Registrar trazabilidad                         | Alta       | La consulta y sus elementos relevantes quedan registrados según política          |
| RF-13  | Gestionar usuarios y roles                     | Alta       | El administrador puede asignar permisos diferenciados                             |
| RF-14  | Permitir revisión humana                       | Alta       | El borrador puede ser revisado antes de cualquier uso institucional               |
| RF-15  | Registrar respuestas no sustentadas o errores  | Media/alta | El usuario puede reportar una respuesta incorrecta o insuficientemente sustentada |
| RF-16  | Permitir exportación de resultados autorizados | Media      | El usuario puede exportar resultados según permisos                               |

## 10.2 Requisitos no funcionales

| Código | Categoría         | Requisito                                                                                                                     |
| ------ | ----------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| RNF-01 | Seguridad         | El sistema deberá aplicar control de acceso basado en roles                                                                   |
| RNF-02 | Seguridad         | Los usuarios deberán operar bajo el principio de mínimo privilegio                                                            |
| RNF-03 | Privacidad        | La información personal deberá tratarse conforme a las políticas y obligaciones aplicables                                    |
| RNF-04 | Privacidad        | No se deberán enviar documentos sensibles a servicios externos sin autorización                                               |
| RNF-05 | Seguridad         | Los mecanismos de cifrado deberán utilizarse cuando sean técnicamente viables y estén definidos por la política institucional |
| RNF-06 | Trazabilidad      | Las fuentes utilizadas en una respuesta deberán poder identificarse                                                           |
| RNF-07 | Trazabilidad      | Deberá registrarse la versión documental utilizada cuando sea técnicamente posible                                            |
| RNF-08 | Trazabilidad      | Deberá poder identificarse la versión del modelo utilizada durante las pruebas                                                |
| RNF-09 | Rendimiento       | El tiempo de respuesta deberá establecerse mediante una línea base y benchmarking                                             |
| RNF-10 | Disponibilidad    | El sistema deberá contar con mecanismos de recuperación ante fallos                                                           |
| RNF-11 | Usabilidad        | La interfaz deberá permitir realizar consultas sin requerir conocimientos avanzados de IA                                     |
| RNF-12 | Mantenibilidad    | Los componentes deberán estar documentados para facilitar mantenimiento                                                       |
| RNF-13 | Reproducibilidad  | Deberán registrarse versiones de modelos, dependencias y configuraciones relevantes                                           |
| RNF-14 | Gobernanza        | Los borradores deberán requerir supervisión humana                                                                            |
| RNF-15 | Seguridad         | No deberán almacenarse secretos en código fuente ni prompts                                                                   |
| RNF-16 | Interoperabilidad | La solución deberá utilizar formatos y mecanismos de integración documentados                                                 |
| RNF-17 | Escalabilidad     | La arquitectura deberá permitir ampliar progresivamente el repositorio                                                        |
| RNF-18 | Sostenibilidad    | La selección de modelos deberá considerar consumo computacional y capacidad institucional                                     |
| RNF-19 | Accesibilidad     | La interfaz deberá considerar principios básicos de accesibilidad                                                             |
| RNF-20 | Auditoría         | Deberán conservarse registros suficientes para analizar incidentes y consultas relevantes                                     |
| RNF-21 | Actualización     | Deberá existir un procedimiento para incorporar nuevas versiones documentales                                                 |
| RNF-22 | Gobernanza        | Las licencias de modelos, bibliotecas y componentes deberán ser verificadas antes de su utilización                           |

Las métricas definitivas de rendimiento, capacidad, disponibilidad y calidad deberán establecerse mediante una línea base construida durante los módulos posteriores. En consecuencia, no se presentan valores de latencia, precisión o volumen como resultados actuales.

---

# 11. DATOS Y FLUJO DE INFORMACIÓN

## 11.1 Categorías de información

Los datos potencialmente involucrados comprenden:

* Normas.
* Decretos.
* Acuerdos.
* Resoluciones.
* Circulares.
* Conceptos.
* Manuales.
* Procedimientos.
* Comunicaciones oficiales.
* Metadatos documentales.
* Registros de consulta.
* Borradores generados.

La clasificación inicial propuesta es conceptual y deberá ser validada por la entidad.

| Tipo de dato             | Fuente                              | Sensibilidad                   | Tratamiento permitido                                 | Riesgo principal                    |
| ------------------------ | ----------------------------------- | ------------------------------ | ----------------------------------------------------- | ----------------------------------- |
| Normativa pública        | Fuentes institucionales autorizadas | Público                        | Consulta, indexación y recuperación                   | Utilizar una versión incorrecta     |
| Decretos                 | Repositorio autorizado              | Público o según clasificación  | Indexación y consulta controlada                      | Desactualización                    |
| Acuerdos                 | Repositorio institucional           | Público o según clasificación  | Consulta y recuperación                               | Confusión de versiones              |
| Resoluciones             | Dependencia productora              | Variable                       | Según autorización                                    | Acceso indebido                     |
| Circulares               | Dependencia productora              | Variable                       | Según autorización                                    | Uso de información interna          |
| Conceptos                | Área responsable                    | Interno/restringido según caso | Acceso según rol                                      | Interpretación fuera de contexto    |
| Manuales                 | Área responsable                    | Interno                        | Consulta autorizada                                   | Uso de versiones antiguas           |
| Procedimientos           | Área responsable                    | Interno                        | Consulta según rol                                    | Información desactualizada          |
| Comunicaciones oficiales | Dependencias                        | Variable                       | Según autorización                                    | Exposición de información           |
| Metadatos                | Sistema documental                  | Variable                       | Gestión y búsqueda                                    | Alteración o pérdida                |
| Registros de consulta    | Sistema                             | Interno/restringido            | Auditoría                                             | Exposición de actividad de usuarios |
| Borradores               | Asistente y usuario                 | Interno                        | Revisión controlada                                   | Uso como documento oficial          |
| Datos personales         | Documentos autorizados              | Personal                       | Solo cuando exista base y autorización aplicable      | Exposición o tratamiento indebido   |
| Datos sensibles          | Documentos específicos, si aparecen | Sensible                       | Tratamiento restringido y conforme al marco aplicable | Daño a titulares y cumplimiento     |

La Ley 1581 de 2012 define el dato personal como información vinculada o asociable a una persona natural determinada o determinable y contempla categorías especiales como los datos sensibles. Por esta razón, la clasificación deberá efectuarse antes de permitir que los documentos sean procesados por componentes de IA.

## 11.2 Flujo preliminar

El flujo de información propuesto es:

**1. Recepción del documento → 2. Validación de procedencia → 3. Clasificación → 4. Extracción → 5. Almacenamiento → 6. Indexación → 7. Consulta → 8. Recuperación de evidencia → 9. Generación del borrador → 10. Revisión humana → 11. Aprobación o rechazo → 12. Registro y conservación.**

### Recepción

El documento ingresa desde una fuente autorizada.

### Validación de procedencia

Se verifica quién proporciona el documento, su identificación y, cuando sea posible, su versión.

### Clasificación

Se determina tipo documental, nivel de acceso, fecha y demás metadatos.

### Extracción

Se convierte el contenido a una representación procesable. Si se requiere OCR, deberán contemplarse mecanismos de control de calidad.

### Almacenamiento

El documento original deberá conservarse sin alteraciones no autorizadas.

### Indexación

Se generan representaciones utilizadas para la búsqueda.

### Consulta

El usuario realiza una pregunta o búsqueda.

### Recuperación de evidencia

El sistema recupera fragmentos relevantes.

### Generación

El modelo utiliza la evidencia recuperada para producir una respuesta o borrador.

### Revisión

El funcionario verifica la respuesta y las fuentes.

### Aprobación o rechazo

El resultado puede utilizarse, modificarse o descartarse.

### Registro

Se conserva evidencia suficiente de la operación conforme a las políticas institucionales.

---

# 12. ALTERNATIVAS DE ARQUITECTURA

| Criterio                            | Local                                | Híbrida                          | Remota o externa                          |
| ----------------------------------- | ------------------------------------ | -------------------------------- | ----------------------------------------- |
| Privacidad                          | Alta capacidad de control            | Depende de qué información salga | Requiere controles y acuerdos adicionales |
| Control de datos                    | Alto                                 | Medio/alto                       | Menor control directo                     |
| Costos iniciales                    | Puede requerir inversión en hardware | Variables                        | Menor infraestructura local inicial       |
| Dependencia de Internet             | Baja después de preparación          | Media                            | Alta                                      |
| Latencia                            | Potencialmente estable en red local  | Variable                         | Dependiente de conexión                   |
| Mantenimiento                       | A cargo de la entidad                | Compartido                       | Mayor dependencia del proveedor           |
| Escalabilidad                       | Limitada por hardware                | Alta flexibilidad                | Generalmente alta                         |
| Calidad potencial                   | Depende del modelo/hardware          | Puede combinar modelos           | Puede acceder a modelos de alta capacidad |
| Trazabilidad                        | Alto control                         | Control condicionado             | Depende del proveedor                     |
| Dependencia tecnológica             | Menor dependencia externa            | Media                            | Alta                                      |
| Facilidad inicial                   | Requiere conocimientos técnicos      | Complejidad media/alta           | Puede ser sencilla inicialmente           |
| Operación con conectividad limitada | Favorable                            | Parcial                          | Desfavorable                              |
| Soberanía tecnológica               | Alta                                 | Media/alta                       | Menor                                     |
| Pertinencia preliminar              | Alta                                 | Alta                             | Condicionada                              |

## 12.1 Arquitectura local

Una arquitectura completamente local concentra almacenamiento, procesamiento, recuperación y generación dentro de infraestructura institucional. Su principal ventaja es el control sobre los datos y la posibilidad de operar sin enviar documentos a proveedores externos. Sus principales limitaciones potenciales son el costo del hardware, la capacidad computacional y la responsabilidad de mantenimiento.

## 12.2 Arquitectura híbrida

Una arquitectura híbrida podría mantener el repositorio documental y el índice local, mientras algunos componentes no sensibles se ejecutan mediante servicios externos. Este escenario puede aumentar la flexibilidad, pero exige reglas claras sobre qué información puede abandonar la infraestructura institucional.

## 12.3 Arquitectura remota

Una arquitectura principalmente externa puede facilitar el acceso a modelos de gran capacidad y disminuir las necesidades de infraestructura local. Sin embargo, introduce mayor dependencia de conectividad y proveedores y requiere analizar cuidadosamente las condiciones de tratamiento de información.

## 12.4 Recomendación preliminar

Se recomienda como alternativa inicial una **arquitectura local-first, con posibilidad de evolución hacia una arquitectura híbrida controlada**.

Esta recomendación se fundamenta en:

1. La necesidad de conservar el control institucional sobre los documentos.
2. La posibilidad de trabajar con conectividad limitada.
3. La necesidad de controlar las fuentes utilizadas por el asistente.
4. La importancia de mantener trazabilidad.
5. La posibilidad de seleccionar modelos proporcionales al hardware disponible.
6. La reducción de la necesidad de enviar documentación institucional a servicios externos.

No obstante, esta decisión es **preliminar**. La arquitectura definitiva deberá establecerse después de diagnosticar:

* Hardware disponible.
* Memoria RAM y GPU, si existe.
* Volumen documental.
* Número de usuarios.
* Frecuencia de consultas.
* Requisitos de disponibilidad.
* Políticas de seguridad.
* Clasificación de la información.
* Presupuesto.
* Capacidades técnicas del personal.

---

# 13. MATRIZ DE RIESGOS BASADA EN NIST AI RMF

El NIST AI RMF 1.0 establece cuatro funciones principales: **Govern, Map, Measure y Manage**. Govern funciona de manera transversal, mientras Map permite comprender el contexto y los riesgos, Measure permite evaluarlos y Manage orienta su priorización y tratamiento. El marco es voluntario y debe adaptarse al contexto específico de la organización; no constituye una lista única de pasos obligatorios.

### Escalas utilizadas

**Probabilidad:** Baja, Media, Alta.
**Impacto:** Bajo, Medio, Alto, Crítico.
**Nivel de riesgo:** Bajo, Medio, Alto, Crítico.

| ID   | Función NIST | Riesgo                                 | Causa                                       | Consecuencia                                             | Probabilidad | Impacto | Nivel   | Control preventivo                | Control detectivo       | Acción de mitigación                  | Responsable          | Evidencia                 |
| ---- | ------------ | -------------------------------------- | ------------------------------------------- | -------------------------------------------------------- | ------------ | ------- | ------- | --------------------------------- | ----------------------- | ------------------------------------- | -------------------- | ------------------------- |
| R-01 | Map          | Uso de documentos desactualizados      | Repositorio sin actualización               | Respuestas basadas en información antigua                | Alta         | Alto    | Alto    | Procedimiento de actualización    | Verificación de versión | Bloquear o marcar documentos antiguos | Gestión documental   | Registro de versión       |
| R-02 | Govern       | Uso de normativa modificada o derogada | Falta de control de estado                  | Interpretaciones incorrectas                             | Media        | Crítico | Alto    | Política de validación            | Revisión periódica      | Marcar estado documental              | Área jurídica        | Acta de validación        |
| R-03 | Measure      | Respuestas sin citas verificables      | Generación sin evidencia                    | Dificultad para comprobar respuesta                      | Media        | Alto    | Alto    | Citas obligatorias                | Prueba de evidencia     | Rechazar respuestas sin fuentes       | TI/área usuaria      | Registro de prueba        |
| R-04 | Measure      | Alucinaciones del modelo               | Limitaciones del LLM                        | Información inexistente presentada como cierta           | Alta         | Crítico | Crítico | RAG y restricciones               | Conjunto de evaluación  | Respuesta de abstención               | TI/área jurídica     | Resultados de evaluación  |
| R-05 | Measure      | Recuperación irrelevante               | Embeddings o chunking inadecuados           | Contexto incorrecto                                      | Media        | Alto    | Alto    | Diseño de recuperación            | Pruebas de recuperación | Ajustar índice y fragmentación        | TI                   | Benchmark                 |
| R-06 | Measure      | Errores de OCR                         | Documentos escaneados                       | Texto incorrecto                                         | Alta         | Alto    | Alto    | Control de calidad OCR            | Muestreo de documentos  | Corrección o exclusión                | Gestión documental   | Registro OCR              |
| R-07 | Map          | Inconsistencias entre documentos       | Fuentes contradictorias                     | Respuesta ambigua                                        | Media        | Alto    | Alto    | Metadatos y versiones             | Detección de conflictos | Mostrar documentos en conflicto       | Área jurídica        | Reporte de conflicto      |
| R-08 | Govern       | Exposición de datos personales         | Clasificación insuficiente                  | Tratamiento indebido                                     | Media        | Crítico | Alto    | Clasificación y permisos          | Auditoría de acceso     | Restringir documentos                 | Responsable de datos | Matriz de permisos        |
| R-09 | Govern       | Acceso no autorizado                   | Roles excesivos                             | Exposición o modificación de información                 | Media        | Crítico | Alto    | Mínimo privilegio                 | Logs de acceso          | Revocar permisos                      | TI                   | Registro de accesos       |
| R-10 | Measure      | Prompt injection en documentos         | Contenido malicioso dentro de una fuente    | Alteración del comportamiento del asistente              | Media        | Alto    | Alto    | Aislamiento de instrucciones      | Pruebas de seguridad    | Filtrado y separación de contenido    | TI                   | Informe de pruebas        |
| R-11 | Manage       | Fuga de información mediante consultas | Consultas maliciosas o permisos incorrectos | Exposición de información interna                        | Media        | Crítico | Alto    | Control de acceso                 | Auditoría de consultas  | Bloqueo y revisión                    | TI                   | Logs                      |
| R-12 | Govern       | Borradores jurídicamente incorrectos   | Uso indebido del modelo                     | Documento institucional incorrecto                       | Media        | Crítico | Crítico | Revisión humana obligatoria       | Revisión experta        | Rechazo o corrección                  | Área jurídica        | Registro de aprobación    |
| R-13 | Govern       | Licencia incompatible                  | Uso sin revisión de licencia                | Restricciones legales o técnicas                         | Media        | Alto    | Alto    | Inventario de licencias           | Auditoría               | Sustitución del componente            | TI                   | Inventario                |
| R-14 | Manage       | Dependencia de un modelo/proveedor     | Arquitectura cerrada                        | Dificultad de migración                                  | Media        | Medio   | Medio   | Arquitectura modular              | Revisión tecnológica    | Mantener alternativas                 | TI                   | Documento de arquitectura |
| R-15 | Manage       | Pérdida o corrupción del repositorio   | Fallo de hardware o software                | Pérdida de conocimiento documental                       | Media        | Crítico | Alto    | Copias de seguridad               | Pruebas de restauración | Recuperación ante fallos              | TI                   | Evidencia de backup       |
| R-16 | Govern       | Ausencia de trazabilidad               | Falta de registros                          | Imposibilidad de reconstruir consultas                   | Media        | Alto    | Alto    | Política de auditoría             | Revisión de logs        | Implementar registro                  | TI                   | Logs                      |
| R-17 | Govern       | Permisos excesivos del asistente       | Diseño sin mínimo privilegio                | Acciones o accesos innecesarios                          | Media        | Crítico | Alto    | Arquitectura de mínimo privilegio | Auditoría técnica       | Reducir permisos                      | TI                   | Matriz de permisos        |
| R-18 | Govern       | Registro inadecuado de consultas       | Diseño deficiente de auditoría              | Falta de evidencia o exposición                          | Media        | Alto    | Alto    | Política de registros             | Auditoría               | Ajustar retención y acceso            | TI                   | Política de logs          |
| R-19 | Measure      | Priorización incorrecta de fuentes     | Ranking inadecuado                          | Respuesta basada en fuente secundaria o menos pertinente | Media        | Alto    | Alto    | Jerarquización documental         | Evaluación de ranking   | Ajustar recuperación                  | TI/área jurídica     | Dataset de prueba         |
| R-20 | Manage       | Fallas de disponibilidad               | Hardware insuficiente                       | Interrupción del servicio                                | Media        | Medio   | Medio   | Dimensionamiento                  | Monitoreo               | Optimización o escalamiento           | TI                   | Reporte de rendimiento    |

## 13.1 Análisis interpretativo de los riesgos

Los riesgos prioritarios corresponden inicialmente a aquellos que pueden afectar la confiabilidad de las respuestas y producir consecuencias institucionales relevantes. En esta categoría se encuentran las alucinaciones, el uso de documentación desactualizada, la generación de borradores jurídicamente incorrectos y la ausencia de citas verificables. Estos riesgos están directamente relacionados con el propósito del sistema, porque un asistente documental solo resulta útil si el usuario puede conocer qué evidencia sustentó una respuesta.

El riesgo de utilizar documentación desactualizada merece especial atención. Un sistema RAG puede recuperar correctamente un fragmento desde el punto de vista técnico y, aun así, producir una respuesta problemática si el documento no representa la versión que corresponde al contexto de consulta. Por esta razón, la gestión de versiones y estados documentales debe considerarse una capacidad fundamental y no un componente secundario.

Los riesgos de seguridad y privacidad también tienen prioridad alta. El acceso a un repositorio local no debe interpretarse como acceso permitido para todos los usuarios. El principio de mínimo privilegio deberá aplicarse tanto a las personas como a los componentes técnicos. Asimismo, si aparecen datos personales o sensibles, deberán establecerse controles específicos de tratamiento. La Ley 1581 de 2012 contempla principios de protección y deberes relacionados con el tratamiento de datos personales, incluyendo la confidencialidad.

El riesgo de *prompt injection* requiere una consideración particular porque los documentos utilizados como fuente pueden contener instrucciones textuales que no deben convertirse en instrucciones para el modelo. La arquitectura deberá diferenciar entre contenido documental y comandos del sistema. Esta condición deberá probarse específicamente durante los módulos posteriores mediante escenarios controlados de seguridad.

Finalmente, los riesgos de disponibilidad, dependencia tecnológica, licenciamiento y capacidad computacional son importantes para la sostenibilidad del proyecto. Una arquitectura local puede aumentar el control sobre la información, pero también transfiere a la organización responsabilidades de mantenimiento, actualización, respaldo y operación. El NIST AI RMF plantea que la gestión de riesgos debe ser continua y que las respuestas a los riesgos deben priorizarse según su impacto y contexto.

La matriz presentada es **preliminar**. Deberá ser validada con [entidad territorial objeto de estudio], los responsables de información, el área jurídica, tecnología, gestión documental, responsables de protección de datos y usuarios finales.

---

# 14. CRITERIOS DE ÉXITO

| Dimensión                 | Criterio de éxito                                     | Indicador                             | Método de verificación           | Meta preliminar                                                  | Responsable                              |
| ------------------------- | ----------------------------------------------------- | ------------------------------------- | -------------------------------- | ---------------------------------------------------------------- | ---------------------------------------- |
| Pertinencia institucional | La solución responde a necesidades reales             | Nivel de correspondencia con procesos | Entrevistas y validación         | Validar con usuarios                                             | [Responsable institucional, por definir] |
| Recuperación documental   | Recupera evidencia pertinente                         | Métrica de recuperación               | Dataset de evaluación            | Definir después de línea base                                    | TI                                       |
| Exactitud de citas        | Las fuentes corresponden a las respuestas             | Porcentaje de citas correctas         | Evaluación manual                | Definir conjunto de prueba                                       | Área jurídica                            |
| Trazabilidad              | Se puede reconstruir una consulta                     | Registro disponible                   | Auditoría                        | 100 % de pruebas registradas                                     | TI                                       |
| Privacidad                | No se exponen datos sin autorización                  | Incidentes de exposición              | Pruebas y auditoría              | 0 documentos sensibles enviados externamente sin autorización    | Responsable de datos                     |
| Seguridad                 | Los controles de acceso funcionan                     | Pruebas exitosas de permisos          | Pruebas de seguridad             | 100 % de escenarios definidos                                    | TI                                       |
| Usabilidad                | Los usuarios comprenden el flujo                      | Evaluación de usuarios                | Prueba de uso                    | Definir mediante piloto                                          | Usuarios                                 |
| Rendimiento               | El sistema responde dentro de condiciones aceptables  | Tiempo de respuesta                   | Benchmarking                     | Definir mediante línea base                                      | TI                                       |
| Disponibilidad local      | El servicio puede operar localmente                   | Porcentaje de disponibilidad          | Monitoreo                        | Definir según necesidad                                          | TI                                       |
| Reproducibilidad          | Las pruebas pueden repetirse                          | Registro de versiones                 | Auditoría técnica                | Modelo y dependencias registrados en cada prueba                 | TI                                       |
| Control humano            | Todos los borradores son revisados                    | Porcentaje revisado                   | Auditoría                        | 100 %                                                            | Área responsable                         |
| Sostenibilidad            | La solución puede mantenerse con recursos disponibles | Recursos requeridos                   | Evaluación técnica               | Validar con hardware institucional                               | TI                                       |
| Aceptación                | Usuarios consideran útil la solución                  | Evaluación cualitativa/cuantitativa   | Encuesta piloto                  | Definir línea base                                               | Responsable del proyecto                 |
| Calidad de borradores     | Los borradores son útiles como documentos de trabajo  | Evaluación experta                    | Revisión jurídica/administrativa | Definir criterios                                                | Área usuaria                             |
| Evidencia suficiente      | No se presentan respuestas sin sustento               | Respuestas con fuentes                | Dataset de prueba                | 100 % de respuestas evaluadas deben mostrar fuentes o abstenerse | TI/área jurídica                         |

## 14.1 Criterios de éxito del proyecto

Durante el Módulo 1, el éxito se evaluará principalmente mediante la existencia de una formulación coherente, verificable y validable. Esto incluye identificación de actores, datos, riesgos, requisitos y arquitectura preliminar.

## 14.2 Indicadores de operación futura

Los indicadores de recuperación, precisión, latencia, disponibilidad y calidad deberán medirse posteriormente. No se presentan como resultados actuales.

## 14.3 Condiciones de aprobación institucional

La futura implementación deberá estar condicionada a la aprobación de los responsables correspondientes, particularmente en relación con documentos, accesos, protección de datos, seguridad y utilización de borradores.

## 14.4 Criterios de no aceptación

La solución deberá considerarse no aceptable para una determinada función cuando:

* No pueda identificar las fuentes utilizadas.
* Produzca respuestas sin evidencia en escenarios donde la evidencia sea obligatoria.
* Permita acceso a documentos sin autorización.
* Permita utilizar borradores como documentos oficiales sin revisión.
* Presente riesgos de privacidad no controlados.
* No permita identificar la versión de la documentación utilizada.
* No pueda operar de forma reproducible durante las pruebas definidas.

---

# 15. SUPUESTOS, RESTRICCIONES Y DEPENDENCIAS

## 15.1 Supuestos

Para la formulación inicial se consideran los siguientes supuestos:

1. La entidad dispone o podrá identificar documentos autorizados para el proyecto.
2. Existe o podrá designarse un responsable institucional para validar las fuentes.
3. Los usuarios participarán en la definición de requisitos.
4. Podrá disponerse de un entorno local de prueba.
5. Los documentos poseen algún nivel de identificación y procedencia.
6. El área jurídica o responsable equivalente podrá participar en la evaluación de resultados.
7. Tecnología podrá proporcionar información sobre infraestructura disponible.
8. La organización podrá establecer reglas de acceso a la información.

Estos supuestos no constituyen hechos confirmados y deberán validarse.

## 15.2 Restricciones

Entre las restricciones potenciales se encuentran:

* Hardware limitado.
* Presupuesto reducido.
* Conectividad intermitente.
* Diversidad de formatos documentales.
* Falta o inconsistencia de metadatos.
* Documentos digitalizados con OCR deficiente.
* Restricciones de licenciamiento.
* Tiempo limitado para el desarrollo.
* Disponibilidad limitada del personal institucional.
* Necesidad de mantener sistemas existentes.
* Diferentes niveles de conocimiento tecnológico entre usuarios.

## 15.3 Dependencias

La evolución del proyecto dependerá de:

* Disponibilidad de documentos.
* Participación del área jurídica.
* Participación del área de tecnologías.
* Participación de gestión documental.
* Política institucional de seguridad.
* Infraestructura local.
* Disponibilidad de hardware.
* Validación de licencias.
* Definición de roles.
* Procedimientos institucionales de actualización documental.
* Autorización para realizar pruebas con información institucional.

---

# 16. DELIMITACIÓN DEL TRABAJO CORRESPONDIENTE AL MÓDULO 1

El Módulo 1 se limita a la formulación y análisis inicial de la solución. En esta etapa se entregan:

* Ficha conceptual del caso de uso.
* Caracterización preliminar del problema.
* Mapa de actores.
* Identificación inicial de usuarios.
* Clasificación preliminar de datos.
* Mapa preliminar del flujo de información.
* Comparación de arquitecturas local, híbrida y remota.
* Requisitos funcionales.
* Requisitos no funcionales.
* Matriz de riesgos basada en NIST AI RMF.
* Criterios de éxito.
* Supuestos.
* Restricciones.
* Dependencias.
* Decisión preliminar de arquitectura.
* Recomendaciones para las etapas posteriores.

La función de gobernanza se considera transversal a todo el planteamiento. El NIST AI RMF señala que Govern debe informar e integrarse con las demás funciones de gestión de riesgos, mientras que Map, Measure y Manage permiten contextualizar, evaluar y tratar los riesgos identificados.

## 16.1 Actividades reservadas para módulos posteriores

Quedan fuera del alcance actual:

* Despliegue definitivo de modelos locales.
* Benchmarking completo de hardware.
* Construcción del sistema RAG.
* Desarrollo de agentes autónomos.
* Implementación de APIs.
* Desarrollo de interfaz definitiva.
* Pruebas exhaustivas de seguridad.
* Evaluación experimental.
* Integración con sistemas institucionales.
* Demostración final.
* Medición definitiva de precisión.
* Evaluación definitiva de rendimiento.

Esta delimitación evita presentar como resultados actuales actividades que todavía corresponden a fases posteriores del proyecto.

---

# 17. CONCLUSIONES

**Primera.** El análisis inicial permite establecer que un asistente documental para normativa pública debe plantearse como un sistema sociotécnico y no únicamente como un modelo de lenguaje. Su utilidad depende de la calidad de los documentos, la clasificación, los metadatos, los mecanismos de recuperación, los controles de acceso, la infraestructura y, especialmente, de la participación de los usuarios responsables de validar los resultados.

**Segunda.** El enfoque local-first resulta preliminarmente pertinente para el caso planteado porque permite mantener un mayor control técnico sobre documentos, modelos, registros y mecanismos de recuperación. Sin embargo, la operación local no elimina las responsabilidades relacionadas con privacidad, seguridad, gestión documental, licenciamiento ni tratamiento de datos personales. La Ley 1581 de 2012 constituye un referente relevante para el análisis de los datos personales que eventualmente aparezcan en los documentos procesados.

**Tercera.** La incorporación de RAG puede proporcionar una estructura para recuperar evidencia documental antes de generar respuestas y facilitar la presentación de citas. No obstante, RAG no garantiza automáticamente exactitud, vigencia jurídica o ausencia de alucinaciones. Por esta razón, el sistema deberá incorporar mecanismos de abstención, evidencia, trazabilidad, evaluación y revisión humana.

**Cuarta.** Los riesgos prioritarios se relacionan con el uso de documentos desactualizados, respuestas sin evidencia, alucinaciones, generación de borradores incorrectos, exposición de información, accesos indebidos y pérdida de trazabilidad. La aplicación del NIST AI RMF permite organizar estos riesgos mediante Govern, Map, Measure y Manage, proporcionando una estructura para continuar el análisis durante el ciclo de vida del proyecto.

**Quinta.** La solución propuesta no debe reemplazar el criterio jurídico, administrativo o profesional de los funcionarios. Los documentos generados por el asistente deberán considerarse borradores de trabajo hasta que sean revisados y aprobados por los responsables correspondientes. Esta condición constituye una regla fundamental de gobernanza del sistema.

**Sexta.** El presente Módulo 1 establece una base para continuar con actividades de diseño, selección tecnológica y experimentación. Antes de implementar el prototipo será necesario validar con la entidad territorial el diagnóstico, el conjunto documental piloto, los roles, las políticas de acceso, el hardware, las restricciones institucionales y los criterios de evaluación.

---

# 18. RECOMENDACIONES

1. **Validar el diagnóstico institucional** mediante entrevistas o sesiones de trabajo con las áreas jurídica, administrativa, tecnológica y de gestión documental.

2. **Seleccionar un conjunto documental piloto** que represente diferentes tipos de archivos, formatos y niveles de complejidad, evitando inicialmente información cuyo tratamiento no haya sido autorizado.

3. **Definir responsables de aprobación**, estableciendo quién podrá validar fuentes, revisar respuestas y aprobar borradores.

4. **Inventariar el hardware disponible**, incluyendo CPU, RAM, GPU, almacenamiento y condiciones de red, antes de seleccionar el modelo de lenguaje.

5. **Establecer políticas de acceso**, diferenciando usuarios de consulta, administradores, responsables de aprobación y personal técnico.

6. **Diseñar un conjunto de evaluación**, con preguntas y respuestas esperadas que permitan medir posteriormente recuperación, citas, pertinencia y comportamiento frente a información insuficiente.

7. **Preparar datos públicos, anonimizados o expresamente autorizados** para las primeras pruebas del sistema.

8. **Validar las licencias** de modelos, embeddings, bases de datos, bibliotecas y demás componentes tecnológicos antes de incorporarlos a la arquitectura.

9. **Preparar un repositorio local de modelos y paquetes**, manteniendo versiones conocidas y documentadas para facilitar reproducibilidad.

10. **Diseñar pruebas de seguridad**, incluyendo escenarios de acceso indebido, recuperación de información restringida, prompt injection y consultas diseñadas para provocar fuga de información.

11. **Definir un procedimiento de actualización documental**, especificando quién incorpora nuevas versiones, cómo se identifican documentos reemplazados y qué sucede con los índices anteriores.

12. **Implementar mecanismos de trazabilidad desde las primeras pruebas**, registrando modelo, versión, documentos consultados, configuración y resultado.

13. **Establecer mecanismos de abstención**, de manera que el asistente pueda indicar que la evidencia disponible no es suficiente en lugar de generar una respuesta aparentemente concluyente.

14. **Mantener separación entre repositorio oficial y entorno de generación**, evitando que el asistente modifique autónomamente documentos institucionales.

15. **Aplicar el principio de mínimo privilegio**, limitando tanto los permisos de los usuarios como los de los componentes técnicos del asistente.

16. **Realizar benchmarking antes de seleccionar el modelo**, comparando calidad, memoria, latencia y consumo computacional con el hardware realmente disponible.

17. **Documentar las decisiones arquitectónicas**, incluyendo las razones para seleccionar modelos, bases de conocimiento, mecanismos de recuperación y herramientas.

18. **Establecer un procedimiento de respuesta ante incidentes**, especialmente para casos de exposición de información, acceso indebido, pérdida de documentos o generación de respuestas no sustentadas.

19. **Incorporar evaluación periódica**, debido a que los documentos, modelos, dependencias y riesgos pueden cambiar durante el ciclo de vida del sistema. El enfoque del NIST AI RMF considera la gestión del riesgo como una actividad continua y no como una evaluación única.

20. **Mantener la supervisión humana como requisito estructural**, evitando que una futura evolución hacia agentes autónomos convierta al asistente en un mecanismo de decisión jurídica o administrativa sin autorización institucional.

---

## NOTA METODOLÓGICA

Los elementos presentados en este documento deben distinguirse entre **hechos suministrados para la formulación del proyecto, supuestos de diseño, propuestas técnicas, riesgos identificados y datos pendientes de validación**. La información específica de **[entidad territorial objeto de estudio]**, incluyendo nombre, estructura, cantidad de documentos, infraestructura, políticas internas, responsables, procesos y restricciones, deberá ser confirmada mediante trabajo de campo o documentación institucional autorizada.

Los requisitos, riesgos, criterios de éxito y alternativas de arquitectura aquí formulados constituyen una **línea base preliminar**. Deberán ser revisados y validados con los usuarios, responsables de información, personal jurídico, gestión documental, tecnologías de la información, responsables de protección de datos y demás partes interesadas antes de iniciar una implementación.

La referencia al marco NIST AI RMF se utiliza como estructura de gestión de riesgos y gobernanza; no se presenta como sustituto de las políticas institucionales ni de las obligaciones legales aplicables. El NIST AI RMF es un marco de uso voluntario orientado a apoyar la gestión de riesgos y la incorporación de características de confianza en sistemas de IA.

De igual manera, la referencia a la Ley 1581 de 2012 tiene finalidad académica y de formulación de requisitos de privacidad. Su inclusión no constituye asesoría jurídica ni pretende determinar la aplicación definitiva de la legislación a un caso institucional específico. La evaluación jurídica concreta deberá realizarse con los responsables competentes de la entidad.

---

## REFERENCIAS DE CONSULTA

**National Institute of Standards and Technology (NIST).** *Artificial Intelligence Risk Management Framework (AI RMF 1.0).* 2023. El marco establece las funciones Govern, Map, Measure y Manage para apoyar la gestión de riesgos de inteligencia artificial.

**National Institute of Standards and Technology (NIST).** *NIST AI RMF Playbook.* Recurso complementario al AI RMF que presenta acciones sugeridas asociadas con Govern, Map, Measure y Manage.

**República de Colombia. Congreso de la República.** *Ley Estatutaria 1581 de 2012, por la cual se dictan disposiciones generales para la protección de datos personales.* Gestor Normativo de Función Pública.

**Fuente académica del diplomado:** Documento base del Diplomado IA 5.0 Lab, Módulo 1, 2026. **[Documento por validar/adjuntar para completar la referencia bibliográfica específica].**

