# Prompt para modulo8_proyectos_avanzados.ipynb

**Meta**: transformar el notebook en un módulo de proyectos avanzados que integre lo aprendido y sea robusto para prácticas reales.

## 1) Revisión inicial
- Leer todo el notebook.
- Identificar secciones clave (`##`, `###`).
- Detectar temas principales: proyecto integral, manejo de datos, modularidad, funciones reutilizables, librerías externas, buenas prácticas, testing básico.

## 2) Navegación y anclas
- Insertar en la introducción:
  - [Introducción](#mod8)
  - [Topic 1: Definición de proyecto](#t1)
  - [Topic 2: Diseño de arquitectura](#t2)
  - [Topic 3: Implementación paso a paso](#t3)
  - [Topic 4: Pruebas y validación](#t4)
  - [Retos Progresivos](#retos)
  - [Proyecto principal](#proyecto)
  - [Glosario](#glosario)
  - [Resumen](#resumen)
- Agregar anclas `t1... t4` etc.

## 3) Secciones teóricas mínimas
**Topic 1** (definición de proyecto):
- objetivo final claro.
- entrada/salida esperada.
- alcance y criterios de éxito.

**Topic 2** (arquitectura):
- modularidad en funciones.
- clases opcionales si aplica.
- segmentar en archivos/funciones reutilizables.

**Topic 3** (implementación):
- ventanas de progreso.
- manejo de estados.
- interacción de módulos previos (condicionales, listas, OOP, pandas, etc.).

**Topic 4** (tests):
- `assert` integrado.
- funciones de test simple para partes clave.
- manejo de casos edge.

## 4) Retos progresivos
- Reto 1: descomponer un requisito grande en funciones pequeñas.
- Reto 2: agregar manejo de entrada inválida y excepciones.
- Reto 3: implementar logs o prints de depuración opcionales.
- Reto 4: añadir un modo de configuración read-only / debug.

## 5) Proyecto central
- Nombre: "App de gestión (tareas/clientes/inventario)".
- Requisitos:
  - integración de datos en colección (listas/dicts). 
  - operaciones CRUD.
  - opción de exportar/importar (CSV/JSON).
  - interfaz simple en terminal o estructura basada en condiciones.
- Validación:
  - asserts de estado tras operaciones.
  - resultados esperados para un flujo de usuario.

## 6) Glosario
- Definir: flujo principal, refactorización, modularidad, edge case, logging, minitest.
- Referencia:
  - https://docs.python.org/es/3/tutorial/modules.html

## 7) Cierre
- Sección `¿Qué aprendimos?` con bullets.

## 8) Formato
- Mantener `VSCode.Cell`, `language` correcto.
- No eliminar `id` existentes.
- Evitar `#@markdown` críptico.

## 9) Salida esperada
- Resumen de cambios
- Diff / patch
- Checklist de cumplimiento
