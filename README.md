# Rasa Language Translation Chatbot

Chatbot conversacional construido con **Rasa** que, además de una conversación
básica de cortesía (saludo, despedida, estado de ánimo), traduce texto entre
idiomas usando la librería **googletrans**.

## Requisitos

- **Python 3.10** (Rasa 3.6 no soporta 3.11+; si no lo tienes, instálalo con
  `winget install --id Python.Python.3.10` en Windows o desde
  [python.org](https://www.python.org/downloads/))
- pip

## Instalación

### 1. Clona el repositorio

```bash
git clone https://github.com/alexoterol/academic-chatbot-rasa.git
cd academic-chatbot-rasa
```

### 2. Crea y activa un entorno virtual

```bash
py -3.10 -m venv .venv

# Windows
.venv\Scripts\activate

# Linux/macOS
source .venv/bin/activate
```

### 3. Instala las dependencias

```bash
pip install -U pip
pip install rasa
pip install googletrans==4.0.0-rc1

pip install -r requirements.txt
```

## Ejecutando el proyecto

Con el entorno virtual activado:

### 1. Entrena el modelo

```bash
rasa train
```

### 2. Inicia el servidor de acciones (necesario para `action_translate`)

En una terminal:

```bash
rasa run actions
```

### 3. Habla con el bot

En otra terminal (con el entorno virtual también activado):

```bash
rasa shell
```

## Estructura del proyecto

```
data/            # Ejemplos de NLU, reglas e historias de conversación
actions/         # Acción personalizada action_translate (googletrans)
tests/           # Historias de prueba para validar el bot
domain.yml       # Intenciones, entidades y respuestas del bot
config.yml       # Pipeline de NLU y políticas de diálogo
endpoints.yml    # Endpoint del servidor de acciones
```

## Probar el traductor

Ejemplo de mensaje que dispara `action_translate`:

```
Traduce "gracias" al alemán
```

## Ejecutar los tests

```bash
rasa test
```
