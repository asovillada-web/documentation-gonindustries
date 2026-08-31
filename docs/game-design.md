# Game design: hipótesis que vamos a probar

Esto no es una especificación final. Es la hipótesis más pequeña que permite obtener feedback jugando.

## Resumen jugable provisional

> Eres una rata diminuta que debe cruzar una zona cotidiana enorme y llegar a un agujero seguro. Saltas sobre objetos reconocibles, evitas peligros simples y reapareces en checkpoints cercanos.

Primer escenario candidato: una **despensa/cocina**. Comunica la escala con objetos conocidos, permite obstáculos fáciles de construir y hace legible el objetivo “escapar al agujero”. Se confirma o descarta después de la primera prueba, no por debate abstracto.

## Qué hace especial al concepto

La prioridad no es inventar un controller complejo. La identidad de rata debe venir primero de:

- Escala: objetos normales se sienten gigantes.
- Ruta: bordes, estantes, latas, cajas, tuberías o huecos que una persona no usaría.
- Silueta y feedback: un placeholder reconocible de rata y uno o dos detalles graciosos.
- Objetivo contextual: alcanzar un rat hole, no una meta genérica flotante.

## Vertical slice de validación

Duración objetivo: 30–60 segundos.

- Spawn claro.
- Tres a cinco saltos/obstáculos hechos con Parts.
- Un hazard que reinicia al jugador.
- Un checkpoint.
- Un goal visible.
- Uno o dos props gigantes de prueba.
- Default Humanoid antes de un movimiento personalizado.

La pregunta del playtest es: **¿la escala y la ruta ya hacen sentir que somos una rata, aunque casi todo sea greybox?**

## MVP si la hipótesis funciona

- Un solo recorrido de 3–5 minutos.
- Checkpoints y respawn fiables.
- Un principio, una meta y feedback básico de victoria.
- Una sola identidad visual coherente.
- Controles Roblox estándar, con prueba básica en teclado, móvil y controller.
- Una rata visual sencilla o un stand-in convincente; no hace falta un sistema de avatar avanzado.

## Filtro de ideas

| Idea | Rat identity | Coste | Decisión MVP |
|---|---:|---:|---|
| Escala diminuta + objetos gigantes | Alta | Baja | Mantener |
| Cocina/despensa | Alta | Baja-media | Probar primero |
| Hazards estáticos (agua, ratonera, caída) | Media-alta | Baja | Mantener, pocos |
| Queso como señal de ruta | Media | Baja | Probar visualmente |
| Economía/contador persistente de queso | Media | Media-alta | Aplazar |
| Un rat hole como meta | Alta | Baja | Mantener |
| Shortcuts por rat holes | Alta | Media | Aplazar hasta que exista nivel |
| Cat/human chase con IA | Alta | Alta | Fuera del MVP |
| Movimiento de escalada personalizado | Alta | Alta | Fuera del MVP |
| Múltiples mundos o niveles | Media | Alta | Fuera del MVP |

## Preguntas abiertas para el primer playtest

1. ¿La diversión viene del platforming, de la escala o de la comedia visual?
2. ¿La cocina se lee mejor que una alcantarilla/tubería con el mismo esfuerzo?
3. ¿El default Humanoid se siente suficientemente bien para terminar un MVP?
4. ¿El prop de rata necesita ser el personaje jugable ya, o puede esperar a que el curso sea divertido?

