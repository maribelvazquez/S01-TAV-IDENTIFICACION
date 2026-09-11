# Aula del Taller Antilavado 360 · sitio completo

**VERSIÓN v8 · 11 de septiembre de 2026.**

> Para saber si ya subiste esta versión: abre el sitio publicado, entra a la **sesión 2** y descarga el
> **Compendio**. Si su portada dice **«Segunda edición, 10 de septiembre de 2026»** y su segunda página
> se titula **«Qué cambió en esta edición»**, estás viendo la v6. (Señas de la v5, que la v6 conserva:
> la tarjeta de la sesión 5 dice «Martes 22 de septiembre · 16:00 a 19:00 — tres horas» y la sesión 2
> cita el artículo 17 de las Reglas en el bloque de medidas simplificadas.)

| Versión | Qué trae |
|---|---|
| v1 · 7 sep | Sesión 4 incorporada, tarjeta 4 encendida, Ley y Reglamento en la biblioteca. 43 láminas |
| v2 · 8 sep | Lámina 35 nueva: el control del fideicomiso con la LGTOC. 44 láminas |
| v3 · 8 sep | Evaluación Nacional de Riesgos 2023 en la biblioteca |
| v4 · 8 sep | Corregida la cita de los diez años en los descargables de la sesión 1 |
| v5 · 10 sep | Calendario nuevo (S5 al martes 22, tres horas; cierre el martes 29) y corrección de medidas simplificadas en la sesión 2 |
| v6 · 10 sep | Compendio de la sesión 2 reeditado por completo: segunda edición, 44 páginas, con siete correcciones de fondo |
| v7 · 10 sep | Las mismas correcciones aplicadas a las páginas de la sesión 2: el umbral inventado de 16,000 UMA en la ficha CATÁLOGO, el Anexo 10 como fuente de PEP, «quince fracciones», los indicadores bloqueados y el régimen de auditoría |
| **v8 · 11 sep** | **Última instancia del `RCG 37 Bis 2`: la página presentaba la restricción a las fracciones V, VIII y X como si fuera de la norma. El artículo no enlista fracciones — es criterio de la herramienta. Corregido en `s02/index.html` y en la ficha `A4`** |

Este paquete es el **sitio entero** —65 archivos—, no un parche. Reemplaza todo lo que hay hoy en el
repositorio. Se sube tal cual y no hay que copiar carpetas a mano ni pegar fragmentos en
ningún archivo.

---

## 1. Cómo se publica

1. Sustituya el contenido del repositorio por el de este paquete, **conservando la raíz**
   (`index.html`, `netlify.toml`, `_headers` y `robots.txt` van en el nivel superior).
2. Netlify reconstruye solo. No hay compilación ni proceso de build: son archivos estáticos.
3. Abra el sitio y compruebe tres cosas: que la **tarjeta 4** del índice ya es clicable, que
   desde la sesión 3 el botón de «sesión siguiente» lleva a la 4, y que las **cinco descargas
   de la sesión 4** abren.

Los archivos que cambiaron respecto de la versión anterior están listados en el apartado 4.

---

## 2. Qué contiene

