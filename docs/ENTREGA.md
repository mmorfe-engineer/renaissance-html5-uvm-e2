# Instrucciones de Entrega

*Proyecto: Renaissance HTML5 Edition - E-Actividad 2.1*
*Curso: FrontEndIVIVFI2026C - Universidad Valle del Momboy (UVM)*
*Profesor: Prof. Anggelo Huz*
*Fecha l\u00edmite: 17 de octubre de 2026, 23:59 (GMT-4)*

---

## 📖 Tabla de Contenidos

- [Instrucciones de Entrega](#instrucciones-de-entrega)
- [📖 Tabla de Contenidos](#-tabla-de-contenidos)
- [📋 Checklist de Entrega Individual](#-checklist-de-entrega-individual)
- [📦 Empaquetado ZIP](#-empaquetado-zip)
- [📁 Contenido del ZIP](#-contenido-del-zip)
- [🚫 Archivos a Excluir](#-archivos-a-excluir)
- [🏷️ Convenciones de Nombrado](#-convenciones-de-nombrado)
- [🔗 Entrega en la Plataforma UVM](#-entrega-en-la-plataforma-uvm)
- [📤 Publicaci\u00f3n en GitHub](#-publicaci\u00f3n-en-github)
- [📝 Declaraci\u00f3n de Autenticidad](#-declaraci\u00f3n-de-autenticidad)
- [📅 Calendario y Fechas](#-calendario-y-fechas)
- [💡 Recomendaciones Finales](#-recomendaciones-finales)
- [⚠️ Errores Comunes a Evitar](#-errores-comunes-a-evitar)
- [📞 Contacto y Soporte](#-contacto-y-soporte)

---

## 📋 Checklist de Entrega Individual

Usa esta lista para verificar que todo est\u00e1 listo antes de la entrega:

### ✅ Requisitos T\u00e9cnicos

- [ ] Dos archivos HTML independientes (index.html, explorar.html)
- [ ] Estructura sem\u00e1ntica HTML5 correcta (header, nav, main, section, article, footer)
- [ ] Jerarqu\u00eda de encabezados coherente (h1, h2, h3, h4)
- [ ] P\u00e1rrafos con contenido significativo
- [ ] Listas ordenadas (ol, li) implementadas
- [ ] Listas desordenadas (ul, li) implementadas
- [ ] Navegaci\u00f3n funcional entre p\u00e1ginas
- [ ] Formularios con etiquetas asociadas (label for)
- [ ] Formularios con fieldset y legend
- [ ] Tablas con caption, thead, tbody, th[scope], td
- [ ] Elementos multimedia (img, audio, video) con controles
- [ ] Elementos multimedia con subt\u00edtulos/transcripciones
- [ ] Sintaxis HTML v\u00e1lida (validada con W3C)
- [ ] Atributos lang="es" en todos los HTML
- [ ] Atributos charset="UTF-8"
- [ ] Meta tag viewport
- [ ] T\u00edtulos descriptivos en todas las p\u00e1ginas
- [ ] Enlaces relativos funcionales
- [ ] No hay IDs duplicados

### ✅ CSS y Dise\u00f1o

- [ ] CSS original en archivo externo (styles.css)
- [ ] Dise\u00f1o responsive (mobile-first)
- [ ] Media queries implementadas
- [ ] Flexbox y/o CSS Grid utilizados
- [ ] Estados de foco visibles
- [ ] Colores con contraste WCAG AA/AAA
- [ ] Sintaxis CSS v\u00e1lida

### ✅ Accesibilidad

- [ ] Textos alternativos (alt) en todas las im\u00e1genes
- [ ] Atributos ARIA apropiados
- [ ] Navegaci\u00f3n por teclado funcional
- [ ] Estados de foco visibles para todos los controles
- [ ] Estructura de tablas accesible
- [ ] Subt\u00edtulos WebVTT v\u00e1lidos
- [ ] Transcripciones para audio/video

### ✅ Contenido

- [ ] M\u00e1s de 500 palabras de contenido original
- [ ] Contenido en espa\u00f1ol correcto
- [ ] Ortograf\u00eda y gram\u00e1tica verificadas
- [ ] Contenido educativo sobre HTML5
- [ ] Explicaci\u00f3n de conceptos del curso

### ✅ Multimedia

- [x] PNG original y accesible
- [x] Audio MP3 (html5-semantico.mp3) - Archivo funcional
- [x] Video MP4 (flujo-educativo.mp4) - Archivo funcional
- [ ] Subt\u00edtulos WebVTT (flujo-educativo.es.vtt)
- [ ] Transcripciones de audio/video

### ✅ Documentaci\u00f3n

- [ ] README.md completo
- [ ] REFERENCIAS.md con formato APA
- [ ] docs/ARQUITECTURA.md
- [ ] docs/VALIDACION.md
- [ ] docs/RUBRICA.md
- [ ] docs/GUIA_VIDEO.md
- [ ] docs/ENTREGA.md

### ✅ Validaci\u00f3n

- [ ] Validaci\u00f3n HTML con W3C Nu Checker
- [ ] Validaci\u00f3n CSS con W3C CSS Validator
- [ ] Pruebas de accesibilidad realizadas
- [ ] Pruebas en m\u00fasltiples navegadores
- [ ] Pruebas de navegaci\u00f3n por teclado
- [ ] Pruebas de enlaces funcionales

---

## 📦 Empaquetado ZIP

### Instrucciones para Crear el ZIP

1. **Navegar al directorio padre del proyecto:**
   ```bash
   cd /home/bitcoinpapa
   ```

2. **Verificar la estructura del proyecto:**
   ```bash
   ls -la renaissance-html5-uvm-e2/
   ```

3. **Crear el archivo ZIP:**
   
   **En Linux/Mac:**
   ```bash
   # Navegar al directorio padre
   cd /home/bitcoinpapa
   
   # Crear ZIP (excluyendo .git/)
   zip -r cedula_nombre.zip renaissance-html5-uvm-e2/ -x "renaissance-html5-uvm-e2/.git/*"
   
   # O usando tar
   tar -czf cedula_nombre.tar.gz renaissance-html5-uvm-e2/ --exclude=".git"
   ```

   **En Windows:**
   - Seleccionar la carpeta `renaissance-html5-uvm-e2`
   - Click derecho > "Enviar a" > "Carpeta comprimida (zip)"
   - Renombrar el archivo resultante a `cedula_nombre.zip`
   - Abrir el ZIP y eliminar el directorio `.git/` si existe

4. **Verificar el contenido del ZIP:**
   ```bash
   # En Linux/Mac
   unzip -l cedula_nombre.zip
   
   # En Windows
   Extraer el ZIP y verificar los archivos
   ```

---

## 📁 Contenido del ZIP

El archivo ZIP debe contener **exactamente** la siguiente estructura:

```
cedula_nombre.zip
└── renaissance-html5-uvm-e2/
    ├── index.html
    ├── explorar.html
    ├── css/
    │   └── styles.css
    ├── assets/
    │   ├── images/
    │   │   └── educational-workflow.svg
    │   ├── audio/
    │   │   ├── html5-semantico.mp3  ✅ Funcional
    │   │   └── README.txt
    │   └── video/
    │       ├── flujo-educativo.mp4  ✅ Funcional
    │       ├── flujo-educativo.es.vtt
    │       └── README.txt
    ├── docs/
    │   ├── ARQUITECTURA.md
    │   ├── VALIDACION.md
    │   ├── RUBRICA.md
    │   ├── GUIA_VIDEO.md
    │   └── ENTREGA.md
    ├── REFERENCIAS.md
    ├── README.md
    └── .gitignore
```

**Total de archivos:** 20 archivos
**Tama\u00f1o estimado:** ~25-30 MB (con archivos de audio/video reales)

---

## 🚫 Archivos a Excluir

**NO incluir los siguientes archivos/directorios:**

1. **Directorio `.git/`**
   - Contiene el historial de Git
   - No es necesario para la entrega
   - Puede causar problemas de tama\u00f1o

2. **Archivos temporales:**
   - `*.tmp`
   - `*.swp` (Vim)
   - `*.swo` (Vim)
   - `.DS_Store` (Mac)
   - `Thumbs.db` (Windows)
   - `.vscode/`
   - `.idea/`
   - `.cache/`
   - `node_modules/` (no aplica para este proyecto)

3. **Archivos de sistema:**
   - `desktop.ini`
   - `*.lnk`

4. **Archivos de entorno:**
   - `.env`
   - `*.env.*`

**Nota:** El archivo `.gitignore` S\u0000 DEBE ser incluido en el ZIP.

---

## 🏷️ Convenciones de Nombrado

### Nombre del Archivo ZIP

El archivo ZIP debe seguir el formato:

```
cedula_nombre.zip
```

**Donde:**
- `cedula` = Tu n\u00famero de c\u00e9dula de identidad (solo d\u00edgitos, sin espacios ni caracteres especiales)
- `nombre` = Tu nombre completo (apellido y nombre, separados por guiones bajos)

**Ejemplos:**
- `12345678_Jose_Perez.zip`
- `23456789_Maria_Gomez_Lopez.zip`
- `123456789_Juan_Carlos_Rodriguez.zip`

**⚠️ ADVERTENCIA:** 
- NO inventar un n\u00famero de c\u00e9dula
- NO usar el n\u00famero de c\u00e9dula de otra persona
- NO usar nombres gen\u00e9ricos como "estudiante" o "alumno"
- El n\u00famero debe ser VERIDICO y CORRESPONDER al estudiante

### Nombre del Repositorio GitHub

Si publicas en GitHub, el repositorio debe llamarse:

```
renaissance-html5-uvm-e2
```

**No usar:**
- `E-Actividad-2.1`
- `HTML5-Project`
- `my-uvm-project`
- Cualquier otro nombre

---

## 🔗 Entrega en la Plataforma UVM

### Pasos para Entregar

1. **Preparar el archivo ZIP:**
   - Asegurarse de que el ZIP tiene el nombre correcto
   - Verificar que contiene todos los archivos necesarios
   - Probar que el ZIP se extrae correctamente

2. **Subir a la plataforma de la UVM:**
   - Acceder al curso FrontEndIVIVFI2026C
   - Ir a la secci\u00f3n de E-Actividad 2.1
   - Buscar el enlace o formulario de entrega
   - Subir el archivo `cedula_nombre.zip`

3. **Verificar la entrega:**
   - Descargar el archivo subido para verificar
   - Asegurarse de que no est\u00e1 corrupto
   - Verificar que se puede abrir y que los archivos est\u00e1n \u00edntegros

4. **Guardar el comprobante:**
   - Tomar una captura de pantalla de la confirmaci\u00f3n de entrega
   - Guardar el correo de confirmaci\u00f3n (si se env\u00eda)
   - Anotar la fecha y hora de entrega

---

## 📤 Publicaci\u00f3n en GitHub

### Instrucciones para Publicar

**⚠️ ADVERTENCIA IMPORTANTE:**

Antes de publicar en GitHub, **VERIFICAR** que:

1. La identidad de Git est\u00e1 configurada correctamente como `mmorfe-engineer`
2. El gh CLI est\u00e1 autenticado como `mmorfe-engineer`
3. No se est\u00e1 viola la pol\u00edtica de identidad del proyecto

**Si NO puedes verificar esto, NO publiques en GitHub.**

#### Pasos para Publicar

1. **Inicializar Git (si no est\u00e1 inicializado):**
   ```bash
   cd renaissance-html5-uvm-e2
   git init
   ```

2. **Configurar identidad local (VERIFICAR ANTES):**
   ```bash
   # Verificar configuraci\u00f3n actual
   git config user.name
   git config user.email
   
   # Si no es mmorfe-engineer, configurar:
   git config user.name "mmorfe-engineer"
   git config user.email "morfemartin@users.noreply.github.com"  # o el email correcto
   ```

3. **A\u00f1adir todos los archivos:**
   ```bash
   git add .
   ```

4. **Hacer el primer commit:**
   ```bash
   git commit -m "feat: implement Renaissance HTML5 academic website"
   ```

5. **A\u00f1adir remote (VERIFICAR URL):**
   ```bash
   git remote add origin https://github.com/mmorfe-engineer/renaissance-html5-uvm-e2.git
   git remote -v  # VERIFICAR que apunta a mmorfe-engineer
   ```

6. **Push a main:**
   ```bash
   git push -u origin main
   ```

7. **Verificar en GitHub:**
   - Abrir https://github.com/mmorfe-engineer/renaissance-html5-uvm-e2
   - Verificar que todos los archivos est\u00e1n presentes
   - Verificar autor de commits (debe ser mmorfe-engineer)
   - Verificar que no hay coauthors

---

## 📝 Declaraci\u00f3n de Autenticidad

### Plantilla de Declaraci\u00f3n

**NOTA:** Esta declaraci\u00f3n debe ser completada y firmada por el estudiante. Este documento NO debe ser incluido en el ZIP, sino entregado por separado si es requerido.

```
DECLARACI\u00d3N DE AUTENTICIDAD

Yo, [Nombre Completo], con c\u00e9dula de identidad n\u00bamero [N\u00bamero de C\u00e9dula], 
declaro bajo juramento que:

1. El trabajo presentedo como "Renaissance HTML5 Edition" para la E-Actividad 2.1 
   del curso FrontEndIVIVFI2026C es de mi exclusiva autor\u00eda.

2. He le\u00eddo y comprendo los requisitos de la actividad establecidos por 
   el Prof. Anggelo Huz.

3. El c\u00f3digo fuente, dise\u00f1o, contenido y documentaci\u00f3n han sido 
   desarrollados por m\u00ed personalmente, con la \u00fanica excepci\u00f3n de:
   - [ ] Ninguno (100% original)
   - [ ] Los siguientes elementos con atribuci\u00f3n:
     - Fuentes tipogr\u00e1ficas: Inter y Lora de Google Fonts (SIL OFL 1.1)
     - [Otro, especificar: _______________]

4. No he copiado c\u00f3digo de internet en m\u00e1s de un 50% del total.

5. No he copiado c\u00f3digo de otros estudiantes o trabajos previos.

6. Todas las referencias externas han sido debidamente citadas en formato APA 
   en el archivo REFERENCIAS.md.

7. El proyecto cumple con todos los requisitos t\u00e9cnicos y acad\u00e9micos 
   especificados para esta actividad.

8. Entiendo que la presentaci\u00f3n de trabajo ajeno como propio constituents 
   una violaci\u00f3n de las normas acad\u00e9micas de la UVM.

Firma: ___________________________
Fecha: _______ / _______ / _______
Nombre: ___________________________
C\u00e9dula: ___________________________
```

---

## 📅 Calendario y Fechas

| Fecha | Actividad | Estado |
|-------|-----------|--------|
| 16 de octubre de 2026 | Desarrollo y validaci\u00f3n | ⏳ En progreso |
| 17 de octubre de 2026, 23:59 | Entrega final | ❌ Pendiente |
| 18 de octubre de 2026 | Revisi\u00f3n y retroalimentaci\u00f3n | ⏳ Pendiente |

**Zona horaria:** GMT-4 (Venezuela)

---

## 💡 Recomendaciones Finales

1. **Reemplazar los archivos placeholders:**
   - Crear/obtener archivos reales de audio y video
   - Verificar que los codecs sean compatibles
   - Probar la reproducci\u00f3n en m\u00fasltiples navegadores

2. **Validar con herramientas oficiales:**
   - Usar https://validator.w3.org/nu/ para HTML
   - Usar https://jigsaw.w3.org/css-validator/ para CSS
   - Usar herramientas de accesibilidad como WAVE o aXe

3. **Probar en m\u00fasltiples navegadores:**
   - Chrome/Chromium
   - Firefox
   - Safari (si es posible)
   - Edge

4. **Probar en dispositivos m\u00f3viles:**
   - Usar el modo device toolbar en Chrome DevTools
   - Probar en un tel\u00e9fono real si es posible

5. **Verificar el ZIP:**
   - Extraer el ZIP en una nueva ubicaci\u00f3n
   - Abrir index.html directamente con el navegador
   - Verificar que todos los enlaces funcionan
   - Verificar que el CSS se carga correctamente
   - Verificar que las im\u00e1genes se muestran

6. **Guardar copias de seguridad:**
   - Guardar una copia del proyecto completo
   - Guardar una copia del ZIP final
   - Guardar el comprobante de entrega

---

## ⚠️ Errores Comunes a Evitar

| Error | Consecuencia | C\u00f3mo Evitar |
|-------|--------------|--------------|
| Archivos corruptos | Multimedia no funciona | Verificar integridad de los archivos |
| Olvidar validar HTML | Errores de sintaxis | Usar W3C Nu Checker |
| IDs duplicados | HTML inv\u00e1lido | Verificar con herramientas |
| Enlaces rotos | Navegaci\u00f3n no funciona | Probar todos los enlaces |
| No incluir .gitignore | Archivos no deseados | Verificar contenido del ZIP |
| Nombre de ZIP incorrecto | Entrega rechazada | Usar formato cedula_nombre.zip |
| Exceder l\u00edmite de tiempo | P\u00e9rdida de puntos | Mantener video < 10 minutos |
| Plagio | Sanci\u00f3n acad\u00e9mica | Crear trabajo original |
| No citar fuentes | P\u00e9rdida de puntos | Incluir REFERENCIAS.md |

---

## 📞 Contacto y Soporte

Para preguntas sobre la entrega:

1. **Profesor:** Prof. Anggelo Huz
   - Contactar a trav\u00e9s de los canales oficiales del curso

2. **Asistente:** (Si aplica)

3. **Plataforma UVM:**
   - Revisar la secci\u00f3n de anuncios del curso
   - Verificar el foro de discusi\u00f3n

**Nota:** Este proyecto ha sido desarrollado como apoyo para la E-Actividad 2.1. El estudiante es responsable de:
- Verificar todos los requisitos
- Realizar las pruebas necesarias
- Entregar el trabajo a tiempo
- Asegurar la autenticidad del contenido

---

## 🎯 Checklist Final Pre-Entrega

- [ ] Todos los archivos HTML existen y son v\u00e1lidos
- [ ] CSS existe y funciona correctamente
- [ ] Todos los assets (im\u00e1genes, audio, video) est\u00e1n en su lugar
- [ ] El formulario funciona (validaci\u00f3n nativa)
- [ ] La tabla se muestra correctamente
- [ ] La navegaci\u00f3n entre p\u00e1ginas funciona
- [ ] Todos los enlaces son relativos y funcionan
- [ ] El ZIP tiene el nombre correcto (cedula_nombre.zip)
- [ ] El ZIP contiene todos los archivos necesarios
- [ ] El ZIP NO contiene el directorio .git/
- [ ] He probado el proyecto en al menos 2 navegadores
- [ ] He verificado la accesibilidad b\u00e1sica
- [ ] He revisado la ortograf\u00eda y gram\u00e1tica
- [x] He integrado los archivos de multimedia definitivos
- [ ] Estoy listo para entregar

**Si todos los puntos est\u00e1n marcados, \u00a1est\u00e1s listo para entregar!**

---

*Documento actualizado: 16 de octubre de 2026*
