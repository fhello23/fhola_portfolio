
---
title: "Prueba Apuntes Clase"
date: "2025-04-27"
summary: "Prueba Apuntes Clase"
description: "Probando syntax highliting"
toc: true
readTime: false
autonumber: true
math: false
showTags: false
hidePagination: true
draft: false
---

Este es un post muy breve con el propósito de probar dos funcionalidades de Hugo: el resaltado de sintaxis de código y la generación automática de una Tabla de Contenidos.

## Propósito de las Pruebas

El objetivo principal es doble:

1.  Verificar que los bloques de código Python se muestren con resaltado de sintaxis adecuado según la configuración de Hugo (usualmente Chroma).
2.  Comprobar que Hugo genere una Tabla de Contenidos (ToC) a partir de los encabezados de este post.

## Código Python para la Secuencia de Fibonacci

Para probar el resaltado de sintaxis, utilizaremos una función simple en Python que genera los primeros `n` números de la secuencia de Fibonacci. La secuencia de Fibonacci es aquella en la que cada número es la suma de los dos anteriores, comenzando generalmente por 0 y 1.

A continuación, el código:

```python
# Función para generar la secuencia de Fibonacci hasta n términos
def generar_fibonacci(n):
    """
    Genera los primeros n números de la secuencia de Fibonacci.

    Args:
        n (int): El número de términos de la secuencia a generar. Debe ser positivo.

    Returns:
        list: Una lista conteniendo los primeros n números de Fibonacci.
              Devuelve una lista vacía si n <= 0.
    """
    if n <= 0:
        print("Por favor, ingresa un entero positivo.")
        return []
    elif n == 1:
        return [0]
    else:
        lista_fib = [0, 1]
        # Generar los términos restantes
        while len(lista_fib) < n:
            siguiente_num = lista_fib[-1] + lista_fib[-2]
            lista_fib.append(siguiente_num)
        return lista_fib

# Ejemplo de uso: generar los primeros 10 números
numero_de_terminos = 10
secuencia = generar_fibonacci(numero_de_terminos)

print(f"Los primeros {numero_de_terminos} números de la secuencia de Fibonacci son:")
print(secuencia)
# Salida esperada: [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
