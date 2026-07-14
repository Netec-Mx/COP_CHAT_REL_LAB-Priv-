# Consultoría interactiva de la LFT para la toma de decisiones

## 1. Metadatos

| Atributo | Detalle |
|---|---|
| **Duración estimada** | 90 minutos |
| **Complejidad** | Alta (Hard) |
| **Nivel Bloom** | Aplicar (Apply) |
| **Módulo** | Módulo 3 — Interpretación normativa asistida por IA |
| **Práctica número** | 03-00-01 |
| **Versión del documento** | 1.0 |
| **Última revisión** | 2025 |

---

> ⚠️ **ADVERTENCIA LEGAL CRÍTICA**
>
> Copilot Chat es una herramienta de apoyo y productividad. **NO sustituye la asesoría jurídico-laboral certificada.** Todos los documentos, interpretaciones y análisis generados durante esta práctica son de carácter pedagógico y deben ser revisados por un profesional legal antes de cualquier implementación en situaciones reales.

> 🔒 **PRIVACIDAD DE DATOS**
>
> **Está estrictamente prohibido** ingresar datos reales de empleados (nombres, CURP, RFC, salarios, números de expediente) en Copilot Chat. Todos los ejercicios utilizan datos ficticios proporcionados por el instructor. Verifique la política de privacidad de su organización antes de usar herramientas de IA generativa.

---

## 2. Descripción General

En esta práctica, el participante asumirá el rol de **asesor de Relaciones Laborales** que debe resolver seis casos laborales de complejidad creciente utilizando **Microsoft 365 Copilot Chat** como herramienta de consultoría normativa interactiva. Cada caso requiere formular prompts con contexto legal específico, recuperar artículos aplicables de la Ley Federal del Trabajo (LFT), evaluar críticamente las respuestas de Copilot contra el texto oficial y documentar cuándo la situación requiere escalamiento a asesoría legal profesional. La práctica aplica directamente el enfoque **"citas primero"** y la arquitectura de razonamiento jurídico (legal reasoning prompts) estudiados en la Lección 3.1, y concluye con la construcción de una **Guía de Consulta Rápida LFT con Copilot** personalizada para el área de RR.HH.

---

## 3. Objetivos de Aprendizaje

Al finalizar esta práctica, el participante será capaz de:

- [ ] Formular prompts de razonamiento jurídico (legal reasoning prompts) que obligan a Copilot Chat a citar artículos específicos de la LFT, distinguir norma de guía orientativa e identificar ambigüedades en cada caso laboral planteado.
- [ ] Analizar y comparar las respuestas de Copilot con el texto oficial de la LFT para seis casos prácticos (rescisión, tipos de contrato, horas extra, modificación unilateral de condiciones, baja voluntaria vs. abandono, y caso integrador).
- [ ] Evaluar críticamente las respuestas de Copilot, identificando imprecisiones, lagunas legales, supuestos no declarados y necesidad de escalamiento a asesoría legal especializada.
- [ ] Construir un flujo documentado de toma de decisiones asistido por IA para situaciones laborales complejas, incluyendo los artículos LFT relevantes en cada etapa.
- [ ] Producir una **Guía de Consulta Rápida LFT con Copilot** en Microsoft Word que pueda reutilizarse como referencia operativa en el área de RR.HH.

---

## 4. Prerrequisitos

### 4.1 Conocimientos Previos

| Requisito | Nivel requerido |
|---|---|
| Haber completado las Prácticas 1 y 2 del curso (o demostrar dominio equivalente de Copilot Chat) | Obligatorio |
| Conocimiento general de la estructura de la LFT y sus títulos principales | Obligatorio |
| Haber leído el material del Módulo 3 sobre interpretación normativa asistida por IA y sus limitaciones éticas y legales | Obligatorio |
| Experiencia mínima de 6 meses en funciones de Relaciones Laborales o Recursos Humanos | Recomendado |

### 4.2 Accesos y Materiales

