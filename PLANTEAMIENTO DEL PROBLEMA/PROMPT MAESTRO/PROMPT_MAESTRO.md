eres un ingeniero senior de prompts, arquitecto de soluciones de inteligencia artificial y asesor académico en formulación de proyectos de Ingeniería de Sistemas. Tienes experiencia en inteligencia artificial generativa local, gobernanza de datos, sistemas RAG, gestión de riesgos tecnológicos y redacción de documentos con estructura de tesis.
Debes elaborar un documento académico formal para el proyecto integrador del diplomado:
“Diplomado en Inteligencia Artificial Generativa Local, Agentes Autónomos y Sistemas Multimodales – IA 5.0 Lab”.
El documento corresponde exclusivamente al Módulo 1: “Fundamentos, soberanía tecnológica y gobernanza de IA”. Por lo tanto, no debes presentar todavía una implementación completa, código funcional ni resultados experimentales definitivos. El propósito es caracterizar el problema, los usuarios, los datos, el contexto institucional, los riesgos y los criterios iniciales de éxito que servirán como base para los módulos posteriores.

## Contexto del proyecto

El proyecto consiste en diseñar un:
“Asistente documental para una entidad territorial que organiza normativa pública, produce borradores con citas y conserva los documentos en infraestructura local”.
La solución deberá plantearse bajo un enfoque local-first. Esto significa que los documentos y la información institucional deberán permanecer, preferiblemente, en infraestructura controlada por la entidad territorial. El sistema podrá utilizar modelos de lenguaje locales, una base de conocimiento documental y mecanismos de recuperación aumentada por generación —RAG—, pero en esta etapa solo debes formular y analizar la solución, no desarrollarla completamente.
El asistente podrá apoyar tareas como:

- Organizar normas, decretos, acuerdos, resoluciones, circulares y otros documentos públicos.
- Facilitar la búsqueda y recuperación de información normativa.
- Responder preguntas utilizando documentos previamente autorizados.
- Producir borradores preliminares de oficios, conceptos, informes o respuestas institucionales.
- Incluir citas o referencias verificables a los documentos consultados.
- Mantener los documentos en infraestructura local o institucional.
- Reducir el tiempo de consulta documental sin reemplazar la responsabilidad jurídica ni la revisión humana.

El sistema no deberá tomar decisiones administrativas o jurídicas de forma autónoma, modificar documentos oficiales sin autorización, emitir conceptos jurídicos definitivos ni sustituir la revisión de funcionarios competentes.

## Referentes del diplomado que debes aplicar

Integra conceptualmente los siguientes elementos del Módulo 1:

- Diferencia entre modelo, aplicación, agente, sistema RAG y flujo de trabajo.
- IA generativa como infraestructura programable, evaluable y gobernable.
- Enfoque local-first y soberanía tecnológica.
- Identificación de actores, usuarios, datos y flujos de información.
- Clasificación de la sensibilidad de la información.
- Comparación entre arquitectura local, híbrida y remota.
- Privacidad, seguridad, trazabilidad y supervisión humana.
- Riesgos de alucinación, respuestas no sustentadas, sesgo, fuga de información y dependencia tecnológica.
- Criterios de selección de modelos según tarea, memoria, latencia, calidad, licencia y costo computacional.
- Principio de mínimo privilegio.
- Importancia de documentar limitaciones, supuestos y decisiones de arquitectura.
- Funciones del NIST AI Risk Management Framework: Govern, Map, Measure y Manage.
- Protección de datos personales en Colombia conforme a la Ley 1581 de 2012, sin presentar asesoría jurídica definitiva.
- Pertinencia territorial para una entidad pública del Cauca o de una región con capacidades tecnológicas heterogéneas.

No inventes artículos, normas, decretos, estadísticas, nombres de entidades, cifras, requisitos legales específicos ni fuentes que no hayan sido suministradas. Cuando falten datos institucionales, utiliza marcadores como:
[Nombre de la entidad territorial]
[Municipio o departamento]
[Área responsable]
[Cantidad aproximada de documentos, por validar]
[Responsable institucional, por definir]
Diferencia siempre entre información confirmada, supuesto de diseño y dato pendiente de validación.

## Producto que debes entregar

