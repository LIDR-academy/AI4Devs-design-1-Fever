# Servicio
Claude Sonnet 3.5

# Consideraciones

Para este ejercicio he creado un proyecto y lo he alimentado con el siguiente contenido:

- Los textos teóricos del curso.
- La siguiente descripción del proyecto:
> Este proyecto contiene todo el material didáctico y enunciado de ejercicios liberado por la academia online de AI4Devs en la que se enseña a utilizar herramientas de inteligencia Artificial para Ingenieros de Software para ser más productivos.

- Las siguientes instrucciones de comportamiento
> Eres un consultor de alumnos de la Academia AI4Devs, una academia cuyo ánimo es potenciar a los ingenieros de software gracias a la inteligencia artificial. Ambos somos ingenieros de software y somos amigos. Te has enterado de que estoy haciendo el curso y me vas a ayudar con cualquier duda que tenga, así como a hacer las tareas entregables que las vamos a hacer juntos.
> 
> Me vas a hablar de forma clara, directa, sin reiterar en tus mensajes cuál es tu papel.

# Prompts:
## Inicio:
> Buenas! Qué te parece si nos ponemos a resolver la tarea ✍️ Diseño de un sistema de gestión de candidatos 🔴 ?

Aquí me plantea un plan de acción y me pregunta por donde quiero empezar

## Promp 2:
> Empecemos por el principio. Vamos a hacer la descripción del software y a hacer el lean+canvas

Aquí ha empezado con la primera parte del ejercicio generando el canvas en formato mermaid, pero me ha sugerido hacerlo en html en una tabla 3x3 que es el formato por defecto para estos escenarios.

## Promp 3:
> Sí, es mejor que lo hagas en html con la tabla con layout tradicional 3x3

Aquí genera la tabla y me propone continuar con los casos de uso

## Promp 4:
> Sí, pasemos a los casos de uso

Aquí genera todos los casos de uso y el diagrama mermeid de todos ellos, pero como teníamos hacer los diagramas por separado así como los casos de uso, he iterado tal que así

## Promp 5:
> Excelente. Hagamos cada caso de uso por separado con su diagrama Mermaid. Empecemos por el primero de gestión de ofertas

Lo ha hecho perfecto, aunque no ha generado la descripción del caso de uso en formato markdown y lo he formateado yo a mano mas o menos.

## Promp 6:
> Vamos a por el siguiente caso de uso: Proceso de evaluación de candidatos con IA

Lo ha hecho bien, igual que en el caso anterior pero esta vez no quería editar el markdown a mano por lo que el siguiente prompt ha sido:

## Promp 7:
> Podrías generar la descripción del caso de uso en formato markdown?


## Promp 8:
> Muy bien! Vamos ahora a por el tercer caso de uso: Portal del Candidato. Necesito que la descripción del caso de uso la generes en formato markdown y que generes igual que en todos los casos anteriores el diagrama

Lo ha hecho perfecto y me ha preguntado si quería revisar algo o pasar al modelo de datos

## Promp 9:
> No. Lo tenemos todo. Pasemos al modelo de datos. ¿Cómo deberíamos abordarlo?

Aquí me ha presentado un plan con los modelos y demás que íbamos a necesitar y me ha preguntado que si lo veo bien para empezar con la implementación del diagrama ER

## Promp 10:
> Si no te falta nada, comencemos con el digrama ER

Ha generado el diagrama y me ha preguntado si quería profundizar en algo o hacer algún ajuste

## Promp 11:
> No, así está bien. Ahora tenemos que pasar al siguiente punto del ejercicio que es "Diseño del sistema a alto nivel, tanto explicado como diagrama adjunto."

Aquí ha cometido un error de sintaxis con el diagrama mermaid

## Promp 12:
> Hay un error en diagrama mermaid:
> ```
> ``Error: Error: Parse error on line 41:
> ...UTH GW --> Core Services JO
> ----------------------^
> Expecting 'SEMI', 'NEWLINE', 'EOF', 'AMP', 'START_LINK', 'LINK', got 'NODE_STRING'
> ```

Lo ha corregido y me preguntado si pasábamos al siguiente punto de los diagramas C4

## Promp 13:
> Perfecto. Pues sí. Vamos a por el diagrama C4

Aquí ha generado los 3 diagramas en formato mermaid, pero utilizando sintaxis de algunos programas de diagramas C4, así como el markdown de la descripción.

## Promp 14:
> Los tres diagramas mermaid muestran errores similares con esta pinta:
> ```
> Error: Error: Lexical error on line 30:. Unrecognized text.
> ...Config($c4ShapeInRow=3, $c4BoundaryInRow
> -----------------------^ 
> ```

Y aquí ya lo ha corregido y he finalizado el ejercicio.
