# sader-egunero.net

Web de la campaña **Sader-Profersa Kanpora!**: el informe «¿Qué estamos respirando?» sobre la planta de residuos peligrosos de Sader y Profersa en Punta Zorroza (Bilbao), con sus datos y sus fuentes, el seguimiento de lo que han hecho las instituciones y el material de campaña para descargar.

- Web: <https://sader-egunero.net>
- Autoría: Sader Egunero

## Cómo está hecha

Es una web estática: HTML, CSS y JavaScript en un solo archivo, sin base de datos, sin compilación y sin dependencias. Los tipos de letra se sirven desde la propia web y no usa cookies. Las visitas se cuentan con GoatCounter, sin datos personales (`js/count.js`).

| Ruta | Qué contiene |
|---|---|
| `index.html` | La página: textos, estilos y datos |
| `material/` | Material de campaña para descargar (imágenes, vídeos, díptico, guía y pegatinas, en castellano y en euskera), sus miniaturas (`material/mini/`) y la página de descargas. La galería de la portada usa estas mismas piezas |
| `docs/` | Informe en PDF (castellano y euskera), díptico y guía de redes |
| `img/` | Figuras y fotografías del informe; `compartir.jpg` es la imagen que se ve al compartir el enlace |
| `kit/` | Cartel de la próxima movilización |
| `data/fuentes.json` | Las fuentes del informe en formato abierto (la misma lista que usa la página) |
| `fonts/` | Tipos de letra (Anton, Barlow y Barlow Condensed, licencia SIL OFL 1.1) |
| `404.html`, `robots.txt`, `sitemap.xml`, `favicon.*` | Archivos de servicio |
| `LICENSE` | Texto legal de la licencia CC BY-SA 4.0 |

## Verla en tu ordenador

Abre `index.html` en el navegador. Para probarla como se verá publicada:

```
python3 -m http.server 8000
```

y entra en <http://localhost:8000>.

## Cómo actualizarla

Todo lo que cambia a menudo está al principio del `<script>` de `index.html`, en el bloque `CONFIG`:

| Clave | Para qué sirve |
|---|---|
| `ribbon` | Aviso rojo de arriba (próxima cita) |
| `events` | Agenda de movilizaciones (`date` en formato `AAAA-MM-DD`). Las pasadas se atenúan solas |
| `whatsapp`, `instagram`, `email` | Canales de contacto |
| `flag`, `stickers` | Textos de la bandera y de las pegatinas |
| `siteUrl`, `materialUrl`, `docBase` | Direcciones de la web, de la página de material y de los documentos |

El contenido está en listas dentro del mismo archivo:

- `FUENTES`: las fuentes. Sus números coinciden con las notas del informe en PDF: no se renumeran sin rehacer el informe. `data/fuentes.json` debe llevar la misma lista.
- `CH`: los capítulos del informe. Las citas se escriben `{12}` o `{12,14}` y se convierten en enlaces a la fuente.
- `ACTORS`: lo que ha hecho y lo que no ha hecho cada institución.
- `TL`: la cronología.
- `QUESTIONS`: las doce preguntas.
- `STATS`, `FINDINGS`, `PROTECT`, `ACTS`: cifras, hallazgos, consejos y formas de participar.

## Criterios

- Cada dato lleva su fuente. Si no la tiene, no se publica.
- Se distinguen los hechos documentados de los indicios, de lo que no se sabe y de las preguntas sin respuesta.
- Los nombres de persona aparecen solo cuando ocupan o han ocupado un cargo público, societario o asociativo, y solo en relación con ese cargo.

¿Has visto un error? Escribe a <sader-egunero-info@ni.eus> y lo corregimos.

## Licencia

© 2026 Sader Egunero.

Salvo que se indique otra cosa, la web, el informe y el material de campaña se publican con licencia [Creative Commons Atribución-CompartirIgual 4.0 Internacional (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.es). Puedes copiarlos, difundirlos y adaptarlos si citas a **Sader Egunero** como autor y compartes el resultado con la misma licencia. El texto legal está en el archivo `LICENSE`.

La licencia no cubre los materiales de terceros:

- el estudio del IPE-CSIC sobre la deposición atmosférica en Bilbao;
- el cartel de la manifestación (`kit/cartel-1-diciembre.jpg`), que es de las organizaciones convocantes;
- los mapas, © OpenStreetMap contributors;
- los tipos de letra (SIL Open Font License 1.1; ver `fonts/LICENCIAS.txt`);
- `js/count.js`, de GoatCounter (licencia ISC).

## Créditos

- Mapas: © OpenStreetMap contributors.
- Tipos de letra: Anton, Barlow y Barlow Condensed (SIL Open Font License 1.1; ver `fonts/LICENCIAS.txt`).
