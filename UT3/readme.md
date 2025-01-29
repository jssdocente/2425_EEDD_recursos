# Tema 3. Instalación y uso de entornos de desarrollo

<img src="https://raw.githubusercontent.com/joseluisgs/EntornosDesarrollo-00-2022-2023/master/images/entornos.png" width="300px">

#### Recursos

- [JetBrains](https://www.jetbrains.com/)
  - [IntelliJ IDEA](https://www.jetbrains.com/idea/)

## 🕶️ Contenidos

1. [Entornos de desarrollo](#1-entornos-de-desarrollo)
2. [IDEs más utilizados](#2-ides-más-utilizados)
3. [Principales IDEs genéricos](#3-principales-ides-genéricos)
4. [Principales IDEs específicos](#4-principales-ides-específicos)

## ➡️ A fondo

- [IntellJ IDEA IDE](./docs/doc_intellj_IDE.md)
- [Intellj para principiantes](./docs/intellj/doc_intellj_principiantes.md)
- [Paquetes en Java](./docs/doc_java_packages.md)
- [Temas prácticos con Intellj IDEA](./docs/intellj/doc_temas_practicos.md)

## 🧬 Ampliación

- [Variable de entorno JAVA_HOME](./docs/doc_javahome.md)
- [SDKMAN! Gestor de SDKs](./docs/doc_sdkman.md)

## 1. Entornos de desarrollo

Un entorno de desarrollo o IDE (Integrated Development Environment) es una aplicación informática que está compuesta por un conjunto de herramientas que facilitan la tarea al programador de forma que ayuda a desarrollar aplicaciones con más rapidez.

Los entornos de desarrollo son utilizados en la fase de codificación del ciclo de vida de software independientemente del modelo que se utilice.

Existen entornos de desarrollo para un solo lenguaje o para múltiples lenguajes.

Los elementos fundamentales que suelen encontrarse en un entorno integrado de desarrollo de software son los siguientes:

**Editor de código**: Proporciona una interfaz para escribir y editar el código fuente. Suele incluir características como resaltado de sintaxis, autocompletado, indentación automática y otras utilidades para facilitar la escritura del código.

**Compilador/Intérprete**: Permite compilar o interpretar el código fuente en un formato ejecutable o en bytecode, dependiendo del lenguaje de programación utilizado. Algunos IDEs también ofrecen la capacidad de ejecutar el código directamente desde el entorno.

**Depurador**: Es una herramienta que ayuda a identificar y corregir errores en el código. Permite establecer puntos de interrupción, examinar el estado de las variables, ejecutar el código paso a paso y realizar otras operaciones para analizar y solucionar problemas en el programa.

**Gestión de proyectos o ficheros**: Permite crear, organizar y administrar proyectos de desarrollo de software. Esto incluye la capacidad de crear estructuras de directorios, agregar o eliminar archivos, gestionar dependencias y realizar otras tareas relacionadas con la organización del proyecto.

**Control de versiones**: Algunos IDEs incluyen integración con sistemas de control de versiones como Git, que permiten realizar seguimiento de cambios en el código, realizar confirmaciones (commits), fusionar (merge) ramas y otras operaciones relacionadas con la gestión del código fuente.

**Herramientas de construcción**: Algunos IDEs proporcionan herramientas para automatizar el proceso de construcción del software, como la generación de archivos de configuración, la compilación, el empaquetado y otras tareas relacionadas con la construcción del proyecto.

**Integración con herramientas externas**: Los IDEs suelen ofrecer integración con otras herramientas y servicios externos, como sistemas de gestión de bases de datos, terminal, servidores web, frameworks, bibliotecas, entre otros, para facilitar el desarrollo y la integración con otros componentes del sistema.

**Plugins**: son complemento que se relacionan con otras herramientas para agregarle una nueva función y generalmente muy específica. Esta aplicación adicional es ejecutada por la aplicación principal.

**Soporte para pruebas**: Algunos IDEs ofrecen soporte para la escritura y ejecución de pruebas unitarias, pruebas de integración y otras pruebas relacionadas con el desarrollo de software.

**Refactorización**: Algunos IDEs ofrecen herramientas para refactorizar el código, es decir, para reestructurarlo de manera que mejore su legibilidad, mantenibilidad y rendimiento sin cambiar su comportamiento.

**Generación de documentación**: Algunos IDEs ofrecen herramientas para generar documentación a partir del código fuente, como comentarios, descripciones de clases, métodos, variables, entre otros.

**Soporte para lenguajes y frameworks**: Los IDEs suelen ofrecer soporte para múltiples lenguajes de programación y frameworks, proporcionando herramientas específicas para cada uno de ellos, como resaltado de sintaxis, autocompletado, refactorización, generación de código, entre otros.

**Personalización**: Algunos IDEs permiten personalizar la apariencia y el comportamiento del entorno, como la disposición de las ventanas, los atajos de teclado, los temas, los colores, las fuentes, entre otros.

**Integración con sistemas de gestión de tareas**: Algunos IDEs ofrecen integración con sistemas de gestión de tareas, como JIRA, Trello, Asana, entre otros, para facilitar la administración de tareas relacionadas con el desarrollo de software.

## 2. IDES más utilizados

Actualmente existen muchos entornos de desarrollo integrados (IDEs) disponibles para los desarrolladores, cada uno con sus propias características, ventajas y desventajas. Algunos son relativamente simples como por ejemplo (Sublime Text, Atom, Visual Studio Code), mientras que otros son más complejos y están orientados a entornos de desarrollo empresariales (Eclipse, NetBeans, IntelliJ IDEA).

Los IDEs los podemos clasificar según diferentes criterios:

1. Específicos o genéricos
2. De código abierto o propietarios
3. Gratuitos o de pago
4. Basados en la nube o de escritorio
5. Según el SO en el que se ejecutan

### IDEs específicos o genéricos

**IDEs específicos para un lenguaje de programación**: Están diseñados para trabajar con un lenguaje de programación en particular, proporcionando herramientas específicas para ese lenguaje, como resaltado de sintaxis, autocompletado, refactorización, generación de código, entre otros. Ejemplos de IDEs específicos para un lenguaje de programación son PyCharm para Python, IntelliJ IDEA para Java, Visual Studio para C#, entre otros.

**IDEs genéricos**: Están diseñados para trabajar con múltiples lenguajes de programación, proporcionando herramientas que son útiles para el desarrollo de software en general, como un editor de código, un compilador/intérprete, un depurador, un gestor de proyectos, un control de versiones, entre otros. Ejemplos de IDEs genéricos son Visual Studio Code, Eclipse, NetBeans, entre otros.

### IDEs de código abierto o propietarios

**IDEs de código abierto**: Son aquellos cuyo código fuente está disponible para su inspección, modificación y redistribución por parte de la comunidad de desarrolladores. Ejemplos de IDEs de código abierto son Eclipse, NetBeans, Visual Studio Code, como principales ejemplos.<br>

| Ventajas                                                                                                           | Desventajas                                                                                     |
| ------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------- |
| **Gratuitos**: No tienen coste de licencia.                                                                        | **Soporte técnico**: No siempre tienen soporte técnico.                                         |
| **Flexibles**: Pueden ser modificados y personalizados por la comunidad de desarrolladores.                        | **Estabilidad**: No siempre son tan estables como los IDEs propietarios.                        |
| **Comunidad**: Suelen tener una comunidad de desarrolladores activa que contribuye al desarrollo y mejora del IDE. | **Funcionalidades limitadas**: A veces ofrecen menos funcionalidades que los IDEs propietarios. |

**IDEs propietarios**: Son aquellos cuyo código fuente no está disponible para su inspección, modificación y redistribución por parte de la comunidad de desarrolladores. Ejemplos de IDEs propietarios son IntelliJ IDEA Ultimate Edition, Visual Studio, PyCharm, entre otros.

### IDEs gratuitos o de pago

**IDEs gratuitos**: Son aquellos que se pueden utilizar sin costo alguno, ya sea porque son de código abierto o porque ofrecen una versión gratuita con funcionalidades limitadas. Los de código abierto son gratuitos por licencia, y no se puede cobrar por su uso, pero su principal problema es su soporte técnico.

**IDEs de pago**: Son aquellos que requieren el pago de una licencia para su uso, ya sea porque son propietarios o porque ofrecen una versión de pago con funcionalidades adicionales. Los IDEs de pago suelen ofrecer soporte técnico, estabilidad y funcionalidades avanzadas, pero tienen un coste asociado.

### IDEs basados en la nube o de escritorio

En los últimos años se están popularizando el uso de IDEs basados en la nube, que permiten desarrollar aplicaciones directamente desde el navegador web, sin necesidad de instalar ningún software adicional en el equipo. Veámos sus ventajas e inconvenientes.

**IDEs basados en la nube**: Son aquellos que se ejecutan en un servidor remoto y se accede a ellos a través de un navegador web.<br>
Estos IDEs ofrecen ventajas como la accesibilidad desde cualquier lugar y dispositivo, la facilidad de colaboración en proyectos, la escalabilidad y la flexibilidad, pero también tienen desventajas como la dependencia de la conexión a Internet, la limitación de recursos, la privacidad y la seguridad de los datos, entre otros.

Ejemplos de IDEs basados en la nube son Cloud9, Codeanywhere, Eclipse Che, y JetBrains Space (aunque este último es más que un IDE).

**IDEs de escritorio**: Son aquellos que se instalan y ejecutan en el equipo del desarrollador, proporcionando un entorno de desarrollo local. Estos IDEs ofrecen ventajas como la independencia de la conexión a Internet, el control total sobre el entorno de desarrollo, la privacidad y la seguridad de los datos, pero también tienen desventajas como la falta de accesibilidad desde cualquier lugar y dispositivo, la dificultad de colaboración en proyectos, la necesidad de recursos locales, entre otros.

### IDEs según el SO en el que se ejecutan

**IDEs multiplataforma**: Son aquellos que se pueden ejecutar en diferentes sistemas operativos, como Windows, macOS y Linux. Estos IDEs ofrecen ventajas como la portabilidad, la flexibilidad y la compatibilidad con diferentes entornos de desarrollo, pero también tienen desventajas como la necesidad de mantener la coherencia entre las diferentes versiones, la dependencia de las bibliotecas y herramientas del sistema, entre otros.

Ejemplos de IDEs multiplataforma son Visual Studio Code, Eclipse, NetBeans, IntelliJ IDEA, entre otros.

En algunas ocasiones, el IDE solo está disponible para un sistema operativo en concreto, como Xcode para macOS, o Visual Studio para Windows, no por una limitación del IDE en sí mismo, sino por que la plataforma a la que va dirigido.

**IDES específicos para un sistema o plataforma**: Son aquellos que están diseñados para un sistema operativo en particular, como Windows, macOS o Linux. Cuando un IDE está disponible solamente para un SO, suele ser o bien porque el IDE utiliza tecnologías específicas de ese SO, o bien porque el IDE está orientado a un tipo de desarrollo específico para ese SO.
Tamibén aunque en menor medida, porque el IDE sea muy joven y no haya sido portado a otros SO.

Un caso muy significativo es Xcode para macOS, y todo el entorno de desarrollo de Apple, que es exclusivo para macOS, y que es el entorno de desarrollo para iOS, macOS, watchOS y tvOS. Tambien su su lenguaje de programación Swift, que es exclusivo para el desarrollo de aplicaciones para los dispositivos de Apple.

El caso de Microsoft aunque parecido a Apple, es diferente, ya que Visual Studio Code es multiplataforma, pero Visual Studio es exclusivo para Windows, aunque se puede ejecutar en macOS y Linux con ciertas limitaciones.

Microsoft desde hace unos años ha abierto sus miras, y ha cambiado radicalmente de estrategia, sacando frameworks como el .Net Core, que es multiplataforma, y que ha abierto el desarrollo de aplicaciones a otros sistemas operativos, y no solo a Windows.

## 2. Principales IDEs genéricos

Como se indico en el punto anterior, los IDEs genéricos suelen permitir trabajar con varios lenguajes de programación, y suelen ser multiplataforma, por lo que se pueden ejecutar en diferentes sistemas operativos. Pero tienen un handicap muy importante, son como die el refrán "aprendiz de todo, maestro de nada", es decir, están pensados para un uso general, pero que no destacan en nada en concreto.

### Visual Studio Code

Una excepción a esto es Visual Studio Code, que aunque es un IDE genérico, es muy potente, y tiene una gran cantidad de extensiones que lo hacen muy versátil, y que lo hacen destacar en muchos aspectos. Actualmente es uno de los IDEs más utilizados, por sus bajos requerimientos de hardware, su facilidad de uso, su gran cantidad de extensiones, y su gran comunidad de desarrolladores.

Visual Studio Code es un editor de código fuente desarrollado por Microsoft para Windows, Linux y macOS. Incluye soporte para la depuración, control integrado de Git, resaltado de sintaxis, finalización inteligente de código, fragmentos y refactorización de código. También es personalizable, por lo que los usuarios pueden cambiar el tema del editor, los atajos de teclado y las preferencias. Es gratuito y de código abierto, aunque la descarga oficial está bajo software propietario, y se publica bajo una licencia de fuente cerrada, pero el código fuente está disponible bajo la licencia MIT.

La evolución de este IDE es constante, y cada pocos meses sacan nuevas carácteristicas. Además, la comunidad de desarrolladores es muy activa, y se pueden encontrar extensiones para casi cualquier cosa.

También al ser Microsoft, tiene una gran integración con sus servicios, como Azure, y con sus lenguajes de programación, como C#, y .Net Core, además de tener una gran empresa detrás le da prestigio, y seguridad que no se va a quedar obsoleto.

### Atom y Sublime Text

Atom y Sublime Text son dos editores de texto muy populares, que aunque no son IDEs propiamente dichos, tienen una gran cantidad de extensiones que los hacen muy potentes, y que los hacen destacar en muchos aspectos.

Con la irrupción de Visual Studio Code, han perdido algo de protagonismo, pero siguen siendo muy utilizados, y tienen una gran comunidad detrás.

Más que IDEs se les puede considerar como editores de texto avanzados, con enfoque en la edición de código fuente, y con una gran cantidad de extensiones que los hacen muy versátiles.

### Eclipse

Eclipse es un entorno de desarrollo integrado (IDE) que se utiliza en la actualizad principalmente para el desarrollo de aplicaciones en Java, aunque también se puede utilizar para otros lenguajes de programación a través de complementos. Es multiplataforma y está escrito en Java. Eclipse es un proyecto de código abierto que se puede utilizar para el desarrollo de aplicaciones de escritorio y aplicaciones web. También se puede utilizar para el desarrollo de aplicaciones móviles con Android.

Eclipse suele ser la puerta de entrada al desarrollo de aplicaciones en Java, y es muy utilizado en el mundo académico, aunque en el mundo empresarial ha perdido algo de protagonismo con la irrupción de IntelliJ IDEA.

Ventajas de Eclipse:

- **Comunidad activa**: Eclipse tiene una gran comunidad de desarrolladores que contribuyen al desarrollo y mejora del IDE.
- **Extensible**: Eclipse es altamente extensible a través de complementos que proporcionan soporte para diferentes lenguajes de programación, herramientas de desarrollo, bibliotecas, frameworks, entre otros.
- **Multiplataforma**: Eclipse se puede ejecutar en diferentes sistemas operativos, como Windows, macOS y Linux.
- **Gratuito**: Eclipse es de código abierto y se puede utilizar sin costo alguno.

Desventajas de Eclipse:

- **Rendimiento**: Eclipse puede ser lento y consumir muchos recursos, especialmente cuando se utilizan muchos complementos.
- **Curva de aprendizaje**: Eclipse puede tener una curva de aprendizaje empinada para los principiantes, especialmente si se utilizan muchos complementos.
- **Interfaz de usuario**: La interfaz de usuario de Eclipse puede ser confusa y desordenada, especialmente para los principiantes.
- **Soporte técnico**: Eclipse no siempre tiene soporte técnico, y la documentación puede ser escasa o desactualizada.
- **Estabilidad**: Eclipse no siempre es tan estable como otros IDEs, y puede tener problemas de rendimiento y errores.
- **Funcionalidades limitadas**: Eclipse a veces ofrece menos funcionalidades que otros IDEs, especialmente en áreas como la depuración, la refactorización y la generación de código.

En general, Eclipse es un IDE muy potente, pero que ha perdido algo de protagonismo con la irrupción de IntelliJ IDEA, que es más moderno, más potente, y más fácil de utilizar, y que tiene una gran empresa detrás, como es JetBrains.

### NetBeans

NetBeans es un entorno de desarrollo integrado (IDE) que se utiliza principalmente para el desarrollo de aplicaciones en Java, aunque también se puede utilizar para otros lenguajes de programación a través de complementos. Es multiplataforma y está escrito en Java. <br>

NetBeans es un proyecto de código abierto que se puede utilizar para el desarrollo de aplicaciones de escritorio y aplicaciones web. También se puede utilizar para el desarrollo de aplicaciones móviles con Android.

**Eclipse vs NetBeans** tabla comparativa

Ambos IDEs son muy parecidos, son multiplataforma, y están escritos en Java, y son de código abierto, y se utilizan principalmente para el desarrollo de aplicaciones en Java, aunque también se pueden utilizar para otros lenguajes de programación a través de complementos.

La principal diferencia entre ellos radica en su arquitectura, mientras que Eclipse es un IDE basado en plugins, NetBeans es un IDE monolítico, es decir, que todo está integrado en el mismo paquete, y no necesita de plugins para funcionar. De esto último se deduce que NetBeans es más fácil de instalar y de utilizar, y que es más estable, pero a cambio es menos versátil, y es más difícil de extender.

### IntelliJ IDEA

IntelliJ IDEA es actualmente el IDE más utilizado para el desarrollo de aplicaciones en Java, y es el que más está creciendo en los últimos años. Es un IDE de código cerrado, y de pago, aunque tiene una versión gratuita, la Community Edition, que es muy potente, y que es suficiente para la mayoría de los desarrolladores.

Aunque su uso principal es para el desarrollo de aplicaciones en Java, también se puede utilizar para otros lenguajes de programación a través de complementos. Es el IDE más completo dentro de la gran oferta de IDEs que tiene JetBrains, y es el que más se utiliza en el mundo empresarial.

## 3. Principales IDEs específicos

Este punto es muy amplio, ya que hay tantos IDEs como lenguajes de programación de cierta relevancia existen, por lo que nos centraremos en los más utilizados, y en los que tienen una gran comunidad detrás.

La mayoría de los IDEs que mencionaremos son realizados por JetBrains, la principal empresa actualmente dedicada al desarrollo de IDEs y que es ampliamente reconocida por la calidad de sus productos.

Todos los IDEs de Jebrains compartes muchas características, como la facilidad de uso, la gran cantidad de extensiones, la gran cantidad de herramientas que tienen integradas, y la gran comunidad de desarrolladores que tienen detrás.

Además la intefaz de usuario es muy similar en todos ellos, por lo que si se conoce uno, es muy fácil cambiar a otro. También los atajos de teclado son muy similares, lo que aumenta mucho la productividad, trasladando los conocimientos de uno a otro.

Todos los IDEs de Jebrains tienen caracteristicas comunes como:

- Control de versiones integrado
- Docker integrado
- Terminal integrado
- Integración con servicios de la nube
- Integración con bases de datos
- Integración con frameworks
- Integración con lenguajes de programación
- Integración con herramientas de pruebas
- Integración con herramientas de análisis de código

### PyCharm

PyCharm es un IDE específico para el desarrollo de aplicaciones en Python, y es el más utilizado en la actualidad. Es un IDE de código cerrado, y de pago, aunque tiene una versión gratuita, la Community Edition, que es muy potente, y que es suficiente para la mayoría de los desarrolladores.

Hoy Python se ha convertido en uno de los lenguajes de programación más utilizados, y PyCharm permite integrarse con la mayoría de las herramientas y frameworks que se utilizan en el desarrollo de aplicaciones en Python, como Django, Flask, y otros.

### WebStorm

WebStorm es un IDE específico para el desarrollo de aplicaciones web, centrandose principalmente en el lenguaje Javascrip y TypeScript.

A través de diferentes plugins, se puede utilizar para trabajar con diferentes frameworks y librerías, como Angular, React, Vue, y otros.

También destaca sobre manera su integración con Node.js, asi como la facilidad de uso para integrar herramientas de control de versiones, como Git (Aunque esta integración es común a todos los IDEs de JetBrains).

### Android Studio

Android Studio es el IDE oficial para el desarrollo de aplicaciones para Android, y es el más utilizado en la actualidad.

Es el IDE oficial de Google, y es el que más se utiliza en el mundo empresarial, y en el mundo académico, aunque está desarrollado por JetBrains, y comparte muchas características con los otros IDEs de la empresa.

Es un IDE muy potente, y con un foco muy claro en el desarrollo de aplicaciones para Android, y tiene una gran integración con las herramientas y servicios de Google, como Firebase, y Google Cloud Platform.

Sin duda, la única opción para el desarrollo de aplicaciones para Android de forma profesional.

### PhpStorm

Es un IDE enfocado al desarrollo de aplicaciones en PHP, siendo el más utilizado para este lenguaje de programación.

Tiene una integración muy potente con los principales frameworks de PHP, como Symfony, Laravel, y otros, y con las BDs más utilizadas, como MySQL, PostgreSQL, y otras.

Al ser PHP un lenguaje del lado del servidor (Backend), pero muy enfocado al desarrollo web, tiene una gran integración con las tecnologías del lado del cliente (Frontend), como HTML, CSS, y JavaScript.

Se puede decir que PHPStorm es WebStorm + PHP + BD/SQl.

### Rider

En el mundo del desarrollo de aplicaciones en .Net, el IDE más utilizado es Visual Studio, pero en los últimos años ha aparecido Rider, un IDE de JetBrains, que está ganando mucha popularidad, y que es muy potente.

Además de las características comunes a todos los IDEs de JetBrains, tiene una gran integración con las herramientas y servicios de Microsoft, como Azure, y con los lenguajes de programación de Microsoft, como C#, y .Net Core.

También dentro del sector de los videojuegos, es muy utilizado, ya que tiene una gran integración con Unity, el motor de videojuegos más utilizado en la actualidad.

Rider frente a Visual Studio, es más ligero, y más fácil de utilizar, y sobre todo mantiene la filosofía de JetBrains, que es la facilidad de uso, y la unififormidad entre todos sus IDEs. Esto lo hace la opción preferida para muchos desarrolladores que hasta hace unos años la única opción que tenían era Visual Studio.

### RubyMine

RubyMine es un IDE específico para el desarrollo de aplicaciones en Ruby, un lenguaje de programación poco conocido actualmente, pero que sigue teniendo una gran cantidad de software desarrollado en él y que sigue siendo muy utilizado.

Ruby es un lenguaje de programación que se utiliza muchas cosas, desde el desarrollo de aplicaciones web hasta el análisis de datos. También es mu fácil de usar en comparación con otros lenguajes, y es batante fácil de aprender.

Ruby fue lanzado en 1995, y es un lenguaje de programación interpretado, orientado a objetos, con una sintaxis elegante y fácil de leer. Es un lenguaje de programación de alto nivel, que se utiliza para el desarrollo de aplicaciones web, aplicaciones de escritorio, aplicaciones móviles, juegos, herramientas de línea de comandos, entre otros.

Ruby es gratuito y de código abierto, y se puede utilizar en diferentes sistemas operativos, como Windows, macOS y Linux. Ruby tiene una gran comunidad de desarrolladores que contribuyen al desarrollo y mejora del lenguaje, y proporciona una gran cantidad de bibliotecas y frameworks para el desarrollo de aplicaciones.

_Su framework más conocido es Ruby on Rails, que es un framework de desarrollo web que utiliza el lenguaje de programación Ruby._

### GoLand

GoLand es un IDE específico para el desarrollo de aplicaciones en Go, un lenguaje de programación que ha sido desarrollado por Google, y que está ganando mucha popularidad en los últimos años.

Go, al igual que C y C++, es un lenguaje compilado y concurrente, pero con un enfoque muy distinto a otros lenguajes que utilizan Threads (hilos)

Características de Go:

- Simplicidad: Go es un lenguaje de programación simple y fácil de aprender, con una sintaxis clara y concisa.
- Eficiencia: Es eficiente y rápido, con un tiempo de compilación muy rápido y un rendimiento alto.
- Funcionalidades: Está orientado a la programación de sistemas, con soporte para concurrencia, paralelismo, comunicación en red, gestión de memoria, entre otros.

### RustOver

Es un IDE específico para el desarrollo de aplicaciones en Rust, un lenguaje de programación que ha sido desarrollado por Mozilla, y que está ganando mucha popularidad en los últimos años.

Se denomina el sucesor de C++, ya que su objetivo es ser un lenguaje de programación de bajo nivel, pero con una sintaxis más moderna, y con menos errores.

_¿ Por qué Rust ?_

- **Rendimiento**
  Es increiblemente rápido y eficiente con la memoria. Sin runtime ni recolector de basura. Puede sustentar servicios de rendimiento crítico y sistemas operativos. Puede ejecutarse en dispositivos integrados y en la nube.

- **Fiabilidad**
  Es un lenguaje muy fiable con un sistema de tipos muy rico y flexible, con énfaxis en la seguridad y la concurrencia, eliminando gran cantidad de errores en tiempo de compilación.

- **Productividad**
  Posee una documentación muy completa, y una comunidad muy activa, gran cantidad de librerías.

¿ Qué se puede hacer con Rust ?

- Líneas de comandos
- WebAssembly (permte potenciar JavaScript)
- Redes (servidores, clientes, etc)
- Dispositivos integrados: IoT, Robótica, etc
