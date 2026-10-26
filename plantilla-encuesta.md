# Plantilla de diseño — Encuesta de satisfacción (hito 1)

**Equipo:** Grupo 5

**Integrantes:** Ganchala Pavel, Lamiña Matias, Magarisca Bryan, Martínez Domenica, Medina Juan

**Fecha:** 20/10/2026

**Repositorio (fork):** https://github.com/pavexl/IDSD422-lab2-diseno-encuesta-grupo-5/blob/main/plantilla-encuesta.md

**Enfoque del equipo (aprobado en clase):** Variedad y stock: satisfacción y disponibilidad.

Completa cada sección. Usa commits por sección; la historia del repositorio se revisa.

> **Formato del entregable:** exporta esta plantilla completada a PDF, con el enlace de tu fork en la carátula, y guarda el PDF en `informes/` del fork. Entrega el PDF y el enlace del fork en el aula virtual.

## 1. Objetivo de la encuesta

Conocer las opiniones y expectativas de los consumidores adultos sobre la variedad y disponibilidad de productos en los supermercados, tomando a RetailAndina S.A. como un caso empresarial hipotético. Con esta información, se busca identificar posibles mejoras en el surtido y la reposición de productos que ayuden a orientar las decisiones de abastecimiento de la gerencia.

## 2. Población objetivo

- **Población:** Personas de 18 años o más que compran en supermercados al menos una vez al mes y que residen en Quito, Guayaquil o Cuenca.

- **Límites y justificación:** La encuesta está dirigida a personas adultas que compran habitualmente en supermercados, ya que pueden compartir sus experiencias y opiniones sobre la variedad y disponibilidad de los productos. Se consideran Quito, Guayaquil y Cuenca porque son las ciudades incluidas en el caso hipotético de RetailAndina S.A. <br> No participarán menores de 18 años ni personas que compren en supermercados con una frecuencia menor a una vez al mes. Además, se trabajará con personas a las que los integrantes del equipo puedan contactar durante el laboratorio y que acepten responder voluntariamente. <br>Como RetailAndina S.A. es una empresa ficticia, no será necesario que los participantes hayan comprado en sus tiendas. Las preguntas se plantearán tomando como referencia la situación hipotética de la empresa y las opiniones de los encuestados sobre la variedad y disponibilidad de productos en los supermercados.

## 3. Método de muestreo

- **Método:** Muestreo no probabilístico por conveniencia y referidos.

- **Tamaño y justificación:** El equipo se propone reunir 25 respuestas reales, con cinco participantes asignados a cada uno de los cinco integrantes. Esta cantidad está dentro del rango de 15 a 30 respuestas solicitado en el laboratorio y permitirá conocer las opiniones y expectativas de los participantes mediante un análisis descriptivo.

- **Cómo se seleccionarán los participantes:** Cada integrante invitará a participar a familiares, amigos, compañeros u otras personas conocidas que cumplan con los requisitos establecidos. También se podrá pedir a quienes respondan la encuesta que compartan la invitación con otras personas que cumplan los mismos criterios. <br>La participación será voluntaria y cada integrante procurará conseguir cinco respuestas válidas. De esta manera, el equipo podrá alcanzar la meta propuesta utilizando los contactos disponibles.<br>Se eligió este método porque el equipo puede contactar directamente a los participantes sin necesidad de disponer de un listado completo de consumidores para seleccionarlos al azar. Sin embargo, como las personas serán elegidas por su accesibilidad y por las recomendaciones de otros participantes, es posible que sus opiniones no representen las de todos los consumidores.<br>Por esta razón, los resultados se utilizarán para describir las respuestas obtenidas, sin generalizarlos estadísticamente a toda la población.

- **Equivalente en código (Python):** <br>El siguiente código permite organizar la meta de respuestas de cada integrante y comprobar cuántas respuestas se espera reunir. La selección de los participantes se realizará mediante invitaciones directas y referidos, no mediante un sorteo aleatorio..

`import pandas as pd`

`integrantes = ["Pavel", "Bryan", "Domenica", "Juan", "Matias"]`

`meta = pd.DataFrame({`<br>
   `"integrante": integrantes,`<br>
    `"respuestas_objetivo": [5, 5, 5, 5, 5]`<br>
`})`

`print(meta)`<br>
`print("Total de respuestas reales previstas:",
      meta["respuestas_objetivo"].sum())`



**Resultado esperado:**  Se mostrará una tabla con los cinco integrantes y una meta de cinco respuestas para cada uno, lo que suma un total de 25 respuestas previstas. Este resultado corresponde a la planificación del equipo y no significa que los participantes ya hayan sido seleccionados o que las respuestas se hayan recopilado.