```
index.html                 índice del aula · la tarjeta 4 ya está activa
biblioteca/                SEIS documentos transversales, ordenados por capa.
                           Se enlazan SOLO desde la portada (index.html,
                           bloque «Biblioteca del taller»). Las sesiones
                           traen un renglón que apunta ahí, no copias.
      LFPIORPI_texto_vigente_DOF_16_julio_2025.pdf   NUEVO · la Ley, 39 pp.
      Reglamento_LFPIORPI_texto_vigente_DOF_27_marzo_2026.pdf   NUEVO · 21 pp.
      ACUERDO_115_2026_DOF_07_agosto_2026.pdf   la publicación del Diario
      Oficial, 31 pp. Es la fuente con valor legal.
      Reglas_de_Caracter_General_texto_compilado.pdf   texto oficial compilado
      de las RCG con todas sus reformas, 53 pp. OJO: tiene seis erratas
      cotejadas contra el DOF; la de peso está en el art. 6.
      Preguntas_del_Sector_ACUERDO_115.pdf   177 preguntas, 6a edición, 130 pp.
      Para actualizar cualquiera se reemplaza el archivo con el mismo
      nombre: las ligas no cambian.

netlify.toml               sin cambios
_headers  robots.txt       sin cambios

s00/  index.html           la clase abierta del 11 de agosto
      autodiagnostico.html · guia/ · sanciones/ · juego/ · estilo.css

s01/  index.html           estilos embebidos · 3 descargables · 28 láminas

s02/  index.html           estilo.css · hojas/ (19 páginas)
      descargables/        5 archivos · matriz v9.1 · 34 láminas

s03/  index.html           diagnostico.html · estilo.css
      descargables/        5 archivos · 31 láminas

s04/  index.html           NUEVA
      estilo.css           copia idéntica de la de s03, comprobada por diff
      descargables/        5 archivos · 44 láminas
```

---

## 3. La navegación

Cada sesión tiene dos salidas, porque el aula va incrustada en Thinkific dentro de un marco
y el usuario no tiene la barra del navegador para regresar:

- **Arriba**, una barra delgada con «← Todas las sesiones» y el contador «Sesión N de 6».
- **Abajo**, antes del pie: sesión anterior, sesión siguiente y un botón «Volver al aula».

La sesión 4 muestra la 3 como anterior y **«LUNES 14 de septiembre» en gris** como siguiente,
para que se vea que el taller sigue y todavía no está publicada. El contador dice «Sesión 4
de 6» porque la del 11 de agosto es la de apertura y no cuenta dentro de las seis.

La navegación va **con estilos en línea**, sin tocar las hojas de estilo ni las clases
existentes, porque las sesiones tienen sistemas visuales distintos: la 1 lleva sus estilos
embebidos; la 0, la 2, la 3 y la 4 comparten `estilo.css`. Lo único común es la clase `.wrap`.

---

## 4. Qué cambió respecto de la versión anterior

### 4.1 · En la v8 (11 de septiembre) — el último resto del 37 Bis 2

Apareció al preparar la versión suelta de la sesión 2 para otro curso. Dos archivos:

| Archivo | Cambio |
|---|---|
| `s02/index.html` | Decía «**Sólo** las fracciones V, VIII y X admiten «No aplica»», con las citas del `RCG 37 Bis` y `37 Bis 2` debajo — lo que atribuye a la norma una restricción que es de la herramienta. El artículo **no enlista fracciones**: exenta cualquier supuesto de acto u operación que la entidad determine no realizar, con constancia en el Manual, y la exención cae cuando decida realizarlos. Reescrito, con la restricción declarada como criterio de diseño |
| `s02/hojas/a4.html` | La misma aclaración añadida al «Ojo» de la ficha, que es donde se usa el «No aplica» |

**Por qué se escapó al barrido de la v7:** los cinco patrones que se buscaron eran los del pliego
de auditoría del compendio. Éste decía lo mismo con otras palabras —«Sólo las fracciones»— y no
coincidía con ninguno. Buscar cadenas encuentra repeticiones; no encuentra paráfrasis. Para el
barrido de las sesiones 0, 1, 3 y 4 hay que leer los pasajes donde se cite el artículo, no
sólo buscar el texto de la primera versión.

### 4.2 · En la v7 (10 de septiembre) — las páginas de la sesión 2

La reedición del compendio (v6) corrigió el documento, pero **las páginas del sitio arrastraban
los mismos errores**. Este barrido los cierra. Seis archivos:

