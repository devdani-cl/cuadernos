Código 1: Hola mundo
```go
package main

import "fmt"

func main () {
  fmt.Println("Hello, world")
}
```

Código 2: Declaración de variables

```go
package main

import "fmt"

func main() {
	fmt.Println("hola mundo")

	// declaración de variables

	var adios string
	var num int

	adios = "adios ctm"
	num = 19
	fmt.Println(adios)
	fmt.Println("num es una variable de tipo entero igual a ", num)

	// la función decirAlgo retorna en un string y la guardamos en una variable ":=" para usarla en la función principal 
	deciralgo, gorditarica:= decirAlgo()
	fmt.Println(deciralgo, gorditarica)
}

//funciones
func decirAlgo() (string, string) { // una función que retorna en una cadena string
	return "decir algo como", "gordita rica"
}
```
