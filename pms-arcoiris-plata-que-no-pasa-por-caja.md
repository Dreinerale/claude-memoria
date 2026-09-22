---
name: pms-arcoiris-plata-que-no-pasa-por-caja
description: Solo el efectivo exige turno de caja abierto; la transferencia y los pagos hechos desde la web llegan al banco y no deben obligar a abrir caja.
metadata: 
  node_type: memory
  pinned: false
  originSessionId: f4bbb2a9-942e-4df8-8932-e4bf8902dee3
  modified: 2026-09-11T03:44:56.073Z
---

# La plata que no pasa por la caja no exige abrir caja

El dueño de Termales Arco Iris corrigió esto mirando la operación real:
un huésped paga la reserva por la página, el dinero cae directo a la
cuenta de Bancolombia, y aun así el PMS le pedía a recepción **abrir un
turno de caja** para poder registrar ese pago. Sus palabras fueron: «si
vamos a la practica real el cliente ya pago por la web y llega a la
cuenta directo».

## La regla

El turno de caja existe para una sola cosa: que al cerrar, alguien pueda
contar los billetes del cajón y comparar. Por eso **el efectivo sí exige
turno abierto**; sin eso entra plata al cajón que ningún cuadre reclama,
que fue justamente el error que costó 4.340.000 en pagos sin turno.

Pero la transferencia, Nequi, Daviplata y la tarjeta **no entran al
cajón**: se concilian contra el extracto del banco. Exigirles turno
obliga a recepción a abrir caja para anotar plata que nunca estuvo ahí, y
peor, ensucia el efectivo esperado del cierre con dinero que nadie puede
contar.

En la base esto se distingue con la columna `cuenta_en_caja` de
`formas_pago`. Esa columna es la que debe decidir si se exige turno, no
el hecho de estar registrando un pago.

## Al construir flujos de cobro

Conviene pensar primero en cómo ocurre de verdad en el hotel, no en cómo
queda ordenado el modelo de datos. La pregunta útil es: ¿esta plata la va
a tener que contar alguien al cerrar el turno? Si la respuesta es no, el
turno no pinta nada en ese registro.
