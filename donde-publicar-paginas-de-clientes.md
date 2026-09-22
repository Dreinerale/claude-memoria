---
name: donde-publicar-paginas-de-clientes
description: "Las páginas que el usuario le presenta a sus clientes van en un hosting real con URL propia, no en un Artifact de Claude."
metadata: 
  node_type: memory
  pinned: false
  originSessionId: cfe47665-e5d8-4abb-9c8b-7ddb8c950747
  modified: 2026-09-09T21:55:18.781Z
---

# Las páginas de clientes van en hosting real, no en Artifacts

Al terminar la landing del Hotel Dubái de Zetaquira la publiqué como
Artifact, que es lo más rápido y da un enlace que abre cualquiera. El
usuario primero pidió «publiques las 2 versiones para poder compartirlo y
que lo vean desde su navegador», y cuando le entregué los enlaces de
claude.ai respondió: «No lo quiero en artifact, ¿puede ser en github?».

## Qué significa en la práctica

Cuando el trabajo es una página que él le va a mostrar a un cliente suyo
—un hotel, unos termales, una peluquería—, la entrega no está completa
mientras viva en un Artifact. Hay que llevarla a un hosting de verdad:
GitHub Pages, Vercel o similar, con una URL que se pueda mandar por
WhatsApp, que no lleve la marca de Claude y a la que después se le pueda
apuntar un dominio propio. El Artifact sirve para revisar mientras se
trabaja, no como entrega final.

Conviene preguntarle desde el principio dónde quiere que quede publicada,
porque el destino cambia cómo se arma el archivo: para un Artifact las
imágenes tienen que ir incrustadas como data URI, porque un Artifact no
carga archivos externos, mientras que en un hosting normal deben ir como
archivos sueltos. La diferencia no es menor: la misma página pasó de 1,1 MB
a 29 KB al sacar las fotos del HTML, y así el navegador las guarda en
caché.

## Lo que hay que resolver antes

En su equipo hay git, pero no tenía identidad configurada, ni credenciales
de GitHub, ni `gh` instalado, y `winget install GitHub.cli` se quedó colgado
sin instalar nada. La vía que no depende de instalar nada es que él genere
un token personal de GitHub y lo pegue en el chat, y desde ahí usar git con
la API de GitHub. Eso encaja con su preferencia, ya anotada aparte, de
conseguir y escribir él mismo las claves.
