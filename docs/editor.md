---
title: Editor
---

# Editor de bitácora

<p class="meta">Armar · escribir · subir fotos y archivos · publicar en el repositorio</p>

!!! quote "Atribución · desarrollado con IA"
    Esta sección del sitio (el editor, el constructor por elementos, las [plantillas](plantillas/index.md) y los componentes para fotos) fue **desarrollada con Claude (Anthropic)** a pedido mío, siguiendo la [guía de documentación](metodo/documentar.md) de la EFDI: reconozco el trabajo generado por máquinas y documento cómo lo usé. La idea, los requisitos, las decisiones de estilo y las correcciones son mías; el código lo generó la IA en conversación y yo lo revisé probándolo en el sitio. Uso declarado con la etiqueta [CCL · Cognitive Contribution Label](https://santifu.github.io/ccl/).

??? note "Pedidos que le hice a la IA, resumidos"
    - «Pasá todo a una estética minimalista como la guía rápida de captura de datos, al estilo de fisicabit.com: blanco, negro y líneas».
    - «Mantené toda la configuración original del sitio; solo cambiá la estética».
    - «Quiero un apartado en la propia página para subir ítems nuevos con el formato que piden mis docentes, pero solo con mi cuenta».
    - «Dame plantillas lindas para cada sección, con carretes de fotos y antes/después, conservando el estilo».
    - «Mejorá el editor y hacelo más gráfico, como Word: que me deje generar elementos para la página».
    - «Quiero poner los archivos en Google Drive o poder subirlos a GitHub».

    No es la transcripción completa: la conversación incluyó pruebas, errores (por ejemplo, un rediseño que rompió el menú lateral y hubo que revertir) y ajustes sobre capturas de pantalla.

<a class="md-button md-button--primary" href="../editor-app/" target="_blank" rel="noopener">Abrir el editor ↗</a>
<a class="md-button" href="../plantillas/">Ver plantillas</a>

## Qué hace

- **Armar página**: elegís elementos (título, texto, imagen, carrete, galería, antes/después, ficha de datos, tabla, línea de tiempo, resultado, nota, video, código, archivos), los completás y la página se arma con vista previa en vivo. Hay plantillas por sección para empezar.
- **Markdown**: pegás o escribís Markdown, lo ves con el estilo del sitio y lo publicás. También abre cualquier página o archivo existente para editarlo.
- **Ubicación en el menú**: al publicar elegís la sección (existente, nueva o nivel principal) y la posición exacta: al principio, al final o después de una página concreta.
- **Publicar**: un solo commit con la página, las fotos, los archivos y el menú. GitHub Actions reconstruye el sitio en uno o dos minutos.

Solo publica quien conecta su cuenta de GitHub con un token personal (pestaña **Mi cuenta** del editor). Sin cuenta, el editor sirve igual para armar, previsualizar y descargar.

