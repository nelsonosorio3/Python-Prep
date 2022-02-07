## Estructuras de Datos

1) Crear una lista que contenga nombres de ciudades del mundo que contenga más de 5 elementos e imprimir por pantalla

cities = ["Bogota", "Buenos Aires", "La Paz", "Londres", "Beijing"]
print(cities)

2) Imprimir por pantalla el segundo elemento de la lista
print(cities[1])

3) Imprimir por pantalla del segundo al cuarto elemento

print(cities[1:4])

4) Visualizar el tipo de dato de la lista

print(type(cities))

5) Visualizar todos los elementos de la lista a partir del tercero de manera genérica, es decir, sin explicitar la posición del último elemento

print(cities[2:])

6) Visualizar los primeros 4 elementos de la lista

print(cities[:4])

7) Agregar una ciudad más a la lista que ya exista y otra que no ¿Arroja algún tipo de error?

cities.append("Berlin")
cities.append("Buenos Aires")

8) Agregar otra ciudad, pero en la cuarta posición

cities.insert(3, "Sofia")

9) Concatenar otra lista a la ya creada

more_cities = ["Madrid", "Istanbul", "Tokyo", "Sidney"]
cities2 = cities + more_cities
cities.extend(more_cities)

10) Encontrar el índice de la ciudad que en el punto 7 agregamos duplicada. ¿Se nota alguna particularidad?

cities.index("Buenos Aires")
#regresa la primera instancia solamente

11) ¿Qué pasa si se busca un elemento que no existe?

cities.index("No existe")
#regresa valueError is not in list

12) Eliminar un elemento de la lista

cities.remove("Buenos Aires")
print(cities)

#remueve solo la primera instancia


13) ¿Qué pasa si el elemento a eliminar no existe?

cities.remove("no")
#value Error  x not in list

14) Extraer el úlimo elemento de la lista, guardarlo en una variable e imprimirlo

last_city = cities.pop()
print(last_city)

15) Mostrar la lista multiplicada por 4

print(cities*4)

16) Crear una tupla que contenga los números enteros del 1 al 20

int_1_to_20 = tuple(range(1, 21))
print(int_1_to_20)

17) Imprimir desde el índice 10 al 15 de la tupla

print(int_1_to_20[10:16])

18) Evaluar si los números 20 y 30 están dentro de la tupla

print(20 in int_1_to_20)
print(30 in int_1_to_20)

19) Con la lista creada en el punto 1, validar la existencia del elemento 'París' y si no existe, agregarlo. Utilizar una variable e informar lo sucedido.

was_added = False
if "París" not in cities:
  cities.append("París")
  was_added = True

if was_added:
  print("Se agrego Paris a cities")
else:
  print("Paris ya esta en cities")


20) Mostrar la cantidad de veces que se encuentra un elemento específico dentro de la tupla y de la lista

print(cities.count("Buenos Aires"))
print(int_1_to_20.count(5))

21) Convertir la tupla en una lista

lst = list(int_1_to_20)
print(lst)
print(type(lst))

22) Desempaquetar solo los primeros 3 elementos de la tupla en 3 variables

first, second, third = int_1_to_20[:3]

23) Crear un diccionario utilizando la lista crada en el punto 1, asignandole la clave "ciudad". Agregar tambien otras claves, como puede ser "Pais" y "Continente".

dictionary = {
  "ciudad": cities,
  "pais": ["Colombia", "Bolivia", "Bulgaria", "Inglaterra", "China", "Alemania", "Argentina", "Spain", "Turquia", "Japon", "Francia"],
  "continente": ["America", "America", "Europa", "Europa", "Asia", "Europa", "America", "Europa", "Europa", "Asia", "Europa"]
}

24) Imprimir las claves del diccionario

print(dictionary.keys())

25) Imprimir las ciudades a través de su clave

print(dictionary["ciudad"])
