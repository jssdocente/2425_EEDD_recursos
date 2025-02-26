# 02. Práctica: Trabajo con dependencias externas

## Objetivos de la práctica

1. Configurar un proyecto en IntelliJ IDEA sin gestor de dependencias (sin Maven/Gradle).
2. Descargar y enlazar manualmente la librería Joda Money.
3. Crear una clase para gestionar conversiones entre diferentes monedas.
4. Implementar un programa de prueba que use la funcionalidad de la librería externa.

## Entrega

- El proyecto se almacenará dentro de tu repositorio oficial de alumno, en la carpeta `UT3\EC\02`.
- Se entregará en Moodle, indicando en enlace al directorio en vuestro repositorio.


## **Requisitos Previos**

- Tener instalado IntelliJ IDEA.
- Tener configurado Java en el entorno de desarrollo.


## **Pasos a seguir**

El objetivo de esta práctica será una aplicación de conversión de divisas utilizando la librería `Joda Money`, que permite manejar valores monetarios con precisión.

Siguiendo con la práctica anterior, somos trabajadores de la emrpesa `softmar.com` y queremos desarrollar un nuevo programa llamada `MoneyConvert` que permitirá la conversión entre diferentes divisas.

EL paquete base del proyecto es `com.softmar.MoneyConvert`.

### **1. Creación del Proyecto**

1. Abre IntelliJ IDEA y selecciona **Nuevo Proyecto**.
2. Elige **Java** como tipo de proyecto.
3. Asigna el nombre `MoneyConvert` y guarda en la ubicación `<carpeta-repositorio\UT3\EC\02\`
4. Crea un fichero .gitignore (para solo subir a git ficheros necesario.)
5. Con la herramienta online `https://www.toptal.com/developers/gitignore`, genera el contenido del fichero, indicando las palabras clave `Java Intellj`.
6. Copia el contenido generado en la herramienta, al fichero .gitignore del proyecto.
7. Crea un fichero `readme.md` en la raíz del proyecto, y copia esta documentación.


### **2. Descargar la librería Joda Money**

1. Visita la página `https://www.joda.org/joda-money/` y descarga la versión `v2.0.0`, el fichero `joda-money-2.0.0.jar`.
2. Crea una carpeta dentro del proyecto, llamada `libs` (librerias).

### **3. Configurar la librería en IntelliJ**

1. Abre el proyecto en IntelliJ IDEA.
2. Ir a `File > Project Structure > Modules > Dependencies`.
3. Click en botón `+ > JARs or directories…` y seleccionen el archivo `joda-money-1.0.3.jar`.


### **4. Crear clases**

1. Crea la clase `CurrencyConverter.java` dentro del paquete `com.softmar.MoneyConvert`.
   
```java
package com.softmar.MoneyConvert;

public class CurrencyConverter {
    public static Money convert(Money amount, CurrencyUnit targetCurrency, double rate) {
        double convertedAmount = amount.getAmount().doubleValue() * rate;
        return Money.of(targetCurrency, convertedAmount);
    }
}
```
2. Realize las importaciones necesarias.
3. Dentro de la clase Main, incluye el siguiente código.
   ```java
    public static void main(String[] args) {
        // Definir cantidades en diferentes monedas
        Money usdAmount = Money.of(CurrencyUnit.USD, 100);
        CurrencyUnit eur = CurrencyUnit.EUR;

        // Tipo de cambio ficticio (1 USD = 0.85 EUR)
        double exchangeRate = 0.85;

        // Realizar conversión
        Money eurAmount = CurrencyConverter.convert(usdAmount, eur, exchangeRate);

        // Mostrar resultado
        System.out.println(usdAmount + " equivale a " + eurAmount);
    }
   ``` 
4. Ejecute el código para comprobar el funcionamiento.
5. Si no funciona, aplica los cambios que considres oportunos según la información de los mensajes de error.

---


