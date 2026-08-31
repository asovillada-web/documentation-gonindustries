# Equipo y ownership inicial

Las áreas son provisionales para el primer prototipo. Tener owner significa coordinar y poder explicar ese sistema, no trabajar solo ni decidir sin review.

| Persona | Ownership inicial | Oportunidad de aprendizaje | No significa |
|---|---|---|---|
| Project Lead | alcance, prioridades, acceso, roadmap, integración y release | fundamentos de todos los sistemas y revisión | hacer el trabajo que otros no terminan |
| Dhrystone | hazards y lógica server-side pequeña | eventos, `Script`, validación y debugging | ser “backend” de todo el juego |
| Enrico | greybox y gameplay moment-to-moment | Parts, físicas, playtest y scripting de gameplay | diseñar todo el juego solo |
| Machuc | escala visual, props, entorno y asset pipeline | studs, importación, budget y assets de Group | producir arte final antes del prototype |
| Vekatorke | checkpoints, progreso de sesión y pruebas client/server | estado autoritativo, respawn y multiplayer tests | crear sistemas de datos prematuros |

## Responsabilidades compartidas

- Todos juegan cada vertical slice y dejan una observación concreta.
- Quien implementa actualiza la nota corta del sistema o tarea.
- Cada tarea tiene un reviewer distinto del owner.
- Nadie edita un sistema ajeno sin avisar al owner.
- Si alguien queda bloqueado más de 20–30 minutos, publica qué intentó, error exacto y siguiente hipótesis en `#desarrollo`.
- El lead protege el alcance y redistribuye trabajo; no absorbe silenciosamente tareas atrasadas.

## Parejas de review sugeridas

- Dhrystone ↔ Vekatorke para lógica server-side.
- Enrico ↔ Project Lead para gameplay/greybox.
- Machuc ↔ Enrico para escala y colisiones del nivel.

Las parejas rotan después del primer sprint para que todos aprendan a explicar y revisar.

