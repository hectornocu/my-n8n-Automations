# my-n8n-Automations
some n8n automations made as introductions to AI and automation processes
# AI-Driven Lead Processing Automation 🚀

Este proyecto implementa un pipeline automatizado para la gestión inteligente de clientes potenciales, integrando captura de datos, procesamiento mediante Modelos de Lenguaje de Gran Escala (LLM) y comunicación automatizada.

## 📊 Arquitectura del Workflow

![Diagrama del Workflow]

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

---
*Este proyecto forma parte de mi portfolio como Ingeniero de Software enfocado en Automatización y Procesos de IA.*
