Using CbatGPT
# Primer prompt
## Rol
Eres un experto **product manager** que trabaja en una startp.
Tu objetivo es definir las funcionalidades clave que harán brillar a LTI .
LTI es un sistema **ATS (Applicant-Tracking System)** del futuro.
Todavía no hay nada creado, así que toca ponerse el gorro de product manager y **definir esas funcionalidades clave que harán brillar a LTI por encima de los competidores**: aumentar la eficiencia para los departamentos de HR, mejorar la colaboración en tiempo real entre reclutadores y managers, automatizaciones, asistencia de IA en diversas tareas... es el momento de hacer brainstorming, investigar cuáles pueden ser las claves del éxito, y dejarlo plasmado para el resto del equipo.
Usa la imagen que te paso para definir el sistema LTI.

## Objetivos

Tu misión es **diseñar la primera versión del sistema**, entregando los siguientes artefactos:

1. **Descripción breve del software LTI**, valor añadido y ventajas competitivas. Explicación de las funciones principales. Añadir un diagrama Lean Canvas para entender el modelo de negocio.
2. **Descripción de los 3 casos de uso principales**, con el diagrama asociado a cada uno.
3. **Modelo de datos** que cubra entidades, atributos (nombre y tipo) y relaciones.
4. **Diseño del sistema a alto nivel**, tanto explicado como diagrama adjunto.
5. **Diagrama C4** que llegue en profundidad a uno de los componentes del sistema, el que prefieras.

## Salida

Documenta todo en un único documento markdown (`.md`).

# Segundo prompt
genera los diagramas con mermeaid y adjuntalos al documento markdown.

# Tercer prompt
ahora como **experto arquitecto software** quiero que mejores los siguientes apartados:
3. **Modelo de datos** que cubra entidades, atributos (nombre y tipo) y relaciones.
4. **Diseño del sistema a alto nivel**, tanto explicado como diagrama adjunto.
5. **Diagrama C4** que llegue en profundidad a uno de los componentes del sistema, el que prefieras.

# Tercer prompt
ahora como **experto arquitecto software** quiero que mejores los siguientes apartados:
3. **Modelo de datos** que cubra entidades, atributos (nombre y tipo) y relaciones.
4. **Diseño del sistema a alto nivel**, tanto explicado como diagrama adjunto.
5. **Diagrama C4** que llegue en profundidad a uno de los componentes del sistema, el que prefieras.

# Cuarto prompt
quiero que añadas diagramas hechos en mermaid para los apartados 2, 3, 4 y 5