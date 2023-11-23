# Reto 12: Strings

## Punto uno

Consulte que hacen los siguientes métodos de strings en python: endswith, startswith, isalpha, isalnum, isdigit, isspace, istitle, islower, isupper.

### endswith
**Funcionalidad**

Retorna *True* cuando el string termina con el valor especificado. En el caso contrario, retorna *False*. 

**Sintaxis**

*string.endswith(value,start,end)*

*start* y *end* son opcionales; se usan en caso de que se quiera especificar la posición en la que se quiere aplicar el método.

**Ejemplo**

```
string="Hola, mi nombre es Paula"
print(string.endswith("Paula"))
#output:True
```
### startswith
**Funcionalidad**

Retorna *True* cuando el string comienza con el valor especificado. En el caso contrario, retorna *False*.

**Sintaxis**

*string.startswith(value,start,end)*

*start* y *end* son opcionales; se usan en caso de que se quiera especificar la posición en la que se quiere aplicar el método.

**Ejemplo**

```
string="Estoy muy feliz"
print(string.startswith("muy",6,9))
#output:True
```
### isalpha
**Funcionalidad**

Retorna *True* cuando todos los caracteres del string son letras (caracteres alfabéticos). En el caso contrario, retorna *False*.

**Sintaxis**

*string.isalpha()*

**Ejemplo**

```
string="AsdFGHjklñ"
print(string.isalpha())
#output:True
```
### isalnum
**Funcionalidad**

Retorna *True* cuando todos los caracteres del string son letras (caracteres alfabéticos) y/o dígitos numéricos. En el caso contrario, retorna *False*.

**Sintaxis**

*string.isalnum()*

**Ejemplo**

```
string="Hola mundo 123"
print(string.isalnum)
#output:False
```
### isdigit
**Funcionalidad**

Retorna *True* cuando todos los caracteres del string son dígitos numéricos. En el caso contrario, retorna *False*.

**Sintaxis**

*string.isdigit()*

**Ejemplo**

```
string=chr(50)
print(string.isdigit())
#output:True
```
### isspace
**Funcionalidad**
Retorna *True* cuando todos los caracteres del string son espacios. En el caso contrario, retorna *False*.

**Sintaxis**

*string.isspace()*

**Ejemplo**

```
string="    -     "
print(string.isspace())
#output:False
```
### istitle
**Funcionalidad**

Retorna *True* cuando todas las palabras del string tienen su primera letra en mayúscula y el resto de las letras en minúscula. En el caso contrario, retorna *False*. Este método solo revisa los caracteres del abecedario, es decir, ignora los símbolos, números y espacios.

**Sintaxis**

*string.istitle()*

**Ejemplo**

```
string="Harry Potter Y Las Reliquias De La Muerte - Parte 1"
print(string.istitle())
#output:True
```
### islower
**Funcionalidad**

Retorna *True* cuando todos los caracteres del string están en minúsculas. En el caso contrario, retorna *False*. Este método solo revisa los caracteres del abecedario, es decir, ignora los símbolos, números y espacios.

**Sintaxis**

*string.islower()*

**Ejemplo**

```
string="mi nombre es Paula"
print(string.islower())
#output:False
```
### isupper
**Funcionalidad**

Retorna *True* cuando todos los caracteres del string están en mayúsculas. En el caso contrario, retorna *False*. Este método solo revisa los caracteres del abecedario, es decir, ignora los símbolos, números y espacios.

**Sintaxis**

*string.isupper()*

**Ejemplo**

```
string="CIEN AÑOS DE SOLEDAD"
print(string.isupper())
#output:True
```

## Punto dos

Procesar el archivo y extraer:
* Cantidad de vocales
* Cantidad de consonantes

**Código cantidad de vocales**

```
def cantidadVocales(archivo)->int:#Creando función para contar la cantidad de vocales
    vocales:int=0#Declarando variable que servirá para contar las vocales, se inicializa en 0
    for i in archivo:#Para cada letra que se encuentra en el archivo:
        if i in "aeiou" or i in "AEIOU":#Si la letra es una vocal mayúscula o minúscula...
            vocales+=1#...entonces se le suma una unidad al contador de las vocales
    return vocales#La función retorna el número final de las vocales contadas

if __name__=="__main__":#Función main
    with open('mbox-short.txt',"r") as file:#Se abre el archivo y se nombra como file
        conteoVocales=cantidadVocales(file.read())#Se llama a la función cantidadVocales, para aplicar la función en el file
        print("El archivo tiene {} vocales".format(conteoVocales))#Se imprime la cantidad de vocales que hay en el archivo
```

**Código cantidad de consonantes**

```
def consonantes(archivo):#Creando función para contar la cantidad de consonantes
    cons:int=0#Declarando variable que servirá para contar las consonantes, se inicializa en 0
    for i in archivo:#Para cada letra que se encuentra en el archivo:
        if i in "bcdfghjklmnñpqrstvwxyz" or i in "BCDFGHJKLMNÑPQRSTVWXYZ":#Si la letra es una consonantes mayúscula o minúscula...
            cons+=1#...entonces se le suma una unidad al contador de las consonantes
    return cons#La función retorna el número final de las consonantes contadas
if __name__=="__main__":#Función main
    with open("mbox-short.txt","r") as file:#Se abre el archivo y se nombra como file
        conteoConsonantes=consonantes(file.read())#SE llama a la función consonantes, para aplicar la función en el file
        print("El archivo tiene {} consonantes.".format(conteoConsonantes))#Se imprime la cantidad de consonantes que hay en el archivo
```
