---
title: Editor
---

# Editor de bitácora

<p class="meta">Escribir · subir imágenes · publicar en el repositorio</p>

!!! note "Plantillas"
    Para una entrada con carrete, galería, comparación y ficha de datos, copiá la plantilla de tu sección desde [Plantillas](plantillas/index.md) en la pestaña **Editar archivo**.

<div id="bitacora-editor" class="be" data-owner="martinfp642" data-repo="martin_ferreira" data-branch="main" data-site="https://martinfp642.github.io/martin_ferreira/">

<div class="be-toolbar">
  <button type="button" data-panel="nueva" aria-pressed="true">Nueva entrada</button>
  <button type="button" data-panel="editar">Editar archivo</button>
  <button type="button" data-panel="cuenta">Mi cuenta</button>
  <button type="button" data-panel="ayuda">Ayuda</button>
  <span class="be-status" id="be-status">Sin conexión</span>
</div>

<!-- ============================ NUEVA ENTRADA ============================ -->
<section class="be-panel active" data-panel="nueva">

<div class="be-row">
  <div class="be-field">
    <label for="be-titulo">Título</label>
    <input type="text" id="be-titulo" placeholder="Ej.: Primer corte láser">
  </div>
  <div class="be-field">
    <label for="be-seccion">Sección <small>Dónde aparece en el menú</small></label>
    <select id="be-seccion"></select>
    <input type="text" id="be-seccion-nueva" placeholder="Nombre de la sección nueva" style="display:none;margin-top:.4rem">
  </div>
</div>

<div class="be-row">
  <div class="be-field">
    <label for="be-fecha">Fecha</label>
    <input type="date" id="be-fecha">
  </div>
  <div class="be-field">
    <label for="be-semana">Semana o bloque <small>Ej.: Semana 3 · MT02</small></label>
    <input type="text" id="be-semana" placeholder="Semana 3">
  </div>
  <div class="be-field">
    <label for="be-slug">Nombre del archivo <small>Se genera solo desde el título</small></label>
    <input type="text" id="be-slug" placeholder="primer-corte-laser">
    <span class="hint be-kv" id="be-ruta"></span>
  </div>
</div>

<div class="be-section">
  <h3><span class="be-num">1</span>Introducción</h3>
  <div class="be-field">
    <label for="be-intro">Objetivo de la semana <small>Qué quería lograr y por qué.</small></label>
    <textarea id="be-intro"></textarea>
  </div>
</div>

<div class="be-section">
  <h3><span class="be-num">2</span>Investigación y referencias</h3>
  <div class="be-field">
    <label for="be-investigacion">Fuentes, enlaces, inspiración <small>Si usé IA, lo digo y pego los prompts.</small></label>
    <textarea id="be-investigacion"></textarea>
  </div>
</div>

<div class="be-section">
  <h3><span class="be-num">3</span>Proceso paso a paso</h3>
  <div class="be-field">
    <label for="be-proceso">Qué hice, con qué herramientas y materiales <small>Una línea por paso. Las imágenes se insertan donde esté el cursor con el botón de cada foto.</small></label>
    <div class="be-tb be-tb-mini" id="be-tb-proceso">
      <div class="be-tb-group">
        <button type="button" data-fmt="bold" title="Negrita"><b>B</b></button>
        <button type="button" data-fmt="h3" title="Subtítulo">H3</button>
        <button type="button" data-fmt="ul" title="Lista">• Lista</button>
        <button type="button" data-fmt="link" title="Enlace">Enlace</button>
        <button type="button" data-block="carrete">Carrete</button>
        <button type="button" data-block="galeria">Galería</button>
        <button type="button" data-block="comparar">Comparar</button>
        <button type="button" data-block="datos">Datos</button>
        <button type="button" data-block="video">Video</button>
      </div>
    </div>
    <textarea id="be-proceso" style="min-height:11rem"></textarea>
  </div>
  <div class="be-field">
    <label>Imágenes <small>Se comprimen en el navegador (máx. 1600 px) antes de subirlas al repositorio.</small></label>
    <div class="be-drop" id="be-drop">Arrastrá fotos o capturas acá, o hacé clic para elegirlas</div>
    <input type="file" id="be-files" accept="image/*" multiple style="display:none">
    <div class="be-images" id="be-images"></div>
    <div class="be-actions" style="margin:.6rem 0 0">
      <button type="button" class="small" id="be-ins-carrete">Insertar carrete con todas</button>
      <button type="button" class="small" id="be-ins-galeria">Insertar galería con todas</button>
    </div>
    <label class="be-check"><input type="checkbox" id="be-carrete" checked> Las fotos que no inserte en el texto van juntas en un carrete al final del proceso</label>
  </div>