**Justificación del método:** El muestreo por conveniencia y referidos resulta práctico para el tiempo y los recursos disponibles en el laboratorio. A diferencia del muestreo aleatorio simple o estratificado, no requiere contar con un listado completo de consumidores.

Aun así, se deberá registrar cómo se contactó a los participantes y tener en cuenta que los resultados pueden verse afectados por el sesgo de selección o porque algunas personas decidan no responder. Estas limitaciones se considerarán al interpretar los resultados.

## 4. Cuestionario (5–10 preguntas)

La encuesta presenta a RetailAndina S.A. como una cadena de supermercados hipotética. Las preguntas buscan conocer los hábitos de compra de los participantes y sus opiniones sobre la variedad y disponibilidad de productos. Por lo tanto, no es necesario que hayan comprado anteriormente en RetailAndina para responder.

| # | Pregunta | Tipo de variable | Dtype al cargar | Opciones / escala |
|---|---|---|---|---|
| 1 | ¿Tiene usted 18 años o más? | Categórica binaria | `object` | Sí; No |
| 2 | ¿Con qué frecuencia compra en supermercados? | Categórica ordinal  | `object` | Varias veces por semana; Una vez por semana; De dos a tres veces al mes; Una vez al mes; Menos de una vez al mes |
| 3 | ¿En qué ciudad reside actualmente? | Categórica nominal | `object` | Quito; Guayaquil; Cuenca |
| 4 | ¿Qué tan importante es para usted que un supermercado ofrezca una amplia variedad de productos? | Categórica ordinal | `object` | Nada importante; Poco importante; Moderadamente importante; Importante; Muy importante |
| 5 | ¿Qué tan importante es para usted que los productos que busca estén disponibles cuando visita un supermercado? | Categórica ordinal | `object` | Nada importante; Poco importante; Moderadamente importante; Importante; Muy importante |
| 6 | ¿Con qué frecuencia encuentra disponibles los productos que busca en los supermercados que visita habitualmente? | Categórica ordinal | `object` | Nunca; Casi nunca; Algunas veces; Casi siempre; Siempre |
| 7 | ¿En qué categoría de productos encuentra con mayor frecuencia faltantes en los supermercados que visita? | Categórica nominal | `object` | Alimentos frescos; Productos empacados; Bebidas; Limpieza del hogar; Cuidado personal; Otra; No he encontrado faltantes |
| 8 | Si una cadena de supermercados como la hipotética RetailAndina ofreciera una amplia variedad de productos, ¿qué tan satisfecho estaría con esa variedad? | Categórica ordinal | `object` | Muy insatisfecho; Insatisfecho; Ni satisfecho ni insatisfecho; Satisfecho; Muy satisfecho |
| 9 | Si una cadena de supermercados como la hipotética RetailAndina mantuviera disponibles los productos que busca, ¿qué tan satisfecho estaría con esa disponibilidad? | Categórica ordinal | `object` | Muy insatisfecho; Insatisfecho; Ni satisfecho ni insatisfecho; Satisfecho; Muy satisfecho |
| 10 | ¿Qué tan importante sería para usted que una cadena de supermercados como RetailAndina ofreciera una experiencia de compra satisfactoria en cuanto a la variedad y disponibilidad de productos? | Categórica ordinal |`object` | Nada importante; Poco importante; Moderadamente importante; Importante; Muy importante |

Se espera que las respuestas se carguen como texto (object en pandas). Sin embargo, el tipo de dato definitivo deberá comprobarse al ejecutar el script de verificación con los datos recopilados.

## 5. Análisis de sesgos

*Identifica 2 problemas potenciales de esta encuesta y su mitigación.*

| Sesgo potencial | Mitigación |
|---|---|
| 1. | |
| 2. | |

## 6. Confidencialidad (RA3)

- Datos personales que se piden y por qué:
- Plan de anonimización (qué se quita o codifica antes de compartir):

## 7. Verificación con herramientas (Python/R)

*Escribe `scripts/verificacion_encuesta.py` (o `.R`): debe cargar `plantillas/encuesta_respuestas.csv` y reportar los tipos de cada columna, los datos faltantes por columna y la distribución de `satisfaccion_general` y `recomendaria`. Incluye la salida y responde:*

- ¿Coinciden los tipos con tu predicción de la sección 4?
- ¿Cuántos datos faltantes hay por columna?

*Ejecuta el script sobre el CSV final (separa con un filtro de la columna `origen` las filas reales de las simuladas): ¿qué resultado delataría un sesgo de **no respuesta** y cuál un sesgo de **respuesta**? Escribe tu interpretación usando solo las respuestas reales.*
