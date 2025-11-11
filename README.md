# LangChain-LLM-AREP

Este repositorio contiene el código y la documentación de un proyecto básico desarrollado por Juan Cancelado, que utiliza LangChain y OpenAI para construir una aplicación sencilla de traducción de texto.
El proyecto sigue el tutorial oficial de LangChain: Build a simple LLM application with chat models and prompt templates.

## 🧠Descripción del Proyecto

El objetivo de este proyecto es crear una aplicación que traduzca texto del inglés a otros idiomas utilizando un modelo de lenguaje (LLM) de OpenAI (como GPT-4) junto con el framework LangChain.
A través del uso de prompt templates, se estructuran las entradas al modelo para lograr respuestas más precisas y naturales.

## ⚙️ Requisitos

Para ejecutar este proyecto necesitarás:
1. Una cuenta en OpenAI con una API Key válida.
2. Un entorno de trabajo como Google Colab o Python 3.8+ instalado localmente.
3. Las siguientes bibliotecas de Python:
- langchain
- langchain[openai]
- python-dotenv

## 🧩 Instalación

Sigue estos pasos para configurar el entorno del proyecto:

1. Clona este repositorio:

 ```bash
git clone https://github.com/juanescan/LangChain-LLM-AREP.git
cd LangChain-LLM-AREP
```

2. Instala las dependencias necesarias:
 ```bash
pip install langchain
pip install -qU "langchain[openai]"
pip install python-dotenv
```

3. Configura tus variables de entorno:
    - Crea un archivo llamado .env en la raíz del proyecto con el siguiente contenido:
```bash
OPENAI_API_KEY=tu_clave_de_openai
```

## 📁 Estructura del Proyecto

La organización del proyecto es la siguiente:

```
LangChain-LLM-AREP/
├── README.md
├── src/
│   └── LangChain.ipynb
```
Descripción de archivos:
- README.md: Documentación general del proyecto.
- LangChain.ipynb: Notebook principal con el código de ejemplo.

## ⚙️ Configuración Rápida

1. Clona el repositorio si trabajas de forma local:

 ```bash
git clone https://github.com/juanescan/LangChain-LLM-AREP.git
cd LangChain-LLM-AREP
```
2. Instala las dependencias:

 ```bash
pip install langchain openai
```
3. Configura tu API key en Colab (opcional):

 ```bash
import getpass, os
os.environ["OPENAI_API_KEY"] = getpass.getpass("Enter your OpenAI API key: ")
```

## 💻 Uso

1. Abre el notebook LangChain.ipynb.

2. Ejecuta las celdas paso a paso para:
- Inicializar el modelo de lenguaje.
- Crear y personalizar un prompt template.
- Traducir texto del inglés al idioma que elijas.

3. Ejemplo básico de código:

 ```bash
from langchain.chat_models import init_chat_model
from langchain_core.messages import HumanMessage, SystemMessage
from langchain_core.prompts import ChatPromptTemplate

# Inicializar modelo
model = init_chat_model("gpt-4", model_provider="openai")

# Crear plantilla del prompt
system_template = "Translate the following from English into {language}"
prompt_template = ChatPromptTemplate.from_messages([
    ("system", system_template),
    ("user", "{text}")
])

# Traducir texto
prompt = prompt_template.invoke({"language": "Italian", "text": "good morning"})
response = model.invoke(prompt)
print(response.content)  # Output: "Buongiorno!"

```

## 🌍 Ejemplos de Traducción

- Inglés → Italiano:

 ```bash
prompt = prompt_template.invoke({"language": "Italian", "text": "good morning"})
response = model.invoke(prompt)
print(response.content)  # Output: "Buongiorno!"
```

- Inglés → Francés:

 ```bash
prompt = prompt_template.invoke({"language": "French", "text": "good night"})
response = model.invoke(prompt)
print(response.content)  # Output: "Bonne nuit!"
```

## 🖼️ Capturas de Pantalla

![IA](/imagenes/1.png)

![IA](/imagenes/2.png)

![IA](/imagenes/3.png)

![IA](/imagenes/4.png)

## 👨‍💻 Autor
- Juan Esteban Cancelado - *AREP* *LangChain-LLM-AREP* - [juanescan](https://github.com/juanescan)