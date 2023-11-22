# Reto 12: Strings

## Punto uno

Consulte que hacen los siguientes métodos de strings en python: endswith, startswith, isalpha, isalnum, isdigit, isspace, istitle, islower, isupper.

### Endswith
**Funcionalidad**

Retorna True cuando el string termina con el valor especificado. En el caso contrario, retorna False. 

**Sintaxis**

*string.edswith(value,start,end)*

*start* y *end* son opcionales; se usan en caso de que se quiera especificar la posición en la que se quiere aplicar el método.

**Ejemplo**

```
string="Hola, mi nombre es Paula"
print(string.endswith("Paula"))
#output:True
```


## Punto dos

Procesar el archivo y extraer:
* Cantidad de vocales
* Cantidad de consonantes
