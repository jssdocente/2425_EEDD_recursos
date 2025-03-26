# Ejercicio 3.5 - Usar librería Maven desplegada en repositorio hosted

El objetivo de este ejercicio es usar la librería Maven desplegada en el servidor Maven hosted, creada por un compañero.



### Entrega

Guarda este proyecto en tu repositorio de Github, dentro de la carpeta `TE\3.5`, con el nombre `Uso-UtilidadesMaven`. Será un proyecto basado en Maven.

Copia este documento en el `README.md` del proyecto. Crea también uan carpeta llamada `_res/img` y guarda las capturas de pantalla que se solicitan en este documento. 

### Enunciado

Crea un proyecto Maven con las siguientes características:

1. **`groupId`**: `com.{apellido1}.{nombre}`.
2. **`artifactId`**: `Uso-UtilidadesMaven`.
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
