# Licencias, subvenciones y reclamaciones ante la Administración

> Plugin de Claude Code `formularios-licencias-subvenciones-y-reclamaciones` · **46 formularios** · Administrativo y Tributario · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para tratar con la Administración fuera de lo tributario: licencias urbanísticas y de actividad, subvenciones (solicitud, subsanación y reintegro), reclamaciones ante la AEPD y la CNMV, sanciones de tráfico y procedimiento sancionador, nacionalidad por residencia, responsabilidad patrimonial, recursos administrativos y escritos de contencioso.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 46 está al final):

- **Demandas, peticiones y solicitudes iniciales** (2). Por ejemplo: Recurso contencioso-administrativo contra la denegación de la nacionalidad española; Recurso contencioso-administrativo por el procedimiento de protección de derechos fundamentales.
- **Contestaciones, oposiciones y alegaciones** (1). Por ejemplo: Alegaciones del interesado en el recurso de reposición contra una sanción de tráfico.
- **Recursos** (7). Por ejemplo: Recurso de reposición contra la denegación de prueba en el proceso contencioso-administrativo; Recurso de alzada ante la Sala de Gobierno del TSJ contra la sanción por mala fe procesal; Recurso de reposición contra una sanción de tráfico relativa al transporte de personas.
- **Contratos, pactos y cláusulas** (5). Por ejemplo: Contrato de colaboración y subvención para un evento musical por procedimiento negociado; Acuerdo de la Sala de Gobierno del TSJ que estima la alzada contra la sanción por mala fe procesal; Acuerdo que declara prescrita la sanción y archiva el expediente sancionador.
- **Estatutos, actas, certificaciones y escrituras** (3). Por ejemplo: Informe del denunciante sobre las alegaciones del denunciado contra la propuesta de resolución; Poder de una asociación vecinal para tramitar la segregación ya iniciada de un núcleo del municipio; Poder de una asociación a favor de un tercero para tramitar la segregación municipal.
- **Comunicaciones, requerimientos y cartas** (15). Por ejemplo: Solicitud de licencia de edificación o de usos en suelo urbano especial; Solicitud de limitación del tratamiento de datos personales (modelo de la AEPD); Solicitud de oposición al tratamiento de datos personales (modelo de la AEPD).
- **Escritos de trámite y otros** (13). Por ejemplo: Escrito de reclamación ante la Comisión Nacional del Mercado de Valores; Otrosí de la demanda contencioso-administrativa pidiendo vista o conclusiones; Escrito por el que se otorga representación a otra persona para actuar en el procedimiento.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Solicitud de licencia de obra»
   - «Reclamación ante la Agencia Española de Protección de Datos»
   - «Subsanación de una solicitud de subvención»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-licencias-subvenciones-y-reclamaciones:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-licencias-subvenciones-y-reclamaciones:escrito-reclamacion-ante-comision-nacional-mercado-adm-0026`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 25-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 2.930 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-licencias-subvenciones-y-reclamaciones@formularios-licencias-subvenciones-y-reclamaciones`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-licencias-subvenciones-y-reclamaciones
