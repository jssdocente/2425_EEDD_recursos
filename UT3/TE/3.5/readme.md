# Ejercicio 3.5 - Usar librería Maven desplegada en repositorio hosted

El objetivo de este ejercicio es usar la librería Maven desplegada en el servidor Maven hosted, creada por un compañero.



## Entrega

Guarda este proyecto en tu repositorio de Github, dentro de la carpeta `TE\3.5`, con el nombre `Uso-UtilidadesMaven`. Será un proyecto basado en Maven.

Copia este documento en el `README.md` del proyecto. Crea también uan carpeta llamada `_res/img` y guarda las capturas de pantalla que se solicitan en este documento. 

## Enunciado


### 1. Crear un proyecto Maven y añadir dependencia "UtilidadesMaven"

Crea un proyecto Maven con las siguientes características:

1. **`groupId`**: `com.{apellido1}.{nombre}`.
2. **`artifactId`**: `AnalizadorDatos`.
3. **`version`**: `1.0-SNAPSHOT`.
  

Para este ejercicio, necesitas vincular la librería creada por el compañero en tu proyecto. 

-  Agrega la dependencia de la librería en el archivo `pom.xml` de tu proyecto.


Ahora intenta compilar el proyecto, utilizando el comando `mvn compile`.

- Como la librería no está disponible en el repositorio local, Maven no puede descargarla y se produce un error.<br>

**¿Por qué no puede descargarla?**
Porque la librería no está en el repositorio local, y Maven no conoce la dirección del repositorio hosted.

**¿Qué debes hacer para solucionar este problema?**
Debes indicar a Maven la dirección del repositorio hosted, dentro del fichero `pom.xml` para que pueda descargar la librería.

**¿Dónde se indica la dirección del repositorio hosted?**
En el archivo `pom.xml` y en el archivo `settings.xml` de Maven.

```xml
   <repositories>
        <repository>
            <id>demo-repo</id>
            <url>http://10.0.10.253:8081/repository/demo-repo/</url>
        </repository>
    </repositories>
```

**¿Por qué sigue sin funcionar, y no puede descargarse la dependencia?**

Porque no hemos indicado este repositorio en la configuración local de nuestro Maven, en `.m2\settings.xml`.

```xml
<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 https://maven.apache.org/xsd/settings-1.0.0.xsd">
  <localRepository/>
  <interactiveMode/>
  <offline/>
  <pluginGroups/>
  <servers>
   <server>
        <id>demo-repo</id>
        <username>alumnouser</username>
        <password>alumnouser</password>
    </server>
  </servers>	
  <mirrors/>
  <proxies/>
  <-- agregar esto -->
  <profiles>
   <profile>
     <id>myprofile</id>
     <repositories>
       <repository>
        <id>demo-repo</id>
	<url>http://192.168.65.102:8081/repository/demo-repo</url>
       </repository>
     </repositories>
   </profile>
  </profiles>
  <-- hasta aquí -->
  <activeProfiles/>
</settings>
```

**Sigue sin funcionar, ahora otro error**

Ahora el problema está relacionado con que desde la versión 3.8.1 de Maven, no permite acceder a través del protocolo HTTP, es necesario hacerlo a través del HTTPS.
El problema es que nuestro servidor creado no tiene un certificado, y por tanto no podemos acceder a través de HTTPS.

*Solución*
Desactivar esta comprobación, haciendo el sistema más inseguro.

Agregar una nueva configuración al fichero `.m2\settings.xml`.

```xml
<mirrors>
 <mirror>
    <id>maven-default-http-blocker</id>
    <mirrorOf>external:dummy:*</mirrorOf>
    <name>Pseudo repository to mirror external repositories initially using HTTP.</name>
    <url>http://0.0.0.0/</url>
    <blocked>true</blocked>
 </mirror>
</mirrors>
```

**Volver a probar a compilar**

Ahora sí, nos debería haber compilado el proyecto, y por tanto haber descargado la dependencia.


### 2. Crear funcionalidad utilizando funciones de la librería "UtilidadesMaven"

1. Estructura del Proyecto
   
  El proyecto deberá seguir la estructura de un proyecto Maven con el siguiente esquema:

  AnalizadorDatos/

    │── src/
    │   ├── main/
    │   │   ├── java/
    │   │   │   ├── com.miempresa.analizadordatos/
    │   │   │   │   ├── Main.java
    │   │   │   │   ├── AnalizadorNumerico.java
    │   │   │   │   ├── AnalizadorTexto.java
    │   ├── test/
    │   │   ├── java/
    │   │   │   ├── com.miempresa.analizadordatos/
    │   │   │   │   ├── AnalizadorNumericoTest.java
    │   │   │   │   ├── AnalizadorTextoTest.java
    │── pom.xml

