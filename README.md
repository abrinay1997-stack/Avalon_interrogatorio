# El Falsete

> *Una confesión no es lo contrario de una mentira.*

**Expediente sonoro · ficción noir para adultos.** Trece cintas recuperadas de un interrogatorio que nunca constó en ninguna parte. Una sola noche, un cuarto sin ventanas, dos voces —la cantante más famosa del mundo y un hombre que le jura que no hay ninguna grabadora encendida— y, entre las dos, el cadáver del hombre que inventó a **Avalon Davies**.

Todo es diálogo. Todo es interrogatorio. Todo está grabado, aunque uno de los dos no lo sepa. Quien escuche creerá tres veces haber descubierto al monstruo; las tres se equivocará. Y al llegar a la última cinta, si vuelve a la primera, encontrará que la respuesta estuvo siempre ahí, respirando.

Contiene abuso, adicción, muerte y coacción psicológica. **No apto para menores de dieciocho años.**

Prólogo · 12 cintas · Epílogo.

---

## Cómo está organizado

El texto vive en `content/`, separado por completo de su presentación:

```
content/
  book.json                 · metadatos, sinopsis, dramatis personae, advertencia
  01-la-sala/               · Cara A — La Sala
    part.json
    00-prologo.md
    01-el-vaso-de-agua.md
    02-el-hombre-que-me-invento.md
    03-la-hermana-en-la-sombra.md
  02-el-falsete/            · Cara B — El Falsete
    ...
  03-el-nombre-equivocado/  · Cara C — El Nombre Equivocado
    ...
  04-lo-que-enterramos/     · Cara D — Lo que Enterramos
    ...
    99-epilogo.md
```

Cada cinta es un archivo Markdown con un pequeño encabezado (`title`, `epigraph`, `author`).
Los epígrafes son documentos del caso —titulares, atestados, letras, mensajes de voz— que, releídos al final, dicen más de lo que parecía.

Convenciones del texto (transcripción de audio):

- **Carátula de cinta**: un bloque envuelto en `[[ ... ]]` se compone como cabecera forense monoespaciada (número de cinta, hora, notas del técnico).
- **Pie de voz**: una línea que empieza por `NOMBRE.—` lleva el nombre en versalitas. Solo se oyen `AVALON.—`, `EL INTERROGADOR.—` y, grabada, `VOZ DE VALE.—`.
- **Diseño de sonido**: un párrafo entero entre paréntesis es una acotación de audio (cursiva, sangrada). Dentro de un parlamento, `(así)`.
- **Anotaciones de cinta**: `[estática]`, `[11 s de silencio]`, `[inaudible]` se marcan entre corchetes.
- `*cursiva*` para lo que se canta.

## Cómo leerlo

Generador estático **sin dependencias**. Construye una web de lectura con dos modos —cinta paginada y lectura continua—, tema día/noche (léelo de noche) y memoria de posición.

```bash
node scripts/build.mjs      # genera /dist
npm run serve               # construye y sirve en local
```

`dist/index.html` es la portada (sinopsis, dramatis personae, índice de cintas, advertencia);
`dist/reader.html`, el lector. El sitio se publica en **GitHub Pages** con cada `push` (ver `.github/workflows/`).

## Una advertencia, que también es una invitación

Ninguna de las dos voces de estas cintas tiene el menor interés en que la creas del todo.
Escúchalas despacio. Vuelve atrás. Todo fue sembrado antes de pudrirse.

---

*Obra de ficción. Cualquier parecido entre estas voces y una voz viva —o entre esta confesión y la verdad— queda a cuenta de quien escucha.*
