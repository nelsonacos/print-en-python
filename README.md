# print-en-python
 Un pequeño tutorial sobre como usar print en python

## Imprime y agrega linea nueva luego de cada print()
```python
print( "Hola Mundo!" )
```

## Imprime respetando los espacios en blanco
```python
print( "               Es importante conocer print, es la heramienta principal de comunicacion de un programa en python " )
```

## Imprime sin agregar linea nueva
```python 
print( "Hola", end=" " )
print( "Mundo!")
```
## Agrega linea nueva
```python
print() 
```
## Imprime un lita de elementos y agrega espacio luego de cada elemento de lista
```python
print( 'Esto','imprime', 'una', 'lista', 'con', 'espacios')
```
## Imrime lista de elementos sin espacio luego de cada elemento
```python
print( 'Esto','Imprime', 'Una', 'Lista', 'Sin', 'Espacios', sep="")
```
## Imprime lista de elementos separando cada elemento por --*--
```python
print( 'Esto','imprime', 'lista', 'con', 'separador', sep="--*--")
```
## Variables para otros usos de print()
```python 
nombre = "Nelson" 
resultado = 100      
```
## print() usando substitución con %( )
```python
print( "El resultado total para %s es %s  " % (nombre, resultado) )
```
## print() usando una lista de listerales y variables
```python
print( "El resultado total para", nombre, "es", resultado )
```
## print() usando una lista de literales y variables con sep=''
```python
print( "El resultado total para ", nombre, " es ", resultado, sep='' )
```
## print() Concatenar con el operador +. Para convertir un intero a una cadena se usa el metodo str()
```python
print( "El resultado total para " + nombre + " es " + str(resultado) )
```
## Usando sustitucion con .fotmat()
```python
print( 'Los tres hermanos se llaman {0}, {1}, y {otro}.'
        .format( 'Marcos', 'Pablo', otro='Jorge') )

print( '{0}, {1}, {2}' .format( 'a', 'b', 'c' ) )
```
## Solo fubciona en python 3.1+
```python
print( '{}, {}, {}' .format( 'a', 'b', 'c' ) )  

print( '{2}, {1}, {0}' .format( 'a', 'b', 'c' ) )
```
## Cambiar un string en sus elementos
```python
print( '{2}, {1}, {0}' .format( *'abc' ) )  
```
## Se pueden repetir argumentos
```python
print( '{0}{1}{0}' .format( 'Abra', 'Cad' ) )
```
## Se pueden declarar los argumentos de manera asociativa
```python
print( 'Coordenadas: {latitud}, {longitud}' .format( latitud='37.24N', longitud='-115.81W' ) )
```
## Variables para uso de format()
```python
coord = { 'latitud': '37.24N', 'longitud': '-115.81W' }
```
## Podemos acceder al valor de las variables de esta manera
```python
print( 'Coordenadas: {latitud}, {longitud}' .format( **coord ) )
```
## Importamos el modulo math para evaluar la precision de math.pi
```python
import math
```
## Declaramos el valor de pi
```python
pi = 3.14159265
```
## Formatear cadenas con los metodos antiguos
```python
print( 'El valor de PI es más o menos %03.3f.' % (pi) ) 
```
## Cambiar el valor de la cadena
```python
print( 'El valor de -PI es más o menos %07.3f.' % (-pi) )
```
## Imprime el valor de pi declarado en la variable
```python
print( 'El valor de PI es más o menos {}.' .format( pi ) )
```
## imprime el valor del argumento 0 de format() como float con 3 decimales
```python
print( 'El valor de PI es más o menos {0:.3f}.' .format( pi ) )
```
## Imprime el valor de pi del modulo math
```python
print( 'El valor de PI es más o menos {}.' .format( math.pi ) )
```
## Imprime el valor del argumento 0 de format() como float con 3 decimales
```python
print( 'El valor de PI es más o menos {0:.3f}.' .format( math.pi ) )
```
## Imprime diccioanrio desde el ciclo for formateando pais centrdo y con 14 espacios
```python 
Capital_Pais={ "United States" : "Washington", 
               "US" : "Washington", 
               "Canada" : "Ottawa",
               "Germany": "Berlin",
               "France" : "Paris",
               "England" : "London",
               "UK" : "London",
               "Switzerland" : "Bern",
               "Austria" : "Vienna",
               "Netherlands" : "Amsterdam" }

print( "\nPaises y sus capitales:")

for c in Capital_Pais:
    print("{Pais:^14s}: {Capital}" .format( Pais=c, Capital=Capital_Pais[c] ) )
```
## Imprimir un Diccionario usando format() asociativo
```python
tabla = { 'Julio': 4127, 'Mario': 4098, 'José': 7678 }

print( "{0:10}     {1:^16}" .format( "Nombre", "Extensión" ) )
```
# Imprimir un diccionario usando el metodo items()
```python
for Nombre, Extensión in tabla.items():
  print( '{0:10} ==> {1:10d}' .format( Nombre, Extensión ) )
```
## Alineaciones de format()
```python 
print( "{0:<20s} {1:6.2f}" .format('Jamon y Huevos:', 6.99) )
print( "{0:>20s} {1:6.2f}" .format('Jamon y Huevos:', 6.99) )
print( "{0:>27s} {1:+6.2f}" .format('Jamon, Frijoles y Huevos:', 7.99) )
print( "{0:^27s} {1:6.2f}" .format('Jamon, Frijoles y Huevos:', 7.99) )
print( "{0:<20} {1: 6.2f}" .format('Jamon y Huevos:', 7.99) )
print( "{0:>20} {1:6.2f}" .format('Jamon y Huevos:', 7.99) )
print( "{0:^27} {1:=6.2f}" .format('Jamon, Frijoles y Huevos:', 7.99) )
```
## Otra manera a imprimir un Diccionario
```python
tabla = { 'Julio': 4127, 'Mario': 4098, 'José': 7678 }

print( "{0}/{1:10s}     {0}/{1:10s}    {0}/{1:10s}"
       .format( "Nombre", "Extensión" ) )

print('Mario: {Mario:<16d} Julio: {Julio:<14d} José: {José:<16d}'
       .format(**tabla))
```
## Pasar el diccionario y obtiene las llaves con []
```python
tabla = { 'Julio': 4127, 'Mario': 4098, 'José': 7678 }

print( "{0}/{1:10s}     {0}/{1:10s}    {0}/{1:10s}"

        .format( "Nombre", "Extensión" ) )
print('Mario: {0[Mario]:<16d} Julio: {0[Julio]:<14d} José: {0[José]:<16d}'
       .format(tabla))
```
## Imprime en multiples lineas
```python
print('''

| \ | | ___| |___  ___  _ __      / \   ___ ___  ___| |_ __ _ 
|  \| |/ _ \ / __|/ _ \| '_ \    / _ \ / __/ _ \/ __| __/ _` |
| |\  |  __/ \__ \ (_) | | | |  / ___ \ (_| (_) \__ \ || (_| |
|_| \_|\___|_|___/\___/|_| |_| /_/   \_\___\___/|___/\__\__,_|
                                                                
''')