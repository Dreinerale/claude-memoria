---
name: pms-arcoiris-donde-se-usa
description: "En qué aparatos se usa el PMS de Termales Arco Iris, y qué exige eso de cada pantalla nueva."
metadata: 
  node_type: memory
  pinned: false
  originSessionId: 2f94258a-56d7-411d-a2bd-a6121218487f
  modified: 2026-08-27T20:02:49.181Z
---

# El PMS Arco Iris se abre en computador, tablet y celular

El usuario fue precisando, a lo largo del trabajo, dónde se usa el sistema.
Conviene tenerlo presente antes de diseñar cualquier pantalla nueva, porque
cambia lo que hay que comprobar antes de darla por terminada.

## Los tres tamaños

Se usa en **computador** en recepción, en **tablet** en la cocina, y también
en **celular** — esto último lo pidió explícitamente al ver el sistema
publicado. No basta con que funcione en pantalla grande: cada pantalla nueva
hay que verla a unos 390–414 píxeles de ancho antes de darla por hecha, y el
síntoma que delata el problema es el desplazamiento lateral.

Un truco que funcionó para comprobarlo cuando el navegador no deja cambiar
el tamaño de la ventana: meter la aplicación en un `iframe` de 414 píxeles
dentro de la propia página. Las media queries responden al ancho del marco,
así que se puede medir `scrollWidth - clientWidth` en cada ruta.

## Los puestos y la impresora

Hay tres puntos de venta —caja, restaurante y billar— y **una sola
impresora**, la POS-80C de la cocina, conectada por red. Las comandas de
cocina de los tres puestos salen por ahí; las bebidas del bar no se
imprimen.

## Publicado en internet, agente en la red local

El sistema está publicado en Vercel (https, público) y el agente de
impresión corre en la red local (http). Chrome pide permiso al usuario la
primera vez para que una página pública hable con la red local; hay que
darle *Permitir* una vez por equipo. Si eso alguna vez estorba, la
alternativa es entrar por la dirección local dentro del establecimiento, que
no tiene esa restricción.
