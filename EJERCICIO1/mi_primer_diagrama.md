MI PRIMER DIAGRAMA DE CLASES
===

```mermaid
classDiagram
    PERSONA <|-- EMPLEADOS
    EMPLEADOS <|-- DIRECTIVOS
    DIRECTIVOS"0..*" -- "0..* SUBORDINADOS" EMPLEADOS
    PERSONA <|-- CLIENTES
    EMPRESAS "1..*" *-- "0..* CLIENTES" CLIENTES
    EMPRESAS "1" *-- "1..* EMPLEADOS" EMPLEADOS
    class EMPRESAS{
        * nombre
    }

    class EMPLEADOS{
        + salario_bruto
        + calcular_salario_neto()
        + mostrar()
    }

    class CLIENTES{
        + telefono_de_contacto
        + mostrar()
    }

    class DIRECTIVOS {
        + categoria
        + mostrar()
    }

    class PERSONA{
        + edad
        + nombre
        + mostrar()
    }
