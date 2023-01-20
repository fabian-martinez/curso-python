# Curso de Python

###Variables en python
- Las variables en python es recomendado usar camel_case.
- Las variables son key sensitive
- Para edefinirlas se recomienda usa espacios `var_name = "var_value"`
- Asignar el mismo valor a diferentes variables:
~~~
a = b = c = 10
a, b, c = 1, 2, 3 // a = 1, b = 2, c = 3
~~~
- Identificare el espacio en memoria de una variable podemos usar `id(var_name/var_value)`
- el valor y las variables con dicho valor comparten recursos en memoria
~~~
a = 10
b = 10
id(10) = <id-1>
id(a) = <id-1>
id(b) = <id-1>
~~~

###Tipos de datos
- string
- numbers
- booleans
- lists
- sets
- frozensets
- tuples
- ranges
- dictionary
- None

Los datos pueden ser:
 - Mutable: Puede cambiar despues de su creación
 - Inmutables: No puede cambiar despues de sucreación

 ### strings
 Se pueden crear strings de una linea `var_string = "Este es un string"` o `var_string = 'Este es un string'`
 o se puede hacer de varias lineas:
 ~~~
 var_string_multiline = '''Hola,
 Este es un string
 Multilinea'''
 ~~~
 o con caracter de salto de linea `\n`, asi: `var_string_multiline = "Hola, \nEste es un string \nMultilinea"`

 En multilinea puedo evitar el salto de linea con un `\` al finaliar cada linea:
 ~~~
 var_string_multiline = '''Hola, \
 Este es un string \
 Multilinea'''
 ~~~
 Imprime `Hola, Este es un string Multilinea`

 ### indice de los strings

Los strings son arreglos de caracteres y estos que inicial en el indice 0. Para acceser a un caracter especifico del indice es posible mediante `[]` asi

~~~
string1 = "Cisco Router"
string1[0] // retorna C
string1[2] // retorna s
string1[5] // Retorna espacio
~~~
en case de que se quiera retornar a la inversa se pueden usar indices de negativos:
~~~
string1[-1] // Retorna r
string1[-4] // Retorna u
~~~

Si quieremos saber el tamaño del estring usamos el metodo `len(string)`




