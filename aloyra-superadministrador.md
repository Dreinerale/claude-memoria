---
name: aloyra-superadministrador
description: "Cómo quiere el usuario administrar PROA (antes Aloyra) como dueño de la plataforma: panel aparte con verificación por celular, empresas que se suspenden sin borrarse y módulos que se prenden o apagan por empresa."
metadata: 
  node_type: memory
  pinned: false
  originSessionId: 95be86c1-69e4-4181-996d-6927929c90bb
  modified: 2026-09-14T17:35:27.258Z
---

# El superadministrador de PROA

En septiembre de 2026 el usuario, como dueño de Aloyra (hoy PROA, el PMS que vende
Noabits), pidió poder agregar o quitar empresas y prender o apagar funciones
del PMS para cada una. Eligió cómo tenía que ser, y esas decisiones valen para
todo lo que se construya del lado de la plataforma:

- **Entra por un panel aparte**, no por la pantalla de los negocios, con
  usuario, clave y un código de verificación del celular (TOTP). Su cuenta
  no pertenece a ninguna empresa: el panel muestra empresas, módulos y cifras
  generales, nunca reservas, huéspedes ni ventas de un negocio. Se le advirtió
  que sin el segundo factor, una clave robada daría control de todas las
  empresas, y eligió el panel con verificación.
- **Quitar una empresa es suspenderla, no borrarla.** Nadie de ese negocio
  entra y su página deja de reservar, pero los datos se conservan y se puede
  reactivar. La razón: las facturas electrónicas deben guardarse por ley.
- **Módulos que se prenden y apagan por empresa:** Restaurante y caja,
  Facturación electrónica y Motor de reservas web. El hotel (reservas,
  habitaciones, limpieza) quedó siempre encendido porque no lo marcó.

Al construirlo, apagar un módulo tiene que cortar también en la base (los
permisos de ese módulo dejan de valer), no solo esconder el menú.
