# **Python-Cheat-Sheets**

Hojas de trucos para aprender Python.

---

## **Tipo de datos**

### **Números**

---

> Los números en Python se pueden representar de varias maneras:

---

- #### **Enteros**

---

> Los números enteros pueden ser representados en base decimal `(10)`, octal `(8)`, hexadecimal `(16)` o binario `(2)`.

```python
# Base decimal
>>> 1234
# Base octal
>>> 0o1234
# Base hexadecimal
>>> 0x1234
# Base binaria
>>> 0b1010
# Notación científica
>>> 1.23e4
# Notación decimal
>>> 1.23e-4
```

---

- #### **Punto flotante**

---

> Los números de punto flotante pueden ser representados en `notación científica` o en `notación decimal`.

```python
# Punto decimal
>>>2.34
# Notación científica
>>>2.34e-5
```

---

- #### **Complejos**

---

> Los números complejos son números que tienen una parte real y una parte imaginaria se representan con la letra `j` o `J` al final del numero imaginario.

```python
>>> 5 + 6j
>>> 5 + 6J
```

---

### **Cadenas**

---

> Las cadenas en Python son secuencias de caracteres Unicode (Unicode strings)y pueden ser representadas con comillas simples `'`, comillas dobles `"` o triples `'''`, `"""` las comillas triples se usan para representar cadenas de multiples lineas y que estas ignoren caracteres de escape como `\n` o `\t`.

```python
"Cadenas de 'caracteres' con comillas dobles."
'Cadenas de "caracteres" con comillas simples.'
"""Cadenas de 'caracteres'
con tres comillas dobles."""
'''Cadenas de "caracteres"
con tres comillas simples.'''
```

---

### **Listas**

---

> Una lista es una estructura de datos que contiene una colección o secuencia de datos. Los datos o elementos de una lista deben ir separados con una coma `,` y todo el conjunto entre corchetes `[]`. Se dice que una lista es una estructura mutable porque además de permitir el acceso a los elementos, pueden suprimirse o agregarse nuevos. Puede contener elementos de cualquier tipo, incluso otras listas. Se accede a los elementos de una lista mediante su posición, comenzando por el elemento `0` y entre corchetes `[]`.

```python
# Lista
[1, 2, 3]
# Lista con diferentes tipos de datos
[1, 2.34, 5 + 6j, "siete", [8, 9, 10], (11, 12, 13), {"catorce": 14, "quince": 15}, {16, 17, 18}, True, None]
```

---

### **Tuplas**

---

> Una tupla permite tener agrupados un conjunto inmutable de elementos, es decir, en una tupla no es posible agregar ni eliminar elementos. Las tuplas se declaran separando los elementos por comas `,` y éstos, opcionalmente, pueden ir entre paréntesis `()`. Se recomienda el uso de paréntesis para evitar ambigüedades. Puede contener elementos de cualquier tipo, incluso otras tuplas. Se accede a los elementos de una tupla mediante su posición, comenzando por el elemento `0` y entre corchetes `[]`.

```python
# Tupla
(1, 2, 3)
# Tupla con diferentes tipos de datos
(1, 2.34, 5 + 6j, "siete", [8, 9, 10], (11, 12, 13), {"catorce": 14, "quince": 15}, {16, 17, 18}, True, None)
```

---

### **Diccionarios**

---

> Los diccionarios son objetos que contienen una lista de parejas de elementos. De cada pareja un elemento es la clave, que no puede repetirse, y, el otro, un valor asociado. La clave que se utiliza para acceder al valor tiene que ser un dato inmutable como una cadena, mientras que el valor puede contener elementos de cualquier tipo, incluso otro diccionario. Los diccionarios se declaran con llaves `{"clave": valor}`y cada pareja de elementos se separa con una coma `,`. Se accede a los elementos de un diccionario mediante su clave y entre corchetes `[clave]`.

```python
# Diccionario
{"uno": 1, "dos": 2, "tres": 3}
# Diccionario con diferentes tipos de datos
{"entero": 1, "flotante": 2.34, "complejo": 5 + 6j, "cadena": "siete", "lista": [8, 9, 10], "tupla": (11, 12, 13), "diccionario": {"catorce": 14, "quince": 15}, "conjunto": {16, 17, 18}, "booleano": True, "nulo": None}
```

---

### **Conjuntos**

---

> Un conjunto es una lista de elementos donde ninguno de ellos está repetido. Los conjuntos se declaran con llaves `{}` y cada elemento se separa con una coma `,`. Puede contener elementos de cualquier tipo, incluso otros conjuntos. No se puede acceder a ellos por su posición sino por su valor ya que no tienen orden ni índice de posición.

