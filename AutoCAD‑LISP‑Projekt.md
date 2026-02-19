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
Ich dachte zuerst, KI wäre schuld — dabei war ich es selbst.

Ich beugte mich der Situation und begann, den Umgang mit LISP wirklich zu lernen.

---

### ✔️ AllesNachLayer.lsp

**Ausgangssituation:**  
Eine DWG mit über 300 Blöcken, inklusive verschachtelter Blöcke.  
Viele Objekte waren manuell falsch in den Layereinstellungen angepasst.

Ziel war:  
➡️ Alle Objekte automatisch auf den richtigen Layer legen — auch innerhalb der verschachtelten Blöcke.

Copilot half mir, die Grundstruktur zu erzeugen.  
Ich verstand nur einen Teil davon – aber es lief.

---

### ✔️ DatumAktualisieren_AlleLayouts.lsp

**Ausgangssituation:**  
Über 20 Layouts mit Stempelfeld und Block mit Attributen.  
Das Datum sollte überall einheitlich geändert werden.

Die Idee:  
➡️ Alle Layouts automatisch durchgehen lassen und das Datum aktualisieren.

<img width="306" height="842" alt="image" src="https://github.com/user-attachments/assets/64216e91-26b2-4a45-8728-e027d2604341" />
<img width="306" height="842" alt="image" src="https://github.com/user-attachments/assets/64216e91-26b2-4a45-8728-e027d2604341" />

Mit KI war das grundsätzlich machbar – aber:

- manche Vorschläge waren unvollständig  
- manchmal erfand Copilot Funktionen  
- manchmal passten Befehle nicht zu AutoCAD  

Ich merkte schnell:

➡️ **KI kann LISP unterstützen – aber nicht ohne Fehler.**

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
