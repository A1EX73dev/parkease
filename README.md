# 🅿️ Parkease – Gestor de Plazas de Parking

**Parkease** es un sistema inteligente para la gestión de plazas de parking, que combina una aplicación web desarrollada en **Flask (Python)** con dispositivos **ESP32** para detectar y mostrar el estado de ocupación de las plazas en tiempo real.

## 🚀 Características

- Monitorización en tiempo real del estado de las plazas (ocupado/libre)
- Comunicación entre ESP32 y servidor Flask
- Interfaz web para visualizar el estado de cada plaza
- Código modular y fácil de escalar

## 🛠️ Tecnologías utilizadas

- **Python 3** + **Flask**
- **ESP32** con sensores (ultrasonido)
- **ESP32-CAM** (cámara para leer matriculas de vehículo)
- HTML, CSS

## 🧱 Estructura del proyecto

Parking/ ├── parkease/ # Carpeta principal del proyecto Flask │ ├── templates/ # HTML templates │ ├── static/ # Archivos estáticos │ ├── main.py # Script principal de Flask │ └── ... # Otros módulos o rutas ├── venv/ # Entorno virtual de Python └── README.md # Este archivo

> ⚠️ **Importante**: Antes de ejecutar el proyecto, asegúrate de mover la carpeta `parkease/` fuera de la carpeta `Parking/`, quedando ambas al mismo nivel.

## ⚙️ Cómo ejecutar el proyecto

### 1. 🔌 Activar entorno virtual

Desde la raíz del proyecto, activa el entorno virtual con:

./venv/Scripts/activate

### 2. 🚀 Iniciar la aplicación Flask
Luego ejecuta:

flask --app main.py run --host=0.0.0.0 --port=81 --debug
Esto levantará la app en http://localhost:81 o la IP local del equipo.

### 📡 ESP32
El ESP32 debe estar programado para enviar datos al servidor Flask (usando la IP del host y puerto 81).

Detectará el estado de las plazas (libre/ocupado) mediante sensores físicos y enviará las actualizaciones mediante HTTP o MQTT (según configuración).

Asegúrate de configurar el Wi-Fi y la IP del servidor en el código del ESP32.

Desarrollado por Alex Romero – usando Flask y ESP32.
