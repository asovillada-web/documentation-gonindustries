# Borrador — Step 5: primer obby de práctica

**Estado:** S1-01 publicada en `Ready` para el Lead; S1-02 a S1-05 siguen sin publicar.  
**Duración estimada:** una semana, máximo 3–5 horas por persona.  
**Objetivo:** construir una prueba de 30–60 segundos con Parts, un hazard, un checkpoint y una señal clara de escala de rata.

Solo S1-01 puede crearse en Supabase durante este piloto. No se crean tareas para los otros cuatro miembros ni se envía un anuncio. El Step 4 continúa mientras terminan los accesos pendientes.

## Cuándo se puede activar

- Dhrystone, Enrico, Machuc y Vekatorke aparecen con `Developer` en `Gon Industries`.
- Los cinco pueden abrir el experience correcto en Studio.
- El Lead termina primero S1-01; después se habilitan las otras cuatro tareas.

No buscamos todavía 50 o 100 niveles, una rata final, custom movement, UI, DataStore, economía ni arte terminado.

## Orden

```text
S1-01 Lead: preparar zonas seguras
   ├─ S1-02 Enrico: recorrido greybox
   ├─ S1-03 Dhrystone: hazard
   ├─ S1-04 Vekatorke: checkpoint
   └─ S1-05 Machuc: prueba de escala
                    ↓
             playtest del equipo
```

Cada persona modifica únicamente su carpeta dentro de `Workspace/Prototype`. Si necesita mover algo ajeno, primero avisa al owner.

**Regla bloqueante:** antes de comenzar, cada owner revisa `#progreso`. S1-02, S1-03, S1-04 y S1-05 no se publican ni se trabajan hasta que S1-01 aparezca como `✅ Terminada`.

## S1-01 — Preparar el campo de práctica

**Owner:** Project Lead.  
**Reviewer:** Dhrystone.  
**Difficulty:** Easy.  
**Status:** Ready; publicada únicamente para el Lead el 2026-08-29.  
**Dependencies:** ninguna para el piloto del Lead. Esta tarea desbloquea S1-02 a S1-05 cuando el reviewer la apruebe como `Done`.

**Por qué:** dar a cada persona un espacio claro para practicar sin que todos editen los mismos objetos.

**Learning corto (15–20 min):** reconocer `Explorer`, `Properties`, `Workspace`, `Folder`, `Part` y `Anchored`.

**Pasos:**

1. En Discord, abre tu tarea y presiona **Empezar tarea**.
2. Abre Vinegar desde tus aplicaciones y espera a que aparezca Roblox Studio.
3. En la pantalla inicial de Studio, abre **Obby but You're a Rat** de `Gon Industries`. Si no aparece, no crees otra Baseplate: escribe el bloqueo en el ticket.
4. En la barra superior abre **Window**. Haz clic en `Explorer`, `Properties` y `Output` para que las tres ventanas queden visibles.
5. `Explorer` es el árbol de objetos del juego. Haz clic en la flecha pequeña a la izquierda de `Workspace` para desplegar lo que contiene.
6. Pasa el mouse sobre `Workspace` y pulsa el botón `+`. Escribe `Folder` en la búsqueda y selecciónalo.
7. Haz clic derecho sobre el nuevo `Folder`, elige **Rename**, escribe `Prototype` y presiona Enter.
8. Pulsa la flecha a la izquierda de `Prototype` para abrirlo. Pasa el mouse sobre `Prototype`, pulsa `+`, elige `Folder` y renómbralo `Route`.
9. Repite el paso anterior tres veces para crear `Hazards`, `Checkpoints` y `ScaleTest`. Los cuatro deben estar dentro de `Prototype`, no al mismo nivel.
10. Pasa el mouse sobre `Route`, pulsa `+`, busca `Part` y selecciónala. Renómbrala `StartPlatform`.
11. Selecciona `StartPlatform`. En `Properties`, busca `Anchored` y activa el checkbox para que la plataforma no caiga durante Play.
12. Repite esos pasos para crear otra Part dentro de `Route`, llamada `GoalPlatform`, también con `Anchored = true`.
13. Busca el `SpawnLocation` original en `Explorer`. Arrástralo y suéltalo encima de `Route`, renómbralo `FirstSpawn` y usa **Home → Move** para colocarlo sobre `StartPlatform`. Si no existe, crea uno con `Route → + → SpawnLocation`.
14. Dentro de `Hazards` crea una Part llamada `HazardSlot`; dentro de `Checkpoints`, `CheckpointSlot`; y dentro de `ScaleTest`, `ScaleSlot`. Selecciona cada una y activa `Anchored`.
15. Con **Home → Move**, ordénalas visualmente así: `StartPlatform → HazardSlot → CheckpointSlot → ScaleSlot → GoalPlatform`. No importa que todavía no exista un camino completo.
16. Presiona **Play**. Debes aparecer en `FirstSpawn`. Luego presiona **Stop** y revisa `Output`; si aparece un error rojo, inclúyelo en la entrega.
17. Regresa al ticket creado automáticamente al empezar. Sube una screenshot donde se vean la escena y `Prototype` desplegado en `Explorer`; luego usa **Entregar tarea**. Si el Lead ya comprobó el resultado contigo, puede usar **Aprobar y cerrar** directamente.

