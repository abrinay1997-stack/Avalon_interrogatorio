# El Falsete

> *Una confesión no es lo contrario de una mentira.*

Novela negra psicológica. Un solo escenario —una sala de interrogatorios sin ventanas— y una sola noche. Frente a frente, la cantante **Avalon Davies** y un hombre que no enciende la grabadora. Julian Vale, el manager que la inventó a los quince años, ha aparecido muerto. Pero esta no es la historia de un crimen: es la de dos personas que dominan el mismo oficio —hacer que las palabras signifiquen lo contrario de lo que dicen— jugando la partida de sus vidas.

El lector creerá tres veces haber descubierto al monstruo. Las tres se equivocará. Y al terminar, si vuelve a la primera página, encontrará que la respuesta estuvo siempre delante.

Prólogo · 12 capítulos · Epílogo.

---

## Cómo está organizado el libro

El texto vive en `content/`, separado por completo de su presentación:

```
content/
  book.json                 · metadatos, sinopsis, dramatis personae, nota del autor
  01-la-sala/               · Parte I  — La Sala
    part.json
    00-prologo.md
    01-el-vaso-de-agua.md
    02-el-hombre-que-me-invento.md
    03-la-hermana-en-la-sombra.md
  02-el-falsete/            · Parte II — El Falsete
    ...
  03-el-nombre-equivocado/  · Parte III — El Nombre Equivocado
    ...
  04-lo-que-enterramos/     · Parte IV — Lo que Enterramos
    ...
    99-epilogo.md
```

Cada capítulo es un archivo Markdown con un pequeño encabezado (`title`, `epigraph`, `author`).
Los epígrafes no son adorno: son documentos —titulares, atestados, letras de canciones, mensajes— que enmarcan cada capítulo y que, releídos al final, dicen más de lo que parecía.

Convenciones del texto:

- Un párrafo por bloque, separados por una línea en blanco.
- `*cursiva*` para el énfasis y la voz interior.
- Una línea con `***` marca un corte de escena.

## Cómo leerlo

El proyecto es un generador estático **sin dependencias**. Construye una web de lectura con dos modos —libro paginado y lectura continua—, tema día/noche y memoria de la posición.

```bash
node scripts/build.mjs      # genera /dist
npm run serve               # construye y sirve en local
```

Abre `dist/index.html` para la portada (sinopsis, personajes, índice, nota del autor)
o `dist/reader.html` para leer como un libro.

El sitio se publica solo en **GitHub Pages** con cada `push` (ver `.github/workflows/`).

## Una advertencia, que también es una invitación

Ninguno de los dos que hablan en este libro tiene el menor interés en que lo creamos por completo.
Léelo despacio. Vuelve atrás. La novela está construida para recompensar exactamente eso.

---

*Obra de ficción. Cualquier parecido entre estas voces y una voz viva —o entre esta confesión y la verdad— queda a cuenta del lector.*
