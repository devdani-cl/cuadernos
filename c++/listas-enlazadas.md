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
# Clasificación de listas enlazadas

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

## Insertar elementos en una lista
- Para insertar elementos en una lista es necesario hacer lo siguiente.
1. Crear un nuevo nodo.
2. Asignar a nuevo_nodo -> dato el elemento que queremos incluir a la lista.
3. Crear dos nodos auxiliares y asignar lista al primero de ellos.
4. Insertar el elemento a la lista.

## Crear un nuevo nodo.
![image](https://github.com/user-attachments/assets/2d469b07-5cc0-4ed2-a20c-36eb3fd89692)

```cpp
void insertarLista(Nodo *&lista, int n) {
  Nodo *nuevo_nodo = new Nodo();
}
```
## Asignar a nuevo_nodo -> dato el elemento que queremos incluir a la lista.
```cpp
struct Nodo {
  int dato;
  Nodo *siguiente;
};
```
_"Acá es en la función principal"_
```cpp
void insertarLista(Nodo *&lista, int n){
  Nodo *nuevo_nodo = new Nodo();
  nuevo_nodo -> dato = n;
}
```

## Crear dos nodos auxiliares y asignar lista al primero de ellos.
![image](https://github.com/user-attachments/assets/a80310ff-c495-4256-9862-d85a34614db7)

```cpp
void insertarLista(Nodo *&lista, int n){
  Nodo *nuevo_nodo = new Nodo();
  nuevo_nodo -> dato = n;

  Nodo *aux1 = lista;
  Nodo *aux2;
  
```

## Insertar el elemento a la lista.
Vamos a tener tres casos de listas:
![image](https://github.com/user-attachments/assets/b4ecc361-9637-4f65-aace-b6690e44bf96)

- Cuando la lista esta vacía (Lista -> null)
- Cuando ya tengamos un Nodo _"vamos a tener dos posiciones que agregar, al inicio y al final"_
- Cuando tengamos dos o más nodos _"en este caso se agregar al inicio al medio o al final el nodo que queremos incluir a la lista"_

- _"recordar prioritariamente que tenemos dos casos al principio, en medio o al final, crear la lista de tal manera que el elemento que se inserta sea de manera ordenada y ascendente "_

¿Cómo insertar elementos al principio de la lista?

¿Cómo insertar elementos al medio o al final de la lista?


## Código final.

```cpp
void insertarLista(Nodo *&lista, int n){
  Nodo *nuevo_nodo = new Nodo();
  nuevo_nodo -> dato = n;

  Nodo *aux1 = lista;
  Nodo *aux2;

  while ((aux1 != NULL) && (aux1 -> dato < n)){
    aux2 = aux1;
    aux1 = aux1 ->siguiente;
  }
  if (lista == aux1){
    lista = nuevo_nodo;
  }
  else {
    aux2 -> siguiente = nuevo_nodo;
  }

  nuevo_nodo -> siguiente = aux1;
  std::cout << "\tElemento " << n << "insertado correctamente!\n";
}
```

En la función principal tenemos que crear la variable puntero lista e igualarlo a NULL.

```cpp
int main (){
  Nodo *lista = NULL;

  std::cout << "digita un número: ";
  std::cin >> dato;
  insertarLista(lista, dato);

  getch();
  return 0;
```

## Código de listas enlazadas.

```cpp
#include <iostream>

struct Nodo {
    int dato;
    Nodo *siguiente;
};

void insertarLista(Nodo *&lista, int n) {
    // crear un nuevo nodo y asignar el valor 'n'
    Nodo *nuevo_nodo = new Nodo();
    nuevo_nodo->dato = n;

    Nodo *aux1 = lista;
    Nodo *aux2 = nullptr;

    // recorrer la lista para encontrar la posición correcta de inserción
    while ((aux1 != nullptr) && (aux1->dato < n)) {
        aux2 = aux1;
        aux1 = aux1->siguiente;
    }

    // insertar al inicio si corresponde
    if (lista == aux1) {
        lista = nuevo_nodo;
    } else {
        aux2->siguiente = nuevo_nodo;
    }
    // enlazar el nuevo nodo con el siguiente
    nuevo_nodo->siguiente = aux1;
}

void mostrarLista(Nodo *lista) {
    Nodo *actual = lista;
    std::cout << "Lista ordenada: ";
    while (actual != nullptr) {
        std::cout << actual->dato << " ";
        actual = actual->siguiente;
    }
    std::cout << std::endl;
}

void liberarLista(Nodo *&lista) {
    Nodo *aux;
    while (lista != nullptr) {
        aux = lista;
        lista = lista->siguiente;
        delete aux;
    }
}

int main() {
    Nodo *lista = nullptr;
    int dato;

    std::cout << "Ingrese números enteros (ingrese 0 para terminar):" << std::endl;
    std::cout << "Número: ";
    std::cin >> dato;

    while (dato != 0) {
        insertarLista(lista, dato);
        std::cout << "Número: ";
        std::cin >> dato;
    }

    mostrarLista(lista);

    // liberar la memoria utilizada por la lista
    liberarLista(lista);

    return 0;
}
```

Ejemplo de código de usos de lista enlazadas.

```cpp
#include <iostream>
#include <string>

struct Contacto {
    std::string nombre;
    std::string telefono;
    std::string correo;
    Contacto *siguiente;
    Contacto *anterior;
};

void insertarContacto(Contacto *&inicio, Contacto *&fin, const std::string &nombre, const std::string &telefono, const std::string &correo) {
    Contacto *nuevo_contacto = new Contacto();
    nuevo_contacto->nombre = nombre;
    nuevo_contacto->telefono = telefono;
    nuevo_contacto->correo = correo;
    nuevo_contacto->siguiente = nullptr;
    nuevo_contacto->anterior = nullptr;

    // Si la lista está vacía
    if (inicio == nullptr) {
        inicio = fin = nuevo_contacto;
    } else {
        // Inserta al final de la lista
        fin->siguiente = nuevo_contacto;
        nuevo_contacto->anterior = fin;
        fin = nuevo_contacto;
    }
}

void mostrarAgenda(Contacto *inicio) {
    Contacto *actual = inicio;
    while (actual != nullptr) {
        std::cout << "Nombre: " << actual->nombre << ", Teléfono: " << actual->telefono << ", Correo: " << actual->correo << std::endl;
        actual = actual->siguiente;
    }
}

void liberarAgenda(Contacto *&inicio) {
    Contacto *aux;
    while (inicio != nullptr) {
        aux = inicio;
        inicio = inicio->siguiente;
        delete aux;
    }
}

int main() {
    Contacto *inicio = nullptr;
    Contacto *fin = nullptr;

    insertarContacto(inicio, fin, "Juan Pérez", "1234567890", "juan@example.com");
    insertarContacto(inicio, fin, "María López", "0987654321", "maria@example.com");

    std::cout << "Agenda de Contactos: " << std::endl;
    mostrarAgenda(inicio);

    liberarAgenda(inicio);
    return 0;
}

```
