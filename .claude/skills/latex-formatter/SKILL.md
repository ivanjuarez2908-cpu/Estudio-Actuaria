---
name: latex-formatter
description: Da formato LaTeX formal a borradores de ecuaciones o notas manuscritas.
allowed-tools: [Read, Write]
---
Transforma el texto o borrador matemático proporcionado en LaTeX limpio:
1. Usa sintaxis estándar (`\begin{align*}`, `\mathbb{R}`, `\forall`, `\exists`, etc.).
2. Asegura el correcto uso de delimitadores ajustables (`\left( ... \right)`).
3. Devuelve únicamente el código de LaTeX listo para copiar y pegar en Overleaf o Markdown.