| Archivo | Cambio |
|---|---|
| `s02/hojas/catalogo.html` | **El umbral inventado.** Decía «Fracción V: umbral de identificación 8,025 UMA, umbral de aviso 16,000 UMA». Ahora dice identificación siempre, sin umbral, y Aviso de 8,025 UMA con su conversión a pesos. Además, «quince fracciones» → dieciséis más la V Bis, y la etiqueta de cita `L 17 Bis` —artículo que no existe— sustituida por `L 17, penúltimo párr.` |
| `s02/hojas/variables.html` | El dato de condición PEP ya no sale del Anexo 10, sino de la declaración del Cliente y de Consulta PEP 2.0 (`RCG 23 Quáter 1`) |
| `s02/hojas/parametros.html` | «las quince fracciones» → todas las fracciones del Art. 17 |
| `s02/hojas/mapa.html` | Lo mismo, en la tarjeta de CATÁLOGO |
| `s02/index.html` | Cinco correcciones: los indicadores bloqueados (**diez**, no ocho, con los dos de más declarados como criterio de la herramienta); el régimen de auditoría, que ahora incluye la vía externa electiva del `RCG 45`; las medidas simplificadas en la tabla de consecuencias, que citaban sólo el `R 15`; el renglón BAJO de la tabla de grados, que omitía el `RCG 17`; y la fuente del dato de PEP |
| `LEEME_SITIO_COMPLETO.md` | Este archivo |

### 4.3 · En la v6 (10 de septiembre) — un solo archivo

| Archivo | Cambio |
|---|---|
| `s02/descargables/S02_ALU_06_Compendio_Sesion_02.pdf` | **Reeditado completo.** Segunda edición, 44 páginas. Se auditaron las 59 páginas de la primera y se corrigieron **cuatro errores que rompían el ejercicio** —los umbrales de la fracción V (la primera edición inventaba un umbral de aviso de 16,000 UMA; la fracción V no tiene umbral de identificación y su umbral de Aviso es de 8,025 UMA), las medidas simplificadas incompletas (son **dos** condiciones acumulativas, y el `RCG 17` no aparecía citado ni una vez en todo el documento), la fórmula de agregación por elemento y por entidad, y el conteo de indicadores bloqueados— **más nueve correcciones de conducta**, entre ellas la multa por Aviso omitido (estaba subestimada cincuenta veces), el `RCG 37 Bis 2` (no enlista fracciones), el Anexo 10 (no es fuente del dato de PEP: es la información que las autoridades entregan a la UIF conforme al `L 51 Ter`) y las dieciséis fracciones del artículo 17 más la V Bis. Trae al frente una sección **«Qué cambió en esta edición»** y un **Anexo II** de fundamentos que ahora sí incluye el `RCG 44`, el `RCG 45` y el `RCG 48` |
| `s02/index.html` | La descripción de la tarjeta del compendio, con las señas de la segunda edición |
| `LEEME_SITIO_COMPLETO.md` | Este archivo |

Nada más cambió respecto de la v5. **Si ya subiste la v5, puedes subir sólo esos tres archivos**; el
zip completo se entrega igual, para que no haya que decidir.

### 4.4 · Historia previa

| Archivo | Cambio |
|---|---|
| `index.html` | La tarjeta de la sesión 4 pasa de `.soon` a **liga activa**, con su descripción |
| `s03/index.html` | El bloque «sesión siguiente», que estaba en gris, ahora **enlaza a `../s04/`** |
| `s03/index.html` | La nota de la biblioteca salió del bloque `.dl`: estaba dentro de la rejilla de descargas y su liga heredaba el estilo de tarjeta, así que «biblioteca del aula» se dibujaba como una caja grande a media frase. Es sólo un `</div>` movido; no cambia ni una palabra del texto |
| `s04/` | **Carpeta nueva completa**: página de la sesión, hoja de estilo y cinco descargables |
| `biblioteca/` | **Dos documentos nuevos**: la Ley y el Reglamento, en su texto vigente. Faltaban, y el pie de todas las páginas ya los citaba |
| `index.html` | El bloque «Biblioteca del taller» reescrito: pasa de tres a cinco documentos, **ordenados por capa** —Ley, Reglamento, Reglas—, y cada tarjeta lleva la etiqueta de cita del taller (`L`, `R`, `RCG`) en lugar de la etiqueta genérica «PDF». La biblioteca ahora enseña la nomenclatura de un vistazo |

