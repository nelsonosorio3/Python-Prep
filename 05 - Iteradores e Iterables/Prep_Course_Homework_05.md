## Iteradores e iterables

1) A partir de una lista vacía, utilizar un ciclo while para cargar allí números negativos del -15 al -1

lst = []
counter = -15
while counter < 0:
  lst.append(counter)
  counter +=1

print(lst)

2) ¿Con un ciclo while sería posible recorrer la lista para imprimir sólo los números pares?

counter = 0
while counter < len(lst):
  if lst[counter] % 2 == 0:
    print(lst[counter])
  counter += 1

3) Resolver el punto anterior sin utilizar un ciclo while

evens = [i for i in lst if i% 2 ==0]
print(evens)

4) Utilizar el iterable para recorrer sólo los primeros 3 elementos

for i in lst[:3]:
  print(i)

5) Utilizar la función **enumerate** para obtener dentro del iterable, tambien el índice al que corresponde el elemento

for index, num in enumerate(lst[:3]):
  print(index, num)

6) Dada la siguiente lista de números enteros entre 1 y 20, crear un ciclo donde se completen los valores faltantes: lista = [1,2,5,7,8,10,13,14,15,17,20]

lista = [1,2,5,7,8,10,13,14,15,17,20]
for index, num in enumerate(lista):
  if index + 1 != num:
    lista.insert(index, index + 1)

7) La sucesión de Fibonacci es un listado de números que sigue la fórmula: <br>
n<sub>0</sub> = 0<br>
n<sub>1</sub> = 1<br>
n<sub>i</sub> = n<sub>i-1</sub> + n<sub>i-2</sub><br>
Crear una lista con los primeros treinta números de la sucesión.<br>

fib = [0, 1]
for i in range(28):
  fib.append(fib[i]+ fib[i+1])

8) Realizar la suma de todos elementos de la lista del punto anterior

print(sum(fib))

9) La proporción aurea se expresa con una proporción matemática que nace el número irracional Phi= 1,618… que los griegos llamaron número áureo. El cuál se puede aproximar con la sucesión de Fibonacci. Con la lista del ejercicio anterior, imprimir el cociente de los últimos 5 pares de dos números contiguos:<br>
Donde i es la cantidad total de elementos<br>
n<sub>i-1</sub> / n<sub>i</sub><br>
n<sub>i-2</sub> / n<sub>i-1</sub><br>
n<sub>i-3</sub> / n<sub>i-2</sub><br>
n<sub>i-4</sub> / n<sub>i-3</sub><br>
n<sub>i-5</sub> / n<sub>i-4</sub><br>

for i in range(-1, -6, -1):
  print(f"{fib[i]} / {fib[i-1]} = {fib[i] / fib[i-1]}")
 

10) A partir de la variable cadena ya dada, mostrar en qué posiciones aparece la letra "n"<br>

cadena = 'Hola Mundo. Esto es una practica del lenguaje de programación Python'
for index, character in enumerate(cadena):
  if character == "n":
    print(index)

11) Crear un diccionario e imprimir sus claves utilizando un iterador

dictionary = {"clave1": 3, "clave2":6, "clave3":9, "clave4":12}
for key in dictionary.keys():
  print(key)

12) Convertir en una lista la variable "cadena" del punto 10 y luego recorrerla con un iterador 

lst_cadena = list(cadena)
for i in lst_cadena:
  print(i)

13) Crear dos listas y unirlas en una tupla utilizando la función zip

lst1 = ["verde", "azul", "rojo"]
lst2 = ["amarillo", "naranja", "violeta", "cyan", "magenta"]
tup = zip(lst1, lst2)
print(tup)

14) A partir de la siguiente lista de números, crear una nueva sólo si el número es divisible por 7<br>
lis = [18,21,29,32,35,42,56,60,63,71,84,90,91,100]

lst_7 = [num for num in lis if num % 7 == 0]

15) A partir de la lista de a continuación, contar la cantidad total de elementos que contiene, teniendo en cuenta que un elemento de la lista podría ser otra lista:<br>
lis = [[1,2,3,4],'rojo','verde',[True,False,False],['uno','dos','tres']]

print(len(lis))

counter = 0
for element in lis:
  if type(lis) == list:
    counter += len(lis)
  else:
    counter ==1

16) Tomar la lista del punto anterior y convertir cada elemento en una lista si no lo es

for index, element in enumerate(lis):
  if type(element) != list:
    lis[index] = list(element)

