---
name: indice
description: "Índice de los 46 formularios de Licencias, subvenciones y reclamaciones ante la Administración. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Licencias, subvenciones y reclamaciones ante la Administración: índice de formularios

> Plugin `formularios-licencias-subvenciones-y-reclamaciones` · 46 formularios · normativa revisada el 25-11-2026.

## Qué es

Para tratar con la Administración fuera de lo tributario: licencias urbanísticas y de actividad, subvenciones (solicitud, subsanación y reintegro), reclamaciones ante la AEPD y la CNMV, sanciones de tráfico y procedimiento sancionador, nacionalidad por residencia, responsabilidad patrimonial, recursos administrativos y escritos de contencioso.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Solicitud de licencia de obra»
- «Reclamación ante la Agencia Española de Protección de Datos»
- «Subsanación de una solicitud de subvención»

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

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-licencias-subvenciones-y-reclamaciones:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (2)

| Código | Formulario | Skill |
|---|---|---|
| ADM-0046 | Recurso contencioso-administrativo contra la denegación de la nacionalidad española | `recurso-contencioso-administrativo-contra-denegacion-adm-0046` |
| ADM-0047 | Recurso contencioso-administrativo por el procedimiento de protección de derechos fundamentales | `recurso-contencioso-administrativo-procedimiento-adm-0047` |

### Contestaciones, oposiciones y alegaciones (1)

| Código | Formulario | Skill |
|---|---|---|
| ADM-0056 | Alegaciones del interesado en el recurso de reposición contra una sanción de tráfico | `alegaciones-interesado-recurso-reposicion-contra-adm-0056` |

### Recursos (7)

| Código | Formulario | Skill |
|---|---|---|
| ADM-0036 | Recurso de reposición contra la denegación de prueba en el proceso contencioso-administrativo | `recurso-reposicion-contra-denegacion-prueba-proceso-adm-0036` |
| ADM-0050 | Recurso de alzada ante la Sala de Gobierno del TSJ contra la sanción por mala fe procesal | `recurso-alzada-ante-sala-gobierno-tsj-contra-sancion-adm-0050` |
| ADM-0052 | Recurso de reposición contra una sanción de tráfico relativa al transporte de personas | `recurso-reposicion-contra-sancion-trafico-relativa-adm-0052` |
| ADM-0053 | Recurso de reposición contra una sanción por infringir las normas de tráfico y seguridad vial | `recurso-reposicion-contra-sancion-infringir-normas-adm-0053` |
| ADM-0069 | Recurso de reposición contra la denegación de la nacionalidad española por residencia | `recurso-reposicion-contra-denegacion-nacionalidad-adm-0069` |
| ADM-0070 | Escrito de interposición del contencioso ante la Audiencia Nacional en materia de nacionalidad | `escrito-interposicion-contencioso-ante-audiencia-adm-0070` |
| ADM-0073 | Recurso administrativo potestativo de reposición contra un acto de la Administración | `recurso-administrativo-potestativo-reposicion-contra-adm-0073` |

### Contratos, pactos y cláusulas (5)

| Código | Formulario | Skill |
|---|---|---|
| ADM-0033 | Contrato de colaboración y subvención para un evento musical por procedimiento negociado | `contrato-colaboracion-subvencion-evento-musical-adm-0033` |
| ADM-0051 | Acuerdo de la Sala de Gobierno del TSJ que estima la alzada contra la sanción por mala fe procesal | `acuerdo-sala-gobierno-tsj-estima-alzada-contra-sancion-adm-0051` |
| ADM-0060 | Acuerdo que declara prescrita la sanción y archiva el expediente sancionador | `acuerdo-declara-prescrita-sancion-archiva-expediente-adm-0060` |
| ADM-0064 | Acuerdo del órgano competente que archiva el expediente sancionador por caducidad | `acuerdo-organo-competente-archiva-expediente-adm-0064` |
| ADM-0066 | Acuerdo que inicia el resarcimiento de daños no cuantificados en el expediente sancionador | `acuerdo-inicia-resarcimiento-danos-no-cuantificados-adm-0066` |

### Estatutos, actas, certificaciones y escrituras (3)

| Código | Formulario | Skill |
|---|---|---|
| ADM-0055 | Informe del denunciante sobre las alegaciones del denunciado contra la propuesta de resolución | `informe-denunciante-sobre-alegaciones-denunciado-adm-0055` |
| ADM-0067 | Poder de una asociación vecinal para tramitar la segregación ya iniciada de un núcleo del municipio | `poder-asociacion-vecinal-tramitar-segregacion-ya-adm-0067` |
| ADM-0068 | Poder de una asociación a favor de un tercero para tramitar la segregación municipal | `poder-asociacion-favor-tercero-tramitar-segregacion-adm-0068` |

### Comunicaciones, requerimientos y cartas (15)

