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


<details>
<summary>7. Warum `struct{}` (eine leere Struktur) verwenden und in welchen Szenarien ist es effektiv?</summary>

#### Go

`struct{}` in Go ist eine leere Struktur, also ein feldloser Typ. Seine
Haupteigenschaft: Es trägt keine Datennutzlast, sondern zeichnet lediglich die
Tatsache der Existenz eines Werts oder Ereignisses auf.

#### Warum `struct{}` wirksam ist:

1. Der Typ **Null Informationsvolumen:** enthält keine Felder und wird daher als
   Token und nicht als Datencontainer verwendet.

2. **Klare Absichtssemantik:** Der Code zeigt explizit, dass die Tatsache
   „ist/ist nicht“ wichtig ist, nicht die Nutzlast.

3. **Redundante Zuordnungen in Servicestrukturen reduzieren:** In vielen Mustern
   ist dies eine praktischere Wahl als `bool` oder beliebige Werte, wenn Daten
   nicht benötigt werden.

#### Typische Nutzungsszenarien:

1. **Set über `map[K]struct{}`:** `map` in Go ist ein Schlüsselwert, und für
   einen Satz benötigen wir nur eindeutige Schlüssel. `struct{}` bedeutet hier
   idealerweise „Schlüssel vorhanden“.

2. **Signalkanäle `chan struct{}`:** werden für die Benachrichtigung „Ereignis
   eingetreten“ (Stop/Fertig/Herunterfahren) verwendet, wenn keine
   Datenübertragung erforderlich ist.

3. **Token-Typen und API-Verträge:** Eine leere Struktur kann als leichtes
   semantisches Token in den internen Protokollen der Anwendung fungieren.

4. **Einbettung der Verhaltenskomposition:** `struct{}` wird manchmal als
   technisches Kompositionselement verwendet, wenn eine zustandslose Struktur
   erforderlich ist.

#### Wann nicht verwendet werden sollte:

– Wenn der tatsächliche Zustand oder die tatsächlichen Attribute einer Entität
erforderlich sind. - Wenn `bool` eine klarere Geschäftssemantik liefert (z. B.
ein explizites Bedingungsflag anstelle einer festgelegten Tatsache).

#### Zusammenfassung:

`struct{}` ist ein Werkzeug mit präziser Absicht: Wenn keine Daten benötigt
werden, aber eine Tatsache, Präsenz oder ein Signal angezeigt werden muss, ist
eine leere Struktur eine elegante und effiziente Lösung im Go-Code.

</details>


<details>
<summary>8. Wie funktioniert die interne Struktur `slice` und was passiert, wenn Sie sie an eine Funktion übergeben?</summary>

#### Go

In Go ist `slice` nicht das Array selbst, sondern ein leichter
„Add-on“-Deskriptor über einem Abschnitt des Arrays. Aus diesem Grund
unterscheidet sich das Verhalten von `slice` vom normalen Array-Kopieren und
führt häufig zu Fehlern in Interviews und echtem Code.

#### Internes Modell `slice`:

`slice` besteht konzeptionell aus drei Teilen:

1. **Zeiger auf Basisarray** (`ptr`)

2. **Länge** (`len`) – wie viele Elemente jetzt verfügbar sind

3. **Kapazität** (`cap`) – wie viele Elemente bis zur Grenze des Basisarrays
   verfügbar sind

Das heißt, `slice` speichert Metadaten über die Region im Speicher, anstatt alle
Elemente zu duplizieren.

#### Was passiert, wenn Sie `slice` an eine Funktion übergeben:

1. **Der Header `slice` (ptr/len/cap) wird kopiert, nicht das gesamte Array.**

2. **Beide Parteien (Anrufer und Angerufener) betrachten zunächst dasselbe
   Basisarray.**

3. **Das Ändern von Elementen über den Index** (`s[i] = ...`) in der Funktion
   ist normalerweise von außen sichtbar, da die Daten des gemeinsam genutzten
   Arrays geändert werden.

4. **Das Ändern des Headers selbst** (`s = s[:n]`, `s = append(...)`) in einer
   Funktion ändert den Header im Aufrufer nicht, es sei denn, Sie geben einen
   neuen `slice` zurück.

#### Wichtige Nuance mit `append`:

- Wenn `cap` während `append` ausreicht, geht der Eintrag in dasselbe
  Basisarray.

- Wenn `cap` fehlt, weist die Laufzeit ein neues Array zu, kopiert die Daten
  dorthin und der lokale `slice` in der Funktion beginnt, auf einen anderen
  Speicher zu verweisen.

Nach `append` kann die Funktion also bereits mit dem neuen Array arbeiten,
während das alte `slice` draußen bleibt, wenn der neue Wert nicht zurückgegeben
wird.

#### Praktisches Fazit:

- Möchten Sie die Elemente ändern? Sie können `slice` unverändert übergeben.

- Möchten Sie die Länge/Kapazität oder das Ergebnis von `append` ändern – geben
  Sie das aktualisierte `slice` von der Funktion zurück (oder übergeben Sie
  einen Zeiger auf `slice`, wenn dies architektonisch wirklich gerechtfertigt
  ist).

#### Beispiel:

```go
package main

import "fmt"

func grow(s []int) {
	s = append(s, 99) // змінюємо локальний заголовок slice
}

func mutate(s []int) {
	s[0] = 42 // змінюємо спільний базовий масив
}

func main() {
	s := []int{1, 2, 3}
	mutate(s)
	grow(s)
	fmt.Println(s) // [42 2 3], append у grow не змінив заголовок у викликачі
}
```

</details>


<details>
<summary>9. Warum ist `make([]T, 0, n)` angesichts der bekannten Abmessungen besser als `var s []T`?</summary>

#### Go

Wenn Sie die ungefähre oder genaue Anzahl der Elemente im Voraus kennen, ist das
Konstrukt `make([]T, 0, n)` fast immer praktischer als `var s []T`, da es sofort
die erforderliche Kapazität reserviert und die Anzahl der Speicherneuzuweisungen
reduziert.

#### Was diese beiden Ansätze unterscheidet:

1. **`var s []T`**

- erstellt `nil`-Slice aus `len=0`, `cap=0`;

- das erste `append` bewirkt, dass die Laufzeit Speicher zuweist;

- Wenn die Daten wachsen, kommt es zu neuen Neuzuweisungen und Kopien.

2. **`make([]T, 0, n)`**

- erstellt ein Slice aus `len=0`, aber bereits aus `cap=n`;

- Elemente werden über `append` ohne Neuzuweisung hinzugefügt, bis `cap`
  erschöpft ist;

- weniger Datenkopien und stabilere Leistung.

#### Warum es in der Praxis wichtig ist:

1. **Weniger Zuweisungen im Heap:** reduziert die GC-Last.

2. **Besseres Latenzverhalten:** weniger „Sprünge“ in der Neuzuweisungszeit.

3. **Höherer Durchsatz in Hot Paths:** insbesondere in Schleifen, Parsing,
   Aggregation, Serialisierung.

4. **Ressourcenvorhersagbarkeit:** einfachere Speicherschätzung für ein
   bestimmtes Szenario.

#### Wenn der Unterschied besonders auffällig ist:

- Große Anzahl von `append` in Schleifen.

- Verarbeitung von Datenströmen in Backend-Diensten.

- Häufig aufgerufene Funktionen, bei denen selbst kleine Zuweisungen zu
  erheblichen Kosten führen.

#### Fazit:

Wenn die Größe der Sammlung im Voraus bekannt ist oder gut geschätzt wird, ist
`make([]T, 0, n)` eine technisch ausgereifte Wahl: Sie bietet weniger
Zuweisungen, bessere Leistung und ein stabileres Verhalten unter Last.

</details>


<details>
<summary>10. Wie steuert ein Slice-Ausdruck `a[low:high:max]` `cap` ein neues Slice?</summary>

#### Go

In Go können Sie mit der vollständigen `a[low:high:max]`-Slice-Form nicht nur
die Länge (`len`), sondern auch die Kapazität (`cap`) des neuen `slice` steuern.
Dies ist ein wichtiges Instrument zur Kontrolle von Nebenwirkungen während
`append`.

#### Formeln:

Für `s := a[low:high:max]`:

1. `len(s) = high - low`

2. `cap(s) = max - low`

Unter der Voraussetzung korrekter Grenzwerte:

- `0 <= low <= high <= max <= cap(a)` (für Slice-Basis)

#### Was es praktisch bringt:

1. **Sichtbare Kapazitätsbeschränkungen:** Sie können den Zugriff auf das Ende
   des zugrunde liegenden Arrays „abschneiden“, selbst wenn es physisch
   vorhanden ist.

2. **Sicherer `append`:** Wenn `cap` künstlich reduziert wird, weist `append`
   den Speicher schneller neu zu, anstatt benachbarte Daten im gemeinsam
   genutzten Array zu überschreiben.

3. **Bessere Isolation zwischen Codeteilen:** Dies ist besonders nützlich, wenn
   ein Slice an eine andere Funktions- oder Systemebene übergeben wird und Sie
   nicht möchten, dass er in den Bereich einer anderen Person „hineinwächst“.

#### Konzeptbeispiel:

- `a[2:5]` ergibt `len=3`, `cap` erstreckt sich bis zum Ende des Basisarrays.

- `a[2:5:5]` ergibt `len=3`, `cap=3` – außerdem ist `append` nicht mehr vorrätig
  und erzwingt ein neues Array.

#### Fazit:

Der dritte Index in `a[low:high:max]` ist der Präzisionssteuerhebel `cap`. Es
wird benötigt, wenn es wichtig ist, das Wachstum von `slice` zu kontrollieren,
unerwartetes Überschreiben des gemeinsam genutzten Speichers zu vermeiden und
das Codeverhalten vorhersehbar zu machen.

#### Beispiel:

```go
package main

import "fmt"

func main() {
	a := []int{0, 1, 2, 3, 4, 5}
	s := a[2:4:4] // len=2 (2,3), cap=2
	fmt.Println(len(s), cap(s)) // 2 2

	s = append(s, 99) // новий backing array, а не розширення в a
	fmt.Println(a)    // [0 1 2 3 4 5]
	fmt.Println(s)    // [2 3 99]
}
```

</details>
