# Laboratorio 3 — Funciones, módulos y programación orientada a objetos

Este laboratorio contiene ejercicios prácticos en Python sobre funciones, modularización, clases, objetos y encapsulamiento. El objetivo es pasar de programas básicos a una aplicación organizada en componentes que separan responsabilidades y protegen los datos.

## Contenido del laboratorio

- [`practica-3-1`](./practica-3-1): definición y uso de funciones.
- [`practica-3-2`](./practica-3-2): creación e importación de módulos.
- [`practica-3-3`](./practica-3-3): clases, atributos, métodos y objetos.
- [`practica-3-4`](./practica-3-4): encapsulamiento, propiedades y relaciones entre objetos.
- [`gestor_inventario`](./gestor_inventario): reto integrador de un gestor de inventario por consola.
- [`gestor_inventario_depuracion`](./gestor_inventario_depuracion): ejemplo separado para practicar la depuración.

## Práctica 3.1 — Funciones

La práctica introduce la creación de funciones para dividir un programa en tareas reutilizables.

| Archivo | Descripción y función |
|---|---|
| `alcance.py` | Ejemplifica el alcance local y global de las variables. |
| `calculos.py` | Realiza operaciones básicas mediante funciones y demuestra el uso de `return`. |
| `cotizador_funciones.py` | Cotiza un producto usando funciones separadas para el cálculo y la presentación. |
| `error_retorno.py` | Muestra qué ocurre cuando una función ejecuta cálculos pero no devuelve su resultado. |
| `funciones_listas.py` | Demuestra cómo una función puede modificar una lista recibida o construir y devolver una lista nueva. |
| `inventario_funciones.py` | Organiza operaciones de inventario, como registro y búsqueda, en funciones. |
| `mensajes.py` | Presenta funciones destinadas a mostrar mensajes. |
| `parametros.py` | Ejemplifica parámetros posicionales y nominales al llamar una función. |
| `primeras_funciones.py` | Muestra la definición y llamada de una función simple. |
| `sin_return.py` | Compara una función que solo imprime con una función que devuelve un dato. |
| `valores_predeterminados.py` | Explica y prueba parámetros con valores predeterminados. |

Conceptos trabajados: definición de funciones, parámetros, argumentos, valores predeterminados, `return`, reutilización de código, alcance de variables y modificación de listas.

## Práctica 3.2 — Módulos

La práctica divide el código entre diferentes archivos para evitar que un programa tenga todas sus definiciones y reutilizar código mediante módulos.

| Archivo o carpeta | Descripción y función |
|---|---|
| `operaciones.py` | Contiene funciones de cálculo que pueden importarse desde otros archivos. |
| `main.py` | Importa `operaciones` y usa sus funciones para calcular subtotal, descuento y total. |
| `importar_funciones.py` | Muestra formas de importar funciones desde un módulo. |
| `importacion_incorrecta.py` | Contiene un ejemplo de depuración sobre cómo importar y llamar correctamente una función. |
| `saludos/` | Separa las funciones de saludos de los archivos que las utilizan. |
| `mensajes_demo/` | Ejemplifica la diferencia entre ejecutar un módulo directamente e importarlo desde otro archivo. |
| `validaciones_demo/` | Practica la reutilización de validaciones mediante un módulo independiente. |
| `conversiones/` | Organiza fórmulas de conversión en `unidades.py` y las utiliza desde `main.py`. |
| `cotizador_modular/` | Divide un cotizador en validaciones, cálculos y programa principal. |

Conceptos trabajados: creación de módulos, `import`, `from ... import ...`, espacios de nombres y `if __name__ == "__main__"`.

## Práctica 3.3 — Clases y objetos

La práctica presenta la programación orientada a objetos, incluyendo la creación de clases que representan conceptos del programa.

| Archivo | Descripción y función |
|---|---|
| `primer_producto.py` | Crea una clase vacía y muestra cómo instanciar un objeto con `Producto()`. |
| `producto_objetos.py` | Define atributos y métodos de una clase `Producto` y crea objetos con datos propios. |
| `estudiante.py` | Representa estudiantes mediante una clase y utiliza `self` para guardar su información. |
| `billetera.py` | Modela una billetera con atributos como saldo y métodos para consultar o modificar su estado. |
| `atributos_clase_vs_instancia.py` | Compara atributos compartidos por la clase con atributos particulares de cada instancia. |
| `depuracion_self.py` | Corrige un método cuyo parámetro `self` falta o está mal definido. |
| `depuracion_atributo.py` | Corrige el uso de un atributo inexistente o escrito de forma incorrecta. |

Conceptos trabajados: clases, instancias, atributos, métodos, constructor `__init__`, `self`, atributos de clase y atributos de instancia.

## Práctica 3.4 — Encapsulamiento

La práctica introduce convenciones y mecanismos para proteger la información interna de un objeto y validar cambios.

| Archivo o carpeta | Descripción y función |
|---|---|
| `producto_seguro.py` | Protege atributos con guiones bajos y expone consulta o modificación mediante propiedades y métodos validados. |
| `leer_precio.py` | Lee precios desde la entrada y rechaza valores inválidos o no numéricos. |
| `leer_cantidad.py` | Solicita una cantidad entera y no negativa. |
| `cuenta_puntos.py` | Ejercita atributos internos y métodos que controlan cambios de estado. |
| `lista_compartida.py` | Comprueba cuándo una lista pertenece a una clase o a cada instancia. |
| `relacion_objetos/` | Distribuye las clases `Producto` e `Inventario` en archivos relacionados: un inventario contiene varios objetos `Producto`. |

Conceptos trabajados: atributos internos, propiedades, setters, validación, encapsulamiento por convención y relación entre objetos.

## Reto integrador — Gestor de inventario

La carpeta [`gestor_inventario`](./gestor_inventario) reúne las prácticas anteriores en una aplicación de consola para administrar productos.

- `producto.py`: define la clase `Producto`, valida los datos y calcula el valor de cada artículo.
- `inventario.py`: define la clase `Inventario`, almacena productos y controla registro, búsqueda, actualización, eliminación y resumen.
- `main.py`: muestra el menú, lee los datos ingresados por el usuario y presenta los resultados.
- `pruebas_automaticas.py`: ejecuta comprobaciones automáticas de las reglas y operaciones del gestor.
- `pruebas_independencia.py`: verifica que dos inventarios utilizan colecciones independientes.
- `README.md`: contiene la documentación técnica específica del gestor.

Para ejecutar la aplicación:

```bash
cd gestor_inventario
python main.py
```

Para ejecutar las pruebas:

```bash
python pruebas_automaticas.py
python pruebas_independencia.py
```

Las operaciones disponibles son registrar, listar, buscar, actualizar existencias, eliminar, consultar productos sin stock y mostrar el resumen del inventario.

## Depuración

La carpeta [`gestor_inventario_depuracion`](./gestor_inventario_depuracion) conserva una versión separada del reto para practicar la identificación y corrección de errores sin alterar el programa principal.

## Respuestas y comprobaciones

El archivo [`Readme.md`](./Readme.md) contiene predicciones, resultados de depuración y respuestas a las comprobaciones de las prácticas 3.1 a 3.5.
