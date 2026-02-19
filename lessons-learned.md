# 💡 Lessons Learned: KI & Automatisierung

Dieses Dokument fasst meine Erfahrungen mit **GitHub Copilot** und **Visual Studio** zusammen. Es dient als Leitfaden für den realistischen und produktiven Einsatz in unseren Projekten.

---

### 🖥️ Visual Studio: Das Kraftwerk
Visual Studio ist der Ort, an dem die echte Leistung entsteht. Hier erstelle ich direkt Skripte, `.exe`-Dateien oder Apploads.

* **Vorbereitung ist alles:** Bevor ich Visual Studio öffne, muss ich präzise wissen: Was will ich erreichen? Welche Ressourcen brauche ich? Ist die Automatisierung an dieser Stelle wirklich notwendig?
* **Hohe Output-Qualität:** Wenn das Ziel klar definiert ist, ermöglicht Visual Studio eine extrem schnelle Umsetzung komplexer Tools.

---

### 🤖 GitHub Copilot: Der smarte Assistent
Copilot ist ein starkes Werkzeug, aber kein Autopilot. Er liefert den Rohbau, den ich fachlich prüfen muss.

* **Stärken:** Schnelles Vervollständigen von Code, Inspiration für Logik und Beschleunigung von Routineaufgaben.
* **Grenzen:** Copilot kennt unsere internen BIM- oder Fachregeln nicht. Komplexe Abläufe sind oft unvollständig oder fehlerhaft.
* **Prompts:** Gute Ergebnisse erfordern präzise Anweisungen (Kontext, Ziel, Warum).

---

### 🐞 Fehler als Lernchance
Copilot „halluziniert“ manchmal (erfindet Funktionen). Diese Momente sind wertvoll:
* Sie zeigen mir, ob ich die Logik selbst verstanden habe.
* Sie
- komplexe logische Abläufe werden häufig falsch oder unvollständig erzeugt  

**Fazit:**  
Copilot hilft viel – aber nur, wenn man prüft, verbessert und korrigiert.

---

# 🧠 2. Gute Prompts = gute Ergebnisse

Je klarer ich formuliere:

- *was* ich möchte,  
- *warum* ich es brauche,  
- *in welchem Kontext* es genutzt wird,

desto besser funktioniert Copilot.

### Gute Beispiele:
- „Erstelle eine Funktion, die PDF‑Seiten via OCR ausliest und anhand des BIM‑Codes benennt.“  
- „Gib mir eine LISP‑Schleife, die alle Layouts durchgeht und das Datum aktualisiert.“

### Schlechte Beispiele:
- „Schreib mir was für PDFs.“  
- „Mach die DWG‑Z‑Werte.“

**Fazit:**  
Copilot ist umso hilfreicher, je genauer ich meine Anforderungen kenne.

---

# 🐞 3. Fehler von Copilot sind Lernchancen

Copilot macht oft typische Fehler:

- erfindet Funktionen, die nicht existieren („Halluzinationen“)  
- verwechselt Dateistrukturen oder Datentypen  
- schlägt unvollständigen Code vor  
- macht syntaktische Fehler in LISP  
- interpretiert DWG‑Logik falsch  

Diese Fehler helfen mir zu erkennen:

- wie gut ich selbst die Logik verstehe  
- wo ich Anforderungen klarer formulieren muss  
- welche Teile eines Problems KI‑ungeeignet sind  

**Fazit:**  
Fehler = wertvolle Lernmomente.

---

# 🔧 4. Copilot ersetzt kein Fachwissen

Besonders deutlich wird das bei:

- BIM‑Codierung  
- AutoCAD‑Datenanalyse (DWG / Z‑Koordinaten)  
- LISP‑Automatisierung  
- internen AFRY‑Skripten & Abläufen  
- eigenen Projektstrukturen  

Hier kann Copilot unterstützen, aber nicht entscheiden.

**Fazit:**  
Ich muss immer Fachentscheidung treffen – Copilot liefert nur Vorschläge.

---

# 🧩 5. Copilot ist am stärksten bei kleinen Bausteinen

Typische Aufgaben, bei denen Copilot glänzt:

- Schleifen  
- Datenumwandlungen  
- Regex‑Vorschläge  
- Helferfunktionen  
- kleine Python‑Skripte  
- Code‑Refactoring  
- Erklärungen / Kommentare generieren  

**Fazit:**  
Je kleiner und klarer der Codeblock, desto besser Copilot.

---

# ⚙️ 6. Copilot schwächelt bei komplexen Arbeitsprozessen

Besonders schwierig für Copilot:

- Multi‑Step‑Logik  
- Dateistrukturen (DWG, PDFs, interne Formate)  
- Kombination verschiedener Tools (Python + OCR + CAD)  
- mehrere Programme in Serie  
- spezielle Firmenstandards  

Hier liefert Copilot oft nur Teillösungen.

**Fazit:**  
Komplexe Prozesse niemals blind übernehmen – immer prüfen & testen.

---

# 📈 7. Der produktivste Workflow: Mensch + Copilot + Review

Der ideale Ablauf für mich:

1. **Manuell erklären**, was ich brauche  
2. **Copilot generiert Vorschlag**  
3. **Ich prüfe & korrigiere**  
4. **Ich teste**  
5. **Copilot anpassen lassen (Iterationen)**  

So entsteht die **beste Mischung** aus Geschwindigkeit und Qualität.

---

# ❤️ 8. Copilot macht Lernen schneller und motivierender

Meine persönlichen Vorteile:

- schneller Zugang zu Ideen  
- weniger Zeit für Boilerplate  
- mehr Fokus auf fachliche Entscheidungen  
- schnelleres Verständnis neuer Technologien  
- sofortiges Feedback (Try & Error)  
- "Pair Programming" Gefühl  

**Fazit:**  
Copilot ist nicht perfekt, aber er macht Lernen angenehmer und Projekte effizienter.

---

# ✔️ Zusammenfassung

| Bereich | Erkenntnis |
|--------|------------|
| Stärken | Schnelle Codevorschläge, Fehlererklärungen, Refactoring, Routineaufgaben |
| Schwächen | Speziallogik, Firmenprozesse, komplexe Abläufe, DWG/LISP |
| Wichtigster Faktor | Gute Prompts & eigenes Fachwissen |
| Beste Nutzung | Mensch + Copilot + Kontrolle |

---

# 📬 Feedback

Wenn jemand eigene Erfahrungen ergänzen möchte, freue ich mich über ein Issue oder eine Nachricht.
