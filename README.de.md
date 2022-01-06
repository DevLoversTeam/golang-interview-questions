**Read in other languages: [English 🇺🇸](README.en.md),
[Polska 🇵🇱](README.pl.md), [German 🇩🇪](README.de.md), [French 🇫🇷](README.fr.md),
[Spanish 🇪🇸](README.es.md), [Українська 🇺🇦](README.md).**

<h1>
  Go <img src="./assets/go.svg" width="40" height="40" />
</h1>


<details>
<summary>1. Was ist Go und für welche Aufgaben wurde es entwickelt?</summary>

#### Go

Go (oder Golang) ist eine kompilierte, statisch typisierte Programmiersprache,
die bei Google von Robert Griesemer, Rob Pike und Ken Thompson entwickelt wurde.
Bei ihrer Entwicklung standen Einfachheit, Vorhersagbarkeit, schnelle
Kompilierung und hohe Leistung in Produktivsystemen im Mittelpunkt.

#### Für welche Aufgaben wurde Go entwickelt:

1. **Netzwerk- und Serversysteme:** HTTP-/API-Dienste, Proxys, Gateways und
   Backends für hoch belastete Anwendungen.

2. **Cloud-Infrastruktur:** Werkzeuge für Orchestrierung, CI/CD, Observability
   und DevOps (deshalb sind viele Cloud-Native-Projekte in Go geschrieben).

3. **Nebenläufige Berechnungen:** Aufgaben, bei denen die parallele
   Datenverarbeitung, die Kontrolle der Latenz und eine effiziente
   Ressourcennutzung wichtig sind.

4. **Anwendungsnahe Systemprogrammierung:** CLI-Werkzeuge, Daemons,
   Hintergrund-Worker und Integrationsdienste.

#### Warum gerade Go:

- Prägnante Syntax und geringe kognitive Komplexität des Codes.
- Integriertes Nebenläufigkeitsmodell (`goroutine`, `channel`).
- Schnelle Kompilierung und ein einfacher Entwicklungszyklus.
- Praktische Standardwerkzeuge (`go test`, `go vet`, `pprof`, Module).

Go wurde somit als praxisorientierte Programmiersprache für skalierbare,
wartbare und leistungsfähige Dienste entwickelt, bei denen Zuverlässigkeit,
Entwicklungsgeschwindigkeit und betriebliche Einfachheit entscheidend sind.

</details>


<details>
<summary>2. Was sind die grundlegenden Designprinzipien der Sprache Go?</summary>

#### Go

Das Design von Go basiert nicht auf maximaler „Ausdruckskraft“ um jeden Preis,
sondern auf technischer Machbarkeit: Der Code muss leicht lesbar, leicht zu
warten und über den langen Lebenszyklus des Systems zuverlässig sein.

#### Grundlegende Prinzipien des Go-Designs:

1. **Einfachheit statt Komplexität:** Die Sprache vermeidet bewusst übermäßig
   komplexe Konstruktionen, um die Anzahl der Fehler und die Eintrittsschwelle
   in die Codebasis zu verringern.

2. **Lesbarkeit und Eindeutigkeit:** Klarer Code, der von jedem Ingenieur im
   Team, nicht nur vom Autor, schnell verstanden werden kann, wird bevorzugt.

3. **Schnelle Kompilierung und produktive Entwicklung:** Der Zyklus „Schreiben →
   Erstellen → Testen“ sollte kurz sein, was die Iterationen in realen Projekten
   beschleunigt.

4. **Integrierte Nebenläufigkeit:** `goroutine` und `channel` sind ein
   organischer Teil der Sprache, kein externer Patch, daher wird paralleles
   Rechnen nativ unterstützt.

5. **Komposition statt schwerer Hierarchie:** In Go herrscht der Ansatz vor,
   „Verhalten aus einfachen Teilen zusammenzusetzen“, anstatt tiefe
   Vererbungshierarchien aufzubauen.

6. **Minimalismus in den Funktionen, Maximalismus in der Praktikabilität:**
   weniger „Magie“, vorhersehbareres Verhalten während der Ausführung und beim
   Debuggen.

7. **Einheitlicher Werkzeugstandard:** `go fmt`, `go test`, `go mod`, `go vet`
   bilden eine gemeinsame Entwicklungskultur ohne Werkzeugfragmentierung.

#### Verallgemeinerung:

Go ist als Sprache für Teamentwicklung und industrielle Programmierung
konzipiert: Sie diszipliniert den Stil, fördert die Klarheit des Denkens im Code
und bietet eine gute Balance zwischen Einfachheit und Effizienz.

</details>


<details>
<summary>3. Was sind die Hauptmerkmale von Go im Vergleich zu anderen Sprachen?</summary>

#### Go

Go zeichnet sich dadurch aus, dass es eine prägnante Syntax mit einem sehr
praktischen Engineering-Ausführungsmodell kombiniert: Die Sprache überlastet den
Entwickler nicht mit unnötiger Komplexität, sondern stellt Werkzeuge für den
Aufbau schneller und zuverlässiger Systeme bereit.

