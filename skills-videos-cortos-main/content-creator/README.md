# Content creator

Un espacio para pensar, preparar y producir videos cortos por módulos, conversando con un agente (Claude Code, OpenCode u otro que lea Markdown). No hace falta recorrer todas las etapas: entras por la que necesitas.

## Entrar por lo que necesitas

| Lo que dices | Qué hacemos | Dónde paramos |
|---|---|---|
| «Traigo esta idea…» / «Rebotemos un guion…» | [Ideas y guion](workflows/ideas-y-guion.md): conversar, encontrar el asunto y probar un recorrido | Mapa de la idea; guion completo cuando lo pidas |
| «Revisa / destroza este guion» | Skill [cuestionar-guion](../skills/cuestionar-guion/SKILL.md) | Veredicto y cambios prioritarios |
| «Prepara esta grabación» | [Voz y subtítulos](workflows/voz-y-subtitulos.md) con la skill voz-whisper | Voz y palabras verificadas; subtítulos si los pides |
| «Abramos el sketchbook» | [Sketchbook visual](workflows/sketchbook-visual.md): alternativas, secuencias y cuadros clave en el chat | Diseño elegido; puede quedarse como boceto |
| «Produzcamos estas secuencias» | [Producción](workflows/produccion.md) con las skills motion y sonido | Vista previa; render cuando lo solicites |

Un recorrido posible es **idea → voz → sketchbook → producción**, pero también valen **voz lista → sketchbook** o **corrección → export**. Los tiempos de un boceto se ajustan al cerrar la voz.

## Qué se guarda

- `piezas/<nombre-de-trabajo>/guion.md` y `sketchbook.md`: notas que el agente mantiene para retomar. Solo la que haga falta en cada etapa. Plantillas en [plantillas/](plantillas/).
- [criterios-de-guion.md](criterios-de-guion.md): bases (con fuentes) de los criterios editoriales y sus límites. Consulta opcional.

El código, audio y exports de producción viven en tu proyecto de video (por ejemplo, Remotion), no aquí. Las notas enlazan esos archivos en vez de duplicarlos.

## Empezar

Abre tu agente en esta carpeta (lee `AGENTS.md`) y di algo como:

- «Rebotemos un guion: traigo esta idea…»
- «Abramos sketchbook: me interesa contar ___; lo que me parece raro/chistoso es ___».

El agente devuelve una lectura de tu intención y una propuesta pequeña; una secuencia o decisión por ronda.
