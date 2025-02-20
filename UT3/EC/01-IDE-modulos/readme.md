# Práctica Guiada: Organización de Proyectos y Módulos en IntelliJ IDEA

## **Objetivo**
En esta práctica aprenderás a organizar un proyecto en IntelliJ IDEA utilizando módulos. Simularemos que somos una empresa llamada **Softmar.com**, y este proyecto forma parte de nuestros desarrollos internos. Por ello, el nombre del paquete debe reflejar la estructura empresarial utilizando el prefijo `com.softmar`.


## **Requisitos Previos**
- Tener instalado IntelliJ IDEA.
- Tener configurado Java en el entorno de desarrollo.
- Tener instalada una herramienta para convertir `.jar` en `.exe` (Launch4j o Inno Setup).

## **Pasos a seguir**

Estamos simulandi que somos los desarrolladores de una empresa llamada `softmar` y que tiene dominio `softmar.com`. Todos sus productos tienen que tener este nombre de paquete, pero como en los proyetos de Java, se tiene que invertir el nombre, ya que primero es el dominio `.com` y despues el resto.
Este software se llama `nexus`, por tanto el paquete base se llamará `com.softmar.nexus`.

Este proyecto utilizará la versión, 

### **1. Creación del Proyecto y Módulos**
1. Abre IntelliJ IDEA y selecciona **Nuevo Proyecto**.
2. Elige **Java** como tipo de proyecto.
3. Asigna el nombre `Nexus` y guarda en la ubicación `<tu-carpeta-modulo>\EC\01\`
4. Una vez creado el proyecto, ve a **File > Project Structure**.
5. En la sección **Modules**, agrega dos nuevos módulos:
   - `Modulo1`
   - `Modulo2`
6. Asegúrate de que cada módulo tenga su propio `src` para almacenar código.

### **2. Vincular los Módulos al Proyecto Nexus**
1. Abre **File > Project Structure** y selecciona `Nexus` en la sección **Modules**.
2. Ve a la pestaña **Dependencies** y haz clic en **+ > Module Dependency**.
3. Agrega `Modulo1` y `Modulo2` como dependencias del proyecto `Nexus`.
4. Aplica los cambios y cierra la configuración.

### **3. Creación de Clases**

#### **En `Modulo1` (paquete `com.softmar.nexus.modulo1`)**
Crea una clase `Saludo` que tenga un método para devolver un saludo. Al crear la clase, además del nomre de la clase, pon el nombre del paquete, de esta forma `com.software.nexus.modulo1.Saludo`.

```java
package com.softmar.nexus.modulo1;

public class Saludo {
    public String obtenerSaludo() {
        return "Hola desde Modulo1!";
    }
}
```

#### **En `Modulo2` (paquete `com.softmar.nexus.modulo2`)**
Crea una clase `Operacion` que realice una suma.

```java
package com.softmar.nexus.modulo2;

public class Operacion {
    public int sumar(int a, int b) {
        return a + b;
    }
}
```

#### **En proyecto `Nexus` (paquete `com.softmar.nexus`)**
Crea una clase `Main` que utilice las clases de los módulos.

```java
package com.softmar.nexus;

import com.softmar.nexus.modulo1.Saludo;
import com.softmar.nexus.modulo2.Operacion;

public class Main {
    public static void main(String[] args) {
        Saludo saludo = new Saludo();
        Operacion operacion = new Operacion();

        System.out.println(saludo.obtenerSaludo());
        System.out.println("Resultado de la suma: " + operacion.sumar(5, 3));
    }
}
```

### **Verificación**
- Asegúrate de que el `Nexus` pueda ejecutar la clase `Main` sin errores.
- Verifica que las clases de los módulos se importen y usen correctamente.
- Comprueba que el resultado en consola muestre el saludo y el resultado de la suma correctamente.

---


## 2ª Parte. Creación de un ejecutable

## Recursos

- [IntelljIDEA Artifacts](https://www.jetbrains.com/help/idea/working-with-artifacts.html#build_artifacts)

**Pasos a seguir**

### **1. Generar el Archivo Ejecutable `.jar`**
1. Abre **File > Project Structure** y click sobre "+" para crear un nuevo "Artefacto".
2. Del menu desplegable, seleccione "Platform Specific Package", y "From Module".
3. Elige el módulo "Nexus".
4. En el nombre del artefacto indica "nexusApp".
5. En la pestaña "Packaging", seleccionamos la clase "com.softmar.nexus.Main", dando al icono de la carpeta.
6. Indicamos la versión 1.0.
7. En vendor indiamos com.softmar.
8. El resto de opciones las dejamos por defecto.

### **2. Build Artifact**

1. En el menú Build > Build artefacts.
2. Este proceso generará dentro de la carpeta "out/artifacts/nexus" el fichero ejecutable.
3. Ejecutar el fichero.



---

Con esta práctica, los alumnos aprenderán a generar y distribuir ejecutables de sus aplicaciones Java en un entorno Windows sin depender de Java directamente.