</div>

<div class="be-section">
  <h3><span class="be-num">4</span>Resultados</h3>
  <div class="be-split two">
    <div class="be-field">
      <label for="be-ok">Lo que funcionó</label>
      <textarea id="be-ok"></textarea>
    </div>
    <div class="be-field">
      <label for="be-fail">Lo que falló <small>Fracaso ≠ error. Acá es donde más aprendo.</small></label>
      <textarea id="be-fail"></textarea>
    </div>
  </div>
</div>

<div class="be-section">
  <h3><span class="be-num">5</span>Reflexión</h3>
  <div class="be-field">
    <label for="be-reflexion">Qué aprendí, qué mejoraría</label>
    <textarea id="be-reflexion"></textarea>
  </div>
</div>

<div class="be-section">
  <h3><span class="be-num">6</span>Archivos</h3>
  <div class="be-field">
    <label for="be-archivos">Enlaces a los archivos del repositorio <small>Formato editable original + exportación abierta. Más de 10 MB: consultar antes.</small></label>
    <textarea id="be-archivos" placeholder="- [polea.scad](../files/polea.scad)&#10;- [polea.stl](../files/polea.stl)"></textarea>
  </div>
</div>

<div class="be-section">
  <h3><span class="be-num">7</span>Atribución y uso de IA</h3>
  <div class="be-field">
    <label for="be-ia">A quién le debo qué <small>Colegas, recursos, licencias. Si hubo IA: para qué la usé y la etiqueta <a href="https://santifu.github.io/ccl/" target="_blank" rel="noopener">CCL</a>.</small></label>
    <textarea id="be-ia"></textarea>
  </div>
</div>

<div class="be-actions">
  <button type="button" class="primary" id="be-publicar">Publicar en el sitio</button>
  <button type="button" id="be-previsualizar">Vista previa</button>
  <button type="button" id="be-copiar">Copiar Markdown</button>
  <button type="button" id="be-descargar">Descargar .md</button>
  <button type="button" id="be-limpiar">Limpiar formulario</button>
</div>

<div class="be-log" id="be-log">El borrador se guarda solo en este navegador mientras escribís.</div>
<div class="be-preview md-typeset" id="be-preview" style="display:none"></div>

</section>

<!-- ============================ EDITAR ARCHIVO ============================ -->
<section class="be-panel" data-panel="editar">

<div class="be-filebar">
  <div class="be-field grow">
    <label for="be-archivo">Página <small>Páginas en <code>docs/</code>, estilos, scripts y <code>mkdocs.yml</code> (el menú).</small></label>
    <select id="be-archivo"><option value="">Conectate o elegí una página…</option></select>
  </div>
  <div class="be-filebar-actions">
    <button type="button" class="small" id="be-nueva-pagina">+ Página nueva</button>
    <button type="button" class="small" id="be-recargar">Actualizar lista</button>
    <a id="be-ver" class="md-button" href="#" target="_blank" rel="noopener" style="display:none">Ver en el sitio</a>
  </div>
</div>

<div class="be-np" id="be-np" style="display:none">
  <div class="be-row">
    <div class="be-field">
      <label for="be-np-seccion">Sección</label>
      <select id="be-np-seccion"></select>
    </div>
    <div class="be-field">
      <label for="be-np-plantilla">Plantilla</label>
      <select id="be-np-plantilla">
        <option value="tecnologia">Tecnología y Fabricación</option>
        <option value="diseno">Diseño</option>
        <option value="innovacion">Innovación</option>
        <option value="proyecto">Proyecto Integrador</option>
        <option value="referencia">Referencias</option>
        <option value="">Vacía</option>
      </select>
    </div>
    <div class="be-field">
      <label for="be-np-titulo">Título</label>
      <input type="text" id="be-np-titulo" placeholder="Ej.: MT02 · Corte láser">
      <span class="hint be-kv" id="be-np-ruta"></span>
    </div>
  </div>
  <div class="be-actions" style="margin:0 0 .5rem">
    <button type="button" class="primary small" id="be-np-crear">Crear y abrir en el editor</button>
    <button type="button" class="small" id="be-np-cancelar">Cancelar</button>
  </div>
