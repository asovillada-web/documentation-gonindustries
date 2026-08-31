# Testing mínimo

Probamos para descubrir problemas antes de llamarlos `Done`, no para producir reportes largos.

## Según el cambio

| Cambio | Prueba mínima |
|---|---|
| Mundo, salto, hazard o prop | `Play` o `Play Here` en el camino afectado. |
| Checkpoint, respawn, RemoteEvent o estado compartido | `Server & Clients` con dos clientes. |
| UI o input | Una resolución móvil y Controller Emulator cuando corresponda. |
| Release | Recorrido completo y regresión de spawn, hazards, checkpoints y meta. |

## Evidencia útil

La tarea define qué evidencia tiene sentido: screenshot, video corto, archivo, link o revisión en llamada/pantalla compartida. No existe un formulario obligatorio para todos los casos.

Antes de aprobar:

- otra persona comprueba el `Done when`;
- `Output` no muestra errores nuevos en el camino probado;
- si falla, el ticket registra el problema concreto y el cambio pedido;
- solo el Project Lead marca la tarea como `Done`.

## Reporte corto de bug

```text
Título:
Versión o momento de la prueba:
Modo: Play / Server & Clients / móvil / controller
Pasos para reproducir:
Resultado esperado:
Resultado real:
Evidencia, si ayuda:
```

## Playtest de una slice

Cada persona aporta solamente:

1. una cosa que funcionó;
2. un problema concreto;
3. la respuesta a la pregunta principal del test.

Para la primera slice: **¿la escala y la ruta ya hacen sentir que somos una rata?**
