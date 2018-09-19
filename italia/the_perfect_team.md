#### Score: 50

# Consigna:
La Escuela de Idiomas y Ciencias enseña cinco materias: Física, Química, Matemáticas, Botánica y Zoología. Cada estudiante es experto en una materia. Las habilidades de los alumnos se describen mediante una string de las habilidades citadas que consta de las letras p, c, m, b y z solamente. Cada carácter describe la habilidad de un estudiante de la siguiente manera:
p → Física.
c →  Química.
m → Matemáticas.
b → Botánica.
z  → Zoología.
 
Tu tarea es determinar el número total de diferentes equipos que satisfacen las siguientes restricciones:
 
Un equipo consiste en un grupo de exactamente cinco estudiantes.
Cada estudiante es experto en una materia diferente.
Un estudiante puede estar solo en un equipo.
 
Por ejemplo, si la cadena de habilidades es pcmbzpcmbz, entonces hay dos equipos posibles que se pueden formar a la vez: habilidades [0-4] y habilidades [5-9]. No es importante determinar las permutaciones, ya que siempre estaremos limitados a dos equipos con 10 estudiantes.
 
Se le proporciona un archivo con la entrada https://www.dropbox.com/s/3neyzkiomsb7eh8/Copia%20de%20input013.txt?dl=0
 
## Restricciones 
5 ≤ n ≤ 5 × 10^5
skills[i] ∈ {p,c,m,b,z}

# Resolución:
A primera vista este problema puede ser abrumador por la longitud del string de entrada pero una lectura detenida muestra que es un problema trivial.
Si cada equipo consiste en 5 estudiantes (_Regla 1_), cada estudiante es experto en una materia diferente (_Regla 2_) y solo hay 5 materias, entonces, por equipo, no puede haber más de un estudiante especializado en una materia. Además, dado que cada estudiante solo puede estar en un solo equipo el problema se reduce a saber cuál es la materia que menos expertos tiene y eso se resuelve fácilmente:
```
with open('italia_input.txt', 'r') as file:
    s = file.readline()
    print(min(s.count("p"), s.count("c"), s.count("m"), s.count("b"), s.count("z")))
```
Lo que nos da la respuesta: ```50334```

