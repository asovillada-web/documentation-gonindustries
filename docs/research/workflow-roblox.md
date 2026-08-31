# Research report: workflow actual de Roblox

Investigado: 2026-08-28; Group/collaboration y Rojo reverificados el 2026-08-29. Se priorizaron fuentes oficiales. Rojo se identifica como herramienta comunitaria/open source y no como producto de Roblox.

El Lead tiene Rojo CLI y plugin `7.7.0`, actualizados desde el release oficial estable. Se evalúa únicamente con `ServerScriptService/RojoSmokeTest`; no cambia todavía la recomendación de aplazar su adopción para todo el equipo. [Release oficial 7.7.0](https://github.com/rojo-rbx/rojo/releases/tag/v7.7.0).

## Recomendación ejecutiva

Para este equipo de cinco principiantes:

1. Crear un **Roblox Group** y un experience privado propiedad del Group.
2. Usar **Roblox Studio + Team Create** para construir, modelar, playtestear y publicar.
3. Usar **Git/GitHub** desde el primer día para documentos y bot.
4. Añadir el `Script Sync` integrado de Studio para las carpetas de scripts cuando el equipo ya tenga el experience y la estructura mínima. Así Luau puede revisarse en Git sin trasladar todo el mundo 3D al filesystem.
5. Permitir **Studio Script Editor o VS Code** según preferencia; no obligar a cambiar de editor el primer día.
6. Usar **Blender** para los assets de Machuc que realmente necesiten custom mesh; greybox y medidas primero en Studio.
7. No adoptar todavía Rojo, package managers, formatter/linter externos, CI/CD ni deploy automático. Revaluar Rojo si Script Sync limita el review, se necesitan builds reproducibles o el filesystem debe ser la fuente de verdad del proyecto completo.

Es una inferencia para este equipo basada en las capacidades y costes documentados abajo, no una regla universal de Roblox.

## Entorno mixto: Windows + Linux/Vinegar

El lead usa Linux con Vinegar y los otros cuatro integrantes usan Windows. Vinegar es un bootstrapper open source de la comunidad para ejecutar Roblox Studio en Linux; no es una herramienta oficial de Roblox: [Vinegar GitHub](https://github.com/vinegarhq/vinegar) y [documentación de instalación](https://vinegarhq.org/Vinegar/Installation.html).

Consecuencias prácticas:

- No documentar paths absolutos de Windows como si funcionaran para todo el equipo.
- El experience en Team Create sigue siendo el punto común; no compartir archivos locales `.rbxl` como workflow principal.
- Antes de adoptar `Script Sync` para los tres programadores y el lead, probar un folder pequeño tanto en Windows como en Linux/Vinegar y registrar el mapping real.
- Si Vinegar usa Flatpak, confirmar que Studio puede acceder a la carpeta clonada antes de sincronizar; no cambiar permisos globales del filesystem por ensayo y error.
- El bot, Git y los documentos son cross-platform porque viven fuera de Studio; sus comandos requieren Node pero no Vinegar.

## Comparación de opciones

| Flujo | Pros | Contras | Complejidad / aprendizaje | Encaje actual |
|---|---|---|---|---|
| Studio + Team Create solamente | Editor, mundo 3D, scripting colaborativo, autosave y playtests integrados; menor setup | Review/diffs de código y documentación débiles; trabajo basado en archivos queda fuera | Baja | Bueno para la primera sesión, insuficiente como única memoria |
| Studio + Team Create + Git para docs/bot | Mantiene lo visual simple y da historial/review a archivos normales | El código Luau de Studio aún no está en Git | Baja-media | Adoptar inmediatamente |
| Lo anterior + `Script Sync` oficial | Editar scripts en IDE, versionarlos y seguir usando colaboración de Studio | Solo sincroniza scripts; resolver mal una diferencia de sync puede perder cambios; requiere disciplina de ownership | Media | Recomendado por etapas |
| Rojo + Git (parcial o completo) | Filesystem como fuente de verdad, buen diff/review, acceso a tooling y builds | Plugin/CLI/configuración, nuevos modelos mentales y coordinación delicada con Team Create; mayor coste para principiantes | Media-alta | Aplazar |
| Archivos `.rbxl/.rbxlx` manuales en Git | Snapshot adicional del place | Diffs/merges poco útiles y alto riesgo de sobrescribir trabajo | Media, poco beneficio | No usar como colaboración principal |

### Qué dicen las fuentes

- Roblox presenta Studio como herramienta integrada para construir, script, test, publish y colaborar en tiempo real: [Roblox Studio](https://create.roblox.com/docs/studio).
- La colaboración permite Live Scripting o Drafts; el modo Drafts permite trabajar localmente antes de hacer commit al repositorio compartido de Studio. Roblox documenta también requisitos actuales de age verification para colaborar: [Studio collaboration](https://create.roblox.com/docs/projects/collaboration).
- `Script Sync` sincroniza scripts entre el DataModel y archivos locales, funciona con colaboración y es apropiado si se quiere editor externo/version control conservando Studio para el resto. La misma página dice que Rojo encaja mejor cuando se quiere versionar el proyecto entero o usar el filesystem como fuente de verdad: [Script Sync](https://create.roblox.com/docs/scripting/sync).
- Roblox guarda versiones de cada place y permite revertir desde Creator Dashboard; esto es backup/historial del place, no reemplazo de Git para revisar archivos: [Configure games and places](https://create.roblox.com/docs/projects/configure-experiences).
- Git conserva quién, cuándo, qué y por qué cambió un archivo; GitHub añade pull requests para discutir/revisar antes de integrar: [About Git](https://docs.github.com/en/get-started/using-git/about-git) y [About pull requests](https://docs.github.com/en/pull-requests/get-started/about-pull-requests).
- Rojo se describe a sí mismo como una forma de representar el juego en archivos y aprovechar Git/tooling; su introducción reconoce que añadirlo puede ser intimidante. Su guía separa workflows parciales y completos: [Rojo introduction](https://rojo.space/docs/v7/) y [Recommended workflows](https://rojo.space/docs/v7/workflows/).

## Ownership del experience y assets

### Recomendación

Crear el Group **antes** del experience importante. El Project Lead crea y asegura el Group, pero el experience, meshes/textures/audio del juego y paquetes reutilizables se crean bajo el Group cuando la interfaz lo permita.

Roles iniciales sugeridos en Creator Dashboard:

| Rol | Personas | Permisos iniciales |
|---|---|---|
| Owner | Project Lead | Custodia y recuperación; no compartir cuenta |
| Developer | Dhrystone, Enrico, Vekatorke | Playtest y Edit para este experience; sin publish global |
| Artist | Machuc | Playtest/Edit del experience y crear/configurar development items necesarios |
| Publisher | Project Lead; backup futuro solo tras acuerdo | Edit + Publish del experience |

No conceder por comodidad: administrar todos los roles, monetización, borrar DataStores, administrar secretos ni habilitar place copying. Aplicar permisos por experience cuando sea posible.

### Motivos y límites verificados

- Roblox Groups permiten colaborar, usar assets comunes, compartir beneficios y dar crédito. Crear un Group cuesta actualmente 100 Robux. Roblox también advierte que no arbitra conflictos internos: [Groups (teams)](https://create.roblox.com/docs/projects/groups).
- Los permisos distinguen playtest, edit, publish, monetización, development items, secrets y DataStores. Por eso `Developer` no necesita ser super-admin.
- Un experience personal se puede transferir más tarde a un Group, pero private ModuleScripts, packages/assets y API keys pueden requerir migración; aceptar la transferencia vuelve privado el juego y cierra servidores: [Game ownership transfer](https://create.roblox.com/docs/projects/game-ownership-transfer).
- El importer puede asignar un 3D asset al usuario o al Group dueño del proyecto; seleccionar el Group permite usarlo a miembros elegibles: [Blender workflow](https://create.roblox.com/docs/art/blender).

### Acuerdo humano mínimo

Antes de gastar o publicar, guardar en un documento compartido aceptado por todos:

- Quién custodia la cuenta owner y cómo recuperarla con 2FA.
- Qué ocurre si alguien abandona el equipo.
- Cómo se decide publicar, gastar Robux o monetizar.
- Cómo se atribuyen assets y contribuciones.
- Que cualquier reparto futuro se acuerda antes de activar ingresos.

Esto no sustituye asesoría legal; evita depender de expectativas implícitas que Roblox no resolverá.

## Colaboración práctica

1. Verificar que las cinco cuentas pueden usar colaboración según los requisitos de edad actuales.
2. Dar acceso al experience privado por rol/per-game permission.
3. Usar un owner por sistema o zona. Team Create permite simultaneidad, pero no vuelve buena idea editar la misma cosa sin coordinación.
4. Guardar/publicar con notas entendibles y consultar Activity/Version History ante incidentes.
5. Para Luau sincronizado: commit seguro antes del primer mapping, sync de carpetas completas, leer el diálogo de conflictos y nunca asumir que la copia más nueva está en un lado concreto.

## Testing recomendado para este juego

- Mientras se construye el recorrido: `Test`/`Test Here`, porque inserta avatar y permite validar saltos.
- Para checkpoint/respawn y cualquier RemoteEvent: `Server & Clients` con dos clientes. Studio simula hasta ocho, pero uno o dos suelen bastar.
- Para sesión de equipo: `Team Test` cuando sea útil.
- Antes del MVP: Device Emulator y Controller Emulator; no hace falta optimizar para cada dispositivo en el primer greybox.
- Regression mínima: spawn → hazard → checkpoint → death → respawn correcto → goal.

Fuente principal: [Studio testing modes](https://create.roblox.com/docs/studio/testing-modes). Para un obby, el tutorial oficial recomienda playtest frecuente usando un modo que inserte avatar: [Test and save](https://create.roblox.com/docs/tutorials/curriculums/building/test-and-save).

## Client/server y seguridad

Roblox es multiplayer por defecto. `RemoteEvent` sirve para comunicación unidireccional y `RemoteFunction` para solicitud/respuesta, pero no todo sistema necesita uno: [Remote events and callbacks](https://create.roblox.com/docs/scripting/events/remote).

Regla del proyecto: el client solicita o muestra; el server valida y decide estado compartido. Roblox recomienda validar contexto/permisos, tipos/valores y frecuencia de todo dato enviado por client, además de limitar alcance de remotes: [Securing the client-server boundary](https://create.roblox.com/docs/scripting/security/client-server-boundary).

Para el Sprint 1 no necesitamos DataStore, economía, RemoteFunction ni framework de networking.

## Arte y Blender

Roblox permite crear Parts directamente en Studio; meshes custom se producen en herramientas como Blender/Maya y se importan como `MeshPart`: [Custom 3D assets](https://create.roblox.com/docs/art/modeling). La guía oficial de Blender explica unidades, ejes, escala e import ownership: [Blender](https://create.roblox.com/docs/art/blender).

Orden recomendado para Machuc:

1. Medir en studs contra el default character.
2. Greybox de la silueta/colisión en Studio.
3. Un prop simple en Blender.
4. Importar como asset del Group y validar scale, pivot, collision y moderation.
5. Solo después producir variaciones o detalle.

## Herramientas: ahora, después y no todavía

| Herramienta | Decisión | Problema que resuelve |
|---|---|---|
| Roblox Studio / Team Create | Ahora | Mundo, scripting, collaboration, test y publish |
| Roblox Group | Antes del experience importante | Ownership, permisos, assets y futuro revenue |
| Git + host privado (por ejemplo GitHub) | Ahora | Memoria, historial, review y backup de archivos |
| Discord + bot one-shot | Ahora | Comunicación y anuncios consistentes |
| Blender | Ahora para Machuc, solo assets necesarios | Custom meshes |
| `Script Sync` | Tras crear estructura mínima | Luau en Git/IDE sin abandonar Studio |
| VS Code | Opcional | Preferencia de editor, no requisito de equipo |
| Rojo | Revaluar tras vertical slice/MVP | Proyecto más completo como archivos/builds |
| StyLua/Selene/luau-lsp | Después de existir suficiente código | Formato/análisis consistente |
| Wally/packages externos | Solo ante dependencia real | Gestión de librerías |
| CI/CD/Open Cloud deploy | Después de releases repetitivos | Automatización reproducible |

## Fuentes Discord relevantes al bot

- Crear aplicación, credenciales, install link, scopes y permisos: [Building your first Discord Bot](https://docs.discord.com/developers/quick-start/getting-started).
- Bot token, OAuth scopes y principio de permisos mínimos: [OAuth2 and Permissions](https://docs.discord.com/developers/platform/oauth2-and-permissions).
- Endpoint `Create Message`, permiso `SEND_MESSAGES`, límite de 2000 caracteres y control de mentions: [Message Resource](https://docs.discord.com/developers/resources/message).

Las decisiones aplicadas al equipo están resumidas en [herramientas y canales](../herramientas-y-canales.md) y en [decisiones](../decisiones.md).
