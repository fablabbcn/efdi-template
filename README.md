# Bitácora EFDI · Martín Ferreira

Sitio personal de la **Especialización en Fabricación Digital e Innovación (EFDI · UTEC & Fab Lab Barcelona)**.
Publicado en <https://martinfp642.github.io/martin_ferreira/>.

Está hecho con [MkDocs](https://www.mkdocs.org/) y [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/),
con una estética en blanco y negro (Montserrat, líneas de 2 px, sin sombras ni radios) tomada de
[fisicabit.com](https://fisicabit.com).

## Estructura

| Carpeta / archivo | Qué es |
| --- | --- |
| `docs/` | Las páginas en Markdown. Una carpeta por sección (`tecnicos`, `diseno`, `innovacion`, `proyecto`, `ref`). |
| `docs/images/` | Imágenes, organizadas por sección y entrada. |
| `docs/files/` | Archivos editables y exportaciones (`.scad`, `.stl`, `.ino`, …). |
| `docs/metodo/documentar.md` | Resumen de la guía de documentación y la estructura de cada entrada. |
| `docs/editor.md` + `docs/javascripts/bitacora-editor.js` | Editor en la propia página (ver abajo). |
| `docs/stylesheets/bitacora.css` | Todo el estilo. |
| `mkdocs.yml` | Configuración y menú (`nav`). |
| `.github/workflows/main.yml` | Cada push a `main` reconstruye el sitio y lo publica en `gh-pages`. |

## Editor en la página

La página **Editor** del sitio permite, desde el navegador y sin instalar nada:

- escribir una entrada nueva con la estructura de la guía (introducción, investigación, proceso, resultados, reflexión, archivos, atribución);
- cargar fotos, que se comprimen a 1600 px antes de subirse;
- publicar todo en **un solo commit** a `main`, incluyendo la línea nueva en el menú de `mkdocs.yml`;
- editar o borrar cualquier archivo de `docs/` y el propio `mkdocs.yml`.

Solo funciona con un **token personal fine-grained** de GitHub con permiso *Contents: Read and write* sobre este
repositorio. El token queda guardado únicamente en el navegador. Sin token, el editor igual genera el Markdown para
copiar o descargar. Las instrucciones completas están en la pestaña **Ayuda** del editor.

## Trabajar en local

```bash
pip install -r requirements.txt
mkdocs serve
```

Abrir <http://127.0.0.1:8000>. `mkdocs build` genera la carpeta `site/`, que no se sube al repositorio.

## Licencia

Contenido bajo GNU Free Documentation License. Plantilla original: [fablabbcn/efdi-template](https://github.com/fablabbcn/efdi-template).
