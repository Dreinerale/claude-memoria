---
name: lo-del-negocio-no-vive-en-el-portatil
description: "El computador desde el que trabaja el usuario es su portátil personal; lo que un negocio necesita corriendo (agente de impresión, servicios) se instala en un equipo del establecimiento."
metadata: 
  node_type: memory
  pinned: false
  originSessionId: 71ca7084-fe02-401c-aeb6-6c152aa6608b
  modified: 2026-09-16T18:18:09.407Z
---

# Lo que el negocio necesita encendido no se instala en el portátil del usuario

El equipo donde corre Claude Code es el **portátil personal** del usuario, que
él se lleva. En septiembre de 2026 el agente de impresión del PMS de Termales
Arco Iris había quedado instalado ahí, con arranque automático, y la cocina
dependía de ese portátil para recibir comandas. El usuario lo corrigió con
estas palabras: «esta es mi computadora personal y yo me voy y la idea es que
quede configurado en el establecimiento».

## La regla

Todo lo que un negocio necesita funcionando cuando el usuario no está —el
agente de impresión, tareas programadas, servicios locales— va en un
computador **del establecimiento** que se quede allá y permanezca prendido
(normalmente el de la caja). Si desde la sesión no se alcanza ese equipo, se
entrega un instalador de doble clic que lo deje funcionando solo (arranque
al prender el equipo, sin ventana que se pueda cerrar), en vez de instalarlo
en el portátil "mientras tanto".

## Cuidado al probar desde el portátil

Un agente con una clave válida en el portátil sigue tomando pedidos de la
cola cuando el portátil sale de la red del negocio, falla al imprimir y gasta
los reintentos de esos tiquetes. Por eso no conviene dejarle credenciales
válidas al agente del portátil, ni dejarlo arrancando solo.
