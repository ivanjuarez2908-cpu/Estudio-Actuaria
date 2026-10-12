# Configuración Completa de Claude Code - Actuaría (FES Acatlán)

Este documento contiene la estructura de archivos necesaria para configurar tu entorno de trabajo de estudio de Actuaría con Claude Code.

---

## 1. Estructura de Carpetas

Crea la siguiente estructura dentro de tu carpeta principal de estudio (por ejemplo, `Estudio-Actuaria`):

```text
Estudio-Actuaria/
├── .claude/
│   └── skills/
│       ├── proof-checker.md
│       ├── summary-concept.md
│       └── latex-formatter.md
├── CLAUDE.md
├── Calculo-I/
│   ├── referencias/
│   └── ejercicios/
├── Algebra/
│   ├── referencias/
│   └── ejercicios/
└── Geometria-Analitica/
    ├── referencias/
    └── ejercicios/
```

---

## 2. Contenido de los Archivos

### Archivo 1: `CLAUDE.md`
*Ubicación: `Estudio-Actuaria/CLAUDE.md`*

```markdown
# Contexto del Usuario
- Estudiante de primer semestre de Actuaría en FES Acatlán.
- Asignaturas principales: Cálculo I, Álgebra, Geometría Analítica.
- Enfoque: Rigor matemático, demostraciones formales y resolución sistemática de problemas.
- Atleta de alto rendimiento (MMA/BJJ): valora respuestas concisas, estructuradas y sin palabrería.

# Reglas de Interacción
1. **Directo al punto:** Respuestas cortas, claras y bien estructuradas.
2. **Método Socrático para tareas:** No entregues respuestas completas de inmediato en ejercicios de práctica; guía con preguntas clave o señala el axioma/teorema necesario.
3. **Formato:** Usa notación LaTeX estándar para matemáticas ($inline$ y $$display$$).
4. **Verificación:** Prioriza la detección de errores de rigor deductivo o supuestos implícitos en las demostraciones.
```

---

### Archivo 2: `.claude/skills/proof-checker.md`
*Ubicación: `Estudio-Actuaria/.claude/skills/proof-checker.md`*

```markdown
---
name: proof-checker
description: Evalúa una demostración matemática paso a paso buscando vacíos lógicos o falta de rigor.
allowed-tools: [Read, Grep]
---
Revisa la demostración o argumento matemático del usuario aplicando el rigor de análisis universitario:
1. **Hipótesis y Conclusión:** Identifica ambas explícitamente.
2. **Paso a Paso:** Revisa cada deducción lógica.
3. **Puntos Críticos:** Detecta el uso no justificado de axiomas, teoremas o propiedades (ej. división entre cero, asumir acotamiento no probado, etc.).
4. **Retroalimentación:** Marca los errores o vacíos en la deducción y formula preguntas para que el usuario pueda corregirlos.
```

---

### Archivo 3: `.claude/skills/summary-concept.md`
*Ubicación: `Estudio-Actuaria/.claude/skills/summary-concept.md`*

```markdown
---
name: summary-concept
description: Convierte un texto académico o fragmento de libro en una ficha de estudio resumida.
allowed-tools: [Read]
---
Sintetiza el contenido analizado en el siguiente formato estricto:
1. **Definiciones:** Conceptos clave en notación matemática formal.
2. **Teoremas / LeMAS:** Enunciados exactos con sus condiciones iniciales.
3. **Intuición:** Explicación conceptual breve en 2-3 oraciones.
4. **Contraejemplos / Casos Límite:** Escenarios donde el teorema o propiedad falla si se omite una hipótesis.
5. **Autoevaluación:** 3 preguntas rápidas para comprobar la comprensión.
```

---

### Archivo 4: `.claude/skills/latex-formatter.md`
*Ubicación: `Estudio-Actuaria/.claude/skills/latex-formatter.md`*

```markdown
---
name: latex-formatter
description: Da formato LaTeX formal a borradores de ecuaciones o notas manuscritas.
allowed-tools: [Read, Write]
---
Transforma el texto o borrador matemático proporcionado en LaTeX limpio:
1. Usa sintaxis estándar (`\begin{align*}`, `\mathbb{R}`, `\forall`, `\exists`, etc.).
2. Asegura el correcto uso de delimitadores ajustables (`\left( ... \right)`).
3. Devuelve únicamente el código de LaTeX listo para copiar y pegar en Overleaf o Markdown.
```

---

## 3. Script para Crear Todo Automáticamente (Opcional)

Si estás en Mac o Linux, puedes abrir la terminal en tu carpeta de trabajo y ejecutar el siguiente comando para generar toda la estructura de golpe:

```bash
mkdir -p .claude/skills Calculo-I/referencias Calculo-I/ejercicios Algebra/referencias Algebra/ejercicios Geometria-Analitica/referencias Geometria-Analitica/ejercicios
```