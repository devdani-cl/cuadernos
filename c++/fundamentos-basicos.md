# Fundamentos básicos de programación en C++

En esta sección es conocer la sintaxis y fundamentos básicos en C++.

## Declaración de variables.

Para declarar **variables**, primero se declara el tipo de variable, pueden ser `int` (*entero*), `double` (*décimal*), `float` (*décimal*), `char` (*un solo cáracter*) , `string` (*texto*).

```cpp
// declaracion_variable  nombre_variable = dato

int numero = 23;
double decimal = 0.31;
float decimal = 0.43;
char = 'A';
string = " Esto es texto ";
```

Para declarar datos y hacer un programa ejecutable básico en C++, es necesario incluir el bloque de la función principal que tenga inicio `int main ()` y fin `return 0;`. 

```cpp
int main () {
  int edad = 23;
  double altura = 1.73;
  float peso = 74.4;
  return 0;
}
```

¿cómo se dice cuando el programa se ejecuta? ej: "para manejar y mostrar el código que se creo, antes es necesario llamar la biblioteca `#include <iostream>` para 
mostrar los datos en pantalla". 