</div>

<div class="be-tb" id="be-tb">
  <div class="be-tb-group" data-help="Formato">
    <button type="button" data-fmt="bold" title="Negrita (Ctrl+B)"><b>B</b></button>
    <button type="button" data-fmt="italic" title="Cursiva (Ctrl+I)"><i>I</i></button>
    <button type="button" data-fmt="h2" title="Título de sección">H2</button>
    <button type="button" data-fmt="h3" title="Subtítulo">H3</button>
    <button type="button" data-fmt="ul" title="Lista">• Lista</button>
    <button type="button" data-fmt="ol" title="Lista numerada">1. Lista</button>
    <button type="button" data-fmt="link" title="Enlace (Ctrl+K)">Enlace</button>
    <button type="button" data-fmt="code" title="Código">&lt;/&gt;</button>
    <button type="button" data-fmt="quote" title="Cita">“ Cita</button>
    <button type="button" data-fmt="table" title="Tabla">Tabla</button>
  </div>
  <div class="be-tb-group" data-help="Bloques">
    <button type="button" data-block="carrete" title="Carrusel de fotos">Carrete</button>
    <button type="button" data-block="galeria" title="Grilla de fotos">Galería</button>
    <button type="button" data-block="comparar" title="Antes / después">Comparar</button>
    <button type="button" data-block="hero" title="Foto grande del resultado">Hero shot</button>
    <button type="button" data-block="datos" title="Ficha de datos">Datos</button>
    <button type="button" data-block="linea" title="Línea de tiempo">Línea</button>
    <button type="button" data-block="video" title="Video de YouTube o Vimeo">Video</button>
    <button type="button" data-block="ok" title="Etiqueta de éxito">Éxito</button>
    <button type="button" data-block="fail" title="Etiqueta de fallo">Falló</button>
    <button type="button" data-block="nota" title="Recuadro de nota">Nota</button>
  </div>
  <div class="be-tb-group be-tb-right" data-help="Vista">
    <button type="button" data-view="editar">Texto</button>
    <button type="button" data-view="dividido" aria-pressed="true">Dividido</button>
    <button type="button" data-view="previa">Vista previa</button>
    <button type="button" id="be-full" title="Pantalla completa">⤢</button>
  </div>
</div>

<div class="be-work" id="be-work" data-view="dividido">
  <div class="be-col be-col-texto">
    <textarea id="be-contenido" class="code" spellcheck="false" placeholder="Elegí una página arriba o creá una nueva."></textarea>
  </div>
  <div class="be-col be-col-previa">
    <div class="be-preview md-typeset" id="be-preview2"><p class="be-kv">La vista previa aparece acá mientras escribís.</p></div>
  </div>
</div>

<div class="be-field">
  <label>Imágenes para esta página <small>Se suben junto con el archivo al guardar; el enlace se inserta donde esté el cursor.</small></label>
  <div class="be-drop" id="be-drop2">Arrastrá imágenes acá, o hacé clic para elegirlas</div>
  <input type="file" id="be-files2" accept="image/*" multiple style="display:none">
  <div class="be-images" id="be-images2"></div>
  <div class="be-actions" style="margin:.6rem 0 0">
    <button type="button" class="small" id="be-ins-carrete2">Insertar carrete con todas</button>
    <button type="button" class="small" id="be-ins-galeria2">Insertar galería con todas</button>
  </div>
</div>

<div class="be-field">
  <label for="be-mensaje">Mensaje del commit <small>Qué cambiaste, en una línea.</small></label>
  <input type="text" id="be-mensaje" placeholder="Corrijo rutas de imágenes en MT01">
</div>

<div class="be-actions">
  <button type="button" class="primary" id="be-guardar">Guardar en el repositorio <small>Ctrl+S</small></button>
  <button type="button" id="be-borrar">Borrar archivo</button>
  <span class="be-dirty" id="be-dirty"></span>
</div>

<div class="be-log" id="be-log2">Elegí una página.</div>

</section>

<!-- ============================ MI CUENTA ============================ -->
<section class="be-panel" data-panel="cuenta">

