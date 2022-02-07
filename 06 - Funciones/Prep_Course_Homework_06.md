## Funciones

1) Crear una función que reciba un número como parámetro y devuelva si True si es primo y False si no lo es

def is_prime(num):
  """
  checks if num is prime
  param: num: int

  return: boolean
  """
  if num == 2:
    return True
  if num < 2 or num %2 == 0:
    return False
  round_square = round(num**(1/2))
  for i in range(3, round_square, 2):
    if num % i == 0:
      return False
  return True

is_prime(137)
is_prime(133)

2) Utilizando la función del punto 1, realizar otra función que reciba de parámetro una lista de números y devuelva sólo aquellos que son primos en otra lista

def leave_only_primes(lst):
  """
  given a list of numbers returns a list with only the ones that are prime
  param: lst: list

  return: lst_primes : list
  """
  lst_primes =  [num for num in lst if is_prime(num)]
  return lst_primes

leave_only_primes(list(range(105)))

3) Crear una función que al recibir una lista de números, devuelva el que más se repite y cuántas veces lo hace. Si hay más de un "más repetido", que devuelva cualquiera

lst = [1,2,3,4,5,6,2,3,2,3,2,3,2]

def the_most_repeated(lst):
  """
  Given a list of number returns the number that repeats the most and how many times. 
  If they are two or more with the same frequency, returns any.

  param lst: list
  return number, frequency : int, int
  """
  frequencies = {}
  for num in lst:
    frequencies[num] = frequencies.get(num, 0) + 1
  
  frequency = 0
  for key, value in frequencies.items():
    if value > frequency:
      frequency = value
      number = key
  return number, frequency




4) A la función del punto 3, agregar un parámetro más, que permita elegir si se requiere el menor o el mayor de los mas repetidos.

lst.append(3)
def the_most_repeated(lst, num_repeated_biggest=True):
  """
  Given a list of number returns the number that repeats the most and how many times. 
  If they are two or more with the same frequency, returns the biggest by default or if the second parameter is True, and the smallest if it is False.

  param lst: list
  param num_repeated_biggest: boolean
  return number, frequency : int, int
  """
  frequencies = {}
  for num in lst:
    frequencies[num] = frequencies.get(num, 0) + 1
  
  frequency = 0
  for key, value in frequencies.items():
    if value > frequency:
      frequency = value
      number = key
    if value == frequency:
      if num_repeated_biggest and key > number:
        frequency = value
        number = key
      elif not num_repeated_biggest and key < number:
        frequency = value
        number = key
  return number, frequency

5) Crear una función que convierta entre grados Celsius, Farenheit y Kelvin<br>
Fórmula 1	: (°C × 9/5) + 32 = °F<br>
Fórmula 2	: °C + 273.15 = °K<br>
Debe recibir 3 parámetros: el valor, la medida de orígen y la medida de destino

def temperature_converter(value, orig, dest):
  """
  given a value, and origin and a destination scale the function converts it to the correct number
   param: value int, float
   param: orig str, "c", "f", or "k"
   param: dest str, "c", "f", or "k"

   return float
  """
  possible_scales = ["c", "f", "k"]
  if orig not in possible_scales or dest not in possible_scales:
    return "Error el segundo o tercer parametro deben ser 'c', 'f' o 'k'"
  elif orig == dest:
    return value
  elif orig == "f":
    c = (value - 32)*(5/9)
    if dest == "c":
      return c
    else:
      return c + 273.15
  elif orig == "k":
    c = value - 273.15
    if dest == "c":
      return c
    else:
      return (c*(9/5)) + 32
  elif orig == "c":
    if dest == "k":
      return value + 273.15
    else:
      return (value * (9/5)) + 32

6) Iterando una lista con los tres valores posibles de temperatura que recibe la función del punto 5, hacer un print para cada combinación de los mismos:

lst = ["c", "k", "f"]

lst2 = [i+j for i in lst for j in lst]

7) Armar una función que devuelva el factorial de un número. Tener en cuenta que el usuario puede equivocarse y enviar de parámetro un número no entero o negativo

#recursive factorial
def factorial(num):
  if num < 0 or type(num) != int:
    return "Error, para hallar un factorial el numer debe ser un entero no negativo!"
  if num == 0:
    return 1
  return num* factorial(num-1)

#iteration factorial
def factorial(num):
  if num < 0 or type(num) != int:
    return "Error, para hallar un factorial el numer debe ser un entero no negativo!"
  elif num == 0:
    return 1
  fact = 1
  for i in range(1, num + 1):
    fact *= i
  return fact