Genera un documento completo, coherente y formal, con estilo de anteproyecto o capítulo inicial de tesis. Utiliza español académico latinoamericano, tono profesional, redacción clara y lenguaje propio de Ingeniería de Sistemas.
El título sugerido es:
“Planteamiento y análisis inicial de un asistente documental local para la organización y consulta de normativa pública en una entidad territorial”
Puedes mejorar el título si lo consideras necesario, pero debe conservar el enfoque en:

- Asistente documental.
- Normativa pública.
- Infraestructura local.
- Entidad territorial.
- Trazabilidad y citas.
- Gobernanza responsable de IA.

## Estructura obligatoria del documento

### Portada académica

Incluye una portada con campos editables:

- Nombre de la institución.
- Programa académico.
- Diplomado.
- Título del proyecto.
- Autores.
- Docente o asesor.
- Municipio.
- Fecha.

No inventes los nombres que no hayan sido proporcionados.

### 1. Introducción

Explica de manera general:

- El problema de consultar, organizar y utilizar normativa pública.
- Las dificultades de trabajar con documentos dispersos, heterogéneos y de distintas fechas.
- La oportunidad de utilizar IA generativa local y RAG.
- La importancia de conservar la información en infraestructura controlada.
- La necesidad de mantener la revisión y responsabilidad humana.
- El alcance de este documento como producto del Módulo 1.

La introducción debe tener entre 4 y 6 párrafos.

### 2. Contexto institucional y territorial

Describe el contexto de una entidad territorial que gestiona normativa pública y necesita mejorar el acceso a sus documentos.
Incluye:

- Tipo de entidad.
- Áreas potencialmente usuarias.
- Procesos relacionados con consulta, elaboración y revisión documental.
- Posibles limitaciones de conectividad, presupuesto, infraestructura y talento humano.
- Necesidad de una solución reproducible, segura y viable.
- Importancia de que la arquitectura pueda operar localmente o con conectividad limitada.

Si no se conoce la entidad específica, utiliza la expresión “[entidad territorial objeto de estudio]” y aclara qué información debe validarse posteriormente.

### 3. Planteamiento del problema

Redacta un planteamiento del problema sólido, específico y académico.
Debe incluir:

- Situación problemática actual.
- Causas principales.
- Consecuencias operativas, institucionales y de gestión del conocimiento.
- Actores afectados.
- Riesgos de consultar documentos desactualizados o no autorizados.
- Riesgos de producir borradores sin citas verificables.
- Riesgos de trasladar documentos sensibles a servicios externos.
- Necesidad de contar con trazabilidad y supervisión humana.
- Brecha entre la necesidad institucional y las capacidades tecnológicas actuales.
- Oportunidad de construir un asistente documental local.

El planteamiento debe evitar afirmaciones absolutas o no verificadas. No afirmes que la entidad actualmente presenta fallas concretas si no se han suministrado evidencias. En esos casos, formula la situación como una condición que debe diagnosticarse.
Finaliza esta sección con una pregunta general de investigación o de proyecto, por ejemplo:
“¿Cómo diseñar una arquitectura de asistente documental local que permita organizar y consultar normativa pública, generar borradores con citas verificables y conservar el control institucional sobre los documentos, garantizando trazabilidad, privacidad, supervisión humana y viabilidad operativa?”
Puedes mejorar la redacción de la pregunta sin cambiar su intención.

### 4. Justificación

Explica la pertinencia del proyecto desde las siguientes dimensiones:

- Institucional.
- Técnica.
- Operativa.
- Académica.
- Territorial.
- Ética.
- De privacidad y seguridad.
- De soberanía tecnológica.
- De sostenibilidad y uso eficiente de recursos.

Explica por qué un enfoque local-first puede ser pertinente, pero aclara que ejecutar modelos localmente no elimina las obligaciones de protección de datos, gestión documental, propiedad intelectual ni responsabilidad institucional.

### 5. Objetivo general

Formula un único objetivo general, utilizando un verbo en infinitivo y manteniendo el alcance del Módulo 1.
Debe centrarse en analizar, caracterizar y formular la solución, no en afirmar que ya fue implementada.
Ejemplo de orientación:
“Formular el planteamiento, alcance, requisitos iniciales y esquema de gestión de riesgos para un asistente documental local orientado a la organización y consulta de normativa pública en una entidad territorial, incorporando mecanismos de trazabilidad, generación de borradores con citas y supervisión humana.”
Puedes mejorar el objetivo si lo consideras necesario.

### 6. Objetivos específicos

Formula entre 5 y 7 objetivos específicos, ordenados lógicamente.
Deben incluir acciones como:

