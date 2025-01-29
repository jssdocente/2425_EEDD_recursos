# Uso de paquetes en Java

Los paquetes en Java (packages) son la forma en la que Java nos permite agrupar de alguna manera lógica los componentes de nuestra aplicación que estén relacionados entre sí.

## Paquetes en Java

Un paquete en Java es un conjunto de clases e interfaces que proporcionan una funcionalidad específica.

Los paquetes en Java se utilizan para:

- Evitar conflictos de nombres: dos clases con el mismo nombre pueden coexistir si están en paquetes diferentes.
- Hacer que las clases sean más fáciles de encontrar.
- Proporcionar una estructura de directorios para las clases.

## Declaración de paquetes

Para declarar un paquete en Java, se utiliza la palabra clave `package` seguida del nombre del paquete. La declaración de paquetes debe ser la primera declaración en un archivo fuente de Java.

```java
package com.mycompany.myapp;
```

## Tips en la declaración de paquetes

### El paquete en Java se declara antes que cualquier otra cosa:

La declaración del paquete debe estar al principio del archivo Java, es decir, es la primera línea que se debe ver en nuestro código o archivo .java. Primero se declara el paquete, y luego podremos poner los imports y luego las clases, interfaces, métodos, etc.

### Cada punto en la ruta del paquete es una nueva carpeta:

Cuando se escribe la ruta del paquete en Java, se pueden especificar una ruta compleja usando el punto ".", por ejemplo en el código anterior, nuestra clase, interfaz o archivo estará ubicado en una carpeta llamada "paquete" la cual a su vez está en la carpeta "del" y esta también se encuentra dentro de una carpeta llamada "ruta". De este modo si queremos por ejemplo que una clase quede al interior de una carpeta llamada "mi_paquete" y ésta al interior de una carpeta llamada "otro_paquete" pondríamos:

```java
package otro_paquete.mi_paquete;

/*Se usa el punto para separar cada carpeta
  equivale a la ruta otro_paquete/mi_paquete dentro del proyecto*/
public class mi_clase
{

}
```

Si una clase no tiene un paquete declarado, entonces se considera que está en el paquete por defecto (default package).

### El paquete por defecto

El paquete por defecto es el paquete que se utiliza cuando no se declara un paquete. Si no se declara un paquete, entonces la clase estará en el paquete por defecto. El paquete por defecto no tiene nombre, es decir, no se le pone ningún nombre, simplemente se deja vacío.

```java
/*Esta clase estará en el paquete por defecto*/
public class MiClase
{

}
```

### Classpath y paquetes en Java

El classpath es una variable de entorno que se utiliza para indicarle a Java dónde buscar las clases que se necesitan para ejecutar un programa. Si una clase está en un paquete, entonces el classpath debe incluir la ruta del paquete.

Por ejemplo, si una clase está en el paquete "com.mycompany.myapp", entonces el classpath debe incluir la ruta "com/mycompany/myapp". Cuando se ejecuta un programa Java, el classpath se utiliza para buscar las clases que se necesitan para ejecutar el programa. Si una clase se busca y no se indica el paquete, entonces se buscará en el paquete por defecto.
Es por tanto vital que el classpath esté bien configurado para que Java pueda encontrar las clases que necesita para ejecutar un programa.

### Prácticas recomendadas para nombrar paquetes en Java

También hay varias buenas prácticas y recomendaciones para crear y declarar paquetes en Java. En general, los paquetes en java se declaran siempre en minúsculas y en caso de ser necesario las palabras se separan usando un guión bajo "\_".

### Si no se declara un paquete (paquete por defecto):

Si decidimos no declarar un paquete para nuestra clase, ésta quedará en un paquete que se conoce como paquete por defecto (default package), en este paquete estarán todas las clases que no tengan un paquete declarado. Aunque esto no genera errores de compilación ni nada parecido, siempre es recomendable declarar un paquete a cada componente de nuestro programa Java para poder darle diferentes niveles de seguridad o acceso a dichos componentes y mantener todo ordenado.

### Al momento de declarar el paquete en Java:

Es común usar la primera letra en mayúscula cuando se declara una clase, pues bien, cuando se declaran paquetes es común que todas la letras estén en minúscula y en caso de ser varias palabras separarlas por un guion bajo "\_" por ejemplo "mi_paquete" es adecuado mientras que "MiPaquete" aunque no es incorrecto, no es una buena práctica.

### La estructura de carpetas debe coincidir con la estructura de paquetes:

Cuando se declara un paquete en Java, la estructura de carpetas debe coincidir con la estructura de paquetes. Por ejemplo, si declaramos un paquete "com.mycompany.myapp", entonces la estructura de carpetas debe ser "com/mycompany/myapp".

### Los nombres de los paquetes se suelen escribir al revés:

Los nombres de los paquetes en Java suelen ser nombres de dominio al revés, por ejemplo, si el nombre de dominio de nuestra empresa es "mycompany.com" el nombre del paquete en Java sería "com.mycompany.myapp". Esto se hace para evitar conflictos de nombres con otros paquetes que puedan tener el mismo nombre.

Cuando pensamos en un nombre de paquete, es importante que sea único, es decir, que no exista otro paquete con el mismo nombre en el mundo. Por eso, es común usar el nombre de dominio de la empresa al revés, ya que es muy poco probable que otra empresa tenga el mismo nombre de dominio.

Esto es especialmente importante, cuando nuestro software será utilizado por otras personas, o es por ejemplo una aplicación móvil que será subida a la tienda de aplicaciones, ya que si el nombre del paquete no es único, no podremos subir nuestra aplicación.

## Ejemplo de paquetes en Java

A continuación pondré la declaración de cuatro clases diferentes en paquetes diferentes, cada clase se llamará "Clase_1", "Clase_2", "Clase_3" y "Clase_4" respectivamente.

Voy a jugar un poco con las carpetas donde quedará alojada cada una de las clases para que afiances un poco más el concepto y comprendas bien el funcionamiento de los paquetes en Java y quizá soluciones alguna duda. Por tal motivo, te invito a intentar descifrar la ubicación exacta de cada clase al interior del proyecto según la declaración de su respectivo paquete y ver que sí hayas entendido adecuadamente el tema. Veamos:

Clase 1:

```java
package mis_clases.clases_publicas.clase_1;
public class Clase_1
{

}
```

Clase 2:

```java
package mis_clases.clase_2;
public class Clase_2
{

}
```

Clase 3:

```java
package mis_clases;

public class Clase_3
{

}
```

Clñase 4:

```java
public class Clase_4
{

}
```

- La clase 1 estará ubicada en la carpeta "clase_1" que a su vez estará dentro de la carpeta "clases_publicas" que a su vez estará dentro de la carpeta "mis_clases".
- La clase 2 estará ubicada en la carpeta "clase_2" que a su vez estará dentro de la carpeta "mis_clases".
- La clase 3 estará ubicada en la carpeta "mis_clases" y la clase 4 estará ubicada en la carpeta raíz del proyecto.

De tal forma que la estructura de carpetas es la siguiente:

```
mis_clases
    clase_2
    clases_publicas
        clase_1
Clase_4
```
