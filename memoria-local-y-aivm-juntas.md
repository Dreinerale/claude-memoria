---
name: memoria-local-y-aivm-juntas
description: El usuario decidió usar la memoria local de Claude y AIVM Brain al mismo tiempo; la memoria local no se apaga.
metadata:
  node_type: memory
  pinned: false
  originSessionId: 882cf231-ca5e-4b04-92ea-386e48ea9130
  modified: 2026-09-23T19:44:05.161Z
---

# Memoria local y AIVM Brain, las dos a la vez

El 23 de septiembre de 2026 el usuario conectó Claude Code a AIVM Brain. El
instalador apagó la memoria local (`autoMemoryEnabled: false`) y dejó un
playbook que prohíbe guardar en ella. Se le recomendó usar las dos y aceptó
(«Sí, hazlo»), así que se volvió a prender.

La razón: la memoria local ya funciona y guarda las reglas que aplican en
cada sesión (responder en español, forma de trabajar, decisiones de los
proyectos). Si AIVM falla (sin internet, clave vencida, servicio caído),
Claude no debe arrancar sin saber nada del usuario. Además, AIVM todavía está
en prueba.

Reparto acordado: las preferencias y decisiones duraderas van en la memoria
local, y el historial de sesiones y los documentos quedan en AIVM. Si al
reconectar o actualizar AIVM vuelve a quedar `autoMemoryEnabled: false`, hay
que volver a prenderlo y avisarle al usuario.
