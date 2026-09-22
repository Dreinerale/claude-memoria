---
name: entregar-funcionando-no-listo-para-instalar
description: "El usuario espera que lo que se le entrega quede instalado y funcionando, no empaquetado para que él lo active."
metadata: 
  node_type: memory
  pinned: false
  originSessionId: a3012558-4014-4480-982e-36fa6fd47191
  modified: 2026-09-07T20:58:24.448Z
---

# Lo que se entrega queda funcionando, no listo para instalar

Al exportar su memoria a Codex armé el paquete completo —el resumen global, la
carpeta con las 17 lecciones y un `AGENTS.md` por proyecto— pero dejé el archivo
global como un índice que le decía a Codex cuál archivo leer en cada caso, en
vez de meter el contenido adentro. Su respuesta fue: «integra de una vez la
carpeta en codex de manera que yo abra una sesion y ya tenga todo el contexto».

Es el mismo patrón que ya había aparecido con el PMS de Termales Arco Iris,
donde pidió que toda modificación se publicara sin preguntar: un trabajo que
todavía necesita un paso suyo para servir, para él no está terminado. La forma
correcta de cerrar una tarea de configuración o instalación es dejarla activa y
comprobada en su máquina —tocando la configuración que haga falta— y recién
entonces contarle qué quedó hecho, en vez de entregar algo correcto pero
inerte con instrucciones de cómo activarlo.

De ahí se desprende también cómo verificar: no basta con que los archivos estén
en su sitio. Conviene abrir de verdad la herramienta y comprobar que el efecto
se produce —en este caso, correr `codex exec` con una pregunta que solo se puede
responder si la memoria se cargó— antes de decir que quedó integrado.
