# Primeros pasos con Eclipse (Java)

Este tutorial le ayudará a familiarizarse rápidamente con Eclipse, unos de los IDE más utilizados a nivel académico para el desarrollo de Java. Para utilizar Eclipse de forma eficaz, debe familiarizarse y comprender algunos conceptos y componentes clave del IDE: 
workspaces,

- Workbech, 
- Workspaces,
- Perpectivas,
- Editor, 
- Vistas
- Barra de herramientas.

Primero, veamos cómo descargar e instalar Eclipse IDE.

## 1. Descargue e instale Eclipse

Eclipse IDE está disponible en los principales sistemas operativos: Windows, Mac OS X y Linux. Admite arquitectura de CPU de 32 y 64 bits. Eclipse IDE es una aplicación basada en Java, por lo que primero requiere la instalación de JDK/JRE.

### Descargue e instale Eclipse IDE usando el instalador de Eclipse:
De esta forma, descargas un pequeño programa llamado Eclipse Installer. Ejecute este programa y elija el paquete que desee instalar:

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/dc61e4b2-c6b9-4a48-92a1-528ab30108cc" width="400px">

La instalación facilita mucho el resultado satisfactorio de la misma, ya que son muchos binarios y configuraciones las requeridas para un funcionamiento óptimo.

[Descargar el instalador de Eclipse de 64 bits](https://www.eclipse.org/downloads/download.php?file=/oomph/epp/2018-09/R/eclipse-inst-win64.exe)


## 2. Workbech

Una instancia de eclipse se le suele llamar "Workbech" o "banco de trabajo" (traducido literalmente). Un Workbech consiste de uno o más Perpectivas. Y una perpectiva contiene editores y vistas.

Se permite abrir múltoples instancias simultaneamente (via menu Windows-> New Window). Por ejemplo, cuando estamos trabajando sobre 2 proyectos (podemos abrir dos instancias), una para cada proyecto. Pero todos los `Workbechs` son udados para solo un `Workspaces`.

## 3. Workspaces

Workspaces o espacio de trabajo es un directorio en tu computadora (donde los proyectos son almacenadas). Se debe elegir un workspaces cuando se inicia Eclipse (aunque esto puede ser saltado si se elige un Workspaces por defecto.)

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/3272b398-dbf5-49c9-9a6b-18a3dd91484b">

Puede haber varios proyectos en un Workspaces, lo que significa que podemos trabajar con múltiples proyectos simultaneamente. Sin embargo, puedes trabajar in un solo workspaces en una sesión de trabajo de Eclipse. A para intercambiar a otro workspaces, click `File -> Switch` Workspaces desde el menu principal.

Elipse almacena las preferencias separadamente para cada workspaces dentro del `.metadata` directorio en la carpeta raíz del worksapces. Esto significa que cada workspaces tiene su propia configuración para diseños, JDKs, servidores, etc...

> 💡 **Importante** <br>
Un workspaces puede ser usado para agrupar proyectos relacionados que comparten configuraciones comunes. Por ejemplo, para desarrollar una aplicación que consiste de varios proyectos.

La siguiente pantalla muestra múltiples proyectos incluidos en el un workspaces:

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/bc1e4f94-4ac3-4a8a-a286-8b3b84723e80" style="display: block; margin: 0 auto">

## 4. Perpectivas

En Eclipse, una perspectiva proporciona un diseño inicial organizado para ayudar a los programadores a realizar una tarea o trabajo. Cada perspectiva contiene un conjunto diferente de editores y vistas. Por ejemplo, la perspectiva Java contiene los siguientes editores y vistas:

- Editores Java: para editar archivos fuente Java.
- Explorador de paquetes : le permite navegar por los proyectos.
- Esquema : muestra la estructura del archivo fuente en el editor activo.
- Problemas : muestra errores, advertencias y problemas detectados.
- Javadoc : le permite obtener una vista previa del Javadoc de una clase, método, campo…
- Declaración : muestra la declaración de la variable en la posición del cursor.
- Lista de tareas : muestra las tareas descargadas de una popular herramienta de seguimiento de errores como Bugzilla, Mantis...

La siguiente imange es de uan perspectiva de Java:

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/1abf5419-f63f-4c7f-8950-1106691d51c0" style="display: block; margin: 0 auto">

Cuando trabaja en la perspectiva, abre más editores y vistas cuando es necesario, pero inicialmente una perspectiva contiene un conjunto fijo de editores y vistas. Las barras de herramientas y los elementos del menú también cambian según el propósito de la perspectiva activa actual.

Y esta es la perspectiva de depuración que le permite depurar un programa en ejecución:

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/09c9b3cd-d44f-44cd-959a-5c6d5286740d" style="display: block; margin: 0 auto">

De forma predeterminada, Eclipse proporciona varias perspectivas, como se muestra a continuación:

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/d46d4bbe-dc26-4c24-be0e-9df98a33477d" style="display: block; margin: 0 auto"><br>

Puede ver esta lista al abrir una perspectiva desde el menú `Ventana > Perspectiva > Abrir perspectiva > Otro…`
Para el desarrollo de Java, la mayor parte del tiempo se utilizan sólo algunas perspectivas, por ejemplo, *Java, Java EE y Debug*. Si utiliza el control de versiones, cambiará con frecuencia a las perspectivas *Git o Sincronización de equipos* .

En Eclipse, puede cambiar entre las perspectivas abiertas haciendo clic en los iconos de perspectiva en la barra de herramientas o presionando el atajo Ctrl + F8 . 

Puede abrir perspectivas en la misma ventana de la instancia (predeterminada) o en ventanas nuevas.
Tenga en cuenta que diferentes perspectivas pueden tener vistas diferentes, pero todas comparten los mismos editores.
Puede personalizar una perspectiva, por ejemplo, organizar vistas y editores como desee y guardarla como su propia perspectiva.

Para restablecer la perspectiva activa a su diseño predeterminado, haga clic en Ventana > Perspectiva > Restablecer perspectiva…

## Editores

Un editor le permite editar un archivo fuente. Por ejemplo, cuando hace doble clic en un archivo .java  en la vista Explorador de proyectos/Explorador de paquetes , se abre un editor Java en el área del editor que suele estar en el centro del banco de trabajo:

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/0d3cee65-fbc0-434a-a847-0739714d04bf" style="display: block; margin: 0 auto"><br>

Observe que el borde gris en el margen izquierdo del área del editor puede mostrar pequeños íconos para indicar errores, advertencias, problemas e información en la línea correspondiente.

Cada tipo de búsqueda se puede abrir con el editor asociado. Si Eclipse no tiene un editor asociado para un tipo de archivo, intentará abrirlo utilizando un programa externo disponible en el sistema operativo.

Puede haber varios editores abiertos y están apilados en el área del editor, pero solo hay un editor activo a la vez. El nombre del archivo se muestra en la barra de título del editor y el asterisco (*) indica que el editor tiene cambios no guardados.

En Eclipse, puedes usar el atajo *Ctrl + F6* para cambiar entre editores.

## Vistas

Una vista le permite navegar por la información en el Workbench (instancia). Por ejemplo, en la vista Explorador de proyectos , puede navegar por la estructura de proyectos en un espacio de trabajo (Workspaces):

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/6128d05c-d7f9-487d-a7bc-02955f91bed2" style="display: block; margin: 0 auto"><br>

Una vista también proporciona una representación alternativa para respaldar a un editor. Por ejemplo, la vista Esquema muestra elementos estructurales del archivo fuente en el editor activo. Entonces, si está editando un archivo .java  , muestra las clases, campos y métodos de ese archivo:


<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/eb4a53ac-0f18-42cf-b167-dd198e4b3bf8" style="display: block; margin: 0 auto"><br>

Con la vista Esquema, puede saltar rápidamente a un elemento del archivo fuente.

Puede cambiar el tamaño, mover, minimizar y maximizar las vistas en una perspectiva. Una vista se puede separar del banco de trabajo y convertirse en una ventana flotante (haga clic con el botón derecho en la barra de título de una vista y haga clic en Separar ).

Una vista tiene un menú desplegable que ofrece acciones que le permiten personalizar la representación de la vista. Puede acceder a este menú haciendo clic en la flecha hacia abajo en la esquina superior derecha de la vista. Por ejemplo, la siguiente captura de pantalla muestra el menú desplegable de la vista Explorador de proyectos:

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/e4ea5ed9-7eca-476d-8549-492e2eb841d1" style="display: block; margin: 0 auto"><br>

Para abrir una vista en Eclipse, haga clic en Ventana > Mostrar vista . Y para cambiar entre vistas abiertas, presione Ctrl + F7.

## Barra de herramientas

El último componente visual que quiero contarles en Eclipse son las barras de herramientas . Hay 4 tipos de barras de herramientas en Eclipse:

- Barra de herramientas principal : aparece debajo del menú principal, la barra de herramientas principal consta de botones que se agrupan en diferentes secciones: Abrir/crear/guardar proyecto, Ejecutar, Depurar, Navegación, Buscar… Los botones varían dependiendo de la perspectiva actual.

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/25ab7b27-6e41-4261-9eee-4dd72ba8f24b" style="display: block; margin: 0 auto"><br>

- Barra de herramientas de cambio de perspectiva : esta barra de herramientas contiene botones que le permiten cambiar entre perspectivas abiertas en el banco de trabajo. Puede ver esta barra de herramientas en el lado derecho de la barra de herramientas principal:

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/1532807d-46f5-4015-ba3b-63b467b345d8" style="display: block; margin: 0 auto"><br>

También contiene un botón (el que está más a la izquierda) que le permite abrir la lista de todas las perspectivas.

- Barra de herramientas de vista de pila : esta es una barra de herramientas especial que aparece cuando minimiza una vista en una pila de vistas. Los íconos en esta barra de herramientas le permiten abrir una vista individual en la pila. Por ejemplo, aquí está la barra de herramientas que aparece cuando la vista de la Consola está minimizada:

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/bf72b41e-8f37-4f87-ab8d-e64da8b327a4" style="display: block; margin: 0 auto"><br>

Pues estos son los conceptos y componentes más importantes del IDE de Eclipse. Al comprenderlos, sabrá como utilizar el IDE de forma adecuada y eficaz.


## Temas prácticos

### Crear artefacto JAR

Si necesitamos crear un archivo JAR con nuestro proyecto, podemos hacerlo a través de la opción "Exportar" que se encuentra en el menú "Archivo" de Eclipse.

> 💡 **Conocer más** *¿ Qué es un archivo JAR?* <br>
> - Un archivo JAR (Java ARchive) es un archivo ZIP que contiene un conjunto de archivos comprimidos. Conoce más en este [articulo](https://recoverit.wondershare.es/file-tips/what-is-jar-file.html)
> - Otro concepto importante es el archivo de [MANIFEST.MF](https://www.baeldung.com/java-jar-manifest), que es un archivo de metadatos que contiene información sobre los archivos empaquetados en un archivo JAR.

El siguiente [enlace](https://www.eclipse.org/community/eclipse_newsletter/2017/february/article1.php) de la documentación de Eclipse se explican estos conceptos.

Este proceso en Eclipse es sencillo, como se explica en el siguiente articulo. [Eclipse crear un JAR](https://www.tutorialspoint.com/eclipse/eclipse_create_jar_files.htm)

