# 💻 AutoCAD‑LISP – Meine ersten Erfahrungen mit Automatisierung

Dieses Dokument beschreibt meinen persönlichen Weg in die AutoCAD‑Automatisierung mit LISP.  
Ich habe kein Hintergrundwissen in Programmierung – deshalb war dieses Projekt für mich ein echter Lernweg.

---

## 🌱 Warum ich damit angefangen habe

In unserem Arbeitsalltag kommen viele wiederkehrende Aufgaben vor:  
Layouts aktualisieren, Layer umstellen, Daten einfügen, kleine Routinearbeiten.

Diese Dinge kosten Zeit.  
Zeit, die man manchmal anders nutzen will.

Ich hörte dann, dass man AutoCAD mit **LISP** automatisieren kann.  
Ich wusste:

- weder, was LISP ist  
- noch, wie man damit programmiert  
- noch, wie kompliziert das eigentlich ist  

Trotzdem wollte ich herausfinden:

➡️ **Wie weit komme ich mit KI‑Unterstützung?**

---

## ⚙️ Die ersten kleinen Versuche

Ich startete mit einfachen Aufgaben.  
Zum Beispiel:

### ✔️ AnsichtsfensterManager

Hier sollten alle Ansichtsfenster in einer DWG – in allen vorhandenen Layouts – gesperrt oder entsperrt werden.  
Visual Studio schrieb mir dafür eine `.bat`‑Datei und erzeugte sogar einen vollständigen Ordner mit Anleitung und allen erforderlichen Dateiformaten.

Erst später verstand ich, dass das völlig übertrieben war.  
Dadurch wurde:

- sehr viel Leistung abgerufen  
- massiv in AutoCAD eingegriffen  

Und dann habe ich mir Visual Studio „zerstellt“.  
Ich dachte, ich wäre von der IT-Abteilung reglementiert worden, weil ich zu tief ins System eingreife.  
Später stellte sich heraus:

➡️ Ich hatte einfach nur eine Einstellung verändert.  
➡️ Und wieder wurde mir klar: *Wenn ich etwas weiß, dann dass ich nichts weiß.*

Visual Studio führte meine Befehle nicht mehr wie gewohnt automatisch aus, sondern verlangte manuelle Schritte.  

Ich beugte mich der Situation und begann, den Umgang mit LISP wirklich zu lernen.

<img width="1255" height="802" alt="image" src="https://github.com/user-attachments/assets/01f2163e-b1f4-4f32-977a-a60d0582b075" />

---

### ✔️ AllesNachLayer.lsp

**Ausgangssituation:**  
Eine DWG mit über 300 Blöcken, inklusive verschachtelter Blöcke.  
Viele Objekte waren manuell falsch in den Layereinstellungen angepasst.

Ziel war:  
➡️ Alle Objekte automatisch auf den richtigen Layer legen — auch innerhalb der verschachtelten Blöcke.

Copilot half mir, das Skript für die LISP zu erzeugen. und gab mir Anweisungen diese LISP per Appload in AutoCAD zu laden.
Ich verstand nur einen Teil davon – aber es lief.

---

#### ✔️ DatumAktualisieren_AlleLayouts.lsp

**Ausgangssituation:** In einer Zeichnung mit über 20 Layouts existierte ein Stempelfeld als Block mit Attributen. Das Datum sollte bei einem spezifisch definierten Attribut (Tag) überall einheitlich angepasst werden.

**Die Idee:** Ein einziger Befehl, der automatisch alle Layouts durchläuft und den Wert im Attribut aktualisiert, ohne jedes Layout einzeln öffnen zu müssen.

<img width="306" height="842" alt="Screenshot der LISP-Logik" src="https://github.com/user-attachments/assets/64216e91-26b2-4a45-8728-e027d2604341" />
<img width="323" height="552" alt="image" src="https://github.com/user-attachments/assets/11aa6a0a-2870-4bb0-ae3a-efa62f06a7c3" />
<img width="292" height="682" alt="image" src="https://github.com/user-attachments/assets/447df573-754a-4c96-8e67-f6acd50fd1c3" />
<img width="278" height="682" alt="image" src="https://github.com/user-attachments/assets/77a0e2ac-b8db-434c-ab96-f82f5edd02d5" />
<img width="272" height="660" alt="image" src="https://github.com/user-attachments/assets/dec20a2d-83eb-48b4-9211-3ee6bde4e164" />

