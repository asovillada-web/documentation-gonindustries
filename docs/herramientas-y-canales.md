# Herramientas y canales

Cada herramienta tiene un propósito distinto.

## Roblox Studio

Es el editor del juego. Contiene el experience, el mapa, scripts, UI y assets. Team Create permite que el equipo abra y pruebe el mismo experience. No guardamos aquí roadmap, metodología ni documentos administrativos.

## Discord

Es el hub de trabajo diario:

- `#empieza-aqui`: guía corta y botón hacia este handbook.
- `#progreso`: tablero read-only de tareas pendientes, activas y terminadas.
- `#anuncios`: cambios importantes y nuevas tareas.
- `#desarrollo`: dudas y coordinación técnica.
- `#arte-y-diseno`: modeling, referencias y feedback visual.
- `#tareas`: panel para consultar y comenzar trabajo.
- Tickets privados: entrega, evidencia, review y cambios pedidos.

Flujo del ticket:

```text
Ver mis tareas → Empezar tarea → trabajar y dejar evidencia
→ Entregar tarea → Review → Aprobar y cerrar / Pedir cambios
```

El Lead también puede aprobar desde `In Progress` si ya verificó el resultado por Studio, llamada o pantalla compartida.

## GitHub

Este repositorio conserva la documentación versionada y buscable. Discord enlaza el contenido; no lo duplica. Más adelante Git también puede conservar scripts sincronizados desde Studio, pero no es requisito para todos hasta validar el workflow.

## Herramientas opcionales

- **Rojo/Script Sync:** piloto del Lead para trabajar con Luau como archivos; todavía no es requisito del equipo.
- **VS Code:** útil al trabajar con archivos, no necesario para construir Parts en Studio.
- **Blender:** se introduce cuando un asset real lo necesite; el primer prototype usa Parts.

No añadimos CI/CD, paquetes, frameworks ni publicación automática mientras no resuelvan un problema actual.
