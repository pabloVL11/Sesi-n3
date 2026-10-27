# Historias de usuario de búsqueda

| Campo | Valor |
| --- | --- |
| Proyecto | Proyecto Simbiosis |
| Fecha | [dd/mm/aaaa] |
| Versión | [Versión de trabajo] |
| Estado | Borrador |

## Fuentes comunes

- [Acta de UC-21 Buscar recetas](../captura/acta-acuerdos-uc-21-buscar-recetas.md), v1.1, Vigente.
- [Catálogo de requisitos](catalogo-requisitos.md), UR-08 y FR pertinentes.
- [Modelo de casos de uso](../modelos/modelo-casos-de-uso.md), UC-21.

## Épica de búsqueda

Como usuario registrado, quiero realizar una búsqueda de recetas mediante palabras clave, ingredientes seleccionados e ingredientes excluidos, para localizar una receta que cumpla mis criterios y consultar su detalle.

**Estado:** descompuesta en US-01, US-02 y US-03. Conserva la necesidad conjunta.

## Justificación de la división

La división se realiza en base a los 3 criterios posibles para realizar la búsqueda de recetas. Cada una produce resultados de búsqueda y se pueden combinar.


## US-01

**Título:** Buscar recetas mediante palabras clave

Como usuario registrado, quiero introducir palabras clave como criterio de búsqueda, para encontrar recetas relacionadas a las palabras clave que me interesan.

**Fuentes:** UR-08; UC-21; FR-85; acta, apartado 2.

### Criterios de aceptación

- **CA-01.** Dado que haya una receta publicada con la palabra "calabacín" en el título o descripción, cuado el usuario realiza una búsqueda mediante la palabra "calabacín", entonces esta receta se mostrará entre los resultados de la búsqueda.
- **CA-02.** Dado que haya una receta publicada con las palabras "arroz integral" en su título o descripción y otras que contengan unicamente "arroz" o "integral", cuando el usuario realiza una búsqueda mediante la palabra "arroz integral", entonces solo la primera se mostrará entre los resultados de la búsqueda.
- **CA-03.** Dado que no haya ninguna receta publicada que contenga las palabras "huevos cocidos", cuando el usuario realiza una búsqueda mediante las palabras clave "huevos cocidos", entonces se informará al usuario de que no hay ninguna receta publicada conforme a ese criterio y no se realizará la búsqueda, conservando los criterios.

## US-02

**Título:** Buscar recetas mediante ingredientes contenidos

Como usuario registrado, quiero introducir ingredientes usados en una receta como criterio de búsqueda, para encontrar recetas que contengan los ingredientes que me interesan.

**Fuentes:** UR-08; UC-21; FR-86; acta, apartado 2.

### Criterios de aceptación

- **CA-01.** Dado que haya una receta publicada que use calabacín como ingrediente, cuando el usuario realiza una búsqueda incluyendo calabacín en los ingredientes deseados, entonces esta receta se mostrará entre los resultados de la búsqueda.
- **CA-02.**  Dado que haya una receta publicada que use calabacín como ingrediente, cuando el usuario realiza una búsqueda incluyendo calabacín y arroz en los ingredientes deseados, entonces esta receta no se mostrará entre los resultados de la búsqueda.
- **CA-03.** Dado que no haya ninguna receta publicada que use calabacín como ingrediente, cuando el usuario realiza una búsqueda incluyendo calabacín en los ingredientes deseados, entonces se informará al usuario de que no hay ninguna receta publicada conforme a ese criterio y no se realizará la búsqueda, conservando los criterios

## US-03

**Título:** Buscar recetas mediante ingredientes excluidos

Como usuario registrado, quiero excluir ingredientes usados en una receta como criterio de búsqueda, para encontrar recetas que no contengan ingredientes que no quiero utilizar.

**Fuentes:** UR-08; UC-21; FR-87; acta, apartado 2.

### Criterios de aceptación

- **CA-01.** Dado que haya una receta publicada que use calabacín como ingrediente, cuando el usuario realiza una búsqueda excluyendo calabacín de los ingredientes deseados, entonces esta receta no se mostrará entre los resultados de la búsqueda.
- **CA-02.** Dado que haya una receta publicada que use calabacín y arroz como ingredientes y recetas que solo contienen arroz, cuando el usuario realiza una búsqueda excluyendo calabacín de los ingredientes deseados, entonces solo las recetas que contienen únicamente arroz se mostrarán entre los resultados de la búsqueda.
- **CA-03.** Dado [situación], cuando [acción], entonces [resultado observable].

## Revisión INVEST

La revisión abarca US-01, US-02 y US-03. «Aplicado» indica si se ha realizado la comprobación. «Cumple» indica si todas las historias cumplen el criterio. Si alguna no lo cumple, indicar «No» e identificar la historia y el motivo en la justificación. Si no se ha realizado la comprobación o faltan datos, indicar «Pendiente» en «Cumple».

| Criterio | Pregunta de revisión | Aplicado | Cumple | Justificación |
| --- | --- | --- | --- | --- |
| Independiente | ¿Puede implementarse cada historia y ofrecer un resultado útil sin implementar antes las otras historias del conjunto? Puede compartir infraestructura con ellas. | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Negociable | ¿Cada historia explica qué necesita la persona y deja margen para discutir los detalles de la solución, respetando los acuerdos confirmados? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Valiosa | ¿La parte «para…» de cada historia explica el beneficio que obtiene la persona al usar esa capacidad? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Estimable | ¿Están claros el alcance y los datos necesarios para estimar el trabajo de cada historia? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Pequeña | ¿Se centra cada historia en una única capacidad de alcance manejable? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |
| Comprobable | ¿Los criterios de aceptación de cada historia describen acciones y resultados observables que permiten distinguir un comportamiento correcto de uno incorrecto? | [Sí/No] | [Sí/No/Pendiente] | [Historias y motivo] |

## Dudas pendientes

[Cuestiones pendientes de aclaración. Si no quedan cuestiones, indicar «Ninguna».]
