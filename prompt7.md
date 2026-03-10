# Prompt para modulo7_bibliotecas_practicas.ipynb

**Meta**: transformar el notebook en un módulo de bibliotecas prácticas que sea educativo y operacional, consistente con estilo de módulos precedentes.

## 1) Revisión inicial
- Leer todo el notebook.
- Identificar secciones clave (`##`, `###`).
- Detectar temas principales: uso de requests/JSON, pandas, matplotlib/seaborn, openpyxl, APIs, manejo de dependencias.

## 2) Navegación y anclas
- Insertar en la introducción:
  - [Introducción](#mod7)
  - [Topic 1: HTTP y APIs](#t1)
  - [Topic 2: pandas](#t2)
  - [Topic 3: visualización](#t3)
  - [Topic 4: manejo de archivos con bibliotecas](#t4)
  - [Retos Progresivos](#retos)
  - [Proyecto](#proyecto)
  - [Glosario](#glosario)
  - [Resumen](#resumen)
- Agregar anclas `t1/t2/t3/t4/retos/proyecto/glosario/resumen`.

## 3) Secciones teóricas mínimas
**Topic 1** (requests y APIs):
- `requests.get()`, `requests.post()`.
- chequear `status_code`.
- `response.json()` y manejo de errores.
- ejemplos con API pública gratuita (ej. open-meteo).

**Topic 2** (pandas):
- Series y DataFrame.
- `read_csv`, `head`, `info`, `describe`.
- filtrado, groupby, agregaciones.
- exportar csv/Excel.

**Topic 3** (visualización):
- matplotlib básico (`plot`, etiquetas, leyenda).
- seaborn (`sns.barplot`, `sns.heatmap`).
- guardar gráficos con `plt.savefig()`.

**Topic 4** (archivos/excel):
- `openpyxl` o `pandas` `read_excel` y `to_excel`.
- lectura de JSON con `json.load`, escritura con `json.dump`.
- manejo de rutas (`pathlib`).

## 4) Retos progresivos
- Reto 1: obtener datos de API, parsear JSON y mostrar datos clave.
- Reto 2: cargar datos con pandas, limpiar filas nulas y agregar columna calculada.
- Reto 3: generar gráfico simple con seaborn/matplotlib.
- Reto 4: guardar dataset transformado en CSV/Excel.
- Validaciones suaves con `assert`, y fallback si no hay conexión.

## 5) Proyecto
- Nombre: "Análisis de datos de clima / transacciones".
- Requisitos:
  - usar API externa o fichero local como datos.
  - procesar con pandas.
  - visualizar al menos dos gráficos.
  - exportar resultado.
- Validación:
  - asserts sobre filas o claves en JSON.

## 6) Glosario
- Definir: API, endpoint, JSON, DataFrame, Series, groupby, merge, matplotlib, seaborn.
- Referencia oficial:
  - https://pandas.pydata.org/docs/
  - https://matplotlib.org/stable/contents.html
  - https://docs.python-requests.org/

## 7) Cierre con “¿Qué aprendimos?”
- Listar conceptos clave y pasos prácticos.

## 8) Formato
- Mantener `VSCode.Cell` con `language` correcto.
- No borrar `id` existentes.
- Evitar `#@markdown` críptico.

## 9) Resultado de ejecución
- Devolver:
  - resumen de cambios.
  - diff / patch sugerido.
  - checklist de criterios implementados.
