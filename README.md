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

