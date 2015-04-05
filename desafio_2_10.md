---
title: set 2 - 10 - Implementando modo CBC
layout: default
---

Implementando modo CBC
======================


El modo CBC es un modo de cifrado por bloque que le permite cifrar mensajes de largo irregular, a pesar del hecho de que el cifrado por bloque solamente transforma bloques individuales.

En modo CBC cada bloque de texto cifrado es sumado al siguiente bloque de texto plano antes del próximo llamado al  cifrado principal.

El primer bloque de texto plano, el cual no tienen ningún bloque de texto cifrado previo, es sumado a un "falso bloque de texto cifrado de posición cero" llamado el vector de inicialización o IV (Initialization Vector, en inglés).

Implementa el modo CBC a mano tomando la función ECB que has escrito previamente, haciéndola cifrar en lugar de descifrar (verifica esto descifrando lo que hayas cifrado al hacer pruebas), y utilizando tu función XOR de previos ejercicios, combínalas.

[El archivo aquí]({{ site.url }}/10.txt) es ininteligible (algo así) cuando lo descifras usando CBC contra "YELLOW SUBMARINE" con un IV de todos los ASCII 0 (\x00\x00\x00 &c)


<div class="warning">
<h3>No hagas trampa</h3>

<p>No utilices el código CBC de OpenSSL para realizar el modo CBC, ni siquiera para verificar tus resultados. ¿Cuál es el sentido de hacer esto si no vas a aprender nada?</p>
</div>