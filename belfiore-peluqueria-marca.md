---
name: belfiore-peluqueria-marca
description: Identidad visual y contexto fijados por el usuario para el proyecto de agendamiento de Belfiore Peluquería.
metadata: 
  node_type: memory
  pinned: false
  originSessionId: 7ccdfb43-0527-4f6b-a299-e86a0c38861d
  modified: 2026-08-19T19:20:02.249Z
---

# Belfiore Peluquería — identidad y contexto del proyecto

El usuario está construyendo una plataforma de agendamiento de horas para su propio salón, **Belfiore Peluquería**, ubicado en El Mirador Poniente 1012, Ovalle, Chile. Como el negocio es chileno, todo debe usar pesos chilenos (formato `es-CL`, por ejemplo `$12.000`), teléfonos con prefijo `+56 9` y el vocabulario local: en Chile se dice «reservar una **hora**», no «una cita».

## Paleta y tipografía que el usuario eligió

El usuario rechazó explícitamente una primera propuesta de color (magenta con neutros lilas) y una segunda (verde esmeralda con dorado), y luego fijó él mismo la paleta definitiva. Hay que usar exactamente estos tres colores:

- `#F9F6F0` — fondo crema de toda la interfaz
- `#E5D3B3` — arena, para selección y realce
- `#1A1A1A` — negro, para texto y acciones principales

La tipografía es **Inter**, en todos los roles. No introducir familias tipográficas adicionales ni colores fuera de esos tres sin que el usuario lo pida; cuando haga falta distinguir estados (por ejemplo confirmada / sin respuesta / completada), diferenciarlos por peso de relleno en vez de agregar matices nuevos.

## Prioridad de uso

El equipo del salón trabaja **casi exclusivamente desde el celular**, así que el panel de administración se diseña móvil primero: lista cronológica en vez de grilla de columnas en pantallas chicas, controles con área táctil amplia y acciones en hojas que suben desde abajo. La versión de escritorio es la secundaria.
