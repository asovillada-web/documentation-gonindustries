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
- Tickets de frentes: compartidos por los cinco, privados frente a visitantes. Avances, evidencia y review en el mismo lugar; solo el Lead cierra.

Flujo del ticket:

```text
Frentes del equipo → contexto → Empezar frente → avances y pruebas
→ Entregar tarea → Review → Aprobar y cerrar / Pedir cambios
```

El Lead también puede aprobar desde `In Progress` si ya verificó el resultado por Studio, llamada o pantalla compartida.

## GitHub

Este repositorio conserva la documentación versionada y buscable. Discord enlaza el contenido; no lo duplica. Más adelante Git también puede conservar scripts sincronizados desde Studio, pero no es requisito para todos hasta validar el workflow.

## Herramientas opcionales

- **Rojo:** solo el Lead lo usa en su proyecto separado. Él adapta el sync a los demás, que trabajan directamente en Studio; avisen antes de editar el mismo Script. Script Sync no es requisito.
- **VS Code:** útil al trabajar con archivos, no necesario para construir Parts en Studio.
- **Blender:** útil para adaptar o crear assets cuando haga falta. Ya hay candidatos revisados por el Lead; revisen primero qué pueden reutilizar.

No añadimos CI/CD, paquetes, frameworks ni publicación automática mientras no resuelvan un problema actual.
