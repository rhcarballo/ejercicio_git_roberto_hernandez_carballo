# ejercicio_git_roberto_hernandez_carballo

1. Crea un repositorio en tu cuenta de Github con el siguiente nombre: ejercicio_git_nombre_alumno, donde nombre_alumno debe de ser tu nombre siguiendo el patrón nombre_apellido1_apellido2. No incluyas el fichero README.md.

Repositorio creado.

2. Realiza la clonación del frepositorio creado.

    ```code
    - git clone https://github.com/rhcarballo/ejercicio_git_roberto_hernandez_carballo
    ```

3. Añadir el archivo README al repositorio y realizar el primer commit.

    ```code
    - git add .
    - git commit -m "Creado el README.md, primer commit"
        - salida
        [main (commit-raíz) 226babc] Creado el README.md, primer commit
        1 file changed, 0 insertions(+), 0 deletions(-)
        create mode 100644 README.md
        - salida
    ```

4. Crear una rama con nombre develop.

    ```code
    - git branch develop
    ```
5. Lista las ramas actuales.

    ```code
    - git status
        - salida
        En la rama main
        Tu rama está basada en 'origin/main', pero upstream ha desaparecido.
        (usa "git branch --unset-upstream" para arreglar)

        Cambios no rastreados para el commit:
        (usa "git add <archivo>..." para actualizar lo que será confirmado)
        (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
                modificados:     README.md

        sin cambios agregados al commit (usa "git add" y/o "git commit -a")
        - salida

    - git branch
        - salida
          develop
        * main
        - salida
    ```

6. Moverse a la rama y crear el fichero: hola.html. - Añadir el siguiente contenido: 

    ```code
    - git checkout develop
        - salida
        M       README.md
        Cambiado a rama 'develop'
        - salida
    
    - touch hola.html
    - cat >> hola.html
    ```html
    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
    <html>
    <head>
    <title>Hola </title>
    </head>
    <body>
    <h1 align="center" >Hola soy un título </h1>
    <hr>
    <p> Hola soy el alumno nombre_alumno </p>
    </body>
    </html>
    ```

nombre_alumno cambiado directamente en "hola.html".

7. Moverse a la rama principal y crear el fichero adios.html > Sustituye nombre_alumno por tu nombre.

    ```code
    - git checkout main
        - salida
        Cambiado a rama 'main'
        Tu rama está basada en 'origin/main', pero upstream ha desaparecido.
        (usa "git branch --unset-upstream" para arreglar)
        - salida
    
    - git branch
        - salida
          develop
        * main
        - salida
    
    - touch adios.html
    - cat >> adios.html
    ```html
        <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
        <html>
        <head>
        <title>Adios </title>
        </head>
        <body>
        <h1 align="center" >Adios soy un título </h1>
        <hr>
        <p> Adios soy el alumno nombre_alumno </p>
        </body>
        </html>
        ```
    ```
nombre_alumno cambiado directamente en el documento

8. Crea el commit con un mensaje descriptivo.

    ```code
    - git add .
    - git commit -m "Creado adios.html en la rama main"
        - salida
         [main 353923b] Creado adios.html en la rama main
        2 files changed, 37 insertions(+), 5 deletions(-)
        rename hola.html => adios.html (56%)
        - salida
    ```

9. Sube los cambios a la rama actual.

    ```code
    - git add .
    ```
10. Lista las ramas actuales.

    ```code
    - git branch
        - salida
          develop
        * main
        - salida
    ```

11. Realizar la mezcla en el repositorio principal.

    ```code
    - git merge develop
        - salida
        Los cambios locales de los siguientes archivos serán sobreescritos por merge:
        - salida
    ```

12. Sube los cambios al repositorio a tu cuenta de Github.

    ```code
    - git add .
    - git commit -m "Subimos cambios tras la mezcla en el repositorio principal"
        - salida

        -salida
        
    - git push