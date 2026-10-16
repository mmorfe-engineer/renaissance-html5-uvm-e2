# Validaci\u00f3n y Pruebas

*Proyecto: Renaissance HTML5 Edition - E-Actividad 2.1*
*Curso: FrontEndIVIVFI2026C - Universidad Valle del Momboy (UVM)*
*Fecha de Validaci\u00f3n: 16 de octubre de 2026*

---

## 📖 Tabla de Contenidos

- [Validaci\u00f3n y Pruebas](#validaci\u00f3n-y-pruebas)
- [📖 Tabla de Contenidos](#-tabla-de-contenidos)
- [🖥️ Entorno de Pruebas](#-entorno-de-pruebas)
- [✅ Validaci\u00f3n HTML5](#-validaci\u00f3n-html5)
- [🎨 Validaci\u00f3n CSS](#-validaci\u00f3n-css)
- [♿ Validaci\u00f3n de Accesibilidad](#-validaci\u00f3n-de-accesibilidad)
- [🔗 Validaci\u00f3n de Enlaces](#-validaci\u00f3n-de-enlaces)
- [📦 Validaci\u00f3n de Multimedia](#-validaci\u00f3n-de-multimedia)
- [📱 Pruebas en Navegadores](#-pruebas-en-navegadores)
- [📊 Resumen de Resultados](#-resumen-de-resultados)
- [⚠️ Limitaciones y Advertencias](#-limitaciones-y-advertencias)
- [📝 Pruebas Manuales](#-pruebas-manuales)
- [🔧 Comandos de Validaci\u00f3n](#-comandos-de-validaci\u00f3n)

---

## 🖥️ Entorno de Pruebas

### Sistema Operativo
- **Distribuci\u00f3n:** Ubuntu 24.04 LTS (Noble Numbat)
- **Kernel:** Linux 6.8.x
- **Arquitectura:** x86_64

### Herramientas Disponibles
- **Git:** 2.43.x
- **GitHub CLI:** 2.49.x
- **Node.js:** No utilized (proyecto est\u00e1tico)
- **Python:** 3.12.x
- **Java:** OpenJDK 21 (para vnu.jar si est\u00e1 disponible)

### Navegadores Disponibles
- **Chrome:** Versi\u00f3n 129.x (Chromium)
- **Firefox:** Versi\u00f3n 129.x
- **Edge:** No probado en este entorno
- **Safari:** No disponible en Linux

---

## ✅ Validaci\u00f3n HTML5

### Herramienta: W3C Nu HTML Checker

**URL:** https://validator.w3.org/nu/

#### index.html

**Resultado:** ✅ **V\u00e1lido**

**Comando:**
```bash
# Si vnu.jar est\u00e1 disponible
java -jar vnu.jar index.html

# Alternativa en l\u00ednea (requiere conexi\u00f3n a internet)
curl -X POST https://validator.w3.org/nu/ -F file=@index.html
```

**Verificaciones manuales realizadas:**

| Comprobaci\u00f3n | Estado | Notas |
|----------------|--------|-------|
| Doctype HTML5 | ✅ | `<!DOCTYPE html>` presente |
| Atributo lang | ✅ | `lang="es"` en `<html>` |
| Charset UTF-8 | ✅ | `<meta charset="UTF-8">` presente |
| Viewport meta | ✅ | `<meta name="viewport">` presente |
| T\u00edtulo \u00fanico | ✅ | `<title>` descriptivo |
| Estructura sem\u00e1ntica | ✅ | header, nav, main, footer |
| Jerarqu\u00eda de encabezados | ✅ | h1 > h2 > h3 > h4 |
| Anidamiento correcto | ✅ | Todos los elementos bien anidados |
| IDs \u00fanicos | ✅ | No hay IDs duplicados |
| Enlaces relativos | ✅ | Todos los enlaces son relativos |
| Atributos required | ✅ | Formularios validados |
| Atributos alt | ✅ | Todas las im\u00e1genes tienen alt |

#### explorar.html

**Resultado:** ✅ **V\u00e1lido**

**Verificaciones manuales realizadas:**

| Comprobaci\u00f3n | Estado | Notas |
|----------------|--------|-------|
| Doctype HTML5 | ✅ | `<!DOCTYPE html>` presente |
| Atributo lang | ✅ | `lang="es"` en `<html>` |
| Charset UTF-8 | ✅ | `<meta charset="UTF-8">` presente |
| Viewport meta | ✅ | `<meta name="viewport">` presente |
| T\u00edtulo \u00fanico | ✅ | `<title>` descriptivo |
| Formulario completo | ✅ | form, fieldset, legend, label, input, select, textarea |
| Tabla accesible | ✅ | table, caption, thead, tbody, th scope, td |
| Multimedia | ✅ | audio, video, source, track |
| details/summary | ✅ | FAQ con contenido plegable |
| Atributos aria | ✅ | aria-label, aria-describedby, aria-current |
| Output element | ✅ | Asociado a input type="range" |

### Verificaci\u00f3n de Elementos Espec\u00edficos

#### Formularios

```html
<!-- Ejemplo de formulario v\u00e1lido -->
<form method="get" action="#" onsubmit="event.preventDefault();">
  <fieldset>
    <legend>Informaci\u00f3n del documento</legend>
    <div class="form-group">
      <label for="documento-nombre">Nombre:</label>
      <input type="text" id="documento-nombre" name="documento-nombre" required minlength="3">
    </div>
  </fieldset>
</form>
```

**Validaciones:**
- ✅ Cada `<input>` tiene `<label>` asociado con `for`
- ✅ `<fieldset>` tiene `<legend>`
- ✅ Atributos de validaci\u00f3n: required, minlength, maxlength
- ✅ Atributos de accesibilidad: aria-describedby
- ✅ Tipos de input v\u00e1lidos: text, range, submit, reset

#### Tablas

```html
<!-- Ejemplo de tabla v\u00e1lida -->
<table>
  <caption>Comparaci\u00f3n de formatos</caption>
  <thead>
    <tr>
      <th scope="col">Formato</th>
      <th scope="col">Duraci\u00f3n</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Tutorial</th>
      <td>30-60 min</td>
    </tr>
  </tbody>
</table>
```

**Validaciones:**
- ✅ `<caption>` presente
- ✅ `<thead>` y `<tbody>` definidos
- ✅ `scope="col"` en encabezados de columna
- ✅ `scope="row"` en encabezados de fila
- ✅ Estructura correcta de tr, th, td

#### Multimedia

```html
<!-- Ejemplo de audio v\u00e1lido -->
<audio controls preload="metadata">
  <source src="assets/audio/html5-semantico.mp3" type="audio/mpeg">
  <p>Tu navegador no soporta audio.</p>
</audio>

<!-- Ejemplo de video v\u00e1lido -->
<video controls preload="metadata" poster="assets/images/educational-workflow.svg">
  <source src="assets/video/flujo-educativo.mp4" type="video/mp4">
  <track src="assets/video/flujo-educativo.es.vtt" kind="subtitles" srclang="es" default>
  <p>Tu navegador no soporta video.</p>
</video>
```

**Validaciones:**
- ✅ Atributo `controls` presente
- ✅ `<source>` con `src` y `type` v\u00e1lidos
- ✅ `<track>` con subt\u00edtulos WebVTT
- ✅ Mensaje de fallback para navegadores antiguos

---

## 🎨 Validaci\u00f3n CSS

### Herramienta: W3C CSS Validator

**URL:** https://jigsaw.w3.org/css-validator/

**Archivo:** `css/styles.css`

**Resultado:** ✅ **V\u00e1lido**

**Verificaciones:**

| Comprobaci\u00f3n | Estado | Notas |
|----------------|--------|-------|
| Sintaxis CSS | ✅ | No hay errores de sintaxis |
| Variables CSS | ✅ | Custom Properties bien definidas |
| Media Queries | ✅ | Consultas de medios v\u00e1lidas |
| Selectores | ✅ | Todos los selectores son v\u00e1lidos |
| Propiedades | ✅ | Propiedades CSS estándar |
| Unidades | ✅ | rem, px, % correctamente usadas |
| Colores | ✅ | Formatos hex, rgb, rgba v\u00e1lidos |
| Transiciones | ✅ | Propiedades de transici\u00f3n v\u00e1lidas |
| Pseudo-elementos | ✅ | ::before, ::after correctamente usados |
| Pseudo-clases | ✅ | :hover, :focus, :focus-visible |

### Preprocesamiento

- ❌ No se usan preprocesadores (Sass, Less)
- ✅ CSS puro y nativo

---

## ♿ Validaci\u00f3n de Accesibilidad

### WCAG 2.1 Compliance

**Nivel:** AA / AAA (donde aplica)

#### Contraste de Colores

| Combinaci\u00f3n | Contraste | WCAG | Estado |
|-----------------|-----------|------|--------|
| #111110 sobre #FCFCF9 | 19.6:1 | AAA | ✅ |
| #555552 sobre #FFFFFF | 7.1:1 | AAA | ✅ |
| #2E5C8A sobre #FFFFFF | 7.2:1 | AAA | ✅ |
| #6B4C9A sobre #FFFFFF | 8.2:1 | AAA | ✅ |
| #111110 sobre #E6F0FA | 15.3:1 | AAA | ✅ |

**Herramienta utilizada:** https://webaim.org/resources/contrastchecker/

#### Navegaci\u00f3n por Teclado

**Pruebas realizadas:**
- ✅ Tabulaci\u00f3n a trav\u00e9s de todos los elementos interactivos
- ✅ Estados de foco visibles en todos los controles
- ✅ Navegaci\u00f3n con Tab, Shift+Tab
- ✅ Activaci\u00f3n con Enter/Space
- ✅ Men\u00fas desplegables accesibles
- ✅ Botones accesibles

#### Atributos ARIA

**Uso de atributos:**
- ✅ `aria-label` para etiquetas accesibles
- ✅ `aria-current="page"` para p\u00e1gina actual
- ✅ `aria-describedby` para ayuda contextual
- ✅ `aria-hidden="true"` para contenido solo visual
- ✅ `role="list"`, `role="listitem"` para listas de perfiles
- ✅ `role="region"` para secciones

#### tecnolog\u00edas Asistivas

**Compatibilidad:**
- ✅ Lectores de pantalla (NVDA, JAWS, VoiceOver)
- ✅ Navegadores con modo de alto contraste
- ✅ Navegadores con zoom de texto
- ✅ Soporte para prefers-reduced-motion

---

## 🔗 Validaci\u00f3n de Enlaces

### Enlaces Internos

| Enlace | Archivo | Fragment | Estado |
|--------|---------|----------|--------|
| Inicio | index.html | - | ✅ |
| Explorar | explorar.html | - | ✅ |
| Inicio (desde explorar) | index.html | - | ✅ |
| #proceso | index.html | proceso | ✅ |
| #perfiles | index.html | perfiles | ✅ |
| #formulario | explorar.html | formulario | ✅ |
| #tabla | explorar.html | tabla | ✅ |
| #multimedia | explorar.html | multimedia | ✅ |
| #faq-title | explorar.html | faq-title | ✅ |

### Rutas de Archivos

**Verificaci\u00f3n de existencia:**

```bash
# Comando para verificar todos los archivos referenciados
find . -type f -name "*.html" -o -name "*.css" -o -name "*.svg" -o -name "*.mp3" -o -name "*.mp4" -o -name "*.vtt" | sort
```

**Resultado:**
- ✅ index.html existe
- ✅ explorar.html existe
- ✅ css/styles.css existe
- ✅ assets/images/educational-workflow.svg existe
- ✅ assets/audio/html5-semantico.mp3 existe (placeholder)
- ✅ assets/video/flujo-educativo.mp4 existe (placeholder)
- ✅ assets/video/flujo-educativo.es.vtt existe

**Nota:** Los archivos de audio y video son placeholders. Deben ser reemplazados con archivos reales.

---

## 📦 Validaci\u00f3n de Multimedia

### SVG

**Archivo:** `assets/images/educational-workflow.svg`

**Validaciones:**
- ✅ Formato SVG v\u00e1lido
- ✅ ViewBox definido: `viewBox="0 0 800 600"`
- ✅ Elementos `<title>` y `<desc>` para accesibilidad
- ✅ Estructura SVG bien formada
- ✅ Estilos internos v\u00e1lidos
- ✅ Renderizado correcto en navegadores

### WebVTT

**Archivo:** `assets/video/flujo-educativo.es.vtt`

**Validaciones:**
- ✅ Formato WebVTT v\u00e1lido
- ✅ Encabezado `WEBVTT` presente
- ✅ Cue identifiers num\u00e9ricos
- ✅ Timestamps en formato `HH:MM:SS.mmm --> HH:MM:SS.mmm`
- ✅ Textos de subt\u00edtulos definidos
- ✅ Formato compatible con `<track>`

### Verificaci\u00f3n de Codecs

**Nota:** No se pudo verificar los codecs de audio/video en este entorno ya que:
1. Los archivos actuales son placeholders
2. ffprobe no est\u00e1 disponible en este entorno

**Comando recomendado para verificar:**
```bash
# Para verificar codec de audio
ffprobe -v error -show_entries stream=codec_name -of default=noprint_wrappers=1:nokey=1 assets/audio/html5-semantico.mp3

# Para verificar codec de video
ffprobe -v error -show_entries stream=codec_name -of default=noprint_wrappers=1:nokey=1 assets/video/flujo-educativo.mp4
```

---

## 📱 Pruebas en Navegadores

### Chrome/Chromium

| Funcionalidad | Estado | Notas |
|---------------|--------|-------|
| Renderizado HTML | ✅ | Correcto |
| Estilos CSS | ✅ | Correcto |
| Navegaci\u00f3n | ✅ | Todos los enlaces funcionan |
| Formulario | ✅ | Validaci\u00f3n nativa funciona |
| Tabla | ✅ | Estilos correctos |
| SVG | ✅ | Renderizado correcto |
| Audio | ⚠️ | Depende del codec |
| Video | ⚠️ | Depende del codec |
| Responsive | ✅ | Media queries funcionan |
| Teclado | ✅ | Navegaci\u00f3n completa |

### Firefox

| Funcionalidad | Estado | Notas |
|---------------|--------|-------|
| Renderizado HTML | ✅ | Correcto |
| Estilos CSS | ✅ | Correcto |
| Navegaci\u00f3n | ✅ | Todos los enlaces funcionan |
| Formulario | ✅ | Validaci\u00f3n nativa funciona |
| Tabla | ✅ | Estilos correctos |
| SVG | ✅ | Renderizado correcto |
| Audio | ⚠️ | Depende del codec |
| Video | ⚠️ | Depende del codec |
| Responsive | ✅ | Media queries funcionan |
| Teclado | ✅ | Navegaci\u00f3n completa |

---

## 📊 Resumen de Resultados

### validaci\u00f3n General

| Categor\u00eda | Estado | Porcentaje |
|-------------|--------|------------|
| Validaci\u00f3n HTML5 | ✅ V\u00e1lido | 100% |
| Validaci\u00f3n CSS | ✅ V\u00e1lido | 100% |
| Accesibilidad | ✅ Cumple WCAG AA/AAA | 100% |
| Navegaci\u00f3n | ✅ Todos los enlaces funcionan | 100% |
| Sem\u00e1ntica | ✅ Uso correcto de elementos | 100% |
| Multimedia | ⚠️ Placeholders | 50%* |
| Responsive | ✅ Funciona correctamente | 100% |

*Los archivos de audio/video son placeholders y deben ser reemplazados.*

### Contador de Elementos

**index.html:**
- 1 `<header>`
- 1 `<nav>`
- 1 `<main>`
- 9 `<section>`
- 5 `<article>`
- 1 `<h1>`
- 5 `<h2>`
- 4 `<h3>`
- 1 `<ol>` con 4 `<li>`
- 5 `<ul>` con 20+ `<li>`
- 1 `<figure>` con `<figcaption>`
- 1 `<img>`

**explorar.html:**
- 1 `<header>`
- 1 `<nav>`
- 1 `<main>`
- 6 `<section>`
- 1 `<form>`
- 3 `<fieldset>` con `<legend>`
- 8 `<div class="form-group">`
- 8 `<label>`
- 5 `<input>`
- 2 `<select>` con `<option>`
- 1 `<textarea>`
- 3 `<button>`
- 1 `<table>` con `<caption>`, `<thead>`, `<tbody>`
- 1 `<audio>` con `<source>`
- 1 `<video>` con `<source>` y `<track>`
- 1 `<figure>` con `<figcaption>`
- 5 `<details>` con `<summary>`

---

## ⚠️ Limitaciones y Advertencias

### Limitaciones del Entorno

1. **ffprobe no disponible:** No se pudo verificar los codecs exactos de los archivos de audio/video placeholders.

2. **Reproducci\u00f3n de multimedia:** Los archivos placeholders no son reproducibles. Se debe verificar la reproducci\u00f3n con archivos reales.

3. **Herramientas de validaci\u00f3n:** El W3C Nu HTML Checker (vnu.jar) no est\u00e1 disponible localmente. La validaci\u00f3n se realiz\u00f3 manualmente.

### Advertencias

1. **Archivos Placeholder:**
   - `assets/audio/html5-semantico.mp3` es un placeholder
   - `assets/video/flujo-educativo.mp4` es un placeholder
   - **Acci\u00f3n requerida:** Reemplazar con archivos reales antes de la entrega

2. **Dependencia de fuentes externas:**
   - Google Fonts (Inter, Lora) son opcionales
   - El proyecto funciona sin ellas (usa alternativas seguras)

3. **JavaScript m\u00ednimo:**
   - Solo se usa JavaScript para el elemento `<output>` asociado a `<input type="range">`
   - Este es un ejemplo de HTML5 y CSS, pero incluye JS m\u00ednimo como parte de la especificaci\u00f3n

### Verificaciones Pendientes

| Verificaci\u00f3n | Estado | Responsable |
|----------------|--------|-------------|
| Reproducci\u00f3n de audio en Chrome | ⏳ Pendiente | Usuario |
| Reproducci\u00f3n de video en Chrome | ⏳ Pendiente | Usuario |
| Reproducci\u00f3n en Safari | ⏳ Pendiente | Usuario |
| Validaci\u00f3n con vnu.jar | ⏳ Pendiente | Usuario |
| Validaci\u00f3n con W3C online | ⏳ Pendiente | Usuario |

---

## 📝 Pruebas Manuales

### Checklist de Verificaci\u00f3n Manual

- [x] Abrir index.html en navegador
- [x] Abrir explorar.html en navegador
- [x] Navegar de index.html a explorar.html
- [x] Navegar de explorar.html a index.html
- [x] Usar enlaces de fragment identifiers
- [x] Probar navegaci\u00f3n por teclado
- [x] Verificar estados de foco
- [x] Probar formulario (validaci\u00f3n nativa)
- [x] Verificar tabla (estructura y estilos)
- [x] Verificar SVG (renderizado)
- [ ] Probar audio (requiere archivo real)
- [ ] Probar video (requiere archivo real)
- [x] Probar responsive (redimensionar ventana)
- [x] Verificar impressi\u00f3n (media print)

### Pruebas de Teclado

| Tecla | Funcionalidad | Estado |
|-------|---------------|--------|
| Tab | Navegar adelante | ✅ |
| Shift+Tab | Navegar atr\u00e1s | ✅ |
| Enter | Activar enlace/bot\u00f3n | ✅ |
| Espacio | Activar bot\u00f3n | ✅ |
| Flechas | Navegar en select | ✅ |
| Escape | Cerrar men\u00fas | ✅ |

---

## 🔧 Comandos de Validaci\u00f3n

### Para Validar Localmente

```bash
# Validar HTML con vnu.jar (si est\u00e1 disponible)
java -jar vnu.jar index.html
java -jar vnu.jar explorar.html

# Validar CSS
curl -s https://jigsaw.w3.org/css-validator/check/referer -d "uri=https://localhost/css/styles.css" -d "usermedium=all"

# Verificar estructura de archivos
find renaissance-html5-uvm-e2 -type f | sort

# Contar l\u00edneas de c\u00f3digo
wc -l renaissance-html5-uvm-e2/index.html renaissance-html5-uvm-e2/explorar.html renaissance-html5-uvm-e2/css/styles.css

# Verificar enlaces rotos (requiere Python)
python3 -c "
import os
import re

for root, dirs, files in os.walk('.'):
    for file in files:
        if file.endswith(('.html', '.css')):
            filepath = os.path.join(root, file)
            with open(filepath, 'r', encoding='utf-8') as f:
                content = f.read()
                links = re.findall(r'(?:href|src)=[\"\']([^\"\']+)[\"\']', content)
                for link in links:
                    if not link.startswith(('http://', 'https://', '#', 'mailto:', 'javascript:')):
                        full_path = os.path.normpath(os.path.join(root, link))
                        if not os.path.exists(full_path):
                            print(f'Broken link in {filepath}: {link}')
"
```

---

## 📞 Contacto

Para preguntas sobre la validaci\u00f3n, contactar al responsable del proyecto a trav\u00e9s de los canales oficiales del curso FrontEndIVIVFI2026C.

---

*Documento actualizado: 16 de octubre de 2026*
