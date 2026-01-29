# KI Assistant für Baubranche 🏗️🤖

Eine intelligente, lokale KI-Lösung, die speziell für die Anforderungen der Baubranche entwickelt wurde. Dieses System kombiniert die Leistungsfähigkeit von GPT-4o mit firmeneigenem Wissen durch RAG (Retrieval-Augmented Generation).

## ✨ Kernfunktionen

- **💬 Intelligenter Chat:** Nutzt GPT-4o für präzise Antworten auf technisches und kaufmännisches Fachvissen.
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

---

*Entwickelt für Kranz Engineering - Effizienz am Bau durch KI.*
