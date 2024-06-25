# TALLER 9 Tarea de LLM

Usando Lang CHain, Pinecone y OpenAI, desarrollar los siguientes desafios:

1. Usando Python, escribir un programa para enviar prompts a ChatGPT y recibir respuestas. https://python.langchain.com/docs/integrations/llms/openai
2. Escribir un RAG simple usando una base de datos de vectores en memoria. https://python.langchain.com/docs/use_cases/question_answering/
3. Escribir un RAG usando pinecone. https://python.langchain.com/docs/integrations/vectorstores/pinecone

## Diseño de la aplicación

- Existen 3 archivos Python, cada una correspodientea a cada uno de los desafios.
- Existe un archivo requerimientos.txt donde encontrará los paquetes necesarios para correr los scripts.
- Existe un archivo Conocimiento.txt donde se podra añadir información para ser intrpretada y consultada usando AI.

## Guia de inicio

Estas instrucciones le permitirán obtener una copia del proyecto en funcionamiento en su máquina local para fines de desarrollo y prueba.

### Prerrequisitos

- Python
- Cuenta en pinecone
- Key OpenAI

s

### Instalación

Ubiquese en el directorio en donde desea descargar el repositorio

`git clone https://github.com/Mateo0laya/AREP-Lab9.git`

Cambie al directorio del repositorio

`cd  AREP-Lab9`

Instale los paquetes necesarios

`pip install -r -\requirements.txt`

Configuracíon de keys

- prompt.py:
  En la linea 8 del archivo deberá escribir su clave generada por OpenAI para conectarse a ChatGPT

- simpleRAG.py:
  En la linea 12 del archivo deberá escribir su clave generada por OpenAI para conectarse a ChatGPT

- pineconeRAG.py:
  En la linea 8 del archivo deberá escribir su clave generada por OpenAI para conectarse a ChatGPT
  En la linea 9 y 33 del archivo deberá escribir su clave generda por pinecone
  En la linea 10 deberá asignar el isguiente valor a la variable: gcp-starter

## Probando la aplicación

1. Enviar prompts a ChatGPT y recibir respuestas:
   En el archivo prompt.py en la linea 22 podrá escribir la pregunta que desea realizar, en este caso para el ejemplo preguntaremos: "What is at the core of Popper's theory of science?". Corremos el programa con el comando:

   `python prompt.py`

   Y recibimos respuesta en la terminal:

   ![image](https://github.com/Mateo0laya/AREP-Lab9/assets/89365336/bc85c224-a8ee-4147-807e-92233ee8692b)

2. Simple RAG:
   Aqui tomaremos información de una pagina web y realizaremos la siguiente pregunta configurada en la linea 48: "What is Task Decomposition?". Corremos el programa con el comando:

`python simpleRAG.py`

y recibimos respuesta en la terminal:

![image](https://github.com/Mateo0laya/AREP-Lab9/assets/89365336/25661d67-8fae-4a8b-bbf4-f751db04143f)

3. RAG con pinecone:
   En este caso debemos dirigirnos al archivo Conocimiento.txt, allí escribiremos información sobre un tema que será la base sobre la que nos contestará la AI, en este caso el texto es una noticia de la NASA sobre la Voyager1 estraida de: https://blogs.nasa.gov/voyager/2024/03/15/nasa-engineers-make-progress-toward-understanding-voyager-1-issue/. Una vez este archivo esta listo, la pregunta se realiza en la linea 62, en este caso la pregunta es: "What happened with the Voyager1". Corremos el comando:

   `python pineconeRAG.py`

   y recibimos respuesta en la terminal:

   ![image](https://github.com/Mateo0laya/AREP-Lab9/assets/89365336/9cd366a2-4aff-4616-86c4-f6ebd80250cf)

## Construido con

- [Python](https://www.python.org/) - The main programming language
- [OpenAI](https://chat.openai.com/) - Chat AI
- [Pinecone](https://www.pinecone.io/) - Vector Database

## Version

Version 1.0.0.

## Autor

Mateo Olaya Garzon