Nada más se tocó. Las sesiones 0, 1 y 2 van tal como estaban, y los tres PDF que ya vivían en `biblioteca/` no se reemplazaron.

---

## 5. Sesión 4 · las cinco descargas

| Archivo | Qué es |
|---|---|
| `S04_ALU_02_Protocolo_Aviso_24_horas.docx` | **Plantilla 04 del kit.** 9 páginas, 14 apartados. Los dos avisos, el arranque del plazo, el diferimiento del envío, roles con plazos internos, el procedimiento en seis pasos, cláusulas modelo para el Manual y ficha de registro imprimible |
| `S04_ALU_04_Checklist_Beneficiario_Controlador.xlsx` | **Plantilla 05 del kit.** 6 hojas. La prelación de tres niveles con la columna que dice sola en qué nivel cerró, la cadena de control con un ejemplo de dos niveles resuelto, las dos excepciones con su alcance, y qué datos por tipo de cliente. **Se usa en el taller del minuto 84** |
| `S04_ALU_03_Perfil_Alertas_y_Bitacoras.xlsx` | Anexo de la Plantilla 04. 5 hojas: perfil transaccional con la reevaluación a seis meses calculada, bitácora de alertas y bitácora de intentos. **Se usa en el ejercicio del minuto 20** |
| `S04_ALU_05_Efectivo_y_Avisos.xlsx` | Anexo de la sesión. 4 hojas: la calculadora de las tres bases del `R 6`, los 28 supuestos del artículo 17 con sus umbrales y topes, y la fecha del acto por fracción del `RCG 24 Bis` |
| `S04_ALU_01_Presentacion.pptx` | Las 44 láminas de la sesión |

Los tres libros de Excel y el documento de Word separan, en su propia hoja o apartado, **lo
que la norma exige de lo que es método del taller**. El formato de las bitácoras, los cuatro
pasos del ciclo de la alerta y los seis campos del protocolo están declarados como método,
no como precepto.

---

## 6. Un renglón que puede caducar de un día para otro

En la sesión 4, el bloque **«La fecha que todavía no existe»** dice que el envío del Aviso
de veinticuatro horas está diferido: el `R Trans. Quinto` lo sujeta a que se actualicen los
Anexos de la Resolución de formatos, y el `RCG Trans. Quinto` añade seis meses desde que esa
Resolución entre en vigor.

**Si esa Resolución se publica en el Diario Oficial, ese bloque deja de ser cierto** y hay
que sustituirlo por la fecha de entrada en vigor más seis meses. Es el único contenido del
sitio con esa fragilidad, y por eso el aviso legal del pie de la sesión 4 pide expresamente
verificar el Diario Oficial antes de aplicar ese apartado.

---

## 7. Verificación corrida sobre este paquete

- **56 ligas** de las seis páginas principales probadas con petición real: **ninguna rota**.
- **Sin desbordamiento horizontal** a 1440 px ni a 390 px en el índice, en la sesión 3 y en
  la sesión 4. Comprobado con navegador, midiendo el ancho de desplazamiento del documento.
- **Sin errores de JavaScript** en consola en ninguna de las tres.
- `s03/estilo.css` y `s04/estilo.css` **idénticos**, comprobado por `diff`.
- Las diez anclas de la barra de bloques de la sesión 4 corresponden a sus diez secciones.
- Los cinco descargables verificados por **SHA-256** contra los originales.
- Capturas de la sesión 4 a 1440 px y a 390 px, revisadas una por una.
- Las cifras que aparecen escritas en la página se contaron del archivo: **44 láminas** del
  pptx, **5 y 6 y 4 hojas** de los libros de Excel, **9 páginas** del Word.