**Recursos:**

- [Explore Studio UI](https://create.roblox.com/docs/tutorials/curriculums/studio/explore-ui) — guía oficial visual de la interfaz.
- [Work with parts](https://create.roblox.com/docs/tutorials/curriculums/building/work-with-parts) — tutorial oficial para mover, escalar, rotar y anclar Parts.

**Entrega:** una screenshot donde se vean el recorrido y los folders abiertos en `Explorer`.

**Done when:**

- Los cuatro folders y los objetos indicados tienen exactamente esos nombres.
- Todas las Parts y `FirstSpawn` están `Anchored = true`.
- `FirstSpawn` es el único SpawnLocation inicial y el avatar aparece allí durante Play.
- Dhrystone confirma que puede ver la misma estructura en Studio.
- `Output` no muestra errores nuevos durante la prueba.

## S1-02 — Construir tres obstáculos greybox

**Owner:** Enrico.  
**Reviewer:** Project Lead.  
**Difficulty:** Easy.  
**Status al publicar:** Ready después de S1-01.  
**Dependencies:** S1-01.

**Por qué:** comprobar si existe un recorrido divertido antes de crear arte o sistemas grandes.

**Learning corto (20–30 min):** usar `Move`, `Scale`, `Rotate`, `Duplicate`, `Anchor`, `Play` y `Play Here` con Parts.

**Pasos:**

1. Abre `Workspace > Prototype > Route` en `Explorer`.
2. No muevas `HazardSlot`, `CheckpointSlot`, `ScaleSlot` ni objetos de otras carpetas.
3. Inserta una Part, pon `Anchored = true` y nómbrala `Jump01`.
4. Usa `Move` y `Scale` para convertirla en un salto fácil desde `StartPlatform`.
5. Duplica y adapta la Part para crear `Jump02` y `Jump03`.
6. Haz que la ruta pase cerca de los tres slots y termine en `GoalPlatform`.
7. Prueba desde el inicio. Si fallas un salto tres veces seguidas, acércalo o agrándalo.
8. Repite hasta completar el recorrido dos veces sin usar Studio camera para hacer trampa.

**Recurso:** [Intro to building](https://create.roblox.com/docs/tutorials/curriculums/building) — curso oficial para principiantes; incluye material visual y un obby de ejemplo. Solo necesitas las secciones de Parts y playtest.

**Entrega:** video corto recorriendo inicio → meta y una screenshot de `Route` en `Explorer`.

**Done when:**

- Existen `Jump01`, `Jump02` y `Jump03` dentro de `Route`.
- Las tres Parts están ancladas y no caen durante Play.
- El recorrido puede completarse con controles Roblox normales.
- Otra persona llega a la meta sin recibir instrucciones por voz.
- `Output` no muestra errores nuevos.

## S1-03 — Crear un hazard que reinicie al jugador

**Owner:** Dhrystone.  
**Reviewer:** Vekatorke.  
**Difficulty:** Easy.  
**Status al publicar:** Ready después de S1-01.  
**Dependencies:** S1-01.

**Por qué:** enseñar el primer evento server-side y dar una consecuencia básica al obby.

**Learning corto (20–30 min):** un `Script` ejecuta lógica del servidor; `Touched` avisa qué Part tocó el hazard; el `Humanoid` contiene la vida del personaje. No necesitamos `LocalScript`, `ModuleScript` ni `RemoteEvent` aquí.

**Pasos:**

1. Abre `Workspace > Prototype > Hazards` y selecciona `HazardSlot`.
2. Cámbiale el color/material para que parezca peligroso, pero conserva el nombre.
3. Confirma que `Anchored = true` y `CanTouch = true`.
4. Presiona el `+` junto a `HazardSlot`, inserta un `Script` y llámalo `KillOnTouch`.
5. Sigue la guía **Deadly lava** enlazada abajo y adapta `lava` por `hazard`; escribe el código entendiendo cada bloque.
6. Presiona **Play**, pisa el hazard y confirma que el personaje muere y reaparece.
7. Repite la prueba dos veces y toca una plataforma normal para comprobar que no mata.
8. Abre `Output` y revisa que no haya errores rojos nuevos.

**Recursos:**

- [Deadly lava](https://create.roblox.com/docs/tutorials/use-case-tutorials/scripting/basic-scripting/deadly-lava) — tutorial oficial exacto para `Touched` + `Humanoid`.
- [Script types and locations](https://create.roblox.com/docs/scripting/locations) — explicación oficial con video; por ahora lee solo `Script`, `LocalScript` y `ModuleScript`.

**Entrega:** video corto del hazard funcionando, screenshot de `Output` y tres frases: qué son `script.Parent`, `otherPart` y `Humanoid`.

**Done when:**

- Solo `HazardSlot` provoca la muerte en la zona probada.
- El personaje reaparece después de tocarlo.
- Funciona dos veces seguidas.
- Dhrystone puede explicar las tres partes pedidas sin leer una respuesta copiada.
- Vekatorke revisa el Script y `Output` no muestra errores nuevos.

## S1-04 — Crear un checkpoint individual

**Owner:** Vekatorke.  
**Reviewer:** Dhrystone.  
**Difficulty:** Medium.  
**Status al publicar:** Ready después de S1-01.  
**Dependencies:** S1-01.

**Por qué:** comprobar el loop básico de progreso: avanzar, morir y continuar desde el último punto alcanzado.

**Learning corto (30–40 min):** `SpawnLocation` define un punto válido de aparición; `Player.RespawnLocation` puede guardar uno distinto para cada jugador durante la sesión. El servidor debe decidirlo.

**Pasos:**

1. Abre `Workspace > Prototype > Checkpoints`.
2. Elimina únicamente `CheckpointSlot` y crea en su lugar un `SpawnLocation` llamado `Checkpoint01`.
3. Ponlo donde estaba el slot; confirma `Anchored = true`, `Enabled = true` y `Neutral = true`.
4. Inserta dentro de `Checkpoint01` un `Script` llamado `SetCheckpoint`.
5. Sigue el ejemplo oficial **Change Spawn on Touch** del link de `RespawnLocation`: cuando entra un jugador, asigna `FirstSpawn` como su ubicación inicial.
6. Cuando `Checkpoint01.Touched` se active, busca el Character con `hit:FindFirstAncestorOfClass("Model")` y luego el Player con `Players:GetPlayerFromCharacter(character)`.
7. Si encuentra un Player vivo, asigna `player.RespawnLocation = checkpoint`. No añadas DataStore ni RemoteEvent.
8. En **Play**, muere antes de tocarlo y confirma que vuelves al inicio; luego tócalo, muere y confirma que vuelves a `Checkpoint01`.
9. Abre el selector de testing, elige **Server & Clients**, usa dos clientes y presiona Play/F7. Solo el cliente que tocó el checkpoint debe reaparecer allí.
10. Finaliza la sesión y comprueba que `Output` no tenga errores rojos nuevos.

**Recursos:**

- [Player API: `RespawnLocation`](https://create.roblox.com/docs/reference/engine/classes/Player#RespawnLocation) — propiedad y ejemplo oficial `Change Spawn on Touch` que usaremos.
- [Studio testing modes](https://create.roblox.com/docs/studio/testing-modes) — pasos oficiales para `Server & Clients`.

**Entrega:** video o screenshots del antes/después y una frase explicando por qué el checkpoint vive en un `Script` del servidor.

**Done when:**

- Morir antes de tocar el checkpoint lleva al spawn inicial.
- Morir después de tocarlo lleva a `Checkpoint01`.
- En una prueba de dos clientes, el progreso de uno no cambia el del otro.
- No existen DataStore, RemoteEvent ni progreso permanente.
- Dhrystone revisa el Script y `Output` no muestra errores nuevos.

## S1-05 — Construir una prueba simple de escala de rata

**Owner:** Machuc.  
**Reviewer:** Enrico.  
**Difficulty:** Easy.  
**Status al publicar:** Ready después de S1-01.  
**Dependencies:** S1-01.

**Por qué:** probar si el mundo se siente enorme antes de dedicar horas a Blender, texturas o un modelo final de rata.

**Learning corto (20–30 min):** escala en studs, diferencia entre `Part` y `Model`, `Anchored`, colisiones y cómo se ve un prop desde la cámara de juego.

**Pasos:**

1. Abre `Workspace > Prototype > ScaleTest` y usa `ScaleSlot` como centro de trabajo.
2. Con Parts de Studio, construye **un solo prop cotidiano gigante**: por ejemplo una caja de cereal, lata o bloque de queso.
3. Crea también un rat hole sencillo con tres Parts: lado izquierdo, lado derecho y parte superior.
4. Pon nombres claros a las piezas y selecciónalas para agruparlas en un `Model` llamado `RatScaleTest`.
5. Confirma que todas las piezas estén `Anchored = true`.
6. Ajusta `CanCollide` para que el jugador pueda atravesar el rat hole sin quedarse trabado.
7. Prueba el modelo con **Play**, desde la cámara normal del personaje, no solo desde la cámara de edición.
8. No uses Toolbox, Blender, texturas finales ni más de un prop en esta tarea.

**Recurso:** [3D art and Studio](https://create.roblox.com/docs/art/overview-studio) — vista oficial de Explorer, Parts, Models, MeshParts y Output para artistas.

**Entrega:** dos screenshots: una desde la cámara del jugador y otra con `RatScaleTest` abierto en `Explorer`.

**Done when:**

- Existe un solo Model llamado `RatScaleTest` dentro de `ScaleTest`.
- El prop cotidiano se percibe grande desde Play.
- El avatar puede atravesar el rat hole sin atascarse.
- Ninguna pieza cae o se mueve sola.
- Enrico confirma que el prop no bloquea el recorrido y `Output` no muestra errores nuevos.

## Playtest de cierre — todavía no es una tarea del bot

Cuando las cinco tareas estén en Review, los cinco juegan la prueba. Cada persona aporta solamente:

- una cosa que funcionó;
- un problema concreto;
- una respuesta: ¿la escala ya empieza a vender la idea de ser una rata?

El Lead acepta, pide cambios pequeños o separa bugs. Las ideas de 50/100 niveles siguen en Backlog hasta que esta prueba sea divertida.

## Preparación para el bot

Este documento es la fuente para generar las cinco filas de tareas más adelante. La futura publicación debe:

1. crear solamente S1-01 durante el piloto del Lead;
2. esperar su aprobación;
3. mantener S1-02 a S1-05 fuera de Supabase hasta una nueva orden;
4. cuando se autoricen, crear esas cuatro y enviar un único anuncio compacto.

`202608290010_assign_lead_workspace_task.sql` publicó solamente S1-01 y retiró el TEST visual anterior. `202608300001_update_lead_task_learning_layout.sql` actualizó su contenido al embed aprobado. No se envió anuncio ni se crearon las otras tareas; la próxima migration requiere una orden explícita del Lead después de revisar `messages-testing/`.

`202608300002_task_detailed_guides.sql` añade la guía DM a S1-01. Todas las tarjetas muestran `📘 Información detallada`, pero las tareas antiguas sin una guía propia generan una explicación de respaldo desde sus campos. Las guías futuras deben revisarse en `messages-testing/details/` antes de crear la fila correspondiente.
