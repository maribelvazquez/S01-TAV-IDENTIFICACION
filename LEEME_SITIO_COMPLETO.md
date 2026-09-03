# Aula del Taller Antilavado 360 · sitio completo

**Versión del 31 de agosto de 2026, con la Sesión 3 incorporada y la navegación arreglada.**

Este paquete es el **sitio entero**, no un parche. Reemplaza todo lo que hay hoy en el
repositorio de Netlify. Se sube tal cual y no hay que copiar carpetas a mano ni pegar
fragmentos en ningún archivo.

---

## 1. Cómo se publica

1. Sustituya el contenido del repositorio por el de este paquete, **conservando la raíz**
   (`index.html`, `netlify.toml`, `_headers` y `robots.txt` van en el nivel superior).
2. Netlify reconstruye solo. No hay compilación, ni gestor de paquetes, ni proceso de build:
   son archivos estáticos.
3. Abra el sitio y compruebe tres cosas: que la tarjeta 3 del índice ya es clicable, que
   desde cualquier sesión hay una liga de regreso arriba y abajo, y que las cinco descargas
   de la sesión 3 abren.

Si prefiere no reemplazar todo, los archivos que cambiaron respecto de la versión anterior
están listados en el apartado 4.

---

## 2. Qué contiene

```
index.html                 índice del aula · la tarjeta 3 ya está activa
biblioteca/                NUEVA · documento transversal del taller
      Preguntas_del_Sector_ACUERDO_115.pdf   145 preguntas, 3a edicion, 89 pp.
      Reglas_de_Caracter_General_texto_compilado.pdf   texto oficial compilado
      de las RCG con todas sus reformas, 53 pp. OJO: tiene seis erratas
      cotejadas contra el DOF; la de peso esta en el art. 6.
      ACUERDO_115_2026_DOF_07_agosto_2026.pdf   la publicacion del Diario
      Oficial, 31 pp. Es la fuente con valor legal.
      Se enlaza desde las tres sesiones. Para actualizarlo se reemplaza el
      archivo con el mismo nombre: las ligas no cambian.

netlify.toml               sin cambios
_headers  robots.txt       sin cambios

s01/  index.html           + navegación
      3 descargables

s02/  index.html           + navegación · dos correcciones de contenido
                           + siete correcciones de la matriz v9.0
      estilo.css           + regla de tablas en teléfono
      descargables/        5 archivos · los 4 anteriores sustituidos (matriz v9.1)
                           + S02_ALU_06_Compendio_Sesion_02.pdf, NUEVO
      hojas/               19 páginas · bcliente.html sustituida, 18 sin cambios

s03/  index.html           NUEVA
      diagnostico.html     NUEVA · el calificador del Manual, con el que abre la sesión
      estilo.css           copia idéntica de la de s02, con la misma regla añadida
      descargables/        5 archivos
```

---

## 3. La navegación, que era el problema

Antes, las páginas de sesión eran **callejón sin salida**: se entraba desde el índice y no
había forma de volver. El aula va incrustada en Thinkific dentro de un marco, así que el
usuario tampoco tiene la barra del navegador para regresar. Quedaba atrapado.

Ahora cada sesión tiene dos salidas:

- **Arriba**, una barra delgada con «← Todas las sesiones» y el contador «Sesión N de 6».
- **Abajo**, antes del pie: sesión anterior, sesión siguiente, y un botón «Volver al aula».

La sesión 1 muestra «No hay anterior» y la 3 muestra «Martes 8 de septiembre» en gris,
para que se vea que el taller sigue y todavía no está publicada.

La navegación se escribió **con estilos en línea**, sin tocar las hojas de estilo ni las
clases existentes. Las tres sesiones tienen sistemas visuales distintos —la 1 lleva sus
estilos embebidos y pestañas con JavaScript; la 2 y la 3 comparten `estilo.css`— y así
ninguna se altera. Lo único que las tres comparten es la clase `.wrap`, que es de la que
se cuelga la barra para que quede alineada con el resto de la página.

Las 19 hojas de la matriz de la sesión 2 ya tenían su propia navegación —anterior, siguiente
y «volver al mapa»—, y el mapa regresa a la sesión 2. Con el arreglo de arriba, esa cadena
ya llega hasta el índice del aula.

---

## 4. Qué cambió respecto de la versión anterior

| Archivo | Cambio |
|---|---|
| `index.html` | La tarjeta de la sesión 3 pasa de `.soon` a liga activa, con su descripción |
| `s01/index.html` | Barra de regreso arriba · salto de sesión abajo |
| `s02/index.html` | Barra de regreso · salto de sesión · **dos correcciones de contenido** · **siete correcciones de la matriz v9.0** |
| `s02/estilo.css` | Regla de tablas para pantallas de menos de 600 px |
| `s02/descargables/` | **Los cuatro archivos sustituidos**: matriz v9.1 con ejemplo y en blanco, guía regenerada, presentación de 34 láminas · **+ compendio de 59 páginas, nuevo** |
| `s02/hojas/bcliente.html` | **Sustituida**: 23 → 22 factores y la calificación del ejemplo 2.91 → 2.79 |
| `s03/` | Carpeta nueva completa, incluido `diagnostico.html` |