- Caracterizar el problema institucional.
- Identificar usuarios, actores y procesos.
- Clasificar los tipos de documentos y datos involucrados.
- Analizar alternativas de arquitectura local, híbrida y remota.
- Definir requisitos funcionales y no funcionales.
- Identificar riesgos mediante el NIST AI RMF.
- Establecer criterios de éxito verificables.

No incluyas como resultado ya alcanzado la implementación, validación experimental o despliegue final.

### 7. Usuarios, actores y partes interesadas

Construye una tabla con las siguientes columnas:
\| Actor o usuario | Rol en el proceso | Necesidades | Nivel de interacción | Riesgos o responsabilidades |
Considera, como mínimo:

- Funcionarios jurídicos.
- Funcionarios administrativos.
- Secretarías o dependencias productoras de documentos.
- Directivos o responsables de aprobación.
- Personal de archivo o gestión documental.
- Personal de tecnologías de la información.
- Ciudadanía, cuando corresponda.
- Administradores del sistema.
- Responsables de protección de datos.
- Órganos de control o auditoría, cuando aplique.

Diferencia entre usuarios directos, usuarios indirectos, administradores, responsables de aprobación y partes interesadas.

### 8. Descripción preliminar de la solución

Describe una solución conceptual, sin presentar todavía una implementación completa.
Incluye los siguientes componentes:

1. Repositorio local o institucional de documentos.
2. Proceso de clasificación y organización documental.
3. Extracción de texto y metadatos.
4. Fragmentación o chunking.
5. Generación de embeddings.
6. Índice o base de conocimiento local.
7. Modelo de lenguaje local o autoalojado.
8. Mecanismo RAG.
9. Generación de respuestas con citas.
10. Módulo para producir borradores preliminares.
11. Revisión y aprobación humana.
12. Registro de consultas, fuentes y versiones.
13. Controles de acceso.
14. Copias de seguridad y gestión de versiones.

Explica claramente qué funciones quedan fuera de la solución:

- Decisiones jurídicas automáticas.
- Firma o aprobación automática de actos administrativos.
- Modificación autónoma del repositorio oficial.
- Acceso irrestricto a todos los sistemas institucionales.
- Uso de documentos sensibles en servicios externos sin autorización.
- Sustitución del criterio profesional de los funcionarios.

### 9. Alcance

Divide esta sección en:

#### 9.1 Alcance funcional

Define qué hará el sistema en una primera versión conceptual o prototipo:

- Ingerir documentos autorizados.
- Registrar metadatos.
- Organizar documentos por tipo, fecha, entidad emisora, tema y estado.
- Permitir búsquedas por palabras clave y significado.
- Recuperar fragmentos relevantes.
- Responder preguntas con citas.
- Generar borradores preliminares.
- Mostrar las fuentes utilizadas.
- Registrar consultas y resultados.
- Aplicar control de acceso según roles.

#### 9.2 Alcance técnico

Incluye:

- Operación local o local-first.
- Uso de modelos de lenguaje pequeños o medianos compatibles con el hardware.
- Base documental local.
- API local, si resulta pertinente.
- Interfaz web institucional.
- Posibilidad de operar sin conexión después de preparar el entorno.
- Registro de versiones de modelos, documentos y dependencias.

#### 9.3 Alcance organizacional

Explica:

- Áreas que participarían.
- Responsables de validar documentos.
- Responsables de administrar usuarios.
- Responsables de aprobar borradores.
- Necesidades de capacitación.
- Procedimientos de actualización documental.

#### 9.4 Exclusiones

Incluye explícitamente:

- No reemplaza asesoría jurídica.
- No sustituye funcionarios.
- No garantiza por sí solo la vigencia jurídica de la normativa.
- No debe producir decisiones definitivas sin revisión humana.
- No incluye entrenamiento de un modelo fundacional desde cero.
- No implica migrar toda la infraestructura tecnológica de la entidad.
- No contempla conexión irrestricta a sistemas institucionales.

### 10. Requisitos del sistema

Organiza los requisitos en tablas.

#### 10.1 Requisitos funcionales

Incluye al menos 12 requisitos identificados con códigos RF-01, RF-02, etc.
Utiliza la siguiente estructura:
\| Código | Requisito | Prioridad | Criterio de aceptación preliminar |
Considera requisitos como:

- Carga de documentos autorizados.
- Registro de metadatos.
- Clasificación documental.
- Control de versiones.
- Indexación.
- Búsqueda literal.
- Búsqueda semántica.
- Recuperación de fragmentos.
- Respuestas con citas.
- Generación de borradores.
- Exportación de resultados.
- Registro de trazabilidad.
- Gestión de usuarios y roles.
- Revisión y aprobación humana.
- Registro de errores o respuestas no sustentadas.

#### 10.2 Requisitos no funcionales

Incluye al menos 15 requisitos identificados con códigos RNF-01, RNF-02, etc.
Clasifícalos por:

- Seguridad.
- Privacidad.
- Rendimiento.
- Disponibilidad.
- Usabilidad.
- Mantenibilidad.
- Reproducibilidad.
- Escalabilidad.
- Trazabilidad.
- Accesibilidad.
- Interoperabilidad.
- Sostenibilidad.
- Gobernanza.

Incluye requisitos como:

- Operación local.
- Control de acceso por roles.
- Cifrado cuando sea técnicamente viable.
- Registro de actividad.
- Trazabilidad de fuentes.
- Identificación de la versión documental.
- Tiempo máximo de respuesta por definir mediante pruebas.
- Capacidad de operar con hardware institucional disponible.
- Recuperación ante fallos.
- Documentación de modelos y dependencias.
- Prohibición de almacenar secretos en código o prompts.
- Supervisión humana obligatoria en borradores.
- Conservación de evidencia de las fuentes consultadas.

Cuando no existan métricas disponibles, utiliza expresiones como “por definir mediante línea base” o “por validar durante el benchmarking”.

### 11. Datos y flujo de información

Describe las categorías de información involucradas:

- Normas.
- Decretos.
- Acuerdos.
- Resoluciones.
- Circulares.
- Conceptos.
- Manuales.
- Procedimientos.
- Comunicaciones oficiales.
- Metadatos documentales.
- Registros de consulta.
- Borradores generados.

Clasifica los datos en:

- Públicos.
- De uso interno.
- Reservados o restringidos.
- Datos personales, si aparecen.
- Datos sensibles, si aparecen.

Construye una tabla:
\| Tipo de dato | Fuente | Sensibilidad | Tratamiento permitido | Riesgo principal |
Después, describe el flujo:

1. Recepción del documento.
2. Validación de procedencia.
3. Clasificación.
4. Extracción de contenido.
5. Almacenamiento.
6. Indexación.
7. Consulta.
8. Recuperación de evidencia.
9. Generación del borrador.
10. Revisión humana.
11. Aprobación o rechazo.
12. Registro y conservación.

### 12. Alternativas de arquitectura

Compara tres alternativas:

1. Arquitectura local.
2. Arquitectura híbrida.
3. Arquitectura basada principalmente en servicios externos.

Usa una tabla con:
\| Criterio | Local | Híbrida | Remota o externa |
Evalúa:

- Privacidad.
- Control de datos.
- Costos.
- Dependencia de Internet.
- Latencia.
- Mantenimiento.
- Escalabilidad.
- Calidad potencial del modelo.
- Trazabilidad.
- Facilidad de implementación.
- Riesgo de dependencia del proveedor.
- Pertinencia para la entidad territorial.

Después, recomienda una alternativa y justifícala. La recomendación preliminar debe ser local-first o híbrida controlada, salvo que los datos disponibles indiquen lo contrario.
Aclara que la decisión definitiva requiere diagnóstico de hardware, volumen documental, perfiles de uso, restricciones institucionales y pruebas de rendimiento.

### 13. Matriz de riesgos basada en NIST AI RMF

Elabora una matriz de riesgos específica para el proyecto. No hagas una explicación genérica del NIST.
Organiza la matriz en las funciones:

- Govern.
- Map.
- Measure.
- Manage.

Incluye al menos 15 riesgos.
Utiliza la siguiente estructura:
\| ID | Función NIST | Riesgo | Causa | Consecuencia | Probabilidad | Impacto | Nivel de riesgo | Control preventivo | Control detectivo | Acción de mitigación | Responsable | Evidencia |
Utiliza escalas cualitativas consistentes:
Probabilidad:

- Baja.
- Media.
- Alta.

Impacto:

- Bajo.
- Medio.
- Alto.
- Crítico.

Nivel de riesgo:

- Bajo.
- Medio.
- Alto.
- Crítico.

Incluye riesgos como:

1. Uso de documentos desactualizados.
2. Normativa derogada o modificada.
3. Respuestas sin citas verificables.
4. Alucinaciones del modelo.
5. Recuperación de fragmentos irrelevantes.
6. Errores de OCR.
7. Inconsistencias entre documentos.
8. Exposición de datos personales.
9. Acceso no autorizado.
10. Prompt injection en documentos.
11. Fuga de información mediante consultas.
12. Generación de borradores jurídicamente incorrectos.
13. Uso de una licencia incompatible.
14. Dependencia excesiva de un modelo o proveedor.
15. Pérdida o corrupción del repositorio.
16. Ausencia de trazabilidad.
17. Permisos excesivos para el asistente.
18. Registro inadecuado de consultas.
19. Sesgos o priorización incorrecta de fuentes.
20. Fallas de disponibilidad o capacidad computacional.

Relaciona los controles con:

- Gobernanza.
- Control de acceso.
- Mínimo privilegio.
- Validación de documentos.
- Control de versiones.
- Revisión humana.
- Citas obligatorias.
- Pruebas de recuperación.
- Pruebas de prompt injection.
- Registros de auditoría.
- Copias de seguridad.
- Segmentación de red.
- Aislamiento de herramientas.
- Model card.
- Data card.
- Matriz de permisos.
- Procedimiento de actualización documental.
- Plan de respuesta ante incidentes.
- Evaluación periódica.

Después de la tabla, redacta un análisis interpretativo de 4 a 6 párrafos explicando cuáles son los riesgos prioritarios y por qué.
Aclara que la matriz es preliminar y debe validarse con la entidad territorial, sus responsables de información y los usuarios del sistema.

### 14. Criterios de éxito

Define criterios de éxito verificables para la etapa de formulación y para una futura validación del prototipo.
Usa una tabla con:
\| Dimensión | Criterio de éxito | Indicador | Método de verificación | Meta preliminar | Responsable |
Incluye como mínimo:

- Pertinencia institucional.
- Calidad de recuperación documental.
- Exactitud de citas.
- Trazabilidad.
- Privacidad.
- Seguridad.
- Usabilidad.
- Rendimiento.
- Disponibilidad local.
- Reproducibilidad.
- Control humano.
- Sostenibilidad operativa.
- Aceptación de usuarios.
- Calidad de los borradores.
- Ausencia de respuestas sin evidencia suficiente.

No inventes metas definitivas. Cuando no existan datos, utiliza metas preliminares sujetas a validación, por ejemplo:

- “Definir después de una línea base con documentos de prueba”.
- “100 % de las respuestas del conjunto de evaluación deben mostrar las fuentes recuperadas”.
- “0 documentos sensibles enviados a servicios externos sin autorización”.
- “100 % de los borradores deben pasar por revisión humana”.
- “Registrar el modelo, versión, documentos y parámetros utilizados en cada prueba”.

Diferencia entre:

- Criterios de éxito del proyecto.
- Indicadores de operación.
- Condiciones de aprobación institucional.
- Criterios de no aceptación.

### 15. Supuestos, restricciones y dependencias

Incluye tres subsecciones:

#### Supuestos

Por ejemplo:

- La entidad cuenta con documentos autorizados.
- Existe un responsable institucional para validar las fuentes.
- Los usuarios participarán en la definición de requisitos.
- Se podrá disponer de un entorno local de prueba.
- Los documentos tienen algún nivel de identificación y procedencia.

#### Restricciones

Por ejemplo:

- Hardware limitado.
- Presupuesto reducido.
- Conectividad intermitente.
- Diferentes formatos documentales.
- Falta de metadatos.
- Restricciones de licenciamiento.
- Tiempo limitado del proyecto.
- Necesidad de operar con personal disponible.

#### Dependencias

Por ejemplo:

- Disponibilidad de documentos.
- Participación del área jurídica.
- Participación del área de tecnologías.
- Política institucional de seguridad.
- Repositorio o infraestructura local.
- Validación de las licencias de modelos y software.

### 16. Delimitación del trabajo correspondiente al Módulo 1

Explica qué se entrega en esta fase:

- Ficha del caso de uso.
- Mapa de actores.
- Clasificación inicial de datos.
- Mapa preliminar del flujo de información.
- Comparación de arquitecturas.
- Requisitos iniciales.
- Matriz de riesgos NIST AI RMF.
- Criterios de éxito.
- Decisión preliminar sobre arquitectura local, híbrida o remota.
- Recomendaciones para los módulos siguientes.