<p>La página es pública, pero <strong>solo quien tenga un token de mi cuenta de GitHub puede publicar</strong>. El token se guarda únicamente en este navegador y viaja directo a la API de GitHub: no pasa por ningún otro servidor.</p>

<div class="be-field">
  <label for="be-token">Token personal de GitHub <small>Fine-grained, con permiso <em>Contents: Read and write</em> solo sobre este repositorio. Ver Ayuda.</small></label>
  <input type="password" id="be-token" placeholder="github_pat_…" autocomplete="off">
</div>

<label class="be-check"><input type="checkbox" id="be-recordar" checked> Recordar en este navegador (no lo marques en una computadora compartida)</label>

<div class="be-actions">
  <button type="button" class="primary" id="be-conectar">Conectar</button>
  <button type="button" id="be-olvidar">Olvidar token</button>
</div>

<div class="be-log" id="be-log3">Sin token guardado.</div>

</section>

<!-- ============================ AYUDA ============================ -->
<section class="be-panel" data-panel="ayuda">

<h3>Crear el token (una sola vez)</h3>
<ol class="pasos">
  <li>En GitHub: <strong>Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token</strong>.</li>
  <li><strong>Repository access</strong>: <em>Only select repositories</em> → elegí <code>martin_ferreira</code>.</li>
  <li><strong>Permissions → Repository permissions → Contents</strong>: <em>Read and write</em>. <em>Metadata</em> queda en <em>Read</em> solo.</li>
  <li>Elegí un vencimiento (por ejemplo, 90 días), generá el token y pegalo en <strong>Mi cuenta</strong>.</li>
</ol>

<h3>Qué pasa al publicar</h3>
<ol class="pasos">
  <li>El editor arma el Markdown con la estructura de la guía (Introducción, Investigación, Proceso, Resultados, Reflexión, Archivos, Atribución).</li>
  <li>Comprime las imágenes y las sube a <code>docs/images/&lt;sección&gt;/&lt;entrada&gt;/</code>.</li>
  <li>Agrega la página al menú en <code>mkdocs.yml</code> y hace <strong>un solo commit</strong> en la rama <code>main</code>.</li>
  <li>GitHub Actions reconstruye el sitio. Tarda uno o dos minutos; el avance se ve en <a href="https://github.com/martinfp642/martin_ferreira/actions" target="_blank" rel="noopener">Actions</a>.</li>
</ol>

<h3>Editor de páginas</h3>
<ul>
  <li><strong>+ Página nueva</strong> crea una página en la sección elegida a partir de una plantilla, y al guardar la agrega al menú.</li>
  <li>La barra <strong>Formato</strong> aplica negrita, títulos, listas, enlaces y tablas al texto seleccionado. La barra <strong>Bloques</strong> inserta carrete, galería, comparación, ficha de datos, línea de tiempo, video y etiquetas de resultado. Si hay fotos cargadas, el carrete y la galería se arman con ellas.</li>
  <li>La vista previa se actualiza sola mientras escribís, con los carretes funcionando. Se puede ver solo el texto, solo la vista previa, o las dos en paralelo. El botón <strong>⤢</strong> pone el editor a pantalla completa (Esc para salir).</li>
  <li>Atajos: <kbd>Ctrl</kbd>+<kbd>B</kbd> negrita, <kbd>Ctrl</kbd>+<kbd>I</kbd> cursiva, <kbd>Ctrl</kbd>+<kbd>K</kbd> enlace, <kbd>Ctrl</kbd>+<kbd>S</kbd> guardar.</li>
</ul>

<h3>Sin token</h3>
<p>Igual podés escribir la entrada, <strong>copiar el Markdown</strong> o <strong>descargar el .md</strong> y subirlo después desde Visual Studio Code, como hasta ahora.</p>

<h3>Si algo no anda</h3>
<ul>
  <li><strong>401 o 403</strong> → el token venció o no tiene <em>Contents: Read and write</em> sobre este repositorio.</li>
  <li><strong>409 o 422</strong> → alguien (o vos, desde otra computadora) cambió el repositorio mientras editabas. Actualizá la lista y volvé a intentar.</li>
  <li><strong>La página no aparece</strong> → mirá Actions: si el build falló, el error suele ser una ruta de imagen o una línea mal indentada en <code>mkdocs.yml</code>. Se corrige desde <strong>Editar archivo</strong>.</li>
</ul>

</section>

</div>
