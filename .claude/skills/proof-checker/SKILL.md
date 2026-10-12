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
