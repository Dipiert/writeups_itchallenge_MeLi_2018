#### Score: 50

# Consigna:
Arturo es un escritor aficionado de novelas de misterios. Hace pocos días ha terminado su último libro y, hasta ahora, su mejor obra, titulada "El Misterio de la Mano". No solo eso, Arturo acaba de firmar un contrato con una editorial para que lo ayude a comercializar su libro y lograr que el mundo conozca su trabajo.

Una de las decisiones más importantes que Arturo debe tomar es el tamaño en el que su libro será impreso. Para ello, le ayudaría mucho saber la cantidad de páginas que su libro tendría en cada formato.
Dependiendo del formato del libro, cada página puede contener hasta Z caracteres. Sin embargo, la editorial exige que cada página incluya el título del libro de largo Y , además del número de página actual y la cantidad de páginas del libro separados por el carácter ’/’. Para escribir el número de página actual se usa la misma cantidad de espacios que el número de paginas, anteponiendo los ’0’ que sean necesarios. Por ejemplo, la página “uno de diez” se escribe 01/10, ocupando cinco caracteres.
Arturo sabe que su libro tiene X caracteres. Ayuda a Arturo a determinar la mínima cantidad de páginas que tendría su libro, dependiendo del formato que escoja.
La primera línea de la entrada contiene tres enteros X, Y y Z, donde X (1 ≤ X ≤ 10^5) es el número de caracteres en el libro, Y (0 ≤ Y ≤ 10^2) es el largo del título, y Z (0 ≤ Z ≤ 10^5) es el número de caracteres que se puede escribir en una página. La entrada está construida de manera que siempre es posible generar un libro.
Como salida se espera un valor entero que representa el mínimo número de páginas que puede tener el libro.

# Resolución:
La consigna es un poco tediosa de leer y oscurece el objetivo pero si van traduciendo a código a medida que van comprendiendo el escenario, puede que terminen con algo parecido a lo que sigue.
```
X = 171024 # Num de caracteres del libro
Y = 12825 # Largo del titulo
Z = 14359 # Chars totales por pagina
```
La cantidad de caracteres por página, en principio, viene dada por la cantidad de caracteres que entran por página menos el largo del título, es decir:
```
Zef = Z - Y
```
Con esto podríamos ya podríamos calcular de manera auxiliar la cantidad de páginas que llevará el libro y, por ello, la cantidad de caracteres que implicará el pie:
```
pags = X / Zef
pie = len(str(pags))*2 + 1
```
Con esto ya tenemos todos los datos para el cálculo final:
```
Zef -= pie
pagsEf = X / Zef
print(pagsEf)
```
Esto es: ```112```