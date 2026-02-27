# 🤖 Jarvis AI Voice Assistant

A real-time AI voice assistant built with [LiveKit Agents](https://docs.livekit.io/agents/) and Google Gemini, featuring a React frontend for seamless browser-based interaction.

## ✨ Features

- 🎙️ **Real-time Voice AI** – Low-latency speech-to-speech powered by LiveKit and Google Gemini
- 🔍 **Google Search** – Jarvis can search the web and summarize results
- 🌤️ **Weather Lookup** – Fetches live weather data via OpenWeather API
- 🧠 **Memory & Reasoning** – Persistent memory store and multi-step reasoning capabilities
- 🪟 **Window & Keyboard Control** – Automate desktop windows and simulate keyboard/mouse input
- 📂 **File Operations** – Open and manage files on the host machine

## 📋 Prerequisites

- Python 3.10+
- Node.js 18+ and [pnpm](https://pnpm.io/)
- [LiveKit Cloud](https://livekit.io/) account (free tier available)
- Google Gemini API key ([Google AI Studio](https://aistudio.google.com/))

## 🚀 Setup

### 1. Backend (Python Agent)

```bash
cd Jarvis_code
python -m venv venv
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

pip install -r requirements.txt

# Copy the environment template and fill in your keys
cp ../.env.example .env

python agent.py dev
```

### 2. Frontend (React App)

```bash
cd agent-starter-react
pnpm install

# Copy the environment template and fill in your LiveKit credentials
cp .env.example .env.local

pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## 🏗️ Architecture

```
User ↔ React Frontend ↔ LiveKit Server ↔ Python Agent ↔ APIs
                                                        ├── Google Gemini (LLM)
                                                        ├── Google Custom Search
                                                        └── OpenWeather
```

## 🚢 Deployment

| Component | Recommended Platform |
|-----------|---------------------|
| React Frontend | [Vercel](https://vercel.com/) |
| Python Agent | [LiveKit Cloud](https://livekit.io/), [Railway](https://railway.app/), or [Render](https://render.com/) |

The `Jarvis_code/Dockerfile` is provided for containerized deployment of the Python agent.

## 📄 License

MIT
