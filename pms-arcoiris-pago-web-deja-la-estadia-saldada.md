---
name: pms-arcoiris-pago-web-deja-la-estadia-saldada
description: "Si el huésped paga completo en la página, la reserva debe llegar al PMS confirmada y con la estadía ya saldada, para que en el check-out solo queden los consumos."
metadata: 
  node_type: memory
  pinned: false
  originSessionId: f4bbb2a9-942e-4df8-8932-e4bf8902dee3
  modified: 2026-09-11T04:11:11.447Z
---

# El que paga por la web no vuelve a pagar en recepción

El dueño de Termales Arco Iris lo pidió así, con estas palabras: «mi idea
es pagan por via web completo les llega la reserva al sistema, el sistema
aparece la reserva confirmada ya porque ya pago completo la idea es que
entre la cuenta en 0 o que refleje que ya pago la estadia del hotel y al
momento del check out o registrar pago solo le aparezca los consumos o
gastos que tuvo dentro de las termales».

## La regla

Cuando alguien paga la estadía completa desde la página:

1. La reserva entra **confirmada**, no provisional.
2. El pago queda **registrado solo**, sin que recepción lo escriba.
3. La cuenta de la estadía queda en cero.
4. En el check-out solo aparece lo que consumió adentro: restaurante, bar,
   lo que se cargó a la habitación.

Recepción no debe tener que anotar a mano una plata que el huésped ya
pagó. Facilitar ese registro no basta: la corrección fue justamente que
seguir pidiéndoselo «es estar en las mismas».

## El cuidado que sí hace falta

Mientras no haya pasarela de pagos, lo único que el sistema sabe es que el
huésped **dice** que pagó y subió un comprobante. Por eso el pago se
registra de una vez pero marcado como **sin verificar**, y el hotel lo
coteja después contra el extracto del banco. Así la cuenta refleja la
realidad para el huésped desde el primer momento, y el hotel conserva una
lista de lo que le falta confirmar.

Lo que no se debe hacer es bloquear el flujo por esa duda: la reserva
queda saldada y la verificación va por detrás, no por delante.
