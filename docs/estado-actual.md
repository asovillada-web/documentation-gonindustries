# Step 4 — Entrar a Gon Industries

**Estado real:** Dhrystone y Vekatorke ya tienen acceso; Enrico y Machuc siguen pendientes de confirmación. En el task manager, los cuatro tickets continúan `In Progress` hasta que el Lead cierre formalmente cada review como `Done`.  
**Objetivo:** incorporar las cuentas correctas al Group con el rol mínimo antes de abrir Roblox Studio juntos.

## Acceso del equipo

Enrico y Machuc todavía siguen [Entrar a Gon Industries](tasks/step-04-unirse-al-grupo.md). Cada uno:

1. Usa la cuenta de Roblox con la que trabajará.
2. Envía friend request a `treapath`.
3. Abre su ticket y comparte su username exacto.
4. El Lead lo invita al rol `Developer`.
5. Acepta la invitación y usa **Entregar tarea**, o deja que el Lead la cierre directamente si ya confirmó el acceso.

El Lead actúa como reviewer, envía las invitaciones y verifica el rol antes de aprobar `Done`. Tener acceso real no cambia automáticamente el estado del ticket: `#progreso` muestra el estado guardado en Supabase.

## Piloto del siguiente step

La tarea visual `TEST` del Lead fue eliminada. El Lead recibió únicamente `S1-01 — Preparar el campo de práctica`, con instrucciones detalladas para crear `Workspace/Prototype` y sus zonas. Su tarjeta ya usa el embed aprobado con `¿Qué hacer primero?`, documentación/puntos/keywords y `Al finalizar:`.

S1-02 a S1-05 siguen fuera del bot y no hubo anuncio. Sus vistas previas están en `messages-testing/`; cuando Enrico y Machuc terminen el acceso y S1-01 sea revisada, el Lead decide cuál publicar.

Las tarjetas incorporan `📘 Información detallada`: el resumen permanece compacto y la explicación completa se envía por DM. La guía del piloto vive en `messages-testing/details/lead.md`; las cuatro futuras están preparadas en la misma carpeta pero sus tareas siguen sin publicar.

`#progreso` está fuera de categorías y registra el estado de todas las tareas publicadas. S1-01 es la base: S1-02 a S1-05 no se empiezan ni se publican hasta verla como `✅ Terminada` en ese tablero.

El workflow final de Discord ya no usa un formulario de entrega: **Empezar tarea** abre el ticket, **Entregar tarea** manda a `Review` con un click y el Lead puede usar **Aprobar y cerrar** desde `In Progress` cuando ya verificó el resultado.
