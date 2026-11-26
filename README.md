# Laboratorio 2 — Condicionales, ciclos y estructuras de datos

Este laboratorio profundiza en la programación con estructuras condicionales, ciclos, colecciones y comprensión de datos. Incluye ejercicios independientes y un reto integrador con un gestor de inventario por consola.

## Condicionales

Los ejercicios de esta sección toman decisiones según una o varias condiciones.

| Archivo | Descripción y función |
|---|---|
| `comparaciones.py` | Utiliza operadores de comparación para determinar relaciones entre valores. |
| `rango_edad.py` | Comprueba si una edad pertenece a un rango determinado. |
| `validar_edad.py` | Valida que la edad cumpla una condición mínima o máxima. |
| `clasificar_numero.py` | Clasifica un número según su relación con el cero o sus propiedades. |
| `clasificar_nota.py` | Convierte una calificación en una categoría o resultado descriptivo. |
| `acceso_sala.py` | Decide si una persona puede ingresar a una sala según sus datos. |
| `acceso_actividad.py` | Autoriza o rechaza una actividad mediante condiciones combinadas. |
| `Disponibilidad.py` | Comprueba si existe disponibilidad antes de permitir una operación. |
| `costo_envio.py` | Calcula o determina el costo según las condiciones del envío. |
| `precio_con_impuestos.py` | Aplica impuestos o modifica el precio según una condición. |
| `validar_compra.py` | Evalúa si una compra cumple las reglas establecidas. |
| `evaluar_solicitud.py` | Aprueba o rechaza una solicitud según edad, inscripción y documentos. |
| `error_indentacion.py` | Presenta un ejemplo de error producido por una sangría incorrecta. |

## Ciclos

Esta sección practica la repetición controlada mediante `for` y `while`.

| Archivo | Descripción y función |
|---|---|
| `contador_while.py` | Repite instrucciones mientras se mantenga una condición. |
| `contador_for.py` | Recorre una secuencia o rango con un ciclo `for`. |
| `sumar_numeros.py` | Suma varios números mediante repetición. |
| `suma_interactiva1.py` | Solicita valores y los procesa dentro de un ciclo. |
| `hasta_cero.py` | Continúa solicitando datos hasta recibir el valor cero. |
| `tabla_multiplicar.py` | Genera la tabla de multiplicar de un número. |
| `cuadrados.py` | Calcula y muestra los cuadrados de varios números. |
| `filtrar_numeros.py` | Recorre números y conserva únicamente los que cumplen una regla. |
| `menu_repetitivo.py` | Mantiene un menú activo hasta que el usuario elige salir. |
| `control_ahorros.py` | Realiza un seguimiento repetido de ahorros o acumulaciones. |

## Listas

Los ejercicios muestran cómo crear, recorrer y modificar colecciones de elementos.

| Archivo | Descripción y función |
|---|---|
| `primera_lista.py` | Crea una lista y accede a sus elementos. |
| `lista_materias.py` | Guarda materias en una lista y recorre sus nombres. |
| `lista_tareas.py` | Representa tareas dentro de una lista y permite consultarlas o modificarlas. |
| `operaciones_lista.py` | Practica operaciones básicas como agregar, eliminar o buscar elementos. |
| `append.py` | Ejemplifica la adición de elementos con el método `append()`. |
| `actualizar_producto.py` | Modifica un elemento o dato dentro de una estructura de producto. |
| `calificaciones_lista.py` | Procesa calificaciones almacenadas en una lista. |
| `promedio_notas.py` | Calcula el promedio de las notas de una lista. |
| `sin_duplicados.py` | Elimina o evita valores repetidos. |
| `normalizar_codigos.py` | Convierte códigos a una forma uniforme dentro de una colección. |

## Tuplas y conjuntos

| Archivo | Descripción y función |
|---|---|
| `primeras_tuplas.py` | Crea tuplas y muestra el acceso a sus elementos. |
| `categorias_tupla.py` | Guarda categorías inmutables en una tupla y las utiliza como valores autorizados. |
| `ciudades.py` | Representa ciudades mediante una colección de datos. |
| `ubicaciones.py` | Trabaja con ubicaciones almacenadas en una estructura de colección. |
| `participantes.py` | Practica la administración de participantes sin elementos duplicados. |
| `invitados.py` | Representa un conjunto de invitados y evita repeticiones. |

## Diccionarios y datos estructurados

| Archivo | Descripción y función |
|---|---|
| `primer_diccionario.py` | Crea un diccionario y accede a sus claves y valores. |
| `perfil_diccionario.py` | Organiza información de una persona mediante pares clave-valor. |
| `catalogo_diccionario.py` | Representa varios productos o registros dentro de un diccionario. |
| `catalogo_libros.py` | Guarda información de libros como título, autor y datos relacionados. |
| `etiquetas.py` | Trabaja con etiquetas asociadas a elementos o registros. |
| `curso_anidado.py` | Accede a datos almacenados dentro de diccionarios y listas anidadas. |

## Comprensiones

| Archivo | Descripción y función |
|---|---|
| `informe_comprensiones.py` | Construye nuevas colecciones mediante comprensión de listas o conjuntos. |
| `inscripciones_talleres.py` | Procesa inscripciones y produce la información solicitada en forma compacta. |

## Reto integrador — Gestor de inventario

El archivo [`gestor_inventario.py`](./laboratorio%202/gestor_inventario.py) integra listas, diccionarios, tuplas, condicionales, ciclos y comprensiones en un programa completo.

Sus funciones principales son:

- Registrar productos con código, nombre, categoría, precio y cantidad.
- Rechazar campos vacíos, categorías no permitidas, códigos repetidos, precios negativos y cantidades negativas.
- Listar todos los productos registrados.
- Buscar un producto por su código.
- Actualizar las existencias de un producto existente.
- Eliminar un producto por código.
- Mostrar los productos que no tienen existencias.
- Consultar el resumen: cantidad de productos, unidades, valor total y categorías utilizadas.
- Mantener un menú repetitivo hasta seleccionar la opción de salida.

## Ejecución

Desde la carpeta del laboratorio:

```bash
cd "laboratorio 2"
python nombre_del_archivo.py
```

Ejemplo para el reto integrador:

```bash
python gestor_inventario.py
```

## Conceptos trabajados

- Condiciones simples y múltiples con `if`, `elif` y `else`.
- Operadores lógicos y de comparación.
- Ciclos `for` y `while`.
- Menús repetitivos.
- Listas, tuplas, conjuntos y diccionarios.
- Acceso y modificación de colecciones.
- Colecciones anidadas.
- Comprensiones de listas y conjuntos.
- Validación de datos y programación de un programa integrador.
