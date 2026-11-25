---
name: recurso-reposicion-contra-sancion-trafico-relativa-adm-0052
description: "Recurso de reposición contra una sanción de tráfico relativa al transporte de personas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de reposición contra una sanción de tráfico relativa al transporte de personas

> Formulario **ADM-0052** del plugin **Licencias, subvenciones y reclamaciones ante la Administración** (`formularios-licencias-subvenciones-y-reclamaciones`) · Administrativo y Tributario › Administrativo general (licencias, subvenciones, autoridades de control) · normativa revisada el 25-11-2026.

## Qué es

Recurso de reposición potestativo contra una resolución sancionadora de tráfico por infracciones relativas al transporte de personas (exceso de ocupantes, falta de la placa interior de plazas, exceso de masa). Permite alegar la vulneración de los principios sancionadores, defectos de procedimiento (presunción de inocencia, derecho de defensa, incompetencia, prescripción, caducidad, concurrencia de sanciones) y razones de fondo, y proponer prueba.

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de reposición contra una sanción de tráfico relativa al transporte de personas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de reposición contra una sanción de tráfico relativa al transporte de personas” para mi caso». También puedes invocarla directamente con `/formularios-licencias-subvenciones-y-reclamaciones:recurso-reposicion-contra-sancion-trafico-relativa-adm-0052`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-licencias-subvenciones-y-reclamaciones:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Licencias, subvenciones y reclamaciones ante la Administración) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] PROVINCIA (2 veces)
- [ ] CAUSA
- [ ] CIRCUNSTANCIA
- [ ] CIRCUNSTANCIAS
- [ ] CUALIFICACIÓN PROFESIONAL
- [ ] CÓDIGO POSTAL
- [ ] DIRECCIÓN ELECTRÓNICA
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] ESPECIFICAR
- [ ] EXTREMOS
- [ ] EXTREMOS QUE ACREDITA
- [ ] EXTREMOS QUE SE PRETENDEN ACREDITAR
- [ ] IMPORTE
- [ ] NOMBRE Y APELLIDOS DE LOS TESTIGOS
- [ ] NOMBRE Y APELLIDOS DEL PERITO
- [ ] Nº
- [ ] Nº DE EXPEDIENTE
- [ ] RELATO DE LOS HECHOS TAL Y COMO SUCEDIERON
- [ ] ÓRGANO COMPETENTE
- [ ] ÓRGANO QUE DICTÓ LA RESOLUCIÓN

## Normas que cita el formulario

- art. 9.1 Real Decreto 1428/2003
- art. 12.6 Real Decreto Legislativo 6/2015
- art. 27 Ley 40/2015
- art. 29.3 LRJS
- art. 28 LRJS
- art. 130.1 Ley 30/1992
- art. 53.2.b Ley 39/2015
- art. 77 LPAC
- art. 13 Real Decreto 320/1994
- art. 18 Real Decreto 320/1994
- art. 31 LRJS
- art. 112 LPAC
- art. 118 LPAC

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Avisos de actualización (5) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: Se mantiene la nota sobre la calificación: el art. 12.6 TR LTCVMSV vigente se refiere a la carga de los vehículos; usar el precepto que cite la propia resolución.
- Junto a «…re a la carga de los vehículos; usar el precepto que cite la propia resolución.]»: El RD 320/1994 sigue en el BOE consolidado, pero cede ante el TR LTCVMSV (p. ej., sus plazos de prescripción del art. 18 difieren de los del art. 112 TR).
- Junto a «…. ej., sus plazos de prescripción del art. 18 difieren de los del art. 112 TR).]»: Cita doctrinal de V. Magro Servet (2011) (sin comprobar).
- Junto a «…epasando, entre viajeros y equipaje, el peso máximo autorizado para el vehículo.»: compruébense la calificación y el precepto legal que cite la propia resolución. El art. 12.6 TR LTCVMSV vigente se refiere a la carga de los vehículos; y el art. 9.3 del Reglamento General de Circulación califica como muy graves las infracciones que supongan aumentar en un 50 por ciento el número de plazas autorizadas, excluida la del conductor (salvo autobuses de líneas urbanas e interurbanas), con inmovilización del vehículo.
- Junto a «…motivada las pruebas propuestas por los interesados, cuando sean improcedentes».»: según el art. 95.3 TR LTCVMSV, solo es obligatorio dar traslado de la propuesta de resolución al interesado si figuran en el procedimiento o se han tenido en cuenta en la resolución hechos, alegaciones o pruebas distintos de los aducidos por él; alegar la falta de traslado únicamente en ese caso.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

- Ninguna.

### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
