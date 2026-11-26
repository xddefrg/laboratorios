# Laboratorios de Python

Este repositorio reúne los laboratorios de Python. Cada laboratorio se desarrolla en una rama independiente y contiene sus prácticas, ejemplos y su respectivo README.

## Laboratorio 4 — Excepciones, archivos, persistencia y POO

En este laboratorio se trabajó el manejo de errores y datos en Python, desde la validación de entradas hasta la construcción de un gestor de inventario persistente.

### Contenido realizado

- Manejo de excepciones con `try`, `except`, `else` y `finally`.
- Captura y diferenciación de errores como `ValueError`, `TypeError`, `ZeroDivisionError` y `FileNotFoundError`.
- Validación de edades, precios, cantidades, productos y entradas numéricas.
- Recuperación de errores mediante reintentos y mensajes claros al usuario.
- Lectura y escritura de archivos de texto con `open()` y manejo de rutas con `pathlib`.
- Creación de carpetas, agregación de notas, recorrido de líneas y generación de reportes.
- Depuración de problemas comunes relacionados con excepciones y archivos.
- Conversión de estructuras Python a JSON y recuperación de datos desde JSON.
- Manejo de JSON mal formado, objetos no serializables y lectura protegida de archivos.
- Exportación e importación de datos mediante archivos CSV.
- Uso de herencia, sobrescritura de métodos, `super()`, polimorfismo y composición.
- Implementación de ejemplos con vehículos, notificaciones, reportes e instructores.
- Desarrollo de un proyecto integrador: **Gestor de inventario persistente**.

### Estructura del laboratorio

- [`python-laboratorio-04/practica-4-1/`](python-laboratorio-04/practica-4-1/): excepciones, validaciones y recuperación de errores.
- [`python-laboratorio-04/practica-4-2/`](python-laboratorio-04/practica-4-2/): archivos de texto, rutas y `pathlib`.
- [`python-laboratorio-04/practica-4-3/`](python-laboratorio-04/practica-4-3/): persistencia con JSON y exportación a CSV.
- [`python-laboratorio-04/practica-4-4/`](python-laboratorio-04/practica-4-4/): herencia, sobrescritura, polimorfismo y composición.
- [`python-laboratorio-04/gestor_inventario/`](python-laboratorio-04/gestor_inventario/): reto integrador con productos, inventario, almacenamiento y reportes.

Para conocer los ejercicios y las instrucciones de ejecución, consulta el [README del Laboratorio 4](python-laboratorio-04/README.md).

### Ejecutar el proyecto integrador

Desde la raíz del proyecto:

```bash
cd python-laboratorio-04/gestor_inventario
python main.py
```

Para ejecutar las pruebas automáticas:

```bash
python -m unittest -v
```
