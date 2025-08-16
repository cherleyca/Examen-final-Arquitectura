Microservicio de Optimizaci´on de Portafolio de Inversiones con Restricci´on Presupuestaria
Este proyecto es una aplicación web de página única que implementa un microservicio simulado para resolver el problema de la mochila (Knapsack Problem) con el objetivo de optimizar un portafolio de inversiones. Dada una capacidad presupuestaria y una lista de proyectos con sus costos y ganancias, la aplicación encuentra la combinación de proyectos que maximiza la ganancia total sin exceder el presupuesto.

Tecnologías Utilizadas
HTML5: Para la estructura de la aplicación.

Tailwind CSS: Para el estilo y el diseño responsivo de la interfaz.

JavaScript (Vanilla JS): Para la lógica del frontend y la implementación del algoritmo de optimización.

Características Principales
Frontend Dinámico: Permite a los usuarios agregar, editar y eliminar proyectos de inversión de forma interactiva.

Algoritmo de Optimización Eficiente: Utiliza un algoritmo de programación dinámica para resolver el problema de forma óptima.

Visualización de Resultados: Muestra claramente los proyectos seleccionados, la ganancia total y el costo total en una tarjeta de resultados.

Validación de Errores: Incluye validaciones básicas para asegurar que los datos de entrada sean válidos.

Uso
Para utilizar la aplicación, simplemente abre el archivo index.html en cualquier navegador web moderno. No se requiere servidor ni instalación de dependencias adicionales.

Pasos
Ingresar la Capacidad: Introduce tu presupuesto total en el campo "Capacidad Presupuestaria".

Gestionar Proyectos: Utiliza los campos de entrada para definir los proyectos de inversión, sus costos y sus ganancias. Haz clic en "Agregar Proyecto" para añadir más filas.

Calcular: Presiona el botón "Calcular" para que el algoritmo procese los datos y muestre la solución óptima.

Limpiar: El botón "Limpiar" borra todos los campos para comenzar un nuevo cálculo.

Explicación del Algoritmo
La lógica central de la aplicación se basa en la programación dinámica para resolver el problema de la mochila 0/1 (donde cada proyecto puede ser seleccionado una vez o no).

El algoritmo construye una tabla (dp) donde dp[i][j] representa la máxima ganancia que se puede obtener con los primeros i proyectos y una capacidad de j. La tabla se llena iterativamente, decidiendo en cada paso si se incluye o no el proyecto actual para maximizar el valor. Finalmente, la solución óptima se reconstruye a partir de la tabla para identificar los proyectos seleccionados.

Esta implementación garantiza una solución correcta y eficiente, con una complejidad temporal de O(n×W), donde n es el número de proyectos y W es la capacidad máxima.
