🏦 Agente de Servicio Bancario (Demo Agentic)

Siéntete libre de leer la guía completa paso a paso:
"Construyendo un Agente de Servicio al Cliente Bancario con RAG + Tools + SQLite"

Un demo ligero de asistente bancario agentico que:

Recupera productos del cliente desde una base de datos local SQLite usando un Customer ID

Consulta un documento de políticas para responder qué puede o no puede hacer el cliente con esos productos

Responde con orientación segura y alineada a las políticas

Este proyecto es únicamente con fines de aprendizaje/demo. Utiliza políticas ficticias y datos de ejemplo.

✨ Características

Herramienta 1 — Recuperación de Productos: obtiene los productos del cliente por customer_id desde SQLite

Herramienta 2 — Preguntas y Respuestas sobre Políticas: lee un documento de políticas y encuentra secciones relevantes para responder preguntas

Bucle del Agente (Agent Loop): decide qué herramienta(s) llamar y luego genera la respuesta final

Seguridad: rechaza acciones no permitidas por la política y evita alucinaciones sobre operaciones de cuenta

🧠 Cómo funciona (Nivel General)

El usuario proporciona el Customer ID

El agente llama a get_customer_products(customer_id) (SQLite)

El usuario hace preguntas sobre los productos (ej. límites, elegibilidad, restricciones)

El agente llama a search_policy(question, product_context) (recuperación de políticas)

El agente genera una respuesta final basada en la política recuperada