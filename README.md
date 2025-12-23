# my-n8n-Automations
some n8n automations made as introductions to AI and automation processes
# AI-Driven Lead Processing Automation 🚀

Este proyecto implementa un pipeline automatizado para la gestión inteligente de clientes potenciales, integrando captura de datos, procesamiento mediante Modelos de Lenguaje de Gran Escala (LLM) y comunicación automatizada.

## 📊 Arquitectura del Workflow

![Diagrama del Workflow](Captura%20de%20pantalla%202025-12-23%20175619.png)

## 🛠️ Stack Tecnológico
* **Orquestador:** n8n (Arquitectura basada en eventos).
* **IA/LLM:** Llama 3.3 70B vía **Groq** (Inferencia de baja latencia).
* **Integraciones:** Gmail API (OAuth2), n8n Forms.

## 📝 Descripción Técnica
El flujo de trabajo transforma una solicitud pasiva en una oportunidad de negocio activa mediante los siguientes pasos:

1.  **Ingesta Estructurada:** Captura de requerimientos técnicos y presupuesto a través de un disparador de formulario nativo.
2.  **Lógica de Control:** Incorporación de un nodo de espera (**Wait**) para asegurar la consistencia del estado del flujo.
3.  **Generación de Contenido con IA:** Utiliza un agente de LangChain conectado a **Groq**. Se ha implementado un *System Prompt* específico que procesa los inputs del usuario para generar una respuesta en formato **HTML profesional**, personalizada según el tipo de automatización solicitada.
4.  **Despliegue de Comunicación:** Automatización del envío mediante Gmail, asegurando que el cliente reciba una respuesta inmediata y un enlace de agendamiento sincronizado.

## 🚀 Valor de Ingeniería
A diferencia de automatizaciones simples, este flujo destaca por:
* **Prompt Engineering:** Optimización de instrucciones para la generación de código HTML inline compatible con múltiples clientes de correo.
* **Manejo de Variables:** Mapeo dinámico de JSON para inyectar datos del formulario directamente en la lógica del LLM.
* **Escalabilidad:** Diseñado para integrarse fácilmente con CRMs o bases de datos de Big Data en futuras iteraciones.

-----------
## 📧 Intelligent Email Categorizer & Cleanup

Este workflow es un sistema avanzado de gestión de correo electrónico que utiliza Inteligencia Artificial para auditar, clasificar y organizar la bandeja de entrada de forma autónoma.

## 📊 Arquitectura del Proyecto

![Diagrama del Workflow](./image_0c6b22.png)

## 🛠️ Stack Tecnológico
* **Orquestador:** n8n.
* **IA/NLP:** Llama 3.3 70B (vía Groq) con **Structured Output Parser**.
* **Lenguajes:** JavaScript (Node.js) para transformación de datos.
* **Integraciones:** Gmail API con flujos de lectura/escritura.

## 📝 Descripción Técnica
A diferencia de un filtro de spam convencional, este sistema aplica una capa de razonamiento cognitivo para la toma de decisiones:

1.  **Configuración de Workflow:** Utiliza un nodo de **Set** para centralizar variables globales (como el límite de correos a procesar), facilitando el mantenimiento del software.
2.  **Extracción de Datos:** Ingesta dinámica de correos electrónicos mediante la API de Gmail.
3.  **Clasificación Estructurada (IA):** Emplea un agente de LangChain que no solo detecta spam, sino que categoriza los correos legítimos en tópicos específicos (*Work, Personal, Healthcare*, etc.). El uso de un **Structured Output Parser** garantiza que la IA devuelva un objeto JSON válido, eliminando la variabilidad de las respuestas de texto plano.
4.  **Lógica de Negocio (JavaScript):** Implementación de un nodo de código para realizar un mapeo (*Label Mapping*) entre las categorías semánticas de la IA y los IDs de etiquetas internos de la API de Gmail.
5.  **Ejecución de Acciones:** Basado en un nodo condicional (**If**), el sistema decide si mover el mensaje a la papelera o etiquetarlo según su categoría.

## 🚀 Valor de Ingeniería
Este flujo demuestra habilidades avanzadas en:
* **Manejo de JSON Estructurado:** Obligar a un LLM a seguir un esquema estricto para integración en pipelines de software.
* **Programación Funcional:** Uso de `.map()` y *spread operators* en JavaScript para transformar el estado del flujo sin mutaciones no deseadas.
* **Eficiencia Energética/Costes:** Uso de Groq para inferencia rápida, optimizando los tiempos de ejecución del workflow.

---
*Estos proyecto forma parte de mi portfolio como Ingeniero de Software enfocado en Automatización y Procesos de IA.*
