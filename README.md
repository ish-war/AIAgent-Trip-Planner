# 🌍 AI Agent Trip Planner

An **AI-powered travel planning application** that helps you plan trips for any city worldwide using real-time data.  
The system combines **FastAPI** as a backend with **Streamlit** as a frontend, integrating multiple APIs for weather, attractions, hotels, currency conversion, itinerary planning, and expense calculation.

---

## 📜 Problem Statement

The goal of this project is to build an **agentic AI system** that plans a trip for any city worldwide using real-world, live data.  
The application provides:

1. 🌦 **Real-time weather information**
2. 🗺 **Attractions and activities** in the selected location
3. 🏨 **Hotel cost estimates**
4. 💱 **Currency conversion rates**
5. 📅 **Itinerary planning**
6. 💰 **Total trip expense calculation**
7. 📝 **Summary generation** for the trip

---

## 🚀 Features

- **Agentic Workflow** using LangChain + Groq for dynamic reasoning.
- **Real-time APIs** integration:
  - OpenWeatherMap – Weather data
  - Google Places / Tavily / Foursquare – Attractions & POIs
  - ExchangeRate API – Currency conversion
  - Hotel price APIs – Cost estimation
- **Fallback mechanism** – If one API fails (e.g., Google Places), an alternate API (e.g., Tavily) is used automatically.
- **Backend**: FastAPI with async handling.
- **Frontend**: Streamlit for interactive UI.
- **Graph-based workflow** with Mermaid visualization of the agent’s reasoning steps.

---

## 🛠 Tech Stack

**Backend:**
- Python 3.12+
- FastAPI
- LangChain
- Groq LLM
- Pydantic

**Frontend:**
- Streamlit

**APIs Used:**
- `GROQ_API_KEY` – Groq LLM
- `GOOGLE_API_KEY` – Google Search API
- `GPLACES_API_KEY` – Google Places API
- `FOURSQUARE_API_KEY` – Foursquare Places API
- `TAVILY_API_KEY` – Tavily Search API
- `OPENWEATHERMAP_API_KEY` – OpenWeatherMap API
- `EXCHANGE_RATE_API_KEY` – ExchangeRate API
- `LANGCHAIN_API_KEY` – LangChain API

---

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/ish-war/AIAgent-Trip-Planner.git
cd AIAgent-Trip-Planner
```

### 2️⃣ Create and activate a virtual environment

# Using uv

```bash
uv init 
uv venv env  --python 3.12
env\Scripts\activate     # Windows
```

# Or using conda

```bash
conda create --name tripplanner python=3.12
conda activate tripplanner
```

### 3️⃣ Install dependencies

```bash
uv pip install -r requirements.txt
```

### 4️⃣ Set environment variables

Create a .env file in the project root:

```bash
GROQ_API_KEY=your_groq_key
GOOGLE_API_KEY=your_google_key
GPLACES_API_KEY=your_gplaces_key
FOURSQUARE_API_KEY=your_foursquare_key
TAVILY_API_KEY=your_tavily_key
OPENWEATHERMAP_API_KEY=your_openweather_key
EXCHANGE_RATE_API_KEY=your_exchange_key
LANGCHAIN_API_KEY=your_langchain_key
```

## ▶️ Running the Application

### 1️⃣ Start the FastAPI backend

```bash
uvicorn main:app --reload --port 8000
```

### 2️⃣ Start the Streamlit frontend

```bash
streamlit run streamlit_app.py
```

## 📜 License

This project is licensed under the MIT License – feel free to use, modify, and distribute.

