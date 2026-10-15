# Registro de decisiones

Estados: `Aceptada` (decisión explícita), `Propuesta` (requiere confirmación del equipo), `Reemplazada` o `Descartada`.

| ID | Fecha | Estado | Decisión | Motivo |
|---|---|---|---|---|
| D-001 | 2026-08-28 | Aceptada | Roblox Studio es la primera plataforma y Discord el hub. | Definido por el equipo. |
| D-002 | 2026-08-28 | Aceptada | Documentación en español latinoamericano natural; technical terms reconocibles en inglés cuando suenen mejor. | Definido por el equipo; evitar traducciones forzadas. |
| D-003 | 2026-08-28 | Aceptada | Priorizar un MVP pequeño y aprendizaje mediante tareas. | Evitar feature creep y terminar el primer juego. |
| D-004 | 2026-08-28 | Aceptada | El repositorio es la memoria durable; Discord enlaza el contenido canónico. | El contexto no debe depender del historial de chat. |
| D-005 | 2026-08-28 | Aceptada | El experience privado pertenece a `Gon Industries` (`128593985`) antes de comenzar trabajo importante. | El Lead completó el setup el 2026-08-29 y verificó el experience bajo el Group. |
| D-006 | 2026-08-28 | Propuesta | Flujo híbrido: Team Create para el mundo, Git para docs/bot/scripts y `Script Sync` para Luau; no Rojo al inicio. | Equilibra colaboración integrada, review de archivos y coste de aprendizaje. |
| D-007 | 2026-08-28 | Aceptada | Probar primero una despensa/cocina en greybox con default Humanoid. | El Lead confirmó el 2026-08-29 que avanzaremos en esta dirección simple y progresiva; refuerza escala sin crear un controller prematuro. |
| D-008 | 2026-08-28 | Aceptada | Bot local por REST: setup idempotente de canales + anuncios, sin slash commands ni hosting. | Crea el hub compacto y permite updates sin mantener un proceso 24/7. |
| D-009 | 2026-08-28 | Aceptada | El lead usa Linux/Vinegar; los otros cuatro miembros usan Windows. | Las guías deben reconocer diferencias de paths, instalación y troubleshooting. |
| D-010 | 2026-08-28 | Aceptada | Trabajar progresivamente por steps semanales; mostrar y asignar solo el step actual. | Evitar saturar al equipo y ajustar el siguiente trabajo a lo aprendido cada semana. |
| D-011 | 2026-08-28 | Aceptada | Mantener temporalmente `Manage Channels` en el rol del bot. | El lead quiere que pueda reorganizar Discord más adelante; el token debe permanecer privado. |
| D-012 | 2026-08-28 | Aceptada | Usar Discord buttons + HTTP interactions en lugar de emoji reactions + Gateway. | Permite hosting serverless on demand y evita mantener una conexión WebSocket 24/7. |
| D-013 | 2026-08-28 | Aceptada | Hospedar el task manager MVP en Supabase Edge Functions + Postgres Free. | Incluye endpoint y persistencia; Supabase mantiene un ejemplo oficial de Discord. Cloudflare se descartó por un bug abierto con `POST` a Discord. |
| D-014 | 2026-08-28 | Reemplazada | El owner mueve `Ready → In Progress → Review`; solo el Project Lead aprueba `Done` o pide cambios. | D-031 conserva la autoridad del Lead pero permite aprobar directamente desde `In Progress`. |
| D-015 | 2026-08-28 | Aceptada | Mostrar siempre la tarea en una respuesta ephemeral e intentar el DM además. | Si el usuario bloquea DMs, el flujo sigue funcionando sin crear channels privados. |
| D-016 | 2026-08-28 | Aceptada | Guardar learning corto y fuentes verificadas dentro de cada tarea; no generar contenido con AI en runtime. | Enseña justo lo necesario sin costo, API externa ni documentación masiva. |
| D-017 | 2026-08-28 | Aceptada | El bot conserva `Administrator` por decisión explícita del Lead hasta que él decida reducirlo. | Evita bloqueos mientras evoluciona el servidor, aunque no es requisito técnico y aumenta el impacto de un token comprometido. |
| D-018 | 2026-08-28 | Reemplazada | Cada entrega usa un review channel privado para owner, reviewer, Lead y bot; conserva archivos y conversación, exige evidencia visible y queda read-only al aprobar. | D-020 conserva el channel privado pero reemplaza el gate automático por revisión humana. |
| D-019 | 2026-08-29 | Aceptada | Cada ticket mantiene una sola tarjeta compacta que cambia según el estado: enviar para el owner, decidir para el Lead y cerrado al aprobar. | Repetir la tarea completa en cada transición hacía flood y escondía los controles importantes. |
| D-020 | 2026-08-29 | Aceptada | Cada entrega conserva su review channel privado y evidencia, pero el bot solo muestra instrucciones simples: no inspecciona mensajes ni usa checklists automáticos; el owner envía cuando está listo y el Lead aprueba o explica cambios manualmente. | Sin `MESSAGE_CONTENT`, Discord vacía `content`, `embeds`, `attachments` y `components` en mensajes del servidor; activar ese privileged intent solo para este gate añade acceso innecesario y la calidad de una entrega requiere juicio humano. |
| D-021 | 2026-08-29 | Aceptada | `🔒 REVISIONES` contiene tickets activos y pedidos de cambios; `🗃️ HISTORIAL` contiene `#review-log` y mueve allí los tickets aprobados read-only. | Evita mezclar trabajo pendiente con reviews ya cerradas. |
| D-022 | 2026-08-29 | Aceptada | El Lead crea y verifica primero Group, rol y experience privado; solo después se asignan al resto las tareas de acceso y metodología. | Evita mandar cinco tareas bloqueadas y permite aprender sobre el proyecto real. |
| D-023 | 2026-08-29 | Aceptada | La cuenta alternativa segura `treapath` es owner de `Gon Industries`; la cuenta principal del Lead puede añadirse como cuenta secundaria sin cambiar el ownership. | El Lead prefiere separar el proyecto de su cuenta principal y confirmó seguridad y age check en la cuenta owner. |
| D-024 | 2026-08-29 | Aceptada | El primer onboarding real es únicamente un step-by-step para agregar a `treapath`, compartir el username exacto y aceptar la invitación al rol `Developer`. Age check y Team Create se tratan después, cuando hagan falta. | Mantiene la primera tarea directa y evita meter learning que no es necesario para unirse al Group. |
| D-025 | 2026-08-29 | Aceptada | El equipo intentará discutir roles y áreas de aprendizaje antes del primer trabajo de Roblox; si no llegan a definirlos, el technical guide propondrá el reparto inicial según habilidades actuales, dependencias, aprendizaje útil y necesidades del MVP. El Lead conserva la decisión final. | Permite avanzar sin dejar que una reunión pendiente bloquee el proyecto ni convertir roles iniciales en silos permanentes. |
| D-026 | 2026-08-29 | Aceptada | Probar Rojo `7.7.0` solo entre el Lead y el technical guide con un `Script` aislado; Studio sigue siendo fuente del mapa y Rojo todavía no es requisito del equipo. | Permite asistencia y review desde el repositorio sin comprometer el workflow completo antes de validarlo. |
| D-027 | 2026-08-29 | Aceptada | Publicar primero solo S1-01 para el Lead; S1-02 a S1-05 permanecen fuera del bot hasta revisar el piloto y recibir otra orden. | Permite comprobar que las instrucciones sirven a principiantes absolutos sin llenar al equipo de trabajo prematuro. |
| D-028 | 2026-08-30 | Aceptada | Antes de publicar una tarea, guardar su mensaje en `messages-testing/<persona>.md` para aprobación del Lead. Las tarjetas usan un embed único con `¿Qué hacer primero?`, recursos/puntos/keywords, `Al finalizar:` y `Done when`. | El Lead necesita revisar el contenido exacto; el embed aprovecha más espacio sin dividir la tarea en mensajes que hagan flood. |
| D-029 | 2026-08-30 | Aceptada | Cada tarjeta de tarea incluye `📘 Información detallada`; al presionarlo, el bot envía por DM una guía revisada con propósito, conceptos, pasos, pruebas, errores comunes y entrega. El botón no cambia estados ni abre tickets. | Mantiene Discord compacto y permite enseñar a principiantes absolutos sin recortar la ayuda necesaria. Si el DM está bloqueado, el bot lo informa de forma ephemeral. |
| D-030 | 2026-08-30 | Aceptada | `#progreso` vive sin categoría como tablero público, read-only y de un solo mensaje. Separa tareas publicadas pendientes/activas de las terminadas, se refresca al cambiar estados o con su botón, y es la referencia obligatoria antes de comenzar una dependencia. | Hace visibles los bloqueos sin llenar `#tareas`; las tareas futuras no se publican antes de que su dependencia esté `Done`, evitando necesitar un sistema relacional prematuro. |
| D-031 | 2026-08-30 | Aceptada | **Empezar tarea** crea el ticket automáticamente. El owner entrega con un solo botón y sin formulario; el Lead puede usar **Aprobar y cerrar** desde `In Progress` si ya verificó el resultado, o esperar `Review` y conservar **Pedir cambios**. | La evidencia puede estar en el ticket, Studio, llamada o pantalla compartida; exigir tres campos siempre añadía fricción sin mejorar todas las reviews. La base de datos sigue registrando cada transición y solo el Lead puede marcar `Done`. |
| D-032 | 2026-08-30 | Aceptada | La documentación de consulta del equipo vivirá en un repositorio de GitHub separado del juego. `#empieza-aqui` tendrá un embed con un link button hacia ese handbook; Roblox Studio conservará únicamente contenido del juego. Hasta crear y poblar el repo separado, este repositorio sigue siendo la fuente canónica. | Mantiene metodología, propósito, requisitos y decisiones buscables y versionadas sin meter texto administrativo en Studio. La transición explícita evita dos fuentes de verdad. |

