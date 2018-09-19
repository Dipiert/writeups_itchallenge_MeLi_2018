#### Score: 150
# Consigna:
Mercado Libre se está expandiendo, por ello estamos construyendo una nueva oficina. La misma está en proceso de construcción. Sin embargo el equipo encargado de la decoración está en un dilema y solicitó ayuda a IT.

Tienen que decorar el muro principal de la oficina para que sea el punto focal de la oficina. El muro tiene 32 x 3 metros (ancho x alto, sin ninguna aberturas) y se quiere utilizar planchas de vinilo de 1 metro por 3 metros (ancho x alto, pueden ser dispuesta tanto horizontalmente como verticalmente) de distintos colores y patrones de diseño pero no están muy seguros de cómo disponerlos para que quede lindo. Por ello pidieron al equipo de IT si les podían calcular todas las posibles disposiciones (sin superponer planchas) para poder tomar una decisión sin dejar ninguna opción sin evaluar.

Has sido asignado la resolución de esta incógnita: ¿qué cantidad de formas distintas de disponer las planchas van a tener que evaluar para tomar una decisión?

# Resolución: 
Apenas terminé de leer la consigna pensé que se trataba de un problema de optimización. Un caso de [bin packing](https://en.wikipedia.org/wiki/Bin_packing_problem) o [2D Knapsack](https://en.wikipedia.org/wiki/Knapsack_problem) o alguno de esos que gente mucho más inteligente que yo estudia con mucho afán. Por estos derroteros me encontré un paper muy interesante llamado ["Thousand Ways to Pack the Bin - A Practical Approach to Two-Dimensional Rectangle Bin Packing."](clb.demon.fi/files/RectangleBinPack.pdf) pero la cuestión era que el problema que tenía entre manos era mucho más sencillo. No fue hasta que dibujé un esquema del problema en un cuaderno que me di cuenta de que una de las dimensiones de los paneles (ya que éstos pueden rotarse) era igual al alto de la pared y que esto era un [Tiling puzzle](https://en.wikipedia.org/wiki/Tiling_puzzle). Para no reinventar la rueda hice una pequeña búsqueda en ~~Google~~ DuckDuckGo y me encontré con [un artículo](https://www.geeksforgeeks.org/count-number-ways-tile-floor-size-n-x-m-using-1-x-m-size-tiles/) del cual, Marge no voy a mentirte, saqué el código que me permitió dar con la solución:
```
125491
```