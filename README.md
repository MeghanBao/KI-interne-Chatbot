# KI Assistant für Baubranche 🏗️🤖 / AI Assistant for the Construction Industry 🏗️🤖

| Deutsch | English |
|---------|---------|
| Eine intelligente, lokale KI-Lösung, die speziell für die Anforderungen der Baubranche entwickelt wurde. | An intelligent, local AI solution designed specifically for the needs of the construction industry. |
| Dieses System kombiniert die Leistungsfähigkeit von **GPT-4o** mit firmeneigenem Wissen durch **RAG (Retrieval-Augmented Generation)**. | This system combines the power of **GPT-4o** with company-specific knowledge via **RAG (Retrieval-Augmented Generation)**. |

---

## ✨ Kernfunktionen / Core Features

| Deutsch | English |
|---------|---------|
| **💬 Intelligenter Chat:** Nutzt GPT-4o für präzise Antworten auf technisches und kaufmännisches Fachwissen. | **💬 Intelligent Chat:** Uses GPT-4o to provide precise answers to technical and business-related questions. |
| **📄 Dokumenten-KI (RAG):** Laden Sie Bauverträge, Angebote oder DIN-Normen (PDF) hoch. Die KI nutzt diese als exklusive Wissensbasis. | **📄 Document AI (RAG):** Upload construction contracts, offers, or DIN standards (PDF). The AI uses these as an exclusive knowledge base. |
| **🗃️ Lokale Historie:** Alle Gespräche werden sicher in einer lokalen SQLite-Datenbank gespeichert. | **🗃️ Local History:** All conversations are securely stored in a local SQLite database. |
| **🔒 Datenschutz:** Firmendaten verbleiben auf Ihrem System und werden nur zur Verarbeitung über die API gesendet (kein Training!). | **🔒 Data Privacy:** Company data remains on your system and is only sent to the API for processing (no training!). |
| **🌐 Modernes Interface:** Intuitive Weboberfläche mit Sidebar für die Chat-Historie und Markdown-Unterstützung. | **🌐 Modern Interface:** Intuitive web interface with sidebar for chat history and Markdown support. |

---

## 🛠️ Technologie-Stack / Technology Stack

| Deutsch | English |
|---------|---------|
| **Backend:** FastAPI (Python), SQLAlchemy (SQLite), LangChain, ChromaDB (Vector DB) | **Backend:** FastAPI (Python), SQLAlchemy (SQLite), LangChain, ChromaDB (Vector DB) |
| **Frontend:** React, Vite, TypeScript, Lucide-React (Icons) | **Frontend:** React, Vite, TypeScript, Lucide-React (Icons) |
| **KI-Modell:** OpenAI GPT-4o via API | **AI Model:** OpenAI GPT-4o via API |

---

## 🚀 Installation & Start / Installation & Start

### 1. Backend einrichten / Setup Backend

| Deutsch | English |
|---------|---------|
| ```bash
cd backend
pip install -r requirements.txt
cp .env.template .env
# Tragen Sie Ihren API-Key ein
uvicorn main:app --reload
```<br>Der API-Server läuft nun unter [http://localhost:8000](http://localhost:8000) | ```bash
cd backend
pip install -r requirements.txt
cp .env.template .env
# Enter your OPENAI_API_KEY
uvicorn main:app --reload
```<br>The API server is now running at [http://localhost:8000](http://localhost:8000) |

### 2. Frontend einrichten / Setup Frontend

| Deutsch | English |
|---------|---------|
| ```bash
cd frontend
npm install
npm run dev
```<br>Das Interface ist nun unter [http://localhost:5173](http://localhost:5173) erreichbar | ```bash
cd frontend
npm install
npm run dev
```<br>The interface is now available at [http://localhost:5173](http://localhost:5173) |

### 3. Deployment mit Docker (Empfohlen / Recommended)

| Deutsch | English |
|---------|---------|
| Docker ist der einfachste Weg, wenn Sie die KI auf einem zentralen Firmen-Server installieren möchten.<br>- Docker & Docker Compose müssen installiert sein.<br>- API-Key in `backend/.env` eintragen.<br>- System starten: ```docker-compose up -d --build```<br>Die KI ist nun im Netzwerk unter der IP-Adresse des Servers erreichbar (Port 80 für das Interface, Port 8000 für die API). | Docker is the easiest way if you want to deploy the AI on a central company server.<br>- Ensure Docker & Docker Compose are installed.<br>- Enter your API key in `backend/.env`.<br>- Start the system: ```docker-compose up -d --build```<br>The AI is now accessible on the network via the server's IP (port 80 for the interface, port 8000 for the API). |

---

## 📖 Benutzung / Usage

| Deutsch | English |
|---------|---------|
| **Chat:** Wählen Sie "Neuer Chat" in der Sidebar, um ein Gespräch zu beginnen. | **Chat:** Select "New Chat" in the sidebar to start a conversation. |
| **Wissen hinzufügen:** Nutzen Sie den "PDF hochladen"-Button, um Dokumente zu indizieren. Die KI berücksichtigt diese Informationen automatisch in zukünftigen Antworten. | **Add Knowledge:** Use the "Upload PDF" button to index documents. The AI will automatically include this information in future responses. |

---

## ⚠️ Warnhinweis / Warning

| Deutsch | English |
|---------|---------|
| Urheberrechtshinweis: Der Quellcode dieses Projekts ist aufgrund interner Unternehmensrichtlinien nicht öffentlich zugänglich. Dieses Repository enthält lediglich eine detaillierte README, um die Struktur, das Design und die Ergebnisse des Projekts zu dokumentieren. Alle Materialien werden ausschließlich zu Bildungs- und Portfoliozwecken geteilt. | Copyright notice: The source code of this project is not publicly available due to internal company policies. This repository contains only a detailed README to document the project’s structure, design, and outcomes. All materials are shared exclusively for educational and portfolio purposes. |
