---
name: conseguir-fotos-de-productos-por-sku
description: "Al buscar las fotos que faltan de un listado de SKU, hay que revisar en cualquier tienda, no quedarse en MercadoLibre."
metadata: 
  node_type: memory
  pinned: false
  originSessionId: b00f4836-d7d7-4703-9e6c-76d815c49d28
  modified: 2026-09-03T06:05:51.501Z
---

# Conseguir fotos de productos por SKU

El usuario tiene una tarea recurrente: entrega un Excel con SKU, código de
barras y descripción de una marca (Chicco, Suavinex, Nuk, Baby Innovation…) y
pide "conseguir las imágenes igual como venimos haciendo". El flujo es bajar la
foto de cada producto, nombrar el archivo con el SKU sin espacios ni guiones más
un índice entre paréntesis (`BI00004AZ(1).webp`), y dejar dos reportes: uno de
pendientes y otro de matches dudosos o de fuentes no oficiales
(`reporte_dudoso_no_encontrado.csv`).

## Para los SKU que faltan, buscar en cualquier página

Cuando quedan SKU sin foto, el usuario fue explícito: "revisa los pendientes no
solamente en Mercado Libre, en cualquier página que aparezca; en alguna deben
salir las que faltan". No hay que frenar en MercadoLibre ni entregar una lista
de pendientes sin haber agotado otras fuentes. Sirven el sitio oficial de la
marca en otros países (por ejemplo `babyinnovation.com.uy`, que suele conservar
productos viejos que el sitio argentino descontinuó), los mayoristas oficiales
(BEMAR, Grupo Baby Store) y cualquier tienda minorista que revenda la marca
(muchas están hechas en Tiendanube o WooCommerce y se pueden leer directo). La
expectativa es que la lista final de pendientes quede lo más cerca posible de
cero.
