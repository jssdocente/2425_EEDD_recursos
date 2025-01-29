<!-- omit in toc -->
# SDKMAN, ¿Qué es, cómo se instala y cómo se usa?

<!-- omit in toc -->
## 💼 Recursos

- [Video Makigas: explicación de SDKMAN!](https://youtu.be/ShpX6NMg0Nk)
- [Web SDKMAN!](https://sdkman.io/)

<!-- omit in toc -->
## indice

- [¿Qué es un SDKMAN? ](#qué-es-un-sdkman-)
  - [Características de SDKMAN! ](#características-de-sdkman-)
  - [Instalación de SDKMAN! en Windows](#instalación-de-sdkman-en-windows)
    - [Modificar el script de instalación](#modificar-el-script-de-instalación)
  - [Ejemplo de cómo usar SDKMAN!](#ejemplo-de-cómo-usar-sdkman)
  - [Configurando nuestro IDE y las variables de entorno](#configurando-nuestro-ide-y-las-variables-de-entorno)
- [🧬 En profundidad](#-en-profundidad)
  - [Uso en profundidad](#uso-en-profundidad)
  - [➡️ Integración con IntelliJ Idea](#️-integración-con-intellij-idea)
  - [➡️ Integración con Eclipse](#️-integración-con-eclipse)
  - [Conclusión](#conclusión)
  - [Referencias](#referencias)

SDKMan es una heramienta que permite instalar y gestionar múltiples versiones de SDKs de diferentes lenguajes de programación, como Java, Groovy, Kotlin, Scala, entre otros.

## ¿Qué es un SDKMAN? <hr>

**SDKMAN!** es una herramienta que nos permite manejar la instalación y configuración de diversas versiones de SDKs (Software Developments Kits) mediante línea de comandos. Inicialmente, fue conocido como GVM (Groovy enVironment Manager) y está inspirado en otras herramientas utilizadas por la comunidad Ruby.

En nuestro día a día como desarrolladores, nos encontramos a veces ante aplicaciones que funcionan y deben compilar en versiones muy diferentes su SDK. Por ejemplo, de Java 1.8, 11, posterior, anterior, etc. También nos ocurre lo mismo con `Maven` y con otros SDKs. 

Cada vez que queremos cambiar de versión, se hace tedioso el tener que buscar, descargar, instalar y configurar nuestro sistema operativo para que utilice esta versión recientemente instalada. Para ello, tenemos a nuestra disposición aplicaciones como SDKMAN!.

### Características de SDKMAN! <hr>

- Centrado en JDKs de la JVM: Java, Groovy, Scala, Kotlin y Ceylon. Ant, Gradle, Grails, Maven, SBT, Spark, Spring Boot, Vert.
- Ligero al ser por lineal de comandos.
- Multiplataforma
- Open Source con licencia Apache 2.0.


### Instalación de SDKMAN! en Windows

En su [web](https://sdkman.io/), nos proporciona una instalación muy sencilla para Linux y Mac, pero en nuestro caso vamos a instalarlo en nuestro Windows 10/11.

La instalación en Windows nos plantea un problema inicial, y es que se realiza con un `script bash`. Para la instalación hemos utilizado la consola de `GitBash` que se nos instaló junto al Git.

```bash
curl -s "https://get.sdkman.io" | bash
```

> 🚧 **Aviso**
> Una vez ejecutamos este comando, nos da un error: no encuentra zip, unzip. Para solventarlo, se puede realizar de dos formas.
> 1. Instalar `zip` y `unzip` dentro de GitBash.
> 2. Modificar el script de instalación.


#### Modificar el script de instalación

1. Descargar el script de instalación.

```bash
curl -s "https://get.sdkman.io" > sdkman.sh
```

2. Modificar el script `sdkman.sh` y comentar el fragmento de código que se indica a continuación.

```bash
#echo "Looking for unzip..."
#if ! command -v unzip > /dev/null; then
#    echo "Not found."
#    echo "======================================================================================================"
#    echo " Please install unzip on your system using your favourite package manager."
#    echo ""
#    echo " Restart after installing unzip."
#    echo "======================================================================================================"
#    echo ""
#    exit 1
#fi

#echo "Looking for zip..."
#if ! command -v zip > /dev/null; then
#    echo "Not found."
#    echo "======================================================================================================"
#    echo " Please install zip on your system using your favourite package manager."
#    echo ""
#    echo " Restart after installing zip."
#    echo "======================================================================================================"
#    echo ""
#    exit 1
#fi
```

Una vez comentado este fragmento de código, podemos instalarlo mediante el comando:

```bash
bash sdkman.sh
```

> 🚧 **Aviso**<br>
> Debes ejecutar el comando desde GitBash, ya que si lo haces desde la consola de Windows, no funcionará.


### Ejemplo de cómo usar SDKMAN!

Una vez tengamos instalado el SDKMAN! mediante nuestra terminal podemos realizar la instalación de distintas versiones de SDKs en nuestro sistema. A continuación, ilustraremos ejemplos de cómo instalar varias versiones de Java.

```bash	
sdk list java
```

Mediante este comando, podemos visualizar un listado de todas las versiones de la JDK de Java que tenemos instaladas, la que tenemos configurada por defecto, las que podemos instalar, etc. Tal y como se muestra en la siguiente imagen:

<img src="https://profile.es/wp-content/media/versiones-jdk-java.jpg.webp">

Para instalar/desinstalar/cambiar uso o cambiar el que usaremos por defecto, utilizaremos el identificador de la columna Identifier. Observamos que actualmente tenemos instalada por defecto la 11.0.12 open de Java.net. Si quisiéramos cambiar a la 8.322.06.1 de Amazon, tendríamos que realizar el siguiente comando:

```bash
$ sdk use java  8.322.06.1-amzn

Using java version 8.322.06.1-amzn in this shell.
```

Tenemos la opción de utilizar para esta consola, por defecto o de manera predeterminada.

Como hemos indicado, todo esto se puede hacer para Java, Kotlin, Groovy, Maven, Scala y un largo etcétera de SDKs que nos proporciona esta herramienta. Seguidamente, se incluye enlaces al portal de SDKMAN! en los que podemos ver todas las JDKs y SDKs que nos proporcionan, así como más ejemplos de uso de los comandos:

- JDKs: https://sdkman.io/jdks
- SDKs: https://sdkman.io/sdks
- Ejemplos de uso: https://sdkman.io/usage

### Configurando nuestro IDE y las variables de entorno

Una vez instalado SDKMAN!. deberemos configurar las variables de entorno de nuestro Windows (si queremos usarlo en consola) o bien la ruta de la SDK de nuestro IDE para que apunte a la carpeta donde se encuentra la versión current seleccionada por SDKMAN!.

```bash	
~/.sdkman/candidates/java/current
```

En este caso, para cada SDK que SDKMAN! tenga instalado, tendremos varias carpetas con las versiones y una carpeta llamada current, donde se encuentra la versión que hayamos configurado como current.

Si utilizamos la ruta a esta current para la variable del entorno de Windows o de nuestro IDE, cada vez que cambiemos por consola la versión current tendremos nuestra consola y nuestros IDEs tirando de la versión que hayamos dictaminado por consola en el SDKMAN!. Esta es la gran ventaja que nos proporciona SDKMAN!: mediante un comando podemos ir saltando de una versión a otra de la SDK de una forma simple y rápida.


## 🧬 En profundidad

En windows esta herramienta solo funciona bajo GitBash, ya que es un script bash. En Linux y MacOS, se puede utilizar en cualquier terminal.

En el script de instalación, instala un directorio oculto en el directorio de usuario llamado `.sdkman` donde se almacenan todas las versiones de los SDKs que instalemos. En este directorio, se almacenan las versiones de los SDKs que instalemos, así como la versión current que tengamos seleccionada.

En `.bashrc` o `.zshrc` se añade una línea que carga el script de SDKMAN! para que esté disponible en todas las terminales que abramos. En Windows, se añade en el `.bashrc` que se encuentra en el directorio de usuario.

```bash
export SDKMAN_DIR="$HOME/.sdkman"
[[ -s "$HOME/.sdkman/bin/sdkman-init.sh" ]] && source "$HOME/.sdkman/bin/sdkman-init.sh"
```
Sin esta linea en el `.bashrc` o `.zshrc`, no podremos utilizar SDKMAN! en la terminal.

**¿Dónde se instalan las versiones de los SDKs?**

En el directorio `~/.sdkman/candidates/java` tendremos todas las versiones de Java que tengamos instaladas, y en la carpeta `current` tendremos la versión que tengamos seleccionada en ese momento.

Current es un enlace simbólico a la versión que tengamos seleccionada. Si cambiamos de versión, el enlace simbólico se cambiará a la versión que hayamos seleccionado.

### Uso en profundidad

Existen varios ámbitos de alcance para las versiones de los SDKs que instalemos. Podemos tener una versión global, una versión por usuario y una versión por proyecto.

- Global: La versión que tengamos seleccionada en ese momento será la que se utilice por defecto en todas las terminales que abramos.
- Terminal: La versión que tengamos seleccionada en ese momento será la que se utilice por defecto en todas las terminales que abramos.
- Proyecto: La versión que tengamos seleccionada en ese momento será la que se utilice por defecto en todas las terminales que abramos.

Para comprobar la versión actual del SDK que aplica sobre nuestra terminal, utilizaremos el comando `sdk current java`. Con este comando, podremos ver la versión que se está utilizando en ese momento.

```bash
$ sdk current java
# podemos comprobar cualquier SDK
$ sdk current maven
```

Para comprobar qué es lo que está actualmente en uso para todos los SDKs, utilizaremos el comando `sdk current`. Con este comando, podremos ver la versión que se está utilizando en ese momento para todos los SDKs.

```bash
$ sdk current

Using:
groovy: 4.0.18
java: 21.0.2-tem
scala: 3.3.1
```

▶️ **Cambiar la versión global**

Para cambiar la versión global, utilizaremos el comando `sdk default java 11.0.12-open`. Con este comando, la versión 11.0.12-open será la que se utilice por defecto en todas las terminales que abramos.
Además también cambiará el enlace simbólico current a la versión 11.0.12-open.

```bash	
sdk default java 11.0.12-open
```

▶️ **Cambiar la versión por terminal**

Para cambiar la versión por terminal, utilizaremos el comando `sdk use java 11.0.12-open`. Con este comando, la versión 11.0.12-open será la que se utilice por defecto mientras el terminal esté abierto.

▶️ **Cambiar la versión por proyecto**

A veces es importante que un proyecto utilice una versión concreta de un SDK. Los propios IDEs almacenan esta configuracion en un archivo de configuración del proyecto, eclip se llama `.project` y en IntelliJ se llama `.idea`.

Pero a veces es neceario cambiar la versión de un SDK en un proyecto sin tener que abrir el IDE, ya que necesitamos compilar o ejecutar algo desde la terminal.

Para esto, SDKMAN! nos proporciona una herramienta que nos permite cambiar la versión de un SDK en un proyecto sin tener que abrir el IDE.

  1. Inicializar el proyecto con la versión que queramos.

    ```bash
    # Dentro de la carpeta del proyecto, ejecutamos el siguiente comando.
    # Crea un fichero .sdkmanrc con la versión que actualmente esté activa sobre la terminal.
    sdk env init
    ``` 
  2. Si queremos que se auto-active esta versión al acceder a la carpeta del proyecto, tenemos que activar en la configuración de SDKMAN, `sdkman_auto_env=true`

  3. Para que se aplique este cambio en la configuración será necesario cerrar la terminal y volver a abrirla.

Ahora cada vez que accedamos a la carpeta del proyecto, la versión que esté seleccionada en el fichero `.sdkmanrc` será la que se utilice por defecto en ese proyecto.


### ➡️ Integración con IntelliJ Idea

**Configuración Manual**

Para configurar la versión de un SDK en un proyecto de IntelliJ Idea, tendremos que ir a `File -> Project Structure -> Project Settings -> Project -> Project SDK` y seleccionar la versión que queramos.

Podemos elegir la versión de las disponibles en el sistema, o bien, si tenemos SDKMAN! instalado, podremos seleccionar la versión que queramos.

La ruta donde se encuentra las versiones instaladas por SDKMAN! es `~/.sdkman/candidates/java/`


**Configuración Automática**

Si tenemos configurado el fichero `.sdkmanrc` en la carpeta del proyecto, al abrir el proyecto, IntelliJ Idea detectará que hay un fichero `.sdkmanrc` y seleccionará la versión que esté en ese fichero.

> 💡 **Nota**<br>
> Esta opción solo está disponible a partir de la versión 2023 de IntelliJ Idea.


### ➡️ Integración con Eclipse

Para configurar la versión de un SDK en un proyecto de Eclipse, tendremos que ir a `Window -> Preferences -> Java -> Installed JREs` y seleccionar la versión que queramos.

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/53eca6f1-451a-4a99-a7b6-7f0d08efccec" width="600px">

Además podemos las ubicaciones disponibles de donde están instaladas las versiones de Java, a través del menú `Add -> Standard VM` y seleccionar la ruta donde se encuentre la versión de Java que queramos.	

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/97685080-6c1b-4910-b60d-517a5488eb8d" width="400px">

Y buscamos el directorio donde está ubicado, le indicamos un nombre, esperamos unos pocos segundos a que Eclipse otenga las librerias, y Finalizar.

La nuevamente añadida JRE es mostrada en la lista.

<img src="https://github.com/jssfpciclos/DAW_eedd/assets/72703706/1d8e22c3-ade8-4722-a55f-f1c5789b1198" width="400px">


### Conclusión

En este artículo hemos diseccionado SDKMAN!, una poderosa herramienta para instalar y configurar diversas versiones de SDKs mediante línea de comandos. Así, hemos visto en qué consiste, sus características principales, cómo instalarla y un ejemplo de uso de cómo instalar varias versiones de Java con ella.



### Referencias

- [Web SDKMAN!](https://sdkman.io/)
- [Uso de SDKMAN!](https://sdkman.io/usage)