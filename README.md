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
        [main 3bbbef2] Subimos cambios tras la mezcla en el repositorio principal
        2 files changed, 48 insertions(+), 1 deletion(-)
        -salida

    - git push
        - salida
        Enumerando objetos: 15, listo.
        Contando objetos: 100% (15/15), listo.
        Compresión delta usando hasta 4 hilos
        Comprimiendo objetos: 100% (13/13), listo.
        Escribiendo objetos: 100% (15/15), 2.63 KiB | 2.63 MiB/s, listo.
        Total 15 (delta 4), reusados 0 (delta 0), pack-reusados 0
        remote: Resolving deltas: 100% (4/4), done.
        To https://github.com/rhcarballo/ejercicio_git_roberto_hernandez_carballo
        * [new branch]      main -> main
        - salida
    
13. Muestra todos los cambios realizados.

    ```code
   - git status
        - salida
        En la rama main
        Tu rama está actualizada con 'origin/main'.

        Cambios no rastreados para el commit:
        (usa "git add <archivo>..." para actualizar lo que será confirmado)
        (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
                modificados:     README.md

        sin cambios agregados al commit (usa "git add" y/o "git commit -a")
        -salida
    ```

14. Lista ahora los últimos cambios que se han producido en el repositorio, es decir, los últimos commits que han realizado en el repositorio.

     ```code
    - git log
        - salida
        commit 3bbbef2ad6d4106400aa5eebb964463b838bc4ac (HEAD -> main, origin/main)
        Author: rhcarballo <robertohernandezcarballo@gmail.com>
        Date:   Wed Oct 18 15:43:57 2023 +0100

            Subimos cambios tras la mezcla en el repositorio principal

        commit 353923b2233d4dfe08ab9fadd9becb12027e5d48
        Author: rhcarballo <robertohernandezcarballo@gmail.com>
        Date:   Wed Oct 18 15:30:55 2023 +0100

            Creado adios.html en la rama main

        commit e97263430edad17266c5c005c5ff15dbe4ce60f0
        Author: rhcarballo <robertohernandezcarballo@gmail.com>
        Date:   Wed Oct 18 15:18:31 2023 +0100

            Creado hola.html en rama develop

        commit 226babcf716a5d32bbb388d330fe95eb9f953b27
        Author: rhcarballo <robertohernandezcarballo@gmail.com>
        Date:   Wed Oct 18 14:56:26 2023 +0100

            Creado el README.md, primer commit
        - salida
    ```

15. Lista todos los tags(etiquetas que existan).

    ```code
    - git show
        - salida
        commit 3bbbef2ad6d4106400aa5eebb964463b838bc4ac (HEAD -> main, origin/main)
        Author: rhcarballo <robertohernandezcarballo@gmail.com>
        Date:   Wed Oct 18 15:43:57 2023 +0100

            Subimos cambios tras la mezcla en el repositorio principal

        diff --git a/README.md b/README.md
        index 1f6db3c..19a6684 100644
        --- a/README.md
        +++ b/README.md
        @@ -110,4 +110,51 @@ nombre_alumno cambiado directamente en "hola.html".
                </html>
                ```
            ```
        +nombre_alumno cambiado directamente en el documento
        
        +8. Crea el commit con un mensaje descriptivo.
        +
        +    ```code
        +    - git add .
        +    - git commit -m "Creado adios.html en la rama main"
        +        - salida
        +         [main 353923b] Creado adios.html en la rama main
        +        2 files changed, 37 insertions(+), 5 deletions(-)
            ```
    ```

16. Crea una nueva etiqueta (tag) de nombre v.1 y sube los cambios.

    ```code
    - git tag v.1
    - git add .
    - git commit -m "Creada etiqueta v.1"
        - salida
        reada etiqueta v.1"
        [main ccaccac] Creada etiqueta v.1
        1 file changed, 101 insertions(+), 1 deletion(-)
        - salida
    ```

17.     Crea la feature-2 y muevete a esta.

    ```code
    - git branch feature-2
    - git checkout feature-2
    - git branch
        - salida
          develop
        * feature-2
          main
        - salida
    ```
- Crea el archivo Estamos_a_punto_de_terminar.html, con el siguiente contenido:

    ```code
    - touch Estamos_a_punto_de_terminar.html
    - cat >> Estamos_a_punto_de_terminar.html
        <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
        <html>
        <head>
        <title>Terminando </title>
        </head>
        <body>
        <h1 align="center" >Apunto de terminar </h1>
        <hr>
        <p> Esto se esta acabando nombre_alumno </p>
        </body>
        </html>
    ```

    
18. Realiza el commit y sube los cambios.

    ```code 
    - git add .
    - git commit -m "creada rama feature-2 con  Estamos_a_punto_de_terminar.html"
        - salida
        [feature-2 d86d743] creada rama feature-2 con  Estamos_a_punto_de_terminar.html
        2 files changed, 53 insertions(+)
        create mode 100644 Estamos_a_punto_de_terminar.htmlç
        - salida
    ```

19. Muevete a la rama develop, y realiza la mezcla con la rama feature-2.

    ```code
    - git checkout develop
    - git branch
    - git merge failure-2
    ```