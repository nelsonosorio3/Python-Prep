## Flujos de Control

1) Crear una variable que contenga un elemento del conjunto de números enteros y luego imprimir por pantalla si es mayor o menor a cero

integer = 324
if integer > 0:
  print("Es mayor que 0")
elif integer < 0:
  print("Es menor que 0")
else:
  print("Es 0")

2) Crear dos variables y un condicional que informe si son del mismo tipo de dato

var_1 = "2"
var_2 = 2

if type(var_1) == type(var_2):
  print("Son el mismo tipo de dato")
else:
  print("No son el mismo tipo de dato")

3) Para los valores enteros del 1 al 20, imprimir por pantalla si es par o impar

for i in range(1,21):
  if i % 2 == 0:
    print(f"{i}, Es par")
  else:
    print(f"{i}, Es impar")

4) En un ciclo for mostrar para los valores entre 0 y 5 el resultado de elevarlo a la potencia igual a 3

for i in range(6):
  print(f"{i} elevado al cubo es {i**3}")

5) Crear una variable que contenga un número entero y realizar un ciclo for la misma cantidad de ciclos

number_times = 15
counter = 0
for i in range(number_times):
  print(i)
  counter +=1 

print(counter)

6) Utilizar un ciclo while para realizar el factoreo de un número guardado en una variable, sólo si la variable contiene un número entero mayor a 0

var_1 = -2
var_2 = 3
var_3 = 45
var_4 = 9
var_5 = 1

prime_factors = []

while var_3 > 1:
  if var_3 % 2 == 0:
    var_3 /= 2
    prime_factors.append(2)
  elif var_3 % 3 == 0:
    var_3 /= 3
    prime_factors.append(3)
  elif var_3 % 5 == 0:
    var_3 /= 5
    prime_factors.append(5)
  elif var_3 % 7 == 0:
    var_3 /= 7
    prime_factors.append(7)
  elif var_3 % 11 == 0:
    var_3 /= 11
    prime_factors.append(11)
  elif var_3 % 13 == 0:
    var_3 /= 13
    prime_factors.append(13)
  elif var_3 % 17 == 0:
    var_3 /= 17
    prime_factors.append(17)
  elif var_3 % 19 == 0:
    var_3 /= 19
    prime_factors.append(19)
  elif var_3 % 23 == 0:
    var_3 /= 23
    prime_factors.append(23)
  elif var_3 % 29 == 0:
    var_3 /= 29
    prime_factors.append(29)
  elif var_3 % 31 == 0:
    var_3 /= 31
    prime_factors.append(31)
  else:
    prime_factors.append(var_3)
    break

print(prime_factors)
#solucion solo para unos cuestos numeros y descomponiendo en factores primos

#intentar usar list comprehension para hallar todos los factores de un numero entero positivo

var_4 = 45
if var_4 >0 and type(var_4) == int:
  factors = [i for i in range(2, var_4+1) if var_4%i == 0]
  print(factors)
else:
  print("El numero no es un entero positivo")


7) Crear un ciclo for dentro de un ciclo while

counter = 0
while counter < 3:
  for i in range(10):
    print(i*counter)
  counter +=1

8) Crear un ciclo while dentro de un ciclo for


for i in range(10):
  counter = 0
  while counter < 3:
    print(i*counter)
    counter += 1

9) Imprimir los números primos existentes entre 0 y 30

primes = []
for i in range(2, 31):
  is_prime = True
  for prime in primes:
    if i % prime == 0:
      is_prime = False
  if is_prime:
    print(i)
    primes.append(i)

10) ¿Se puede mejorar el proceso del punto 9? Utilizar las sentencias break y/ó continue para tal fin

primes = []
for i in range(2, 31):
  is_prime = True
  for prime in primes:
    if i % prime == 0:
      is_prime = False
      break
  if is_prime:
    print(i)
    primes.append(i)

11) En los puntos 9 y 10, se diseño un código que encuentra números primos y además se lo optimizó. ¿Es posible saber en qué medida se optimizó?

#es posible agregar un print para llevar el conteno de cuantas veces se ejecuta uno vs el otro 

counter = 0

primes = []
for i in range(2, 31):
  is_prime = True
  for prime in primes:
    counter +=1
    if i % prime == 0:
      is_prime = False
  if is_prime:
    print(i)
    primes.append(i)

print(counter) 
#el bucle intero se es ejecutado 171 veces 

counter = 0
primes = []
for i in range(2, 31):
  is_prime = True
  for prime in primes:
    counter +=1
    if i % prime == 0:
      is_prime = False
      break
  if is_prime:
    print(i)
    primes.append(i)

print(counter) 
#el bucle interno es ejectado 70 veces

#existen otras optimizaciones que se puede hacer por ejemplo el unico primo par es 2 asi que enves de avaluar cada numero podemos evaluar solo cada 2
counter = 0
primes = [2]
print(2)
for i in range(3, 31, 2):
  is_prime = True
  for prime in primes:
    counter +=1
    if i % prime == 0:
      is_prime = False
      break
  if is_prime:
    print(i)
    primes.append(i)

print(counter) 
#el bucle interno es ejectado 56 veces

#si quisieramos solo una lista de primos podriamos omitir el dos y luego agregarla al comienzo
counter = 0
primes = []
print(2)
for i in range(3, 31, 2):
  is_prime = True
  for prime in primes:
    counter +=1
    if i % prime == 0:
      is_prime = False
      break
  if is_prime:
    print(i)
    primes.append(i)

primes = [2] + primes
print(counter) 
#el bucle interno es ejectado 42 veces

12) Si la cantidad de números que se evalúa es mayor a treinta, esa optimización crece?

#conforme mas aumenta el numero que queremos evaluar esta optimizacion es mayor y ahorra mas tiempo de ejecucion

13) Aplicando continue, armar un ciclo while que solo imprima los valores divisibles por 12, dentro del rango de números de 100 a 300

number = 300
while number > 99:
  if number % 12 == 0:
    print(number)
    number -=12
    continue
  number-=1

14) Utilizar la función **input()** que permite hacer ingresos por teclado, para encontrar números primos y dar la opción al usario de buscar el siguiente


num = 2;
while num != 0:
  num = int(input(f"Primos hasta el momento, {primes}. Hasta que numero quieres encontar los primos? o presiona 0 para terminar: "))
  primes = [2]
  for i in range(3, num + 1, 2):
    is_prime = True
    for prime in primes:
      if i % prime == 0:
        is_prime = False
        break
    if is_prime:
      primes.append(i)

15) Crear un ciclo while que encuentre dentro del rango de 100 a 300 el primer número divisible por 3 y además múltiplo de 6

number = 100
while number < 301:
  if number % 6 == 0:
    print(number)
    break
  number +=1