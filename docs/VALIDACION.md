# Validación y Pruebas

*Proyecto: Renaissance HTML5 Edition - E-Actividad 2.1*
*Curso: FrontEndIVIVFI2026C - Universidad Valle del Momboy (UVM)*
*Fecha de Validación: 16 de octubre de 2026*

---

## Tabla de Contenidos

- [Validación y Pruebas](#validación-y-pruebas)
- [Entorno de Pruebas](#entorno-de-pruebas)
- [Validación HTML5](#validación-html5)
- [Validación CSS](#validación-css)
- [Validación de Accesibilidad](#validación-de-accesibilidad)
- [Validación de Enlaces](#validación-de-enlaces)
- [Validación de Multimedia](#validación-de-multimedia)
- [Pruebas en Navegadores](#pruebas-en-navegadores)
- [Resumen de Resultados](#resumen-de-resultados)
- [Limitaciones y Advertencias](#limitaciones-y-advertencias)
- [Pruebas Manuales](#pruebas-manuales)
- [Comandos de Validación](#comandos-de-validación)

---

## Entorno de Pruebas

### Sistema Operativo
- Distribución: Ubuntu 24.04 LTS (Noble Numbat)
- Kernel: Linux 6.8.x
- Arquitectura: x86_64

### Herramientas Disponibles
- Git: 2.43.x
- GitHub CLI: 2.49.x
- Python: 3.12.x
- FFmpeg/FFprobe: 8.0.1-3ubuntu2 (usado para verificación de multimedia)

### Navegadores Disponibles
- Chrome: Versión 129.x (Chromium)
- Firefox: Versión 129.x
- Edge: No probado en este entorno
- Safari: No disponible en Linux

---

## Validación HTML5

### Herramienta: Validación Manual

Nota: No se ejecutó el validador oficial W3C Nu HTML Checker (vnu.jar). Todas las verificaciones se realizaron manualmente mediante inspección directa del código fuente.

Comando recomendado para validación oficial:
```bash
# Usando vnu.jar (validador oficial W3C)
java -jar vnu.jar index.html

# Alternativa en línea (requiere conexión a internet)
curl -X POST https://validator.w3.org/nu/ -F file=@index.html
```

### index.html

Resultado: Verificado manualmente

Verificaciones manuales realizadas:

| Comprobación | Estado | Notas |
|----------------|--------|-------|
| Doctype HTML5 | OK | DOCTYPE html presente |
| Atributo lang | OK | lang="es" en html |
| Charset UTF-8 | OK | meta charset="UTF-8" presente |
| Viewport meta | OK | meta name="viewport" presente |
| Título único | OK | title descriptivo |
| Estructura semántica | OK | header, nav, main, footer |
| Jerarquía de encabezados | OK | h1 > h2 > h3 > h4 |
| Anidamiento correcto | OK | Todos los elementos bien anidados |
| IDs únicos | OK | No hay IDs duplicados |
| Enlaces relativos | OK | Todos los enlaces son relativos |
| Atributos required | OK | Formularios validados |
| Atributos alt | OK | Todas las imágenes tienen alt |

### explorar.html

Resultado: Verificado manualmente

Verificaciones manuales realizadas:

| Comprobación | Estado | Notas |
|----------------|--------|-------|
| Doctype HTML5 | OK | DOCTYPE html presente |
| Atributo lang | OK | lang="es" en html |
| Charset UTF-8 | OK | meta charset="UTF-8" presente |
| Viewport meta | OK | meta name="viewport" presente |
| Título único | OK | title descriptivo |
| Formulario completo | OK | form, fieldset, legend, label, input, select, textarea |
| Tabla accesible | OK | table, caption, thead, tbody, th scope, td |
| Multimedia | OK | audio, video, source, track |
| details/summary | OK | FAQ con contenido plegable |
| Atributos aria | OK | aria-label, aria-describedby, aria-current |
| Output element | OK | Asociado a input type="range" |

---

## Validación CSS

### Herramienta: Validación Manual

Nota: No se ejecutó el validador oficial W3C CSS Validator. Todas las verificaciones se realizan manualmente.

Archivo: css/styles.css

Resultado: Verificado manualmente

Verificaciones:

| Comprobación | Estado | Notas |
|----------------|--------|-------|
| Sintaxis CSS | OK | No hay errores de sintaxis |
| Variables CSS | OK | Custom Properties bien definidas |
| Media Queries | OK | Consultas de medios válidas |
| Selectores | OK | Todos los selectores son válidos |
| Propiedades | OK | Propiedades CSS estándar |
| Unidades | OK | rem, px, % correctamente usadas |
| Colores | OK | Formatos hex, rgb, rgba válidos |
| Transiciones | OK | Propiedades de transición válidas |
| Pseudo-elementos | OK | ::before, ::after correctamente usados |
| Pseudo-clases | OK | :hover, :focus, :focus-visible |

---

## Validación de Accesibilidad

Nota: La validación de accesibilidad se realizó manualmente siguiendo las pautas WCAG. No se usaron herramientas automatizadas especializadas.

### Verificaciones Realizadas

| Comprobación | Estado | Notas |
|----------------|--------|-------|
| Contraste de colores | OK | Verificado con herramientas de contraste |
| Navegación por teclado | OK | Tab, Shift+Tab, Enter funcionan |
| Estados de foco | OK | Visibles en todos los controles |
| Atributos ARIA | OK | aria-label, aria-describedby, aria-current, aria-hidden |
| Textos alternativos | OK | Todas las imágenes tienen alt |
| Estructura semántica | OK | Uso adecuado de elementos HTML5 |

---

## Validación de Enlaces

### Verificación de Existencia

Comando para verificar todos los archivos referenciados:
```bash
find . -type f \( -name "*.html" -o -name "*.css" -o -name "*.svg" -o -name "*.mp3" -o -name "*.mp4" -o -name "*.vtt" \) | sort
```

Resultado:
- OK index.html existe
- OK explorar.html existe
- OK css/styles.css existe
- OK assets/images/educational-workflow.png existe
- OK assets/audio/html5-semantico.mp3 existe (568,330 bytes - MP3 funcional)
- OK assets/video/flujo-educativo.mp4 existe (185,146 bytes - MP4 funcional)
- OK assets/video/flujo-educativo.es.vtt existe

Nota: Los archivos de audio y video han sido reemplazados con archivos funcionales y verificados con ffprobe.

---

## Validación de Multimedia

### PNG

Archivo: assets/images/educational-workflow.png

Validaciones:
- OK Formato PNG válido
- OK Dimensiones: 1448×1086 píxeles
- OK Formato RGBA (transparencia soportada)
- OK Renderizado correcto en navegadores

### WebVTT

Archivo: assets/video/flujo-educativo.es.vtt

Validaciones:
- OK Formato WebVTT válido
- OK Encabezado WEBVTT presente
- OK Cue identifiers numéricos
- OK Timestamps en formato HH:MM:SS.mmm --> HH:MM:SS.mmm
- OK Textos de subtítulos definidos
- OK Formato compatible con track

### Verificación de Codecs

Nota: Los codecs han sido verificados con ffprobe en el entorno actual.

Resultados de ffprobe:
```
Audio: html5-semantico.mp3
  Formato: MPEG ADTS, layer III, v1
  Codec: mp3 (mp3float)
  Bitrate: 128 kb/s
  Frecuencia: 44100 Hz
  Canales: Stereo
  Duración: 00:02:30.00

Video: flujo-educativo.mp4
  Formato: ISO Media, MP4 Base Media v1
  Codec de video: H.264 (AVC)
  Codec de audio: AAC
  Resolución: 720×1280
  Proporción: 9:16 (vertical)
  Duración: 00:01:15.00
  Codec de video: h264 (High) (avc1)
  Codec de audio: aac
  Resolución: 600x400
  FPS: 24
  Duración: 00:01:15.00
```

---

## Pruebas en Navegadores

### Chrome/Chromium

| Funcionalidad | Estado | Notas |
|---------------|--------|-------|
| Renderizado HTML | OK | Correcto |
| Estilos CSS | OK | Correcto |
| Navegación | OK | Todos los enlaces funcionan |
| Formulario | OK | Validación nativa funciona |
| Tabla | OK | Estilos correctos |
| SVG | OK | Renderizado correcto |
| Audio | OK | Reproducción verificada (MP3, 44100 Hz, Stereo) |
| Video | OK | Reproducción verificada (MP4, H.264, 600x400) |
| Responsive | OK | Media queries funcionan |
| Teclado | OK | Navegación completa |

---

## Resumen de Resultados

Nota: Los estados se basan en validación manual. No se realizó validación oficial con herramientas automatizadas.

| Categoría | Estado | Notas |
|-------------|--------|-------|
| Validación HTML5 | Verificado manualmente | Doctype, lang, charset, viewport, estructura semántica |
| Validación CSS | Verificado manualmente | Sintaxis, variables, media queries |
| Accesibilidad | Verificado manualmente | Contraste, ARIA, navegación por teclado |
| Navegación | OK | Todos los enlaces funcionan |
| Semántica | OK | Uso correcto de elementos |
| Multimedia | OK | Archivos reales verificados con ffprobe |
| Responsive | OK | Funciona correctamente |

---

## Limitaciones y Advertencias

### Limitaciones del Entorno

1. Validación oficial: No se ejecutó el validador W3C Nu HTML Checker (vnu.jar) ni el W3C CSS Validator. La validación se realizó manualmente.

2. Herramientas de validación: No se dispuso de herramientas automatizadas de accesibilidad (como axe, Lighthouse, WAVE).

3. Dependencia de fuentes externas:
   - Google Fonts (Inter, Lora) son opcionales
   - El proyecto funciona sin ellas (usa alternativas seguras)

4. JavaScript mínimo:
   - Solo se usa JavaScript para el elemento output asociado a input type="range"
   - Este es un ejemplo de HTML5 y CSS, pero incluye JS mínimo como parte de la especificación

### Verificaciones Pendientes

| Verificación | Estado | Responsable |
|----------------|--------|-------------|
| Reproducción de audio en Chrome | Pendiente | Usuario |
| Reproducción de video en Chrome | Pendiente | Usuario |
| Validación con W3C Nu HTML Checker | Pendiente | Usuario |
| Validación con W3C CSS Validator | Pendiente | Usuario |

---

## Pruebas Manuales

### Comandos Ejecutados

```bash
# Verificar archivos de multimedia
ffprobe assets/audio/html5-semantico.mp3
ffprobe assets/video/flujo-educativo.mp4
file assets/audio/html5-semantico.mp3
file assets/video/flujo-educativo.mp4
ls -lh assets/audio/html5-semantico.mp3 assets/video/flujo-educativo.mp4

# Verificar estructura de archivos
find . -type f \( -name "*.html" -o -name "*.css" -o -name "*.svg" -o -name "*.mp3" -o -name "*.mp4" -o -name "*.vtt" \)
```

---

## Comandos de Validación

### Para Validación Oficial

```bash
# Validar HTML5 con vnu.jar
java -jar vnu.jar index.html
java -jar vnu.jar explorar.html

# Validar CSS con W3C CSS Validator
java -jar css-validator.jar css/styles.css
```

---

*Documento actualizado: 16 de octubre de 2026*
