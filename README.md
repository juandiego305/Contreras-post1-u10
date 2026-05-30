# Productos Service

Análisis SonarQube

## Estado inicial del análisis

| Categoría | Cantidad | Rating |
| :--- | :--- | :--- |
| Bugs | X | ? |
| Vulnerabilidades | X | ? |
| Code Smells | X | ? |
| Cobertura | 0.0% | - |

## Hallazgos principales identificados

### Bug 1: Retorno Null sin Optional
* **Archivo:** `ProductoService.java`, línea 43
* **Descripción:** El método `buscar` devuelve un `null` directamente (`orElse(null)`), lo que puede causar un `NullPointerException` en las capas superiores.
* **Severidad:** Major

### Code Smell 1: Método demasiado complejo (Cognitive Complexity)
* **Archivo:** `ProductoService.java`, línea 16
* **Descripción:** El método `procesarProducto` tiene múltiples responsabilidades, demasiados parámetros y una alta complejidad ciclomática debido a la estructura de bloques `if/else`.

### Code Smell 2: Uso de Inyección por Campo
* **Archivo:** `ProductoService.java`, línea 12
* **Descripción:** Se utiliza la anotación `@Autowired` directamente sobre el campo `repo`, lo que dificulta las pruebas unitarias y viola el principio de inyección de dependencias por constructor.


