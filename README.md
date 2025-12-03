# proyecto-copilot
Proyecto de prueba para Estructura de Datos 2
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Blog Técnico – Tablas Hash</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #f4f4f4;
    }
    header {
      background: #00acc1;
      padding: 20px;
      color: white;
      text-align: center;
    }
    nav a {
      margin: 0 10px;
      color: white;
      text-decoration: none;
      font-weight: bold;
    }
    .container {
      max-width: 900px;
      margin: auto;
      padding: 20px;
      background: white;
    }
    h2 {
      color: #006064;
    }
    .code-box {
      background: #eceff1;
      padding: 10px;
      border-radius: 5px;
      font-family: Consolas;
    }
  </style>
</head>
<body>
  <header style="text-align:center;">
    
    <h1>Blog Técnico: Tablas Hash</h1>
    <nav>
      <a href="#post1">Introducción</a>
      <a href="#post2">Colisiones</a>
      <a href="#post3">Implementación</a>
    </nav>
  </header>

<!-- Imagen debajo de la cabecera -->
<div style="text-align:center; margin:15px 0;">
  
</div>

  <div class="container">

    <!-- POST 1 -->
    <section id="post1">
      <h2>Post #1: Introducción a las Tablas Hash</h2>
      <p>Una <strong>Tabla Hash</strong> es una estructura de datos que almacena pares clave–valor y permite realizar operaciones de inserción, búsqueda y eliminación en tiempo promedio <strong>O(1)</strong>.</p>

      <h3>Conceptos clave</h3>
      <ul>
        <li><strong>Clave (key):</strong> Identificador del dato.</li>
        <li><strong>Valor (value):</strong> Información asociada.</li>
        <li><strong>Función hash:</strong> Convierte una clave en un índice numérico.</li>
        <li><strong>Índice:</strong> Posición dentro del arreglo.</li>
        <li><strong>Colisiones:</strong> Cuando dos claves generan el mismo índice.</li>
      </ul>

      <h3>Ejemplo simple</h3>
      <div class="code-box">
        key = "Juan" → hash("Juan") = 4 → Se almacena en índice 4
      </div>
    </section>

    <hr />

    <!-- POST 2 -->
    <section id="post2">
      <h2>Post #2: Manejo de Colisiones</h2>
      <p>Las colisiones ocurren cuando dos claves producen el mismo índice. Existen dos métodos principales para manejarlas:</p>

      <h3>1. Encadenamiento (Chaining)</h3>
      <ul>
        <li>Cada posición de la tabla almacena una lista enlazada.</li>
        <li>Permite crecimiento dinámico.</li>
      </ul>

      <div class="code-box">
        tabla[3] → [ ("Ana", 21) → ("Luis", 9) ]
      </div>

      <h3>2. Direccionamiento Abierto (Open Addressing)</h3>
      <ul>
        <li><strong>Linear Probing:</strong> Buscar el siguiente espacio libre.</li>
        <li><strong>Quadratic Probing:</strong> Saltos crecientes.</li>
        <li><strong>Double Hashing:</strong> Se usa una segunda función hash.</li>
      </ul>

      <div class="code-box">
        índice 5 ocupado → probar 6 → ocupado → probar 7 → libre
      </div>
    </section>

    <hr />

    <!-- POST 3 -->
    <section id="post3">
      <h2>Post #3: Implementación y Operaciones</h2>

      <h3>Insertar (put)</h3>
      <p>Se calcula el hash, se obtiene el índice y se almacena la clave–valor.</p>

      <div class="code-box">
        tabla.put("Carro", 120)
      </div>

      <h3>Buscar (get)</h3>
      <p>Permite obtener un valor usando la clave.</p>

      <div class="code-box">
        tabla.get("Carro") → 120
      </div>

      <h3>Eliminar (delete)</h3>
      <p>Depende del método de manejo de colisiones:</p>
      <ul>
        <li><strong>Chaining:</strong> se elimina un nodo de la lista.</li>
        <li><strong>Open addressing:</strong> se marca la celda como <em>deleted</em>.</li>
      </ul>

      <div class="code-box">
        tabla.delete("Carro")
      </div>

      

    <!-- EJEMPLOS ADICIONALES -->
    <section id="examples">
      <h2>Ejemplos Prácticos</h2>

      <h3>Ejemplo 1: Cálculo de Hash</h3>
      <div class="code-box">
        key = "Gato" <br>
        hash("Gato") = 7 <br>
        → índice 7 en la tabla
      </div>

      <h3>Ejemplo 2: Encadenamiento</h3>
      <div class="code-box">
        tabla[2] → [ ("Rojo", 10) → ("Azul", 15) → ("Verde", 22) ]
      </div>

      <h3>Ejemplo 3: Linear Probing</h3>
      <div class="code-box">
        índice calculado = 4 <br>
        tabla[4] ocupado → probar 5 <br>
        tabla[5] libre → insertar
      </div>

      <h3>Ejemplo 4: Operaciones completas</h3>
      <div class="code-box">
        tabla.put("Perro", 8) <br>
        tabla.put("Gato", 6) <br>
        tabla.put("Pez", 3) <br><br>
        tabla.get("Gato") → 6 <br>
        tabla.delete("Perro") → eliminado
      </div>

    </section>

  </div>


<!-- Imagen al final del blog -->
<div style="text-align:center; margin:20px 0;">
  <img src="FOTO 113.png" alt="imagen final" style="width:120px; border-radius:10px;" />
</div>
</body>
</html>
        <h3>Consideraciones Finales</h3>
        <p>Las tablas hash son fundamentales en informática por su eficiencia. La elección del método de manejo de colisiones y la función hash adecuada son cruciales para un rendimiento óptimo.</p>
        </section>
    
    </div>
