## Variables

1) Crear una variable que contenga un elemento del conjunto de números enteros y luego imprimir por pantalla

integer = 13
print(13)

2) Imprimir el tipo de dato de la constante 8.5

print(type(8.5))

3) Imprimir el tipo de dato de la variable creada en el punto 1

print(type(integer))

4) Crear una variable que contenga tu nombre

my_name = "Nelson"

5) Crear una variable que contenga un número complejo

complex_number = complex(3, 5) 

6) Mostrar el tipo de dato de la variable crada en el punto 5

print(type(complex_number))

7) Crear una variable que contenga el valor del número Pi redondeado a 4 decimales

import math
number_PI = round(math.pi, 4)

8) Crear una variable que contenga el valor 'True' y otra que contenga el valor True. ¿Se trata de lo mismo?

string_true = "True"
boolean_true = True
#son diferentes el primero es un string que contiene los caracteres para formar la palabra True el segundo es un booleano que represente un valor verdadero

9) Imprimir el tipo de dato correspondientes a las variables creadas en el punto 9

print(type(string_true))
print(type(boolean_true))

10) Asignar a una variable, la suma de un número entero y otro decimal

sum_int_float = 3 + 4.522

11) Realizar una operación de suma de números complejos

print(complex(3, 5) + complex(2, 10))

complex_number_1 = complex(3, 5) + complex(2, 10)

complex_1 = complex(3, 5)
complex_2 = complex(2, 10)
complex_number_2 = complex_1 + complex_2
print(complex_number2)

real_part_1 = complex_1.real
real_part_2 = complex_2.real
imag_part_1 = complex_1.imag
imag_part_2 = complex_2.imag
complex_number_real = real_part_1 + real_part_2
complex_number_imag = imag_part_1 + imag_part_2
complex_number_3 = complex(complex_number_real, complex_number_imag)
print(complex_number3)

12) Realizar una operación de suma de un número real y otro complejo

print(complex(3, 2) + 7)

print(complex(complex_1.real + 13, 2))

13) Realizar una operación de multiplicación

print(3*7)

14) Mostrar el resultado de elevar 2 a la octava potencia

print(2**8)

15) Obtener el cociente de la división de 27 entre 4 en una variable y luego mostrarla

quotient = 9523235 / 2425
print(quotient)

16) De la división anterior solamente mostrar la parte entera

integer_part = 9523235 // 2425
print(integer_part)

17) De la división de 27 entre 4 mostrar solamente el resto

remainder = 9523235 % 2425
print(remainder)

18) Utilizando como operandos el número 4 y los resultados obtenidos en los puntos 16 y 17. Obtener 27 como resultado

print((integer_part// remainder) + 4*3)

19) Utilizar el operador "+" en una operación donde intervengan solo variables alfanuméricas

first_part = "kranken"
second_part = "wagen"
print(first_part + second_part)

20) Evaluar si "2" es igual a 2. ¿Por qué ocurre eso?

print("2" == 2)
#no son iguales por que "2" es un string y 2 es un entero, son tipos de datos diferente en python por lo que no pueden ser iguales
print(type("2"))
print(type(2))
print(type("2") == type(2))

21) Utilizar las funciones de cambio de tipo de dato, para que la validación del punto 20 resulte verdadera

print(int("2") == 2)
print("2" == str(2))

22) ¿Por qué arroja error el siguiente cambio de tipo de datos? a = float('3,8')

#la forma de denotar decimales es un con .  no una coma al parsear el string 3,8 float no lo interpreta como un decimal ( la , para separar decimales es usada en paises de habla hispana y general altos dolores de cabeza
#en programas como excel o hojas de calculo a la hora de usar datos si estos no fuera limpiados correctamente)

23) Crear una variable con el valor 3, y utilizar el operador '-=' para modificar su contenido

number_three = 3
number_three -= 2

24) Realizar la operacion 1 << 2 ¿Por qué da ese resultado? ¿Qué es el sistema de numeración binario?

print(1<<2) 

#<< es un operador bitwise que "corre" los bits de objeto a la izquierda una cantidad exacta indicada a la derecha en este caso 1 representado en binario por ejemplo como 0000 0001 (dependiente de la arquitectura del computador)
#se correra hacia la izquierda 2 espacios indicados por el 2, lo que resultara en 0000 0100 que es 4 en binario y por eso el resultado es 4, por ejemplo 1<<7 sera 1128 1000 0000 y 128 >> 4 sera 0000 1000 que es 8

25) Realizar la operación 2 + '2' ¿Por qué no está permitido? ¿Si los dos operandos serían del mismo tipo, siempre arrojaría el mismo resultado? 

#no esta permitido por que son de tipo diferente uno es un string el otro es un entero al sumar enteros el resultado sera la suma 2 + 2 = 4 pero al sumar string el resultado sera la concatenacion de los strings "2" + "2" = "22"

26) Realizar una operación válida entre valores de tipo entero y string

print("Repetir 3 veces. "*3)