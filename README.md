[English](#english) | [Deutsch](#deutsch)

# AI Assistant for the Construction Industry 🏗️🤖

<a id="english"></a>

An intelligent, local AI solution designed specifically for the requirements of the construction industry. This system combines the power of GPT-4o with proprietary company knowledge through RAG (Retrieval-Augmented Generation).

## ✨ Core Features

- **💬 Intelligent Chat:** Uses GPT-4o for precise answers to technical and commercial specialist knowledge.
- **📄 Document AI (RAG):** Upload construction contracts, offers, or DIN standards (PDF). The AI uses these as an exclusive knowledge base.
- **🗃️ Local History:** All conversations are securely stored in a local SQLite database.
- **🔒 Data Privacy:** Company data remains on your system and is only sent via API for processing (no training!).
- **🌐 Modern Interface:** Intuitive web interface with a sidebar for chat history and Markdown support.

## 🛠️ Technology Stack

- **Backend:** FastAPI (Python), SQLAlchemy (SQLite), LangChain, ChromaDB (Vector DB).
- **Frontend:** React, Vite, TypeScript, Lucide-React (Icons).
- **AI Model:** OpenAI GPT-4o via API.

## 🚀 Installation & Start

### Prerequisites
- Python 3.10+
- Node.js (for the Frontend)
- OpenAI API Key

### 1. Setup Backend
1. Navigate to the `backend` folder.
2. Install Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Copy `.env.template` to `.env` and enter your `OPENAI_API_KEY`.
4. Start the server:
   ```bash
   uvicorn main:app --reload
   ```
   *The API server is now running at http://localhost:8000*

### 2. Setup Frontend
1. Navigate to the `frontend` folder.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development environment:
   ```bash
   npm run dev
   ```
   *The interface is now accessible at http://localhost:5173*

### 3. Deployment with Docker (Recommended for Server)
If you want to install the AI on a central company server, Docker is the easiest way:

1.  Ensure **Docker** and **Docker Compose** are installed on the server.
2.  Enter your API Key in `backend/.env`.
3.  Start the entire system with one command:
    ```bash
    docker-compose up -d --build
    ```
4.  The AI is now accessible in the network under the IP address of the server (Port 80 for the interface, Port 8000 for the API).

## 📖 Usage
- **Chat:** Select "New Chat" in the sidebar to start a conversation.
- **Add Knowledge:** Use the "Upload PDF" button to index documents. The AI will automatically include this information in future answers.

> [!WARNING]
> **Copyright Notice**
> The source code of this project is not publicly accessible due to internal company policies.
> This repository only contains a detailed README to document the structure, design, and results of the project.
> All materials are shared exclusively for educational and portfolio purposes.

---

<a id="deutsch"></a>

# AI Assistant für Baubranche 🏗️🤖

Eine intelligente, lokale KI-Lösung, die speziell für die Anforderungen der Baubranche entwickelt wurde. Dieses System kombiniert die Leistungsfähigkeit von GPT-4o mit firmeneigenem Wissen durch RAG (Retrieval-Augmented Generation).

## ✨ Kernfunktionen

- **💬 Intelligenter Chat:** Nutzt GPT-4o für präzise Antworten auf technisches und kaufmännisches Fachwissen.
- **📄 Dokumenten-KI (RAG):** Laden Sie Bauverträge, Angebote oder DIN-Normen (PDF) hoch. Die KI nutzt diese als exklusive Wissensbasis.
- **🗃️ Lokale Historie:** Alle Gespräche werden sicher in einer lokalen SQLite-Datenbank gespeichert.
- **🔒 Datenschutz:** Firmendaten verbleiben auf Ihrem System und werden nur zur Verarbeitung über die API gesendet (kein Training!).
- **🌐 Modernes Interface:** Intuitive Weboberfläche mit Sidebar für die Chat-Historie und Markdown-Unterstützung.

## 🛠️ Technologie-Stack

- **Backend:** FastAPI (Python), SQLAlchemy (SQLite), LangChain, ChromaDB (Vektor-DB).
- **Frontend:** React, Vite, TypeScript, Lucide-React (Icons).
- **KI-Modell:** OpenAI GPT-4o via API.

## 🚀 Installation & Start

### Voraussetzungen
- Python 3.10+
- Node.js (für das Frontend)
- OpenAI API Key

### 1. Backend einrichten
1. Navigieren Sie in den Ordner `backend`.
2. Installieren Sie die Python-Abhängigkeiten:
   ```bash
   pip install -r requirements.txt
   ```
3. Kopieren Sie `.env.template` zu `.env` und tragen Sie Ihren `OPENAI_API_KEY` ein.
4. Starten Sie den Server:
   ```bash
   uvicorn main:app --reload
   ```
   *Der API-Server läuft nun unter http://localhost:8000*

### 2. Frontend einrichten
1. Navigieren Sie in den Ordner `frontend`.
2. Installieren Sie die Abhängigkeiten:
   ```bash
   npm install
   ```
3. Starten Sie die Entwicklungsumgebung:
   ```bash
   npm run dev
   ```
   *Das Interface ist nun unter http://localhost:5173 erreichbar.*

### 3. Deployment mit Docker (Empfohlen für den Server)
Wenn Sie die KI auf einem zentralen Firmen-Server installieren möchten, ist Docker der einfachste Weg:

1.  Stellen Sie sicher, dass **Docker** und **Docker Compose** auf dem Server installiert sind.
2.  Tragen Sie Ihren API-Key in `backend/.env` ein.
3.  Starten Sie das gesamte System mit einem Befehl:
    ```bash
    docker-compose up -d --build
    ```
4.  Die KI ist nun im Netzwerk unter der IP-Adresse des Servers erreichbar (Port 80 für das Interface, Port 8000 für die API).

## 📖 Benutzung
- **Chat:** Wählen Sie "Neuer Chat" in der Sidebar, um ein Gespräch zu beginnen.
- **Wissen hinzufügen:** Nutzen Sie den "PDF hochladen"-Button, um Dokumente zu indizieren. Die KI wird diese Informationen automatisch in zukünftige Antworten einbeziehen.

> [!WARNING]
> **Urheberrechtshinweis**
> Der Quellcode dieses Projekts ist aufgrund interner Unternehmensrichtlinien nicht öffentlich zugänglich.
> Dieses Repository enthält lediglich eine detaillierte README, um die Struktur, das Design und die Ergebnisse des Projekts zu dokumentieren.
> Alle Materialien werden ausschließlich zu Bildungs- und Portfoliozwecken geteilt.
