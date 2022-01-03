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
