## Clase 2.

Objetivos: Entender la lógica del flujo de trabajo con Docker y Python. 

**Lógica de trabajo**

1. Crear una carpeta vacía desde powershell con el comando mkdir <nombre_carpeta>


2. Crear un archivo Dockerfile dentro de nuestra carpeta de trabajo
3. Crear una imagen `docker build -t <nombre_imagen>`
4. Crear y arrancar un contenedor a partir de una imagen ya creada `docker run -it -v .:/app <nombre_imagen>`

   



Glosario y dudas: 
- ¿en qué momento hay que definir un ENTRYPOINT o CMD en el Dockerfile?

