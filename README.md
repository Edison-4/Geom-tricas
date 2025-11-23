# Taller en Clase (POO en Python): Figuras Geométricas

Este código implementa un sistema para gestionar figuras geométricas utilizando **Programación Orientada a Objetos** avanzada:

* **Clases y Abstracción:** La clase base `FiguraGeometrica` define la estructura fundamental (ancho y alto) y obliga a las clases hijas a implementar reglas específicas, como el cálculo del área. Al heredar de `ABC` (Abstract Base Class), actúa como una plantilla que garantiza consistencia.
* **Herencia Múltiple:** Las clases `Cuadrado`, `Rectangulo` y `Circunferencia` son híbridas: heredan propiedades matemáticas de `FiguraGeometrica` y propiedades visuales de la clase `Color` simultáneamente. Esto les permite tener tanto dimensiones como un color asignado.
    
* **Polimorfismo:** El archivo principal `main.py` trata a todas las figuras por igual dentro de una lista. Al recorrerlas en los bucles de suma, el programa invoca los métodos `.area()` o `.perimetro()` y cada objeto responde ejecutando su propia fórmula matemática específica (por ejemplo, $\pi \cdot r^2$ para la circunferencia o $lado \cdot lado$ para el cuadrado) sin que el código principal necesite saber qué tipo de figura es.
* **Manejo de Errores:** El sistema incluye protecciones para asegurar la validez de los datos. Si intentas crear una figura con dimensiones negativas o cero, la clase lanza un error (`ValueError`), el cual es capturado y reportado elegantemente en el bloque `try-except` del archivo principal.

<img width="1920" height="1080" alt="Captura de pantalla 2025-11-20 185829" src="https://github.com/user-attachments/assets/7eac8ed6-7f1a-4674-ab5d-be16da54ea2d" />
