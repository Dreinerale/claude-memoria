---
name: deducir-producto-desde-sku-interno
description: "En tareas de emparejar SKUs internos con productos/fotos reales, el nombre interno es una aproximación y hay que deducir el producto real con criterio."
metadata: 
  node_type: memory
  pinned: false
  originSessionId: 66b99e33-2b7a-4176-a169-e81f5b0728f7
  modified: 2026-09-03T05:08:29.089Z
---

# Los nombres de SKU internos del usuario son aproximados: deducir el producto real

El usuario revende productos de varias marcas (por ejemplo Chicco, bajo la
empresa Noabits) y sus listados internos de SKU no son fiables al pie de la
letra: pueden tener errores de tipeo, nombres de color o de "edición" que no
coinciden con cómo los llama el retail, y códigos que no son el EAN. En una
tarea de recopilar fotos de producto para 76 SKUs de Chicco lo dijo así:
«puede que te confunda el nombre como lo tenemos nosotros así que puedes usar
tu inteligencia para deducir qué es ese», y remató «y lo demás también con
esta lógica».

## Reglas que pidió aplicar

- **El sufijo de color es una pista, no un dato.** Si el SKU dice `-VE`
  (verde) pero no existe ninguna imagen verde de ese producto en el mercado,
  no es verde: es la variante que sí existe (típicamente azul/celeste, o la
  transparente). Igual con `-AM` (amarillo) que no existe.
- **Género sin distinción visual: rosa = nena, azul/celeste = nene.** Cuando
  un producto se vende en un pack unisex "x2" sin versión Girl/Boy separada,
  se asume igual y se asigna la misma foto a ambos sub-SKU.
- **Mismo producto bajo dos códigos: se reutiliza la foto.** Si dos familias
  de SKU describen el mismo producto (mismo tipo, edad y color) con códigos
  distintos, probablemente una es el x1 y otra el x2; se les asigna la misma
  imagen.
- Aun así, **no inventar**: si el producto genuinamente no existe en el
  mercado objetivo, o no se consigue una foto de la variante correcta, se
  deja como DUDOSO con la razón anotada. La deducción cubre el nombre, no la
  existencia.

## Cómo verificar antes de asignar

Conviene mirar la imagen, no solo el título: confirmar el color real y, si el
producto tiene gráficas impresas con texto (por ejemplo los vasos Advanced
Cup de Chicco llevan impresa la palabra de la edición: "imagine", "wonder"),
leer ese texto para casar la edición exacta.