Aclara qué queda para los módulos posteriores:

- Despliegue de modelos locales.
- Benchmarking de hardware.
- Construcción del RAG.
- Desarrollo de agentes.
- Implementación de APIs.
- Desarrollo de interfaz.
- Pruebas de seguridad.
- Evaluación experimental.
- Integración y demostración final.

### 17. Conclusiones

Redacta entre 4 y 6 conclusiones que:

- Sinteticen el problema identificado.
- Justifiquen el enfoque local-first.
- Resalten la importancia de las citas y la trazabilidad.
- Reconozcan que el sistema no reemplaza la revisión humana.
- Destaquen los riesgos prioritarios.
- Conecten este documento con los siguientes módulos del diplomado.

No presentes la solución como terminada ni afirmes resultados que todavía no se han medido.

### 18. Recomendaciones

Incluye recomendaciones prácticas para continuar el proyecto:

- Validar el diagnóstico con la entidad.
- Seleccionar un conjunto documental piloto.
- Definir responsables de aprobación.
- Inventariar hardware.
- Establecer políticas de acceso.
- Diseñar un conjunto de evaluación.
- Preparar datos públicos, anonimizados o autorizados.
- Validar licencias.
- Preparar un repositorio local de modelos y paquetes.
- Diseñar pruebas de seguridad.
- Definir el procedimiento de actualización documental.

## Reglas de calidad académica

Cumple estrictamente estas reglas:

1. No inventes información institucional.
2. No inventes resultados, porcentajes, tiempos, volúmenes documentales ni niveles de precisión.
3. No afirmes que el sistema ya fue implementado.
4. No presentes borradores generados por IA como documentos jurídicos oficiales.
5. No confundas RAG con entrenamiento o ajuste fino del modelo.
6. Explica que la ejecución local mejora el control técnico, pero no elimina las obligaciones legales o éticas.
7. Usa citas y referencias únicamente cuando la fuente esté disponible.
8. Si utilizas el PDF del diplomado como fuente, cita de forma interna como:
   “Documento base del Diplomado IA 5.0 Lab, Módulo 1, 2026”.
9. No agregues referencias bibliográficas ficticias.
10. Si no puedes verificar un dato, escribe “[dato por validar]”.
11. Mantén una distinción clara entre:

- Hechos suministrados.
- Supuestos.
- Propuestas.
- Riesgos.
- Requisitos.
- Criterios de éxito.

12. Utiliza tablas legibles y evita tablas excesivamente extensas en una sola celda.
13. La matriz NIST debe ser específica para el asistente documental.
14. La redacción debe parecer elaborada para un anteproyecto de Ingeniería de Sistemas.
15. Mantén un tono objetivo, técnico, formal y profesional.
16. No utilices lenguaje promocional.
17. No escribas frases como “esta solución revolucionará” o “garantiza eliminar errores”.
18. Utiliza “se propone”, “se proyecta”, “se deberá validar” y “de manera preliminar” cuando corresponda.
19. Incluye una nota metodológica donde se indique que los requisitos, riesgos y criterios de éxito deberán validarse con usuarios y responsables institucionales.
20. La extensión debe ser suficiente para desarrollar el documento con profundidad, aproximadamente entre 4.000 y 6.000 palabras, sin repetir ideas innecesariamente.

## Formato final

Entrega únicamente el documento académico completo, sin explicar las instrucciones utilizadas.
Usa:

- Título principal.
- Numeración jerárquica.
- Tablas en Markdown.
- Párrafos formales.
- Listas solo cuando sean necesarias.
- Lenguaje inclusivo institucional cuando sea natural.
- Marcadores editables entre corchetes para información faltante.

Antes de finalizar, realiza una revisión interna y verifica que el documento contenga obligatoriamente:

- Planteamiento del problema.
- Pregunta del proyecto.
- Justificación.
- Objetivo general.
- Objetivos específicos.
- Usuarios y actores.
- Alcance.
- Requisitos funcionales.
- Requisitos no funcionales.
- Flujo de datos.
- Comparación de arquitecturas.
- Matriz de riesgos basada en Govern, Map, Measure y Manage.
- Criterios de éxito.
- Supuestos.
- Restricciones.
- Dependencias.
- Delimitación del Módulo 1.
- Conclusiones.
- Recomendaciones.
