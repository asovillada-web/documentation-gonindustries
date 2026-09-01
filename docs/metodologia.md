# Workflow de desarrollo

## Del idea al Done

```text
Idea
  ↓ filtro: diversión / alcance / rat identity / aprendizaje
Research breve si hay incertidumbre
  ↓
Decisión registrada si afecta alcance, arquitectura u ownership
  ↓
Tarea Pending clara, sin owner y con Definition of Done
  ↓ alguien disponible la toma
In Progress con owner → Review simple o verificación directa del Lead → Playtest → Fixes
  ↓
Done + documento actualizado si el comportamiento real cambió
```

## Estados

| Estado | Significado |
|---|---|
| `Backlog` | Idea válida, pero no comprometida ahora |
| `Pending` | Accionable y visible para todos, pero todavía sin owner |
| `Ready` | Ya asignada a una persona, pero todavía no iniciada |
| `In Progress` | El owner está trabajando; máximo una principal por persona |
| `Review` | Implementación acabada, pendiente de review/playtest |
| `Done` | Definition of Done comprobada por otra persona |

Si una tarea se bloquea, no se marca `Done` parcial: se anota el bloqueo y se divide o replanifica.

Codex mantiene una cola corta con trabajo de implementación, research, preparación o diseño que realmente mueva el proyecto. En `#tareas`, **Tareas pendientes** muestra las opciones disponibles. Una persona solo puede tomar una si no tiene otra `Ready`, `In Progress` o `Review`. Al tomarla, el sistema elige al azar un reviewer entre los otros cuatro miembros. Las tareas ya asignadas siguen siendo su primer compromiso.

Antes de publicar una Pending, debe quedar claro:

1. qué problema o pregunta del milestone actual resuelve;
2. qué resultado concreto deja y quién lo usará después;
3. que puede hacerse en paralelo sin editar ownership ajeno ni depender de trabajo incompleto;
4. que cabe en una sesión pequeña y tiene `Done when` verificable;
5. qué fuentes oficiales necesita si es research técnico.

Si no cumple estas condiciones, permanece `Backlog`. Mantener muchas opciones nunca justifica adelantar assets, custom characters o sistemas antes de obtener evidencia del prototipo actual.

**Empezar tarea** abre automáticamente el ticket de una tarea asignada. **Tomar** asigna una Pending, la mueve a `In Progress` y también abre su ticket. El owner puede entregar con un botón sin formulario. Si el Lead ya verificó todos los `Done when` en Studio, llamada o pantalla compartida, puede aprobar directamente desde `In Progress`; esto reduce escritura repetida, pero no elimina la verificación real.

Antes de presionar **Empezar tarea**, el owner revisa `#progreso`. Si la tarjeta nombra una dependencia, no comienza hasta verla como `✅ Terminada`. El Lead evita publicar como `Ready` una tarea bloqueada; el canal hace visible la regla, pero no reemplaza ese control de planificación.

## Plantilla de tarea

```md
### S1-XX — Verbo + resultado observable

**What:** Qué cambia.
**Why:** Qué problema del sprint resuelve.
**Owner:** Una persona.
**Reviewer:** Otra persona; para Pending se asigna al azar al tomarla.
**Difficulty:** Easy / Medium / Hard.
**Status:** Backlog / Ready / In Progress / Review / Done.
**Dependencies:** Tareas o “ninguna”.

**Learning (máximo 30–45 min):**
- Concepto necesario y fuente concreta.

**Done when:**
- Resultado observable 1.
- Resultado observable 2.
- Playtest realizado y Output sin errores nuevos.
```

## Definition of Done común

- Cumple todos los criterios específicos de la tarea.
- Otra persona revisó o jugó el cambio.
- No aparecen errores nuevos en Studio Output durante el camino probado.
- Si toca client/server, se probó con Server & Clients, no solo `Play`.
- Si toca input/UI, se hace al menos una prueba con Device/Controller Emulator cuando corresponda.
- No incluye secretos, scripts desconocidos ni trabajo fuera de alcance.
- El documento relevante describe lo que realmente existe.

## Git sin ceremonia excesiva

- `main` representa documentación y herramientas utilizables.
- Una branch corta por tarea basada en archivos: `feat/s1-03-hazard`, `docs/ownership` o `fix/checkpoint-respawn`.
- Commits pequeños que expliquen intención.
- Pull request breve con: qué, cómo probar y captura/log si aporta valor.
- Un reviewer distinto antes de mergear. GitHub documenta que las pull requests permiten discutir y revisar antes de integrar: [About pull requests](https://docs.github.com/en/pull-requests/get-started/about-pull-requests).

Los cambios 3D realizados solo dentro de Team Create no aparecen mágicamente en Git. Su trazabilidad se mantiene con ownership de tarea, notas de publicación y Activity/Version History de Roblox. Los scripts entrarán a Git mediante `Script Sync` cuando se configure.

## Cadencia mínima

- Inicio de sprint: 20 minutos para objetivo, dependencias y owners.
- Durante: updates asíncronos solo cuando cambia estado o existe bloqueo.
- Playtest final: 30–45 minutos; cada persona deja **un problema observado** y **una cosa que funcionó**.
- Cierre: decidir `Done`, mover lo incompleto sin esconderlo y registrar solo decisiones que importan.
