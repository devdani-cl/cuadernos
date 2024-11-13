# Listas enlazadas.

¿Qué es una lista enlazada?
- Una lista enlazada consta de un número de nodos con dos componentes (campos), un enlace al siguiente nodo de
la lista y un valor, que puede ser de cualquier tipo.

![image](https://github.com/user-attachments/assets/7900d502-e09a-4b21-843e-1e4babf4ac60)

El nodo consta de dos campos, el primero que es donde esta el dato (de cualquier tipo) y un puntero que apunta, señala,
desreferencia al siguiente nodo hasta que termine la lista (pueden ser n nodos). Las listas enlazadas son estructuras
de datos dinámicas. 

Una estructura nodo se declara de la siguiente manera. 
```cpp
struct Nodo {
  int dato;
  Nodo *siguiente;
};
```
## Clasificación de listas enlazadas

1. Lista simplementes enlazada
2. Lista doblemente enlazada
3. Lista circular simplemente enlazada
4. Lista circular doblemente enlazada

## Listas simplemente enlazadas

- Cada nodo (elemento) contiene un único enlace que conecta ese nodo al nodo siguiente o nodo sucesor.
La lista es eficiente en recorridos directos (<<adelante>>).
_"el nodo al puntero siguiente apunta al nodo que le sigue el que esta delante"_
![image](https://github.com/user-attachments/assets/027044df-0e20-4b67-ac45-ac3a04555547)

## Listas doblemente enlazadas
- Cada nodo contiene dos enlaces, uno a su nodo predecesor y el otro a su nodo sucesor. La lista es eficiente
  tanto en recorrido directo (<<adelante>>) como en recorrido inverso (<<atrás>>)
  _"tiene el puntero siguiente y el anterior, se puede recorrer en ambas direcciones"_
  ![image](https://github.com/user-attachments/assets/b46ae3f0-bc61-4f31-ab21-38ede743f7c8)

## Listas circular simplemente enlazada 
- Una lista enlazada simplemente en la que el último elemento de la lista (cola) se enlaza al primer elemento (cabeza)
  de tal modo que la lista puede ser recirruda de modo o¿circular (<<en anillo>>)
  _"el ultimo elemento apunta al primer elemento de la fila"_
  ![image](https://github.com/user-attachments/assets/f9fc10cb-2381-45aa-b8aa-8e62718b1665)

## Listas circular doblemente enlazada
- Una lista doblemente enlazada en la que el último elemento se enlaza al primer elemento y viceversa. Esta
  lista se puede recorrer de modo circular (en anillo) tanto en direcciín directa (<<adelante>>) como inversa (<<atrás>>).
  _""_
  ![image](https://github.com/user-attachments/assets/68d3a71e-4568-4e7a-b88b-97a2012f24d5)

# Operaciones en listas enlazadas

- Insertar elementos en una lista enlazada.
- Mostras los elementos de una lista enlazada.
- Buscar un elemento en una lista enlazada.
- Eliminar un elemento en una lista enlazada.