| Código | Formulario | Skill |
|---|---|---|
| ADM-0027 | Solicitud de licencia de edificación o de usos en suelo urbano especial | `solicitud-licencia-edificacion-usos-suelo-urbano-adm-0027` |
| ADM-0028 | Solicitud de limitación del tratamiento de datos personales (modelo de la AEPD) | `solicitud-limitacion-tratamiento-datos-personales-adm-0028` |
| ADM-0029 | Solicitud de oposición al tratamiento de datos personales (modelo de la AEPD) | `solicitud-oposicion-tratamiento-datos-personales-adm-0029` |
| ADM-0030 | Solicitud de rectificación de datos personales (modelo de la AEPD) | `solicitud-rectificacion-datos-personales-modelo-aepd-adm-0030` |
| ADM-0031 | Requerimiento de subsanación y mejora de la solicitud de subvención | `requerimiento-subsanacion-mejora-solicitud-subvencion-adm-0031` |
| ADM-0032 | Declaración responsable del solicitante de subvención sobre el cumplimiento de requisitos | `declaracion-responsable-solicitante-subvencion-sobre-adm-0032` |
| ADM-0034 | Solicitud de medida cautelar de suspensión del acto administrativo recurrido | `solicitud-medida-cautelar-suspension-acto-adm-0034` |
| ADM-0040 | Solicitud de identificación del denunciante y de los funcionarios en un expediente sancionador | `solicitud-identificacion-denunciante-funcionarios-adm-0040` |
| ADM-0041 | Comunicación a Tráfico del arrendatario a largo plazo de un vehículo por su titular | `comunicacion-trafico-arrendatario-largo-plazo-vehiculo-adm-0041` |
| ADM-0042 | Comunicación a Tráfico del fin del arrendamiento a largo plazo de un vehículo por su titular | `comunicacion-trafico-fin-arrendamiento-largo-plazo-adm-0042` |
| ADM-0044 | Comunicación a Tráfico del conductor habitual por el arrendatario a largo plazo del vehículo | `comunicacion-trafico-conductor-habitual-arrendatario-adm-0044` |
| ADM-0045 | Comunicación a Tráfico del conductor habitual por el titular del vehículo | `comunicacion-trafico-conductor-habitual-titular-adm-0045` |
| ADM-0057 | Comunicación del trámite de audiencia a los interesados antes de resolver el recurso administrativo | `comunicacion-tramite-audiencia-interesados-antes-adm-0057` |
| ADM-0061 | Notificación del inicio del expediente de resarcimiento de daños causados a la Administración | `notificacion-inicio-expediente-resarcimiento-danos-adm-0061` |
| ADM-0071 | Reclamación de responsabilidad patrimonial por la denegación indebida de una autorización de trabajo | `reclamacion-responsabilidad-patrimonial-denegacion-adm-0071` |

### Escritos de trámite y otros (13)

| Código | Formulario | Skill |
|---|---|---|
| ADM-0026 | Escrito de reclamación ante la Comisión Nacional del Mercado de Valores | `escrito-reclamacion-ante-comision-nacional-mercado-adm-0026` |
| ADM-0035 | Otrosí de la demanda contencioso-administrativa pidiendo vista o conclusiones | `otrosi-demanda-contencioso-administrativa-pidiendo-adm-0035` |
| ADM-0037 | Escrito por el que se otorga representación a otra persona para actuar en el procedimiento | `escrito-otorga-representacion-otra-persona-actuar-adm-0037` |
| ADM-0038 | Escrito pidiendo el trámite de vista o de conclusiones en el proceso contencioso-administrativo | `escrito-pidiendo-tramite-vista-conclusiones-proceso-adm-0038` |
| ADM-0039 | Escrito de conclusiones en el recurso contencioso-administrativo ordinario | `escrito-conclusiones-recurso-contencioso-adm-0039` |
| ADM-0043 | Consentimiento expreso para figurar como conductor habitual de un vehículo ante Tráfico | `consentimiento-expreso-figurar-como-conductor-habitual-adm-0043` |
| ADM-0054 | Traslado al denunciante de las alegaciones del inculpado contra la propuesta de resolución | `traslado-denunciante-alegaciones-inculpado-contra-adm-0054` |
| ADM-0058 | Resolución que desestima el recurso de reposición contra una sanción administrativa | `resolucion-desestima-recurso-reposicion-contra-sancion-adm-0058` |
| ADM-0059 | Resolución que estima en todo o en parte el recurso de reposición contra una sanción | `resolucion-estima-todo-parte-recurso-reposicion-contra-adm-0059` |
| ADM-0062 | Escrito de alegaciones en el expediente para indemnizar a la Administración por los daños causados | `escrito-alegaciones-expediente-indemnizar-adm-0062` |
| ADM-0063 | Traslado a los demás interesados del recurso de reposición contra una sanción de tráfico | `traslado-demas-interesados-recurso-reposicion-contra-adm-0063` |
| ADM-0065 | Petición del interesado de un certificado que acredite la caducidad del expediente sancionador | `peticion-interesado-certificado-acredite-caducidad-adm-0065` |
| ADM-0072 | Escrito de demanda en el contencioso ante la Audiencia Nacional sobre nacionalidad | `escrito-demanda-contencioso-ante-audiencia-nacional-adm-0072` |
