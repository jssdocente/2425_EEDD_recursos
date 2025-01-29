# JAVA_HOME variable de entorno

JAVA_HOME es una variable de entorno que se utiliza para indicar la ruta de instalación del JDK (Java Development Kit) o JRE (Java Runtime Enviroment). Esta variable se utiliza para que las aplicaciones que necesiten utilizar el JDK/JRE sepan dónde está instalado.

Apunta a la carpeta raíz del JDK o JRE, no a la carpeta bin o lib.

Esta variable debe ser configurada sobre todos los sistemas operativos que tengan una instalación de Java, incluidos Windows, Linux y macOS.

La variables JAVA_HOME no es utilizada por Java, sino por otras aplicaciones que necesiten saber dónde está instalado el JDK/JRE.

Cuando un programa va a iniciarse, lo primero que hace es buscar donde está instalado el JDK/JRE, y una vez encontrado, puede utilizar las herramientas que se encuentran en la carpeta bin.

## Configuración de JAVA_HOME en Windows

Se puede realizar la configuración de JAVA_HOME en Windows de dos formas:

- Configuración de JAVA_HOME mediante la interfaz gráfica.
- Configuración de JAVA_HOME mediante la línea de comandos.

### Configuración de JAVA_HOME mediante la interfaz gráfica

Esta configuración depende de la versión de Windows que se esté utilizando, ya que la ruta de acceso a donde está incluida esta configuración puede variar.

La opción más fácil es desde el botón de inicio, buscar "Variables de entorno" y seleccionar "Editar las variables de entorno del sistema".

Exiten 2 tipos de ámbitos de variables de entorno:

- **Variables de entorno del sistema**: Son accesibles y aplica a todos los usuarios del sistema.
- **Variables de entorno del usuario**: Solo aplica y son accesibles al usuario que las ha creado.


Una variable de entorno es igual a una variable en un lenguaje de programación, su misión es almacenar un valor.


### Configuración de JAVA_HOME mediante la línea de comandos

Para configurar JAVA_HOME mediante la línea de comandos, se debe abrir una terminal y ejecutar el siguiente comando:

```powershell
setx JAVA_HOME "C:\Program Files\Java\jdk1.8.0_281"
```

Para ver todas las variables de entorno, se puede ejecutar el siguiente comando:

```powershell
set
```

Para ver solo el valor de una variable, simplemente incluye el nombre entre dos signos de porcentaje:

```powershell
echo %JAVA_HOME%
```


## Configuración de JAVA_HOME en Linux

Para configurar JAVA_HOME en Linux, se debe editar el archivo `.bashrc` o `.bash_profile`, o `zshrc` dependiendo del shell predeterminado, y que se encuentra en el directorio del usuario.

Para cambiar el valor de una variable de entorno, se debe utilizar el comando `export` seguido del nombre de la variable y el valor que se le quiere asignar.

```bash
export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64
```

Para que los cambios surtan efecto, se debe ejecutar el siguiente comando:

```bash
# Recargar el archivo .bashrc
source ~/.bashrc # o el archivo que corresponda según el shell que se esté utilizando.
```

## JAVA_HOME vs JRE_HOME

JAVA_HOME y JRE_HOME son variables de entorno que se utilizan para indicar la ruta de instalación del JDK y JRE respectivamente.

Algunas aplicaciones requieren solo JRE para funcionar, mientras que otros requiren un JDK completo.

## JAVA_HOME vs PATH variable

Además de configurar la variable de entorno JAVA_HOME, también es necesario configurar la variable de entorno PATH.

La variable de entorno PATH se utiliza para indicar al sistema operativo dónde buscar los ejecutables de las aplicaciones.

> 💡 **Importante**
> En la variable PATH se incluye la ruta de acceso a la carpeta `bin` del JDK/JRE, no la ruta de acceso a la carpeta raíz.

Si un programa no puede localizar la variable JAVA_HOME, puede aún ser capaz de acceder a las herramientas de Java a través del PATH.


## Errores comunes con JAVA_HOME

- **JAVA_HOME no está configurado**: Si la variable de entorno JAVA_HOME no está configurada, es posible que algunas aplicaciones no funcionen correctamente.
- **JAVA_HOME no apunta a la carpeta correcta**: Si la variable de entorno JAVA_HOME apunta a una carpeta incorrecta, es posible que algunas aplicaciones no funcionen correctamente.
- **JAVA_HOME no está en el PATH**: Si la variable de entorno JAVA_HOME no está en el PATH, es posible que algunas aplicaciones no funcionen correctamente.






