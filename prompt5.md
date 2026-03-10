# Prompt para modulo5_archivos_excepciones.ipynb

**Meta**: transformar el notebook en un módulo de archivos y excepciones que sea:
- claro para principiantes,
- estructurado de forma consistente con los módulos anteriores,
- con práctica guiada, validación y navegación interna.

## 1) Revisión inicial
- Leer todo el notebook.
- Identificar secciones clave (`##`, `###`).
- Detectar temas principales (lectura/escritura archivos, modos `r/w/a`, manejo de excepciones, `with`, `raise`, `try/except/else/finally`).

## 2) Navegación y anclas
- Insertar en la introducción:
  - [Introducción](#mod5)
  - [Topic 1: Lectura/escritura de archivos](#t1)
  - [Topic 2: Modos y clasicos](#t2)
  - [Topic 3: Manejo de excepciones](#t3)
  - [Topic 4: Context manager `with`](#t4)
  - [Retos Progresivos](#retos)
  - [Proyecto](#proyecto)
  - [Glosario](#glosario)
  - [Resumen](#resumen)
- Agregar anclas equivalentes (`<a id="t1"></a>`, etc.).

## 3) Secciones teóricas mínimas
**Topic 1** (Archivos):
- `open(path, mode)`.
- `read()`, `readline()`, `readlines()`, `write()`.
- `close()`.

**Topic 2** (modos):
- `r`, `w`, `a`, `x`, `rb`, `wb`.
- riesgos: sobrescritura y fileNotFound.

**Topic 3** (excepciones):
- `try`/`except` básico.
- `except (IOError, OSError)`.
- `else` y `finally`.
- `raise` manual para validaciones.

**Topic 4** (`with`):
- contexto libre de fugas.
- equivalencia con `open(...); finally close()`.
- ejemplos con `with open(...) as f:`.

## 4) Retos progresivos
- Reto 1: crear archivo, escribir líneas, leer y mostrar contenido.
- Reto 2: manejo de errores con `try/except` cuando el archivo no existe.
- Reto 3: función que recibe nombre de archivo y retorna conteo de palabras, con `raise` en inputs inválidos.
- Reto 4: actualizar archivo con `a` y luego comprobar append.
- Incluir validación con `assert` y fallback simple.

## 5) Proyecto
- Nombre: "Administrador de tareas en archivo".
- Requisitos:
  - guardar tareas en archivo de texto,
  - listar tareas,
  - completar tarea y guardar cambios,
  - manejo de excepciones de archivo.
- Validación:
  - asserts de contenido esperado, funciones modulares.

## 6) Glosario
- Definir: `open`, `read`, `write`, `close`, `with`, `try`, `except`, `finally`, `raise`, `FileNotFoundError`, `IOError`, `OSError`.
- Referencia oficial:
  - https://docs.python.org/es/3/tutorial/inputoutput.html#reading-and-writing-files

## 7) Cierre con “¿Qué aprendimos?”
- Resumir: modos de archivo, uso de `with`, excepciones, robustez.

## 8) Formato
- Mantener `VSCode.Cell` con `language` correcto.
- No borrar `id` existentes.
- Evitar notas cortas `#@markdown`; usar explicaciones claras y completas.

## 9) Resultado de ejecución
- Devolver:
  - resumen de cambios
  - diff / patch
  - checklist de puntos incorporados
