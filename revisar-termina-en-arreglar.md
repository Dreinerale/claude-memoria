---
name: revisar-termina-en-arreglar
description: "Cuando el usuario pide revisar o auditar algo, espera que se arregle lo que se encuentre, no solo un informe de hallazgos."
metadata: 
  node_type: memory
  pinned: false
  originSessionId: 55c56f65-eba6-441d-9a4e-697860db6b9c
  modified: 2026-09-09T22:19:28.986Z
---

# Una revisión termina con las cosas arregladas

Al pedir una revisión de integridad de datos del PMS de Termales Arco Iris,
entregué primero un informe con los hallazgos y ofrecí al final dos caminos:
armar una página con el detalle y el SQL de arreglo, o empezar corrigiendo
los dos problemas más urgentes. Su respuesta fue «prefiero que corrijas
todo», y cuando le pedí datos para seguir, «termina la tarea».

La lección es que para este usuario **pedir una revisión es pedir el
arreglo**. El informe es el medio, no el producto. Conviene entonces
plantear el trabajo de una revisión como: encontrar, corregir, comprobar que
quedó corregido y contarlo al final, todo en la misma entrega, sin detenerse
a preguntar si se procede con las correcciones.

Esto encaja con lo que ya había dicho sobre entregar cosas funcionando en
vez de listas para instalar, pero es una situación distinta: allí se trataba
de construir, aquí de auditar. Un informe de auditoría sin los arreglos
hechos le resulta trabajo a medias.

## Lo que sí conviene seguir separando

No todo entra en «corregir todo». Hay dos clases de acción que siguen
necesitando su decisión, y explicarle por qué quedaron fuera es parte de la
entrega, no una excusa:

- Lo que requiere que una persona haga algo físico. En su caso, dos turnos
  de caja llevaban semanas abiertos con ventas adentro; cerrarlos yo habría
  registrado un cuadre falso, porque nadie había contado el cajón.
- Lo que borra o reescribe historia real de plata o de inventario. Anular en
  bloque las ventas de prueba habría devuelto al stock unidades que no están
  en la bodega.