## 2ª Parte. Nuevas funcionalidades

**Objetivo:**

Investigar la documentación de Joda Money y aplicar sus clases para realizar operaciones monetarias adicionales.

**Instrucciones:**

1. Consultar la documentación

   - Accede a la documentación de Joda Money en Joda Money Docs.
   - Busca información sobre la clase Money y otras clases relacionadas.

2. Ampliar el programa actual

   - Agrega una funcionalidad que permita sumar y restar cantidades en la misma moneda.
   - Implementa una funcionalidad que compare dos valores monetarios e indique cuál es mayor.

3. Requisitos del código:

   - Crear un método addMoney(Money m1, Money m2) que devuelva la suma de dos cantidades en la misma moneda.
   - Crear un método subtractMoney(Money m1, Money m2) que reste dos cantidades en la misma moneda.
   - Crear un método compareAmounts(Money m1, Money m2) que indique cuál cantidad es mayor o si son iguales.
  
4. Crea una clase dentro del paqute principal `PruebaA`, con una función main (para probar el código), definiendo lo siguiente:
   
   - Definir 2 variblaes usd1 de moneda USD de valor 100 y otra, usd2 de valor 50.
   - Definir un variable tipo `CurrencyUnit`, nombre `eur` y valor `CurrencyUnit.EUR`.
   - Define un tipo de cambio ficticio (1 USD = 0.85 EUR). `double exchangeRate = 0.85`.
   - Realiza la conversión `usd1 a eur` y almacena en variable `eurAmount`.
   - Muestra los resultados `100 USD equivale a XX Eur`.
   - Suma `usd1 a usd2` y muestra el resultado de la suma.
   - Resta `usd1 a usd2` y muestra el resultado de la resta. 
   - Compara `usd1 a usd2` y muestra el resultado de la comparación.
  
    Ejemplos de la salida.
    ```makefile
    Conversión: USD 100 equivale a EUR 85.
    Suma: USD 150.00  
    Resta: USD 50.00  
    Comparación: USD 100.00 es mayor que USD 50.00  
    ```

🔍 Pistas:

   - Métodos útiles: plus(), minus(), isGreaterThan(), isLessThan(), isEqual().
   - Revisen las clases en la documentación antes de escribir el código.


## 3ª Parte. Gestión de Precios con Descuentos

**Objetivos**

Utilizar la librería Joda Money para gestionar precios de productos y aplicar descuentos de forma dinámica.

**Instrucciones:**

1. Consultar la documentación

   - Accede a la documentación de Joda Money en Joda Money Docs.
   - Busca información sobre la clase Money y otras clases relacionadas.

**Implementar la funcionalidad**

1. Crea una clase Product con los atributos, `String name y Money price`
2. Implementa un método applyDiscount(Money price, double percentage) que devuelva un nuevo precio con el descuento aplicado.
3. Crea una clase ShoppingCart que permita agregar productos y calcular el total antes y después del descuento.

**Requisitos del código:**

Crea una clase PruebaShoppingCard, con una función main (para probar el código), definiendo lo siguiente:

- Instanciar al menos tres productos con diferentes precios.
- Aplicar un descuento del 10% a un producto y del 20% a otro.
- Mostrar en consola el precio original y el precio final después del descuento.
- Calcular el total de la compra con y sin descuentos.

```yaml
Producto: Laptop - Precio Original: USD 1200.00 - Precio con descuento (10%): USD 1080.00  
Producto: Smartphone - Precio Original: USD 800.00 - Precio con descuento (20%): USD 640.00  
Producto: Auriculares - Precio Original: USD 150.00 - Sin descuento aplicado.  

Total sin descuento: USD 2150.00  
Total con descuentos aplicados: USD 1870.00  
```

🔍 Pistas:

  - Métodos útiles: `multipliedBy(), minus(), plus()`.
  - Pueden almacenar los productos en una `List<Product>` dentro de ShoppingCart.


---