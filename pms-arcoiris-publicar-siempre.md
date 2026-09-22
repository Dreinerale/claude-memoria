---
name: pms-arcoiris-publicar-siempre
description: "El usuario pide que toda modificación del PMS Arco Iris se publique en Vercel al terminarla, para poder verla."
metadata: 
  node_type: memory
  pinned: false
  originSessionId: 2f94258a-56d7-411d-a2bd-a6121218487f
  modified: 2026-09-15T20:01:59.663Z
---

# Toda modificación se publica, sin preguntar

El usuario dio esta instrucción con esas palabras: «toda modificación
publícala para poder verla». No es para un cambio puntual, es su forma de
trabajar.

## Qué significa en la práctica

El PMS (hoy multiempresa, proyecto `proapms` en Vercel) está publicado en
<https://app.proapms.com>, el dominio propio que el usuario eligió en
septiembre de 2026 para que la dirección no llevara el nombre de un solo
negocio. Va en el subdominio `app` por decisión suya: `proapms.com` queda
reservado para la página web comercial del sistema, que él construye aparte,
así que nunca se debe apuntar la raíz del dominio al PMS. Las
direcciones `*.vercel.app` y `app.termalesarcoiris.com` quedaron de
respaldo: sirven lo mismo, pero no se nombran al entregar ni se usan para
comprobar que un cambio salió. El usuario tuvo que corregirlo con un «ojo,
recuerda que es app.proapms.com» después de recibir enlaces a la dirección
vieja. Esa es la dirección que se le entrega y el único sitio donde el
usuario mira el trabajo: no lee el código ni
levanta el servidor local. Un cambio que solo existe en el disco, para él,
todavía no existe. Así que al terminar una modificación de la carpeta `app/`
hay que desplegarla y darle el enlace, sin esperar a que lo pida y sin
preguntar si quiere que se publique.

Esto vino después de que en dos ocasiones se le entregara trabajo terminado
y probado que él no podía ver, con la pregunta «¿lo publico?» al final.

## Lo que no cambia

Publicar sigue siendo el paso final, después de las pruebas, no un
sustituto de ellas. Y conviene comprobar antes que `.vercelignore` siga
dejando fuera lo que no debe salir —la llave de ElevenLabs, el LEEME con la
clave de supervisor, las migraciones y las pruebas—, porque lo que se
publica queda accesible en internet.

Los cambios que no viven en `app/` —el agente de impresión, las
migraciones— no se despliegan ahí; esos se le muestran contándoselos o
corriéndolos.
