**Certamen de Nivel Universitario: Punteros en C++**

**Instrucciones**: Este certamen consta de tres secciones. Responda las preguntas seleccionando la alternativa correcta o indicando si son verdaderas o falsas, justificando sus respuestas. Finalmente, analice el código proporcionado y realice el ruteo correspondiente.

---

### **Sección A: Preguntas de Selección Múltiple**

**1.** ¿Cuál es la diferencia entre un puntero y una referencia en C++?

a) Un puntero es una variable que almacena la dirección de memoria de otra variable, mientras que una referencia es un alias para una variable existente.

b) No hay diferencia; punteros y referencias son lo mismo en C++.

c) Una referencia puede ser reasignada a otro objeto después de su inicialización, mientras que un puntero no.

d) Un puntero debe ser inicializado al declararse, mientras que una referencia no.

---

**2.** Dada la declaración `int *ptr = nullptr;`, ¿qué significa `nullptr` en este contexto?

a) `nullptr` es una dirección de memoria inválida.

b) `nullptr` es un puntero que apunta a la dirección de memoria cero.

c) `nullptr` es una constante entera con valor cero.

d) `nullptr` es un tipo de dato que no puede ser asignado a punteros.

---

**3.** ¿Qué operador se utiliza para obtener la dirección de una variable en C++?

a) `*` (asterisco)

b) `&` (ampersand)

c) `->` (flecha)

d) `.` (punto)

---

**4.** ¿Cuál es el resultado de la siguiente expresión?

```cpp
int x = 10;
int *ptr = &x;
int **pptr = &ptr;
std::cout << **pptr;
```

a) 10

b) La dirección de memoria de `x`

c) La dirección de memoria de `ptr`

d) Error de compilación

---

**5.** ¿Qué sucede si intentamos desreferenciar un puntero nulo en C++?

a) Se produce un error de compilación.

b) Se desreferencia correctamente y se obtiene un valor predeterminado.

c) Se produce un comportamiento indefinido y posiblemente una excepción en tiempo de ejecución.

d) El puntero se inicializa automáticamente a una dirección válida.

---

**6.** ¿Cuál de las siguientes opciones es correcta para asignar memoria dinámica para un arreglo de 10 enteros?

a) `int *arr = new int;`

b) `int arr = new int[10];`

c) `int *arr = new int[10];`

d) `int arr[10];`

---

**7.** Si tenemos `int *ptr;`, ¿qué significa `*ptr` en C++?

a) La dirección de memoria a la que apunta `ptr`.

b) El valor almacenado en la dirección a la que apunta `ptr`.

c) La declaración de un puntero nulo.

d) La multiplicación del puntero por un entero.

---

**8.** ¿Qué es un puntero doble en C++?

a) Un puntero que almacena un valor de tipo `double`.

b) Un puntero que apunta a otro puntero.

c) Un puntero que almacena el doble de la dirección original.

d) Un puntero que puede apuntar a dos variables al mismo tiempo.

---

**9.** Dado el siguiente código, ¿qué salida produce?

```cpp
int arr[5] = {1, 2, 3, 4, 5};
int *ptr = arr;
std::cout << *(ptr + 3);
```

a) 1

b) 2

c) 4

d) 5

---

**10.** ¿Cuál es la forma correcta de liberar memoria asignada dinámicamente para un arreglo de enteros en C++?

a) `delete ptr;`

b) `delete [] ptr;`

c) `free(ptr);`

d) `delete arr;`

---

**11.** ¿Qué sucede si olvidamos liberar memoria asignada dinámicamente con `new`?

a) El programa liberará automáticamente la memoria al finalizar.

b) Se produce un error de compilación.

c) Puede causar una fuga de memoria (memory leak).

d) La memoria se libera cuando el puntero sale del alcance (scope).

---

**12.** ¿Qué es aritmética de punteros en C++?

a) Operaciones matemáticas realizadas con variables enteras.

b) Operaciones realizadas sobre direcciones de memoria usando punteros.

c) La capacidad de sumar y restar punteros directamente.

d) La multiplicación y división de valores apuntados por punteros.

---

**13.** ¿Cuál es el resultado de la siguiente expresión si `ptr` es un puntero a `int`?

```cpp
ptr += 2;
```

a) El puntero apunta al siguiente entero en memoria.

b) El puntero avanza dos posiciones de bytes en memoria.

c) El puntero avanza dos posiciones de enteros en memoria.

d) Error de compilación.

---

**14.** ¿Qué operador se utiliza para acceder a un miembro de una estructura a través de un puntero?

