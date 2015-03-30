---
title: set 1 - 6 - Rompiendo clave repetida XOR
layout: default
---

Rompiendo clave repetida XOR
============================

<div class="warning">
<h3>Ahora comienza lo bueno</h3>

<p>Este desafío no es conceptualmente difícil, pero implica una codificación propensa a errores. Los otros desafíos están para ir haciéndote entrar en calor. Este está para calificarte. Si puedes hacer este, entonces probablemente lo harás bien hasta el set 6.</p>
</div>

[Aquí]({{ site.url }}/6.txt) hay un archivo. Ha sido convertido a base64 luego de ser cifrado con XOR por clave repetida.

Decífralo.

Aquí te decimos cómo:

Digamos que LARGO_DE_CLAVE es el largo que suponemos de la clave; prueba valores de 2 a (digamos) 40.

Escribe una función que calcule la distancia de edición/distancia Hamming entre dos cadenas. La distancia Hamming es solamente el número de diferencia de bits. La distancia entre:

	this is a test

y

	wokka wokka!!!

es de 37. Asegúrate de que tu código está de acuerdo antes de proseguir.

Para cada valor de LARGO_DE_CLAVE, toma el primer grupo de bytes del largo de LARGO_DE_CLAVE, y el segundo grupo del largo de LARGO_DE_CLAVE y calcula la distancia de edición entre ellos. Normaliza el resultado dividiéndolo entre el valor de LARGO_DE_CLAVE.

_Nota del traductor:_ Esto es, por ejemplo, para la cadena:

	ESTOESUNACADENACIFRADA

comienzas con LARGO_DE_CLAVE = 2. Entonces tomas:

	ES

y

	TO

y calculas la distancia de edición entre esos dos grupos.

El LARGO_DE_CLAVE con el menor valor normalizado de la distancia de edición es probablemente tu clave. Puedes proceder quizás con los LARGO_DE_CLAVE con menores resultados de 2 o 3. O toma 4 bloques de LARGO_DE_CLAVE en lugar de 2 y calcula el promedio de distancias.

Ahora que probablemente sepas el LARGO_DE_CLAVE: rompe el texto cifrado en bloques de largo de LARGO_DE_CLAVE.

Ahora transpón los bloques: haz un bloque que es la primer letra de cada bloque, y un bloque con el segundo byte de cada bloque, y así sucesivamente.

Resuelve cada bloque como si fuese un XOR de un byte. Ya tienes código para hacer esto.

Para cada bloque, la clave XOR de un byte que produce el mejor histograma es parte de la clave XOR de clave repetida para ese bloque. Pónlas todas juntas y tendrás tu clave.

Este código resultará ser sorprendentemente útil más adelante. El método de romper cifrados con XOR por clave repetida de forma estadística ("Vigenere") es obviamente un ejercicio académico, algo así como "Cifrado 101" (_Nota del traductor:_ los cursos llamados "101" son los cursos de introducción a una materia, en Estados Unidos). Pero más personas "saben cómo" romperlo que las que realmente lo rompen, y una técnica similar rompe algo mucho más importante.

<div class="warning">
<h3>No, no hay ningún error</h3>

<p>Recibimos más preguntas sobre este desafío que con cualquier otro. Te lo prometemos, no hay ningún error descarado en este texto. En particular, la distancia de "wokka wokka!!!" es realmente 37.</p>
</div>
