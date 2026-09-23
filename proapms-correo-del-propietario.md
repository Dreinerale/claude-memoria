---
name: proapms-correo-del-propietario
description: "Decisiones del usuario para el correo verificado y la recuperación de contraseña de ProaPMS (Prioridad 2): camino B, Resend y 3 días para verificar."
metadata:
  node_type: memory
  pinned: false
  originSessionId: 0bd6d3bb-2517-4407-a567-7eac914837e9
  modified: 2026-09-23T15:33:13.422Z
---

# Correo del propietario en ProaPMS

En septiembre de 2026 el usuario decidió cómo se construye la Prioridad 2 del
plan de mejoras de ProaPMS (correo verificado, recuperación y cambio de
correo), después de que se le explicaran las alternativas.

- **Camino B**: la cuenta interna de Supabase Auth sigue siendo
  `supervisor@CODIGO.local` y la entrada por código + usuario + clave no se
  toca. El correo real y verificado vive aparte, en una tabla propia, y un
  servidor de ProaPMS maneja los enlaces (guardando solo su huella, de un
  solo uso y con vencimiento). Se descartó volver el correo real la cuenta
  (camino A) porque para que el dueño siguiera entrando con código la base
  tendría que revelar su correo personal a quien conociera el código.
- **Resend** es el servicio para enviar los correos. El dominio
  `proapms.com` se administra en **Hostinger** (hPanel); ahí van los registros
  DNS que pide Resend. El usuario deja la sesión del hPanel abierta en su
  navegador para que se entre a configurarlos cuando haga falta.
- **3 días** para verificar: el cliente nuevo entra de una vez; si no
  verifica en 3 días, se pausa el acceso operativo hasta verificar, sin
  perder datos.
- **Contra robots, una prueba propia** (el navegador resuelve un cálculo que
  el servidor comprueba) en vez de Cloudflare Turnstile: sin cuentas externas
  ni compartir datos de clientes con terceros.
- **Varios alojamientos por dueño, sin tocar las reglas de acceso de las
  tablas**: cada alojamiento conserva su propia cuenta de supervisor, y el
  correo verificado del dueño las une (cambiar de alojamiento sin volver a
  escribir la clave, agregar otro desde la sesión). El usuario lo pidió para
  ya, en septiembre de 2026, en vez de dejarlo para después.
- Se trabaja por fases: A (registro en pasos, recuperar tras recargar, aviso
  de sesión abierta, sin correos), B (correos) y C opcional (entrar con
  correo). La identidad de un dueño con varios alojamientos queda para
  después, porque toca las reglas de acceso de todas las tablas.

Por qué importa: la Fase B se construye sobre estas decisiones; no hay que
volver a preguntarlas.