### Las correcciones de la matriz, v9.0

El modelo de cliente pasó de 23 a 22 factores: se fusionaron «Frecuencia» y «Volumen»
en uno solo, con fundamento en el **RCG 23 Ter 1 fr. II**, que los nombra juntos. El
indicador «Tipo de persona y estructura» se limpió a «Tipo de persona», porque la
complejidad de la estructura ya la mide el factor de Beneficiario Controlador y tenerla
en los dos era doble conteo. El ejemplo cargado bajó de 2.91 a **2.79 · MEDIO**. La
evaluación de la entidad no cambió: 9.51 inherente · 78.2 % de mitigantes · 5.79 residual.
Los archivos en blanco ya no emiten calificación con datos vacíos: dicen SIN CLASIFICAR
y SIN EVALUAR hasta que estén resueltos los veintidós factores.

En `s02/index.html` eso obligó a estas correcciones de texto: «Catorce factores» → 22
(era el error de dato más visible de la página), «Los 23 factores» → 22, «Tipo de persona
y estructura» → «Tipo de persona», «treinta y dos láminas» → treinta y cuatro,
«en tres archivos» → en cuatro, y las dos tarjetas de descargables reescritas.

**El renglón de frecuencia y volumen.** El `RCG 23 Bis 2 fr. II` los enumera por separado
—«tipo, volumen en número, frecuencia y monto de actos u operaciones, número de
contrapartes…»—. El que los nombra juntos es el `23 Ter 1 fr. II`, que gobierna el **Perfil
transaccional**: otro instrumento, otro capítulo, y no sirve de fundamento aquí. La fusión
en un solo factor sigue siendo válida, pero por otra razón: el artículo dice «pudiendo
incluir… entre otros», o sea lista abierta. Es **criterio propio documentado**, no algo que
la norma nombre junto, y así lo dice ahora la página y la celda «Fuente del dato» del Excel.

**Lo que muestran las dos tarjetas** son los 22 factores de la matriz agrupados en siete
renglones cada una —diez inherentes y doce transaccionales—, no la enumeración del
artículo: la fracción I no menciona PEP, ni listas de personas bloqueadas, ni Beneficiario
Controlador. El encabezado y los conteos por familia ya lo dicen, para que 10 + 12 = 22 se
vea en la página.

### Las dos correcciones de la sesión 2

1. **La banda de cierre anunciaba el tema equivocado de la sesión 3.** Decía «Avisos,
   umbrales y acumulación», que es el tema de la sesión 4. Ahora dice el correcto.
2. **La sección «Para la próxima» listaba tres tareas que nunca se dejaron.** La grabación
   del 25 de agosto lo confirma: el cierre fue «bájenla, píquenle, úsenla, rómpanla».
   Se reencuadró como **«Lo que puedes ir adelantando»**, con una línea que aclara que no
   es tarea, y el tercer punto se cambió por la hoja «Controles», que es de donde arranca
   la sesión 3.

---

## 5. Sesión 3 · las cinco descargas

| Archivo | Qué es |
|---|---|
| `S03_ALU_02_Manual_Politicas_Internas.docx` | Plantilla 03 del kit. 23 apartados, 33 páginas |
| `S03_ALU_05_Guia_Redaccion_Manual.docx` | **Nueva.** Cómo se escribe un Manual: los cuatro escalones, el mapa de las catorce fracciones, dos apartados desarrollados como modelo. Se usa en el ejercicio del minuto 36 |
| `S03_ALU_04_Programa_Capacitacion.xlsx` | 8 hojas con fórmulas vivas. Se usa en el taller del minuto 97 |
| `S03_ALU_03_Aprobacion_PEP_Riesgo_Alto.docx` | Formato del artículo 23 Ter 5, en sus dos variantes |
| `S03_ALU_01_Presentacion.pptx` | Las 31 láminas de la sesión |

---

## 6. Verificación corrida sobre este paquete

- **13 rutas de navegación probadas con clic real**, todas funcionan: del índice a cada
  sesión, de cada sesión al índice por arriba y por abajo, los saltos entre sesiones, y la
  cadena hoja → mapa → sesión 2.
- **Sin desbordamiento horizontal en teléfono.** Antes, la sesión 2 se desplazaba 75 px de
  lado en pantallas de 390 px por culpa de una tabla; la sesión 3, 34 px. Las dos quedaron
  en cero.
- `s02/estilo.css` y `s03/estilo.css` **idénticos**, comprobado por `diff`.
- Todas las clases usadas en `s03/index.html` existen en su hoja de estilo. Ninguna huérfana.
- Las diez anclas de la barra de bloques de la sesión 3 corresponden a sus diez secciones.
- Los cinco descargables verificados por SHA-256 contra los originales.
- Capturas de las cuatro páginas a 1440 px y a 390 px, revisadas una por una.
