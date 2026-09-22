---
name: estilo-de-trabajo-en-sistemas
description: "Cómo pide el usuario que se construyan sus sistemas: revisiones repetidas buscando mejoras, y código simple del que pueda aprender."
metadata: 
  node_type: memory
  pinned: true
  originSessionId: 2f94258a-56d7-411d-a2bd-a6121218487f
  modified: 2026-08-23T05:34:10.335Z
---

# Cómo construir sistemas para este usuario

El usuario dio dos instrucciones permanentes al empezar el PMS de Termales
Arco Iris, y las planteó como forma de trabajar, no como algo de esa tarea
puntual.

## Revisar varias veces buscando qué mejorar

Sus palabras fueron «dale siempre varias revisadas buscando qué mejorar».
No basta con entregar algo que funcione: espera que se vuelva sobre el
trabajo ya hecho a buscar defectos y oportunidades de mejora antes de darlo
por terminado. En la práctica esto significa correr linters y advertencias
de seguridad, escribir pruebas que intenten romper lo construido en vez de
confirmar que funciona, y arreglar lo que aparezca en la misma entrega en
lugar de solo mencionarlo. Cuando pidió esto estábamos por tocar bases de
datos, y lo justificó con eso: los errores de esquema y de permisos son
caros de deshacer después.

## Simple de entender, porque quiere aprender

Pidió que el sistema fuera «lo más simple para aprender también». El usuario
está aprendiendo mientras construimos, así que la legibilidad pesa tanto
como la corrección: conviene preferir la solución directa sobre la
ingeniosa, comentar el porqué de las decisiones (no lo que hace la línea),
nombrar las cosas en español como las nombra el negocio, y explicar los
conceptos nuevos cuando aparecen. Cuando una decisión técnica tiene
alternativas, quiere entender el porqué de la elegida.
