## TAREA EVALUABLE 2.1. TRABAJO CON GIT (Visual Studio Code)

### Objetivos

- Conocer cómo trabajar con GIT desde Visual Studio Code.
- Conocer el entorno de VS Code para trabajar con git.
- Conocer el lenguaje de marcado Markdown y su utilización en el desarrollo de documentación.

### Entrega

- El documento justificativo de la realización de la tarea se realizará en formato `Markdown`, el nombre del fichero será `readme.md` y estará dentro de la carpeta `UT2\TE2.1` dentro del repositorio oficial del alumno para la asignatura.

- El fichero `readme.md` debe contener los siguientes apartados:
  - Cada uno de los puntos de la tarea.
  - Explicación de los pasos realizados y una imagen/gif justificativo del paso. (las imagenes se guardarán en la carpeta `UT2\TE2.1\img`).
  - El nombre de la imagen debe ser el número del punto y subpunto seguido de la extensión correspondiente (`.png`, `.jpg`, `.gif`).
    - Ejemplo: `01.1.png`, `02.5.gif`, `03.3.jpg`.
  
- Copia este documento como plantilla para la realización de este ejercicio en tu repositorio.

### 📦 Recursos

- [Visualizar conceptos con D3](https://onlywei.github.io/explain-git-with-d3)
- [Taller de introducción a GIT](https://sharp-voice-0ff.notion.site/Taller-de-introducci-n-a-git-y-GitHub-5c0269251ed9475fab606cd57b9cae34?pvs=4)
- [Guía de supervivencia de GIT](https://sharp-voice-0ff.notion.site/GIT-Gu-a-de-supervivencia-b1ceff4f3b1040bdb27b1e39df9b4cfb?pvs=4)
- [SOS Git]((https://firstaidgit.io/#/))
- [Escrbir en Markdown](https://docs.github.com/es/get-started/writing-on-github)

- [Curso de GIT y GITHUB (youtube)](https://youtu.be/3GymExBkKjE)


    #### ℹ️ Extensiones de VSCode

    - [Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)
    - [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
    - [Markdown Emoji](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-emoji)

### 1. Crear repositorio local y subir a GITHUB

1. Crea una carpeta llamada `UT2.1.a`.
2. Inicializa un repositorio local en la carpeta `UT2.1.a`. `adjunta la imagen`<br>
   ![Inicializar repositorio](img/01.1.png)  --> imagen de ejemplo, sustituye por el nombre de la imagen.

3. Revisa qué rama se ha creado por defecto. ¿Desde dónde los visualizas? `adjunta la imagen`<br>
   ![Rama por defecto](img/01.2.png) 

4. Renombrar la rama por defecto a `main` en caso de que tenga otro nombre. `adjunta un gif`<br>
   ![Renombrar rama](img/01.3.gif)
   
5. Agrega un fichero `README.md`.

   ```markdown
   # UT2.1.a

   Repositorio de prueba para la tarea 2.1.a
   ```

6. Agrega el fichero `README.md` al stage area. `adjunta un gif`<br>
   ![Agregar README](img/01.6.gif)

7. Realiza un commit con el mensaje "Add README". `adjunta un gif`<br>
   ![Commit README](img/01.7.gif)

8. Agrega otro fichero `01.xml` con siguiente texto.

   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   <libreria>
       <libro>
           <titulo>El Quijote</titulo>
           <autor>Miguel de Cervantes</autor>
           <editorial>Editorial Castalia</editorial>
           <fecha>1605</fecha>
           <genero>Novela</genero>
           <precio>20</precio>
       </libro>
   </libreria>
   ```

9.  Agrega el fichero `01.xml` al stage area y realiza el commit "Add file 01.xml" `adjunta un gif`<br>
    ![Agregar 01.xml](img/01.9.gif)

10. Agrega una nueva rama llamada `fea/wac01` con la ayuda git-graph. `adjunta un gif`<br>
    
11. En qué rama estas ahora mismo? ¿Cómo sabes en qué rama estás? `adjunta la imagen` y explica en breves palabras.
    ```text
    // Respuesta
    
    ``` 
    ![Rama actual](img/01.11.png)

12. Estando en la rama `fea/wac01` agrega un fichero `02.xml`, y agrega al área de stage y realiza commit "Add file 02". `adjunta un gif`<br>

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El Hobbit</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1937</fecha>
            <genero>Fantasía</genero>
            <precio>15</precio>
        </libro>
    </libreria>
    ```

13. Muestra el log (pantalla de git-graph donde se visualize el commit). `adjunta la imagen`<br>
    ![Log rama fea/wac01](img/01.13.png)

14. Posicionate de nuevo en la rama `main`, y crea otra rama `fea/wac02`, posicionandote directamente en ella. Agrega un fichero `03.xml`, agrega al área de stage y realiza commit "Add file 03".

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El Señor de los Anillos</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1954</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
    </libreria>
    ```

15. Posicionate en la rama `main` y muestra los ficheros que hay en el directorio. (mostrar el arból de directorios de VS Code). `adjunta la imagen`<br>
    ![Ficheros en main](img/01.15.png)

16. Realizar un merge de la rama `fea/wac01` en la rama `main`. `adjunta un gif`<br>
    ![Merge rama fea/wac01](img/01.16.gif)

17. Muestra el el log, y los ficheros que hay en el directorio. (mostrar el arból de directorios de VS Code) `adjunta la imagen`
    ![Log y ficheros en main](img/01.17.gif)
    
18. Elimina la rama `fea/wac01` sin posibilidad de recuperación. `adjunta un gif`<br>
    ![Eliminar rama fea/wac01](img/01.18.gif)

19. Realiza un merge de la rama `fea/wac02` en la rama `main`. `adjunta un gif`<br>
    ![Merge rama fea/wac02](img/01.19.gif)
    
20. Muestra el log, y los ficheros que hay en el directorio. (Imagen) `adjunta la imagen`
    ![Log y ficheros en main](img/01.20.png)

21. Vuelve a la rama `fea/wac02` y modifica el fichero `03.xml` añadiendo un nuevo libro.
    
    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El Señor de los Anillos</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1954</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
        <libro>
            <titulo>El Silmarillion</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1977</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
    </libreria>
    ```

    Agrega al área de stage y realiza commit "Update 03 file. Add book El Silmarillion".<br>
    `adjunta un gif, donde se visualize el contenido del fichero y el commit`<br>
    ![Modificar 03.xml](img/01.21.gif)

22. Realiza un merge de la rama `fea/wac02` en la rama `main`. `adjunta un gif`<br>
    ![Merge rama fea/wac02](img/01.22.gif)

23. Muestra el log del repositorio, y muestra el contenido del fichero `03.xml`. (Imagen visualizando comandos) `adjunta gif`
    ![Log y ficheros en main](img/01.23.gif)

24. Ahora, en la rama `main` modifica el fichero `03.xml` incluyendo un nuevo libro.

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El Señor de los Anillos</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1954</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
        <libro>
            <titulo>El Silmarillion</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1977</fecha>
            <genero>Fantasía</genero>
            <precio>25</precio>
        </libro>
        <libro>
            <titulo>El Hobbit</titulo>
            <autor>J.R.R. Tolkien</autor>
            <editorial>Minotauro</editorial>
            <fecha>1937</fecha>
            <genero>Fantasía</genero>
            <precio>15</precio>
        </libro>
    </libreria>
    ```

    Agrega al área de stage y realiza commit "Update 03 file. Add book El Hobbit".<br>
    `adjunta un gif, donde se visualize el contenido del fichero y el commit`<br>
    ![Modificar 03.xml](img/01.24.gif)

25. Agrega un nuevo fichero `04.xml` sobre libros ciencia-ficcion, en la rama `main`.

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <libreria>
        <libro>
            <titulo>El fin de la eternidad</titulo>
            <autor>Isaac Asimov</autor>
            <editorial>Edhasa</editorial>
            <fecha>1955</fecha>
            <genero>Ciencia ficción</genero>
            <precio>20</precio>
        </libro>
    </liberia>
    ```

    Agrega al área de stage y realiza commit "Add 04 file. Add cienca-ficcion books".<br>

26. Muestra el registro de commits (log) y los ficheros que hay en el directorio. `adjunta una imagen`<br>
    ![Log y ficheros en main](img/01.26.png)
    
27. Vuelve un commit atrás, y muestra el log y los ficheros que hay en el directorio. `adjunta un gif`<br>
    ![Volver un commit](img/01.27.gif)
    
28. Vuelve al commit anterior, y muestra el log y los ficheros que hay en el directorio. `adjunta un gif`<br>
    ![Volver un commit](img/01.28.gif)

29. Posicionate de nuevo en el último commit, y muestra el log y los ficheros que hay en el directorio. `adjunta un gif`
    ![Volver un commit](img/01.28.gif)

### 2. Crear repositorio remoto y subir a GITHUB

1. Crea un repositorio remoto en GITHUB llamado `EEDD_{NombreApellido}_TE2.1` público, vacio, sin nada.
   
2. Agrega el repositorio remoto a tu repositorio local. Explica cómo lo haces, y `adjunta una imagen donde se visualizen las url's`<br>
    ![Repositorio remoto](img/02.2.png)

   ```text
    // Comentario
    
    ``` 

3. Sube la rama `main` al repositorio remoto. `adjunta un gif`<br>
    ![Subir rama main](img/02.3.gif)
   

4. Posicionate en la rama `fea/wac02` y sube la rama `fea/wac02` al repositorio remoto. `adjunta un gif`<br>
    ![Subir rama fea/wac02](img/02.4.gif)

5. Ahora desde GITHUB (web) en la rama `fea\wac02`, modifica el fichero `03.xml` añadiendo un nuevo libro.

   ```xml
   <?xml version="1.0" encoding="UTF-8"?>
   <libreria>
       <libro>
           <titulo>El Señor de los Anillos</titulo>
           <autor>J.R.R. Tolkien</autor>
           <editorial>Minotauro</editorial>
           <fecha>1954</fecha>
           <genero>Fantasía</genero>
           <precio>25</precio>
       </libro>
       <libro>
           <titulo>El Silmarillion</titulo>
           <autor>J.R.R. Tolkien</autor>
           <editorial>Minotauro</editorial>
           <fecha>1977</fecha>
           <genero>Fantasía</genero>
           <precio>25</precio>
       </libro>
       <libro>
           <titulo>El Hobbit</titulo>
           <autor>J.R.R. Tolkien</autor>
           <editorial>Minotauro</editorial>
           <fecha>1937</fecha>
           <genero>Fantasía</genero>
           <precio>15</precio>
       </libro>
       <libro>
           <titulo>El hombre bicentenario</titulo>
           <autor>Isaac Asimov</autor>
           <editorial>Edhasa</editorial>
           <fecha>1976</fecha>
           <genero>Ciencia ficción</genero>
           <precio>20</precio>
   </libreria>
   ```

   Realiza un commit con el mensaje "Update 03 file. Add book El hombre bicentenario".
   (Muestra pantallazo de GITHUB con el commit realizado) `adjunta la imagen`

6. Ahora obten los cambios sin acualizar el repositorio local (`git fetch origin`).<br>
   Muestra el log del repositorio local `adjunta la imagen`
    
7.  Ahora actualiza el repositorio local con los cambios del repositorio remoto (`git pull`) y muestra el log. `adjunta un gif`<br>
    ![Pull](img/02.7.gif)

8.  Haz un merge de la rama `fea/wac02` en la rama `main`. Muestra estado, log, y el contenido fichero `03.xml` (Incluye imagen) `adjunta un gif`<br>
    ![Merge](img/02.8.gif)

9.  Sube la rama `main` al repositorio remoto. `adjunta una gif`<br>
    ![Subir rama main](img/02.9.gif)

10. Elimina la rama local `fea/wac02` sin posibilidad de recuperación. `adjunta un gif`<br>
    ![Eliminar rama fea/wac02](img/02.10.gif)

11. Elimina la rama remota `fea/wac02` sin posibilidad de recuperación 
    ```text
    // Respuesta
    
    ```
12. Muestra desde GITHUB (navegador web) las ramas que tienes el en repositorio remoto. `adjunta un gif`<br>
    ![Ramas en GITHUB](img/02.12.gif)

13. Para finalizar, muestra el log del repositorio local (Incluye imagen) `adjunta la imagen`<br>
    ![Log](img/02.13.png)

### 3. Enlace repositorio remoto

1. Incluye el enlace al repositorio remoto en este punto para que el profesor pueda acceder a él.
   ```text
    // Enlace al repositorio remoto (en que aparece en la URL del navegador)
    
    ``` 
