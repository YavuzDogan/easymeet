# easymeet.ai (Arbeitstitel)

**KI-gestützte, multimodale Terminfindung für Gruppen mit komplexen Zeitplänen.**

easymeet.ai ermöglicht es Teilnehmern, ihre Verfügbarkeit auf verschiedene Arten anzugeben:
- Klickbare Kalender-UI (Tage/Zeitfenster markieren)
- Freitext im Chat („kann nur ab 19 Uhr“)
- Foto-Upload von Schichtplänen oder Papierkalendern

Das System interpretiert alle Eingaben, führt sie in einer gemeinsamen Ansicht zusammen und berechnet mithilfe einer gewichteten Optimierung die besten Terminvorschläge.  
Optional können die Vorschläge zur Abstimmung an die Gruppe geschickt werden.

## Kernfunktionen
- **Multimodale Eingabe**: Kalender, Text, Foto
- **Selbsteinstufung** der Teilnehmer (🚨 Muss dabei sein / 🙂 Gern dabei / 😴 Optional)
- **Optimierungs-Algorithmus** mit Gewichtung, Hard-/Soft-Constraints und Teilverfügbarkeiten
- **Heatmap-Dashboard** für Organisatoren
- **Optionale Voting-Runde** für höhere Akzeptanz
- **Viralitätselemente**: Live-Heatmap, Fun-Facts, KI-Kommentare, Memes

## Tech-Stack
- **Frontend**: WeWeb
- **Backend**: Python + FastAPI
- **Datenbank**: Supabase (Postgres)
- **Automationen**: n8n
- **Deployment**: Railway/Fly/Render (API), WeWeb Hosting (Frontend)

## Projektstruktur
- easymeet/
- api/ # FastAPI Backend
- infra/sql/ # Supabase-Schema & SQL-Skripte
- n8n/ # exportierte n8n Workflows
- prompts/ # LLM-Promptvorlagen
- docs/ # Projekt-Dokumentation

## Entwicklung
1. `.env` Datei mit Supabase- und API-Keys erstellen (nicht in Git einchecken!)
2. Virtuelle Umgebung anlegen:
   ```bash
   python -m venv .venv
   . .venv/bin/activate   # Windows: .\.venv\Scripts\activate
   pip install -r requirements.txt
3. API starten:
   uvicorn api.main:app --reload --port 8000

## Lizenz
Dieses Projekt steht unter keiner öffentlichen Lizenz und darf nur mit Genehmigung des Autors genutzt werden.