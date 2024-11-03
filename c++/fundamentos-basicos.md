# Fundamentos básicos de programación en C++

En esta sección es conocer la sintaxis y fundamentos básicos en C++.

## Declaración de variables.

Para declarar **variables**, primero se declara el tipo de variable, pueden ser `int` (*entero*), `double` (*décimal*), `float` (*décimal*), `char` (*un solo cáracter*) , `string` (*texto*).


| Tipo de variable | Descripción | Ejemplo de valor |
|------------------|-------------|------------------|
| `int`           | Almacena números enteros (sin decimales). | `23`, `-5`, `100` |
| `double`        | Almacena números decimales con mayor precisión (64 bits). | `0.31`, `3.1415` |
| `float`         | Almacena números decimales con menor precisión que `double` (32 bits). | `0.43`, `1.5` |
| `char`          | Almacena un solo carácter. | `'A'`, `'7'`, `'#'` |
| `string`        | Almacena cadenas de texto (requiere la biblioteca `<string>`). | `"Hola, mundo"`, `"Texto de ejemplo"` |



```cpp
// declaracion_variable  nombre_variable = dato

int numero = 23;
double decimal = 0.31;
float decimal = 0.43;
char = 'A';
string = " Esto es texto "; // es necesario llamar a la biblioteca <string>
```

Para declarar datos y hacer un programa ejecutable básico en C++, es necesario incluir el bloque de la **función principal** que tenga inicio `int main ()` y fin `return 0;`. 

```cpp
// el punto de entrada para cualquier programa es la función main(). Esta función es el primer bloque que se ejecuta al iniciar el programa.
int main () {
  int edad = 23;
  double altura = 1.73;
  float peso = 74.4;
// el código dentro de la función principal main() debe devolver un valor entero (int), usualmente 0, que indica que el programa terminó correctamente.
  return 0;
}
```

Para mostrar y manejar la salida y entrada de datos del código que se creo, se utiliza la biblioteca `<iostream>` y la función `std::cout` para mostrar los datos en pantalla. Es necesario incluir la biblioteca al inicio del código con `#include <iostream>`.

```cpp
#include <iostream>  // llamando a la biblioteca para mostras datos en pantalla

int main () {  // función principal
  int edad = 23;
  double altura = 1.73;
  float peso = 74.4;

  std::cout << "tengo" << edad << " años y mido " << altura << " y peso " << peso << " kg"; 
  return 0; // fin del bloque principal 
}
```
