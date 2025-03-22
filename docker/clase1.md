## Clase 1.

La primera clase se va a tratar de explicar para que sirve Docker y algunos comandos 
que hay que saber para iniciar.

**Docker ¿qué es?**

Es una tecnología que permite "contenerizar", es decir, hacer todo el proceso de empacar una
aplicación y todas sus dependencias en contenedores mediante imágenes para que pueda ejecutarse
de forma consistente en cualquier entorno donde exista un runtime de contenedores.


**Comandos básicos**

- `docker pull <imagen>`
    - descarga la imagen de docker hub a mi máquina local (¿cuál sería la máquina local?)
    - ejemplo: `docker pull python:3.10`.

- `docker images`
    - muestra y lista todas las imágenes que tengo descargadas en el pc.

- `docker ps`
    - muestra los contenedores activos (que estan en ejecución).
    - `docker ps -a`, es para ver todos los contenedores, incluyendo los que están detenidos.
      
- `docker create`
    - crea un contenedor a partir de una imagen, pero **NO** lo inicia.
    - ejemplo: `docker create --name <mi_contenedor> python:3.10`, crea un contenedor llamado "mi_contenedor" con la base de Python 3.10, pero no lo arranca.  

- `docker start`
    - arranca un contenedor que ya ha sido creado.
    - `docker start mi_contenedor`.

- `docker run`
    - es un atajo que hace un **pull** (si no existe la imagen), **create** y **start** todo en un solo paso.
    - ejemplo: `docker run --name mi_contenedor -d python:3.10`, este comando significa que crea y arranca el contenedor en segundo plano (`-d`).

- `docker rm <contenedor>`
    - borra (elimina) un contenedor.
    - para borrar contenedor que están corriendo, primero hay que detenerlos `docker stop \<contenedor>` y luego eliminarlo `docker rm <contenedor>`

- `docker rmi <images>`
    - borra (elimina) una imagen.
    - solo se puede eliminar una imagen si no hay contenedores dependientes de ella. (¿a qué se refiere esto?)

- `docker build`
    - construye (crea) una nueva imagen usando Dockerfile.
    - ejemplo: si tengo un Dockerfile en la carpeta actual, se puede crear una imagen con `docker build -t <nombre_imagen>`.

(¿cómo se llaman los parámetros de este tipo `-d`, `-a`, `-t`, `--name`, etc?¿cómo utilizarlos dependiendo de lo que se quiera hacer?)
 
**Forma de trabajo con Docker.**

1. Crear una carpeta para el proyecto. (¿`mkdir <nombre_carpeta>` es una forma de crear una carpeta para el proyecto?¿cómo abrir la carpeta en el vscode de forma directo?)
2. Dentro de la carpeta, crear un archivo **Dockerfile**.
3. Construir la imagen `docker build -t <nombre_imagen .>`, el punto indica que el archivo Dockerfile se está construyendo en la carpeta actual. (¿cómo sería si quiero construir la imagen en otra carpeta?)
4. Cada vez que se modifica el Dockerfile, se "buildea" `docker build -t <nombre_imagen> .`, es decir volver a construir la imagen para aplicar los cambios.
5. Crear  y/o correr el **contenedor** a partir de la imagen.

    a. opción uno: usando `docker create` y luego `docker start` de la siguiente forma.
        - crear el contenedor`docker create --name contenedor_python nombre_imagen`
        - correr el contenedor`docker start contenedor_python`
   
    b. opción dos: crear y correr con el comando `docker run`.
        - `docker run -d --name contenedor_python nombre_imagen`
7. Usar `docker ps` para ver los contenedores **activos**



**Glosario y tecnisismo:**

- **Contenerizar:** Proceso de empacar una aplicación y sus dependencias en contenedores a través de imágenes para que puede ejecutarse en cualquier entorno.
  
- **Contenedores:** Es una _instancia en ejecución_ de una imagen. Cada contenedor tiene su propio sistema de archivos aislado, sus variables de entorno y sus propios procesos corriendo en él.
  
- **Imágenes:** Es una plantilla/fotografía de un sistema con todas las dependencias, configuraciones y el código necesario para que una app funcione, es inmutable, es decir, no cambia. Ej: `python:3.10` es una imagen que contiene todo lo necesario para tener Python en la versión 3.10.
  
- **Empacar:**
- **Dependencias:** Son las archivos y ejecutables de la aplicación.  
- **Entorno:** Es donde se trabaja o desarrolla el software. Un ejemplo sería:
- **Runtime:** 
