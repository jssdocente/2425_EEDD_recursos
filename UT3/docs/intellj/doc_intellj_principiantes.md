# IntellJ IDEA para principiantes

Durante el desarrollo de un proyecto, es muy común usarmos IDEs para facilitar todo el proceso de build del proyecto, sea para la realización de compilación de archivos o la ejecución de la aplicación.

Hoy veremos algunos trucos y tips de IntelliJ IDEA, una de las más famosas y poderosas IDEs del mundo Java.

Para poder poner en práctica lo que vayas aprendiendo en este documento, necesitaras un proyecto Java para ir practicando. Por eso vamos a considerar un proyecto Java simple para un `inventario` por lo que todos los ejemplos se volcarán a este ejemplo.

¿Todo listo? Comencemos.

### Configurar los atajos de IntellJ

Uno de los primeros grandes pasos con IntellJ es ajustar los atajos de teclado, en este caso el mapa de teclas (keymap). En este punto debes estar pensando;

*"Entonces los atajos no vienen preconfigurados?"*

Sí, los atajos **ya vienen** preconfigurados pero dependiendo de la plataforma, !puede ser una configuración distinta a la configuración estándar!

### ¿Qué mapa de teclas debo elegir?

Al ajustar el mapa de teclas, verás varias alternativas que hacen referencia a herramientas como Eclipse IDE o NetBeans. Tienes que elegir con el que te sientas más cómodo, pero algunas opciones solo existen en IntellJ y no en Eclipse, por lo que serán diferentes y tendrás que adaptarte.

Todos los IDEs de Jetbrains funcionan con el mismo mapa de teclas, por lo que si aprendes uno, podrás usar los demás sin problemas, por lo que os recomiendo que os acostumbréis a los atajos de IntelliJ.

Aprender los atajos de teclado os hará más productivos, pero requiere tiempo el memorizarlos. Recordar que los músculos tienen memoria, por lo que cuanto más practiques, más fácil será recordar los atajos.

### Configurar el mapa de teclas

En general este tipo de configuraciones no suele cambiar mucho entre versiones del IDE, pero siempre es adecuado acudir a la ayuda oficial.

