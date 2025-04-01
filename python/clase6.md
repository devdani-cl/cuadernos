Clase 6. 

Objetivo: Manejar una lista de diccionario

- todo lo de la bodega al puerto

```py
import json
    
with open ('objetos.json', 'r') as archivo:
    bodega = json.load(archivo)

list_bodega = []
puerto = []
viajes = []

with open ('barcos.json', 'r') as archivo:
    barcos = json.load(archivo)

for barco in barcos:
    for objeto in bodega:
        espacio_disponible = barco["espacio"]
        if barco["espacio"] > 0 and barco["espacio"] >= objeto["espacio"]:
            barco["bodega"].append(objeto)
            
            barco["espacio"] = objeto["espacio"]
        break
    break
print(barco)


```


Lógica de código:

- importar json
- abrir y leer los archivos
- asignar una variable al archivo y luego recorrer
-  
