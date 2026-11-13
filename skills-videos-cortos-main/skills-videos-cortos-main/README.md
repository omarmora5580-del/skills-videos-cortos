# Skills para videos cortos

Un paquete en español para pensar, escribir, grabar y animar videos cortos con un agente de IA (Claude Code, OpenCode u otro que lea Markdown). Sirve para cuestionar guiones, preparar voz con Whisper y construir animaciones con intención en Remotion.

Salió de mi propio taller de videos. Aquí van las skills y los workflows; no incluye proyectos, grabaciones, música, efectos, modelos ni bibliotecas privadas.

## Contenido

### Skills (`skills/`)

| Skill | Para qué sirve |
|---|---|
| [cuestionar-guion](skills/cuestionar-guion/SKILL.md) | Crítica editorial franca y comparación entre episodios, sin prometer viralidad |
| [voz-whisper](skills/voz-whisper/SKILL.md) | Limpieza con FFmpeg, transcripción local con whisper.cpp, cortes de silencios y masterización |
| [referencias-opus](skills/referencias-opus/SKILL.md) | Convertir referencias de catálogos (Awesome Opus u otros) en escenas propias realizables |
| [motion](skills/motion/SKILL.md) | Diseño y revisión de animación en Remotion: causalidad, énfasis y animación por frame |
| [sonido](skills/sonido/SKILL.md) | Efectos, sincronía y mezcla con una biblioteca de audio autorizada |

### Content creator (`content-creator/`)

Un espacio de trabajo por módulos: entras por idea, guion, voz, sketchbook visual o producción sin recorrer todas las etapas. Incluye workflows, plantillas de notas y los [criterios editoriales con sus fuentes](content-creator/criterios-de-guion.md). Ver [content-creator/README.md](content-creator/README.md).

## Instalación

**Claude Code:** copia las carpetas de `skills/` a `~/.claude/skills/` (para todos tus proyectos) o a `.claude/skills/` dentro de tu proyecto. Conserva las subcarpetas; voz-whisper necesita `scripts/voz.py`.

```bash
git clone https://github.com/JustCarlos30/skills-videos-cortos.git
cp -r skills-videos-cortos/skills/* ~/.claude/skills/
```

**Otros agentes:** pídele que lea directamente el `SKILL.md` que necesites.

Para el content creator, abre tu agente dentro de `content-creator/`: su `AGENTS.md` explica cómo trabajar.

## Ejemplos

- «Destroza este guion y compáralo con el anterior».
- «Prepara esta toma con voz-whisper; conserva mis pausas cómicas».
- «Adapta una técnica de este enlace al momento en que explico los tokens».
- «Anima esta escena en mi proyecto Remotion».
- «Mezcla estos efectos debajo de la voz».
- «Rebotemos un guion: traigo esta idea…».

## Voz: requisitos

Python 3 con NumPy, FFmpeg/ffprobe, `whisper-cli` de [whisper.cpp](https://github.com/ggml-org/whisper.cpp) y un modelo GGML multilingüe local. No descarga modelos ni instala nada; no requiere API keys.

Prepara una carpeta de proyecto con un `video.json` (puede contener `{}`) y pásala con `--project-dir`. El script genera intermedios en `.work/voz`, audio en `public/` y tiempos por palabra en `src/`. La transcripción está configurada para español. El preset requiere escucha y puede necesitar ajustes según la toma. No genera SRT ni incluye un proyecto Remotion.

## Recursos externos

No se incluye el catálogo Awesome Opus, clips de terceros, fuentes, música, efectos ni modelos. Usa recursos cuyos permisos permitan el uso previsto. La licencia de este repositorio no cubre recursos externos.

## Validación

Las cinco skills pasaron un validador de estructura. El script de voz pasó una prueba sintética de entrada, limpieza, detección de silencios, corte, masterización, entrega y rechazo de sobrescritura. Eso no valida la transcripción real con Whisper, la lectura de AUP3, la calidad perceptual ni el comportamiento de cada agente.

## Relación con el taller

Estas son las versiones genéricas. El [taller-videos](https://github.com/JustCarlos30/taller-videos) lleva en `.claude/skills/` sus propias variantes, atadas a su motor (MOTION.md, asset-vault, `tools/voz.py`). Si mejoras una regla aquí, decide aparte si aplica también allí; no son copias que se sincronicen.

## Licencia

[MIT](LICENSE).
