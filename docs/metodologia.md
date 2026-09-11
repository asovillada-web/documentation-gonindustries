# Metodología del equipo

Recuperada del handbook y ajustada por decisión del Lead el 2026-09-10.

**Idea → research cuando haga falta → acuerdo → tarea → implementación → review/playtest → correcciones → Done.** Actualizamos documentación solo si cambia algo que merezca conservarse.

## Etapa actual: frentes compartidos

Cada frente tiene un responsable que coordina, colaboradores, objetivo, dificultad, dependencias y resultado observable. Todos los cinco pueden leer el ticket, aportar y comentar la revisión. Solo el Lead aprueba y cierra. Un coordinador no tiene que hacer todo el trabajo.

- **Ready:** disponible, todavía sin iniciar. El ticket compartido ya existe.
- **In Progress:** responsable o colaborador empezó; máximo un frente principal en curso por coordinador. Apoyo puntual en otro frente no significa asumirlo completo.
- **Review:** entrega final del frente, pendiente de feedback/aprobación. Un avance parcial se comparte como mensaje, no mueve toda la tarea a Review.
- **Done:** el Lead comprobó los criterios y aprobó; ticket a Historial, sin perder evidencia.
- **Backlog:** fuera del compromiso actual. Las tareas retiradas se archivan sin declarar que fueron completadas.

## Trabajo cotidiano

1. Mirar #progreso y el contexto del frente. Acordar quién toca cada sección o Script.
2. Proponer una sección pequeña, construir/probar y compartir el avance; extender cuando funcione.
3. Cualquier miembro comenta problemas y sugerencias. Autor y colaboradores entregan con un botón, sin formulario/checklist automático.
4. El Lead puede aprobar desde In Progress si ya comprobó el resultado; **Pedir cambios** desde Review devuelve al mismo ticket.

Las dependencias de inicio impiden comenzar; las de cierre permiten preparación y pruebas parciales. En esta etapa G1-01 requiere G1-02 Done para cerrarse y G1-04 requiere G1-01/02/03 Done. No se crea un ciclo que impida trabajar en paralelo.

## Calidad común

Otra persona prueba el cambio; Output sin errores nuevos en el camino probado; Server & Clients si afecta progreso compartido; PC/móvil para recorrido y UI. Registrar qué se probó y qué falta. No esconder pendientes bajo un Done.

Todo cambio sobre objetos o scripts ajenos se coordina. Los cuatro compañeros usan Studio en Windows. Solo el Lead usa Rojo y adapta su sincronización; nadie debe instalarlo para trabajar. Conservar versiones y no sobrescribir trabajo compartido.

## Planificación sin saturar

El siguiente objetivo es [stages 1–5](sprints/stages-1-5.md), no 50/100 etapas ni un framework. Revisar avances cada semana sin exigir todo terminado en una semana. Codex prepara/actualiza tareas durante nuestras sesiones; no se promete generación autónoma continua.

La cola individual con reviewer al azar queda como mecanismo disponible para tareas pequeñas futuras; **no es el modelo activo de estos cuatro frentes**. Antes de ampliar backlog, comprobar que la nueva tarea aporta a la meta y no duplica trabajo.
