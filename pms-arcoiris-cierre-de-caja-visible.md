---
name: pms-arcoiris-cierre-de-caja-visible
description: "El dueño de Termales Arco Iris eligió que el cierre de caja muestre cuánto efectivo debería haber, en contra del conteo a ciegas."
metadata: 
  node_type: memory
  pinned: false
  originSessionId: 2f94258a-56d7-411d-a2bd-a6121218487f
  modified: 2026-08-28T12:23:15.111Z
---

# El cierre de caja muestra cuánto debería haber, y fue una decisión del dueño

El cierre de turno del PMS Arco Iris nació con **conteo a ciegas**: la
pantalla no le decía al cajero cuánto efectivo debía haber en el cajón,
porque si lo ve, teclea esa cifra y el descuadre no aparece nunca. El
usuario decidió cambiarlo, y conviene no revertirlo por considerar el
conteo a ciegas una buena práctica.

## Por qué lo cambió

El problema no era la ceguera sino que era **a medias**. El resumen enseñaba
las ventas pero callaba los abonos a cuentas de clientes. En un turno donde
toda la plata entró por abonos —pasó de verdad— la pantalla decía «ventas:
$0» y a renglón seguido exigía ese efectivo en el cajón. El usuario lo
describió como que el sistema «lo asume nada más»: desde el mostrador no se
lee como un control, se lee como que el sistema se inventa una plata.

Puesto a elegir entre esconder mal y mostrar bien, eligió **mostrar**. El
cierre ahora desglosa peso por peso de dónde sale lo que debe haber —base,
ventas en efectivo, abonos a cuentas, ingresos y egresos— y nombra de qué
cuenta vino cada abono.

## La lección general

Cuando una pantalla de control le oculta algo al empleado, el usuario
prefiere que la ocultación sea **completa y coherente** o que no exista. Una
cifra que aparece sin explicación le quita credibilidad al sistema delante
de quien lo usa todos los días, y eso le importa más que la pureza del
control. Lo que queda vigilando los faltantes es el historial de
diferencias, que un supervisor revisa.

## Otra cosa que salió de ahí

Las pruebas automáticas abren y cierran turnos de verdad contra la base de
producción, y **no se debe cerrar por detrás el turno de un cajero real**:
es su plata y le falsearía el cuadre. La prueba de operación busca una caja
sin turno abierto y, si no hay ninguna, se detiene explicándolo en vez de
tocar nada.
