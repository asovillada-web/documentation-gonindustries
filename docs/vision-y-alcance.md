# Brief canónico del proyecto

Última actualización: 2026-08-29.

## Proyecto y propósito

Somos cinco amigos comenzando nuestro primer proyecto grupal de game development. Queremos aprender a organizarnos, investigar, documentar, diseñar, programar, modelar, revisar y probar mientras terminamos un juego pequeño. No buscamos producir la mayor cantidad de código; buscamos convertirnos pronto en un equipo que funciona y publica algo terminado.

La primera plataforma de desarrollo es **Roblox Studio** y el hub de comunicación es **Discord**. El primer juego se llama provisionalmente **“Obby but You're a Rat”**: un obstacle course pequeño, gracioso y expandible donde el jugador es o se siente como una rata.

El concepto exacto todavía debe validarse. Las ideas disponibles incluyen escala diminuta, cocinas, tuberías, basura, queso, ratoneras, agujeros de rata, humanos y gatos. Ninguna idea es automáticamente una feature. Se evalúa con cuatro preguntas:

1. ¿Es divertida?
2. ¿Es alcanzable por principiantes?
3. ¿Refuerza la fantasía de ser una rata?
4. ¿Enseña algo útil para terminar el juego?

## Equipo

- **Project Lead:** boss, organizer y coordinador. Puede trabajar en cualquier área, distribuye tareas y también debe tener trabajo propio sin convertirse en quien hace todo. Usa Linux y ejecuta Roblox Studio mediante Vinegar.
- **Dhrystone:** programmer en formación, interesado en backend/programming.
- **Enrico:** programmer en formación, disponible para scripting, gameplay y tareas técnicas.
- **Machuc:** 3D modeler con experiencia previa; dueño natural de props, entorno y pipeline de assets, aprendiendo el flujo específico de Roblox.
- **Vekatorke:** programmer en formación, disponible para scripting, gameplay y tareas técnicas.

Todos están dispuestos a aprender. Las responsabilidades son áreas de ownership, no silos: todos playtestean, documentan lo que cambian y revisan a otra persona. Los detalles están en [equipo-y-roles.md](equipo-y-roles.md).

Dhrystone, Enrico, Machuc y Vekatorke usan Windows. Las instrucciones de paths, instalación y troubleshooting deben separar Windows de Linux/Vinegar cuando exista una diferencia real.

## Principios no negociables

- Construir primero un **Minimum Viable Game** pequeño, gracioso, jugable, aprendible y terminable.
- Aprender mediante tareas conectadas al juego, no mediante una enciclopedia previa.
- Documentar poco, corto y útil; cada documento debe apoyar una decisión o tarea real.
- Dar a cada tarea objetivo, motivo, owner, dificultad, estado, dependencias y Definition of Done.
- Investigar antes de afirmar prácticas o APIs actuales.
- Usar herramientas solo cuando resuelvan un problema presente; su complejidad también cuesta.
- Probar gameplay pronto y arte final después de validar la experiencia básica.
- Mantener ownership claro y evitar que todos editen el mismo sistema a la vez.
- Revisar código para entenderlo; nunca pegar código aleatorio sin poder explicarlo.
- Trabajar en steps semanales y mantener visible solo el trabajo actual; los planes posteriores son borradores, no compromisos.

## Función del asistente técnico

El asistente actúa como technical guide, research assistant, project organizer, teacher, code reviewer y development guide. Debe mantener contexto sobre equipo, roles, tareas, decisiones, arquitectura, documentos, bugs, hitos y diseño. Explica qué, por qué y siguiente paso; implementa la solución práctica más pequeña; advierte ante beginner traps.

Cuando una decisión cambia, se actualiza [decisiones.md](decisiones.md). Cuando un sistema cambia, se actualiza su documento real. Cuando una tarea se completa, se comprueba su Definition of Done antes de marcarla `Done`.

## Organización deseada

El flujo objetivo es:

