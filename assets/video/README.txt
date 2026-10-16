ASSETS/VIDEO - Instrucciones
================================

Este directorio debe contener los archivos de video:
  - flujo-educativo.mp4
  - flujo-educativo.es.vtt (subtítulos, ya creado)

El archivo de video debe ser:
  - Formato: MP4 (MPEG-4 Part 14)
  - Codec de video: H.264 (AVC)
  - Codec de audio: AAC
  - Resolución: 600x400px o similar
  - Duración: 1 minuto 15 segundos
  - Tamaño recomendado: ~5.2 MB
  - Poster: assets/images/educational-workflow.svg (ya configurado)

CONTENIDO RECOMENDADO PARA EL VIDEO:
------------------------------------
Animación o grabación que muestre:
1. Paso 1: Seleccionar documento (icono de libro)
2. Paso 2: Elegir perfil (icono de usuario)
3. Paso 3: Seleccionar formato (icono de lista)
4. Paso 4: Recibir material adaptado (icono de descarga)

El video debe incluir:
- Narración en español sincronizada con los subtítulos
- Visuales claros y educativos
- Formato compatible con el elemento <video> de HTML5

HERRAMIENTAS PARA CREAR EL VIDEO:
---------------------------------
1. OBS Studio (gratis, para grabación de pantalla)
2. Blender (gratis, para animación 3D/2D)
3. OpenShot / Shotcut (gratis, editores de video)
4. Canva (en línea, para animaciones simples)
5. Adobe Premiere Pro / After Effects
6. Herramientas de animación como Lottie

CONVERSIÓN A MP4 H.264:
------------------------
Si necesitas convertir un video a MP4 con H.264:

Usando ffmpeg (recomendado):
  ffmpeg -i input.mp4 -c:v libx264 -c:a aac -strict experimental -b:v 1000k -s 600x400 flujo-educativo.mp4

Usando HandBrake (interfaz gráfica):
  - Selecciona el archivo de entrada
  - Elige formato MP4
  - Codec de video: H.264 (x264)
  - Codec de audio: AAC
  - Resolución: 600x400
  - Bitrate de video: ~1000 kbps

NOTA: El archivo flujo-educativo.mp4 actual es un marcador. 
Debes reemplazarlo con tu propio video.
