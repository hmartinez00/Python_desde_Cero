# Prompt para modulo6_oop.ipynb

**Meta**: transformar el notebook en un módulo OOP claro y didáctico, consistente con los módulos previos.

## 1) Revisión inicial
- Leer todo el notebook.
- Identificar secciones clave (`##`, `###`).
- Detectar temas principales: clases, objetos, constructores, atributos, métodos, herencia, encapsulación, polimorfismo, métodos especiales (`__init__`, `__str__`, `__repr__`, `__eq__`), y design patterns básicos.

## 2) Navegación y anclas
- Insertar en la introducción:
  - [Introducción](#mod6)
  - [Topic 1: Clases y objetos](#t1)
  - [Topic 2: Atributos y métodos](#t2)
  - [Topic 3: Herencia y polimorfismo](#t3)
  - [Topic 4: Encapsulación y métodos especiales](#t4)
  - [Retos Progresivos](#retos)
  - [Proyecto](#proyecto)
  - [Glosario](#glosario)
  - [Resumen](#resumen)
- Agregar anclas equivalentes (`<a id="t1"></a>`, etc.).

## 3) Secciones teóricas mínimas
**Topic 1** (clases, objetos):
- sintaxis `class Nombre:`
- instanciación `obj = Clase()`
- `self` y namespace.

**Topic 2** (atributos y métodos):
- atributos de instancia y de clase.
- métodos de instancia y estáticos (`@staticmethod`, `@classmethod`).
- método constructor `__init__`.

**Topic 3** (herencia y polimorfismo):
- heredar con `class Hija(Base):`
- `super().__init__()`
- sobrescribir métodos.
- polimorfismo básico con listas de objetos.

**Topic 4** (encapsulación):
- atributos públicos/privados/privados por convención (`_x`, `__x`).
- propiedades (`@property`, `@x.setter`).
- métodos especiales `__str__`, `__repr__`, `__eq__`.

## 4) Retos progresivos
- Reto 1: clase `Persona` con `nombre` y `edad`, método `saludar()`.
- Reto 2: clase `CuentaBancaria` con métodos `depositar`, `retirar`, `mostrar_saldo`, y manejo de excepciones para sobregiro.
- Reto 3: herencia con `Empleado` y `Gerente`, override de método `calcular_bono`.
- Reto 4: uso de `@property` para control de acceso a atributos.
- Incluir validación `assert`, fallback dummy.

## 5) Proyecto
- Nombre: "Gestor de biblioteca" o "Inventario OOP".
- Requisitos:
  - clases `Libro`, `Autor`, `Biblioteca`.
  - métodos para agregar/eliminar/buscar libros.
  - herencia opcional para `LibroEspecial`, override de métodos.
  - métodos especiales para impresión y comparación.
- Validación:
  - asserts sobre comportamiento esperado.
  - método `__str__` probado.

## 6) Glosario
- Definir: clase, objeto, instancia, atributo, método, constructor, herencia, polimorfismo, encapsulación, método mágico.
- Referencia oficial:
  - https://docs.python.org/es/3/tutorial/classes.html

## 7) Cierre con “¿Qué aprendimos?”
- Listar puntos clave de OOP y cuándo usar.
- Recomendación de ejercicios adicionales.

## 8) Formato
- Mantener `VSCode.Cell` con `language` correcto. 
- No eliminar `id` existentes.
- Evitar notas `#@markdown` crípticas; usar markdown completo.

## 9) Resultado de ejecución
- Devolver:
  - resumen de cambios.
  - diff / patch sugerido.
  - checklist de requisitos implementados.