#### Hauptmerkmale von Go:

1. **Einfache und strenge Syntax:** Code ist leicht zu lesen und die
   stilistische Einheitlichkeit wird automatisch über `go fmt` gewahrt.

2. **In eine native Binärdatei kompilieren:** Eine Anwendung wird normalerweise
   in eine einzelne ausführbare Datei ohne große externe Abhängigkeiten beim
   Start kompiliert.

3. **Statische Typisierung mit hoher Vorhersagbarkeit:** Ein erheblicher Teil
   der Fehler wird in der Kompilierungsphase erkannt, was die Zuverlässigkeit in
   der Produktion erhöht.

4. **Eingebaute Parallelität:** `goroutine` und `channel` machen die parallele
   Programmierung zu einem natürlichen und nicht zu einem Hilfsmechanismus.

5. **Schneller Entwicklungszyklus:** Relativ schnelle Kompilierung und
   Standardtools beschleunigen das Testen und die Bereitstellung von Änderungen.

6. **Starke Standardbibliothek:** Netzwerk, HTTP, Kryptografie, Dateiverwaltung,
   Profilerstellung und Tests sind sofort verfügbar.

7. **Klares Fehlermodell:** In Go werden Fehler explizit über `error` behandelt,
   wodurch die Zustandskontrolle transparent und kontrollierbar wird.

8. **GC und verwalteter Speicher:** Die Sprache vereinfacht die
   System-Backend-Entwicklung, ohne dass Sie den Lebenszyklus der meisten
   Objekte manuell verwalten müssen.

9. **Ein praktischer modularer Ansatz:** `go mod` standardisiert das
   Abhängigkeitsmanagement und die Build-Reproduzierbarkeit.

#### Fazit:

Im Gegensatz zu vielen Sprachen, die entweder auf maximale Abstraktion oder auf
niedrige Kontrollierbarkeit ausgerichtet sind, sorgt Go gezielt für ein
technisches Gleichgewicht aus Einfachheit, Leistung, Skalierbarkeit und Komfort
bei der Teamentwicklung.

</details>


<details>
<summary>4. Was ist der Unterschied zwischen imperativem und deklarativem Programmierparadigma? Nennen Sie Beispiele für Sprachen.</summary>

#### Go

Imperative und deklarative Paradigmen unterscheiden sich hauptsächlich im Fokus
der Beschreibung: Das erste erklärt, **wie** die Aufgabe Schritt für Schritt
ausgeführt wird, das zweite – **was genau** als Ergebnis erzielt werden soll.

#### Imperatives Paradigma:

1. **Essenz:** Der Programmierer gibt explizit die Reihenfolge der Anweisungen,
   Zustandsübergänge, Schleifen, Verzweigungen und die Ausführungsreihenfolge
   an.

2. **Schwerpunkt:** Algorithmuskontrolle und Ausführungsflusskontrolle.

3. **Typische Merkmale:** Variablen, Zuweisungen, `for`, `if`, Datenmutation.

4. **Beispiele für Sprachen:** Go, C, C++, Rust (in den meisten Praktiken),
   Java.

#### Deklaratives Paradigma:

1. **Essenz:** beschreibt das gewünschte Ergebnis oder die gewünschten
   Eigenschaften des Systems, ohne die Implementierungsschritte im Detail zu
   beschreiben.

2. **Fokus:** Datenmodell, Regeln und Einschränkungen, nicht algorithmische
   Mechanik.

3. **Typische Merkmale:** Ausdrücke auf höherer Ebene, Minimierung expliziter
   Mutationen, Abstraktion von der Ausführungsreihenfolge.

4. **Beispiele für Sprachen/Ansätze:** SQL, HCL (Terraform), HTML/CSS,
   funktionale Stile in Haskell und teilweise in Elixir.

#### Praktisches Fazit:

- In realen Systemen werden Paradigmen häufig kombiniert. - Go ist meist
  zwingender Natur, einige deklarative Elemente kommen jedoch in
  Konfigurationen, Schemabeschreibungen, DSLs und Datenabfragen vor. - Für das
  Interview ist es wichtig zu betonen: Die Wahl eines Paradigmas ist keine Frage
  von „besser oder schlechter“, sondern eine Frage der Übereinstimmung mit der
  Aufgabe, dem Team und den Anforderungen an die Codeunterstützung.

</details>


<details>
<summary>5. Warum eignet sich Go zum Schreiben von Cloud Native-Diensten?</summary>

#### Go

Go gilt nicht umsonst als eine der natürlichsten Sprachen für Cloud Native:
Seine architektonischen Eigenschaften passen gut zu den Anforderungen moderner
verteilter Systeme – Skalierbarkeit, Beobachtbarkeit, Zuverlässigkeit und
betriebliche Einfachheit.

#### Warum Go in einer Cloud Native-Umgebung effektiv ist:

1. **Leichtes Competitive Computing:** `goroutine` und `channel` vereinfachen
   den Aufbau von Diensten, die eine große Anzahl von Anfragen gleichzeitig
   verarbeiten.

2. **Hohe Leistung und vorhersehbare Laufzeit:** Der Go-Compiler und der
   optimierte Scheduler funktionieren gut in stark ausgelasteten
   Netzwerkszenarien.

3. **Schnellstart und Bereitstellung**: Typischerweise ist das Ergebnis eines
   Builds eine einzelne Binärdatei, die einfach zu containerisieren und auf
   Kubernetes oder anderen Orchestratoren bereitzustellen ist.

4. **Geringer Betriebsaufwand:** Einfache Docker-Images, schneller Build,
   weniger Abhängigkeitsprobleme beim Start.

5. **Leistungsstarke Standardbibliothek:** `net/http`, `context`, `crypto`,
   `encoding` und andere Pakete ermöglichen Ihnen die Erstellung von
   Produktionslösungen ohne übermäßige Abhängigkeit von Frameworks von
   Drittanbietern.

6. **Komfort von Observability-Praktiken:** In Go ist es einfach, Metriken,
   Nachverfolgung und Profilerstellung zu integrieren, was für die Nutzung in
   der Cloud von entscheidender Bedeutung ist.

7. **Resistentes Ökosystem von Infrastruktur-Tools:** Ein erheblicher Teil des
   Cloud Native-Stacks ist speziell auf Go geschrieben (z. B. Kubernetes,
   Prometheus, Helm, Terraform), was Integrationen und Befehlskontext
   vereinfacht.

8. **Codeklarheit in der Teamentwicklung:** Go fördert unkomplizierte Lösungen,
   was die kognitive Belastung durch die Unterstützung einer
   Microservice-Architektur verringert.

#### Zusammenfassung:

Go eignet sich gut für Cloud Native-Dienste, da es technische Vorhersehbarkeit
mit Leistung und praktischem Komfort kombiniert: vom Schreiben des Codes bis hin
zu seiner Bereitstellung, Überwachung und langfristigen Unterstützung.

</details>


<details>
<summary>6. Was sind `shadowing`-Variablen und wie können sie Fehler in der Geschäftslogik verursachen?</summary>

#### Go

`Shadowing` (Shadowing) liegt vor, wenn im inneren Bereich eine neue Variable
mit demselben Namen wie die äußere deklariert wird. Dadurch funktioniert der
Code nicht mit der „erwarteten“ Variable, sondern mit ihrer namentlich genannten
lokalen Kopie.

#### Wie es am häufigsten vorkommt:

1. **Kurze Deklaration von `:=` in einem verschachtelten Block:** Der Entwickler
   erwartet eine Zuweisung, und tatsächlich wird eine neue Variable erstellt.

2. **Fehlerbehandlung (`err`) in `if`/`for`/`switch`:** Das lokale `err`
   überschattet das externe, was dazu führt, dass die nachfolgende Statusprüfung
   falsch ist.

3. **Arbeiten mit Zuständen in langen Funktionen:** Das Schattieren von
   Zwischenvariablen erschwert das Lesen und erhöht das Risiko logischer Fehler.

#### Warum dies für die Geschäftslogik gefährlich ist:

1. **Falsche Bedingungsprüfungen:** Das System geht möglicherweise zum falschen
   Ausführungszweig, weil die „falsche“ Variable überprüft wird.

2. **Verlorener oder falscher Status:** Das Berechnungsergebnis blieb
   beispielsweise im lokalen Block und der externe Status wurde nicht
   aktualisiert.

3. **Komplexes Debugging:** Optisch ist der Name derselbe, aber semantisch
   handelt es sich um unterschiedliche Objekte. Der Fehler macht sich
   unauffällig und oft nur in Kampffällen bemerkbar.

4. **Stille Fehler ohne Panik:** Ein Programm kann kompiliert und ausgeführt
   werden, liefert jedoch ein geschäftsunkorrektes Ergebnis.

#### So verhindern Sie `shadowing`:

- Unterscheiden Sie bewusst zwischen `=` und `:=` in allen verschachtelten
  Blöcken. - Halten Sie variable Sichtverhältnisse kurz und vermeiden Sie zu
  lange Funktionen. - Verwenden Sie klare, semantisch korrekte Namen,
  insbesondere für Zustände und Fehler. - Verbinden Sie die statische Analyse
  (`go vet`, `golangci-lint`) mit Regeln zur Schattierungserkennung. - Fügen Sie
  an kritischen Stellen der Logik Tests für negative Szenarien und
  Randbedingungen hinzu.

#### Fazit:

`Shadowing` ist keine syntaktische Eigenart, sondern eine Quelle heimtückischer
Logikfehler. Im Produktions-Go-Code wirkt sich die Disziplin der
Variablendeklaration direkt auf die Korrektheit des Geschäftsverhaltens des
Systems aus.

</details>
