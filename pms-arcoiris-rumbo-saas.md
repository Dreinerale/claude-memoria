---
name: pms-arcoiris-rumbo-saas
description: "El PMS de Termales Arco Iris se construye como SaaS multiempresa con facturación DIAN propia, no como sistema para un solo negocio."
metadata: 
  node_type: memory
  pinned: false
  originSessionId: 2f94258a-56d7-411d-a2bd-a6121218487f
  modified: 2026-09-13T04:50:03.533Z
---

# El PMS Arco Iris se construye para venderse, no solo para usarse

El usuario tomó dos decisiones sobre el rumbo del PMS de Termales Arco Iris
que conviene dar por sentadas en cualquier sesión futura, porque cambian el
diseño de casi todo lo que se toque.

## Es un producto SaaS, no el sistema de un negocio

La intención es **comercializar el PMS con un modelo de pago mensual**, para
que otros negocios lo implementen. El usuario lo dijo con esas palabras al
pedir que "otras empresas a futuro puedan unirse".

La consecuencia práctica es que todo lo nuevo nace multiempresa: cada tabla
que guarde datos del negocio lleva `empresa_id`, y cada política de RLS
compara contra la función `mi_empresa()`. La mudanza del esquema viejo, que
era de un solo negocio, quedó terminada en septiembre de 2026 (migraciones
64 a 68). Cuando el usuario la autorizó, puso como condición que ningún dato
de una empresa pueda modificar los de otra, porque los primeros dos clientes
(Arco Iris y El Ocho) son competidores; por eso cada tabla nueva lleva además
su llave foránea compuesta y el disparador `candado_de_empresa`, y después
de tocar la base se corre `pruebas/prueba-multiempresa.mjs` exigiendo cero
fallas.

## Cómo lo ve cada cliente

Al sumar a Termales El Ocho como segunda empresa (septiembre de 2026), el
usuario eligió tres reglas que valen para cualquier cliente nuevo:

- **Un solo PMS con marca Noabits**, no una copia por cliente. La pantalla
  de entrada es neutra (Noabits) y, al entrar, cada quien ve el nombre y el
  logo de su propio negocio. Copias separadas obligarían a publicar cada
  arreglo varias veces.
- **Se entra con un código numérico de empresa.** El usuario pidió que el
  código sea un número y no el nombre: Arco Iris es 1000, El Ocho 1001, y
  cada negocio nuevo toma el siguiente. La primera vez el equipo lo escribe
  y lo recuerda. Aclaró además que «solo es el código para entrar»: las
  cuentas de acceso NO se renombran (siguen siendo supervisor@arcoiris.local);
  la base traduce el código al dominio de las cuentas.
- **Los avisos por correo salen del buzón propio de cada negocio**, nunca
  del de otro cliente: un aviso de El Ocho que saliera de
  admin@termalesarcoiris.com le mostraría la competencia al huésped.
  Mientras un negocio no tenga buzón configurado, sus reservas entran al PMS
  sin correo.

## La facturación electrónica se hace adentro, no con un proveedor

Se le presentaron dos caminos —contratar un proveedor tecnológico, o
habilitar el software propio ante la DIAN— y **eligió el propio**: la
facturación queda dentro del PMS y el PMS se registra como software ante la
DIAN.

Eso implica certificado de firma digital, registro del software, set de
pruebas y generación de XML UBL con su CUFE. Y como además se va a vender a
otras empresas, cada empresa cliente necesita lo suyo por separado
(certificado, Software ID, PIN, resoluciones), lo que a su vez obliga a
guardar secretos ajenos con mucho cuidado: en el proyecto van en una tabla
propia con RLS encendido y sin ninguna política, de modo que ningún usuario
conectado los alcance.

Vale la pena recordarle, sin repetirlo cada vez, que vender el servicio de
facturación a terceros roza el rol regulado de *proveedor tecnológico* y que
eso lo debe confirmar con alguien especializado.
