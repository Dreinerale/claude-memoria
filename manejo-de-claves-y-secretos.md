---
name: manejo-de-claves-y-secretos
description: "El usuario prefiere que las claves y secretos los consiga y los escriba uno mismo, y no le preocupa que queden en el historial de la conversación."
metadata: 
  node_type: memory
  originSessionId: 08bbc5ad-f964-443a-b807-c9ba561e49f9
  modified: 2026-09-16T19:10:37.402Z
---

# Manejo de claves y secretos

Al configurar el proyecto de Grupo Babystore hizo falta la clave
`service_role` de Supabase. Por prudencia le pedí que la escribiera él mismo
en el archivo `.env` y le aclaré que no me la pegara en el chat, porque esa
clave se salta todas las políticas de seguridad y lo que pasa por la
conversación queda en el historial.

Su respuesta fue: «haz tu la service_role no importa que quede en el
historial. Hazlo».

## Qué hacer entonces

Cuando una tarea necesite una clave, un token o cualquier credencial,
**conseguirla y escribirla uno mismo** en lugar de derivarle a él la tarea
manual de copiarla y pegarla. El usuario ya evaluó el riesgo de que esos
valores queden en el historial y decidió que le resulta aceptable; volver a
plantearle esa objeción cada vez le hace perder tiempo y no le aporta nada
que no haya considerado.

Vale mencionar una vez, en una frase, cuando algo tiene una consecuencia que
él podría no haber visto, pero sin condicionar la entrega a que él haga el
trabajo manual.

**Rotar una clave solo porque quedó escrita en el chat no se recomienda.** En
septiembre de 2026, con la clave del agente de impresión del PMS Arco Iris, se
le sugirió dos veces cambiarla por eso y respondió: «No cambiare la clave esa
va a quedar no importa que quede escrito en el chat». El chat, para él, no es
una exposición. Rotar sí tiene sentido si la clave se filtró por otro lado (un
repositorio público, una página publicada).

Esto **no** cambia dos cosas que siguen valiendo: los secretos no entran a
git (van en `.env`, con el `.env` en el `.gitignore` y un `.env.ejemplo` sin
valores), y las claves que el navegador publica —en Vite, todo lo que empieza
con `VITE_`— no pueden ser las secretas.
