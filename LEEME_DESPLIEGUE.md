# Aula del Taller Antilavado 360 — cómo se publica

Es lo mismo de siempre: zip → repositorio de GitHub → publicar en Netlify.
La única diferencia es que este sitio **va cerrado con contraseña**, y esa contraseña
se pone **una sola vez, con un interruptor de Netlify**. No hay nada que editar en el código.

Contraseña acordada: `360Educa2026`

---

## Los pasos

1. **GitHub** — repositorio nuevo, por ejemplo `aula-antilavado360`.
   Sube el contenido de esta carpeta tal cual: `index.html`, la carpeta `s01/`,
   `netlify.toml`, `_headers` y `robots.txt`.

2. **Netlify** — *Add new site* → *Import an existing project* → elige ese repositorio.
   Sin comando de build. *Publish directory*: un punto (`.`)

3. **La contraseña** — en Netlify, dentro del sitio:
   *Site configuration* → *Access & security* → *Visitor access* → **Password protection**
   → escribe `360Educa2026` → guardar.

   Si tu plan Pro es de los de créditos, la opción se llama *Project visibility*.
   Es la misma función con otro nombre.

4. **Compruébalo** — abre la liga en una ventana de incógnito. Debe pedir la contraseña
   antes de mostrar nada.

Listo. No hay paso 5.

---

## Por qué este sitio va aparte del que ya tienes

La contraseña de Netlify protege **el sitio completo**. No se puede aplicar sólo a una carpeta.
Si metieras el aula dentro del micrositio público, cerrarías también la guía, el autodiagnóstico
y la calculadora, que son abiertas a propósito.

Por eso son dos:

| Sitio | Qué tiene | Acceso |
|---|---|---|
| El que ya tienes | Guía, autodiagnóstico, calculadora, juego | Abierto |
| Éste | El aula: S01 a S06 con sus descargables | Cerrado |

Desde el público puedes poner un enlace al aula. Quien no tenga la clave, no pasa.

---

## Para la sesión 2 y las siguientes

1. Duplica la carpeta `s01/` y llámala `s02/`.
2. Cambia el contenido.
3. En `index.html`, la tarjeta de la sesión 2 ya está hecha: quítale la palabra `soon`
   y ponle `href="s02/"`.

---

## Dos cosas que conviene recordar

**Los descargables son copias.** El Excel, el PDF y la presentación viven físicamente
dentro de `s01/`. Si más adelante corriges alguno, hay que volver a copiarlo ahí,
o la gente descarga la versión vieja.

**Ten la presentación abierta de respaldo el día de la clase.** No por desconfianza del
sitio, sino porque si se cae el internet a media sesión, el sitio se cae contigo.
La PPTX está entre los descargables, a un clic.
