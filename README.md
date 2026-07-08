# El Falsete

> *Una confesión no es lo contrario de una mentira.*

**Pieza teatral noir en cuatro actos.** Un solo escenario —una sala de interrogatorios sin ventanas— y una sola noche. Dos intérpretes: la cantante **Avalon Davies** y un hombre que no enciende la grabadora. (Una tercera voz, la de un muerto, solo se oye, grabada.) Julian Vale, el manager que la inventó a los quince años, ha aparecido muerto. Pero esto no es la historia de un crimen: es un duelo entre dos personas que dominan el mismo oficio —hacer que las palabras signifiquen lo contrario de lo que dicen— jugando la partida de sus vidas.

Todo es diálogo. Todo es interrogatorio. Quien mira creerá tres veces haber descubierto al monstruo; las tres se equivocará. Y al bajar el telón, si vuelve a la primera escena, encontrará que la respuesta estuvo siempre delante.

Prólogo · 12 escenas · Epílogo.

---

## Cómo está organizado el libro

El texto vive en `content/`, separado por completo de su presentación:

```
content/
  book.json                 · metadatos, sinopsis, dramatis personae, puesta en escena
  01-la-sala/               · Acto I  — La Sala
    part.json
    00-prologo.md
    01-el-vaso-de-agua.md
    02-el-hombre-que-me-invento.md
    03-la-hermana-en-la-sombra.md
  02-el-falsete/            · Acto II — El Falsete
    ...
  03-el-nombre-equivocado/  · Acto III — El Nombre Equivocado
    ...
  04-lo-que-enterramos/     · Acto IV — Lo que Enterramos
    ...
    99-epilogo.md
```

Cada escena es un archivo Markdown con un pequeño encabezado (`title`, `epigraph`, `author`).
Los epígrafes no son adorno: son documentos —titulares, atestados, letras de canciones, mensajes de voz— que enmarcan cada escena y que, releídos al final, dicen más de lo que parecía.

Convenciones del texto (composición teatral):

- **Pie de personaje**: una línea que empieza por `NOMBRE.—` se compone con el nombre en versalitas y el parlamento a continuación. En escena solo hablan `AVALON.—` y `EL INTERROGADOR.—`; la voz grabada del muerto es `VOZ DE VALE.—`.
- **Acotaciones**: un párrafo entero entre paréntesis es una acotación (cursiva, sangrada). Entre paréntesis dentro de un parlamento, una acotación breve `(así)`.
- `*cursiva*` para lo que se canta o se subraya.
- Una línea con `***` marca un corte de escena; los actos y las escenas los da la estructura de carpetas.

## Cómo leerlo

El proyecto es un generador estático **sin dependencias**. Construye una web de lectura con dos modos —libro paginado y lectura continua—, tema día/noche y memoria de la posición.

```bash
node scripts/build.mjs      # genera /dist
npm run serve               # construye y sirve en local
```

Abre `dist/index.html` para la portada (sinopsis, dramatis personae, índice, puesta en escena)
o `dist/reader.html` para leer la obra en modo libro.

El sitio se publica solo en **GitHub Pages** con cada `push` (ver `.github/workflows/`).

## Una advertencia, que también es una invitación

Ninguno de los dos que hablan en este libro tiene el menor interés en que lo creamos por completo.
Léelo despacio. Vuelve atrás. La novela está construida para recompensar exactamente eso.

---

*Obra de ficción. Cualquier parecido entre estas voces y una voz viva —o entre esta confesión y la verdad— queda a cuenta del lector.*
