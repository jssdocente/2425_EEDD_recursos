# Tarea evaluable 4.4. Unit Testing con JUnit 5. 

En esta tarea evaluable se van a realizar una serie de ejercicios para practicar el uso de JUnit 5. Para su realización se recomienda seguir los siguientes pasos:

- Todos los ejercicios se entregan dentro de un proyecto de IntelliJ.
- El proyecto debe ser gestionado por Maven.
- Copiar este fichero `readme.md` en la raiz del proyecto.
- Nombre del proyecto: `ProyectoBanco`.
- Paquete raiz del proyecto: `com.{apellido1.nombre}.ProyectoBanco`.

### Entrega

- El proyecto debe crearse dentro de la ruta `UT4/TE4.5/` de vuestro repositorio.
- Copiar el enlace a la carpeta `UT4/TE4.5/` y pegar en el formulario de entrega de la tarea evaluable.


### Recursos

- [JUnit 5 User Guide](https://junit.org/junit5/docs/current/user-guide/)
- [Curso de JUnit 5](https://www.youtube.com/playlist?list=PLTd5ehIj0goPcVH3xhSudzyazW8CtMvsq)
- [Maven in 5 Minutes](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)


### Enuncionado

El proyecto `TE4.5\ProyectoBanco` contiene una serie de clases que implementan un sistema bancario. El objetivo de esta tarea es realizar pruebas unitarias sobre el código existente utilizando JUnit 5.

Condiciones:

- Una cuenta bancaria tiene un saldo inicial de 0 euros, pertenece a un cliente y tiene un número de cuenta único.
  - Una cuenta puede estar inactiva o activa.
  - Una cuenta no puede tener un saldo negativo.
  - Tiene un método "agregarImporte" que permite agregar dinero a la cuenta. No se permiten importes negativos.
  - Tiene un método "retirarImporte" que permite retirar dinero de la cuenta. No se puede retirar más dinero del que hay en la cuenta ni importes negativos.
- Un cliente tiene un nombre y un identificador válidos.
  - Un cliente no puede tener más de una cuenta bancaria en el mismo banco.
- Un banco tiene un nombre
  - Tendrá un listado de cuentas, cada una con su saldo y su cliente.
  - Podrá realizar una transferencia entre cuentas, siempre que ambas cuentas pertenezcan al mismo banco, y el saldo de la cuenta origen sea suficiente para realizar la transferencia.


Las clases son las siguientes:

**Cliente**

```	java
public class Cliente {
    private final String nombre;
    private final String nif;

    public Cliente(String nombre, String nif) {
        this.nombre = nombre;
        this.nif = nif;
    }

    public String getNombre() {
        return nombre;
    }

    public String getNif() {
        return nif;
    }

    @Override
    public boolean equals(Object obj) {
        if (this == obj) return true;
        if (!(obj instanceof Cliente other)) return false;
        return nif.equals(other.nif);
    }

    @Override
    public int hashCode() {
        return nif.hashCode();
    }
}
```

**Cuenta**

```java
public class Cuenta {
    private final Cliente titular;
    private final String numeroCuenta;
    private double saldo;
    private boolean activa;

    public Cuenta(Cliente titular, String numeroCuenta) {
        this.titular = titular;
        this.numeroCuenta = numeroCuenta;
        this.saldo = 0.0;
        this.activa = true;
    }

    public Cliente getTitular() {
        return titular;
    }

    public String getNumeroCuenta() {
        return numeroCuenta;
    }

    public double getSaldo() {
        return saldo;
    }

    public boolean estaActiva() {
        return activa;
    }

    public void agregarImporte(double importe) {
        if (!activa) throw new IllegalStateException("Cuenta inactiva");
        if (importe < 0) throw new IllegalArgumentException("Importe negativo");
        saldo += importe;
    }

    public void retirarImporte(double importe) {
        if (!activa) throw new IllegalStateException("Cuenta inactiva");
        if (importe < 0 || importe > saldo) throw new IllegalArgumentException("Importe inválido");
        saldo -= importe;
    }

    public void cerrar() {
        if (saldo != 0) throw new IllegalStateException("No se puede cerrar la cuenta con saldo diferente de 0");
        activa = false;
    }
}

```

**Banco**

```java
import java.util.*;

public class Banco {
    private final String nombre;
    private final Map<String, Cuenta> cuentas = new HashMap<>();
    private final Map<String, String> clientesACuentas = new HashMap<>();
    private int contadorCuenta = 1000;

    public Banco(String nombre) {
        this.nombre = nombre;
    }

    public Cuenta abrirCuenta(Cliente cliente) {
        if (clientesACuentas.containsKey(cliente.getNif())) {
            throw new IllegalArgumentException("El cliente ya tiene una cuenta");
        }

        String numeroCuenta = generarNumeroCuenta();
        Cuenta cuenta = new Cuenta(cliente, numeroCuenta);
        cuentas.put(numeroCuenta, cuenta);
        clientesACuentas.put(cliente.getNif(), numeroCuenta);
        return cuenta;
    }

    public void cerrarCuenta(String numeroCuenta) {
        Cuenta cuenta = obtenerCuenta(numeroCuenta);
        cuenta.cerrar();
        cuentas.remove(numeroCuenta);
        clientesACuentas.remove(cuenta.getTitular().getNif());
    }

    public void transferir(String origen, String destino, double importe) {
        Cuenta cuentaOrigen = obtenerCuenta(origen);
        Cuenta cuentaDestino = obtenerCuenta(destino);

        if (cuentaOrigen.getTitular().equals(cuentaDestino.getTitular())) {
            throw new IllegalArgumentException("El titular de origen y destino no puede ser el mismo");
        }

        cuentaOrigen.retirarImporte(importe);
        cuentaDestino.agregarImporte(importe);
    }

    public Cuenta obtenerCuenta(String numeroCuenta) {
        Cuenta cuenta = cuentas.get(numeroCuenta);
        if (cuenta == null) throw new NoSuchElementException("Cuenta no encontrada");
        return cuenta;
    }
}
```

**Realizar los siguientes test:**

1. CuentaTest.java
   - agregarImporte suma correctamente saldo.
   - agregarImporte con cuenta inactiva lanza excepción.
   - agregarImporte con valor negativo lanza excepción.
   - retirarImporte resta correctamente saldo.
   - retirarImporte con cuenta inactiva lanza excepción.
   - retirarImporte con importe negativo lanza excepción.
   - retirarImporte con importe mayor al saldo lanza excepción.
   - cerrar() con saldo 0 cambia el estado de la cuenta a inactiva.
   - cerrar() con saldo distinto de 0 lanza excepción.

2. BancoTest.java
    - abrirCuenta: para mismo cliente lanza excepción.
    - cerrarCuenta: pone la cuenta inactiva.
    - cerrarCuenta: con saldo lanza excepción.
    - obtenerCuenta: devuelve cuenta correcta.
    - obtenerCuenta con número inválido lanza excepción.
    - transferir:
      - titulares iguales lanza excepción.
      - si alguna cuenta está inactiva, lanza excepción.
      - saldo de la cuenta de origen y cuenta de destino son correctos despues de la transferencia.



Después de crear los test, se debe conseguir una cobertura del 100% en todos los tipos de cobertura.

| Clases | Cobertura clase | Cobertura métodos | Cobertura líneas | Cobertura ramas |
|--------|-----------------|-------------------|------------------|-----------------|
| Cliente | 100%             | 100%               | 100%              | 100%             |
| Cuenta  | 100%             | 100%               | 100%              | 100%             |
| Banco   | 100%             | 100%               | 100%              | 100%             |


> Si no se consigue la cobertura del 100% en todos los tipos de cobertura, se debe añadir nuevos test para conseguirlo.


> 🧲 Adjunta una imagen donde se visualize la cobertura de los test.


> 🧲  Adjuntar un GIF donde se visualize que el resultado de pasar los test y se muestre la cobertura de código resultante.

