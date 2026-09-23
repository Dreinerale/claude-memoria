---
name: proapms-clientes-fundadores-sin-cobro
description: "Termales Arco Iris y Termales El Ocho no pagan suscripción de ProaPMS y tienen soporte gratis, por ser los primeros clientes."
metadata:
  node_type: memory
  pinned: false
  originSessionId: 0bd6d3bb-2517-4407-a567-7eac914837e9
  modified: 2026-09-23T19:48:29.701Z
---

# Arco Iris y El Ocho: sin suscripción y con soporte gratis

En septiembre de 2026 el usuario decidió que **Termales Arco Iris (empresa 1,
código 1000) y Termales El Ocho (empresa 2, código 1001) quedan excluidas del
plan de suscripción de ProaPMS y tienen soporte gratis**, porque fueron sus
primeros clientes.

Cómo aplicarlo:
- Nunca se les cobra, no se les mandan avisos de vencimiento, no se les pausa
  ni se les pone en modo consulta. Técnicamente ya es así: no tienen fila en
  `suscripciones_empresa`, y sin suscripción el acceso no vence.
- En el panel de plataforma se muestran como clientes de cortesía (sin
  cobro), no como «vencidas» ni «sin plan».
- Cualquier regla nueva de cobro, límites o avisos debe excluirlas a
  propósito, no por casualidad.
