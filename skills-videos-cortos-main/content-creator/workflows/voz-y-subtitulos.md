# Voz y subtítulos

Entrada: una grabación y una carpeta de proyecto acordada. Sigue la skill [voz-whisper](../../skills/voz-whisper/SKILL.md); conserva siempre el original y no instales ni descargues herramientas por defecto.

## Elegir el alcance

- **Solo limpiar:** `entrada` y `limpiar`; comparar a volumen parecido y entregar `01-eq.wav`. Sin cortes ni transcripción.
- **Voz completa:** la cadena por etapas de la skill, revisando la transcripción antes de cortar. Conserva pausas expresivas: las del humor no son material sobrante.
- **Solo subtítulos:** partir de la voz vigente y sus palabras; no reprocesar el audio.

La petición del autor determina el alcance; no pedir que elija un modo si ya quedó claro.

## Subtítulos

El script entrega tiempos por palabra: **no genera SRT, agrupación de frases ni diseño visual**. Decide el entregable (SRT, subtítulos en el video o ambos).

1. Partir de la voz vigente y sus palabras revisadas.
2. Agrupar por sentido y lectura; comprobar puntuación, nombres y pausas.
3. Para SRT: bloques con tiempos positivos, ordenados, sin solapes accidentales y dentro de la duración.
4. Elegir encuadre y estilo en el sketchbook; no animar cada palabra por defecto.
5. Revisar con la voz y en tamaño de teléfono. Registrar la versión de audio usada.

Salida: rutas de voz, palabras y subtítulos generados; qué se escuchó y qué queda pendiente.