| Recurso | Estado requerido |
|---|---|
| Licencia **Microsoft 365 Copilot** activa (no Copilot gratuito de Bing) | ✅ Verificado por TI con 48 h de anticipación |
| Acceso a **Microsoft 365 Copilot Chat** en [https://m365.cloud.microsoft/chat](https://m365.cloud.microsoft/chat) | ✅ Confirmado |
| **Microsoft Word** (Microsoft 365 Apps, versión 2301 o superior) | ✅ Instalado |
| PDF oficial de la LFT (proporcionado por el instructor o descargado de la fuente oficial) | ✅ Disponible localmente |
| Archivo de casos ficticios `Casos_LFT_Ficticios.docx` (proporcionado por el instructor) | ✅ Descargado en escritorio |
| Adobe Acrobat Reader o Microsoft Edge para visualizar el PDF de la LFT | ✅ Disponible |

---

## 5. Entorno de Laboratorio

### 5.1 Requisitos de Hardware

| Componente | Mínimo | Recomendado |
|---|---|---|
| Procesador | Intel Core i5 8ª gen / AMD Ryzen 5 | Intel Core i7 / AMD Ryzen 7 |
| Memoria RAM | 8 GB | 16 GB |
| Almacenamiento libre | 2 GB | 5 GB |
| Resolución de pantalla | 1366 × 768 | 1920 × 1080 |
| Conexión a Internet | 10 Mbps | 25 Mbps o superior |

### 5.2 Requisitos de Software

| Software | Versión mínima |
|---|---|
| Microsoft 365 Copilot Chat (empresarial) | Licencia M365 Copilot activa |
| Microsoft Word (Microsoft 365) | Versión 2301 o superior |
| Microsoft Edge o Google Chrome | Edge 120+ / Chrome 120+ |
| Adobe Acrobat Reader o Edge PDF Viewer | 2020 o superior |
| Microsoft OneDrive | Integrado con Microsoft 365 |

### 5.3 Configuración Inicial del Entorno

Realice los siguientes pasos **antes de iniciar la práctica**:

**Paso A — Verificar acceso a Copilot Chat empresarial:**

```
1. Abra Microsoft Edge o Google Chrome.
2. Navegue a: https://m365.cloud.microsoft/chat
3. Inicie sesión con su cuenta corporativa Microsoft 365.
4. Confirme que el encabezado muestra "Copilot" con el ícono de su organización
   (NO la versión gratuita de Bing Copilot).
5. Verifique que el modo esté configurado en "Trabajo" (Work), no "Web".
```

**Paso B — Preparar el documento de trabajo en Word:**

```
1. Abra Microsoft Word.
2. Cree un nuevo documento en blanco.
3. Guárdelo en OneDrive con el nombre:
   Practica3_[SusIniciales]_ConsultoriaLFT.docx
   Ejemplo: Practica3_JGM_ConsultoriaLFT.docx
4. Agregue un encabezado con: Nombre, Fecha, Práctica 3 — Consultoría LFT con Copilot.
5. Mantenga el documento abierto durante toda la práctica para registrar sus hallazgos.
```

**Paso C — Abrir el PDF de la LFT como referencia:**

```
1. Abra el archivo PDF de la LFT proporcionado por el instructor.
   (Fuente oficial: https://www.diputados.gob.mx/LeyesBiblio/pdf/LFT.pdf)
2. Ábralo en una segunda ventana o en una segunda pantalla si dispone de ella.
3. Tenga a mano los siguientes artículos para consulta rápida durante la práctica:
   - Arts. 35–39 (Tipos de contrato)
   - Arts. 46–55 (Rescisión de la relación de trabajo)
   - Arts. 47–48 (Causas de rescisión y liquidación)
   - Arts. 66–68 (Jornada extraordinaria)
   - Arts. 51–52 (Rescisión por causa imputable al patrón)
   - Arts. 53–55 (Terminación de la relación de trabajo)
```

---

## 6. Desarrollo Paso a Paso

> 📋 **Instrucción general:** Para cada caso, siga el ciclo de cuatro fases:
> 1. **Leer** el caso ficticio.
> 2. **Formular** el prompt en Copilot Chat usando la plantilla indicada.
> 3. **Analizar** la respuesta de Copilot comparándola con el PDF oficial de la LFT.
> 4. **Documentar** hallazgos, coincidencias, discrepancias y decisión de escalamiento en su documento Word.

---

### Paso 1 — Configuración de la Plantilla Base de Prompt Legal

**Objetivo:** Establecer la instrucción maestra (system-level prompt) que Copilot usará como marco de referencia para todos los casos de la práctica, aplicando el enfoque "citas primero" de la Lección 3.1.

#### Instrucciones

1. Abra **Microsoft 365 Copilot Chat** en su navegador ([https://m365.cloud.microsoft/chat](https://m365.cloud.microsoft/chat)).
2. Asegúrese de estar en el modo **"Trabajo" (Work)**.
3. Inicie una **nueva conversación** haciendo clic en el ícono de nueva sesión (lápiz o "+").
4. Copie y pegue el siguiente prompt de configuración inicial. Este es su **prompt de sistema** para toda la sesión:

```text
Actúa como un asistente especializado en cumplimiento laboral mexicano.
Tu función es interpretar la Ley Federal del Trabajo (LFT) de México
aplicada a casos prácticos de Recursos Humanos.

Reglas que debes seguir en TODAS tus respuestas:
1. Responde en español profesional, estructurado y conciso.
2. Cita SIEMPRE el artículo específico de la LFT que fundamenta tu respuesta,
   con el formato: [Art. XX, LFT — Título del capítulo].
3. Distingue claramente entre: NORMA (obligatorio por ley) y GUÍA (orientativo).
4. Declara explícitamente los supuestos que estás asumiendo para el caso.
5. Señala ambigüedades, lagunas legales o datos faltantes que afecten tu análisis.
6. Indica cuándo la situación REQUIERE ESCALAMIENTO a un abogado laboral.
7. NO inventes artículos ni cifras. Si no tienes certeza, indícalo claramente.
8. NO incluyas datos personales reales en ninguna circunstancia.
9. Cierra cada respuesta con una sección: "Acciones recomendadas para RR.HH."

¿Entendiste las reglas? Confirma con: "Listo. Estoy configurado como asistente
de cumplimiento laboral. Puedes presentar el primer caso."
```

5. Presione **Enter** y espere la confirmación de Copilot.
6. Capture una pantalla de la confirmación y péguela en su documento Word bajo el título **"Paso 1 — Configuración de sesión"**.

#### Resultado Esperado

Copilot debe responder confirmando las reglas y mostrando disposición para recibir el primer caso. Si Copilot no confirma adecuadamente o ignora las instrucciones, repita el prompt y verifique que está usando la versión empresarial (no la versión gratuita).

#### Verificación

- [ ] Copilot confirmó las reglas de la sesión.
- [ ] El modo "Trabajo" está activo (no "Web").
- [ ] La captura de pantalla está pegada en el documento Word.

---

### Paso 2 — Caso 1: Rescisión de Contrato (Justificada vs. Injustificada)

**Objetivo:** Utilizar Copilot para interpretar los Arts. 47 y 48 de la LFT aplicados a un caso de rescisión, y evaluar las implicaciones en el cálculo de liquidación.

#### Instrucciones

1. En la misma sesión de Copilot Chat, ingrese el siguiente prompt del **Caso 1**:

```text
CASO 1 — RESCISIÓN DE CONTRATO

Contexto ficticio:
La empresa "Manufacturas del Norte S.A. de C.V." (empresa ficticia) desea
rescindir el contrato de un trabajador llamado "Trabajador A" (dato ficticio)
que tiene 5 años de antigüedad, jornada diurna y salario mensual de $15,000 MXN
(dato ficticio). El motivo alegado por la empresa es "bajo rendimiento y
faltas injustificadas repetidas" sin haber levantado actas administrativas previas.

Preguntas:
1. ¿Cuáles son las causas de rescisión justificada según la LFT y cuáles aplican
   a este caso?
2. ¿Qué diferencia hay entre rescisión justificada e injustificada en términos
   de obligaciones del patrón?
3. ¿Qué componentes debe incluir la liquidación si la rescisión es injustificada?
4. ¿Qué errores procedimentales cometió la empresa en este caso?
5. ¿Cuándo esta situación requiere intervención de un abogado laboral?

Cita los artículos específicos de la LFT para cada punto. Declara tus supuestos.
```

2. Presione **Enter** y espere la respuesta completa de Copilot.
3. **Analice la respuesta** usando el PDF oficial de la LFT:
   - Verifique que los artículos citados (especialmente Arts. 47 y 48) correspondan al texto real de la LFT.
   - Confirme si Copilot mencionó la obligación de notificación por escrito (Art. 47, párrafo final).
   - Verifique si Copilot calculó o describió correctamente los componentes de la liquidación (3 meses de salario + 20 días por año + partes proporcionales de vacaciones, prima vacacional y aguinaldo).
4. En su documento Word, bajo **"Caso 1 — Rescisión"**, registre:
   - La respuesta de Copilot (puede copiar y pegar o resumir).
   - Una tabla de **Coincidencias y Discrepancias** con el texto oficial.
   - Su decisión: ¿Este caso requiere escalamiento a abogado? Justifique.

#### Tabla de Registro para el Documento Word

Use esta estructura en su documento:

```
CASO 1 — ANÁLISIS COMPARATIVO
┌─────────────────────────┬──────────────────────┬──────────────────────┐
│ Punto analizado         │ Respuesta de Copilot │ Texto oficial LFT    │
├─────────────────────────┼──────────────────────┼──────────────────────┤
│ Causas de rescisión     │                      │ Art. 47 LFT          │
│ justificada             │                      │                      │
├─────────────────────────┼──────────────────────┼──────────────────────┤
│ Obligaciones del patrón │                      │ Art. 48 LFT          │
│ en rescisión injust.    │                      │                      │
├─────────────────────────┼──────────────────────┼──────────────────────┤
│ Componentes de          │                      │ Arts. 48, 76, 80,    │
│ liquidación             │                      │ 87 LFT               │
├─────────────────────────┼──────────────────────┼──────────────────────┤
│ Errores procedimentales │                      │ Art. 47 (notif.      │
│ del patrón              │                      │ escrita)             │
└─────────────────────────┴──────────────────────┴──────────────────────┘
Decisión de escalamiento: [ ] Sí requiere abogado  [ ] No requiere
Justificación: ___________________________________________
```

#### Resultado Esperado

Copilot debe identificar que la empresa cometió errores procedimentales graves (ausencia de actas administrativas, falta de notificación escrita), que la rescisión probablemente sería calificada como injustificada, y que los componentes de liquidación incluyen indemnización constitucional. Debe citar los Arts. 47, 48 y relacionados.

#### Verificación

- [ ] Copilot citó al menos los Arts. 47 y 48 de la LFT.
- [ ] Se identificaron errores procedimentales de la empresa.
- [ ] La tabla comparativa está completada en el documento Word.
- [ ] Se documentó la decisión de escalamiento.

---

### Paso 3 — Caso 2: Tipos de Contratación Laboral

**Objetivo:** Interpretar las diferencias entre contrato por tiempo indeterminado, determinado y por obra determinada según los Arts. 35–39 de la LFT, y aplicarlos a un escenario de contratación ficticio.

#### Instrucciones

1. En la misma sesión de Copilot, ingrese el **Caso 2**:

```text
CASO 2 — TIPOS DE CONTRATACIÓN

Contexto ficticio:
"Constructora Ficticia S.A." necesita contratar personal para tres situaciones:
- Situación A: Un contador que se integrará de manera permanente al equipo de finanzas.
- Situación B: Un promotor de ventas para una campaña de 3 meses durante temporada alta.
- Situación C: Un supervisor de obra para un proyecto de construcción específico
  con duración estimada de 8 meses.

Preguntas:
1. ¿Qué tipo de contrato corresponde a cada situación según la LFT?
2. ¿Qué requisitos formales debe cumplir cada tipo de contrato?
3. ¿Qué ocurre si se usa un contrato por tiempo determinado cuando la naturaleza
   del trabajo es permanente?
4. ¿Cuáles son las diferencias en derechos y obligaciones entre los tres tipos?
5. ¿En qué casos la LFT presume que el contrato es por tiempo indeterminado?

Cita artículos específicos (Arts. 35-39 LFT principalmente). Declara supuestos.
Señala si alguna situación presenta riesgo legal para la empresa.
```

2. Espere la respuesta de Copilot y **analícela** contra los Arts. 35–39 del PDF oficial de la LFT.
3. Verifique específicamente:
   - ¿Copilot mencionó la presunción de contrato por tiempo indeterminado (Art. 35)?
   - ¿Distinguió correctamente entre contrato por obra determinada y por tiempo determinado?
   - ¿Identificó el riesgo legal en la Situación A si se usa contrato temporal?
4. Documente sus hallazgos en el formato de tabla del Paso 2, adaptado al Caso 2.
5. **Formule una pregunta de seguimiento** (Socratic questioning prompt) para profundizar:

```text
Pregunta de seguimiento — Caso 2:
Si la empresa renueva el contrato por tiempo determinado del promotor de ventas
(Situación B) por tres períodos consecutivos de 3 meses cada uno, ¿qué implicaciones
legales tiene esto según la LFT? ¿En qué momento la ley considera que la relación
se vuelve por tiempo indeterminado? Cita el artículo aplicable.
```

6. Analice esta segunda respuesta y documente el hallazgo adicional.

#### Resultado Esperado

Copilot debe asignar correctamente: Situación A → tiempo indeterminado (Art. 35), Situación B → tiempo determinado (Art. 37), Situación C → por obra determinada (Art. 36). En la pregunta de seguimiento, debe señalar el riesgo de conversión automática a contrato indefinido por renovaciones sucesivas.

#### Verificación

- [ ] Los tres tipos de contrato fueron identificados correctamente con citas.
- [ ] Se identificó el riesgo legal de la Situación A.
- [ ] La pregunta de seguimiento generó una respuesta útil sobre renovaciones.
- [ ] Hallazgos documentados en Word.

---

### Paso 4 — Caso 3: Horas Extraordinarias y Límites de Jornada

**Objetivo:** Aplicar el análisis de horas extras de la Lección 3.1 a un caso práctico específico, verificando límites legales y cálculos de pago conforme a los Arts. 66–68 de la LFT.

#### Instrucciones

1. Ingrese el **Caso 3** en Copilot Chat:

```text
CASO 3 — HORAS EXTRAORDINARIAS

Contexto ficticio:
"Empresa Logística Ficticia S.A." opera con personal administrativo en jornada
diurna (8 horas diarias, lunes a viernes). Por cierre de mes, la empresa ha
solicitado a 10 colaboradores trabajar:
- Semana 1: 2 horas extra por día, 5 días (total: 10 horas extra en la semana)
- Semana 2: 1 hora extra por día, 3 días (total: 3 horas extra en la semana)
- Semana 3: 3 horas extra por día, 4 días (total: 12 horas extra en la semana)

Preguntas:
1. ¿Cuál es el límite legal de horas extra por día y por semana según la LFT?
2. ¿Cuál es la forma correcta de pagar las horas extra en cada semana del ejemplo?
3. ¿En qué semanas se excede el límite legal? ¿Qué consecuencias tiene el exceso?
4. ¿Qué sanciones puede enfrentar la empresa por exceder los límites?
5. ¿Qué controles administrativos debe implementar RR.HH. para evitar violaciones?

Usa el enfoque "citas primero": cita Arts. 66, 67 y 68 LFT para cada punto.
Realiza el análisis semana por semana. Indica si hay datos faltantes.
```

2. Espere la respuesta y **verifique contra el PDF de la LFT**:
   - Art. 66: límite de 3 horas diarias y máximo 3 veces por semana (9 horas semanales).
   - Art. 67: pago doble (100% adicional) para horas extra dentro del límite.
   - Art. 68: pago triple (200% adicional) para horas que excedan el límite semanal.
3. Construya en su documento Word una **tabla de análisis semanal**:

```
ANÁLISIS SEMANAL DE HORAS EXTRA
┌──────────┬───────────┬──────────────┬────────────────┬──────────────────┐
│ Semana   │ Hrs extra │ Límite legal │ ¿Excede límite?│ Forma de pago    │
│          │ totales   │ (9 hrs/sem)  │                │ según LFT        │
├──────────┼───────────┼──────────────┼────────────────┼──────────────────┤
│ Semana 1 │ 10 hrs    │ 9 hrs        │                │                  │
├──────────┼───────────┼──────────────┼────────────────┼──────────────────┤
│ Semana 2 │ 3 hrs     │ 9 hrs        │                │                  │
├──────────┼───────────┼──────────────┼────────────────┼──────────────────┤
│ Semana 3 │ 12 hrs    │ 9 hrs        │                │                  │
└──────────┴───────────┴──────────────┴────────────────┴──────────────────┘
```

4. Complete la tabla con base en la respuesta de Copilot y su verificación en el PDF oficial.
5. Documente si Copilot también analizó correctamente el límite **diario** (3 horas por día) además del semanal.

#### Resultado Esperado

Copilot debe identificar que las Semanas 1 y 3 exceden el límite semanal de 9 horas. La Semana 1 tiene 1 hora en exceso (pago triple) y la Semana 3 tiene 3 horas en exceso (pago triple). Debe citar Arts. 66, 67 y 68 y señalar posibles sanciones por reincidencia.

#### Verificación

- [ ] Copilot identificó correctamente las semanas que exceden el límite legal.
- [ ] Se citaron los Arts. 66, 67 y 68 LFT.
- [ ] La tabla de análisis semanal está completada en Word.
- [ ] Se documentaron los controles administrativos recomendados.

---

### Paso 5 — Caso 4: Modificación Unilateral de Condiciones Laborales

**Objetivo:** Analizar los derechos del trabajador ante un cambio unilateral de condiciones laborales, identificando los artículos aplicables y el procedimiento correcto.

#### Instrucciones

1. Ingrese el **Caso 4** en Copilot Chat:

```text
CASO 4 — MODIFICACIÓN UNILATERAL DE CONDICIONES LABORALES

Contexto ficticio:
"Empresa Comercial Ficticia S.A." decide implementar los siguientes cambios
para el área de ventas, sin consultar ni notificar previamente a los trabajadores:
- Cambio A: Reducir el salario base en un 15% y compensarlo con comisiones variables.
- Cambio B: Cambiar el horario de trabajo de turno matutino (7am-3pm) a turno
  vespertino (3pm-11pm).
- Cambio C: Reubicar físicamente al personal de la Ciudad de México a una sucursal
  en Monterrey (dato ficticio de ciudad).
- Cambio D: Modificar las funciones del puesto agregando responsabilidades
  significativamente distintas al contrato original.

Preguntas:
1. ¿Cuáles de estos cambios constituyen una modificación sustancial de condiciones
   de trabajo según la LFT?
2. ¿Qué derechos tiene el trabajador ante estas modificaciones?
3. ¿Puede el trabajador considerarse despedido indirectamente (rescisión imputable
   al patrón)? ¿En qué casos?
4. ¿Qué procedimiento debe seguir la empresa para implementar cambios lícitos?
5. ¿Cuál es el riesgo legal para la empresa en cada uno de los cuatro cambios?

Aplica razonamiento jurídico cadena-de-pensamiento (chain-of-thought):
analiza cada cambio de forma independiente antes de dar una conclusión general.
Cita artículos aplicables de la LFT. Señala cuándo se requiere abogado laboral.
```

2. Espere la respuesta de Copilot y evalúe si aplicó correctamente el **chain-of-thought** solicitado (análisis independiente de cada cambio).
3. Verifique contra el PDF de la LFT:
   - Art. 51 (causas de rescisión imputables al patrón).
   - Art. 52 (derecho a indemnización cuando el trabajador rescinde por causa del patrón).
   - Arts. 56 y 57 (condiciones de trabajo, principio de no desmejora).
4. **Formule una pregunta de seguimiento con razonamiento socrático**:

```text
Pregunta socrática — Caso 4:
Si el trabajador acepta en silencio el Cambio A (reducción salarial) durante
3 meses sin protestar formalmente, ¿pierde su derecho a reclamar posteriormente?
¿Qué establece la LFT sobre la renuncia de derechos laborales? ¿Es válida
una renuncia tácita en materia laboral mexicana?
```

5. Documente ambas respuestas en su documento Word, resaltando los artículos verificados y los que no pudo confirmar en el PDF oficial.

#### Resultado Esperado

Copilot debe identificar que los Cambios A, B, C y D constituyen modificaciones sustanciales. Debe mencionar el principio de irrenunciabilidad de derechos (Art. 5 LFT) en la pregunta socrática, indicando que la renuncia tácita no es válida en materia laboral mexicana. Debe recomendar escalamiento a abogado para los Cambios A y C por su alta complejidad.

#### Verificación

- [ ] Copilot analizó cada cambio de forma independiente (chain-of-thought).
- [ ] Se identificaron los artículos sobre rescisión imputable al patrón.
- [ ] La pregunta socrática generó análisis sobre irrenunciabilidad de derechos.
- [ ] Se documentó la recomendación de escalamiento a abogado.

---

### Paso 6 — Caso 5: Baja Voluntaria vs. Abandono de Empleo

**Objetivo:** Distinguir el procedimiento correcto para una baja voluntaria de un abandono de empleo, identificando las diferencias legales, documentales y de riesgo para la empresa.

#### Instrucciones

1. Ingrese el **Caso 5** en Copilot Chat:

```text
CASO 5 — BAJA VOLUNTARIA VS. ABANDONO DE EMPLEO

Contexto ficticio:
"Empresa de Servicios Ficticia S.A." enfrenta dos situaciones simultáneas:

SITUACIÓN 5A — Baja voluntaria:
"Trabajador B" (ficticio) informa verbalmente a su supervisor que renuncia
"porque consiguió otro trabajo", pero no entrega carta de renuncia escrita.
La empresa desea procesar su baja de inmediato.

SITUACIÓN 5B — Posible abandono:
"Trabajador C" (ficticio) no se presentó a trabajar durante 4 días consecutivos
sin aviso previo ni justificación. La empresa no ha podido localizarlo.
El supervisor quiere registrarlo como "abandono de empleo" y dar de baja
sin pagar liquidación.

Preguntas para ambas situaciones:
1. ¿Cuál es el procedimiento legalmente correcto para cada caso?
2. ¿Qué documentación debe recabar RR.HH. en cada situación?
3. ¿Cuáles son los riesgos legales si la empresa actúa incorrectamente?
4. En la Situación 5B: ¿el "abandono de empleo" es una figura reconocida
   expresamente en la LFT? ¿Cómo debe manejarse?
5. ¿Qué diferencia hay en las obligaciones de pago del patrón en cada caso?

Aplica el enfoque "citas primero". Distingue entre norma y guía.
Señala ambigüedades. Indica cuándo se requiere abogado.
```

2. Espere la respuesta y verifique específicamente:
   - Si Copilot mencionó que el "abandono de empleo" **no está definido explícitamente** como tal en la LFT, sino que se maneja como ausencias injustificadas que pueden ser causa de rescisión (Art. 47, fracción X).
   - Si identificó el riesgo de que la empresa sea demandada por despido injustificado si no documenta correctamente la Situación 5B.
   - Si recomendó el uso de actas circunstanciadas y notificaciones formales.
3. Documente en su Word:
   - Un **cuadro comparativo** de Situación 5A vs. 5B con: procedimiento correcto, documentación requerida, riesgos legales y obligaciones de pago.
   - Una sección de **"Alerta de escalamiento"** para esta situación.

#### Resultado Esperado

Copilot debe recomendar para la Situación 5A obtener renuncia por escrito y finiquito firmado. Para la Situación 5B, debe indicar que la empresa debe agotar intentos de localización, levantar actas administrativas de ausencia y notificar formalmente antes de proceder a rescisión, para evitar ser demandada por despido injustificado. Debe recomendar escalamiento a abogado para ambas situaciones dada su complejidad.

#### Verificación

- [ ] Copilot distinguió correctamente los procedimientos de cada situación.
- [ ] Se identificó la ausencia del concepto "abandono de empleo" como figura autónoma en la LFT.
- [ ] El cuadro comparativo está completado en Word.
- [ ] Se documentó la alerta de escalamiento.

---

### Paso 7 — Caso 6 (Integrador): Estrategia de Decisión con Múltiples Variables

**Objetivo:** Construir un flujo de toma de decisiones documentado para un caso laboral complejo con múltiples variables simultáneas, integrando todos los aprendizajes de los casos anteriores.

#### Instrucciones

1. Este es el caso más complejo de la práctica. Ingrese el **Caso 6** en Copilot Chat:

```text
CASO 6 — CASO INTEGRADOR: MÚLTIPLES VARIABLES SIMULTÁNEAS

Contexto ficticio:
"Corporativo Industrial Ficticio S.A. de C.V." enfrenta la siguiente situación:

"Trabajador D" (ficticio), 8 años de antigüedad, contrato por tiempo indeterminado,
jornada diurna, salario mensual de $22,000 MXN (ficticio), se encuentra en la
siguiente situación simultánea:

VARIABLE 1: Ha acumulado 6 faltas injustificadas en los últimos 2 meses.
            La empresa tiene actas administrativas de solo 2 de las 6 faltas.

VARIABLE 2: Durante el último mes trabajó 15 horas extra semanales en promedio
            (excediendo el límite legal), pero no hay registro formal de esto.

VARIABLE 3: La empresa le comunicó verbalmente hace 3 semanas que su puesto
            será "reestructurado" y su salario reducido en 20%.

VARIABLE 4: El trabajador presentó una queja ante la PROFEDET hace 1 semana
            por las condiciones anteriores.

VARIABLE 5: La empresa ahora quiere proceder con su rescisión argumentando
            las faltas injustificadas.

Tarea para el asistente:
Aplica razonamiento jurídico paso a paso (chain-of-thought legal reasoning):
1. Analiza cada variable de forma independiente citando artículos LFT aplicables.
2. Identifica cómo las variables interactúan y se afectan mutuamente.
3. Evalúa la posición legal de la empresa: ¿puede proceder con la rescisión?
4. Evalúa la posición legal del trabajador: ¿qué derechos puede ejercer?
5. Diseña una estrategia de decisión para RR.HH. con 3 escenarios posibles:
   Escenario A: La empresa procede con la rescisión.
   Escenario B: La empresa ofrece una terminación negociada.
   Escenario C: La empresa revierte los cambios y regulariza la situación.
6. Para cada escenario, indica: probabilidad de éxito legal, riesgos, costos
   aproximados (en términos de obligaciones legales, no cifras exactas) y
   recomendación de acción.
7. Concluye con una recomendación clara para RR.HH. e indica si se requiere
   abogado laboral de manera URGENTE.
```

2. Espere la respuesta completa de Copilot (puede tardar más que los casos anteriores).
3. **Evalúe críticamente la respuesta** verificando:
   - ¿Copilot identificó que la queja ante la PROFEDET (Variable 4) complica significativamente la posición de la empresa?
   - ¿Mencionó el principio de que las faltas sin acta administrativa son difíciles de probar ante un tribunal?
   - ¿Identificó la exposición de la empresa por horas extra no registradas (Variable 2)?
   - ¿Distinguió los tres escenarios con suficiente profundidad?
   - ¿Recomendó escalamiento urgente a abogado laboral?
4. En su documento Word, construya el **Flujo de Toma de Decisiones** basado en la respuesta de Copilot y su verificación:

```
FLUJO DE TOMA DE DECISIONES — CASO 6

[Situación inicial: múltiples variables simultáneas]
           ↓
[Paso 1: Auditoría de documentación disponible]
  → ¿Hay actas de todas las faltas? → Si NO → Riesgo alto de rescisión fallida
  → ¿Hay registro de horas extra? → Si NO → Exposición adicional de la empresa
           ↓
[Paso 2: Evaluación de la queja PROFEDET]
  → Queja activa → Escalamiento URGENTE a abogado laboral
           ↓
[Paso 3: Evaluación de escenarios]
  → Escenario A: Rescisión → [Arts. 47, 48 LFT] → Riesgo: ALTO
  → Escenario B: Negociación → [Arts. 53-55 LFT] → Riesgo: MEDIO
  → Escenario C: Regularización → [Arts. 56, 57 LFT] → Riesgo: BAJO
           ↓
[Decisión RR.HH.: Documentar, escalar a Legal, no actuar unilateralmente]
```

5. Guarde el documento Word con este flujo completado.

#### Resultado Esperado

Copilot debe producir un análisis multivariable que identifique que la empresa se encuentra en una posición legal vulnerable en todos los frentes, y debe recomendar urgentemente la intervención de un abogado laboral antes de cualquier acción. El flujo de decisiones debe reflejar la complejidad real del caso.

#### Verificación

- [ ] Copilot analizó las 5 variables de forma independiente e interrelacionada.
- [ ] Se identificó la complicación de la queja PROFEDET.
- [ ] Los tres escenarios fueron evaluados con sus riesgos.
- [ ] El flujo de toma de decisiones está documentado en Word.
- [ ] Se documentó la recomendación de escalamiento urgente.

---

### Paso 8 — Construcción de la Guía de Consulta Rápida LFT con Copilot

**Objetivo:** Consolidar los aprendizajes de la práctica en un documento de referencia reutilizable para el área de RR.HH.

#### Instrucciones

1. Abra su documento Word `Practica3_[SusIniciales]_ConsultoriaLFT.docx`.
2. Agregue una nueva sección al final titulada: **"Guía de Consulta Rápida LFT con Copilot — Área de RR.HH."**
3. Ingrese el siguiente prompt en Copilot Chat para generar el borrador inicial de la guía:

```text
Basándote en los 6 casos que analizamos en esta sesión, genera una
"Guía de Consulta Rápida LFT con Copilot" para el área de RR.HH.

La guía debe incluir:
1. TABLA DE ARTÍCULOS CLAVE: Una tabla con los artículos LFT más relevantes
   para RR.HH., organizados por tema (contratación, jornada, rescisión,
   terminación), con una descripción de 1-2 líneas de cada uno.

2. PLANTILLA DE PROMPT BASE: La plantilla de prompt recomendada para consultas
   normativas en Copilot Chat (adaptada de las instrucciones de esta sesión).

3. CRITERIOS DE ESCALAMIENTO: Una lista de situaciones que SIEMPRE requieren
   abogado laboral, independientemente de lo que diga Copilot.

4. ADVERTENCIAS DE USO: Las 3 limitaciones más importantes de usar Copilot
   para consultas de la LFT.

5. CHECKLIST DE VERIFICACIÓN: Una lista de verificación de 8 puntos que RR.HH.
   debe revisar antes de tomar cualquier decisión laboral basada en
   una respuesta de Copilot.

Formato: Estructura clara con subtítulos, tablas donde aplique, y lenguaje
profesional pero accesible para personal de RR.HH. sin formación jurídica.
```

4. Copie la respuesta de Copilot y péguela en la sección de la Guía en Word.
5. **Revise y edite** el contenido generado:
   - Corrija cualquier artículo que Copilot haya citado incorrectamente (verifique contra el PDF oficial).
   - Agregue la advertencia legal crítica del curso en la sección de "Advertencias de uso".
   - Personalice con el nombre de su organización ficticia y la fecha.
6. Aplique formato profesional al documento Word:
   - Estilos de título (Título 1, Título 2).
   - Tabla de contenido automática al inicio del documento.
   - Numeración de páginas.
   - Pie de página con: "Documento generado con apoyo de Microsoft 365 Copilot Chat — Requiere validación legal antes de su implementación."
7. Guarde el documento final en OneDrive.

#### Resultado Esperado

Un documento Word completo y profesional que incluya: los análisis de los 6 casos, las tablas comparativas, el flujo de toma de decisiones del Caso 6, y la Guía de Consulta Rápida lista para uso del área de RR.HH.

#### Verificación

- [ ] La Guía de Consulta Rápida está incluida en el documento Word.
- [ ] Los artículos de la LFT fueron verificados contra el PDF oficial.
- [ ] El documento tiene formato profesional con tabla de contenido.
- [ ] El pie de página incluye la advertencia legal.
- [ ] El documento está guardado en OneDrive.

---

## 7. Validación y Pruebas

### 7.1 Criterios de Evaluación por Caso

| Caso | Criterio de éxito | Puntos |
|---|---|---|
| Caso 1 — Rescisión | Identificó errores procedimentales y componentes de liquidación con citas correctas | 15 |
| Caso 2 — Tipos de contrato | Asignó correctamente los 3 tipos y analizó la pregunta de seguimiento | 15 |
| Caso 3 — Horas extra | Completó la tabla semanal con análisis correcto de límites y pagos | 15 |
| Caso 4 — Modificación unilateral | Aplicó chain-of-thought y analizó irrenunciabilidad de derechos | 15 |
| Caso 5 — Baja/Abandono | Distinguió procedimientos y documentó alertas de escalamiento | 15 |
| Caso 6 — Integrador | Construyó flujo de decisiones con los 3 escenarios evaluados | 15 |
| Guía de Consulta Rápida | Documento completo, formateado y con advertencia legal | 10 |
| **Total** | | **100** |

### 7.2 Prueba de Calidad de Prompts

Para verificar la calidad de su trabajo de ingeniería de prompts, responda estas preguntas en su documento Word bajo una sección titulada **"Reflexión sobre Ingeniería de Prompts"**:

1. ¿En cuántos casos Copilot citó artículos que NO pudiste verificar en el PDF oficial de la LFT? Describe uno de ellos.
2. ¿En qué caso Copilot solicitó información adicional por datos faltantes? ¿Fue útil esa solicitud?
3. ¿Hubo algún caso en que la respuesta de Copilot fue ambigua o contradictoria? ¿Cómo lo resolviste?
4. ¿Qué elemento de la plantilla de prompt base (del Paso 1) fue más efectivo para mejorar la calidad de las respuestas?
5. ¿En cuántos de los 6 casos concluiste que se requiere escalamiento a abogado laboral? ¿Coincide con tu criterio profesional?

### 7.3 Lista de Verificación Final

Antes de dar por concluida la práctica, confirme que su documento Word contiene:

- [ ] Análisis documentado de los 6 casos con tablas comparativas.
- [ ] Capturas de pantalla de al menos 3 respuestas de Copilot (Casos 1, 3 y 6 como mínimo).
- [ ] Flujo de toma de decisiones del Caso 6.
- [ ] Guía de Consulta Rápida LFT con Copilot completa.
- [ ] Sección de Reflexión sobre Ingeniería de Prompts.
- [ ] Tabla de contenido automática y numeración de páginas.
- [ ] Pie de página con advertencia legal.
- [ ] Documento guardado en OneDrive con nombre correcto.

---

## 8. Solución de Problemas

### Problema 1 — Copilot ignora las instrucciones del prompt de sistema y no cita artículos

**Síntoma:** Las respuestas de Copilot no incluyen citas de artículos de la LFT, o responde de manera genérica sin seguir la estructura solicitada en el prompt del Paso 1.

**Causa probable:** Copilot Chat en modo empresarial no tiene un "system prompt" persistente entre mensajes de la misma forma que una API configurada. Las instrucciones del primer mensaje pueden diluirse en conversaciones largas. También puede ocurrir si se está usando la versión gratuita (Bing Copilot) en lugar de la versión empresarial con licencia M365 Copilot.

**Solución:**

```
1. Verifique que está en https://m365.cloud.microsoft/chat y que el modo
   "Trabajo" (Work) está activo — debe mostrar el ícono de su organización.

2. Si las respuestas se degradan en calidad después de varios mensajes,
   refuerce las instrucciones con un recordatorio breve:

   "Recuerda: debes citar artículos específicos de la LFT con el formato
   [Art. XX, LFT], distinguir norma de guía, y declarar supuestos.
   Continúa con el siguiente caso aplicando estas reglas."

3. Si el problema persiste, inicie una nueva sesión y repita el prompt
   de configuración del Paso 1 antes de continuar con el caso pendiente.

4. Confirme con su administrador de TI que su cuenta tiene activa la
   licencia Microsoft 365 Copilot (no confundir con Copilot gratuito).
   Señal de alerta: si no ve el modo "Trabajo/Work" en la interfaz,
   probablemente no tiene la licencia correcta.
```

---

### Problema 2 — Copilot cita artículos de la LFT con numeración incorrecta o contenido que no coincide con el PDF oficial

**Síntoma:** Al verificar las respuestas de Copilot contra el PDF oficial de la LFT, se encuentran artículos con numeración diferente, contenido parcialmente incorrecto, o referencias a disposiciones que no existen en la versión vigente de la ley.

**Causa probable:** Los modelos de lenguaje grandes (LLMs) como Copilot tienen una fecha de corte de conocimiento y pueden mezclar versiones históricas de la LFT con la versión vigente. Esto es especialmente relevante en una ley que ha tenido múltiples reformas. Además, la variabilidad probabilística de los LLMs puede producir "alucinaciones" en citas legales específicas.

**Solución:**

```
1. NUNCA tome como definitiva una cita de artículo de Copilot sin verificarla
   en el PDF oficial de la LFT. Este es el principio fundamental de la
   práctica: "validación humana siempre".

2. Fuente oficial de verificación:
   https://www.diputados.gob.mx/LeyesBiblio/pdf/LFT.pdf
   Confirme la fecha de la última reforma en la portada del PDF.

3. Si encuentra una discrepancia, documente en su Word:
   - Artículo citado por Copilot: [número y texto según Copilot]
   - Artículo real en LFT: [número y texto real]
   - Tipo de discrepancia: numeración incorrecta / contenido parcial /
     artículo inexistente

4. Reformule el prompt con mayor especificidad para reducir alucinaciones:
   "Basándote únicamente en artículos que puedas citar con certeza de la LFT
   vigente, ¿cuál es el fundamento legal para [situación]? Si no tienes
   certeza del número exacto del artículo, indícalo explícitamente."

5. Recuerde a los participantes: la variabilidad de respuestas entre sesiones
   es normal en LLMs. Dos participantes pueden obtener respuestas diferentes
   al mismo prompt — esto es parte del aprendizaje sobre el comportamiento
   de los modelos de lenguaje.
```

---

## 9. Limpieza del Entorno

Una vez concluida la práctica, realice los siguientes pasos de cierre:

### 9.1 Cierre de la Sesión de Copilot Chat

```
1. En Microsoft 365 Copilot Chat, haga clic en el ícono de nueva conversación
   para cerrar la sesión activa de la práctica.
   (Esto evita que información de los casos ficticios persista en el historial
   de sesión activa.)
2. Si su organización requiere borrar el historial de Copilot:
   - Vaya a Configuración → Historial de conversaciones → Eliminar historial
   (según las políticas de su organización)
```

### 9.2 Guardado Final del Documento Word

```
1. Asegúrese de que el documento Word está guardado en OneDrive:
   Practica3_[SusIniciales]_ConsultoriaLFT.docx

2. Verifique que el documento está sincronizado en OneDrive
   (ícono de nube sin indicador de error en la barra de estado de Word).

3. Si el instructor requiere entrega, comparta el documento desde OneDrive:
   Archivo → Compartir → Copiar vínculo → Enviar al instructor.
```

### 9.3 Cierre de Archivos de Referencia

```
1. Cierre el PDF de la LFT (no es necesario eliminarlo; consérvelo como
   referencia para prácticas futuras).

2. Cierre el archivo Casos_LFT_Ficticios.docx proporcionado por el instructor.

3. Cierre todas las pestañas del navegador relacionadas con la práctica,
   excepto si el instructor indica continuar con una actividad de cierre grupal.
```

---

## 10. Resumen y Recursos Adicionales

### 10.1 Resumen de la Práctica

En esta práctica aplicó Microsoft 365 Copilot Chat como herramienta de consultoría normativa interactiva para resolver seis casos laborales de complejidad creciente. Los aprendizajes clave son:

| Aprendizaje | Aplicación práctica |
|---|---|
| **Enfoque "citas primero"** | Todo prompt de consulta legal debe exigir artículos específicos antes de conclusiones generales |
| **Validación humana siempre** | Las respuestas de Copilot son punto de partida, no veredicto legal |
| **Chain-of-thought legal** | Analizar variables complejas de forma independiente antes de integrar conclusiones reduce errores |
| **Criterios de escalamiento** | Queja PROFEDET activa, rescisiones con documentación incompleta y modificaciones salariales siempre requieren abogado |
| **Variabilidad de LLMs** | Respuestas diferentes entre sesiones son normales; la verificación contra fuentes oficiales es el control de calidad |
| **Irrenunciabilidad de derechos** | Principio fundamental de la LFT que Copilot debe identificar en casos de modificación de condiciones |

### 10.2 Artículos LFT de Referencia Rápida

| Tema | Artículos clave |
|---|---|
| Tipos de contrato | Arts. 35, 36, 37, 38, 39 |
| Rescisión por causa del patrón | Arts. 51, 52 |
| Rescisión por causa del trabajador | Arts. 47, 48 |
| Terminación de la relación laboral | Arts. 53, 54, 55 |
| Condiciones de trabajo | Arts. 56, 57 |
| Jornada extraordinaria | Arts. 66, 67, 68 |
| Descanso semanal y prima dominical | Arts. 69, 71, 73 |
| Irrenunciabilidad de derechos | Art. 5 |

### 10.3 Recursos Adicionales

| Recurso | URL |
|---|---|
| Texto oficial de la LFT (Cámara de Diputados) | [https://www.diputados.gob.mx/LeyesBiblio/pdf/LFT.pdf](https://www.diputados.gob.mx/LeyesBiblio/pdf/LFT.pdf) |
| PROFEDET — Orientación laboral | [https://www.gob.mx/profedet](https://www.gob.mx/profedet) |
| STPS — Información y guías | [https://www.gob.mx/stps](https://www.gob.mx/stps) |
| Diario Oficial de la Federación (DOF) | [https://www.dof.gob.mx](https://www.dof.gob.mx) |
| Microsoft Copilot para M365 — Documentación | [https://learn.microsoft.com/es-es/microsoft-365-copilot/](https://learn.microsoft.com/es-es/microsoft-365-copilot/) |
| Principios OCDE sobre IA (español) | [https://oecd.ai/es/principles](https://oecd.ai/es/principles) |

### 10.4 Próximos Pasos Recomendados

- **Práctica 4:** Aplicar las técnicas de esta práctica a la redacción automatizada de documentos laborales (contratos, actas administrativas, cartas de rescisión) con Copilot en Microsoft Word.
- **Actualización normativa:** Revise periódicamente el DOF para confirmar que los artículos de la LFT utilizados en esta guía corresponden a la versión vigente.
- **Validación con Legal:** Comparta la Guía de Consulta Rápida generada con el área jurídica de su organización para su revisión y aprobación antes de distribuirla operativamente.
- **Repositorio RAG:** Si su organización cuenta con infraestructura técnica, considere implementar la arquitectura RAG descrita en la Lección 3.1 para conectar Copilot directamente con el PDF oficial de la LFT y políticas internas aprobadas.

---

> 📌 **Nota final para el instructor:** Recuerde verificar que los artículos de la LFT citados en esta práctica correspondan a la versión vigente de la ley al momento de impartir el curso. Consulte el Diario Oficial de la Federación (DOF) para confirmar la última versión publicada. La LFT puede sufrir modificaciones que afecten la numeración y contenido de los artículos aquí referenciados.

---
*Fin del Lab 03-00-01 — Práctica 3. Consultoría interactiva de la LFT para la toma de decisiones.*
