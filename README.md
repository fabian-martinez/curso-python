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
En caso de que se quiera retornar a la inversa se pueden usar indices de negativos:
~~~
string1[-1] // Retorna r
string1[-4] // Retorna u
~~~

Si quieremos saber el tamaño del estring usamos el metodo `len(string)` de esta manera:
~~~
string1 = "Cisco Router"
len(string1) // Retorna 12 
~~~

En caso de que lo que necesitemos no sepamos cual es el indice de una letra dentro del string podemos usar la función index `string.index("character")`:
~~~
string1 = "Cisco Router"
string1.index("i") // Retorna el indice de la primera letra i en el string en este caso 0
~~~

En caso de que lo que necesitemos las ocurrencias de una letra dentro del string podemos usar la función count `string.count("character")`:
~~~
string1 = "Cisco Router"
string1.count("o") // Retorna 2
~~~

En caso de que lo que necesitemos no sepamos cual es el indice de un sub string dentro del string podemos usar la función find `string.index("substring")`. En caso de no encontrarlo retorna -1.
~~~
string1 = "Cisco Router"
string1.find("sco") // Retorna el indice de la primera letra del substring en el string en este caso 2
~~~

Para transformar los string tenemos `string.lower()` y `string.upper()` para pasar todas las letras a mayusculas o a minusculas respectivamente.

Si quieres verificar el inicio o final de un string puiedes usar `string.startswith("character")` y `strings.endswith("character")` que retornan true o false si el caracter corresponde con el del string.

En el caso de que el string tiene espacios no deseados al inicio o final de este se puede usar el metodo `strimg.trim()` para eliminatrlos. En caso de que sean caraceteres se pueden eliminar poniendo el caracter en el metodo `string.trim("character")`

En caso de que se quieran remplazar mas cahracteres se puede usar el metodo `string.replace("character_in","character_out")`

Para separar in string podemos usar el metodo `string.plit("plite_character")` que genera un arreglo de strings:
~~~
string1 = "Cisco, Junper, HP, Avaya, Nortel"
string1.split(", ") // Retorna ['Cisco', 'Junper', 'HP', 'Avaya', 'Nortel']
~~~

Si al contrario se quiere unit se quiere el unir existe el metodo `string.join()` que une un caracter a cada caracter 
~~~
string1 = "Cisco Router"
"_".join(string1) // Retorna "C_i_s_c_o_ _R_o_u_t_e_r"
~~~

