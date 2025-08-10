# Rasa Language Translation Chatbot

Este es un chatbot de traducción de idiomas desarrollado con **Rasa**. Utiliza la librería **googletrans** para traducir texto entre diferentes idiomas.

## Descripción

Este proyecto de chatbot está diseñado para permitir a los usuarios traducir texto de un idioma a otro utilizando un bot conversacional. Está basado en **Rasa**, un marco de código abierto para construir aplicaciones de inteligencia artificial conversacional, como chatbots y asistentes virtuales. La traducción se realiza utilizando la librería **googletrans**.

## Requisitos

Asegúrate de tener las siguientes dependencias instaladas:

- Python 3.7 o superior
- Rasa
- googletrans
- Virtualenv o entorno de Conda (opcional pero recomendado)

## Instalación

Sigue estos pasos para configurar el proyecto en tu máquina local:

### 1. Clona el repositorio

```bash
git clone [https://github.com/tu_usuario/tu_repositorio.git](https://github.com/alexoterol/academic-chatbot-rasa)
cd tu_repositorio
```

### 2. Crea y activa un entorno virtual (opcional)
Usando virtualenv:

```bash
Copy
python -m venv .venv
source .venv/bin/activate  # En Linux/macOS
.venv\Scripts\activate  # En Windows
```

### 3. Instalar las dependencias
```bash
pip install -U pip
pip install rasa
pip install googletrans==4.0.0-rc1
```

## Ejecutando el proyecto
### Iniciar el servidor
En una terminal, ejecuta:

```bash
rasa run actions
rasa bash
```