a) `.` (punto)

b) `->` (flecha)

c) `*` (asterisco)

d) `&` (ampersand)

---

**15.** En C++, ¿es posible tener un puntero a una función?

a) No, C++ no admite punteros a funciones.

b) Sí, pero solo para funciones miembro de clases.

c) Sí, podemos tener punteros que apuntan a funciones.

d) Sí, pero solo para funciones estáticas.

---

**16.** ¿Cuál es la sintaxis correcta para declarar un puntero constante a un entero en C++?

a) `int const *ptr;`

b) `int *const ptr;`

c) `const int *ptr;`

d) Tanto b) como c) son correctas.

---

**17.** Si queremos que un puntero no pueda cambiar la dirección a la que apunta después de ser inicializado, ¿cómo lo declaramos?

a) `int *ptr;`

b) `int const *ptr;`

c) `int *const ptr;`

d) `const int *ptr;`

---

**18.** ¿Qué es el operador `sizeof` cuando se aplica a un puntero en C++?

a) Devuelve el tamaño del tipo al que apunta el puntero.

b) Devuelve el tamaño del puntero en bytes.

c) Devuelve el tamaño del contenido al que apunta el puntero.

d) Devuelve el número de elementos a los que apunta el puntero.

---

**19.** Dado `char str[] = "Hola";`, ¿cuál es la diferencia entre `str` y `&str`?

a) `str` es un puntero, `&str` es una referencia.

b) No hay diferencia entre `str` y `&str`.

c) `str` es la dirección del primer carácter, `&str` es la dirección del arreglo completo.

d) `str` es el contenido del arreglo, `&str` es el primer carácter.

---

**20.** ¿Qué sucede al utilizar `delete` en un puntero que no fue inicializado con `new`?

a) Se libera correctamente la memoria.

b) Se produce un error de compilación.

c) Comportamiento indefinido y posible fallo en tiempo de ejecución.

d) La memoria se libera cuando el puntero sale del alcance.

---

### **Sección B: Verdadero o Falso (Justifique su respuesta)**

**1.** Es posible tener punteros a referencias en C++.

**2.** Un puntero puede apuntar a una función en C++.

**3.** Los punteros y los arreglos son equivalentes en todas las situaciones en C++.

**4.** Un puntero `void*` puede ser desreferenciado sin casting en C++.

**5.** Los punteros pueden ser asignados a variables de tipo entero sin casting en C++.

**6.** La aritmética de punteros considera el tamaño del tipo al que apunta el puntero.

**7.** El operador `new` en C++ siempre inicializa la memoria asignada a cero.

**8.** Es seguro desreferenciar cualquier puntero que no sea `nullptr`.

**9.** En C++, los punteros pueden ser comparados usando los operadores relacionales.

**10.** Los punteros constantes no pueden cambiar el valor al que apuntan.

**11.** Un puntero a una clase base puede apuntar a un objeto de una clase derivada.

**12.** Un puntero `const int*` permite modificar el valor apuntado.

**13.** Es posible crear un arreglo de punteros en C++.

**14.** El operador `&` se utiliza para desreferenciar un puntero.

**15.** La expresión `*(ptr + i)` es equivalente a `ptr[i]`.

**16.** Un puntero puede tener el valor `nullptr`.

**17.** Un puntero a un puntero se declara con la sintaxis `int *ptr*;`.

**18.** Los punteros pueden ser pasados a funciones como argumentos.

**19.** Al copiar un puntero, se copia el contenido al que apunta.

**20.** Los punteros pueden ser inicializados con la dirección de una variable estática.

---

### **Sección C: Análisis de Código y Ruteo**

Analice el siguiente código y realice el ruteo correspondiente, mostrando el estado de las variables en cada paso importante del programa.

```cpp
#include <iostream>

void swap(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    int x = 5, y = 10;
    int *p = &x;
    int *q = &y;

    std::cout << "Antes del swap:\n";
    std::cout << "x = " << x << ", y = " << y << "\n";

    swap(p, q);

    std::cout << "Después del swap:\n";
    std::cout << "x = " << x << ", y = " << y << "\n";

    return 0;
}
```

**Preguntas:**

1. **¿Cuál es la salida del programa y por qué?**

2. **Explique paso a paso cómo funciona la función `swap` utilizando punteros.**

3. **Si en lugar de pasar `p` y `q` a la función `swap`, hubiéramos pasado `&p` y `&q`, ¿cuál sería el efecto y por qué?**

---

**Fin del Certamen**
