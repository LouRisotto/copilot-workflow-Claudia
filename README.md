# copilot-workflow-Claudia
Meine Erfolge und Herausforderungen
# 🚀 Copilot-Erfahrungen – Erfolge & Herausforderungen

Dieses Repository dokumentiert meine persönlichen Erfahrungen mit **GitHub Copilot** in Kombination mit **Visual Studio**.  
Es dient als Praxisbeispiel für eine interne Schulung in unserem Unternehmen – mit einem ehrlichen Blick auf:

- ✔️ funktionierende Copilot-Vorschläge  
- ⚠️ fehlerhafte oder unbrauchbare Vorschläge  
- 🔧 eigene Lösungswege  
- 📉 typische Hürden im Alltag  
- 📈 Lern- und Verbesserungsprozesse  

Ziel ist es, transparent zu zeigen, wie Copilot **unterstützen**, aber auch **fehlleiten** kann – und wie ich als technische Systemplanerin produktiv damit arbeite.

---

# 📂 Struktur des Repositories
/success → Beispiele erfolgreicher Copilot-Unterstützung
/failures → Situationen …
/manual-fixes → …
/screenshots → …
lessons-learned.md → …

---

# 📘 Übersicht der bisherigen Projekte

Im Folgenden sind die Projekte aufgeführt, die im Workspace bzw. im bisherigen Verlauf gemeinsam entstanden sind.  
Sie bilden die praktische Grundlage für viele Beispiele dieses Repositories.

---

## 1. 🔄 Automatisches Umbenennen von PDF-Dateien nach BIM-Datencodierung  
**Datei:** `rename_bim_pdf.py`  

**Ziel:**  
PDF-Dateien automatisch anhand eines im Dokument enthaltenen BIM‑Codes erkennen und korrekt umbenennen.

**Technologien:**  
- Python  
- pypdf  
- OCR (pytesseract, pdf2image, Pillow)

**Status:**  
- ❌ erster Ansatz (pypdf Textauslesen) fehlgeschlagen  
- ✔️ zweiter Ansatz mit OCR erfolgreich  
- 🔧 aktuell in Überarbeitung

---

## 2. 🧰 Python-Skripte im Ordner **AFRY_Einarbeitung**

**Beispiele:**  
- `convert_json.py`  
- `extrahiere_dokumente.py`  
- `fix_quiz.py`  
- `restructure.py`  
- `remove_tag10.py`  

**Ziel:**  
Automatisierung und Datenaufbereitung für Einarbeitungs- und Schulungsunterlagen.

**Hintergrund:**  
Viele Skripte entstanden mit Copilot-Unterstützung – teils erfolgreich, teils fehlerhaft → ideale Lernbeispiele.

---

## 3. 📐 DWG-Koordinaten- und Z-Check  
**Dateien:**  
- `dwg_z_koordinaten.py`  
- `dwg_z_check.py`

**Ziel:**  
Auswertung, Prüfung und Analyse von AutoCAD-Daten (insbesondere Z‑Koordinaten).

**Besonderheit:**  
Copilot liefert hier oft fehlerhafte Annahmen, da DWG‑Strukturen komplex sind → wertvolle Fehler- und Lernbeispiele.

---

## 4. 💻 AutoCAD-Automatisierung (LISP)  
**Ordner:** `/LISP`  

**Beispiele:**  
- `AllesNachLayer.lsp`  
- `DatumAktualisieren_AlleLayouts.lsp`

**Ziel:**  
Automatisieren wiederkehrender Aufgaben in AutoCAD.

**Beobachtung:**  
Copilot ist hier hilfreich für einfache Strukturen, macht aber oft syntaktische Fehler → gute Demonstration der Grenzen von KI.

---

# 🧩 Inhalt & Beispiele im Repository

### ✔️ Erfolgreiche Beispiele (Ordner: *success*)
- korrekt generierte Python-Funktionen  
- funktionierende OCR-Workflows  
- sinnvolle Refactorings  
- Zeiteinsparungen durch Code-Vervollständigungen  

---

### ⚠️ Herausforderungen (Ordner: *failures*)
- fehlerhafte Code-Vorschläge  
- nicht existierende Funktionen („Halluzinationen“)  
- unvollständige Python-Logik  
- AutoCAD-/LISP-Fehler aufgrund unpräziser Kontexte  

---

### 🔧 Manuelle Lösungen (Ordner: *manual-fixes*)
- komplett überarbeitete Copilot-Vorschläge  
- manuell korrigierte Fehler  
- Gegenüberstellungen *Copilot-Version vs. finale Version*  

---

# 💡 Lessons Learned (Auszug)

- Gute Ergebnisse entstehen nur mit **klaren, präzisen Prompts**.  
- Copilot ist eine Unterstützung – ersetzt aber kein Fachwissen.  
- Fehler des Copilots sind wertvolle Lerngelegenheiten.  
- Für komplexe Aufgaben liefert Copilot oft Teillösungen, aber keine vollständigen.  
- Produktiver Einsatz entsteht im Zusammenspiel:  
  **Menschliche Expertise + KI-Unterstützung + kritische Prüfung**

---

# 👤 Über dieses Projekt

Ich dokumentiere hier praxisnah meine Erfahrungen im Umgang mit GitHub Copilot, Visual Studio und verschiedenen Automatisierungsprojekten.  
Dieses Repository soll Kolleginnen und Kollegen helfen, Copilot realistisch einzuschätzen und produktiv einzusetzen.

Das Repository ist **privat**, aber zur internen Schulung freigegeben.

---

# 📬 Feedback & Zusammenarbeit

Wer Hinweise, Ergänzungen oder eigene Beispiele beitragen möchte, kann gerne ein Issue erstellen oder mich direkt kontaktieren.
