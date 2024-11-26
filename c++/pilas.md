# pilas
Una pila es una estructura de datos que opera bajo el principio LIFO.

# implementación de pilas c++
C++ proporciona la clase "stack" de la biblioteca "estandar":

Funciones para trabajar con pilas.
- push(): añade un elemento de la pila.
- pop(): quita un elemento de la pila (LIFO).
- empty(): comprueba si la pila está vacía.
- size(): permite ver el tamaño de la pila.

```cpp
#include <iostream>
#include <stack>

void imprimirPila(stack<int> copiaPila) {
  while (!copiaPila.empty()) {
    std::cout << copiaPila.top() << std::endl;
    copiaPila.pop();
  }
}

int main() {
  // guardar numeros dentro de la pila
  stack<int> numerosPila;

  // agregar elementos a la pila
  numerosPila.push(1);
  numerosPila.push(2);
  numerosPila.push(3);

  // llamamos a la funcion pop
  numerosPila.pop();

  // llamando a función empty
  if (numeroPila.empty()) {
    std::cout << "pila vacia" << std::endl;
  } else {
    std::cout << "pila no está vacía" << std::endl;
}
  // llamando a función size
  std::cout << "el tamaño de la pila es: " << numerosPila.size() << std::endl;
  imprimirPila(numerosPila);
```
