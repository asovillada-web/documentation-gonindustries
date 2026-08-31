# Requisitos ligeros del juego

Este documento cumple el propósito práctico de una SRS para nuestro MVP. Está inspirado en la organización de requisitos formales, pero no declara cumplimiento con IEEE 830 ni con otro estándar.

## Propósito

Construir un obby de Roblox pequeño en el que la escala, la ruta y el entorno hagan sentir al jugador como una rata. El primer release debe ser terminable por un equipo principiante y servir como aprendizaje real de Studio, scripting, modeling, testing y colaboración.

## Usuarios

- Jugadores de Roblox que entienden los controles básicos de un obby.
- El equipo de cinco personas que necesita editar, probar y publicar el experience.

## Requisitos funcionales del MVP

| ID | El juego debe… | Aceptación |
|---|---|---|
| RF-01 | Permitir aparecer y recorrer el nivel con controles Roblox estándar. | Un jugador nuevo puede moverse y saltar sin instrucciones especiales. |
| RF-02 | Tener un recorrido claro de principio a fin. | Otra persona llega a la meta sin guía por voz. |
| RF-03 | Incluir hazards simples con respawn fiable. | El hazard probado reinicia al jugador cada vez sin errores nuevos. |
| RF-04 | Conservar el último checkpoint durante la sesión. | Tras tocarlo y morir, ese jugador reaparece allí; otro jugador no se ve afectado. |
| RF-05 | Comunicar victoria de forma básica. | Llegar a la meta produce feedback visible y no se activa antes. |
| RF-06 | Comunicar la fantasía de rata. | El playtest reconoce escala diminuta, objetos cotidianos gigantes y una meta contextual. |

## Requisitos no funcionales iniciales

- El recorrido completo objetivo dura entre 3 y 5 minutos; primero validamos una slice de 30–60 segundos.
- El camino principal no produce errores nuevos en `Output`.
- Checkpoints, victoria y progreso compartido son decididos por el server.
- El juego recibe una prueba básica en teclado, móvil y controller antes del release.
- Los assets importantes pertenecen al Group cuando el workflow lo permita.
- Un principiante del equipo puede explicar el código que entrega.

## Fuera del MVP

- Economía o tienda.
- Guardado persistente.
- Múltiples mundos o 50/100 niveles desde el inicio.
- IA compleja de gatos o humanos.
- Matchmaking, monetización o frameworks propios.
- Movimiento de escalada personalizado antes de validar el obby normal.

## Cambios

Un requisito nuevo no entra automáticamente al MVP. Primero pasa por el filtro de diversión, alcance, identidad de rata y aprendizaje; si cambia el alcance, se registra en [decisiones.md](decisiones.md).
