# Generación de cartas, avisos y traducciones profesionales.

## Metadatos

| Atributo | Detalle |
|---|---|
| **Duración estimada** | 60 minutos |
| **Complejidad** | Fácil |
| **Nivel Bloom** | Aplicar (Apply) |
| **Módulo** | 1 — Ingeniería de prompts aplicada a la gestión de personas |
| **Versión del laboratorio** | 1.0 |
| **Última revisión** | 2025 |

---

> ⚠️ **ADVERTENCIA LEGAL CRÍTICA**
> Copilot Chat es una herramienta de apoyo y productividad, **NO un sustituto de asesoría jurídica laboral certificada**. Todos los documentos generados durante esta práctica deben ser revisados por un profesional legal antes de su implementación en situaciones reales.
>
> 🔒 **PRIVACIDAD DE DATOS**: No ingreses datos reales de empleados (nombres, CURP, RFC, salarios) en Copilot Chat. Todos los ejercicios utilizan datos **ficticios**. Verifica la política de privacidad de datos de tu organización antes de usar herramientas de IA generativa.

---

## Descripción General

En esta práctica aplicarás la plantilla **RCTF-EC** (Rol, Contexto, Tarea, Formato, Evidencias y Cumplimiento) para generar cinco tipos de documentos laborales de uso cotidiano en Recursos Humanos mediante Microsoft 365 Copilot Chat. Aprenderás a construir prompts iniciales, evaluar las respuestas obtenidas, aplicar refinamiento iterativo y documentar versiones mejoradas. Al finalizar, compilarás un mini-repositorio personal de prompts reutilizables que podrás adaptar a escenarios reales de Relaciones Laborales.

---

## Objetivos de Aprendizaje

Al completar este laboratorio, serás capaz de:

- [ ] Construir prompts estructurados con la plantilla RCTF-EC para generar documentos laborales formales en Copilot Chat.
- [ ] Aplicar técnicas de refinamiento iterativo (*follow-up prompts*) para mejorar la calidad, precisión y apego normativo de los documentos generados.
- [ ] Generar traducciones profesionales de documentos laborales evaluando la fidelidad terminológica en contextos de Relaciones Laborales.
- [ ] Identificar los elementos legales mínimos requeridos en comunicados laborales conforme a la Ley Federal del Trabajo (LFT) mexicana.
- [ ] Organizar un repositorio personal de prompts parametrizados reutilizables para el área de RR.HH.

---

## Prerrequisitos

### Conocimientos previos

| Área | Nivel requerido |
|---|---|
| Estructura de una carta formal en español | Básico |
| Tipos de documentos laborales en empresas mexicanas | Básico |
| Conceptos de ingeniería de prompts (lección 1.1) | Completado |
| Conocimiento general de la LFT | Referencial |

### Acceso y licencias

| Recurso | Requisito |
|---|---|
| Cuenta corporativa Microsoft 365 | Activa y verificada |
| Licencia Microsoft 365 Copilot | **Habilitada** (confirmar con TI con 48 h de anticipación) |
| Microsoft Word (Microsoft 365 Apps, versión 2301+) | Instalado |
| Microsoft OneDrive | Sincronizado con la cuenta corporativa |
| Navegador Microsoft Edge 120+ o Google Chrome 120+ | Instalado y actualizado |

