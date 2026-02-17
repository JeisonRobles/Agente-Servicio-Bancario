# 🏦 Agente de Servicio Bancario (Agentic Banking Demo)

Un asistente bancario **agentic** que:

1. 📊 Consulta productos del cliente desde una base SQLite
2. 📜 Lee y consulta políticas internas del banco (RAG)
3. 🤖 Decide automáticamente qué herramienta utilizar
4. 🛡️ Responde de forma alineada a políticas y sin alucinaciones

> Proyecto educativo/demostrativo. Usa datos ficticios y políticas simuladas.

---

## 🚀 ¿Qué demuestra este proyecto?

Este repositorio muestra cómo construir un **sistema agentic realista**:

- Uso de herramientas (tools)
- Bucle de decisión del agente
- Recuperación de información estructurada (SQLite)
- Recuperación semántica de documentos (RAG)
- Control de seguridad basado en políticas

Es una base sólida para:
- Agentes bancarios
- Sistemas regulatorios
- Asistentes internos empresariales
- Multi-agent systems

---

## 🧠 Arquitectura

Usuario  
⬇  
Agente (LLM + Tool Schemas)  
⬇ decide  
🔧 Tool 1 → Consulta productos en SQLite  
🔧 Tool 2 → Búsqueda semántica en documento de política  
⬇  
Respuesta final alineada a reglas

---

## 📂 Estructura del Proyecto

Agente-Servicio-Bancario/
│
├── BankingServiceAgent_4.ipynb # Notebook principal (demo funcional)
├── Bank_Policy_Spanish.md # Documento de políticas internas
├── LICENSE
├── README.md
├── requirements.txt
└── .gitignore


---

## ⚙️ Instalación Local

### 1️⃣ Clonar repositorio

git clone https://github.com/JeisonRobles/Agente-Servicio-Bancario.git
Tambien puede consultarse en Google Colaboratory : https://colab.research.google.com/drive/1hJpDvZ6FK92922PKcqnrQDVOuQvpNaKa#scrollTo=zlogiPXUv8FV
cd Agente-Servicio-Bancario
2️⃣ Crear entorno virtual
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
3️⃣ Instalar dependencias
pip install -r requirements.txt
4️⃣ Configurar API Key

Crear archivo .env:

OPENAI_API_KEY=tu_api_key_aqui
🧪 Ejecutar

Actualmente el proyecto corre desde el notebook:

BankingServiceAgent_4.ipynb

Puedes ejecutarlo en:

Google Colab
Jupyter Notebook
VSCode Notebook

🔒 Seguridad
El agente:
No ejecuta acciones prohibidas
No inventa operaciones bancarias
Respeta restricciones de política
Minimiza divulgación de información sensible

📈 Próximas Mejoras
Separar lógica en carpeta src/
Implementar CLI interactivo
Añadir tests automatizados
Integrar base vectorial persistente
Migrar a arquitectura multi-agente

👨‍💻 Autor

Jeison Robles Arias
Data Scientist | Agentic Systems | AI Engineering