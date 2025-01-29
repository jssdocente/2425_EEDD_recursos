# Cómo abrir varios proyetos en IntellJ IDEA

¿ Te has preguntado cómo abrir varios proyectos en IntellJ? Aunque IntellJ no soporta workspaces, hay formas de trabajar con múltiples proyectos en la misma ventana. En este documento te explicamos cómo hacerlo.

### ¿Por qué IntellJ no soporta Workspaces?

IntelliJ IDEA, a diferencia de otros entornos de desarrollo como Eclipse, no utiliza el concepto de workspaces para manejar proyectos. En Eclipse, un workspace es esencialmente un lugar donde se almacenan todos tus proyectos, permitiéndote abrir y trabajar en varios proyectos simultáneamente dentro de una misma instancia de Eclipse.

IntelliJ IDEA, por otro lado, adopta un enfoque diferente. En lugar de tener un workspace que contiene varios proyectos, considera todo como un único proyecto, que puede contener varios módulos. En este contexto, un módulo es como un proyecto en Eclipse. Cada módulo puede tener su propio conjunto de dependencias, su propia configuración de compilación y ejecución, etc.

El enfoque de IntelliJ IDEA tiene varias ventajas. 

- Facilita la gestión de dependencias entre módulos 
- Permite una mayor flexibilidad en la configuración de cada módulo.
  
Sin embargo, también significa que no puedes simplemente abrir varios proyectos en la misma ventana de IntelliJ IDEA de la misma manera que lo harías en Eclipse.

### Abrir varios proyectos

No te preocupes, hacer esto mismo en el que a día de hoy se ha convertido en el IDE estándar para desarrollo en Java es también súper sencillo.

Sólo vas a necesitar cambiar el chip, y empezar a pensar en módulos, cómo lo que en Eclipse probablemente llamabas proyectos.

Para añadir un nuevo proyecto en la misma ventana de tu IntelliJ, sigue estos pasos:

- Haz clic en `File` y selecciona `New`.
- Eligir `Module from Existing Sources`.
- Selecciona el directorio del proyecto que quieres añadir.

¡Y eso es todo! Ya tendrás abierta en tu instancia de IntelliJ todos los proyectos que tienes en esa carpeta de una forma muy similar a como lo hace Eclipse con sus workspaces.

Abrir varios proyectos en Intellij puede parecer un tanto raro al principio, especialmente si estás acostumbrado a trabajar con los workspaces de Eclipse. Pero una vez que te acostumbras, te das cuenta de que es una forma muy potente y flexible de trabajar con varios proyectos a la vez.