**Ergebnis - ein kleiner Einblick**

[![Video ansehen](./screenshots/layout_update_thumb.png)](./DatumAktualisieren_AlleLayouts.mp4)

**Die Bilanz der Automatisierung:**

| Methode | Zeitaufwand | Bemerkung |
| :--- | :--- | :--- |
| **Manuelle Anpassung** | ~ 10 Min. | Fehleranfällig bei vielen Layouts |
| **Skript-Erstellung (KI)** | ~ 30 Min. | Einmaliger Lernaufwand ohne Vorkenntnisse |
| **Anwendung der Lisp** | **~ 2 Min.** | Sofortiger Erfolg für alle Layouts |

## 🧠 Erfahrungen mit Copilot

Die Umsetzung war grundsätzlich machbar, aber sie erforderte eine kritische Prüfung der Ergebnisse. Ich habe dabei festgestellt:

- Manche Vorschläge waren unvollständig.
- Copilot hat teilweise Funktionen „erfunden“, die es in LISP gar nicht gibt.
- Einige Befehle passten nicht exakt zu meiner AutoCAD‑Version.
- Damit das LISP zuverlässig funktioniert, müssen **alle Block-Namen und Attribute einheitliche Namen** haben – hier ist also Standardisierung entscheidend.

> **Mein Fazit:** > KI kann die Erstellung von LISP-Routinen massiv unterstützen und Hürden abbauen – aber sie ersetzt nicht das Testen und das grundlegende Verständnis der AutoCAD-Befehle.

---

## 🧩 Wo ich an Grenzen gestoßen bin

Je komplexer das Vorhaben, desto schwieriger wurde es:

- Ich verstand nicht, warum etwas funktionierte oder nicht  
- Copilot schrieb Code, der gut klang, aber in AutoCAD gar nicht existierte  
- Fehlermeldungen waren schwer zu deuten  
- Kleine Änderungen konnten alles kaputt machen  

Ich habe viel ausprobiert und viel verworfen.  
Das gehört dazu.

---

## 🤖 Wie Copilot mir geholfen hat

Copilot war für mich:

- ein Ideengeber  
- ein Startpunkt für neue Befehle  
- ein Werkzeug, das aus meinen Worten LISP‑Code baut  
- eine Art Dolmetscher  

Aber genauso oft war Copilot:

- ungenau  
- verwirrend  
- zu kreativ  
- technisch falsch  

Ich habe gelernt:

> **KI liefert den Rohbau.  
> Verstehen und Anpassen muss ich selbst.**

---

## ⚠️ Wichtige Lektionen aus diesem Projekt


- LISP ist eine eigene kleine Welt  
- AutoCAD reagiert sehr empfindlich auf falsche Befehle  
- KI hilft – aber ersetzt keine Tests und kein Nachdenken  
- Viele Vorschläge muss man korrigieren oder anpassen  
- Ich muss klare und genaue Anweisungen/Prompts geben, sonst wird das Ergebnis unbrauchbar  
- Je besser ich formuliere, desto besser arbeitet Copilot

---

## 🎓 Warum dieses Projekt wichtig für mich war

Dieses Projekt hat mir gezeigt:

- dass ich Automatisierung lernen kann  
- dass ich nicht alles verstehen muss, um anzufangen  
- dass KI mir Mut gemacht hat, Neues auszuprobieren  
- dass Fehler normal sind und zum Lernprozess gehören  
- dass kleine Schritte oft große Wirkung haben  
- **wann ich Visual Studio brauche und wann Copilot mir hilft**  
    - Visual Studio nutze ich, wenn ich etwas ausprobieren, testen oder „anfassen“ möchte  
    - Copilot nutze ich, wenn ich Ideen brauche, Texte besser verstehen will oder einen ersten Vorschlag für Code haben möchte  

Es war kein perfektes Projekt –  
aber ein sehr wertvolles.

---

## ❤️ Fazit

Ich bin keine Programmiererin.  
Aber mit KI habe ich gelernt:

- Dinge zu verstehen, die ich vorher nie verstanden hätte  
- Aufgaben zu automatisieren, die mich sonst Zeit gekostet hätten  
- mutig zu werden bei neuen Themen  

Und genau deshalb dokumentiere ich diesen Weg.