```python
# Conjunto
{1, 2, 3}
# Conjunto con diferentes tipos de datos
{1, 2.34, 5 + 6j, "siete", [8, 9, 10], (11, 12, 13), {"catorce": 14, "quince": 15}, {16, 17, 18}, True, None}
```

---

### **Booleanos**

---

> Los valores booleanos en Python son usados para representar valores lógicos y pueden ser `True` o `False`.

```python
# Booleanos
True
False
```

---

### **Nulos**

---

> Los valores nulos en Python son usados para representar valores nulos osea que no tienen valor y pueden ser `None`.

```python
# Nulos
None
```

---

## **Comentarios**

> Los comentarios en Python son líneas de texto que son ignoradas por el intérprete de Python y que se utilizan para documentar o agregar notas al código. Pueden ser representados usando el símbolo `#` para comentarios de una sola línea o usando tres comillas simples `'''` o dobles `"""`para comentarios de varias líneas.

```python
# Comentarios en linea con usando un "#" hashtag.
'''Comentarios multilíneas
con tres comillas simples.'''
"""Comentarios multilíneas
con tres comillas dobles."""
```

---

## **Imprimir**

> La función `print()` es usada para imprimir en pantalla el valor de una expresión o una cadena de caracteres.

```python
# Imprimir en la consola
print("Hola mundo!")
```

---

## **Variables**

> Variables en Python son contenedores que almacenan valores de cualquier tipo. Se declaran con un nombre y se les asigna un valor usando el operador de asignación `=`. El nombre de una variable puede ser cualquier combinación de letras, números y guiones bajos `_`, pero no puede comenzar con un número. No se pueden usar palabras reservadas como nombres de variables. Las variables son sensibles a mayúsculas y minúsculas, es decir, `nombre` y `Nombre` son dos variables diferentes. Por convención, los nombres de variables se escriben en minúsculas y si son compuestos, se separan con guiones bajos `_`.

```python
# Asignación de variables
edad_juan = 27
edad_pedro = 30
edad_carlos = 28

# Asignación múltiple
edad_juan, edad_pedro, edad_carlos = 27, 30, 28

# Asignación múltiple con el mismo valor
edad_juan = edad_pedro = edad_carlos = 29

# Asignación de variables con valores de diferentes tipos
nombre, edad, estatura = "Carlos", 28, 1.75

# Asignación de variables con valores de diferentes tipos
nombre = "Carlos"
edad = 28
estatura = 1.75
```

---

## **Constantes**

> Las constantes en Python son variables que no pueden ser modificadas una vez que se les ha asignado un valor. Se declaran con un nombre y se les asigna un valor usando el operador de asignación `=`. El nombre de una constante puede ser cualquier combinación de letras, números y guiones bajos `_`, pero no puede comenzar con un número. No se pueden usar palabras reservadas como nombres de constantes. Las constantes son sensibles a mayúsculas y minúsculas, es decir, `NOMBRE` y `Nombre` son dos constantes diferentes. Por convención, los nombres de constantes se escriben en mayúsculas y si son compuestos, se separan con guiones bajos `_`.

```python
PI = 3.14159
GRAVEDAD = 9.8
```

---

## **Concatenación**

> La concatenación en Python es la unión de dos o más cadenas de caracteres. Se realiza con el operador `+` y se puede usar con cadenas de caracteres y variables que contengan cadenas de caracteres u otros tipos de datos que se conviertan a cadenas de caracteres. Hay diferentes formas de concatenar cadenas de caracteres en Python. La primera es usando el operador `+`. La segunda es usando el método `format()` de la clase `str`. La tercera es usando el método `join()` de la clase `str`. La cuarta es usando el operador `%` y la quinta es usando el operador `f` antes de la cadena de caracteres.

```python
# Concatenación con el operador + no es posible con tipos de datos diferentes a cadenas de caracteres.

nombre = "Juan"
print("Hola " + nombre + "!")
>>>Hola Juan!

# Concatenación con el método format()
nombre = "Juan"
print("Hola {}!".format(nombre))
>>>Hola Juan!

# Concatenación con el método join()
nombre = "Juan"
print("Hola".join(nombre))
>>>HolaJuan

# Concatenación con el operador %
nombre = "Juan"
print("Hola %s!" % nombre)
>>>Hola Juan!

# Concatenación con el operador f
nombre = "Juan"
print(f"Hola {nombre}!")
>>>Hola Juan!
```
