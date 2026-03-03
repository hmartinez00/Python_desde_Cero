```markdown
# Metaprompt para Generar Notebooks .ipynb para Módulos del Curso de Python

Este metaprompt es un template que puedes copiar y pegar en un LLM (como Grok o ChatGPT) para generar un archivo .ipynb por módulo. El prompt toma como input la data de un módulo específico del JSON (por ejemplo, copias las claves como "title", "topics", etc., y las pegas en el placeholder correspondiente).

**Instrucciones de Uso:**
1. Copia todo el texto del metaprompt a continuación.
2. Edita los placeholders `[INSERTE DATA DEL MÓDULO AQUÍ]` con la información real del módulo (por ejemplo, para Módulo 1, pega el JSON del módulo 1 del archivo anterior).
3. Ejecuta el prompt en un LLM.
4. El output del LLM será un JSON que representa el archivo .ipynb. Copia ese JSON y guárdalo en un archivo con extensión `.ipynb` (usa un editor de texto o VS Code).
5. Sube el `.ipynb` a Google Drive y ábrelo en Colab – será reconocido automáticamente como un notebook interactivo.
6. Si necesitas ajustes, edita el metaprompt (es legible y en Markdown para fácil manipulación).

**Notas Adicionales:**
- El metaprompt asegura que el .ipynb incluya: 
  - Celdas markdown para explicaciones detalladas y recursos.
  - Celdas de código para demostraciones (ejemplos ejecutables).
  - Retos progresivos: Encadenados (variables de un reto alimentan al siguiente), con placeholders (# Tu código aquí), asserts suaves para feedback (no errores fatales), hints en celdas colapsadas (usando #@markdown en Colab para ocultar), resets opcionales, fallbacks (datos dummy), y soluciones parciales al final.
- Mantiene exigencia: Retos requieren aplicación real, pero con mitigaciones para no frustrar (e.g., mensajes amigables como "¡Intenta de nuevo! Revisa la pista.").
- Estructura general del .ipynb generado: Metadata estándar de Colab, celdas secuenciales lógicas, y un reto final integrador que usa elementos previos.
- Asegura compatibilidad con Python 3.12+ en Colab.

---

**Metaprompt Template:**

Eres un generador experto de notebooks Jupyter (.ipynb) para cursos educativos de programación en Python. Tu tarea es crear un archivo .ipynb completo y válido, reconocible por Google Colab, basado en la data de un módulo de curso proporcionada.

**Especificaciones Clave para el Notebook:**
- **Estructura General:**
  - Metadata: Incluye kernel Python 3, con display_name "Python 3" y metadata para Colab (colab provenance vacío).
  - Celdas: Mezcla de markdown (para explicaciones, títulos, recursos) y code (para demos, retos).
  - Idioma: Explicaciones en español (como el curso), código en inglés estándar.
  - Título del Notebook: "Módulo [module_id]: [title] - Curso Python de Cero a Pro".
- **Contenido Explicativo:**
  - Celda inicial markdown: Introducción al módulo, objetivos (basado en topics), tiempo estimado, y lista de recursos.
  - Por cada topic: Celda markdown con explicación clara, concisa y educativa (2-4 párrafos), seguida de celda code de demostración.
- **Celdas de Demostración:**
  - Código ejecutable simple que ilustra el topic (e.g., para variables: asignación y print).
  - Incluir comentarios en el código (# Explicación aquí).
  - Usar print() para outputs visibles.
- **Retos Progresivos:**
  - Basado en "exercises" y "project": Crea 2-4 retos por módulo, encadenados (e.g., variable de reto 1 se usa en reto 2).
  - Cada reto: Celda markdown con instrucciones, seguida de celda code con placeholder (# Tu código aquí), y una celda de validación con assert suave (try/except con print de feedback amigable, e.g., "¡Bien! Sigue." o "Intenta de nuevo: [pista]").
  - Reto final: Integrador, usando elementos previos, que alimenta al "project".
  - Safeguards/Mitigaciones (para no ser agresivo pero mantener exigencia):
    - Hints: Celda markdown colapsada (#@markdown Pista: [hint simple]).
    - Soluciones Parciales: Al final del notebook, una sección colapsada con código de ejemplo (no completo, para fomentar esfuerzo).
    - Resets: Celda opcional al inicio de retos para reset variables (e.g., del mi_variable if exists).
    - Fallbacks: En retos encadenados, opción para definir dummy si previo falla (e.g., "Si no tienes la variable, define mi_lista = [1,2,3] aquí").
    - Feedback: Asserts no bloquean; usan print("Éxito!") o print("Revisa: [error amigable]").
  - Exigencia: Retos requieren código funcional para "desbloquear" (via print de confirmación), pero con guías para retención.
- **Proyecto:**
  - Sección final: Markdown con instrucciones del project, celda code para implementación (placeholder), y validación simple.
- **Challenges Description:** Integra la descripción y mitigaciones proporcionadas.
- **Output Formato:** Genera SOLO un JSON válido que represente el .ipynb completo (no texto extra). Estructura estándar: {"nbformat": 4, "nbformat_minor": 0, "metadata": {...}, "cells": [array de celdas]}.
  - Cada celda: {"cell_type": "markdown" o "code", "metadata": {}, "source": ["línea1\n", "línea2\n"], "execution_count": null para code, "outputs": []}.

**Data del Módulo de Input:**
[INSERTE DATA DEL MÓDULO AQUÍ]
(Ejemplo: {
  "module_id": 1,
  "title": "Fundamentos Básicos",
  "topics": ["Instalación via Colab...", "..."],
  "resources": ["Documentación oficial..."],
  "exercises": ["Calculadora simple..."],
  "project": "Tip Calculator...",
  "challenges": {
    "description": "Retos progresivos: ...",
    "mitigations": ["Hints en celdas colapsadas...", "..."]
  },
  "estimated_time": "5 horas."
})

Genera el .ipynb JSON basado en esto.

---
```