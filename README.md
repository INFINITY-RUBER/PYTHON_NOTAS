# PYTHON_NOTAS
Notas de repaso para  No olvidar los comandos basicos de Soy Pythonista 🐍

-Si estás usando la versión 2.x de Python y quieres hacer uso de caractéres NO-ASCII en tu código, no olvides añadir la siguiente línea al principio de tu script 
Por ejemplo:
## `-*- coding: utf-8 -*- `
`print("Hola, ¿cómo estás?")`
## La forma más sencilla para generar un secreto o API KEY en Python 2.x
`>>>import os, binascii`
`>>>binascii.b2a_hex(os.urandom(20))`
b 'b6026f861fd41a94c3389d54293de9d04bde6f7c'
## La forma más sencilla para generar un secreto o API KEY en Python 3.x
`>>> import secrets`
`>>> secrets.token_hex(20)`
*ccaf5c9a22e854856d0c5b1b96c81e851bafb288*
## Cómo comprobar en Python si una lista o diccionario están vacíos
 ```python
 d = {}
 l = []
if d:
    print("Contiene elementos")
else:
    print("No contiene elementos")
if l:
    print("Contiene elementos")
else:
    print("No contiene elementos")
 ```
 ## Cómo clonar o copiar un objeto list usando la operación de copia de la clase list
```python
>>>new_list = old_list.copy()
```
### Creando una nueva lista
```python
>>>new_list = list(old_list)
```
### Usando el método genérico del módulo copy
```python
>>>import copy
>>>new_list = copy.copy(old_list)
```
### Usa deepcopy si la lista contiene objetos y también quieres una copia de los mismos
```python
>>>import copy
>>>new_list = copy.deepcopy(old_list)
```
## Cómo usar el operador ternario en Python
**`a if condition else b`**
#### Por ejemplo:
```python
>>> a = 1
>>> 'true' if a == 1 else 'false'
'true'
>>> 'true' if a == 2 else 'false'
'false'
```
## Cómo convertir un string en un datetime
```python
>>>from datetime import datetime
>>>fecha_str = "08/11/2017 17:00:00"
>>>fecha = datetime.strptime(fecha_str, '%d/%m/%Y %H:%M:%S')
>>>fecha
datetime.datetime(2017, 11, 8, 17, 0)
```
## Cómo convertir un datetime en un string
```python
>>>from datetime import datetime
>>>fecha = datetime(2017, 11, 8, 17, 0)
>>>fecha_str = fecha.strftime('%d/%m/%Y %H:%M:%S')
>>>fecha_str
'08/11/2017 17:00:00'
```
## Cómo mezclar dos diccionarios en una sola expresión
```python
# Cómo mezclar dos diccionarios
# en una sola expresión
# A partir de Python 3.5
>>> x = {'a':1, 'b': 2}
>>> y = {'b':3, 'c': 4}
>>> z = {**x, **y}
>>> z
{'a': 1, 'b': 3, 'c': 4}
# Antes de Python 3.5
>>> z = x.copy()
>>> z.update(y)
>>> z
{'a': 1, 'b': 3, 'c': 4}
# NOTA: Los valores de y
# sobreescriben los de x
```
## Contar las ocurrencias de un elemento en una lista
```python
# Contar las ocurrencias de un
# elemento en una lista
# Ocurrencias de un solo elemento
>>> l = ["a", "b", "c", "b", "d"]
>>> l.count("b")
2
# Ocurrencias de todos los elementos
>>> from collections import Counter
>>> Counter(l)
Counter({'b': 2, 'a': 1, 'c': 1, 'd': 1})
```
## Generar una cadena separada por comas a partir de los elementos de una lista
```python
# Generar una cadena separada por comas
# a partir de los elementos de una lista
# Si es una lista de cadenas
>>> l = ['elementos', 'separados', 'por', 'comas']
>>> l_str = ','.join(l)
>>> l_str
'elementos,separados,por,comas'
# Si no es una lista de cadenas (int, float, ...)
>>> l = [1, 2, 3, 4]
>>> l_str = ','.join(map(str, l))
>>> l_str
'1,2,3,4'
```
## Eliminar duplicados de una lista
```python
# Eliminar duplicados de una lista
>>> l = [1, 2, 3, 1, 4, 2, 1]
>>> l = list(set(l))
>>> l
[1, 2, 3, 4] 
```
## Truncar el tiempo en un objeto DateTime
```python
# Truncar el tiempo en un objeto DateTime
# Por ej: Quitar los segundos y microsegundos
>>> from datetime import datetime
>>> ahora = datetime.now()
>>> ahora
datetime.datetime(2018, 12, 14, 8, 18, 20, 610516)
>>> ahora = ahora.replace(second=0, microsecond=0)
>>> ahora
datetime.datetime(2018, 12, 14, 8, 18)
```
##
```
```
##
```
```
##
```
```
