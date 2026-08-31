# Estándares de desarrollo iniciales

Son guardrails para principiantes, no una arquitectura definitiva.

## Estructura en Studio

```text
Workspace
  Prototype/             Greybox y objetos interactivos del nivel
ReplicatedStorage
  Shared/                ModuleScripts usados por server y client
  Remotes/               Solo cuando haga falta cruzar client/server
ServerScriptService
  Server/                Reglas autoritativas del juego
ServerStorage
  ArtTests/              Assets no replicados que todavía se evalúan
StarterPlayer
  StarterPlayerScripts/
    Client/              Input, cámara y feedback local
StarterGui
  UI/
```

No creamos una carpeta vacía para cada sistema futuro. Esta estructura crece al aparecer código real.

## Nombres y estilo

- Código e Instances técnicas en inglés para coincidir con documentación y APIs.
- `PascalCase`: ModuleScripts, clases/tipos y Models importantes.
- `camelCase`: variables locales, parámetros y funciones.
- `UPPER_SNAKE_CASE`: constantes reales.
- Nombres describen intención: `CheckpointService`, no `Manager2` ni `Stuff`.
- Un script tiene una responsabilidad. Extrae un ModuleScript cuando una lógica se comparte o la separación ya mejora la lectura, no antes.
- Comentarios explican **por qué** existe una decisión extraña; no traducen cada línea.

Usaremos Luau con type checking gradual. No se exige `--!strict` en todo el primer día; se adopta en módulos nuevos que el owner pueda explicar y se mantienen limpios los warnings relevantes. Referencias oficiales: [Luau types](https://luau.org/types/) y [Luau lints](https://luau.org/lint/).

## Client y server

- **Server:** checkpoints, respawn autorizado, estado compartido, victoria y cualquier progreso/recompensa.
- **Client:** input, cámara, UI, animaciones y efectos que no deciden verdad compartida.
- Usa `RemoteEvent` para comunicación asíncrona cuando haga falta; no crees remotes para lógica que puede quedarse en un solo lado.
- El servidor valida tipo, rango, contexto, permiso y frecuencia de cualquier dato del client. Roblox advierte que toda entrada del client puede abusarse: [Securing the client-server boundary](https://create.roblox.com/docs/scripting/security/client-server-boundary).
- Nunca dejes que el client se otorgue checkpoint, victoria, moneda o asset.

## Errores y debugging

- Abre `Output` y `Script Analysis` mientras trabajas.
- No ocultes errores con `pcall` sin manejar o registrar el resultado.
- Un mensaje de error debe indicar el sistema y la condición que falló, sin imprimir secretos.
- Si un bug no se reproduce, registra modo de test, place version, pasos y resultado real.

## Assets

- Greybox con Parts antes de arte final.
- Machuc define escala y pivots; quien integra gameplay valida colisiones.
- Los assets destinados al juego se importan bajo el Group cuando sea posible.
- Todo modelo de Toolbox se trata como código de terceros: inspeccionar jerarquía y scripts antes de introducirlo. En el MVP preferimos Parts y assets propios.

## Pruebas proporcionales

- Cada cambio: `Play` o `Play Here` en el camino afectado.
- Checkpoints, remotes o estado compartido: Server & Clients con dos clientes.
- UI/input: una resolución móvil y Controller Emulator antes de release.
- Antes de release: recorrido completo desde spawn hasta goal y una regresión de respawn/checkpoints.

Studio admite tests con uno o varios clientes, Team Test y emuladores de dispositivo/controller: [Studio testing modes](https://create.roblox.com/docs/studio/testing-modes).