```text
Idea → filtro/research → decisión → tarea → implementación
     → review → playtest → fixes → Done → documentación real
```

Estados: `Backlog`, `Ready`, `In Progress`, `Review`, `Done`. Dificultad: `Easy`, `Medium`, `Hard`. Una dependencia bloqueante impide mover una tarea a `Ready`.

## Discord

Discord debe permitir comunicación, anuncios, tareas, bugs, ideas, progreso, diseño, programación, modeling y playtests sin crear docenas de canales. `#progreso`, fuera de categorías, conserva un solo tablero read-only con tareas publicadas pendientes/activas y terminadas; es la comprobación obligatoria antes de iniciar una dependencia. La capa local crea/reutiliza la estructura y envía anuncios. El task manager serverless usa buttons, DMs best-effort, fallback ephemeral, estados persistentes y un review channel privado por entrega; reviews activas y archivo Done viven separados. Slash commands (`/project`, `/docs`, `/bug`, etc.) siguen aplazados hasta demostrar una necesidad real.

El token del bot nunca entra al código ni al repositorio. La guía debe cubrir registro, credenciales, instalación, permisos mínimos, ejecución local, variables de entorno, mensaje de prueba y evolución posterior.

## Áreas de trabajo que habrá que cubrir

- **Gameplay:** control de personaje, obstáculos, hazards, checkpoints, respawn, meta y progresión mínima.
- **World:** greybox, nivel, plataformas, props, materiales, decoración y escala de rata.
- **UI:** únicamente señales necesarias como checkpoint, muerte/reintento y victoria.
- **Technical:** estructura, client/server, networking, datos solo si llegan a ser necesarios y pruebas.
- **Quality:** playtesting, bugs, regression, performance y experiencia en móvil/controller.
- **Management:** roadmap, tareas, documentación, builds y releases.

## Aprendizaje dentro del trabajo

Las tareas técnicas pueden incluir un bloque corto de aprendizaje seguido de uso práctico. Ejemplo: aprender `Script`, `LocalScript` y `ModuleScript`; después aplicar esa diferencia al sistema de checkpoint. No se asignan cursos gigantes desconectados del sprint.

## Riesgos que debemos señalar

Feature creep, sistemas grandes antes de una vertical slice, overengineering, client/server incorrecto, spaghetti hardcodeado, falta de version control o testing, edición sin ownership, tareas vagas, assets finales antes de gameplay, monetización prematura, secretos expuestos, dependencia ciega de Toolbox/free models y código que nadie entiende.

## Herramientas candidatas

Roblox Studio es obligatorio. Discord, Git/GitHub, Studio `Script Sync`, VS Code, Blender y el bot se adoptan gradualmente según su utilidad. Rojo, Luau tooling, paquetes, CI/CD, Open Cloud y automatización de publicación quedan como opciones futuras, no como requisitos de inicio. La comparación investigada vive en [research/workflow-roblox.md](research/workflow-roblox.md).

## Propiedad y publicación

El experience privado vive bajo el Roblox Group **Gon Industries** (`128593985`), propiedad de la cuenta alternativa segura del Project Lead, `treapath`. El juego actual es [Obby but You're a Rat](https://www.roblox.com/games/139385577314595/Obby-but-Youre-a-Rat) (`PlaceId 139385577314595`). La cuenta principal del Lead puede participar como cuenta secundaria, pero no cambia el ownership del Group. El rol `Developer` permite playtest/edit y el owner conserva publish. No se monetiza el MVP.

## Idioma y memoria

La documentación usa español latinoamericano natural, sin traducciones forzadas. Luau, código, nombres de clases, servicios y technical terms permanecen en inglés cuando mejora la claridad. Los mensajes actuales del bot pueden conservar su redacción por ahora. No se confía en el historial de chat para conservar el propósito del proyecto.

Este repositorio es el handbook enlazado desde `#empieza-aqui`; Roblox Studio solo conserva contenido del juego. El código del bot y el código fuente del juego pueden vivir en repositorios de desarrollo separados.
