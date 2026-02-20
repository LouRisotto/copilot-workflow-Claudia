# 🗂️ Projekt: Dateinamen‑Umbenennung nach BIM‑Codierung

**Status:** In Testphase  
**ASK-Modus inkl. Fehlversuch: ca. 1h
**OCR-Umsetzung (Agent):** ca. 1,5 h  
**Tools:** Visual Studio, GitHub Copilot (ASK & AGENT), Python, PowerShell, OCR

---

## 🎯 Ziel

PDF‑Dateien automatisch anhand einer **BIM‑Codierung** im Schriftfeld erkennen und die Datei nach diesem Code **automatisch umbenennen**.  
Beispiel: Aus `Plan_ABC_123.pdf` wird `KDM_LST_2D_.....pdf`.

---

## 🧭 Ausgangslage & Ansatz

### 1) Copilot – ASK‑Modus  
- Ich habe mein Problem in natürlicher Sprache beschrieben (Prompt siehe unten).  
- Copilot hat ein **Python‑Skript** und eine **PowerShell‑Ausführung** erzeugt.

### 2) Problem  
- Die BIM‑Zeile im PDF wurde **nicht erkannt**.  
- Grund: Der Text im Schriftfeld war **kein echter Text**, sondern ein **Bild** → reiner PDF‑Text‑Extrakt schlug fehl.

### 3) Zweiter Versuch – Copilot AGENT‑Modus  
- Aufgabe neu formuliert.  
- Fokus auf **OCR** (Texterkennung aus Bildern).  
- Aktuell befinde ich mich in der **Testphase**.

---

## ✍️ Meine Prompts (ASK‑Modus)

> *Der Original‑Prompt lautet:*

Ich habe 24 PDF dateien. In der PDF ist ein Bezeichnung im feld BIM-Datenkodierung angegeben. Die BIM-Datenkodierung muss der Dateiname der PDF sein. 
Wie bekomme ich eine Lösung ohne manuell anpassungen?


### Copilot‑Antwort (Kurzfassung)

<img width="952" height="712" alt="image" src="https://github.com/user-attachments/assets/8e9f105c-59a5-4e34-b906-908d6f19852e" />
<img width="968" height="635" alt="image" src="https://github.com/user-attachments/assets/2fcb20b2-315a-4eb7-8b70-ef3028b93eea" />
<img width="930" height="667" alt="image" src="https://github.com/user-attachments/assets/1f3c5222-b237-4dcf-bae3-6324780cf5de" />

**Ergebnis:**  
- Die BIM‑Zeile wurde nicht gefunden  
- Vermutung: Der Text ist **eingebettet als Bild** → **OCR notwendig**

<img width="931" height="679" alt="image" src="https://github.com/user-attachments/assets/1476fa30-4beb-4fec-8817-eef974ddc964" />

---

## 🔁 Zweiter Anlauf (AGENT‑Modus)

> *(Der Original‑Prompt lautet:)*

Beispiel: Mein Freund, ich habe eine dwg, ich plotte den Plan in PDF. Im Plan befindet sich unten rechts ein Stempelfeld mit vielen Angaben. Unter anderem ist eine BIM-Datencodierung enthalten. Die BIM-Datencodierung hat die Struktur KDM_LST_2D_3_N_TLS-LP_006. Der Code steht eine Zeile unterhalb „BIM-Datencodierung“. Ich möchte ein Skript, das die PDF liest und die Datei automatisch nach diesem Code umbenennt. Jeder Code muss zusätzlich auf .Signallageplan enden.

<img width="1546" height="840" alt="image" src="https://github.com/user-attachments/assets/a1f2510a-ccf8-4821-8b31-7f99b0f01718" />

**Zielanpassung:**

- Falls Text‑Extrakt scheitert → **OCR** nutzen  
- OCR: `pytesseract` + `pdf2image`  
- Fokus auf typische Muster („BIM‑Codierung“)  
- Einsatz eines **klaren Regex‑Patterns**

**Arbeitsstand: Testphase**

- OCR erkennt die relevanten Zeilen **besser**, aber noch nicht **zuverlässig**  
- Abhängig von:
  - Scan‑Qualität  
  - Schriftart  
  - Kontrast  
  - Drehungen  
  - grauen Kästen / Stempelhintergründen  

---

## 🧪 Technik‑Notizen (kurz & verständlich)

- Text‑Extraktion funktioniert nur, wenn der Text **echter Text** im PDF ist  
- Schriftfeld ist häufig ein **Bild** → nur OCR kann es lesen  
- OCR wird besser mit:
  - 300–400 DPI  
  - Schwarz/Weiß‑Kontrast  
  - zugeschnittenem Bereich (nur Schriftfeld)  
  - sauberem Regex‑Pattern  

---

## 🧷 Beispiel‑Regex (Platzhalter)

Dieser Regex trifft BIM‑ähnliche Codes besser als der einfache Standard:

```python
pattern = re.compile(r"[A-Za-z]{2,4}_[A-Za-z0-9]{3,5}-[A-Za-z0-9]{2,4}_[A-Za-z0-9]{2,4}")

<img width="1852" height="808" alt="image" src="https://github.com/user-attachments/assets/c8dd3425-3f69-4b2f-a019-156ed542e5d5" />