> 💡 **Verificación rápida de licencia**: Accede a [https://copilot.microsoft.com](https://copilot.microsoft.com) con tu cuenta corporativa. Si ves la interfaz de Copilot Chat empresarial (con el logo de tu organización o la indicación "Trabajo"), la licencia está activa. Si redirige a Bing o muestra una versión gratuita, contacta a tu administrador de TI.

---

## Entorno del Laboratorio

### Especificaciones de hardware

| Componente | Mínimo requerido | Recomendado |
|---|---|---|
| Procesador | Intel Core i5 8ª gen / AMD Ryzen 5 | Intel Core i7 / AMD Ryzen 7 |
| RAM | 8 GB | 16 GB |
| Almacenamiento libre | 2 GB | 5 GB |
| Resolución de pantalla | 1366 × 768 | 1920 × 1080 |
| Conexión a Internet | 10 Mbps | 25 Mbps o superior |

### Especificaciones de software

| Software | Versión mínima | Propósito en el laboratorio |
|---|---|---|
| Microsoft 365 Copilot Chat | Licencia empresarial activa | Generación de documentos con IA |
| Microsoft Word (Microsoft 365) | 2301 o superior | Edición y almacenamiento de documentos |
| Microsoft OneDrive | Integrado con M365 | Organización de entregables |
| Microsoft Edge o Google Chrome | 120 o superior | Acceso a Copilot Chat web |
| Adobe Acrobat Reader o Edge PDF Viewer | 2020 o superior | Revisión de documentos en PDF |

### Configuración inicial del entorno

Antes de comenzar los ejercicios, realiza los siguientes pasos de configuración:

**1. Crear la estructura de carpetas en OneDrive**

Abre el Explorador de archivos o accede a [https://onedrive.com](https://onedrive.com) y crea la siguiente estructura:

```
OneDrive/
└── Curso_Copilot_RRHH/
    └── Practica_01/
        ├── Prompts/
        ├── Documentos_Generados/
        └── Repositorio_Prompts/
```

**2. Crear el archivo de registro de prompts**

Abre Microsoft Word y crea un documento nuevo llamado `Repositorio_Prompts_P01.docx`. Guárdalo en `OneDrive/Curso_Copilot_RRHH/Practica_01/Repositorio_Prompts/`. Este archivo será tu mini-repositorio personal al final de la práctica.

Agrega la siguiente tabla de encabezado al documento:

```
| ID Prompt | Tipo de Documento | Versión | Fecha | Propósito | Notas de Ajuste |
|-----------|-------------------|---------|-------|-----------|-----------------|
|           |                   |         |       |           |                 |
```

**3. Acceder a Microsoft 365 Copilot Chat**

1. Abre Microsoft Edge o Google Chrome.
2. Navega a [https://copilot.microsoft.com](https://copilot.microsoft.com).
3. Inicia sesión con tu cuenta corporativa Microsoft 365.
4. Verifica que aparezca el modo **"Trabajo"** (Work) en la parte superior de la interfaz.
5. Selecciona el modo de conversación **"Más equilibrado"** o **"Más preciso"** para obtener respuestas formales.

> ⚠️ Si no aparece el modo "Trabajo", detente y contacta a tu administrador de TI. No continúes con datos en el modo "Web" (Bing), ya que los datos no están protegidos bajo el acuerdo empresarial.

---

## Instrucciones Paso a Paso

---

### Paso 1: Carta de Bienvenida a Nuevo Colaborador

**Objetivo del paso:** Construir y refinar un prompt RCTF-EC para generar una carta de bienvenida profesional y cálida para un nuevo empleado ficticio, aplicando lenguaje inclusivo y elementos formales de RR.HH.

#### Instrucciones

**1.1 — Construir el prompt inicial (versión genérica)**

En la interfaz de Copilot Chat, escribe el siguiente prompt básico y observa el resultado:

```text
Escribe una carta de bienvenida para un nuevo empleado.
```

Copia la respuesta obtenida en un documento Word llamado `Carta_Bienvenida_v1.docx` y guárdalo en `Practica_01/Documentos_Generados/`.

**1.2 — Analizar las deficiencias del prompt genérico**

Antes de continuar, responde mentalmente (o en tu cuaderno) las siguientes preguntas de evaluación:

- ¿La carta menciona el nombre de la empresa o el puesto del colaborador?
- ¿Tiene un tono formal y profesional adecuado para RR.HH.?
- ¿Incluye información sobre el primer día, prestaciones o contacto de RR.HH.?
- ¿Utiliza lenguaje inclusivo (sin asumir género)?

**1.3 — Construir el prompt mejorado con RCTF-EC**

En el **mismo hilo de conversación** de Copilot Chat, escribe el siguiente prompt refinado:

```text
Rol y audiencia:
Soy especialista de Recursos Humanos de una empresa manufacturera mediana en México.
Este documento es para un nuevo colaborador que se incorpora al área de Operaciones.

Contexto y datos:
- Empresa ficticia: "Manufacturas del Norte, S.A. de C.V."
- Nombre del colaborador (ficticio): Alex Martínez
- Puesto: Analista de Operaciones Jr.
- Fecha de ingreso: primer lunes del próximo mes
- Prestaciones de ley: IMSS, INFONAVIT, vacaciones, prima vacacional, aguinaldo conforme a LFT
- Contacto de RR.HH. (ficticio): recursos.humanos@manufacnorte.com.mx

Tarea:
Redacta una carta de bienvenida formal para Alex Martínez que transmita entusiasmo
institucional, explique brevemente qué esperar el primer día y oriente sobre a quién
contactar para dudas iniciales.

Formato:
- Extensión: 180–220 palabras
- Estructura: párrafo de bienvenida, párrafo de información práctica del primer día,
  párrafo de cierre motivacional
- Encabezado formal con lugar, fecha y destinatario
- Firma ficticia: "Lic. Carmen Solís, Gerente de Recursos Humanos"
- Idioma: español formal, tono cálido y profesional

Evidencias y criterios:
- Menciona al menos dos prestaciones de ley conforme a la LFT
- Señala con [SUPUESTO] cualquier información que hayas inferido y no esté en el contexto

Cumplimiento y tono:
- Usa lenguaje inclusivo (evita asumir género en términos generales)
- No incluyas datos personales reales
- No hagas promesas de empleo indefinido ni garantías no contempladas en la LFT
```

**1.4 — Guardar y comparar versiones**

Copia la respuesta mejorada en un nuevo documento llamado `Carta_Bienvenida_v2.docx` y guárdalo en `Practica_01/Documentos_Generados/`.

**1.5 — Registrar el prompt en el repositorio**

Abre `Repositorio_Prompts_P01.docx` y agrega una fila con los siguientes datos:

| ID Prompt | Tipo de Documento | Versión | Fecha | Propósito | Notas de Ajuste |
|---|---|---|---|---|---|
| P01-001 | Carta de Bienvenida | v2 | [fecha actual] | Onboarding de nuevo colaborador | Se añadió RCTF-EC completo; se eliminó ambigüedad de género; se incluyeron prestaciones LFT |

#### Resultado Esperado

La versión v2 debe producir una carta con:
- Encabezado formal (ciudad, fecha, nombre y puesto del destinatario).
- Tres párrafos bien diferenciados (bienvenida, primer día, cierre).
- Mención explícita de al menos dos prestaciones de ley.
- Firma ficticia de la Gerente de RR.HH.
- Ausencia de promesas laborales no fundamentadas.
- Marcas `[SUPUESTO]` donde Copilot haya inferido información.

#### Verificación

✅ La carta v2 tiene entre 180 y 220 palabras.
✅ Contiene lenguaje inclusivo (sin asumir género).
✅ Menciona prestaciones conforme a la LFT.
✅ El archivo está guardado en OneDrive en la ruta correcta.
✅ El prompt v2 está registrado en `Repositorio_Prompts_P01.docx`.

---

### Paso 2: Aviso de Modificación de Condiciones de Trabajo

**Objetivo del paso:** Generar un aviso formal de modificación de condiciones laborales aplicando los requisitos legales del Artículo 51 y relacionados de la LFT, utilizando la técnica de *chain-of-thought* para que Copilot razone los elementos legales antes de redactar.

#### Instrucciones

**2.1 — Construir el prompt con técnica chain-of-thought**

En Copilot Chat (puedes iniciar un nuevo hilo o continuar el anterior), escribe el siguiente prompt:

```text
Rol y audiencia:
Soy HRBP (HR Business Partner) de una empresa de servicios de tecnología en México.
El aviso está dirigido a todos los colaboradores del área de Desarrollo de Software.

Contexto y datos:
- Empresa ficticia: "TechSoluciones S.A. de C.V."
- Cambio: modificación del horario de trabajo
  · Horario actual: lunes a viernes, 9:00–18:00 h (1 h de comida)
  · Nuevo horario: lunes a viernes, 8:00–17:00 h (1 h de comida)
  · Vigencia: a partir del día 1 del próximo mes
- Motivo: optimización de operaciones con clientes en zona horaria del Este (EE.UU.)
- Total de horas semanales: sin cambio (40 h/semana)

Tarea:
PASO 1 — Antes de redactar, lista los elementos legales mínimos que debe contener
un aviso de modificación de condiciones de trabajo conforme a la Ley Federal del
Trabajo mexicana. Cita los artículos relevantes.

PASO 2 — Con base en esa lista, redacta el aviso formal incluyendo todos los
elementos identificados.

Formato:
- Aviso en español formal, extensión 200–250 palabras
- Estructura: encabezado institucional, antecedentes, descripción del cambio,
  vigencia, firma de RR.HH. y espacio para acuse de recibo del colaborador
- Incluye una tabla de comparación: "Condición anterior vs. Nueva condición"

Evidencias y criterios:
- Cita los artículos de la LFT utilizados en el pie del documento
- Señala con [VERIFICAR CON LEGAL] cualquier afirmación que requiera validación jurídica

Cumplimiento y tono:
- Tono institucional y respetuoso
- No uses datos personales reales
- No incluyas cláusulas que puedan interpretarse como renuncia de derechos
```

**2.2 — Evaluar el razonamiento legal de Copilot**

Revisa el "PASO 1" de la respuesta (la lista de elementos legales). Verifica que Copilot haya mencionado elementos como:
- Notificación por escrito al trabajador.
- Plazo de aviso previo.
- Acuse de recibo.
- Referencia a artículos de la LFT.

> 📌 **Nota del instructor**: Los artículos específicos de la LFT pueden variar según la versión vigente. Verifica siempre en el Diario Oficial de la Federación (DOF) la versión actualizada antes de usar este documento en situaciones reales.

**2.3 — Aplicar follow-up prompt si la respuesta es incompleta**

Si el aviso generado no incluye el espacio de acuse de recibo o la tabla comparativa, usa este *follow-up prompt*:

```text
El aviso está bien, pero necesito dos ajustes:
1. Agrega al final una sección de "Acuse de Recibo" con campos para: nombre completo
   del colaborador, número de empleado, firma y fecha.
2. Asegúrate de que la tabla comparativa "Condición anterior vs. Nueva condición"
   esté incluida con formato de tabla Markdown.
Mantén el resto del documento sin cambios.
```

**2.4 — Guardar el documento**

Guarda la versión final como `Aviso_Modificacion_Condiciones_v1.docx` en `Practica_01/Documentos_Generados/`.

**2.5 — Registrar en el repositorio**

Agrega el prompt al `Repositorio_Prompts_P01.docx` con ID `P01-002`.

#### Resultado Esperado

El aviso debe contener:
- Lista de elementos legales de la LFT (PASO 1 del chain-of-thought).
- Documento formal con encabezado, descripción del cambio y vigencia.
- Tabla comparativa de condiciones.
- Sección de acuse de recibo.
- Citas de artículos de la LFT al pie del documento.
- Marcas `[VERIFICAR CON LEGAL]` donde aplique.

#### Verificación

✅ Copilot ejecutó los dos pasos del chain-of-thought en orden.
✅ El aviso cita artículos de la LFT (aunque requieran verificación profesional).
✅ La tabla comparativa está presente y legible.
✅ El espacio de acuse de recibo está incluido.
✅ El prompt y el documento están guardados y registrados.

---

### Paso 3: Carta de Reconocimiento por Desempeño

**Objetivo del paso:** Generar una carta de reconocimiento laboral utilizando la técnica *few-shot* (ejemplos de entrada/salida) para inducir el estilo, tono y estructura deseados en Copilot Chat.

#### Instrucciones

**3.1 — Construir el prompt con few-shot examples**

```text
Rol y audiencia:
Soy Director de Operaciones de una empresa de logística en México.
La carta es para un colaborador del área de Distribución.

Contexto y datos:
- Empresa ficticia: "LogiMex Distribución S.A. de C.V."
- Colaborador ficticio: Jordan Reyes, Coordinador de Distribución
- Logro específico: redujo el tiempo promedio de entrega en su ruta en un 18%
  durante el trimestre Q3, logrando cero quejas de clientes en ese período
- La empresa tiene un programa de reconocimiento trimestral llamado "Estrella LogiMex"

Tarea:
Redacta una carta de reconocimiento por desempeño para Jordan Reyes.

A continuación te doy un ejemplo del estilo y estructura que busco:

--- EJEMPLO DE REFERENCIA (no uses este contenido, solo el estilo) ---
Ciudad de México, [fecha]

Estimado/a [Nombre]:
Es un honor para [Empresa] reconocer su destacada contribución durante este período.
Su compromiso con [logro específico] ha tenido un impacto directo en [resultado medible].
Este reconocimiento es parte de nuestro programa [nombre del programa] y refleja
los valores que nos distinguen como organización.
Felicitamos a [Nombre] por este logro y lo/la invitamos a continuar siendo ejemplo
para su equipo.
Atentamente,
[Nombre y cargo del firmante]
--- FIN DEL EJEMPLO ---

Formato:
- Extensión: 150–180 palabras
- Tono: formal, cálido, motivacional
- Estructura idéntica al ejemplo de referencia
- Idioma: español formal
- Firma ficticia: "Ing. Roberto Fuentes, Director de Operaciones"

Evidencias y criterios:
- Menciona el logro cuantificable (18% de reducción, cero quejas)
- Referencia explícita al programa "Estrella LogiMex"
- Señala con [SUPUESTO] cualquier información inferida

Cumplimiento y tono:
- Lenguaje inclusivo (usa formas neutras o ambas formas cuando sea necesario)
- No incluyas referencias a compensaciones económicas ni promesas de ascenso
- No menciones atributos personales no laborales
```

**3.2 — Evaluar fidelidad al ejemplo de referencia**

Compara la carta generada con el ejemplo de referencia. Verifica:
- ¿Sigue la misma estructura de párrafos?
- ¿Menciona el logro cuantificable?
- ¿Hace referencia al programa de reconocimiento?
- ¿Usa lenguaje inclusivo?

**3.3 — Aplicar refinamiento si es necesario**

Si la carta no usa lenguaje inclusivo o no menciona el dato cuantitativo, usa este *follow-up*:

```text
Por favor ajusta la carta con dos cambios:
1. Asegúrate de que el logro cuantificable (18% de reducción en tiempo de entrega
   y cero quejas) esté mencionado explícitamente en el segundo párrafo.
2. Reemplaza cualquier pronombre de género por formas neutras o ambas formas
   (ej.: "su desempeño" en lugar de "su trabajo como él/ella").
Mantén el resto sin cambios.
```

**3.4 — Guardar y registrar**

Guarda como `Carta_Reconocimiento_v1.docx` en `Practica_01/Documentos_Generados/` y registra el prompt en el repositorio con ID `P01-003`.

#### Resultado Esperado

La carta debe:
- Seguir la estructura del ejemplo de referencia (3 párrafos + firma).
- Mencionar el 18% de reducción y cero quejas.
- Hacer referencia al programa "Estrella LogiMex".
- Tener entre 150 y 180 palabras.
- Usar lenguaje inclusivo.

#### Verificación

✅ La estructura coincide con el ejemplo de referencia.
✅ El logro cuantificable está explícito.
✅ El programa de reconocimiento está mencionado.
✅ No hay promesas de compensación o ascenso.
✅ Documento y prompt guardados y registrados.

---

### Paso 4: Comunicado Interno sobre Actualización de Política de Asistencia

**Objetivo del paso:** Generar un comunicado interno corporativo para todos los empleados, aplicando la técnica de variables parametrizadas `{{variable}}` para crear una plantilla reutilizable, e incorporando una sección de preguntas frecuentes (FAQ).

#### Instrucciones

**4.1 — Construir el prompt con plantilla parametrizada**

```text
Rol y audiencia:
Soy especialista de Relaciones Laborales. El comunicado es para todos los
colaboradores de planta y administrativos de la empresa.

Contexto y datos:
- Empresa ficticia: "Grupo Industrial Bajío S.A. de C.V."
- Cambio en política: actualización de la política de registro de asistencia
  · Nuevo sistema: registro biométrico (huella dactilar) en sustitución de tarjeta
  · Fecha de implementación: primer día del próximo mes
  · Tolerancia de llegada: 10 minutos (sin cambio)
  · Consecuencias de 3 retardos injustificados en un mes: llamada de atención por escrito
  · Consecuencias de 3 faltas injustificadas en 30 días: proceso disciplinario conforme a LFT
- El comunicado debe ser aplicable a todas las plantas (Monterrey, Guadalajara, CDMX)

Tarea:
1. Redacta un comunicado interno formal anunciando la actualización de la política.
2. Genera un FAQ de 5 preguntas y respuestas para los colaboradores.
3. Al final, proporciona la versión del prompt como PLANTILLA PARAMETRIZADA,
   reemplazando los datos específicos de esta empresa con variables entre llaves
   dobles: {{nombre_empresa}}, {{tipo_cambio}}, {{fecha_implementacion}}, etc.

Formato:
- Comunicado: 180–220 palabras, estructura formal con encabezado, cuerpo y cierre
- FAQ: 5 preguntas en formato "P:" y "R:" con respuestas de máximo 2 oraciones
- Plantilla parametrizada: al final, en un bloque de código separado
- Idioma: español formal

Evidencias y criterios:
- El comunicado debe mencionar el fundamento legal de las consecuencias disciplinarias
  (referencia a la LFT, aunque sea genérica)
- Señala con [VERIFICAR CON LEGAL] las consecuencias disciplinarias mencionadas
- Indica si hay información que deba adaptarse por planta

Cumplimiento y tono:
- Tono institucional y respetuoso, no amenazante
- Lenguaje inclusivo
- No uses datos personales reales
- Evita lenguaje que pueda interpretarse como intimidatorio o discriminatorio
```

**4.2 — Revisar el FAQ generado**

Verifica que las cinco preguntas del FAQ cubran aspectos prácticos relevantes, por ejemplo:
- ¿Qué pasa si el lector biométrico no reconoce mi huella?
- ¿Cómo se registran las llegadas tardías por causas de fuerza mayor?
- ¿Dónde puedo consultar la política completa?
- ¿Qué sucede durante el período de transición?
- ¿A quién contacto si tengo dudas?

Si alguna de estas preguntas no está incluida y consideras que es relevante, usa un *follow-up prompt*:

```text
Por favor agrega al FAQ la siguiente pregunta adicional:
P: ¿Qué procedimiento debo seguir si el sistema biométrico no reconoce mi huella?
R: [genera una respuesta breve y práctica de máximo 2 oraciones]
```

**4.3 — Extraer y guardar la plantilla parametrizada**

Copia el bloque de plantilla parametrizada que Copilot generó al final de su respuesta. Pégalo en un nuevo documento llamado `Plantilla_Comunicado_Asistencia.docx` en `Practica_01/Repositorio_Prompts/`.

**4.4 — Guardar el comunicado completo**

Guarda el comunicado y FAQ como `Comunicado_Politica_Asistencia_v1.docx` en `Practica_01/Documentos_Generados/`. Registra el prompt en el repositorio con ID `P01-004`.

#### Resultado Esperado

La respuesta debe incluir:
- Comunicado formal de 180–220 palabras con encabezado, cuerpo y cierre.
- FAQ con exactamente 5 preguntas y respuestas concisas.
- Plantilla parametrizada con variables `{{variable}}` en bloque de código separado.
- Referencias a la LFT (aunque genéricas) para las consecuencias disciplinarias.
- Marcas `[VERIFICAR CON LEGAL]` en secciones disciplinarias.

#### Verificación

✅ El comunicado tiene entre 180 y 220 palabras.
✅ El FAQ contiene 5 preguntas con respuestas de máximo 2 oraciones cada una.
✅ La plantilla parametrizada usa variables `{{variable}}` correctamente.
✅ Las consecuencias disciplinarias están marcadas con `[VERIFICAR CON LEGAL]`.
✅ Todos los archivos están guardados en las rutas correctas de OneDrive.

---

### Paso 5: Traducción al Inglés de una Carta de Oferta de Empleo

**Objetivo del paso:** Generar una traducción profesional al inglés de una carta de oferta de empleo, evaluando la fidelidad terminológica en contextos de Relaciones Laborales y aplicando un prompt de evaluación crítica de la traducción.

#### Instrucciones

**5.1 — Preparar el documento fuente en español**

Usa el siguiente texto ficticio como carta de oferta en español. Cópialo en tu hilo de Copilot Chat como parte del prompt:

```text
--- DOCUMENTO FUENTE (Carta de Oferta de Empleo en Español) ---
Ciudad de México, [fecha ficticia]

Estimada Sra. Valeria Ortiz:

Por medio de la presente, Servicios Empresariales Centrales S.A. de C.V.
(en adelante "la Empresa") tiene el agrado de extenderle una oferta formal de empleo
para ocupar el puesto de Gerente de Proyectos Tecnológicos, adscrita a la Dirección
de Transformación Digital.

Las condiciones de la oferta son las siguientes:
- Salario mensual bruto: $45,000 MXN (cuarenta y cinco mil pesos mexicanos)
- Tipo de contrato: por tiempo indeterminado, conforme al Artículo 35 de la LFT
- Fecha de inicio: a convenir entre las partes
- Prestaciones de ley: IMSS, INFONAVIT, vacaciones, prima vacacional y aguinaldo
- Prestaciones superiores a las de ley: seguro de gastos médicos mayores, fondo
  de ahorro del 13% y vales de despensa

Esta oferta está sujeta a la satisfactoria conclusión del proceso de verificación
de referencias y antecedentes.

Esperamos contar con su valiosa incorporación a nuestro equipo.

Atentamente,
Lic. Fernando Castillo
Director de Recursos Humanos
Servicios Empresariales Centrales S.A. de C.V.
--- FIN DEL DOCUMENTO FUENTE ---
```

**5.2 — Construir el prompt de traducción con evaluación crítica**

```text
Rol y audiencia:
Soy especialista de RR.HH. en una empresa mexicana con operaciones internacionales.
La traducción es para enviarla a una candidata extranjera (hablante nativa de inglés
de EE.UU.) que requiere la oferta en inglés para sus trámites migratorios.

Contexto y datos:
El documento fuente es la carta de oferta de empleo incluida arriba.

Tarea:
PARTE 1 — Traduce la carta al inglés profesional (American English), manteniendo
el formato original y la equivalencia terminológica en Relaciones Laborales.

PARTE 2 — Genera una tabla de análisis terminológico con las siguientes columnas:
| Término en español | Traducción utilizada | Alternativa(s) | Nota de contexto |

Incluye en la tabla al menos 8 términos técnicos de RR.HH. o legales de la carta
(ej.: "salario mensual bruto", "prestaciones de ley", "contrato por tiempo
indeterminado", "prima vacacional", "aguinaldo", etc.)

PARTE 3 — Señala cualquier concepto del sistema laboral mexicano que NO tenga
equivalente directo en el sistema laboral de EE.UU. y sugiere una nota aclaratoria
entre paréntesis en la traducción.

Formato:
- Parte 1: carta en inglés con el mismo formato que el original
- Parte 2: tabla Markdown con 4 columnas
- Parte 3: lista de conceptos sin equivalente con nota aclaratoria sugerida
- Idioma de la traducción: American English formal

Evidencias y criterios:
- Las equivalencias terminológicas deben ser apropiadas para un contexto laboral
  formal en EE.UU. (no traducciones literales)
- Señala con [REVISAR] los términos donde la traducción pueda ser ambigua

Cumplimiento y tono:
- No modifiques el contenido legal ni las condiciones de la oferta
- Mantén los montos en MXN con nota aclaratoria de la divisa
- No incluyas datos personales reales
```

**5.3 — Evaluar la fidelidad terminológica**

Revisa la tabla de análisis terminológico generada en la PARTE 2. Presta especial atención a:

- **"Aguinaldo"**: ¿Copilot usó "Christmas bonus" o "year-end bonus"? ¿Incluyó nota aclaratoria?
- **"Prima vacacional"**: ¿Usó "vacation premium" o "holiday bonus"? ¿Es comprensible para un lector anglosajón?
- **"Contrato por tiempo indeterminado"**: ¿Usó "indefinite-term employment contract"? ¿Añadió la nota sobre el Artículo 35 de la LFT?
- **"IMSS" e "INFONAVIT"**: ¿Copilot explicó qué son estas instituciones para el lector extranjero?

**5.4 — Aplicar follow-up para mejorar la tabla terminológica**

Si la tabla tiene menos de 8 términos o falta alguno importante, usa este *follow-up*:

```text
Por favor amplía la tabla terminológica para incluir los siguientes términos
que no están en la versión actual:
- "fondo de ahorro"
- "vales de despensa"
- "verificación de antecedentes"
Para cada uno, proporciona la traducción utilizada, al menos una alternativa y
una nota de contexto que explique la diferencia cultural o legal relevante.
```

**5.5 — Guardar y registrar**

Guarda la traducción completa (carta + tabla + notas) como `Traduccion_Carta_Oferta_EN_v1.docx` en `Practica_01/Documentos_Generados/`. Registra el prompt en el repositorio con ID `P01-005`.

#### Resultado Esperado

La respuesta debe incluir:
- Carta de oferta traducida al inglés americano formal con el mismo formato que el original.
- Tabla terminológica con al menos 8 términos técnicos de RR.HH./legales.
- Lista de conceptos sin equivalente en EE.UU. con notas aclaratorias.
- Montos en MXN con nota de divisa.
- Marcas `[REVISAR]` en términos ambiguos.

#### Verificación

✅ La carta traducida mantiene el formato y estructura del original en español.
✅ La tabla terminológica tiene al menos 8 términos con las 4 columnas requeridas.
✅ "Aguinaldo", "prima vacacional", "IMSS" e "INFONAVIT" tienen notas aclaratorias.
✅ Los montos en MXN están conservados con nota de divisa.
✅ Todos los archivos están guardados y el prompt registrado.

---

### Paso 6: Compilación del Mini-Repositorio de Prompts

**Objetivo del paso:** Consolidar los cinco prompts desarrollados durante la práctica en un repositorio estructurado y reutilizable, aplicando la técnica de plantillas parametrizadas con variables `{{variable}}`.

#### Instrucciones

**6.1 — Completar la tabla del repositorio**

Abre `Repositorio_Prompts_P01.docx` y verifica que las cinco entradas estén completas:

| ID Prompt | Tipo de Documento | Versión | Fecha | Propósito | Notas de Ajuste |
|---|---|---|---|---|---|
| P01-001 | Carta de Bienvenida | v2 | [fecha] | Onboarding | RCTF-EC completo; lenguaje inclusivo |
| P01-002 | Aviso Modificación Condiciones | v1 | [fecha] | Cambio horario | Chain-of-thought; citas LFT |
| P01-003 | Carta de Reconocimiento | v1 | [fecha] | Reconocimiento desempeño | Few-shot; logro cuantificable |
| P01-004 | Comunicado Política Asistencia | v1 | [fecha] | Actualización política | Plantilla parametrizada; FAQ |
| P01-005 | Traducción Carta Oferta | v1 | [fecha] | Traducción ES→EN | Tabla terminológica; notas culturales |

**6.2 — Crear una sección de "Lecciones Aprendidas"**

Al final del documento `Repositorio_Prompts_P01.docx`, agrega una sección con el título **"Lecciones Aprendidas"** y responde brevemente las siguientes preguntas (3–5 oraciones por respuesta):

1. ¿Cuál fue la diferencia más notable entre el prompt genérico (Paso 1.1) y el prompt RCTF-EC (Paso 1.3)?
2. ¿En qué momento fue más útil la técnica de *chain-of-thought*?
3. ¿Qué términos laborales mexicanos presentaron mayor dificultad de traducción y por qué?

**6.3 — Usar Copilot para generar una versión parametrizada universal**

En Copilot Chat, usa el siguiente prompt para obtener una plantilla maestra parametrizada:

```text
Rol y audiencia:
Soy especialista de RR.HH. construyendo un repositorio de prompts reutilizables.

Tarea:
Toma el siguiente prompt de carta de bienvenida y conviértelo en una PLANTILLA
PARAMETRIZADA UNIVERSAL. Reemplaza todos los datos específicos por variables
entre dobles llaves: {{nombre_empresa}}, {{nombre_colaborador}}, {{puesto}},
{{area}}, {{fecha_ingreso}}, {{prestaciones}}, {{contacto_rrhh}},
{{nombre_firmante}}, {{cargo_firmante}}.

Incluye al final una tabla de "Guía de variables" con: Variable | Descripción | Ejemplo.

[Pega aquí el prompt completo del Paso 1.3]
```

Guarda la plantilla maestra como `Plantilla_Maestra_Bienvenida.docx` en `Practica_01/Repositorio_Prompts/`.

**6.4 — Verificar la estructura final de OneDrive**

Confirma que la carpeta `Practica_01/` contiene:

```
Practica_01/
├── Prompts/
│   (vacío o con capturas de pantalla opcionales)
├── Documentos_Generados/
│   ├── Carta_Bienvenida_v1.docx
│   ├── Carta_Bienvenida_v2.docx
│   ├── Aviso_Modificacion_Condiciones_v1.docx
│   ├── Carta_Reconocimiento_v1.docx
│   ├── Comunicado_Politica_Asistencia_v1.docx
│   └── Traduccion_Carta_Oferta_EN_v1.docx
└── Repositorio_Prompts/
    ├── Repositorio_Prompts_P01.docx
    ├── Plantilla_Comunicado_Asistencia.docx
    └── Plantilla_Maestra_Bienvenida.docx
```

#### Resultado Esperado

- Tabla del repositorio completa con los 5 prompts documentados.
- Sección de "Lecciones Aprendidas" con reflexiones propias.
- Plantilla maestra parametrizada con tabla de guía de variables.
- Estructura de carpetas completa y organizada en OneDrive.

#### Verificación

✅ Los 5 prompts están registrados en la tabla con todos los campos.
✅ La sección "Lecciones Aprendidas" tiene al menos 3 respuestas documentadas.
✅ La plantilla maestra usa variables `{{variable}}` en todos los campos específicos.
✅ La estructura de carpetas en OneDrive está completa.

---

## Validación y Pruebas

Al finalizar todos los pasos, realiza las siguientes verificaciones globales para confirmar que los objetivos de la práctica han sido alcanzados:

### Lista de verificación final

| # | Criterio de validación | Estado |
|---|---|---|
| 1 | Generé 5 documentos laborales distintos usando Copilot Chat | ☐ |
| 2 | Apliqué la plantilla RCTF-EC completa en al menos 3 prompts | ☐ |
| 3 | Usé al menos 3 técnicas diferentes (chain-of-thought, few-shot, parametrización) | ☐ |
| 4 | Apliqué al menos 2 follow-up prompts de refinamiento iterativo | ☐ |
| 5 | Todos los documentos usan datos ficticios (sin datos reales de empleados) | ☐ |
| 6 | Los documentos laborales incluyen referencias a la LFT donde corresponde | ☐ |
| 7 | Los documentos con implicaciones legales están marcados con [VERIFICAR CON LEGAL] | ☐ |
| 8 | La traducción incluye tabla terminológica con al menos 8 términos técnicos | ☐ |
| 9 | El repositorio de prompts está completo con los 5 registros | ☐ |
| 10 | La estructura de carpetas en OneDrive está organizada correctamente | ☐ |

### Prueba de reutilización de plantilla (opcional — 5 minutos adicionales)

Para confirmar que tus plantillas parametrizadas son verdaderamente reutilizables, toma la `Plantilla_Maestra_Bienvenida.docx` y reemplaza las variables con un nuevo escenario ficticio diferente al del Paso 1. Pega el prompt resultante en Copilot Chat y verifica que genera una carta coherente y diferente a la versión original.

---

## Solución de Problemas

### Problema 1: Copilot genera respuestas genéricas o ignora partes del prompt

**Síntoma:** La respuesta de Copilot no sigue la estructura RCTF-EC, omite secciones solicitadas (como la tabla comparativa o el FAQ), o produce texto genérico sin personalización para el escenario ficticio proporcionado.

**Causa probable:** El prompt es demasiado largo para ser procesado de manera uniforme, o los bloques de instrucción no están claramente delimitados. Copilot puede perder el hilo de instrucciones cuando el prompt supera cierta longitud sin separadores claros.

**Solución:**
1. Divide el prompt en partes más cortas usando separadores claros como `---` entre secciones.
2. Numera explícitamente cada tarea: `TAREA 1:`, `TAREA 2:`, `TAREA 3:`.
3. Usa un *follow-up prompt* específico para la sección omitida en lugar de reescribir todo el prompt:
   ```text
   En tu respuesta anterior omitiste la tabla comparativa solicitada.
   Por favor genera SOLO esa tabla con las columnas: "Condición anterior" y
   "Nueva condición", usando los datos del contexto que ya te proporcioné.
   ```
4. Si el problema persiste, inicia un nuevo hilo de conversación con un prompt más corto y enfocado en una sola tarea a la vez.

---

### Problema 2: La traducción al inglés produce términos literales o culturalmente incorrectos

**Síntoma:** Copilot traduce "aguinaldo" como "bonus" sin contexto, "prima vacacional" como "vacation premium" sin explicación, o usa términos propios del sistema laboral de EE.UU. que no aplican al contexto mexicano (como "at-will employment").

**Causa probable:** Sin instrucciones explícitas sobre el contexto legal mexicano vs. estadounidense, Copilot puede priorizar traducciones literales o términos más comunes en inglés que no reflejan la equivalencia conceptual correcta.

**Solución:**
1. Usa este *follow-up prompt* correctivo:
   ```text
   Por favor revisa la traducción de los siguientes términos. Para cada uno,
   proporciona la traducción más apropiada para un contexto laboral MEXICANO
   explicado a un lector anglosajón de EE.UU., incluyendo una nota aclaratoria
   entre paréntesis que explique el concepto:
   - aguinaldo
   - prima vacacional
   - IMSS
   - INFONAVIT
   - contrato por tiempo indeterminado (Art. 35 LFT)
   ```
2. Especifica en el prompt original el público objetivo y el propósito de la traducción (trámites migratorios, negociación internacional, etc.), ya que esto orienta a Copilot hacia traducciones más contextualizadas.
3. Valida los términos técnicos con un glosario bilingüe de RR.HH. o con un profesional de Relaciones Laborales con experiencia internacional antes de enviar el documento.

---

## Limpieza del Entorno

Al finalizar la práctica, realiza los siguientes pasos para dejar el entorno ordenado:

**1. Verificar y organizar archivos en OneDrive**

Confirma que todos los documentos generados están guardados en las carpetas correctas dentro de `OneDrive/Curso_Copilot_RRHH/Practica_01/`. Elimina cualquier archivo duplicado o borrador sin nombre.

**2. Cerrar hilos de conversación en Copilot Chat**

No es necesario eliminar los hilos de conversación de Copilot Chat, pero se recomienda:
- Anotar el enlace o nombre del hilo en el `Repositorio_Prompts_P01.docx` para referencia futura.
- Evitar dejar información sensible o confidencial en hilos activos.

**3. Verificar que no se usaron datos reales**

Revisa rápidamente los documentos generados y confirma que ninguno contiene:
- Nombres reales de empleados de tu organización.
- CURP, RFC, salarios reales o números de seguridad social.
- Información confidencial de la empresa.

Si encontraras algún dato real accidentalmente ingresado, elimina el documento y notifica a tu instructor.

**4. Compartir el repositorio con el instructor (si aplica)**

Si el instructor solicitó la entrega de los entregables, comparte la carpeta `Practica_01/` desde OneDrive usando el botón "Compartir" y proporcionando el enlace al instructor. Asegúrate de que los permisos sean "Solo lectura".

---

## Resumen

### Logros de la práctica

En esta práctica aplicaste la plantilla **RCTF-EC** para construir prompts estructurados y generar cinco tipos de documentos laborales de uso cotidiano en Recursos Humanos: carta de bienvenida, aviso de modificación de condiciones, carta de reconocimiento, comunicado de política interna y traducción profesional. Practicaste tres técnicas clave de ingeniería de prompts: *chain-of-thought* para razonamiento legal paso a paso, *few-shot examples* para inducir estilo y estructura, y *plantillas parametrizadas* para crear activos reutilizables.

### Conceptos clave reforzados

| Concepto | Aplicación en la práctica |
|---|---|
| Plantilla RCTF-EC | Estructura base de todos los prompts (Pasos 1–5) |
| Chain-of-thought | Razonamiento legal en dos pasos (Paso 2) |
| Few-shot examples | Inducción de estilo en carta de reconocimiento (Paso 3) |
| Refinamiento iterativo | Follow-up prompts en todos los pasos |
| Plantillas parametrizadas | Comunicado de asistencia y plantilla maestra (Pasos 4 y 6) |
| Verificación legal | Marcas `[VERIFICAR CON LEGAL]` y `[SUPUESTO]` |
| Fidelidad terminológica | Tabla de análisis en traducción (Paso 5) |

### Recordatorio crítico

> ⚠️ Ninguno de los documentos generados en esta práctica debe utilizarse en situaciones laborales reales sin revisión previa por un **profesional legal certificado en derecho laboral mexicano**. La LFT puede haber sufrido modificaciones; verifica siempre la versión vigente en el [Diario Oficial de la Federación (DOF)](https://www.dof.gob.mx).

### Recursos adicionales

| Recurso | Descripción | Enlace |
|---|---|---|
| Microsoft Learn — Prompt Engineering | Conceptos de ingeniería de prompts en Azure OpenAI | [https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/prompt-engineering](https://learn.microsoft.com/en-us/azure/ai-services/openai/concepts/prompt-engineering) |
| Microsoft 365 Copilot Overview | Descripción general de Copilot para empresas | [https://learn.microsoft.com/en-us/microsoft-365-copilot/microsoft-365-copilot-overview](https://learn.microsoft.com/en-us/microsoft-365-copilot/microsoft-365-copilot-overview) |
| OpenAI — Prompt Engineering Guide | Guía oficial de ingeniería de prompts | [https://platform.openai.com/docs/guides/prompt-engineering](https://platform.openai.com/docs/guides/prompt-engineering) |
| Diario Oficial de la Federación | Versión vigente de la LFT | [https://www.dof.gob.mx](https://www.dof.gob.mx) |
| AEPD — Protección de datos laborales | Guía sobre protección de datos en relaciones laborales | [https://www.aepd.es/sites/default/files/2019-09/guia-relaciones-laborales.pdf](https://www.aepd.es/sites/default/files/2019-09/guia-relaciones-laborales.pdf) |
| SHRM — Generative AI in HR | Cómo RR.HH. puede usar IA generativa | [https://www.shrm.org/resourcesandtools/hr-topics/technology/pages/how-hr-can-use-generative-ai.aspx](https://www.shrm.org/resourcesandtools/hr-topics/technology/pages/how-hr-can-use-generative-ai.aspx) |

---

*Fin del Laboratorio 01-00-01*