2. Funcionalidades del Programa
   
  El programa debe permitir al usuario interactuar mediante un menú de opciones en la consola, donde podrá analizar números y textos ingresados.

  Opción 1: Análisis Numérico

     - El usuario ingresará un número entero y el programa deberá mostrar:

     - Si el número es par o impar (esPar, esImpar).

     - Si el número es primo (esPrimo).

     - Su factorial (factorial).

     - Sus divisores (devolverDivisores).

     - Si es perfecto (esPerfecto).

  Opción 2: Análisis de Texto
  
  El usuario ingresará una cadena de texto y el programa deberá mostrar:

  Si la cadena es un palíndromo (esPalindromo).

  El número de vocales (contarVocales).

  El número de consonantes (contarConsonantes).

  El número de palabras (contarPalabras).

  El número de caracteres (contarCaracteres).


  Opción 3: Salir
El programa se cerrará cuando el usuario lo indique.

3. Requisitos Técnicos
Uso de Maven:

El proyecto debe configurarse con Maven e incluir la librería UtilidadesMaven en el pom.xml.

Buena Práctica de Código:

Se deben utilizar clases separadas (AnalizadorNumerico.java y AnalizadorTexto.java) para manejar la lógica de análisis de números y textos.

La clase Main.java solo debe encargarse de la interacción con el usuario y la ejecución del programa.

Pruebas Unitarias:

Implementar pruebas unitarias en la carpeta test/ para verificar el correcto funcionamiento de los métodos.

Entrega y Evaluación
Fecha de entrega: (indicar fecha según calendario de clases)

Criterios de evaluación:

✔ Correcta implementación de la lógica del programa.

✔ Uso correcto de la librería UtilidadesMaven.

✔ Estructura del código siguiendo el paradigma POO.

✔ Uso adecuado de Maven y la estructura del proyecto.

✔ Implementación de pruebas unitarias con JUnit.

Notas Adicionales
Se recomienda utilizar Scanner para la entrada de datos del usuario.

Opcionalmente, los alumnos pueden agregar más funcionalidades o una interfaz gráfica con Swing o JavaFX.

🔹 ¡Buena suerte y a programar! 🚀





You said:
Muy bien, pero además quiero que indiques cual debería ser la salida que debería mostrar el programa para que los alumnos tengan esa referencia.


ChatGPT said:
Ejemplo de Salida Esperada
A continuación, se muestra un ejemplo de la ejecución del programa con diferentes entradas para que los alumnos tengan una referencia clara del comportamiento esperado.

Ejemplo 1: Análisis Numérico
📌 Entrada del usuario:

makefile
Copy
Edit
Seleccione una opción:  
1 - Análisis Numérico  
2 - Análisis de Texto  
3 - Salir  
Opción: 1  
Ingrese un número: 28
📌 Salida esperada:

diff
Copy
Edit
🔢 Análisis del número: 28  
- ¿Es par? ✅ Sí  
- ¿Es impar? ❌ No  
- ¿Es primo? ❌ No  
- Factorial: 3,048,883,200  
- Divisores: [1, 2, 4, 7, 14, 28]  
- ¿Es perfecto? ✅ Sí (La suma de sus divisores propios es 28)  
Ejemplo 2: Análisis de Texto
📌 Entrada del usuario:

makefile
Copy
Edit
Seleccione una opción:  
1 - Análisis Numérico  
2 - Análisis de Texto  
3 - Salir  
Opción: 2  
Ingrese una cadena de texto: "Anita lava la tina"
📌 Salida esperada:

diff
Copy
Edit
📝 Análisis del texto: "Anita lava la tina"  
- ¿Es palíndromo? ✅ Sí  
- Número de vocales: 8  
- Número de consonantes: 8  
- Número de palabras: 4  
- Número de caracteres (sin espacios): 16  
Ejemplo 3: Salida del Programa
📌 Entrada del usuario:

makefile
Copy
Edit
Seleccione una opción:  
1 - Análisis Numérico  
2 - Análisis de Texto  
3 - Salir  
Opción: 3
📌 Salida esperada:

Copy
Edit
👋 ¡Gracias por usar el Analizador de Datos! Hasta pronto.