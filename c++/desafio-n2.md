# Desafío 2

Crea un código en C++ que sea capaz de insertar elementos a una lista de manera ordenada.

```cpp
#include <iostream>

class Nodo {
public:
    int dato;
    Nodo* siguiente;

    Nodo(int valor) {
        dato = valor;
        siguiente = nullptr;
    }
};

class ListaEnlazada {
private:
    Nodo* cabeza;

public:
    ListaEnlazada() {
        cabeza = nullptr;
    }

    void insertarOrdenado(int valor) {
        Nodo* nuevoNodo = new Nodo(valor);

        if (cabeza == nullptr || cabeza->dato >= valor) {
            nuevoNodo->siguiente = cabeza;
            cabeza = nuevoNodo;
        } else {
            Nodo* actual = cabeza;
            while (actual->siguiente != nullptr && actual->siguiente->dato < valor) {
                actual = actual->siguiente;
            }
            nuevoNodo->siguiente = actual->siguiente;
            actual->siguiente = nuevoNodo;
        }
    }

    void mostrarLista() {
        Nodo* actual = cabeza;
        std::cout << "Lista ordenada: ";
        while (actual != nullptr) {
            std::cout << actual->dato << " ";
            actual = actual->siguiente;
        }
        std::cout << std::endl;
    }

    ~ListaEnlazada() {
        Nodo* actual = cabeza;
        while (actual != nullptr) {
            Nodo* siguiente = actual->siguiente;
            delete actual;
            actual = siguiente;
        }
    }
};

int main() {
    ListaEnlazada lista;
    int numero;

    std::cout << "Ingrese números enteros (ingrese 0 para terminar):" << std::endl;
    while (true) {
        std::cout << "Número: ";
        std::cin >> numero;

        if (numero == 0) {
            break;
        }

        lista.insertarOrdenado(numero);
    }

    lista.mostrarLista();

    return 0;
}
```

## Explicación.

El programa define una clase `Nodo` para representar cada elemento de la lista enlazada y una clase `ListaEnlazada` para manejar la lista en sí. Cuando el usuario ingresa un número, se crea un nodo nuevo y se inserta en la posición correcta dentro de la lista para mantener el orden ascendente. Luego el programa solicira al usuario que ingrese números enteros desde la consola hasta que ingrese `0`. Después de la inserción, el programa muestra todos los números en la lista ordenada. 


# Desafío N2 (otro código)

```cpp
#include <iostream>

class Nodo {
public:
    int dato;
    Nodo* siguiente;

    Nodo(int valor) {
        dato = valor;
        siguiente = nullptr;
    }
};

class ListaEnlazada {
private:
    Nodo* cabeza;

public:
    ListaEnlazada() {
        cabeza = nullptr;
    }

    void insertarAlFinal(int valor) {
        Nodo* nuevoNodo = new Nodo(valor);
        if (cabeza == nullptr) {
            cabeza = nuevoNodo;
        } else {
            Nodo* actual = cabeza;
            while (actual->siguiente != nullptr) {
                actual = actual->siguiente;
            }
            actual->siguiente = nuevoNodo;
        }
    }

    void insertarOrdenado(int valor) {
        Nodo* nuevoNodo = new Nodo(valor);
        if (cabeza == nullptr || cabeza->dato >= valor) {
            nuevoNodo->siguiente = cabeza;
            cabeza = nuevoNodo;
        } else {
            Nodo* actual = cabeza;
            while (actual->siguiente != nullptr && actual->siguiente->dato < valor) {
                actual = actual->siguiente;
            }
            nuevoNodo->siguiente = actual->siguiente;
            actual->siguiente = nuevoNodo;
        }
    }

    void mostrarLista() {
        Nodo* actual = cabeza;
        while (actual != nullptr) {
            std::cout << actual->dato << " ";
            actual = actual->siguiente;
        }
    }

    ~ListaEnlazada() {
        Nodo* actual = cabeza;
        while (actual != nullptr) {
            Nodo* siguiente = actual->siguiente;
            delete actual;
            actual = siguiente;
        }
    }
};

int main() {
    ListaEnlazada listaSinOrdenar;
    ListaEnlazada listaOrdenada;
    int numero;

    std::cout << "Ingrese números enteros (ingrese 0 para terminar):" << std::endl;
    while (true) {
        std::cout << "Número: ";
        std::cin >> numero;

        if (numero == 0) {
            break;
        }

        listaSinOrdenar.insertarAlFinal(numero);
        listaOrdenada.insertarOrdenado(numero);
    }

    std::cout << "Lista sin ordenar: ";
    listaSinOrdenar.mostrarLista();
    std::cout << std::endl;

    std::cout << "Lista ordenada: ";
    listaOrdenada.mostrarLista();
    std::cout << std::endl;

    return 0;
}
```
