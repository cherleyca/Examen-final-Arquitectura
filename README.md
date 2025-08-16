# Microservicio de Optimizaci´on de Portafolio de Inversiones

Este proyecto es una solución completa para la optimización de un portafolio de inversiones, resuelto como un microservicio y una interfaz de usuario. El backend utiliza un algoritmo de programación dinámica para encontrar la combinación óptima de proyectos que maximiza la ganancia total sin exceder un presupuesto dado, mientras que el frontend proporciona una interfaz intuitiva para interactuar con la API.

##  **Características**

* **Backend (Python + Flask):** Un microservicio ligero con un ´unico endpoint `/optimizar` que implementa el algoritmo del problema de la mochila 0/1. Incluye validaci´on robusta de datos de entrada.

* **Frontend (React + Tailwind CSS):** Una interfaz web din´amica que permite a los usuarios agregar proyectos, ingresar costos y ganancias, y visualizar los resultados de la optimizaci´on en tiempo real.

* **Documentaci´on:** La API est´a documentada con una especificaci´on OpenAPI, y este archivo README proporciona instrucciones completas de uso y despliegue.

##  **Instalación y Uso**

Sigue estos pasos para configurar y ejecutar la aplicaci´on.

### **1. Configuración del Backend**

Navega al directorio `backend`, crea un entorno virtual e instala las dependencias.

```sh
cd backend
python3 -m venv venv
source venv/bin/activate  # En Windows usa `venv\Scripts\activate`
pip install -r requirements.txt

##  **1. Configuración del Backend**
Navega al directorio backend, crea un entorno virtual e instala las dependencias.

cd backend
python3 -m venv venv
source venv/bin/activate  # En Windows usa `venv\Scripts\activate`
pip install -r requirements.txt

##  **2. Configuración del Frontend**
Navega al directorio frontend e instala las dependencias de Node.js.

cd frontend
npm install

##  **3. Despliegue de la Aplicación**
Ejecuta el backend y el frontend en terminales separadas.

Backend
Asegúrate de que estás en el directorio backend con el entorno virtual activado y ejecuta el servidor.

flask run

El servidor se ejecutará en http://127.0.0.1:5000.

Frontend
Asegúrate de que estás en el directorio frontend y ejecuta la aplicación de React.

npm start

##  **La aplicación se abrirá en tu navegador en http://localhost:3000.**

##  ** Documentación de la API**
El endpoint /optimizar del microservicio está documentado con la especificación OpenAPI, que se puede encontrar en el archivo docs/openapi.yaml.

##  **Endpoint: /optimizar (POST)**
Este endpoint recibe un objeto JSON con la capacidad presupuestaria y una lista de proyectos, y devuelve la combinación óptima.

##  **Entrada (JSON):**

{
  "capacidad": 10000,
  "objetos": [
    {"nombre": "A", "peso": 2000, "ganancia": 1500},
    {"nombre": "B", "peso": 4000, "ganancia": 3500}
  ]
}

##  **Salida (JSON):**

{
  "seleccionados": ["B"],
  "ganancia_total": 3500,
  "peso_total": 4000
}

##  **Casos de Error:**

400 Bad Request: Se devuelve si los datos de entrada son inválidos o faltan.
