# Prompt para modulo4_funciones.ipynb

**Meta**: transformar el notebook en un módulo de funciones que sea:
- accesible para principiantes absolutos,
- estructurado uniformemente con los módulos anteriores,
- completo en teoría, ejemplos y ejercicios,
- con navegación interna, glosario y cierre con resumen.

## 1) Revisión inicial
- Leer todo el notebook.
- Identificar secciones clave (`##`, `###`).
- Detectar temas principales (definición, parámetros, returns, scope, recursión, *args/**kwargs, lambda, docstrings, modularidad).

## 2) Navegación y anclas
- Insertar en la introducción:
  - [Introducción](#mod4)
  - [Topic 1: Definición + llamadas](#t1)
  - [Topic 2: Parámetros y return](#t2)
  - [Topic 3: Scope / variable locals/globals](#t3)
  - [Topic 4: Funciones avanzadas (args/kwargs, lambda, map/filter)](#t4)
  - [Retos Progresivos](#retos)
  - [Proyecto](#proyecto)
  - [Glosario](#glosario)
  - [Resumen](#resumen)
- Agregar anclas equivalentes (`<a id="t1"></a>`, etc.).

## 3) Secciones teóricas mínimas
**Topic 1** (qué es función):
- `def nombre(args):`
- `return`
- llamada `mi_funcion()`
- ventajas (reutilización, legibilidad, pruebas).

**Topic 2** (parámetros):
- parámetros posicionales y nombrados.
- valores por defecto.
- retorno simple.
- ejemplos incluyendo `None`.

**Topic 3** (scope):
- local vs global.
- `global` keyword.
- variable shadowing.
- ejercicio en pequeño código.

**Topic 4** (avanzado):
- `*args`, `**kwargs`.
- lambda + ejemplo `map/filter`.
- función como objeto (asignar, pasar a otra).
- docstring + `help(func)`.

## 4) Retos progresivos (3-4 retos)
- Reto 1: función que calcule área de rectángulo; usa argumentos posicionales.
- Reto 2: función que reciba lista y devuelva suma, con argumento opcional `incluir_negativos=True`.
- Reto 3: función que use `*args` para multiplicar valores.
- Reto 4: función tipo "login" con archivos o diccionarios y condicionales.
- Añadir fallback dummy y validaciones suaves (`assert`, mensaje claro).

## 5) Proyecto
- Nombre: “Juego de funciones” o “Mini-librería de utilidades”.
- Requisitos:
  - definir 3-4 funciones con diferentes tipos de argumentos.
  - llamar las funciones desde un bloque principal.
  - usar `lambda` + `map`/`filter` si se puede.
- Validación:
  - `assert` de salida esperada.
  - comprobación de docstring no vacío.

## 6) Glosario
- Definir:
  - función, parámetro, argumento, retorno.
  - scope (local/global).
  - lambda.
  - *args, **kwargs.
  - modularidad.
- Referencia oficial:
  - https://docs.python.org/es/3/tutorial/controlflow.html#defining-functions
  - https://docs.python.org/es/3/tutorial/controlflow.html#more-on-defining-functions

## 7) Cierre con “¿Qué aprendimos?”
- Lista de puntos clave (igual que módulos anteriores).
- Pregunta de reflexión: “¿Qué tipo de función usarías para...?”

## 8) Formato
- Mantener en `VSCode.Cell` con `language` correcto.
- No borrar `id` existentes.
- Evitar `#@markdown` críptico; usar explicaciones enteras.
- Mantener títulos y estilos consistentes con módulo previo.

## 9) Resultado de la ejecución
- Return:
  - resumen de cambios
  - diff / patch alteraciones
  - checklist de puntos incorporados
