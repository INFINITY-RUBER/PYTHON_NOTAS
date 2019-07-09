# PYTHON_NOTAS
Notas de repaso para  No olvidar los comandos basicos de Soy Pythonista 🐍

-Si estás usando la versión 2.x de Python y quieres hacer uso de caractéres NO-ASCII en tu código, no olvides añadir la siguiente línea al principio de tu script 
Por ejemplo:
## -*- coding: utf-8 -*- 
'print("Hola, ¿cómo estás?")'

## La forma más sencilla para generar un
## secreto o API KEY en Python 2.x
'>>>import os, binascii'

>>>binascii.b2a_hex(os.urandom(20))
b'b6026f861fd41a94c3389d54293de9d04bde6f7c'
