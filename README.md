# proyecto-copilot
Proyecto de prueba para Estructura de Datos 2

Blog Técnico: Tablas Hash
Introducción
Colisiones
Implementación
Post #1: Introducción a las Tablas Hash
Una
Tabla Hash
es una estructura de datos que almacena pares clave–valor y permite realizar operacionesde inserción, búsqueda y eliminación en tiempo promedio
O(1)
.
Conceptos clave
Clave (key):
Identificador del dato.
Valor (value):
Información asociada.
Función hash:
Convierte una clave en un índice numérico.
Índice:
Posición dentro del arreglo.
Colisiones:
Cuando dos claves generan el mismo índice.
Ejemplo simple
key = "Juan" → hash("Juan") = 4 → Se almacena en índice 4
Post #2: Manejo de Colisiones
Las colisiones ocurren cuando dos claves producen el mismo índice. Existen dos métodos principales paramanejarlas:
1. Encadenamiento (Chaining)
Cada posición de la tabla almacena una lista enlazada.
Permite crecimiento dinámico.
tabla[3] → [ ("Ana", 21) → ("Luis", 9) ]
2. Direccionamiento Abierto (Open Addressing)
Linear Probing:
Buscar el siguiente espacio libre.
Quadratic Probing:
Saltos crecientes.
Double Hashing:
Se usa una segunda función hash.
índice 5 ocupado → probar 6 → ocupado → probar 7 → libre
Post #3: Implementación y Operaciones
Insertar (put)
Se calcula el hash, se obtiene el índice y se almacena la clave–valor.
tabla.put("Carro", 120)
Buscar (get)
Permite obtener un valor usando la clave.
tabla.get("Carro") → 120
Eliminar (delete)
Depende del método de manejo de colisiones:
Chaining:
se elimina un nodo de la lista.
Open addressing:
se marca la celda como
deleted
.
tabla.delete("Carro")
Ejemplos Prácticos
Ejemplo 1: Cálculo de Hash
key = "Gato"
hash("Gato") = 7
→ índice 7 en la tabla
Ejemplo 2: Encadenamiento
tabla[2] → [ ("Rojo", 10) → ("Azul", 15) → ("Verde", 22) ]
Ejemplo 3: Linear Probing
índice calculado = 4
tabla[4] ocupado → probar 5
tabla[5] libre → insertar
Ejemplo 4: Operaciones completas
tabla.put("Perro", 8)
tabla.put("Gato", 6)
tabla.put("Pez", 3)
tabla.get("Gato") → 6
tabla.delete("Perro") → eliminado
Consideraciones Finales
Las tablas hash son fundamentales en informática por su eficiencia. La elección del método de manejo decolisiones y la función hash adecuada son cruciales para un rendimiento óptimo.