## Dirección vigente — 2026-10-14

- Lead confirma los cuatro frentes G1 completados; se archivan sin borrar evidencia.
- Publicar dos frentes de cocina 6–15: Enrico/Machuc (diseño, ambiente, recorrido y Explorer), Dhrystone/Vekator (respawn, sistemas e integración).
- Propuesta visual y piloto antes de extender. Cantidad de obstáculos y layout modificables; no regenerar encima de trabajo manual.
- Ideas nuevas solo pasan a trabajo pendiente tras validación del Lead. Colección/economía/guardado siguen con él.
- G2-01 cierra tras G2-02; G2-02 prueba la ruta construida sin esperar Done de G2-01. Todos revisan; solo Lead cierra.

## Dirección anterior — 2026-09-10

Las siguientes decisiones del Lead reemplazan las reglas iniciales que entren en conflicto:

- Recuperar esta metodología ligera y dejar RAT RUSH como experimento histórico, no juego del equipo.
- Terminar stages 1–5 dentro de una pared; el greybox existente es completamente modificable. Ya hay rata animada y HUD.
- Plataformas: Enrico/Machuc, prioridad máxima. Sistemas: Dhrystone/Vekator. Ambiente: Machuc, prioridad secundaria. Integración: Vekator/Dhrystone; no sobrecargar Enrico.
- El Lead trabaja solo en colección/economía y usa Rojo por separado; se adapta al equipo Studio. Nadie más necesita Rojo ni agentes.
- Cuatro tickets compartidos desde Ready. Todos aportan y comentan reviews; responsables/colaboradores inician y entregan. Solo Lead aprueba/cierra o pide cambios de estado.
- Avances parciales en mensajes. G1-01 cierra después de G1-02; G1-04 después de G1-01/02/03. Pruebas parciales desde ahora.
- Cuerda: investigación aislada después de estabilidad. Integrarla no es requisito de esta entrega.
- Tareas iniciales completas según el Lead; tickets conservados en Historial. Pending antiguas retiradas, no falsamente completadas.

## Propuestas históricas para revisar cuando hagan falta

1. Acordar por escrito recuperación de la cuenta owner, salida de miembros y criterio futuro de reparto.
2. Confirmar los requisitos de collaboration/age verification en el próximo step, cuando probemos acceso desde Studio; no forman parte de la tarea actual de unirse al Group.
3. Aceptar D-006 y elegir si `Script Sync` se configura al final del Sprint 1 o al inicio del Sprint 2; probar primero el mapping en Windows y Linux/Vinegar.
4. Confirmar el límite de tiempo: una semana, máximo 3–5 horas por persona.

No hace falta resolverlas todas durante el Step 4. Primero incorporamos al equipo al Group; las demás vuelven cuando comprobemos acceso y empecemos el prototype.

Cuando se confirme una propuesta, cambia su estado y añade una frase con quién/qué evidencia la confirmó.
