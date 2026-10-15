# Cocina — stages 6–15

Etapa aprobada por el Lead el 2026-10-14. Reemplaza stages 1–5 como trabajo activo; el Lead confirmó que todos terminaron el ciclo anterior. No significa que los bugs nuevos estén resueltos.

## Objetivo y equipos

Transformar la base en una cocina diseñada, divertida y confiable. Preservar stages 1–5 y enlace 5→6; la meta está en 15. Los 366 obstáculos / ~4,430 studs reportados son una base modificable, no una cuota.

| Frente | Coordina | Colaborador | Estado inicial |
|---|---|---|---|
| G2-01 diseño, recorrido, ambiente y Explorer | Enrico | Machuc | Ready |
| G2-02 respawn, sistemas e integración | Dhrystone | Vekator | Ready |

Todos comentan y revisan; solo el Lead cierra. El Lead conserva colección/economía/guardado y usa Rojo por separado; los cuatro usan Studio.

## Hitos y dependencias

Referencias y boceto → piloto (Stage 6 sugerida) → feedback del Lead → extensión por secciones → pruebas y cierre. Unas tres referencias, un dibujo y una lista de qué conservar/cambiar bastan.

Diseño y diagnóstico empiezan en paralelo. G2-01 requiere G2-02 Done para cerrar. G2-02 prueba la ruta construida de G2-01 sin exigir que ese ticket esté Done: no hay ciclo de dependencias. Avances parciales se comparten sin entregar toda la tarea.

## Explorer propuesto

    Course
    ├── Stage06 … Stage15
    │   ├── Platforms
    │   ├── Hazards
    │   ├── Decoration
    │   └── Checkpoint (conservar ruta/nombre esperado por scripts)
    └── KitchenSection (elementos compartidos existentes)

Nombres descriptivos y Models para objetos compuestos. No crear carpetas por obligación ni mover/renombrar sin revisar referencias y atributos. Copia recuperable de pruebas retiradas. Otra persona debe encontrar y editar una sección; probar después de organizar.

## Precauciones reales

El arreglo local de respawn en CheckpointPlacement.lua, RatCharacter.server.lua y CourseController.server.luau no está confirmado aplicado ni validado en Studio. Comparar fuentes reales antes de sobrescribir fixes de compañeros.

El builder local reemplaza stages 6–15 y exige 30 obstáculos por stage. No ejecutarlo sobre ediciones manuales sin coordinar y respaldar; esa cifra no es requisito del diseño. No se tocó Studio al publicar tareas.

Humanos prueban gameplay; agentes solo static/edit-mode, sin iniciar Play ni conducir la rata. Guardado de moneda publicado sigue sin prueba confirmada y queda con el Lead; no ampliar pickups, tiendas o economía aquí.

## Criterios de cierre

### G2-01 — Diseñar y transformar la cocina: stages 6–15

- Referencias, boceto y sección piloto revisados antes de extender el diseño
- Stages 6–15 forman una cocina legible, variada y coherente con escala de rata; sin cuota obligatoria de obstáculos
- Cámara, superficies y colisiones corresponden a lo visible; no hay atajos o peligros ocultos accidentales
- Otro compañero encuentra y edita una sección desde Explorer sin perderse; la reorganización no rompe sistemas
- Se probó la ruta final en PC y móvil con feedback del Lead; se conservan stages 1–5 y transición 5→6
- G2-02 aprobada y el Lead verifica la entrega final antes de cerrar

### G2-02 — Estabilizar e integrar la cocina: respawn, obstáculos y pruebas

- Scripts reales de Studio comparados con el arreglo local; se preservaron los fixes de compañeros
- Muerte, RESET y retorno al suelo comprobados en los 15 checkpoints, con repeticiones donde fallaba, sin reaparecer fuera del mapa ni quedar inmóvil
- Hazards, plataformas móviles/desaparecibles y conveyors conservados funcionan y tienen colisiones/tiempos justos
- La reorganización no rompe referencias, atributos o funcionamiento de checkpoints y obstáculos
- Ruta final de G2-01 probada: transición 5→6, progreso independiente con dos jugadores, meta 15 y regresión 1–5; PC/móvil y Output sin errores nuevos en caminos probados
- Evidencia y limitaciones compartidas; aprobación final del Lead

## Ideas propuestas — pendientes de validar

No son tareas asignadas ni requisitos de cierre:

- **I-C01: puente de utensilios y subida por platos.** Aprovecha equilibrio/saltos existentes y escala de rata. Validar referencias, colisiones y qué reemplaza.
- **I-C02: recorrido por el escurridor del fregadero.** Convierte barras en objetos reconocibles. Validar cámara, legibilidad y superficies antes de modelar.
- **I-C03: tabla de cortar con pausas seguras.** Tematiza chopping gates existentes; no añade IA. Validar señales de peligro y ritmo justo.

Propuesta con boceto → comentarios del equipo → validación del Lead → trabajo pendiente priorizado (o aplazar/descartar). No implementar solo por estar escrito aquí. Se pueden proponer alternativas en #lluvia-de-ideas.

## Recursos oficiales

- [Greyboxing](https://create.roblox.com/docs/tutorials/curriculums/environmental-art/greybox-your-environment)
- [Explorer](https://create.roblox.com/docs/studio/explorer)
- [Testing](https://create.roblox.com/docs/studio/testing-modes)
- [Colisiones](https://create.roblox.com/docs/workspace/collisions)

Tarjetas y guías: messages-testing/kitchen-6-15/ en G-industries. Contenido: tools/discord-bot/content/kitchen-6-15.json.

