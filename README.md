# my-n8n-Automations
some n8n automations made as introductions to AI and automation processes
1.-My workflow:
Automated Lead Engagement System (n8n + LLM)
Este workflow automatiza el ciclo de vida inicial de un lead, desde la captación hasta la respuesta personalizada, utilizando Inteligencia Artificial para maximizar la conversión.

Arquitectura Técnica:

Ingesta de Datos: Utiliza un nodo de Form Trigger para capturar inputs estructurados (Nombre, Presupuesto, Necesidad Técnica).

Capa de Inteligencia (IA): Integra el modelo Llama-3.3-70B a través de Groq, configurado como un agente de LangChain. Se utiliza un System Message optimizado para transformar los datos del formulario en un correo persuasivo con formato HTML inline.

Control de Flujo: Incluye un nodo de Wait para gestionar la cadencia de la automatización y asegurar la disponibilidad de los datos en el contexto del flujo.

Salida de Datos: Conexión mediante Gmail OAuth2 para el envío automatizado de propuestas personalizadas con enlaces de agendamiento (Cal.com).

Actualmente, el flujo asume que el correo electrónico es válido debido a la validación del formulario. Como mejora futura (v2), se planea implementar un nodo de validación de sintaxis de email
