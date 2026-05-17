# 🚑 Agente de IA para Emergencias Hospitalarias

Sistema inteligente para gestión y análisis de emergencias hospitalarias utilizando IA, FastAPI, React, Supabase, OpenAI y automatizaciones con n8n + Discord.

---

# 🌐 Demo del Sistema

🔗 Sistema desplegado:

[https://proyectohackiathon.vercel.app](https://proyectohackiathon.vercel.app)

---

# 💬 Canal de Alertas Discord

🔗 Discord:

[https://discord.gg/65ypTrYr](https://discord.gg/65ypTrYr)

---

# 🧠 Tecnologías Utilizadas

## Frontend

* React + Vite
* JavaScript
* Fetch API
* CSS inline

## Backend

* FastAPI
* Python
* OpenAI API
* Supabase
* Requests
* Uvicorn

## Base de Datos

* Supabase PostgreSQL

## Automatización

* n8n
* Discord Webhooks

---

# 🤖 Modelo de IA Utilizado

Modelo utilizado:

```bash
GPT-4.1-mini
```

La IA analiza:

* Motivo de emergencia
* Cobertura médica
* Preexistencias
* Riesgo del paciente
* Recomendaciones rápidas

---

# 🏥 Lógica del Sistema de Pólizas

El sistema trabaja con 3 tipos principales de pólizas médicas:

| Póliza  | Estado   | Cobertura         | Copago |
| ------- | -------- | ----------------- | ------ |
| VIP-001 | Activa   | Emergency Full    | $25    |
| VIP-002 | Inactiva | Basic             | $50    |
| VIP-003 | Activa   | Premium Emergency | $15    |

## Funcionamiento

Cuando un paciente ingresa:

1. El sistema valida la póliza en Supabase.
2. Verifica si la póliza está activa o inactiva.
3. Consulta enfermedades preexistentes.
4. La IA analiza el motivo de emergencia.
5. Genera nivel de riesgo y recomendaciones.
6. Guarda el caso en la base de datos.
7. Envía una alerta automática a Discord mediante n8n.

## Ejemplos

### VIP-001

* Cobertura completa de emergencias.
* Riesgo alto recibe atención prioritaria.
* Copago reducido.

### VIP-002

* Cobertura básica.
* Mayor copago.
* Puede requerir validación manual.

### VIP-003

* Cobertura premium.
* Atención prioritaria.
* Copago mínimo.

---

# ⚙️ Funcionalidades

✅ Validación de pólizas

✅ Consulta de preexistencias

✅ Análisis inteligente con IA

✅ Historial de emergencias

✅ Notificaciones automáticas en Discord

✅ Sistema desplegado en la nube

---

# 🏥 Flujo del Sistema

1. El usuario ingresa datos del paciente.
2. FastAPI recibe la emergencia.
3. Se consulta Supabase.
4. OpenAI genera el análisis.
5. Se guarda el caso clínico.
6. n8n envía alerta automática.
7. Discord recibe la notificación.

---

# 📦 Estructura del Proyecto

```bash
proyecto_hackiathon/
│
├── backend/
│   ├── main.py
│   ├── requirements.txt
│   └── .env
│
├── frontend/
│   ├── src/
│   ├── public/
│   └── package.json
│
└── README.md
```

---

# 🔐 Variables de Entorno

## Backend (.env)

```env
SUPABASE_URL=your_url
SUPABASE_KEY=your_key
OPENAI_API_KEY=your_openai_key
```

---

# ▶️ Ejecución Local

## Backend

```bash
cd backend

python -m venv venv

venv\Scripts\activate

pip install -r requirements.txt

uvicorn main:app --reload
```

---

## Frontend

```bash
cd frontend

npm install

npm run dev
```

---

# 🚀 Despliegue

## Frontend

* Vercel

## Backend

* Render

## Base de Datos

* Supabase

---

# 📡 Endpoints API

## Obtener historial

```http
GET /cases
```

## Analizar emergencia

```http
POST /emergency
```

Ejemplo:

```json
{
  "nombre": "Carlos Mena",
  "cedula": "1723456789",
  "poliza": "VIP-001",
  "motivo": "Dolor torácico"
}
```

---

