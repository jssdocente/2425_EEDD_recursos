# Ejercicio 3.4 - Maven

El objetivo de este ejercicio es crear un proyecto/librería que utilice Maven como sistema de construcción y gestión de dependencias.

### Enunciado

Crea un proyecto Maven con las siguientes características:

1. **`groupId`**: `com.{apellido1}.{nombre}`.
2. **`artifactId`**: `utilidades`.
3. **`version`**: `1.0-SNAPSHOT`.

Crea una clase, dentro del paquete `com.{apellido1}.{nombre}`, con la clase.

- `UtilidadesNumeros`:
  - Método `esPar(int numero)`: devuelve `true` si el número es par, `false` en caso contrario.
  - Método `esImpar(int numero)`: devuelve `true` si el número es impar, `false` en caso contrario.
  - Método `esPrimo(int numero)`: devuelve `true` si el número es primo, `false` en caso contrario.
  - Método `factorial(int numero)`: devuelve el factorial del número.
  - Método `devolverDivisores(int numero)`: devuelve un `List<Integer>` con los divisores del número.
  - Método `esPerfecto(int numero)`: devuelve `true` si el número es perfecto, `false` en caso contrario.

- `UtilidadesTexto`:
  - Método `esPalindromo(String cadena)`: devuelve `true` si la cadena es un palíndromo, `false` en caso contrario.
  - Método `contarVocales(String cadena)`: devuelve el número de vocales en la cadena.
  - Método `contarConsonantes(String cadena)`: devuelve el número de consonantes en la cadena.
  - Método `contarPalabras(String cadena)`: devuelve el número de palabras en la cadena.
  - Método `contarCaracteres(String cadena)`: devuelve el número de caracteres en la cadena.


Dentro del proyecto, crea una clase `TestUtilidadesNumeros` y `TestUtilidadesTexto` con métodos para probar las funcionalidades de las clases anteriores.

Dentro del archivo `pom.xml`, indica lo siguiente:

- formato de empaquetado: `jar`.
- versión de Java: `21`.
  

#### Acciones Maven

Desde la terminal, ejecuta los siguientes comandos:

1. **Limpiar el proyecto**.
2. **Compilar el proyecto**.
3. **Empaquetar el proyecto en un JAR**.


### Configurar repositorio Maven de clases

#### Agregar repositorio maven hosted

- Dentro del fichero `pom.xml` añadir el siguiente fragmento de código:

```xml
<distributionManagement>
    <repository>
        <id>demo-repo</id>
        <url>http://<ip_del_servidor>:8081/...</url>
    </repository>   
</distributionManagement>
```

#### Agregar configuración de repositorio

- Dentro del fichero `settings.xml` de Maven, en `%userprofile%\.m2\settins.xml` añadir el siguiente fragmento de código:

```xml
<servers>
    <server>
        <id>demo-repo</id>
        <username>alumnouser</username>
        <password>alumnouser</password>
    </server>
</servers>
```

#### Subir el proyecto al repositorio

Desde la terminal, ejecuta los siguientes comandos:

1. `mvn clean package`.
2. `mvn deploy`.



### Utilizar librería de otro compañero