[Configuar atajos teclado](https://www.jetbrains.com/help/idea/configuring-keyboard-and-mouse-shortcuts.html)


#### Aprender los atajos

IntelliJ proporciona un documento de referencia para los atajos, basado en el mapa de teclas configurado. Este documento se conoce como Keymap References. Para verlo, ve al menú Help > Keyboard Shortcuts PDF. 

Esto abrirá un PDF con los atajos más utilizados para el sistema operativo actual.

El mapa de teclas hace referencia al último mapa de teclas configurado, por lo que si cambia el mapa de teclas, recuerda solicitar el documento en Keymap References otra vez.


### Organización: Projectos y Módulos

El desarrollo en IntellJ IDEA inicia con un proyecto. Los proyectos ayudan a organizar el código y recursos en una unidad simple y fácil de almacenar y compartir. En pocas palabras, un proyecto es un directorio que mantiene toda tu aplicación. Un proyecto típico es normamente un conjunto de configuraciones y uno o varios módulos (dependencias).

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/5e43281b-8809-4c23-b1a7-bf1faa34024e" style="display: block; margin: 0 auto;" width="400px" >

Un proyecto es un envoltorio que mantiene módulos juntos, permitiendo dependencias entre ellos, y almacena una configuración común, compartiendola.

Un móudlo es también compuesto de un fichero `.iml` que almacena una representación interna de la configuración del módulo y es por así decirlo, es contenedor raíz, el cual almacena código fuente, recursos, tests, etc..

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/607bbe7a-584a-40a3-9ef3-ebbdf557d996" style="display: block; margin: 0 auto;" width="400px" >

#### Projecto, módulo y configuraciones globales

Hay 3 tipos de configuraciones en IntellJ IDEA: 

- Global
- Projecto
- Módulo

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/a151514f-2835-4b09-9768-8a83f57f06d0" style="display: block; margin: 0 auto;" width="400px"><br>

> **Configuraciones a nivel de módulo**<br>
> Solo se aplican a un módulo y se almacenan en un fichero .iml. Un módulo puede tener un SDK y un nivel de lenguaje que > pueden ser difierentes de aquellos configurados para el proyecto, y sus propias librerias.

> **Configuraciones a nivel de projecto**<br>
> Estas configuraciones aplican solo al proyecto actual, y son almacenadas junto con otros ficheros del proyecto dentro de una carpeta `.idea` en formato `xml`.

> **Configuraciones globales**<br>
> Estas configuraciones aplican aplican a todos los poryectos de una instalación específica de IntellJ IDEA. Tales configuraciones inluyen apariencia del IDE (temas, colores, atajos), los plugins instalados, configuraciones de depuración y mucho más.


### Crear el primero proyecto

En el mundo Java existen muchas tecnologías y frameworks, y IntellJ soporta la mayoría de ellas, por lo que al crear un proyecto debemos indicar con qué opciones vamos a trabajar. 

En nuestro caso como principiantes, vamos a trabar en los más básico, en un proyecto sencillo sin ninguna complicación.

Para crear nuestro primer proyecto, [seguir la guia oficial](https://www.jetbrains.com/help/idea/creating-and-running-your-first-java-application.html).

El proyecto con de nombre **Inventario**, elegir el JDK que querais, y crear el proyecto.


### Generar código

Crear código va a ser la principal ocupación como desarrolladores, es por eso, que el IDE pone gran parte de su enfoque sobre esto, y nos facilita mucho este cometido.

En la siguiente guía/ayuda ofical se indica las funcionalidades que tiene el IDE sobre este punto.

[Generar código](https://www.jetbrains.com/help/idea/generating-code.html)


#### Plantillas o Snippets de código

IntellJ facilita mucho la creación de código repetitivo, evitando las tareas pesadas a través de un concepto que llama "Snippets o fragmentos de código".

Estos `snippets` permite generar tanto fragmentos de código, como archivos completos. Desde el argot del IDE, estas carácteristicas se llaman `File Template` y `Live Template`

- [Live Templates](https://www.jetbrains.com/help/idea/using-live-templates.html#live_templates_types)
- [File Templates](https://www.jetbrains.com/help/idea/using-file-and-code-templates.html)


### Ejecutar la aplicación

Uno de los puntos que repetiremos más veces al desarrollar una aplicación, es ejecutarla, depurarla, una y otra vez, y esto lo vamos a tener que realizar con diferentes configuraciones, para BDs, entornos, credenciales, etc... todo esto es complejo y propenso a errores.

Para este fin, IntellJ pone a nuestra disposición el concepto de `Configuraciones`. 

Como siempre hacemos uso de la guía oficial:

- [Ejecutar aplicaciones](https://www.jetbrains.com/help/idea/run-java-applications.html)

Al ejecutar la aplicación veremos si el resultado es correcto o no, pero muchas veces no sabremos porqué no funciona, o el motivo de porque hace o no hace algo, o el motivo por el cual lanza un error.

Una práctica habitual es incluir mensajes de `log` que permitan verificar lo que la aplicación está realizando, pero este proceso es muy tedioso, y pensado para etapas más avanzadas del diseño de la aplicación. Para estas etapas tempranas, en el que necesito saber qué exactamente está haciendo mi código, es necesario contar con otras herramientas, como la `depuración paso a paso`

**¿Por qué depurar?**

- Encontar y solucionar problemas (bugs)
- Analizar el código
    - Qué partes de el código son ejecutadas
    - Ser familiar con el código nuevo
- Cambios de comportamiento
    - Reproducir complejas configuraciones
    - Intercambiar el estado de la aplicación, para simular diferentes condiciones o estados


- [Depurar código, nuestro gran aliado](https://www.jetbrains.com/help/idea/debugging-code.html)

IntellJ tiene funciones muy poderosas que te ayudarán mucho en conseguir tus objetivos y ser mejojr desarrollador. Como todo lleva su tiempo, pero aprender y manejar bien la depuración es pasar a otro nivel como desarrollador.

Para comenzar, aquí tienes un pequeño tutorial, para depurar tu primera aplicación Java:

- [Tutorial: Depurar tu primera aplicación Java](https://www.jetbrains.com/help/idea/debugging-your-first-java-application.html)


### Navegar en el proyecto / Módulos

La organización del proyecto es fundamental, manejar las carpetas, los paquetes, saber qué forma parte del código fuente y que no, como son los ficheros compilados, artefactos generados y otras librerias de terceros.

IntellJ tiene una herramienta muy potente para ello, la "Ventana Proyecto", la cual permite una mirada al proyecto desde varios puntos de viesta y ejecutar diferentes tareas.

[Vetana Gestión Proyecto](https://www.jetbrains.com/help/idea/project-tool-window.html)