/plugin install formularios-licencias-subvenciones-y-reclamaciones@formularios-licencias-subvenciones-y-reclamaciones
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-licencias-subvenciones-y-reclamaciones`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-licencias-subvenciones-y-reclamaciones/releases/latest/download/formularios-licencias-subvenciones-y-reclamaciones.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (46)

| Código | Formulario | Skill |
|---|---|---|
| ADM-0026 | Escrito de reclamación ante la Comisión Nacional del Mercado de Valores | `escrito-reclamacion-ante-comision-nacional-mercado-adm-0026` |
| ADM-0027 | Solicitud de licencia de edificación o de usos en suelo urbano especial | `solicitud-licencia-edificacion-usos-suelo-urbano-adm-0027` |
| ADM-0028 | Solicitud de limitación del tratamiento de datos personales (modelo de la AEPD) | `solicitud-limitacion-tratamiento-datos-personales-adm-0028` |
| ADM-0029 | Solicitud de oposición al tratamiento de datos personales (modelo de la AEPD) | `solicitud-oposicion-tratamiento-datos-personales-adm-0029` |
| ADM-0030 | Solicitud de rectificación de datos personales (modelo de la AEPD) | `solicitud-rectificacion-datos-personales-modelo-aepd-adm-0030` |
| ADM-0031 | Requerimiento de subsanación y mejora de la solicitud de subvención | `requerimiento-subsanacion-mejora-solicitud-subvencion-adm-0031` |
| ADM-0032 | Declaración responsable del solicitante de subvención sobre el cumplimiento de requisitos | `declaracion-responsable-solicitante-subvencion-sobre-adm-0032` |
| ADM-0033 | Contrato de colaboración y subvención para un evento musical por procedimiento negociado | `contrato-colaboracion-subvencion-evento-musical-adm-0033` |
| ADM-0034 | Solicitud de medida cautelar de suspensión del acto administrativo recurrido | `solicitud-medida-cautelar-suspension-acto-adm-0034` |
| ADM-0035 | Otrosí de la demanda contencioso-administrativa pidiendo vista o conclusiones | `otrosi-demanda-contencioso-administrativa-pidiendo-adm-0035` |
| ADM-0036 | Recurso de reposición contra la denegación de prueba en el proceso contencioso-administrativo | `recurso-reposicion-contra-denegacion-prueba-proceso-adm-0036` |
| ADM-0037 | Escrito por el que se otorga representación a otra persona para actuar en el procedimiento | `escrito-otorga-representacion-otra-persona-actuar-adm-0037` |
| ADM-0038 | Escrito pidiendo el trámite de vista o de conclusiones en el proceso contencioso-administrativo | `escrito-pidiendo-tramite-vista-conclusiones-proceso-adm-0038` |
| ADM-0039 | Escrito de conclusiones en el recurso contencioso-administrativo ordinario | `escrito-conclusiones-recurso-contencioso-adm-0039` |
| ADM-0040 | Solicitud de identificación del denunciante y de los funcionarios en un expediente sancionador | `solicitud-identificacion-denunciante-funcionarios-adm-0040` |
| ADM-0041 | Comunicación a Tráfico del arrendatario a largo plazo de un vehículo por su titular | `comunicacion-trafico-arrendatario-largo-plazo-vehiculo-adm-0041` |
| ADM-0042 | Comunicación a Tráfico del fin del arrendamiento a largo plazo de un vehículo por su titular | `comunicacion-trafico-fin-arrendamiento-largo-plazo-adm-0042` |
| ADM-0043 | Consentimiento expreso para figurar como conductor habitual de un vehículo ante Tráfico | `consentimiento-expreso-figurar-como-conductor-habitual-adm-0043` |
| ADM-0044 | Comunicación a Tráfico del conductor habitual por el arrendatario a largo plazo del vehículo | `comunicacion-trafico-conductor-habitual-arrendatario-adm-0044` |
| ADM-0045 | Comunicación a Tráfico del conductor habitual por el titular del vehículo | `comunicacion-trafico-conductor-habitual-titular-adm-0045` |
| ADM-0046 | Recurso contencioso-administrativo contra la denegación de la nacionalidad española | `recurso-contencioso-administrativo-contra-denegacion-adm-0046` |
| ADM-0047 | Recurso contencioso-administrativo por el procedimiento de protección de derechos fundamentales | `recurso-contencioso-administrativo-procedimiento-adm-0047` |
| ADM-0050 | Recurso de alzada ante la Sala de Gobierno del TSJ contra la sanción por mala fe procesal | `recurso-alzada-ante-sala-gobierno-tsj-contra-sancion-adm-0050` |
| ADM-0051 | Acuerdo de la Sala de Gobierno del TSJ que estima la alzada contra la sanción por mala fe procesal | `acuerdo-sala-gobierno-tsj-estima-alzada-contra-sancion-adm-0051` |
| ADM-0052 | Recurso de reposición contra una sanción de tráfico relativa al transporte de personas | `recurso-reposicion-contra-sancion-trafico-relativa-adm-0052` |
| ADM-0053 | Recurso de reposición contra una sanción por infringir las normas de tráfico y seguridad vial | `recurso-reposicion-contra-sancion-infringir-normas-adm-0053` |
| ADM-0054 | Traslado al denunciante de las alegaciones del inculpado contra la propuesta de resolución | `traslado-denunciante-alegaciones-inculpado-contra-adm-0054` |
| ADM-0055 | Informe del denunciante sobre las alegaciones del denunciado contra la propuesta de resolución | `informe-denunciante-sobre-alegaciones-denunciado-adm-0055` |
| ADM-0056 | Alegaciones del interesado en el recurso de reposición contra una sanción de tráfico | `alegaciones-interesado-recurso-reposicion-contra-adm-0056` |
| ADM-0057 | Comunicación del trámite de audiencia a los interesados antes de resolver el recurso administrativo | `comunicacion-tramite-audiencia-interesados-antes-adm-0057` |
| ADM-0058 | Resolución que desestima el recurso de reposición contra una sanción administrativa | `resolucion-desestima-recurso-reposicion-contra-sancion-adm-0058` |
| ADM-0059 | Resolución que estima en todo o en parte el recurso de reposición contra una sanción | `resolucion-estima-todo-parte-recurso-reposicion-contra-adm-0059` |
| ADM-0060 | Acuerdo que declara prescrita la sanción y archiva el expediente sancionador | `acuerdo-declara-prescrita-sancion-archiva-expediente-adm-0060` |
| ADM-0061 | Notificación del inicio del expediente de resarcimiento de daños causados a la Administración | `notificacion-inicio-expediente-resarcimiento-danos-adm-0061` |
| ADM-0062 | Escrito de alegaciones en el expediente para indemnizar a la Administración por los daños causados | `escrito-alegaciones-expediente-indemnizar-adm-0062` |
| ADM-0063 | Traslado a los demás interesados del recurso de reposición contra una sanción de tráfico | `traslado-demas-interesados-recurso-reposicion-contra-adm-0063` |
| ADM-0064 | Acuerdo del órgano competente que archiva el expediente sancionador por caducidad | `acuerdo-organo-competente-archiva-expediente-adm-0064` |
| ADM-0065 | Petición del interesado de un certificado que acredite la caducidad del expediente sancionador | `peticion-interesado-certificado-acredite-caducidad-adm-0065` |
| ADM-0066 | Acuerdo que inicia el resarcimiento de daños no cuantificados en el expediente sancionador | `acuerdo-inicia-resarcimiento-danos-no-cuantificados-adm-0066` |
| ADM-0067 | Poder de una asociación vecinal para tramitar la segregación ya iniciada de un núcleo del municipio | `poder-asociacion-vecinal-tramitar-segregacion-ya-adm-0067` |
| ADM-0068 | Poder de una asociación a favor de un tercero para tramitar la segregación municipal | `poder-asociacion-favor-tercero-tramitar-segregacion-adm-0068` |
| ADM-0069 | Recurso de reposición contra la denegación de la nacionalidad española por residencia | `recurso-reposicion-contra-denegacion-nacionalidad-adm-0069` |
| ADM-0070 | Escrito de interposición del contencioso ante la Audiencia Nacional en materia de nacionalidad | `escrito-interposicion-contencioso-ante-audiencia-adm-0070` |
| ADM-0071 | Reclamación de responsabilidad patrimonial por la denegación indebida de una autorización de trabajo | `reclamacion-responsabilidad-patrimonial-denegacion-adm-0071` |
| ADM-0072 | Escrito de demanda en el contencioso ante la Audiencia Nacional sobre nacionalidad | `escrito-demanda-contencioso-ante-audiencia-nacional-adm-0072` |
| ADM-0073 | Recurso administrativo potestativo de reposición contra un acto de la Administración | `recurso-administrativo-potestativo-reposicion-contra-adm-0073` |

## Privacidad

Ver `PRIVACY.md`.
