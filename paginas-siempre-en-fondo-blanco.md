---
name: paginas-siempre-en-fondo-blanco
description: "Las páginas web para clientes van con fondo blanco fijo y letra oscura, sin versión en modo oscuro."
metadata: 
  node_type: memory
  pinned: false
  originSessionId: e0dc1c05-3260-4e47-adb4-715e9390a94d
  modified: 2026-09-04T20:26:16.859Z
---

# Las páginas para clientes van siempre en fondo blanco

Al revisar la propuesta de Termales El Ocho, el usuario pidió: «el fondo de la
página, los espacios vacíos donde va el texto, lo quiero blanco y las letras
oscuras». Lo tuvo que pedir dos veces, porque la primera vez yo entendí que
hablaba de la paleta y la página seguía cambiando sola.

La causa era que la página traía tokens de modo oscuro
(`@media (prefers-color-scheme: dark)` y `:root[data-theme="dark"]`). El usuario
revisa su trabajo en un visor con tema oscuro, así que la página se le volvía
negra sola y nunca veía el diseño que él había pedido. Peor todavía, eso es lo
que iba a ver el cliente si tenía el celular en modo oscuro.

Por eso, en las páginas web que él le presenta a sus clientes no se deben
escribir bloques de modo oscuro: hay que dejar un solo juego de colores, con
fondo blanco y letra oscura, pintados explícitamente en `body`. Que la página se
adapte al tema del visitante suena a buena práctica, pero aquí trabaja en contra
del objetivo, que es que la pieza se vea igual para todo el mundo.

Esto vale para las páginas de clientes. No hay que extenderlo sin preguntar a
herramientas internas ni al PMS, donde el modo oscuro puede ser deseable.
