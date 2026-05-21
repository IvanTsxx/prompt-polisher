# prompt-polisher

A meta-prompt that transforms messy, ambiguous user prompts into clean, well-structured prompts following Anthropic's official prompt engineering best practices.

Un meta-prompt que transforma prompts desordenados y ambiguos en prompts limpios y bien estructurados siguiendo las mejores prácticas oficiales de prompt engineering de Anthropic.

## What it does / Qué hace

Takes a raw user prompt as input and returns a refined version that applies:

- **XML tag delimiters** for clear section boundaries
- **Layered structure**: role, context, instructions, examples, output format
- **Dynamic variables** marked with `{{VARIABLE}}` placeholders
- **Few-shot examples** when the task requires consistent formatting
- **Repeated critical instructions** for long prompts
- **Clear role establishment** at the start

The original user intent is always preserved — the meta-prompt restructures, it doesn't expand scope.

Toma un prompt crudo del usuario y devuelve una versión refinada que aplica delimitadores XML, estructura en capas (rol, contexto, instrucciones, ejemplos, formato), variables dinámicas marcadas con `{{VARIABLE}}`, ejemplos few-shot cuando la tarea lo requiere, y repetición de instrucciones críticas. La intención original del usuario siempre se preserva.

## Files / Archivos

- `prompt-polisher.en.md` — English version
- `prompt-polisher.es.md` — Versión en español

## Usage / Uso

Replace `{{PROMPT}}` at the end of the meta-prompt with the messy prompt you want to improve, then send it to Claude.

Reemplazá `{{PROMPT}}` al final del meta-prompt con el prompt sucio que querés mejorar, y enviáselo a Claude.

## Based on / Basado en

Anthropic's prompt engineering guidelines presented by their engineering team, covering prompt structure, XML organization, few-shot examples, and information layering.