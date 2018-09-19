#### Score: 50

# Consigna:
Julia tiene cadena de caracteres, s, compuesta por las letras a, b, c y d. Se dice que la cadena de caracteres está equilibrada si se cumplen las dos condiciones siguientes:
 
El número sumado de a's y c's es par.
El número sumado de b's y d's es par.

Por ejemplo, las cadenas de caracteres 'abcd' y 'aacc' están equilibradas, pero 'abc' y 'bcd' no lo están.

Tu tarea consiste en ayudar a Julia a determinar si dos cadenas de caracteres están equilibradas o no.
 
Formato de entrada 

La entrada consiste en una sola línea con la cadena de caracteres a analizar.

## Restricciones
Cada carácter s[i] ∈ {abcd}.

Se le proporciona un archivo con la entrada https://www.dropbox.com/s/e25p5zi1twsdvse/Copia%20de%20input029.txt?dl=0
 
Sample Case 0
Sample Input 0
acdbddbbbbaaac
 
Sample Output 0
true

# Resolución:
Si bien la implementación de la solución es trivial, me dejé llevar por la tentación de probar los únicos 2 valores posibles que admitía la solución: ```true``` y ```false```.
La respuesta era: ```false```. En todo caso, una solución _rusheada_:
```
if (string.count("a") + string.count("c") % 2 == 0) and (string.count("b") + string.count("d") % 2 == 0):
    print("True")
else:
    print("False")
```
