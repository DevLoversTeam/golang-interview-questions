**Read in other languages: [English 🇺🇸](README.en.md),
[Polska 🇵🇱](README.pl.md), [German 🇩🇪](README.de.md), [French 🇫🇷](README.fr.md),
[Spanish 🇪🇸](README.es.md), [Українська 🇺🇦](README.md).**

<h1>
  Go <img src="./assets/go.svg" width="40" height="40" />
</h1>

<h2>Most Popular Go Interview Questions and Answers</h2>


<details>
<summary>1. Czym jest Go i do jakich zadań został stworzony?</summary>

#### Go

Go (lub Golang) to skompilowany język programowania ze statycznym typem
stworzony w Google przez Roberta Griesemera, Roba Pike'a i Kena Thompsona.
Został zaprojektowany z naciskiem na prostotę, przewidywalność, szybką
kompilację i wysoką wydajność w systemach produkcyjnych.

#### Do jakich zadań stworzono Go:

1. **Systemy sieciowe i serwerowe:** usługi HTTP/API, serwery proxy, bramy,
   backend dla aplikacji o dużym obciążeniu.

2. **Infrastruktura chmurowa:** narzędzia do orkiestracji, CI/CD,
   obserwowalność, narzędzia DevOps (dlatego wiele projektów natywnych dla
   chmury jest napisanych w Go).

3. **Przetwarzanie współbieżne:** zadania, w których ważne jest równoległe
   przetwarzanie danych, kontrola opóźnień i efektywne wykorzystanie zasobów.

4. **Programowanie systemu na poziomie aplikacji:** narzędzia CLI, demony,
   procesy robocze w tle, usługi integracyjne.

#### Dlaczego Go:

- Zwięzła składnia i niska złożoność poznawcza kodu.

- Wbudowany model współbieżności (`goroutine`, `channel`).

- Szybka kompilacja i łatwy cykl programowania.

- Wygodny standardowy zestaw narzędzi (`go test`, `go vet`, `pprof`, moduły).

Dlatego Go został stworzony jako praktyczny język inżynieryjny dla skalowalnych,
łatwych w utrzymaniu i wydajnych usług, w których ważna jest niezawodność,
szybkość rozwoju i prostota operacyjna.

</details>


<details>
<summary>2. Jakie są główne zasady projektowania języka Go?</summary>

#### Go

Projekt Go nie opiera się na maksymalnej „wyrazistości” za wszelką cenę, ale na
wykonalności inżynieryjnej: kod musi być łatwy do odczytania, łatwy w utrzymaniu
i niezawodny przez długi cykl życia systemu.

#### Podstawowe zasady projektowania Go:

1. **Prostota ponad złożoność:** Język celowo unika zbyt skomplikowanych
   konstrukcji, aby zmniejszyć liczbę błędów i próg wejścia do bazy kodu.

2. **Czytelność i jednoznaczność:** Preferowany jest przejrzysty kod, który może
   szybko zrozumieć każdy inżynier w zespole, a nie tylko autor.

3. **Szybka kompilacja i produktywny rozwój:** Cykl „napisany → zbudowany →
   przetestowany” powinien być krótki, co przyspiesza iteracje w rzeczywistych
   projektach.

4. **Wbudowana współbieżność:** `goroutine` i `channel` stanowią organiczną
   część języka, a nie zewnętrzną łatkę, więc przetwarzanie równoległe jest
   natywnie obsługiwane.

5. **Kompozycja zamiast ciężkiej hierarchii:** Go preferuje podejście polegające
   na „komponowaniu zachowania z prostych części” zamiast budowania głębokich
   łańcuchów dziedziczenia.

6. **Minimalizm w funkcjach, maksymalizacja w praktyczności:** mniej „magii”,
   bardziej przewidywalne zachowanie podczas wykonywania i debugowania.

7. **Pojedynczy standard narzędziowy:** `go fmt`, `go test`, `go mod`, `go vet`
   tworzą wspólną kulturę rozwoju bez fragmentacji narzędzi.

#### Uogólnienie:

Go został zaprojektowany jako język do rozwoju zespołowego i programowania
przemysłowego: dyscyplinuje styl, zachęca do przejrzystości myślenia w kodzie i
zapewnia dobrą równowagę pomiędzy prostotą i wydajnością.

</details>


<details>
<summary>3. Jakie są najważniejsze cechy Go w porównaniu z innymi językami?</summary>

#### Go

Go wyróżnia się tym, że łączy zwięzłą składnię z bardzo praktycznym inżynierskim
modelem wykonania: język nie obciąża programisty niepotrzebną złożonością, ale
zapewnia narzędzia do budowania szybkich i niezawodnych systemów.

#### Kluczowe cechy Go:

1. **Prosta i ścisła składnia:** kod jest łatwy do odczytania, a jednolitość
   stylistyczna jest utrzymywana automatycznie poprzez `go fmt`.

2. **Kompiluj do natywnego pliku binarnego:** aplikacja jest zwykle kompilowana
   do pojedynczego pliku wykonywalnego bez dużych zewnętrznych zależności
   podczas uruchamiania.

3. **Statyczne pisanie z dużą przewidywalnością:** na etapie kompilacji
   wykrywana jest duża liczba błędów, co zwiększa niezawodność produkcji.

4. **Wbudowana współbieżność:** `goroutine` i `channel` sprawiają, że
   programowanie równoległe jest mechanizmem naturalnym, a nie pomocniczym.

5. **Szybki cykl rozwoju:** stosunkowo szybka kompilacja i standardowe narzędzia
   przyspieszają testowanie i dostarczanie zmian.

6. **Silna biblioteka standardowa:** obsługa sieci, HTTP, kryptografia,
   manipulowanie plikami, profilowanie i testowanie dostępne od razu po wyjęciu
   z pudełka.

7. **Model jawnego błędu:** w Go błędy są obsługiwane jawnie za pośrednictwem
   `error`, dzięki czemu kontrola stanu jest przejrzysta i możliwa do
   kontrolowania.

8. **GC i pamięć zarządzana:** Język upraszcza rozwój zaplecza systemu bez
   konieczności ręcznego zarządzania cyklem życia większości obiektów.

9. **Praktyczne podejście modułowe:** `go mod` standaryzuje zarządzanie
   zależnościami i powtarzalność kompilacji.

#### Wniosek:

W przeciwieństwie do wielu języków, które skłaniają się albo do maksymalnej
abstrakcji, albo do sterowalności na niskim poziomie, Go celowo utrzymuje
równowagę inżynieryjną: prostotę, wydajność, skalowalność i wygodę pracy
zespołowej.

</details>


<details>
<summary>4. Jaka jest różnica między paradygmatem programowania imperatywnego i deklaratywnego? Podaj przykłady języków.</summary>

#### Go

Paradygmaty imperatywne i deklaratywne różnią się przede wszystkim przedmiotem
opisu: pierwszy wyjaśnia **jak** krok po kroku wykonać zadanie, drugi — **co
dokładnie** należy w rezultacie uzyskać.

#### Paradygmat imperatywny:

1. **Istota:** Programista wyraźnie określa sekwencję instrukcji, przejścia
   stanów, pętle, rozgałęzienia i kolejność wykonywania.

2. **Nacisk:** kontrola algorytmów i kontrola przepływu wykonywania.

3. **Typowe cechy:** zmienne, przypisania, `for`, `if`, mutacja danych.

4. **Przykłady języków:** Go, C, C++, Rust (w większości praktyk), Java.

#### Paradygmat deklaratywny:

1. **Esencja:** opisuje pożądany wynik lub właściwości systemu bez
   wyszczególniania etapów wdrażania.

2. **Nacisk:** model danych, zasady i ograniczenia, a nie mechanika
   algorytmiczna.

3. **Typowe cechy:** wyrażenia wyższego poziomu, minimalizacja jawnej mutacji,
   abstrakcja od kolejności wykonania.

4. **Przykładowe języki/podejścia:** SQL, HCL (Terraform), HTML/CSS, style
   funkcjonalne w Haskell i częściowo w Elixir.

#### Wniosek praktyczny:

- W rzeczywistych systemach paradygmaty są często łączone.

- Go ma głównie charakter imperatywny, ale pewne elementy deklaratywności
  pojawiają się w konfiguracjach, opisach schematów, DSL i zapytaniach o dane.

- Na potrzeby rozmowy należy podkreślić, że wybór paradygmatu nie jest kwestią
  „lepszy czy gorszy”, ale kwestią dopasowania zadania, zespołu i wymagań
  dotyczących wsparcia kodu.

</details>


<details>
<summary>5. Dlaczego Go dobrze nadaje się do pisania usług Cloud Native?</summary>

#### Go

Nie przez przypadek Go uznawany jest za jeden z najbardziej naturalnych języków
dla Cloud Native: jego właściwości architektoniczne dobrze wpisują się w
wymagania stawiane nowoczesnym systemom rozproszonym – skalowalność,
obserwowalność, niezawodność i prostota obsługi.

#### Dlaczego Go działa skutecznie w środowisku Cloud Native:

1. **Lekkie, konkurencyjne obliczenia:** `goroutine` i `channel` upraszczają
   konstrukcję usług obsługujących jednocześnie dużą liczbę żądań.

2. **Wysoka wydajność i przewidywalny czas działania:** Kompilator Go i
   zoptymalizowany harmonogram działają dobrze w scenariuszach obciążonej sieci.

3. **Szybki start i wdrożenie:** zazwyczaj wynikiem kompilacji jest pojedynczy
   plik binarny, który można łatwo skontenerować i wdrożyć w Kubernetes lub
   innych koordynatorach.

4. **Niski narzut operacyjny:** Proste obrazy Dockera, szybka kompilacja, mniej
   problemów z zależnościami podczas uruchamiania.

5. **Zaawansowana biblioteka standardowa:** `net/http`, `context`, `crypto`,
   `encoding` i inne pakiety pozwalają budować rozwiązania produkcyjne bez
   nadmiernej zależności od frameworków innych firm.

6. **Wygoda dla praktyków zajmujących się obserwowalnością:** W Go łatwo jest
   zintegrować metryki, śledzenie i profilowanie, co ma kluczowe znaczenie dla
   wykorzystania chmury.

7. **Odporny ekosystem narzędzi infrastrukturalnych:** Duża część stosu Cloud
   Native została napisana specjalnie w Go (np. Kubernetes, Prometheus, Helm,
   Terraform), co upraszcza integrację i kontekst poleceń.

8. **Przejrzystość kodu w rozwoju zespołu:** Go zachęca do prostych rozwiązań,
   które zmniejszają obciążenie poznawcze związane ze wspieraniem architektury
   mikrousług.

#### Podsumowanie:

Go dobrze nadaje się do usług Cloud Native, ponieważ łączy przewidywalność
inżynieryjną z wydajnością i praktyczną wygodą: od pisania kodu po jego
wdrożenie, monitorowanie i długoterminowe wsparcie.

</details>


<details>
<summary>6. Co to są zmienne `shadowing` i jak mogą powodować błędy w logice biznesowej?</summary>

#### Go

`Shadowing` (shadowing) ma miejsce, gdy w zakresie wewnętrznym zadeklarowana
jest nowa zmienna o tej samej nazwie co zmienna zewnętrzna. W rezultacie kod nie
działa z „oczekiwaną” zmienną, ale z jej lokalną kopią według nazwy.

#### Jak to się najczęściej dzieje:

1. **Krótka deklaracja `:=` w zagnieżdżonym bloku:** programista oczekuje
   przypisania, a tak naprawdę tworzona jest nowa zmienna.

2. **Obsługa błędów (`err`) w `if`/`for`/`switch`:** lokalny `err` przesłania
   zewnętrzny, powodując niepowodzenie kolejnych kontroli stanu.

3. **Praca ze stanem w funkcjach długich:** cieniowanie zmiennych pośrednich
   utrudnia odczyt i zwiększa ryzyko defektów logicznych.

#### Dlaczego jest to niebezpieczne dla logiki biznesowej:

1. **Sprawdzanie fałszywych warunków:** system może przeskoczyć do niewłaściwej
   gałęzi wykonania, ponieważ sprawdzana jest „niewłaściwa” zmienna.

2. **Stan utracony lub nieprawidłowy:** na przykład wynik obliczeń pozostał w
   bloku lokalnym, a stan zewnętrzny nie został zaktualizowany.

3. **Złożone debugowanie:** wizualnie nazwa jest taka sama, ale semantycznie są
   to różne obiekty; błąd objawia się niepozornie i często tylko w przypadkach
   bojowych.

4. **Ciche defekty bez paniki:** program może się skompilować i uruchomić, ale
   zwrócić wynik niepoprawny biznesowo.

#### Jak zapobiegać `shadowing`:

- Świadomie rozróżniaj `=` i `:=` we wszystkich zagnieżdżonych blokach.

- Utrzymuj krótką widoczność zmiennych i unikaj zbyt długich funkcji.

- Używaj jasnych, semantycznie dokładnych nazw, szczególnie w przypadku stanów i
  błędów.

- Połącz analizę statyczną (`go vet`, `golangci-lint`) z regułami wykrywania
  cieniowania.

- W krytycznych miejscach logiki dodaj testy dla negatywnych scenariuszy i
  warunków brzegowych.

#### Wniosek:

`Shadowing` nie jest dziwactwem składniowym, ale źródłem podstępnych błędów
logicznych. W produkcyjnym kodzie Go dyscyplina deklaracji zmiennych
bezpośrednio wpływa na poprawność zachowań biznesowych systemu.

</details>


<details>
<summary>7. Dlaczego warto używać `struct{}` (pustej struktury) i w jakich scenariuszach jest to skuteczne?</summary>

#### Go

`struct{}` w Go jest pustą strukturą, tj. typem bez pól. Jego kluczowa
właściwość: nie przenosi ładunku danych, a jedynie rejestruje sam fakt istnienia
wartości lub zdarzenia.

#### Dlaczego `struct{}` jest skuteczny:

1. **Null wolumin informacji:** typ nie zawiera pól, więc jest używany jako
   token, a nie kontener danych.

2. **Jasna semantyka intencji:** kod wyraźnie pokazuje, że ważny jest fakt
   „jest/nie jest”, a nie ładunek.

3. **Ograniczenie zbędnych alokacji w strukturach usług:** w wielu wzorach jest
   to bardziej praktyczny wybór niż `bool` lub dowolne wartości, gdy dane nie są
   potrzebne.

#### Typowe scenariusze użycia:

1. **Ustaw przez `map[K]struct{}`:** `map` w Go to para klucz-wartość, a do
   zestawu potrzebujemy tylko unikalnych kluczy. `struct{}` tutaj idealnie
   oznacza „prezent kluczy”.

2. **Kanały sygnałowe `chan struct{}`:** są używane do powiadamiania o
   wystąpieniu zdarzenia (zatrzymanie/wykonanie/wyłączenie), gdy nie ma potrzeby
   przesyłania danych.

3. **Typy tokenów i kontrakty API:** Pusta struktura może działać jako lekki
   token semantyczny w wewnętrznych protokołach aplikacji.

4. **Osadzanie kompozycji zachowań:** `struct{}` jest czasami używane jako
   element techniczny kompozycji, gdy wymagana jest struktura bezstanowa.

#### Kiedy nie stosować:

- Kiedy wymagany jest faktyczny stan lub atrybuty jednostki.

- Kiedy `bool` zapewnia jaśniejszą semantykę biznesową (np. wyraźna flaga
  warunku zamiast ustalonego faktu).

#### Podsumowanie:

`struct{}` to narzędzie do precyzyjnej intencji: jeśli dane nie są potrzebne,
ale trzeba wskazać fakt, obecność lub sygnał, pusta struktura jest eleganckim i
wydajnym rozwiązaniem w kodzie Go.

</details>


<details>
<summary>8. Jak działa struktura wewnętrzna `slice` i co się dzieje, gdy przekazujesz ją do funkcji?</summary>

#### Go

W Go `slice` nie jest samą tablicą, ale lekkim deskryptorem „dodatkowym” w
sekcji tablicy. Dlatego zachowanie `slice` różni się od normalnego kopiowania
tablicy i często powoduje błędy w wywiadach i prawdziwym kodzie.

#### Model wewnętrzny `slice`:

`slice` koncepcyjnie składa się z trzech części:

1. **Wskaźnik do tablicy bazowej** (`ptr`)

2. **Długość** (`len`) - ile artykułów jest obecnie dostępnych

3. **Pojemność** (`cap`) — ile elementów jest dostępnych aż do limitu tablicy
   bazowej

Oznacza to, że `slice` przechowuje metadane dotyczące regionu w pamięci, zamiast
duplikować wszystkie elementy.

#### Co się stanie, gdy przekażesz `slice` do funkcji:

1. **Kopiowany jest nagłówek `slice` (ptr/len/cap), a nie cała tablica.**

2. **Obie strony (osoba dzwoniąca i wywoływana) początkowo korzystają z tej
   samej tablicy podstawowej.**

3. **Zmiana elementów poprzez indeks** (`s[i] = ...`) w funkcji jest zwykle
   widoczna z zewnątrz, ponieważ zmieniają się dane współdzielonej tablicy.

4. **Zmiana samego nagłówka** (`s = s[:n]`, `s = append(...)`) w funkcji nie
   powoduje zmiany nagłówka w obiekcie wywołującym, chyba że zwrócisz nowy
   `slice`.

#### Kluczowy niuans z `append`:

- Jeśli w czasie `append` jest wystarczająca ilość `cap`, wpis trafia do tej
  samej tablicy podstawowej.

- Jeśli brakuje `cap`, środowisko wykonawcze przydziela nową tablicę, kopiuje do
  niej dane, a lokalny `slice` w funkcji zaczyna odwoływać się do innej pamięci.

Zatem po `append` funkcja może już działać z nową tablicą, natomiast stara
`slice` pozostanie na zewnątrz, jeśli nowa wartość nie zostanie zwrócona.

#### Wniosek praktyczny:

- Chcesz zmienić elementy - możesz przekazać `slice` bez zmian.

- Chcesz zmienić długość/pojemność lub wynik `append` - zwróć zaktualizowaną
  `slice` z funkcji (lub przekaż wskaźnik do `slice`, jeśli jest to naprawdę
  uzasadnione architektonicznie).

#### Przykład:

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
<summary>9. Dlaczego `make([]T, 0, n)` jest lepszy niż `var s []T`, biorąc pod uwagę znane wymiary?</summary>

#### Go

Jeśli znasz z góry przybliżoną lub dokładną liczbę elementów, konstrukcja
`make([]T, 0, n)` jest prawie zawsze bardziej praktyczna niż `var s []T`,
ponieważ natychmiast rezerwuje wymaganą pojemność i zmniejsza liczbę realokacji
pamięci.

#### Co wyróżnia te dwa podejścia:

1. **`var s []T`**

- tworzy `nil`-wycinek z `len=0`, `cap=0`;

- pierwszy `append` powoduje, że środowisko wykonawcze przydziela pamięć;

- w miarę wzrostu ilości danych pojawiają się nowe realokacje i kopie.

2. **`make([]T, 0, n)`**

- tworzy wycinek z `len=0`, ale już z `cap=n`;

- elementy są dodawane poprzez `append` bez zmiany alokacji, aż do wyczerpania
  `cap`;

- mniej kopii danych i stabilniejsza wydajność.

#### Dlaczego jest to ważne w praktyce:

1. **Mniej alokacji na stercie:** zmniejsza obciążenie GC.

2. ** Lepsze zachowanie w zakresie opóźnień:** mniej „skoków” w czasie
   realokacji.

3. **Wyższa przepustowość w gorących ścieżkach:** szczególnie w pętlach,
   analizowaniu, agregacji, serializacji.

4. **Przewidywalność zasobów:** łatwiejsze oszacowanie pamięci dla konkretnego
   scenariusza.

#### Kiedy różnica jest szczególnie zauważalna:

- Duża liczba `append` w pętlach.

- Przetwarzanie strumieni danych w usługach backendu.

- Często wywoływane funkcje, w przypadku których nawet małe alokacje kumulują
  się w znacznych kosztach.

#### Wniosek:

Jeśli rozmiar kolekcji jest znany lub dobrze oszacowany z góry, `make([]T, 0,
n)` jest wyborem dojrzałym pod względem inżynieryjnym: zapewnia mniej alokacji,
lepszą wydajność i bardziej stabilne zachowanie pod obciążeniem.

</details>


<details>
<summary>10. W jaki sposób wyrażenie plasterka `a[low:high:max]` steruje `cap` nowym plasterkiem?</summary>

#### Go

W Go pełna forma wycinka `a[low:high:max]` pozwala kontrolować nie tylko długość
(`len`), ale także pojemność (`cap`) nowego `slice`. Jest to ważne narzędzie do
kontrolowania skutków ubocznych podczas `append`.

#### Formuły:

Dla `s := a[low:high:max]`:

1. `len(s) = high - low`

2. `cap(s) = max - low`

Pod warunkiem prawidłowych limitów:

- `0 <= low <= high <= max <= cap(a)` (dla podstawy plasterka)

#### Co daje praktycznie:

1. **Widoczne ograniczenie pojemności:** możesz „odciąć” dostęp do końca
   podstawowej tablicy, nawet jeśli fizycznie istnieje.

2. **Bezpieczniejsze `append`:** jeśli `cap` zostanie sztucznie zmniejszone,
   `append` szybciej ponownie przydzieli pamięć, zamiast nadpisywać sąsiednie
   dane we współdzielonej tablicy.

3. **Lepsza izolacja pomiędzy fragmentami kodu:** jest to szczególnie przydatne,
   gdy jeden wycinek jest przekazywany do innej funkcji lub warstwy systemu i
   nie chcesz, aby „rozrósł się” w obszar innej osoby.

#### Przykład koncepcyjny:

- `a[2:5]` daje `len=3`, `cap` rozciąga się na koniec tablicy podstawowej.

- `a[2:5:5]` daje `len=3`, `cap=3` - dalej `append` jest niedostępny i wymusza
  nową tablicę.

#### Wniosek:

Trzeci indeks w `a[low:high:max]` to dźwignia precyzyjnego sterowania `cap`.
Jest to potrzebne, gdy ważne jest kontrolowanie wzrostu `slice`, unikanie
nieoczekiwanego nadpisania pamięci współdzielonej i zapewnienie przewidywalności
zachowania kodu.

#### Przykład:

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


<details>
<summary>11. Czy wskaźnik do elementu plasterka ma pozostać ważny po wywołaniu `append`?</summary>

#### Go

Krótka odpowiedź: **nie, nie gwarantujemy**. Po `append` wskaźnik do elementu
starego `slice` może stracić swoje znaczenie dla nowego `slice`, jeśli
podstawowa tablica została ponownie przydzielona.

#### Dlaczego tak się dzieje:

1. `append` dodaje elementy w obrębie istniejącego `cap`, jeśli jest
   wystarczająco dużo miejsca.

2. Jeśli `cap` zostanie wyczerpany, środowisko wykonawcze tworzy nową tablicę,
   kopiuje dane i zwraca `slice`, który już odnosi się do nowego adresu.

3. Wcześniej pobrane wskaźniki pozostają powiązane ze starą tablicą, a nie
   zaktualizowaną `slice`.

#### Konsekwencje praktyczne:

1. **Aliasing wskaźników staje się niebezpieczny:** logika może „zajrzeć” w
   nieaktualny obszar pamięci.

2. **Nieoczekiwane błędy w modyfikacjach:** zmiany dokonane za pomocą starego
   wskaźnika nie mają wpływu na nowy `slice` po przeniesieniu.

3. **Trudne debugowanie:** kod kompiluje się i często działa, ale wykazuje
   nieprzewidywalne zachowanie pod obciążeniem lub na innych woluminach danych.

#### Jak pisać bezpiecznie:

- Nie przechowuj długotrwałych wskaźników do `slice` elementów, które
  potencjalnie będą rosły przez `append`.

- Jeśli wskaźnik jest naprawdę potrzebny, zapewnij stabilność pamięci: wstępnie
  zarezerwuj pojemność (`make(..., 0, n)`) lub nie wykonuj `append` po pobraniu
  adresów.

- Często bezpieczniej jest przekazać indeks lub zwrócić nowy `slice` i powiązać
  wszystkie pochodne odniesienia.

#### Wniosek:

Po `append` ważność wskaźników do elementów `slice` nie jest umową Go.
Bezpieczny kod musi zakładać, że `append` może zmienić adres bazowy danych.

</details>


<details>
<summary>12. Jak sprawnie usunąć elementy z plasterka bez zachowania porządku w Go?</summary>

#### Go

Jeśli kolejność elementów nie ma znaczenia, najskuteczniejszą strategią usuwania
jest zastąpienie usuwanego elementu ostatnim elementem `slice`, a następnie
skrócenie `slice` o jeden.

#### Idea podejścia:

1. Znajdź indeks `i` elementu do usunięcia.

2. Przypisz `s[i] = s[len(s)-1]`.

3. Zmniejsz długość: `s = s[:len(s)-1]`.

#### Dlaczego jest skuteczny:

1. **O(1) w czasie** (bez przesuwania wszystkich kolejnych elementów).

2. **Minimalna liczba kopii** w porównaniu do usuwania w kolejności.

3. **Dobrze skaluje się** w przypadku dużych kolekcji i gorących pętli.

#### Na co zwrócić uwagę:

- Kolejność elementów zmienia się po operacji.

- Wymagane jest sprawdzenie poprawności indeksu.

- W przypadku `slice` ze wskaźnikami czasami wskazane jest wyzerowanie elementu
  końcowego przed obcięciem, aby uniknąć przechowywania zbędnych odniesień w
  pamięci.

#### Wniosek:

Gdy stabilny porządek nie jest wymogiem logiki biznesowej, „zamień z ostatnim +
obcięcie” jest kanonicznym i najszybszym sposobem na usunięcie elementu z
`slice` w Go.

#### Przykład:

```go
func removeUnordered[T any](s []T, i int) []T {
	last := len(s) - 1
	s[i] = s[last]
	var zero T
	s[last] = zero // опційно: щоб не тримати зайве посилання
	return s[:last]
}
```

</details>


<details>
<summary>13. Jaka jest kluczowa kolejność iteracji w `map` i czy można na niej polegać? Jaki to ma wpływ na testy i serializację?</summary>

#### Go

W Go kolejność iteracji kluczy w `map` jest **niedeterministyczna**. Oznacza to,
że podczas `for range` sekwencja klawiszy może się różnić pomiędzy
uruchomieniami programu, a nawet pomiędzy poszczególnymi iteracjami w ramach
pojedynczego przebiegu.

#### Czy możesz polegać na zamówieniu:

1. **Nie, nie możesz.**

2. Zamówienie w `map` nie jest częścią umowy językowej.

3. Każda logika, która w sposób dorozumiany opiera się na „stabilnym” porządku,
   jest potencjalnie błędna.

#### Jak to wpływa na testy:

1. **Niestabilne testy:** porównania ciągów/tablic utworzonych za pomocą `map`
   mogą losowo zakończyć się niepowodzeniem ze względu na inną kolejność
   elementów.

2. **Fałszywe regresje:** nie ma zmian w logice biznesowej, ale test kończy się
   niepowodzeniem z powodu niestabilnych danych wyjściowych.

3. **Właściwe podejście:** testy wymagają:

- porównaj struktury jako zbiory/zbiory skojarzeniowe;

- lub wstępnie posortuj klucze i zbuduj deterministyczny wynik.

#### Jak to wpływa na serializację:

1. Jeśli serializacja opiera się na bezpośrednim obejściu `map`, wynik tekstowy
   może mieć inną kolejność pól/par klucz-wartość.

2. To utrudnia:

- migawka/złote-testy;

- hashowanie ładunków;

- porównanie artefaktów w CI.

3. Aby uzyskać stabilne wyniki, powinieneś:

- kup klucze osobno;

- posortuj je;

- uformuj wynik w ustalonej kolejności.

#### Wniosek:

`map` w Go jest zoptymalizowany pod kątem szybkiego dostępu za pomocą klucza, a
nie zachowania porządku. Dlatego testy, rejestrowanie, podpisywanie danych i
serializacja muszą celowo wprowadzać determinizm poprzez sortowanie kluczy lub
inne zasady kanoniczne.

</details>


<details>
<summary>14. Jak iterować po `map` w przewidywalnej kolejności?</summary>

#### Go

Ponieważ `map` w Go nie gwarantuje stabilnej kolejności przechodzenia,
zamierzona iteracja musi być zorganizowana jawnie: najpierw zbierz klucze,
następnie je posortuj, a dopiero potem odczytaj wartości w ustalonej kolejności.

#### Podejście kanoniczne (Go 1.23+):

1. Użyj `maps.Keys`, aby uzyskać kluczowy iterator.

2. Użyj `slices.Sorted` (`slices.SortedFunc`), aby uzyskać posortowany fragment
   klucza.

3. Iteruj po posortowanym wycinku.

#### Dlaczego to prawda:

1. **Determinizm:** to samo wejście daje tę samą kolejność wyników.

2. **Testy stabilne:** losowe awarie spowodowane inną sekwencją znikają.

3. **Przewidywana serializacja:** łatwiejsze wykonywanie złotych testów,
   podpisów, porównywanie artefaktów.

#### Ważne niuanse:

- W przypadku kluczy strukturalnych lub typów niestandardowych należy
  zdefiniować jawne kryterium sortowania.

- Trudność wzrasta z powodu sortowania (`O(n log n)`), ale taka jest cena
  przewidywalności.

- Jeśli porządek w ścieżce dostępu ma kluczowe znaczenie, czasami warto rozważyć
  inną strukturę danych (np. utrzymanie osobnej uporządkowanej listy kluczy).

#### Wniosek:

Zamierzona iteracja `map` w Go jest zawsze świadomą strategią trójfazową:
„zbieraj klucze → sortuj → przemierzaj”. Ten wzór jest uważany za standard
produkcyjny zapewniający stabilną produkcję. Kompaktowy formularz za
pośrednictwem `slices.Sorted(maps.Keys(m))` jest dostępny od wersji Go 1.23.

#### Przykład:

```go
keys := slices.Sorted(maps.Keys(m))
for _, k := range keys {
	fmt.Printf("%v=%v\n", k, m[k])
}
```

</details>


<details>
<summary>15. Dlaczego nie mogę uzyskać adresu elementu mapy?</summary>

#### Go

W Go nie możesz pobrać adresu elementu `map` (na przykład `&m[key]`), ponieważ
wartość w `map` nie ma stabilnego adresu w pamięci. Podczas wzrostu,
przywracania równowagi lub wewnętrznej reorganizacji środowisko wykonawcze `map`
może przenosić elementy między zasobnikami.

#### Kluczowy powód ograniczenia:

1. **Niestabilność umiejscowienia:** `map` zmienia dynamicznie strukturę
   wewnętrzną.

2. **Niebezpieczeństwo „wiszących” wskaźników:** uzyskany dzisiaj adres może
   utracić ważność po kolejnych operacjach z `map`.

3. **Gwarancja bezpieczeństwa języka:** kompilator zabrania tej operacji, aby
   uniknąć ukrytych błędów pamięci.

#### Konsekwencje praktyczne:

1. Nie możesz modyfikować pola struktury bezpośrednio poprzez `m[key].Field =
   ...`, jeśli wartość mapy jest strukturą.

2. Wzorzec aktualizacji struktury wartości mapy wygląda następująco:

- odczytaj wartość do zmiennej tymczasowej;

- zmień to;

- odpisz do `map`.

#### Gdy wymagana jest zmienność w:

- Użyj `map[K]*T` zamiast `map[K]T`, jeśli chcesz pracować z tym samym obiektem
  za pomocą wskaźnika.

- Należy jednak pamiętać o kompromisach: dodatkowe alokacje, problemy z cyklem
  życia obiektów i potrzeba synchronizacji przy równoczesnym dostępie.

#### Wniosek:

Zakaz przyjmowania adresu elementu `map` jest celowym projektem Go na rzecz
bezpieczeństwa pamięci. Jeśli wymagane są zmiany „w miejscu”, wybierz pętlę
odczyt-modyfikacja-zapis lub `map` z wartościami wskaźników.

</details>


<details>
<summary>16. Dlaczego `map` nie jest fabrycznie zabezpieczony wątkowo w Go?</summary>

#### Go

`map` w Go nie jest z założenia bezpieczny dla wątków: jednoczesny dostęp z
wielu goroutines bez synchronizacji (szczególnie, gdy istnieje rekord) prowadzi
do wyścigów danych i niezdefiniowanego zachowania.

#### Dlaczego tak się dzieje:

1. **Wydajność w scenariuszu podstawowym:** większość `map` jest używana
   lokalnie w pojedynczej procedurze gor; wbudowana blokada dla każdej operacji
   spowolniłaby te scenariusze.

2. **Jawny model współbieżności:** Go przekazuje kontrolę nad synchronizacją
   programiście, dzięki czemu wybiera on mechanizm dla konkretnego obciążenia.

3. **Elastyczność architektury:** różne zadania wymagają różnych strategii
   (mutex, sharding, podejście aktora, `sync.Map`), a „uniwersalna” automatyczna
   blokada nie jest optymalna we wszystkich przypadkach.

#### Co to oznacza w praktyce:

1. **Jednoczesny odczyt i zapis bez zabezpieczenia jest zabroniony.**

2. **Zapis + zapis bez zabezpieczenia jest zabroniony.**

3. **Odczyt + tylko odczyt** może być bezpieczny, jeśli nikt nie modyfikuje
   `map`.

#### Jak zrobić to dobrze:

- `map` + `sync.Mutex` lub `sync.RWMutex` dla zarządzanej synchronizacji.

- `sync.Map` dla określonych wzorców dostępu (wiele odczytów, rzadkie zapisy lub
  niezależne klucze).

- Izolacja stanu architektonicznego za pomocą jednej „zastrzeżonej” procedury i
  kanałów.

#### Wniosek:

`map` bezpieczeństwo braku przepływu po wyjęciu z pudełka nie jest wadą, ale
świadomym kompromisem Go: minimalny narzut w ogólnym przypadku i pełna kontrola
współbieżności w rękach inżyniera.

</details>


<details>
<summary>17. Czy struktura może być kluczem w `map` i jakie są tego ograniczenia? W czym jest to lepsze od map zagnieżdżonych?</summary>

#### Go

Tak, w Go struktura może być kluczem w `map` **jeśli jest porównywana**
(`comparable`). Oznacza to, że wszystkie jego pola muszą być również
porównywalne.

#### Ograniczenia klucza strukturalnego:

1. **Wszystkie pola struktury muszą być porównywalne.**

- Dozwolone w szczególności: liczby, stringi, bool, wskaźniki, tablice (z
  elementami porównywalnymi), inne porównywalne struktury.

- Niedozwolone pola typów w kluczu: `slice`, `map`, `func` (nie są
  porównywalne).

2. **Porównanie opiera się na wartości wszystkich pól.**

- Dwa klucze są uważane za równe tylko wtedy, gdy wszystkie odpowiadające im
  pola są równe.

3. **Klucz musi być stabilny po włożeniu.**

- Zmienianie „sensu” klucza poprzez zewnętrzny, zmienny stan jest złą praktyką,
  ponieważ niszczy przewidywalność dostępu.

#### Dlaczego klucz strukturalny jest często lepszy niż zagnieżdżony `map`:

1. **Prostszy model danych:**

- Zamiast `map[A]map[B]V` możesz użyć `map[CompositeKey]V`, gdzie `CompositeKey`
  to struktura z polami `A`, `B`.

2. **Mniej szablonów i kontroli w dniu `nil`:**

- W zagnieżdżonych `map` mapach wewnętrznych należy zainicjować i obsłużyć
  brakujące klucze pośrednie.

3. **Lepsza lokalizacja logiczna:**

- Wszystkie kluczowe wymiary są zebrane w jednym typie, co poprawia czytelność i
  łatwość konserwacji.

4. **Mniej miejsca na błędy:**

- Łatwiej uniknąć częściowo zainicjowanych struktur i niespójnych ścieżek
  dostępu.

#### W przypadku zagnieżdżenia `map` może być odpowiedni:

- Kiedy wymagana jest hierarchiczna semantyka danych.

- W przypadku częstej pracy z segmentami pośrednimi na poziomie pierwszego
  klawisza.

- Gdy różne warstwy mają oddzielne zasady cyklu życia.

#### Wniosek:

Klucz strukturalny Go jest potężnym i przejrzystym narzędziem do adresowania
złożonego. Jeśli typ klucza jest poprawnie zaprojektowany i to `comparable`, to
rozwiązanie jest często bardziej eleganckie i niezawodne niż zagnieżdżone `map`.

</details>


<details>
<summary>18. Jak porównać dwie struktury - kiedy się kompiluje, a kiedy nie? </summary>

#### Go

W Go dwie struktury można porównać za pomocą operatora `==` lub `!=` tylko
wtedy, gdy typ struktury to `comparable`. W praktyce oznacza to: **należy
porównać wszystkie pola konstrukcji**.

#### Po skompilowaniu porównania:

1. Struktury są tego samego typu.

2. Każde pole w strukturze jest typu porównywalnego.

3. Porównanie odbywa się na wartościach wszystkich pól.

#### Gdy porównanie się nie kompiluje:

1. Jeśli co najmniej jedno pole ma nieporównywalny typ:

- `slice`

- `map`

- `func`

2. Jeśli próbujesz porównać różne typy struktur, nawet z podobnymi polami.

#### Ważne wyjaśnienia:

1. **Tablice są porównywane**, jeśli porównywane są ich elementy.

2. **Porównywane są wskaźniki** (porównywane są adresy).

3. **Interfejsy są porównywane**, jeśli porównywana jest także wartość
   dynamiczna wewnątrz; w przeciwnym razie możliwa jest panika w czasie
   wykonywania podczas porównywania.

#### Wniosek praktyczny:

- Jeśli struktura składa się wyłącznie z porównywalnych pól, możesz użyć `==`.

- Jeśli struktura to `slice/map/func`, użyj jawnego porównania pól lub
  oddzielnych podejść (takich jak wyspecjalizowana logika porównania), a nie
  bezpośredniego operatora równości.

</details>


<details>
<summary>19. Jak zaimplementować porównanie dwóch struktur, jeśli zawierają one wycinki lub mapy? Co to jest `reflect.DeepEqual()`?</summary>

#### Go

Jeśli struktura zawiera `slice` lub `map`, bezpośrednie porównanie za pomocą
`==` nie zostanie skompilowane. W takich przypadkach porównanie należy
przeprowadzić osobno: ręcznie lub za pomocą narzędzi do głębokich porównań.

#### Podstawowe podejścia:

1. **Jawne porównanie pól (zalecane w przypadku logiki krytycznej):**

- porównaj bezpośrednio proste pola;

- dla `slice` sprawdź długość i elementy;

- dla `map` sprawdź liczbę kluczy i pasujące wartości.

2. **`reflect.DeepEqual(a, b)`:**

- przeprowadza rekurencyjne („głębokie”) porównywanie złożonych struktur;

- przydatny do szybkich kontroli, prototypów i części scenariuszy testowych.

#### Co to jest `reflect.DeepEqual()`:

`reflect.DeepEqual()` to funkcja standardowego pakietu `reflect`, która próbuje
określić głęboką równość dwóch wartości poprzez rekursywne przechodzenie przez
zagnieżdżone pola, elementy kolekcji i struktury danych.

#### Niuanse `reflect.DeepEqual`, o których warto pamiętać:

1. **Semantyka może nie odpowiadać równości biznesowej:**

- na przykład `nil`-plasterek i pusty `[]T{}` są często traktowane inaczej.

2. **Mniej przejrzysta diagnostyka:**

- podczas upadku trudniej jest zrozumieć, które pole jest inne, bez dodatkowych
  narzędzi.

3. **Wydajność:**

- odbicie jest wolniejsze niż specjalistyczne ręczne porównywanie w gorących
  ścieżkach.

#### Kiedy wybrać:

1. **Zasady biznesowe i produkcyjne:** wyraźne porównanie domen (jasna
   semantyka).

2. **Testy i kontrole pomocnicze:** `reflect.DeepEqual` lub więcej
   wyspecjalizowanych bibliotek testów.

3. **Scenariusze krytyczne:** unikaj „magii” odbicia, gdy wymagane jest ścisłe
   sprawdzanie równoważności.

#### Wniosek:

W przypadku struktur z `slice/map` prawidłowe porównanie jest przede wszystkim
kwestią semantyki, a nie techniki. `reflect.DeepEqual()` to przydatne narzędzie,
ale najbardziej niezawodną metodą inżynieryjną pozostaje wyraźna metoda
porównania oparta na domenie.

</details>


<details>
<summary>20. Co się dzieje podczas rzutowania między nazwanymi typami o tej samej strukturze, jeśli mają one różne metody?</summary>

#### Go

W Go rzutowanie między nazwanymi typami o tej samej strukturze podrzędnej
dotyczy **tylko wartości danych**, ale nie „portuje” metod. Oznacza to, że po
konwersji otrzymasz nową wartość innego nazwanego typu z własnym zestawem metod.

#### Główna zasada:

1. **Konwersja zmienia typ wartości, zamiast ujednolicać zachowanie typów.**

2. **Metody należą do określonego, nazwanego typu**, w którym są zadeklarowane.

3. Po `T2(vT1)` dostępne są metody `T2`, a metody `T1` nie są już bezpośrednio
   dostępne.

#### Co jest zapisywane podczas konwersji:

1. Bitowa/boolowska reprezentacja pól (zgodnie z regułami zgodności typów).

2. Wartość danych.

#### Co nie jest zapisywane:

1. Zestaw metod oryginalnego typu.

2. Automatyczne dopasowanie interfejsu zapewniane przez oryginalny typ.

#### Konsekwencje praktyczne:

1. Dwa typy z tymi samymi polami mogą mieć różne zachowanie w interfejsie API.

2. Po konwersji kod może się nie skompilować w miejscach, w których oczekiwano
   interfejsu zaimplementowanego wyłącznie przez typ źródłowy.

3. Jest to przydatne do modelowania domen: ta sama struktura danych, ale różne
   role semantyczne i kontrakty.

#### Wniosek:

W Go konwersja między nazwanymi typami zmienia „tożsamość” typu, a nie
kopiowanie zachowania. Dane mogą być takie same, ale metody i możliwości
interfejsu są definiowane wyłącznie przez typ docelowy.

</details>


<details>
<summary>21. Co to jest `Memory Alignment` (wyrównanie) i jak wpływa na wielkość konstrukcji?</summary>

#### Go

`Memory Alignment` (wyrównanie) to reguła umieszczania danych w pamięci pod
adresami wielokrotnościami określonego kroku (wymóg wyrównania) dla określonego
typu. Procesor i środowisko wykonawcze odczytują takie dane szybciej i
bezpieczniej, gdy spełnione są te wymagania.

#### Jak to działa w frameworkach:

1. Każde pole ma własne wymagania dotyczące wyrównania (np. `int64` zwykle
   wymaga bardziej rygorystycznego wyrównania niż `byte`).

2. Pomiędzy polami kompilator może dodać **dopełnienie** (bajty usługi
   zastępczej), tak aby następne pole zaczynało się od prawidłowego adresu.

3. Na końcu konstrukcji może znajdować się również wyściółka, dzięki czemu
   szereg takich struktur zachowuje prawidłowe ustawienie każdego elementu.

#### Wpływ na rozmiar konstrukcji:

1. **Rozmiar struktury jest często większy niż suma rozmiarów pól** ze względu
   na dopełnienie.

2. **Kolejność pól ma znaczenie:** złe rozmieszczenie (`byte`, `int64`, `byte`,
   ...) może znacznie zwiększyć całkowity rozmiar.

3. **Optymalne grupowanie pól** (od większych do mniejszych) zwykle zmniejsza
   zużycie pamięci.

#### Dlaczego jest to ważne w praktyce:

1. Mniejszy rozmiar struktury = lepsza lokalizacja pamięci podręcznej.

2. Mniejsze zużycie pamięci RAM w dużych tablicach/pamięci podręcznej/indeksach.

3. Wyższa przepustowość w gorących ścieżkach dzięki zmniejszonemu wykorzystaniu
   pamięci.

#### Wniosek inżynierski:

Wyrównanie nie jest „egzotyką niskiego poziomu”, ale praktycznym czynnikiem
wydajności. W Go właściwa kolejność pól w strukturze wpływa bezpośrednio na jej
wielkość, a co za tym idzie na wydajność pamięci i szybkość systemu.

</details>


<details>
<summary>22. Dlaczego przekazywanie dużej struktury „według wartości” jest często wolniejsze niż przekazywanie wskaźnika?</summary>

#### Go

Przekazywanie dużej struktury przez wartość oznacza kopiowanie całej jej
zawartości przy każdym wywołaniu funkcji. W przypadku typów zbiorczych może to
być znacznie droższe niż przekazywanie pojedynczego wskaźnika do tych samych
danych.

#### Dlaczego istnieje różnica w wydajności:

1. **Koszt kopiowania pamięci:** im większa struktura, tym więcej bajtów należy
   skopiować w wywołaniach we/wy.

2. **Załaduj pamięć podręczną procesora:** masowe kopie zwiększają ruch w
   pamięci i mogą pogorszyć lokalizację pamięci podręcznej w obszarach gorącego
   kodu.

3. **Efekt kaskadowy w pętlach i potokach:** jeśli struktura jest przekazywana
   wielokrotnie, kumulują się koszty ogólne.

4. **Potencjalny wpływ na alokacje:** W niektórych scenariuszach zachowanie
   kopiowania i ucieczki może wydłużyć czas wykonywania i ciśnienie GC.

#### Kiedy wskaźnik jest często lepszy:

1. Kiedy struktura jest duża i często przechodzi między funkcjami.

2. Kiedy chcesz zmienić stan udostępnienia bez dodatkowego kopiowania.

3. Kiedy ważne jest stabilne zachowanie opóźnień pod obciążeniem.

#### Ale nie zawsze wskaźnik jest automatycznie lepszy:

1. W przypadku małych struktur przekazywanie wartości może być prostsze i
   całkiem wydajne.

2. Value zapewnia lepszą izolację stanu (brak ukrytego współdzielonego stanu
   zmiennego).

3. Wskaźnik zwiększa ryzyko aliasingu i potrzebę dokładniejszej synchronizacji w
   konkurencyjnym kodzie.

#### Wniosek praktyczny:

W Go wybór między wartością a wskaźnikiem nie jest dokonywany dogmatycznie, ale
na podstawie profilu danych: duże struktury i częste wywołania faworyzują
wskaźnik; małe, niezmienne dane często są odpowiednie do przekazywania wartości.

</details>


<details>
<summary>23. Dlaczego `map` jest wolniejszy niż `slice` przy dostępie sekwencyjnym i kiedy co wybrać?</summary>

#### Go

W przypadku dostępu sekwencyjnego (`sequential access`) `slice` jest zwykle
szybszy niż `map`, ponieważ elementy `slice` są zwarte i czytane liniowo,
podczas gdy `map` wykonuje mieszanie kluczy i dostęp do bardziej złożonej
struktury wewnętrznej.

#### Dlaczego `slice` jest szybszy w przebiegu sekwencyjnym:

1. **Liniowe rozmieszczenie w pamięci:** elementy znajdują się obok siebie, co
   dobrze pasuje do pamięci podręcznej procesora.

2. **Prosty dostęp według indeksu:** minimalna liczba operacji pomocniczych na
   element.

3. **Większa przewidywalność dla procesora:** wzór liniowy zmniejsza liczbę
   braków pamięci podręcznej.

#### Dlaczego `map` działa wolniej w tym scenariuszu:

1. **Klucze mieszające** zwiększają obciążenie obliczeniowe.

2. **Nierówne rozmieszczenie segmentów** jest gorsze w przypadku lokalizacji
   pamięci.

3. **Bardziej złożona logika dostępu** (wyszukiwanie w segmentach, kolizje,
   kontrole usług).

#### Kiedy wybrać `slice`:

1. Dane przekazywane są sekwencyjnie.

2. Wymaga iteracji, sortowania i przetwarzania wsadowego.

3. Klucz jest w rzeczywistości pozycją (indeksem), a nie dowolnym
   identyfikatorem.

#### Kiedy wybrać `map`:

1. Wymaga szybkiego dostępu za pomocą klucza (`id`, `name`, klucz złożony).

2. Semantyka zestawu/słownika jest ważna.

3. Wyszukiwanie według wartości klucza dominuje w pełnym przechodzeniu liniowym.

#### Wniosek praktyczny:

`slice` — narzędzie do uporządkowanych, gęstych iteracji; `map` — dla dostępu do
adresu za pomocą klucza. Jeśli obciążenie ma głównie charakter sekwencyjny,
`slice` zwykle zapewnia lepszą wydajność i mniejsze obciążenie.

</details>


<details>
<summary>24. Jak sprawdzić, czy zmienna implementuje interfejs?</summary>

#### Go

W Go implementacja interfejsu jest niejawna: uważa się, że typ implementuje
interfejs, jeśli ma cały wymagany zestaw metod. Dzięki temu weryfikacja jest
możliwa zarówno na etapie kompilacji, jak i w czasie wykonywania.

#### 1) Weryfikacja na etapie kompilacji (zalecane):

Najbardziej niezawodnym podejściem jest dodanie asercji w czasie kompilacji:

```go
var _ MyInterface = (*MyType)(nil)
```

Co to oznacza:

1. Jeśli `*MyType` nie implementuje `MyInterface`, kod nie zostanie
   skompilowany.

2. To dokumentuje kontrakt typu bezpośrednio w bazie kodu.

3. Szczególnie przydatne w przypadku publicznych interfejsów API, adapterów i
   dużych poleceń.

#### 2) Sprawdź podczas wykonywania (w czasie wykonywania):

Jeśli istnieje wartość typu `any`/interfejs, używana jest asercja typu:

```go
v, ok := x.(MyInterface)
```

1. `ok == true` — wartość implementuje interfejs.

2. `ok == false` — nie implementuje.

3. Wariant bez `ok` może wywołać panikę, dlatego kod produkcyjny zwykle używa
   bezpiecznej formy z `ok`.

#### Wskaźnik a odbiorca wartości — kluczowy niuans:

1. Zestawy metod `T` i `*T` są różne.

2. Często to `*T` implementuje interfejs, a `T` nie.

3. Podczas rozmowy kwalifikacyjnej ważne jest, aby jasno omówić tę kwestię,
   ponieważ jest to typowe źródło błędów.

#### Wniosek:

Najlepszą praktyką jest naprawienie implementacji interfejsu za pomocą asercji w
czasie kompilacji i użycie weryfikacji w czasie wykonywania za pomocą asercji, w
której typ wartości jest znany tylko w czasie wykonywania.

</details>


<details>
<summary>25. Czym są `type assertion` i `type switch` – jakie są ich zalety i jak radzić sobie z asercjami bez paniki?</summary>

#### Go

`type assertion` i `type switch` w Go to mechanizmy służące do pracy z
wartościami interfejsu, gdy w czasie wykonywania należy określić rzeczywisty
(dynamiczny) typ.

#### Co to jest `type assertion`:

`type assertion` ma postać:

```go
v, ok := x.(T)
```

1. `x` — wartość typu interfejsu.

2. `T` to typ, do którego staramy się doprowadzić.

3. `ok == true` oznacza, że ​​typ dynamiczny jest zgodny z `T`.

#### Korzyści `type assertion`:

1. Umożliwia dostęp do określonego zachowania określonego typu.

2. Umożliwia bezpieczną pracę z `any`/interfejsami w adapterach, dekoderach,
   oprogramowaniu pośrednim.

3. Przydatne, gdy oczekiwany jest jeden konkretny typ.

#### Jak uniknąć paniki:

Niebezpieczna forma:

```go
v := x.(T) // panic, якщо x не є T
```

Bezpieczna forma:

```go
v, ok := x.(T)
if !ok {
    // обробити невідповідність типу
}
```

Jest to dwucyfrowa forma z `ok`, która jest standardem produkcyjnym.

#### Co to jest `type switch`:

`type switch` to wygodny sposób obsługi kilku możliwych typów jednocześnie:

```go
switch v := x.(type) {
case string:
    // ...
case int:
    // ...
default:
    // ...
}
```

#### Korzyści `type switch`:

1. Sprawia, że rozgałęzienia typów są czytelne.

2. Redukuje kaskadę wielu stwierdzeń.

3. Podaje jawną ścieżkę `default` dla nieznanych typów.

#### Kiedy używać czego:

1. **`type assertion`** — przy sprawdzaniu jednego oczekiwanego typu.

2. **`type switch`** — gdy dopuszczamy kilka typów i dla każdego potrzebujemy
   innej logiki.

#### Wniosek:

`type assertion` i `type switch` to kontrolowany sposób „ujawniania” typu
wartości interfejsu dynamicznego. Aby uniknąć awarii, asercja powinna być
dokonana w bezpiecznej formie `v, ok := ...` i zawsze mieć skrypt przetwarzający
`ok == false`.

</details>


<details>
<summary>26. Dlaczego `interface{}` i `any` są identyczne, ale `*interface{}` prawie zawsze jest błędem?</summary>

#### Go

W Go `any` jest po prostu aliasem (`alias`) dla `interface{}`. Oznacza to, że z
punktu widzenia typowego systemu są one absolutnie takie same: różnica jest
jedynie stylistyczna i semantyczna w zakresie czytelności kodu.

#### Dlaczego `interface{}` == `any`:

1. `any` wprowadzono dla większej przejrzystości, szczególnie w kodzie ogólnym.

2. Kompilator interpretuje `any` i `interface{}` jako ten sam typ.

3. Zachowanie podczas przypisywania, potwierdzania i przełączania jest
   identyczne.

#### Dlaczego `*interface{}` prawie zawsze oznacza błąd:

1. **Interfejs jest już „kontenerem referencyjnym” dla wartości i typu.**
   Dodawanie kolejnego poziomu wskaźnika zwykle nie ma sensu.

2. **Komplikacja semantyki zera:** przy `*interface{}` pojawia się kolejna
   warstwa stanów (wskaźnik `nil`, niezerowy wskaźnik na interfejsie zerowym
   itp.), co generuje nieoczywiste błędy.

3. **Słaba czytelność i projekt interfejsu API:** ten typ prawie zawsze
   sygnalizuje, że model danych lub sygnatura funkcji jest źle zaprojektowana.

4. **Zamiast `*interface{}` zwykle wystarcza:**

- lub przekaż `interface{}`/`any` według wartości;

- lub użyj określonego typu wskaźnika (`*T`), jeśli wymagana jest zmienność
  obiektu `T`.

#### Kiedy może się zdarzyć `*interface{}`:

- W wąskich scenariuszach technicznych (gdzie należy zmienić dokładnie zmienną
  interfejsu, taką jak komórka), ale w zastosowanym kodzie produkcyjnym, jest to
  rzadki i przeważnie niepożądany wzorzec.

#### Wniosek:

`any` i `interface{}` są identyczne. Zamiast tego `*interface{}` jest w
większości przypadków niepotrzebną abstrakcją, która komplikuje kod i zwiększa
ryzyko błędów logicznych.

</details>


<details>
<summary>27. Kiedy należy używać `interface{}` (`any`) i kiedy uważa się to za zły dźwięk?</summary>

#### Go

`any` (tj. `interface{}`) jest odpowiedni, gdy typ wartości jest obiektywnie
nieznany na granicy API. Jednak nadmierne użycie `any` w logice domeny zwykle
pogarsza bezpieczeństwo typów i utrudnia konserwację.

#### Kiedy `any` jest naprawdę uzasadnione:

1. **Warstwy infrastruktury i kontenery uniwersalne:** logowanie, opakowania
   ogólne, oprogramowanie pośrednie, biblioteki niskiego poziomu.

2. **Dekodowanie formatów o słabym typie:** takich jak części JSON o
   nieprzewidywalnym schemacie.

3. **Punkty integracji z zewnętrznymi API:** gdy kontrakt jest dynamiczny i nie
   można z góry ustalić jego ścisłego typu.

4. **Przejściowe etapy refaktoryzacji:** jako tymczasowy kompromis z późniejszym
   powrotem do konkretnych typów.

#### Kiedy ton jest zły:

1. **W modelu biznesowym, w którym znany jest typ:** `any` ukrywa błędy do czasu
   wykonania, a nie do czasu kompilacji.

2. **Kiedy `any` zastępuje normalny projekt API:** wielokrotne potwierdzenia i
   zmiany typu w każdym innym miejscu są objawem niezdefiniowanych kontraktów.

3. **Kiedy możesz używać typów ogólnych lub interfejsu z metodą minimalną:**
   daje to bardziej rygorystyczne i bardziej czytelne ograniczenia.

4. **Kiedy `any` dostaje się „wszędzie” na skutek bezwładności:** kod staje się
   kruchy, trudniejszy do testowania i trudniejszy do ewolucji.

#### Ogólna zasada:

- Domyślnie wybierz **konkretny typ**.

- Jeśli wymagana jest abstrakcja zachowań — **interfejs z jasną umową**.

- Jeśli wymagane jest uogólnienie danych — **ogólne**.

- `any` pozostaw prawdziwie dynamiczne granice systemu.

#### Wniosek:

`any` to przydatne narzędzie, ale nie jest to uniwersalna odpowiedź. W dojrzałym
kodzie Go używa się go punktowo: tam, gdzie niejednoznaczność typu jest
naturalna, a nie tam, gdzie można i należy wyrazić ścisły kontrakt.

</details>


<details>
<summary>28. Jaka jest zaleta akceptowania interfejsów i zwracania określonych struktur?</summary>

#### Go

W Go obowiązuje wspólna i niezwykle praktyczna zasada: **akceptuj interfejsy,
zwracaj struktury**. Jego siła polega na tym, że zależności wejściowe są
elastyczne, a kontrakty wyjściowe przejrzyste i bogate w funkcje.

#### Co oznacza „akceptowanie interfejsów”:

1. Funkcja/metoda akceptuje umowę o minimalnym zachowaniu (np. `io.Reader`), a
   nie typ zakodowany na stałe.

2. Redukuje to sprzężenie między modułami.

3. Ułatwia testowanie: łatwo zastąpić kod pośredniczący/próbny/fałszywy
   wymaganymi metodami.

#### Co oznaczają „struktury zwrotu”:

1. Wywołanie otrzymuje konkretny typ z pełnym zestawem metod.

2. API staje się bardziej przejrzyste: użytkownik widzi rzeczywiste możliwości
   obiektu.

3. Łatwiej ewoluować typ bez zrywania umów dotyczących interfejsu zewnętrznego.

#### Dlaczego ta kombinacja jest skuteczna:

1. **Na wejściu — abstrakcja, na wyjściu — konkret.**

2. **Większa elastyczność integracji** bez utraty wyrazistości API.

3. ** Lepsza łatwość konserwacji:** granice modułów są jasne, zależności są
   kontrolowane.

4. **Łatwiejsza refaktoryzacja:** Zmiany wewnętrzne są łatwiejsze do
   wprowadzenia bez edycji kaskadowych.

#### Kiedy zachować ostrożność:

1. Nie twórz interfejsów zastępczych bez rzeczywistej potrzeby.

2. Interfejs powinien działać tam, gdzie jest używany, a nie tam, gdzie jest
   zaimplementowany.

3. Jeśli potrzebna jest tylko jedna implementacja i nie ma korzyści z
   testowania, zbyt duża abstrakcja może zaszkodzić czytelności.

#### Wniosek:

Akceptowanie interfejsów i przywracanie konkretnych struktur to równowaga między
rozszerzalnością a przejrzystością. Pozwala na pisanie kodu Go, który jest
jednocześnie wygodny w testowaniu, łatwy w utrzymaniu i naturalnie rozwijany.

</details>


<details>
<summary>29. Dlaczego Go używa interfejsów jednometodowych (np. `io.Reader`, `fmt.Stringer`) i jakie korzyści architektoniczne zapewnia?</summary>

#### Go

Interfejsy jednometodowe w Go to skoncentrowany kontrakt zachowania: opisują
dokładnie jedną zdolność obiektu, bez przeciążania API. Dlatego `io.Reader`,
`io.Writer`, `fmt.Stringer` stały się podstawowymi elementami budulcowymi
ekosystemu.

#### Dlaczego to podejście jest tak skuteczne:

1. **Minimalna umowa:** typ musi zaimplementować tylko jedną metodę, aby
   zintegrować się z dużą liczbą komponentów.

2. **Niskie sprzężenie:** Moduły zależą od możliwości, a nie od konkretnej
   implementacji lub dużego „grubego” interfejsu.

3. **Kompozytowość:** złożone możliwości można łatwo zbudować z kombinacji
   małych interfejsów.

4. **Proste testowanie:** do testu wystarczy mała podróbka/odcinek z jedną
   metodą.

#### Korzyści architektoniczne:

1. **Wymienność implementacji podobna do wtyczki:** plik, gniazdo sieciowe,
   bufor w pamięci mogą działać tak samo jak `io.Reader`.

2. **Stabilne granice modułów:** zależności pomiędzy warstwami systemu stają się
   jasne i ewolucyjnie stabilne.

3. **Łatwa ewolucja kodu:** można dodać nową implementację bez zmiany
   konsumentów, jeśli umowa zostanie zachowana.

4. **Czytelność intencji:** sygnatura funkcji natychmiast odpowiada na pytanie
   „co jest wymagane od argumentu”.

#### Wniosek praktyczny:

Interfejsy jednometodowe nie są ozdobą stylistyczną, ale strategią
architektoniczną Go: małe kontrakty, wysoka kompozycyjność, łatwa testowalność i
kontrolowana skalowalność systemu.

</details>


<details>
<summary>30. Dlaczego `nil != nil` jest w Go i jaki ma to związek z interfejsami?</summary>

#### Go

Wyrażenie „`nil != nil`” w Go zwykle odnosi się do interfejsów i oznacza, że
wartość interfejsu może zawierać **typ + wartość**, gdzie wartość w środku to
`nil`, ale sam interfejs nie jest `nil`.

#### Konceptualny układ interfejsu:

Interfejs składa się z dwóch części:

1. **Typ dynamiczny**

2. **Wartość dynamiczna**

Interfejs jest `nil` tylko wtedy, gdy brakuje **obu** części.

#### Gdzie występuje pułapka:

1. Mamy `var p *MyType = nil`.

2. Przypisz `var i any = p`.

3. Teraz `i` zawiera:

- typ: `*MyType`

- wartość: `nil`

Zatem `i != nil`, ponieważ typowa część jest wypełniona.

#### Konsekwencje praktyczne:

1. Kontrola `if err != nil` lub `if x != nil` może nie działać zgodnie z
   oczekiwaniami programisty, jeśli w interfejsie zostanie wpisane nil.

2. Jest to typowe źródło błędów w błędach, fabrykach, oprogramowaniu pośrednim,
   kodzie DI.

#### Jak uniknąć problemów:

1. Return `nil` dokładnie jako „pusty interfejs”, a nie wpisany nil w
   interfejsie.

2. Konstruuj `error` i inne wyniki interfejsu ostrożnie.

3. W razie potrzeby wykonaj jawne sprawdzenie określonego typu poprzez
   asercję/przełącznik.

#### Wniosek:

W Go „`nil != nil`” nie jest paradoksem, ale konsekwencją dwuskładnikowego
charakteru interfejsu. Kluczową zasadą jest to, że interfejs jest `nil` tylko
wtedy, gdy nie zawiera ani typu dynamicznego, ani wartości dynamicznej.

#### Przykład:

```go
var p *bytes.Buffer = nil
var x any = p

fmt.Println(p == nil) // true
fmt.Println(x == nil) // false: type=*bytes.Buffer, value=nil
```

</details>


<details>
<summary>31. Czy metody można wywoływać na wartościach `nil` i gdzie jest to aktywnie wykorzystywane?</summary>

#### Go

Tak, w Go można wywołać metodę na wartości `nil`, **o ile jest to dopuszczalne z
punktu widzenia typu odbiornika**. Najczęściej mówimy o metodach z odbiornikiem
wskaźnikowym (`*T`), gdzie odbiornikiem może być `nil`.

#### Kluczowa idea:

1. Wywołanie metody na wskaźniku `nil` jest technicznie możliwe.

2. Pytanie brzmi, co kod metody robi wewnątrz.

3. Jeśli metoda bez sprawdzenia zmieni nazwę odbiorcy, wpadniemy w panikę.

#### Kiedy działa bezpiecznie:

1. Metoda  jawnie obsługuje odbiornik `nil`:

- zwraca wartość domyślną;

- zwraca błąd;

- zachowuje się jak nikt inny.

2. Ten projekt jest czasami celowo używany w wygodnym interfejsie API.

#### Gdzie to jest faktycznie używane:

1. **Typy błędów i opakowania:** metody na typach wskaźników mogą poprawnie
   współpracować z `nil`, aby uprościć obsługę błędów.

2. **Struktury połączone/listowe/drzewne:** `nil`-węzeł można interpretować jako
   stan pusty z poprawnym zachowaniem.

3. **Obiekty usługowe z opcjonalnymi komponentami:** `nil` odbiornik jest
   czasami używany w trybie „wyłączonym” lub „pustym”.

#### Ważny niuans dotyczący interfejsów:

Jeśli wskaźnik `nil` jest opakowany w interfejs, sam interfejs może nie być
`nil`. Dlatego kontrole pod kątem `nil` należy przeprowadzać ostrożnie, aby
uniknąć fałszywej pewności.

#### Wniosek praktyczny:

Metody na wartościach `nil` w Go są legalnym narzędziem, ale tylko przy
świadomym projektowaniu API: albo bezpieczna obsługa `nil` wewnątrz metody, albo
jasna dokumentacja mówiąca, że wywołanie `nil` nie jest dozwolone.

</details>


<details>
<summary>32. Jak powiedzieć głównej procedurze, aby czekała na zakończenie wszystkich procedur roboczych?</summary>

#### Go

Kanonicznym sposobem oczekiwania na zakończenie wszystkich działających
goroutines w Go jest użycie `sync.WaitGroup`. Zapewnia prosty i solidny wzór:
zwiększ licznik przed rozpoczęciem zadania, zmniejsz go po jego zakończeniu i
wywołaj `Wait()` w głównej procedurze gor.

#### Schemat podstawowy:

1. Utwórz `var wg sync.WaitGroup`.

2. Przed każdym wywołaniem goroutine `wg.Add(1)`.

3. Wewnątrz goroutine wykonaj `defer wg.Done()`.

4. W głównej procedurze wywołaj `wg.Wait()`.

#### Dlaczego to działa:

1. `WaitGroup` zlicza liczbę niedokończonych zadań.

2. `Wait()` blokuje wykonanie, dopóki licznik nie osiągnie zera.

3. Dzięki temu `main` nie zakończy się przed działającymi procedurami gor.

#### Typowe błędy, których należy unikać:

1. Zadzwoń `Add(1)` **po** rozpoczęciu goroutine (ryzyko wyścigu i
   nieprawidłowego zakończenia).

2. Zapomnij o `Done()` w przypadku błędu lub wczesnej gałęzi `return`.

3. Ponowne użycie tego samego `WaitGroup` w różnych fazach bez wyraźnej
   synchronizacji.

#### Kiedy jest lepiej `errgroup`:

Jeśli oprócz czekania potrzebujesz także:

1. zbierz pierwszy błąd,

2. anuluj inne zadania poprzez `context`,

wtedy bardziej praktyczne jest użycie `errgroup.Group`.

#### Wniosek:

W przypadku zadania „czekaj na zakończenie wszystkich procedur” standardowym
narzędziem jest `sync.WaitGroup`: prosty kontrakt, przewidywalne zachowanie i
niezawodność produkcji.

#### Przykład:

```go
var wg sync.WaitGroup

for i := 0; i < 3; i++ {
	wg.Add(1)
	go func(id int) {
		defer wg.Done()
		fmt.Println("worker", id)
	}(i)
}

wg.Wait()
```

</details>


<details>
<summary>33. Dlaczego wzór `value := value` został użyty w pętlach i czy ma on zastosowanie po wersji 1.22?</summary>

#### Go

Szablon `value := value` był historycznie używany w pętlach `for range` do
tworzenia oddzielnej lokalnej kopii zmiennej i bezpiecznego przechwytywania jej
w zamknięciu, szczególnie w goroutine.

#### Dlaczego było to potrzebne przed wersją 1.22:

1. Zmienna iteracyjna w `range` została w rzeczywistości ponownie użyta pomiędzy
   iteracjami.

2. Zamknięcie często przechwytuje tę samą zmienną zamiast jej „bieżącej”
   wartości.

3. W rezultacie goroutine zobaczyła nieoczekiwane dane (zwykle ostatnią
   wartość).

Dlatego napisali:

`v := v`

aby utworzyć nową zmienną w ramach iteracji.

#### Co się zmieniło od wersji 1.22:

1. Zmieniono semantykę `range`: dla każdej iteracji zmienne pętli mają osobne
   wartości do przechwycenia w zamknięciu.

2. Typowy błąd z „późną” wartością w goroutines został naprawiony na poziomie
   języka.

3. W większości współczesnych przypadków szablon `value := value` nie jest już
   potrzebny.

#### Czy szablon jest aktualny dzisiaj:

1. ** W przypadku kodu gwarantującego działanie w wersji Go 1.22+** – zwykle
   nie.

2. **W przypadku projektów ze starszymi wersjami Go** – tak, może być konieczne.

3. **W przypadku środowisk/bibliotek mieszanych** należy dążyć do najniższej
   obsługiwanej wersji.

#### Wniosek praktyczny:

`value := value` był wzorcem ochronnym przed konkretną pułapką `range`. Po
wersji 1.22 potrzeba tego w większości zniknęła, ale pozostaje istotna w
starszym kodzie lub podczas obsługi starszych wersji.

</details>


<details>
<summary>34. Czy używanie goroutines może spowolnić system i w jakich przypadkach?</summary>

#### Go

Tak, może. Pomimo lekkiego charakteru goroutines, nie są one „darmowe”.
Niewłaściwe lub nadmierne ich użycie może zmniejszyć wydajność, zwiększyć
opóźnienia i skomplikować środowisko wykonawcze.

#### Kiedy goroutines mogą spowolnić system:

1. **Nadmierna liczba goroutines (eksplozja goroutine):** tysiące lub setki
   tysięcy zadań bez ograniczania konkurencji wywierają presję na program
   planujący i pamięć.

2. **Zadania szczegółowe:** jeśli praca jest bardzo mała, narzut związany z
   uruchomieniem/koordynacją może być większy niż praca użyteczna.

3. **Intensywna synchronizacja:** częste blokowanie (`mutex`, kanały, `select`)
   powoduje rywalizację i zmniejsza przepustowość.

4. **Nieudana wymiana danych przez kanały:** nadmiarowe przekazywanie dużych
   ładunków lub złożone topologie typu fan-in/fan-out mogą kosztować więcej niż
   prostsze modele.

5. **Brak przeciwciśnienia:** gdy producenci generują pracę szybciej niż
   konsumenci ją przetwarzają, kumulują się kolejki, rośnie pamięć i opóźnienia.

6. **Problemy z we/wy i zasobami zewnętrznymi:** nadmierna równoległość może
   przeciążyć bazę danych, sieć, system plików lub interfejsy API innych firm,
   degradując cały system, a nie go przyspieszając.

#### Jak uniknąć degradacji:

1. Konkurencja graniczna (pula procesów roboczych, semafor, ograniczone
   kolejki).

2. Profil (`pprof`, ślad) zamiast polegać na intuicji.

3. Zmniejsz współdzielony stan zmienny i zablokuj rywalizację.

4. Wybierz rozmiar równoległości zgodnie z rzeczywistym obciążeniem pracą i
   zasobami.

#### Wniosek:

Horoutines przyspieszają system tylko wtedy, gdy kontrolowana jest równoległość.
W produkcji zasada jest prosta: nie „więcej goroutin”, ale „wystarczająca ilość
goroutines z właściwymi granicami i synchronizacją”.

</details>


<details>
<summary>35. Jaka jest różnica między kanałami buforowanymi i niebuforowanymi? Kiedy należy używać slice + mutex zamiast kanałów?</summary>

#### Go

Kanały w Go mogą być buforowane lub niebuforowane i ta różnica określa semantykę
synchronizacji pomiędzy goroutinami. Wybór typu kanału jest wyborem modelu
koordynacji, a nie tylko „kwestią techniczną”.

#### Kanał niebuforowany (`make(chan T)`):

1. **Wymiana synchroniczna:** `send` jest blokowana do czasu, aż inna goroutine
   wykona odpowiednią `receive` (i odwrotnie).

2. **Wyraźne przekazanie:** jest dobre, gdy wymagana jest ścisła synchronizacja
   kroków.

3. **Minimalna kolejka:** dane nie kumulują się w kanale.

#### Kanał buforowany (`make(chan T, n)`):

1. **Więcej interakcji asynchronicznej:** `send` nie blokuje, dopóki jest
   miejsce w buforze.

2. **Zarządzana kolejka:** pozwala wygładzić krótkie szczyty obciążenia.

3. ** Przeciwciśnienie ze względu na pojemność:** gdy bufor jest pełny, `send`
   ponownie się blokuje.

#### Gdy zamiast kanałów odpowiednie jest `slice + mutex`:

1. **Wymaga współdzielonego bufora z nietrywialnymi operacjami:** usuwanie
   partii, zmiana kolejności, dostęp losowy, złożone reguły agregacji.

2. **Kiedy model ma „stan współdzielony z jawną blokadą”, a nie przepływ
   komunikatów:** kanały nie zawsze są najłatwiejszym narzędziem do
   modyfikowalnych kolekcji.

3. **Gdy istotna jest subtelna optymalizacja pamięci/układu:** `slice` zapewnia
   bardziej bezpośrednią kontrolę nad strukturą i operacjami danych.

4. **Kiedy architektura kanału tworzy niepotrzebną złożoność:** czasami `mutex`
   z wyraźnym niezmiennikiem jest prostszy, bardziej czytelny i szybszy.

#### Praktyczna zasada wyboru:

1. **Kanały** — do przekazywania zdarzeń/wiadomości pomiędzy niezależnymi
   goroutinami przypominającymi aktora.

2. **`slice + mutex`** — do zarządzania kolekcją współdzieloną z bogatym
   zestawem operacji stanowych.

#### Wniosek:

Kanały buforowane i niebuforowane różnią się poziomem synchroniczności wymiany.
Alternatywa `slice + mutex` jest uzasadniona, gdy potrzebna jest zarządzana
struktura stanu współdzielonego, a nie transport wiadomości.

#### Przykład:

```go
unbuf := make(chan int)    // надсилання чекає отримувача
buf := make(chan int, 100) // надсилання не блокується, поки є місце

buf <- 1
buf <- 2
```

</details>


<details>
<summary>36. Co się stanie, gdy kanał `nil` zostanie odczytany, zapisany lub zamknięty?</summary>

#### Go

Kanał `nil` w Go to kanał bez zainicjowanego wewnętrznego bufora i mechanizmów
synchronizacji. Jego zachowanie jest ściśle określone i bardzo ważne dla logiki
konkurencji.

#### Zachowanie kanału `nil`:

1. **Czytanie z `nil`-kanału** - blokuje na zawsze.

2. **Zapis na kanale `nil`** - blokuje na zawsze.

3. **Zamknięcie kanału `nil`** - powoduje panikę.

#### Dlaczego tak:

1. Kanał `nil` nie ma struktury „na żywo”, za pośrednictwem której można
   wymieniać informacje.

2. W związku z tym operacje wysyłania/odbioru nie mogą zostać pomyślnie
   zakończone.

3. `close(nil)` jest zabronione, ponieważ tak naprawdę nie ma co zamykać.

#### Konsekwencje praktyczne:

1. W normalnym kodzie losowy kanał `nil` często prowadzi do zakleszczenia.

2. W `select` może to być celowe narzędzie:

- oddział z kanałem `nil` staje się nieaktywny;

- tak dynamicznie „wyłącz” konkretny przypadek bez dodatkowych flag.

#### Wniosek:

Dla kanału `nil` wysyłanie/odbieranie — wieczne blokowanie i `close` — panika.
Ta właściwość jest zarówno źródłem typowych błędów, jak i potężną techniką
kontroli `select`, jeśli jest używana celowo.

</details>


<details>
<summary>37. Jak i dlaczego używać kanałów `nil` w `select`? Dlaczego kanał `nil` blokuje się na zawsze i jak z tego korzystać?</summary>

#### Go

Kanał `nil` w `select` to kontrolowany sposób dynamicznego włączania i
wyłączania poszczególnych gałęzi. Ponieważ operacje na kanale `nil` nie mogą
zostać zakończone, odpowiedni kanał `case` staje się nieaktywny.

#### Dlaczego kanał `nil` blokuje się na zawsze:

1. Kanał nie jest zainicjowany (`var ch chan T`), to znaczy nie ma struktury
   wykonawczej do wysyłania/odbioru.

2. `send` i `receive` nie mają „miejsca spotkania”, więc czekają w
   nieskończoność.

3. W `select` oznacza to: sprawa z tym kanałem nigdy nie zostanie wybrana.

#### Jak z niego korzystać w `select`:

1. **Dynamicznie wyłącz źródło zdarzenia:** przypisz `ch = nil` i gałąź `case
   <-ch:` nie jest już aktywowana.

2. **Zarządzanie cyklem życia etapów rurociągu:** po zakończeniu danego etapu
   rurociąg jest resetowany w celu wykluczenia go z dalszej selekcji.

3. **Unikanie zbędnych flag stanu:** zamiast dodatkowych `if` wewnątrz pętli
   logika stanu jest przenoszona do samego mechanizmu `select`.

#### Praktyczne środki ostrożności:

1. Jeśli wszystkie kanały w `select` staną się `nil` i nie będzie żadnego
   `default`, otrzymasz trwałą blokadę.

2. `close(nil)` powoduje panikę, dlatego nie należy mylić zerowania i
   zamknięcia.

3. Kod z `nil`-kanałami wymaga wyraźnych niezmienników, w przeciwnym razie łatwo
   jest uzyskać zakleszczenie trudne do debugowania.

#### Wniosek:

Kanał `nil` w `select` to elegancki przełącznik aktywności obudowy. Jest to
przydatne w przypadku logiki kontrolowanej współbieżności, o ile stany są
dokładnie kontrolowane i unika się sytuacji, w której wszystkie ścieżki ulegają
zakleszczeniu.

#### Przykład:

```go
var in <-chan int = source
for {
	select {
	case v, ok := <-in:
		if !ok {
			in = nil // вимикаємо гілку
			continue
		}
		_ = v
	case <-ctx.Done():
		return
	}
}
```

</details>


<details>
<summary>38. Kiedy należy używać `select` z gałęzią `default` i jakie scenariusze to obejmuje?</summary>

#### Go

`select` z odgałęzieniem `default` sprawia, że operacja nie jest blokowana:
jeśli żaden kanał nie jest gotowy do wymiany, sterowanie natychmiast przechodzi
do `default`. Jest to przydatne w przypadku kontrolowanej reakcji, ale
niebezpieczne, jeśli jest używane bezmyślnie.

#### W stosownych przypadkach:

1. **Scenariusze „próba wysłania/odbioru”:** należy wypróbować wymianę i, jeśli
   w tej chwili nie jest to możliwe, wybrać alternatywną ścieżkę bez blokowania.

2. **Pętle zdarzeń z pracą w tle:** gdy w oczekiwaniu na zdarzenia goroutine
   powinna wykonywać akcje pomocnicze (bicie serca, sprzątanie, telemetria
   świetlna).

3. ** Przeciwciśnienie i kontrolowane odciążanie:** jeśli bufor jest pełny,
   `default` może odmówić/opóźnić zadanie zamiast blokować całą pętlę.

4. **Miękkie limity czasu/odpytywanie statusu:** w połączeniu z `time.Ticker`
   lub inną logiką pozwala nie „zawieszać się” w oczekiwaniu na kanał.

#### Jakie ryzyko obejmuje i stwarza:

1. **Obejmuje ryzyko zamarznięcia** w krytycznych obszarach, w których
   blokowanie jest niedopuszczalne.

2. **Może jednak utworzyć pętlę zajętości** (aktywne wirowanie procesora), jeśli
   `default` uruchamia się zbyt często bez przerwy i znaczącej pracy.

#### Praktyczne środki ostrożności:

1. Nie używaj `default`, jeśli pożądane jest blokowanie synchronizacji.

2. W pętlach dodaj kontrolę tempa (`ticker`, `sleep`, limity), aby uniknąć
   marnowania zużycia procesora.

3. Wyraźnie napraw politykę: co robimy, gdy kanał nie jest gotowy (upuść, ponów
   próbę, kolejka, dziennik, metryka).

#### Wniosek:

`select` z `default` to nieblokujące narzędzie współbieżności. Jest to właściwe,
gdy priorytetem jest reaktywność i zarządzanie obciążeniem, ale wymaga
dyscypliny, aby nie zamienić cyklu przetwarzania w nieefektywne aktywne
odpytywanie.

</details>


<details>
<summary>39. Jak działa `select` podczas odbierania danych z wielu kanałów jednocześnie?</summary>

#### Go

Jeśli jest wiele gotowych `case`, gdy zostanie wykonane `select`, Go wybiera
jeden z nich pseudolosowo. Ma to na celu uniknięcie sztywnego priorytetu
pierwszej gałęzi i ograniczenie systematycznego „głodu” poszczególnych kanałów.

#### Co dzieje się krok po kroku:

1. Runtime sprawdza wszystkie `case` w `select`.

2. Definiuje zestaw gotowych operacji (wysyłanie/odbieranie, które można teraz
   wykonać).

3. Jeśli jeden `case` jest gotowy, zostaje wykonany.

4. Jeśli kilka jest gotowych, jeden jest wybierany pseudolosowo.

5. Jeśli żaden nie jest gotowy:

- wykonuje `default` (jeśli istnieje),

- w przeciwnym razie `select` zostanie zablokowany, dopóki przynajmniej jeden
  `case` nie będzie gotowy.

#### Konsekwencje praktyczne:

1. **Nie ma gwarancji zlecenia przetwarzania** pomiędzy jednocześnie gotowymi
   kanałami.

2. **Nie można zakodować priorytetu biznesowego** tylko w zamówieniu `case` w
   `select`.

3. **Zachowanie jest poprawne pod względem konkurencyjnym, ale
   niedeterministyczne**, co jest normalne w przypadku logiki sterowanej
   zdarzeniami.

#### Jak wdrożyć priorytet, jeśli jest to potrzebne:

1. Zbuduj układ dwufazowy `select` (najpierw kanał krytyczny, potem wspólny).

2. Użyj oddzielnych kolejek/programu planującego priorytety.

3. Egzekwuj wyraźną politykę uczciwości/priorytetu w warstwie aplikacji, zamiast
   polegać na randomizacji w czasie wykonywania.

#### Wniosek:

Jeśli jednocześnie dostępnych jest kilka kanałów, `select` wybiera jeden losowo
(pseudolosowo). Jest to dobra strategia zapewniająca ogólną uczciwość, ale
ustalenie priorytetów wymaga wyraźnej logiki architektonicznej oprócz
podstawowej `select`.

</details>


<details>
<summary>40. Jak bezpiecznie zamknąć kanał w Go, jeśli pisze do niego wiele goroutines?</summary>

#### Go

Podstawowa zasada Go: kanał jest zamykany przez **kto jest właścicielem strony
zapisu** i dopiero wtedy, gdy wszystkie operacje `send` zostaną zakończone.
Skrypt z wieloma procedurami pisania wymaga koordynacji ukończenia.

#### Bezpieczne podejście (kanoniczne):

1. Uruchom kilka podprogramów piszących.

2. Każdy pisarz sygnalizuje to po zakończeniu pracy (`WaitGroup.Done()`).

3. Oddzielna procedura kontrolna czeka na `wg.Wait()`.

4. Dopiero wtedy wywołuje `close(ch)`.

#### Dlaczego jest to bezpieczne:

1. Żadna goroutine nie pisze na kanale po `close`.

2. Unika paniki `send on closed channel`.

3. Zamknięcie następuje dokładnie raz na kontrolowany punkt.

#### Czego nie można zrobić:

1. Pozwól każdemu autorowi na niezależne zamknięcie udostępnionego kanału.

2. Zamknij kanał „na wszelki wypadek” z wielu lokalizacji.

3. Wychwytywanie paniki jako „mechanizmu synchronizacji” jest antywzorcem.

#### Dodatkowe praktyki:

1. W przypadku wcześniejszego zatrzymania użyj oddzielnego `done/context`
   zamiast `close(dataCh)` po stronie czytnika.

2. Jeśli chcesz zagwarantować jednorazowe zamknięcie w złożonej topologii, użyj
   `sync.Once`.

#### Wniosek:

W scenariuszu z wieloma programami piszącymi kanał jest bezpiecznie zamykany
przez koordynatora po wyraźnym potwierdzeniu wykonania wszystkich podprogramów
piszących. Zasada jest prosta: **wielu nadawców, jeden bliżej, ostatecznie
wysyła**.

#### Przykład:

```go
ch := make(chan int)
var wg sync.WaitGroup

for i := 0; i < 5; i++ {
	wg.Add(1)
	go func(v int) {
		defer wg.Done()
		ch <- v
	}(i)
}

go func() {
	wg.Wait()
	close(ch) // один координатор закриває канал
}()
```

</details>


<details>
<summary>41. Jak zaimplementować semafor przez kanał buforowany?</summary>

#### Go

W Go semafor jest naturalnie modelowany przez kanał buforowany o stałej
pojemności. Liczba slotów w buforze jest równa maksymalnej dozwolonej liczbie
jednoczesnych operacji (równoległość).

#### Zasada działania:

1. **Pobierz (zajmij miejsce):** przed rozpoczęciem pracy goroutine wykonuje
   `sem <- token`. Jeżeli bufor jest pełny, wysyłanie jest blokowane.

2. **Zwolnienie (zwolnienie gniazda):** po zakończeniu goroutine wykonuje
   `<-sem`. W ten sposób zostaje zwolnione miejsce na następne zadanie.

#### Typowa forma:

- `sem := make(chan struct{}, N)`

- `N` — limit jednocześnie aktywnych zadań.

- `struct{}` jest wybrany jako lekki token bez ładunku.

#### Dlaczego jest skuteczny:

1. **Prosty model przeciwciśnienia:** Nadmiarowe zadania naturalnie czekają.

2. **Przejrzysta synchronizacja:** Środowisko wykonawcze Go wykonuje
   blokadę/wzbudzenie bez ręcznego sterowania zmiennymi warunkowymi.

3. **Dobrze odczytany z kodu:** zamiar „ograniczenia konkurencji” jest
   natychmiast widoczny.

#### Praktyczne środki ostrożności:

1. Zawsze wykonuj `release` zamiast `defer`, aby uniknąć utraty miejsca w
   przypadku błędu.

2. Aby anulować oczekiwanie, użyj `select` z `context.Done()`.

3. Nie należy mylić semafora (limitu równoległości) z kolejką zadań (pulą
   procesów roboczych).

#### Wniosek:

Buforowany kanał w Go to kanoniczna implementacja semafora zliczającego: prosta,
niezawodna i dobrze zintegrowana z modelem goroutine. To jeden z najlepszych
sposobów kontrolowania poziomu konkurencji w usługach produkcyjnych.

#### Przykład:

```go
sem := make(chan struct{}, 10) // максимум 10 одночасних задач

run := func(job Job) {
	sem <- struct{}{}         // зайняти слот
	defer func() { <-sem }() // звільнити слот
	job.Do()
}
```

</details>


<details>
<summary>42. Jak zaimplementować wzorce `Fan-in` i `Fan-out`?</summary>

#### Go

`Fan-out` i `Fan-in` to podstawowe wzorce współbieżności w Go for zarządzanej
równoległości: pierwszy rozdziela pracę między wielu wykonawców, drugi zbiera
wyniki z powrotem do wspólnego wątku.

#### `Fan-out` (rozgałęzianie obciążenia):

1. Występuje kanał powodujący problemy.

2. Uruchamia `N` procedurę procesu roboczego.

3. Każdy pracownik czyta ze wspólnego kanału wejściowego i przetwarza jego
   część.

#### `Fan-in` (wyniki łączenia):

1. Kilka kanałów producentów lub wyniki pracowników.

2. Indywidualne procedury scalania wysyłają dane do jednego kanału wyjściowego.

3. Po zakończeniu wszystkich gałęzi scalających kanał wyjściowy zostaje
   zamknięty.

#### Typowy schemat architektoniczny:

1. `jobs` kanał → `fan-out` dotyczący pracowników.

2. Każdy pracownik pisze do `results`.

3. `fan-in` łączy `results` (lub kilka `results`-kanałów) w jeden kanał na
   potrzeby następnego etapu potoku.

#### Niezwykle ważne zasady:

1. Zamykanie kanałów powinno być scentralizowane i jednorazowe.

2. Użyj `WaitGroup` do koordynowania zakończenia pracy.

3. W przypadku wcześniejszego zakończenia użyj `context`/`done`, aby uniknąć
   wycieków goroutine.

4. Kontroluj rozmiar buforów i poziom równoległości, aby uniknąć przeciążenia
   pamięci lub zależności zewnętrznych.

#### Wniosek:

`Fan-out` skaluje przetwarzanie, `Fan-in` zwraca kontrolę nad strumieniem
wynikowym. Razem stanowią podstawę najbardziej efektywnych rozwiązań potokowych
w usługach Go.

</details>


<details>
<summary>43. Dlaczego nie powinieneś używać kanałów do przesyłania dużych ilości danych?</summary>

#### Go

Kanały w Go to świetne narzędzie do koordynowania i przekazywania
wydarzeń/małych wiadomości, ale nie są najlepszym sposobem transportu ogromnych
ładunków. W przypadku dużych ilości danych często powodują niepotrzebne
obciążenie.

#### Dlaczego to może nie być skuteczne:

1. **Koszt kopiowania:** przekazywanie dużych wartości przez kanał zwiększa
   liczbę operacji pamięciowych i ruch pomiędzy goroutines.

2. **Koszty rywalizacji i synchronizacji:** kanały mają wewnętrzną koordynację
   dostępu; przy dużym obciążeniu może stać się wąskim gardłem.

3. **GC i zużycie pamięci:** duże bufory kanałów lub liczne duże komunikaty
   zwiększają wykorzystanie pamięci i mogą zwiększać koszty przerw/czasu
   działania.

4. **Degradacja lokalizacji pamięci podręcznej:** duże obiekty przechodzą przez
   konkurencyjny rurociąg gorzej niż sygnały kompaktowe + dostęp do
   współdzielonej pamięci.

#### Lepsze alternatywy:

1. Transfer kanałem **linków/uchwytów/indeksów**, a nie dużych zbiorów danych.

2. Trzymaj ładunek we współdzielonym buforze/puli i używaj kanału jako sygnału
   gotowości.

3. W stosownych przypadkach użyj puli procesów roboczych z kontrolowanym
   dostępem do współdzielonej struktury danych (`slice/map + mutex`).

#### Kiedy kanały są nadal odpowiednie:

1. Dla małych komunikatów kontrolnych.

2. Dla zdarzeń, poleceń, statusów i sygnałów zakończenia.

3. Dla potoku, w którym przesuwa się lekki kontekst metadanych.

#### Wniosek:

Kanał w Go to przede wszystkim mechanizm synchronizacji i koordynacji. W
przypadku dużych danych skuteczniejsze jest rozdzielenie: przesyłania informacji
„co należy zrobić” kanałem i najbardziej masywnych ładunków — za pośrednictwem
bardziej odpowiednich struktur pamięci.

</details>


<details>
<summary>44. Jak poprawnie zwrócić błąd z goroutine do głównego wątku? </summary>

#### Go

Procedura nie może „zwrócić” wartości bezpośrednio poprzez `return` do osoby
wywołującej. Dlatego błąd z zadania współbieżnego jest przekazywany jawnie:
kanałem błędu lub poprzez `errgroup`, który hermetyzuje ten wzorzec.

#### Podejścia kanoniczne:

1. **`errgroup.Group` + `context` (zalecane):** najlepsze do uruchamiania grupy
   goroutines, zbierania pierwszego błędu i anulowania pozostałych zadań.

2. **Oddzielne `errCh` + `WaitGroup`:** wyraźna kontrola nad cyklem życia; po
   zakończeniu wszystkich procesów roboczych kanał zostaje zamknięty, a główny
   wątek odczytuje błędy.

#### Kluczowe zasady poprawności:

1. Błędy przesyłane są w jednym uzgodnionym kanale/agregatorze.

2. Zamknięcie `errCh` jest wykonywane przez koordynatora po zakończeniu
   wszystkich procedur zapisu.

3. W przypadku pierwszego błędu krytycznego inne zadania należy zatrzymać za
   pomocą `context` (aby uniknąć bezużytecznej pracy i wycieków goroutine).

4. Błędów w konkurencyjnych gałęziach nie można zignorować - powoduje to „ciche”
   defekty.

#### Typowa strategia przetwarzania:

1. Uruchom pracowników z dostępem do `ctx`.

2. W przypadku błędu wyślij `error` do agregatora.

3. Anuluj kontekst (jeśli wymagana jest zasada szybkiego działania).

4. Poczekaj na zakończenie wszystkich procedur.

5. Zwróć uzgodniony wynik (pierwszy błąd lub błąd zagregowany).

#### Wniosek:

Poprawny błąd „powrotu” z goroutine to dyscyplina jawnego kanału komunikacji
oraz zarządzanie cyklem życia za pośrednictwem `WaitGroup`/`errgroup` i
`context`. W produkcji najczęściej optymalnym wyborem jest `errgroup`.

#### Przykład (wersja 1.22+):

```go
g, ctx := errgroup.WithContext(context.Background())

for _, task := range tasks {
	g.Go(func() error {
		return task.Run(ctx)
	})
}

if err := g.Wait(); err != nil {
	return err
}
```

</details>


<details>
<summary>45. Czy `defer` w Go może złapać (`recover`) panikę, która wystąpiła w gorutynie podrzędnej?</summary>

#### Go

Krótka odpowiedź: **nie**. `recover` działa tylko w tej samej procedurze gor, w
której wystąpiła panika, i tylko w funkcji `defer` wykonywanej na stosie
wywołań.

#### Główna zasada:

1. Panika nie „przelatuje” pomiędzy goroutinami jako kontrolowany sygnał dla
   `recover`.

2. `defer` w nadrzędnej procedurze gor nie może wychwycić paniki dziecka.

3. Aby wywołać panikę w procedurze roboczej, `defer` z `recover` musi znajdować
   się w tej konkretnej procedurze roboczej.

#### Konsekwencje praktyczne:

1. Jeśli panika w podprogramie podrzędnym nie zostanie wykryta lokalnie, proces
   może ulec awarii.

2. W przypadku stabilnych usług każda „ryzykowna” gorutyna jest owinięta folią
   ochronną `defer func(){ if r := recover(); r != nil { ... } }()`.

3. Po `recover` należy wyraźnie zasygnalizować awarię obwodu głównego (poprzez
   kanał `error`, `errgroup`, metryki, logowanie).

#### Co jest uważane za dobrą praktykę:

1. Lokalny `recover` w miejscu wypuszczenia długowiecznych pracowników.

2. Jasne zasady: panika zamienia się w błąd/ostrzeżenie i nie znika po cichu.

3. Używanie `context` do skoordynowanego zakończenia innych goroutines po
   krytycznej awarii.

#### Wniosek:

`recover` w Go ma zasięg lokalny — pojedynczą procedurę gor. Dlatego
przechwytywanie paniki w konkurencyjnym kodzie musi być zaprojektowane osobno na
poziomie każdej procedury podrzędnej.

</details>


<details>
<summary>46. Porozmawiaj o wzorcach konkurencji w Go.</summary>

#### Go

Wzorce współbieżności w Go to powtarzalne wzorce architektoniczne służące do
koordynowania goroutines, potoków i prymitywów synchronizacji. Ich celem jest
zapewnienie łatwej do opanowania równoległości bez chaosu, wycieków i
zakleszczeń.

#### Najczęściej używane wzorce:

1. **Pula pracowników**

- stała liczba procedur roboczych odczytuje zadania z kolejki;

- ogranicza poziom równoległości i stabilizuje ładunek.

2. **Wentylacja / Wentylacja**

- `fan-out`: przydział jednej kolejki zadań wielu wykonawcom;

- `fan-in`: Łączenie wyników z wielu źródeł w jeden kanał.

3. **Rurociąg (przenośnik etapów)**

- dane przechodzą przez kolejne etapy przetwarzania;

- każdy etap może mieć własną konkurencję i przeciwciśnienie.

4. **Semafor poprzez kanał buforowany**

- ogranicza liczbę jednoczesnych operacji;

- przydatny do pracy z bazami danych, deskryptorami plików, zewnętrznymi API.

5. **Anulowanie kontekstu**

- scentralizowane anulowanie całej grupy goroutines;

- zapobiega wyciekom w przypadku przekroczenia limitu czasu, błędu lub
  zamknięcia.

6. **Errgroup (bezawaryjna orkiestracja)**

- zbiera błędy z grupy zadań;

- wygodnie łączy się z `context`, aby wcześniej zatrzymać resztę pracy.

7. **Jeden właściciel / Pętla przypominająca aktora**

- jedna goroutine ma stan zmienny;

- inni komunikują się za pośrednictwem wiadomości, ograniczając rywalizację o
  blokady.

8. **Publikuj/Subskrybuj (transmisja)**

- zdarzenia są wysyłane do wielu odbiorców;

- wymaga dokładnego monitorowania buforów i cyklu życia subskrybenta.

#### Podstawowe zasady dotyczące wszystkich wzorców:

1. Jasne zasady dotyczące własności zasobów i zamykania kanałów.

2. Ograniczenia konkursu (nie „nieskończone” goroutiny).

3. Wymagana ścieżka zakończenia (`context`, `done`, `WaitGroup`).

4. Obserwowalność: metryki, rejestrowanie, profilowanie.

#### Wniosek:

Siła Go nie leży w „samych goroutinach”, ale w dyscyplinie wzorców. Jest to
właściwa kombinacja puli procesów roboczych, potoków, włączania i wyłączania,
anulowania i koordynacji błędów, która zapewnia skalowalność, przewidywalność i
niezawodność produkcji systemów.

</details>


<details>
<summary>47. Kiedy używać `sync.Mutex` i kiedy używać `sync.RWMutex`?</summary>

#### Go

`sync.Mutex` i `sync.RWMutex` rozwiązują ten sam problem — chronią stan
współdzielony, ale przy użyciu innego modelu konkurencji. Właściwy wybór zależy
od profilu dostępu do danych: proporcji odczytów i zapisów, czasu trwania sekcji
krytycznych oraz poziomu rywalizacji.

#### `sync.Mutex` — kiedy wybrać:

1. **Zapisy mieszane lub częste:** jeśli operacje zapisu nie są częste, korzyści
   płynące z `RWMutex` są często zanegowane.

2. **Krótkie sekcje krytyczne:** proste blokowanie/odblokowywanie zwykle
   zapewnia przewidywalne i szybkie działanie.

3. **Podstawowy wybór domyślny:** mniejsza złożoność, mniejsze ryzyko błędnego
   modelu zamka.

4. **Gdy ważna jest łatwość konserwacji:** `Mutex` jest łatwiejsza do
   odczytania, debugowania i profilowania.

#### `sync.RWMutex` — kiedy ma to sens:

1. ** Dominują odczyty, zapisy są rzadkie:** wielu jednoczesnych czytelników
   może pracować równolegle.

2. **Odczyty są stosunkowo długie:** równoległy dostęp do odczytu zapewnia
   rzeczywisty wzrost przepustowości.

3. **Konkurencja w zakresie odczytu jest duża:** i istnieją dowody empiryczne na
   to, że wąskim gardłem staje się blokada odczytu.

#### Ważne uwagi:

1. `RWMutex` nie jest „automatycznie szybszy” — ze względu na bardziej złożoną
   koordynację wewnętrzną może działać wolniej przy rzeczywistych obciążeniach.

2. Czytniki są nadal blokowane podczas częstych operacji zapisu.

3. Ostatecznego wyboru należy dokonać w oparciu o profilowanie (`pprof`,
   benchmarki), a nie intuicję.

#### Ogólna zasada:

1. Zacznij od `sync.Mutex`.

2. Przejdź do `sync.RWMutex` tylko wtedy, gdy istnieje scenariusz z dużą ilością
   odczytów i udowodniony wzrost wydajności.

#### Wniosek:

`sync.Mutex` to niezawodna wartość domyślna dla większości zadań. `sync.RWMutex`
to narzędzie do optymalizacji punktowej dla obciążeń zorientowanych na
czytelnika, gdzie zysk jest potwierdzany metrykami.

</details>


<details>
<summary>48. Dlaczego nie można skopiować obiektów `sync.Mutex`?</summary>

#### Go

`sync.Mutex` zawiera stan blokady wewnętrznej. Kopiowanie takiego obiektu już po
pierwszym użyciu stwarza niebezpieczną sytuację: pojawiają się dwa różne
przypadki stanu blokady, które programista może błędnie uznać za jeden.

#### Dlaczego jest to zasadniczo zabronione:

1. **Mutex to nie tylko „dane”, ale element podstawowy synchronizacji
   stanowej.**

2. **Kopia nie ma tego samego stanu blokady** co oryginał.

3. To narusza gwarancje wzajemnego wykluczenia i może prowadzić do wyścigu,
   impasu lub paniki w złożonych scenariuszach.

#### Typowe sposoby przypadkowego skopiowania muteksu:

1. Przekaż strukturę zawierającą `sync.Mutex` według wartości do funkcji.

2. Po inicjalizacji/użyciu zwróć następującą strukturę według wartości.

3. Zachowaj/przekaż kopie za pośrednictwem kanałów lub kolekcji wartości.

#### Prawidłowa praktyka:

1. Struktury z `sync.Mutex` należy używać poprzez wskaźniki (`*T`), a nie
   poprzez kopiowanie wartości.

2. Nie eksportuj `Mutex` bezpośrednio do publicznego interfejsu API.

3. Jeżeli typ posiada blokadę, należy udokumentować, że nie zostanie skopiowany
   po pierwszym użyciu.

4. Użyj `go vet` (blokad kopiujących) i lintersów do wczesnego wykrywania.

#### Wniosek:

`sync.Mutex` nie można skopiować, ponieważ podważa to sam model synchronizacji.
Zapamiętaj zasadę: elementy podstawowe zamka mają stabilną tożsamość i muszą
istnieć w jednej instancji na każdy stan chroniony.

</details>


<details>
<summary>49. Dlaczego odczytywanie i zapisywanie stanu współdzielonego bez synchronizacji jest wyścigiem danych, nawet jeśli jest „logicznie bezpieczne”?</summary>

#### Go

Jeśli chodzi o model pamięci Go, `data race` występuje, gdy dwie lub więcej
gorprogramów jednocześnie uzyskuje dostęp do tej samej zmiennej, z których co
najmniej jedna jest operacją zapisu, i nie ma ustalonej relacji `happens-before`
(tj. synchronizacji) pomiędzy tymi dostępami.

#### Dlaczego „logicznie bezpieczny” nie zapisuje:

1. **Logika w głowie programisty ≠ gwarancja modelu pamięci.** Bez
   synchronizacji nie jest zdefiniowana kolejność widoczności rekordów pomiędzy
   rdzeniami/wątkami.

2. **Optymalizacje kompilatora i procesora mogą zmienić obserwowaną kolejność**
   odczytów/zapisów w dozwolonym modelu pamięci.

3. **Niestabilność pod obciążeniem:** kod może „działać” podczas lokalnego
   uruchamiania, ale może wystąpić przerwa w produkcji lub CI.

#### Jakie są konsekwencje rasy:

1. Odczytywanie nieaktualnych lub częściowo zaktualizowanych wartości.

2. Niepowtarzalne błędy (heisenbugs), które są trudne do debugowania.

3. Naruszenie niezmienników stanu biznesowego bez wyraźnej paniki.

#### Co uważa się za prawidłową synchronizację:

1. `sync.Mutex` / `sync.RWMutex`

2. Atomics (`sync/atomic`) dla prostych scenariuszy niskiego poziomu

3. Kanały jako mechanizm własności/sygnalizacji

4. `WaitGroup`, `Cond`, `Once`, `context` — w swoich rolach koordynacyjnych

#### Wniosek:

Bez synchronizacji współdzielony odczyt/zapis w Go to z definicji wyścig,
niezależnie od subiektywnego „bezpieczeństwa logicznego”. Jedynym niezawodnym
sposobem jest jawne utworzenie relacji `happens-before` za pomocą poprawnych
operacji podstawowych współbieżności.

</details>


<details>
<summary>50. Co to jest stan wyścigu i jak działa detektor `-race`? Co może, a czego nie może wykryć?</summary>

#### Go

`Race Condition` to ogólna klasa defektów współbieżności, w których wynik
programu zależy od nieprzewidywalnej kolejności zdarzeń pomiędzy wątkami
wykonania. `Data race` to szczególny przypadek sytuacji wyścigu, która odnosi
się do niebezpiecznego jednoczesnego dostępu do tej samej pamięci bez
synchronizacji.

#### Jak działa `-race`:

1. Podczas `go test -race` / `go run -race` kod jest instrumentowany.

2. Runtime śledzi odczyty/zapisy pamięci pomiędzy goroutines.

3. W przypadku wykrycia dostępu bez `happens-before` (i istnieje rekord) —
   zgłaszany jest `data race` ze śladami stosu.

#### Co `-race` dobrze wykrywa:

1. Klasyczne wyścigi odczytu/zapisu i zapisu/zapisu na zmiennych
   współdzielonych.

2. Nieodebrane zablokowanie/odblokowanie w obszarach konkurencyjnych.

3. Część błędów koordynacji w scenariuszach testowych z prawdziwą konkurencją.

#### Czego `-race` nie gwarantuje:

1. **Nie wykrywa wszystkich warunków wyścigu jako błędów logicznych:** np.
   nieprawidłowy protokół interakcji bez bezpośredniego wyścigu danych.

2. **Nie widzi niezrealizowanego kodu:** jeśli testy nie obejmują ścieżki
   konkurencyjnej, wyścig może pozostać niezauważony.

3. **Nie jest wolny od błędów:** „Czysty” przebieg oznacza jedynie, że narzędzie
   nie wykrył w jego trakcie żadnych naruszeń.

4. **Ma narzut:** spowolnienie i zwiększone zużycie pamięci w trybie
   oprzyrządowania.

#### Wniosek praktyczny:

`-race` jest obowiązkowym narzędziem zapewniającym konkurencyjną higienę kodu,
ale nie jest absolutną wyrocznią poprawności. Jego moc ujawnia się w połączeniu
z testami jakości, niezmiennikami projektowymi i dyscypliną synchronizacji.

</details>


<details>
<summary>51. Jakie są zalety operacji atomowych w porównaniu z mutexem w przypadku prostych operacji konkurencyjnych?</summary>

#### Go

Operacje `atomic` w Go są odpowiednie w bardzo prostych scenariuszach
konkurencyjnych, w których trzeba bezpiecznie wykonać elementarną operację na
pojedynczej wartości (inkrementacja, odczytanie flagi, CAS). W takich
przypadkach mogą być lżejsze niż `mutex`.

#### Zalety podejścia atomowego:

1. **Mniejsze obciążenie w przypadku prostych operacji:** brak wyraźnego
   `Lock/Unlock` wokół krótkiej operacji.

2. **Wysoka wydajność w licznikach i flagach gorącej ścieżki:** np. metryki,
   stany stop/start, lekka koordynacja.

3. **Brak blokowania w klasycznym sensie:** wątki nie muszą czekać na
   właściciela blokady w celu atomowego odczytu/zapisu.

4. ** Jasne gwarancje kolejności pamięci poprzez API `sync/atomic`:** zapewniona
   jest poprawna widoczność pomiędzy goroutinami dla określonej zmiennej.

#### Kiedy atom jest lepszy niż muteks:

1. Operacja dotyczy **jednej** zmiennej lub stanu bardzo lokalnego.

2. Logika jest prosta i dobrze sformalizowana (`Load`, `Store`, `Add`,
   `CompareAndSwap`).

3. Wymaga minimalnego opóźnienia na ścieżce wysokiej częstotliwości.

#### Kiedy mutex jest lepszy:

1. A **niezmiennik między wieloma polami** musi być chroniony.

2. Operacja obejmuje kilka kroków z logiką domeny.

3. Czytelność i łatwość konserwacji są ważniejsze niż mikrooptymalizacja.

#### Ważna uwaga:

Atomic nie jest uniwersalnym zamiennikiem `mutex`. Nadmierne użycie atomów
komplikuje kod i zwiększa ryzyko subtelnych błędów w modelu pamięci.

#### Wniosek:

Zaletą operacji atomowych jest szybka i tania synchronizacja w prostych
przypadkach. W przypadku złożonych niezmienników stanu współdzielonego i
biznesowego `mutex` jest zwykle bardziej niezawodnym narzędziem.

</details>


<details>
<summary>52. Jak działa `sync.WaitGroup` i co się stanie, jeśli licznik będzie ujemny? Dlaczego nie można wywołać `wg.Done()` przed `wg.Add()`?</summary>

#### Go

`sync.WaitGroup` to licznik aktywnych zadań konkurencyjnych. Jego celem jest
umożliwienie jednej goroutine (`Wait`) poczekania, aż inne zakończą swoją pracę.

#### Jak to działa:

1. `wg.Add(n)` zwiększa licznik o `n` (dodajemy liczbę zadań).

2. Każde ukończone zadanie wyzwala `wg.Done()` (odpowiednik `Add(-1)`).

3. `wg.Wait()` jest blokowany do momentu osiągnięcia przez licznik zera.

#### Co się stanie z licznikiem ujemnym:

1. To jest logiczny błąd koordynacji.

2. Środowisko wykonawcze powoduje panikę (zwykle: `sync: negative WaitGroup
   counter`).

3. Ta sytuacja oznacza, że ​​`Done()` został wywołany więcej razy niż `Add()`.

#### Dlaczego nie możesz zrobić `Done()` do `Add()`:

1. Naruszona została umowa dotycząca cyklu życia zadania.

2. `Wait()` może zakończyć się przedwcześnie, ponieważ w momencie oczekiwania
   licznik nie odzwierciedla jeszcze rzeczywistej liczby zleceń.

3. W najgorszym przypadku otrzymamy negatywny licznik i panikę.

#### Prawidłowa dyscyplina:

1. Zadzwoń `Add(1)` **zanim** rozpocznie się goroutine.

2. Wewnątrz goroutyny ustaw `defer wg.Done()` bezpośrednio przy wejściu.

3. Zadzwoń `Wait()` dopiero po zarejestrowaniu wszystkich zadań.

#### Wniosek:

`WaitGroup` jest niezawodny tylko w ścisłej sekwencji `Add -> go -> Done ->
Wait`. Licznik ujemny i `Done()` do `Add()` to sygnał zepsutego modelu
synchronizacji, co nieuchronnie prowadzi do niestabilnego zachowania lub paniki.

#### Przykład:

```go
var wg sync.WaitGroup
wg.Add(1)

go func() {
	defer wg.Done()
	work()
}()

wg.Wait()
```

</details>


<details>
<summary>53. Jaka jest różnica między `sync.WaitGroup` i `errgroup.Group`? Kiedy używać każdego z nich?</summary>

#### Go

`sync.WaitGroup` i `errgroup.Group` koordynują realizację goroutines, ale mają
różne poziomy abstrakcji: `WaitGroup` tylko czeka, podczas gdy `errgroup`
dodatkowo obsługuje błędy i anulowanie poprzez `context`.

#### `sync.WaitGroup`:

1. Odpowiada tylko za oczekiwanie na zakończenie zadań.

2. Nie rejestruje błędów od razu po wyjęciu z pudełka.

3. Nie anuluje automatycznie innych goroutines.

4. Wymaga infrastruktury ręcznej:

- kanał błędu;

- koordynacja `context`;

- niezawodna logika.

#### `errgroup.Group`:

1. Umożliwia uruchamianie goroutines przez `Go(func() error)`.

2. Zwraca pierwszy błąd otrzymany w `Wait()`.

3. W połączeniu z `errgroup.WithContext` automatycznie anuluje kontekst w
   przypadku błędu.

4. Redukuje standardowe wzorce dla typowego wzorca „zadania równoległe +
   zatrzymanie w przypadku błędu”.

#### Kiedy wybrać `WaitGroup`:

1. Po prostu poczekaj na zakończenie bez agregacji błędów.

2. Zasady obsługi błędów są niestandardowe i całkowicie niestandardowe.

3. Kontrola niskiego poziomu jest ważniejsza niż wygoda API.

#### Kiedy wybrać `errgroup`:

1. Potrzebuje jasnego modelu „niepowodzenie w jednym zadaniu → zatrzymaj
   resztę”.

2. Musisz szybko i sprawnie wdrożyć konkurencyjną orkiestrację.

3. Ważna jest czytelność i krótki, łatwy w utrzymaniu kod.

#### Wniosek:

`WaitGroup` - element podstawowy synchronizacji „tylko czekaj”. `errgroup` -
wyższy poziom: „poczekaj + zwróć błąd + anuluj resztę poprzez kontekst”. W
przypadku większości scenariuszy produkcyjnych z błędami i semantyką
zapewniającą szybką awarię `errgroup` jest bardziej praktyczny.

</details>


<details>
<summary>54. Opisz cel i implementację `sync.Once` - w jaki sposób gwarantuje jednorazową inicjalizację?</summary>

#### Go

`sync.Once` przeznaczony jest do gwarantowanego jednorazowego wykonania funkcji
w warunkach równoczesnego dostępu. Niezależnie od liczby goroutines wywołujących
`once.Do(f)` w tym samym czasie, treść `f` musi zostać wykonana tylko raz.

#### Do czego się go używa:

1. Leniwa inicjalizacja zasobów singletonu.

2. Jednorazowa konfiguracja/ładowanie pamięci podręcznej.

3. Bezpiecznie przeprowadzaj intensywną inicjalizację bez powielania pracy.

#### Jak `sync.Once` gwarantuje powtarzalność:

1. Sprawdza wewnętrzną flagę stanu wykonanego/nieudanego.

2. Jeśli inicjalizacja nie została jeszcze wykonana — blokuje synchronicznie
   konkurentów.

3. Dokładnie jedna goroutine wykonuje `f`.

4. W przypadku powodzenia oznacza stan jako „gotowy” i dalej `Do` powraca bez
   ponownego uruchamiania `f`.

#### Ważne właściwości:

1. Zapewniona jest prawidłowa widoczność zainicjowanych danych dla innych
   goroutines (bezpieczeństwo pamięci poprzez wewnętrzną synchronizację).

2. Inne goroutines, które pojawiły się podczas wykonywania `f`, będą czekać na
   zakończenie.

3. `Once` nie jest przeznaczony do „ponownego uruchamiania” — jest to
   jednorazowy cykl życia.

#### Niuanse i ostrzeżenia:

1. Jeśli `f` wpada w panikę, zachowanie to wymaga dokładnego rozważenia przy
   projektowaniu: `Once` nie jest mechanizmem awaryjnym.

2. Nie powinieneś ukrywać zbyt złożonej logiki biznesowej w `Do`; lepiej jest
   tam zachować inicjalizację zasobu.

3. Zadania resetowania/przeładowania wymagają innych wzorców (wskaźnik atomowy,
   muteks, stan wersjonowania itp.).

#### Wniosek:

`sync.Once` to zdyscyplinowany prymityw jednorazowej inicjalizacji: bezpieczny
pod względem wyścigowym, przewidywalny i bardzo przydatny tam, gdzie ponowne
uruchomienie inicjalizacji jest albo zbędne, albo niebezpieczne.

</details>


<details>
<summary>55. Co to jest `sync.Cond` i kiedy zastępuje kanał?</summary>

#### Go

`sync.Cond` to prymityw synchronizacji warunkowej: pozwala gorutynom czekać, aż
określony stan (warunek) stanie się prawdziwy i zostać obudzonym sygnałem z
innej goroutiny.

#### Model podstawowy `sync.Cond`:

1. `Cond` działa na `Locker` (zwykle `*sync.Mutex`).

2. Procedura w pętli sprawdza warunek pod blokadą.

3. Jeśli warunek jest fałszywy — wywołuje `Wait()`.

4. Inna goroutine wywołuje `Signal()` lub `Broadcast()` po zmianie stanu.

#### Kluczowe metody:

1. **`Wait()`** — atomowo zwalnia zamek, zasypia, a po przebudzeniu ponownie
   chwyta zamek.

2. **`Signal()`** — budzi jedną oczekującą procedurę.

3. **`Broadcast()`** - budzi wszystkich oczekujących.

#### Gdy przeważa kanał `sync.Cond`:

1. **Złożony warunek dotyczący stanu współdzielonego, a nie przesyłania
   komunikatu:** gdy ważne jest oczekiwanie na „predykat nad stanem” i nie
   odbieranie ładunku.

2. **Wielu kelnerów w jednym zasobie chronionym blokadą:** `Cond` w bardziej
   naturalny sposób wyraża koordynację wokół stanu współdzielonego.

3. **Wymagana precyzyjna kontrola wybudzania:** `Signal/Broadcast` są czasami
   lepiej dopasowane niż semantyka kanału.

4. **Scenariusze o wysokiej częstotliwości z minimalnym szumem alokacji:** w
   niektórych przypadkach niskiego poziomu `Cond` daje bardziej efektywny model
   niż budowanie dodatkowych protokołów kanałów.

#### Kiedy kanał jest lepszy:

1. Kiedy zadaniem jest przesyłanie zdarzeń/danych pomiędzy niezależnymi
   aktorami.

2. Kiedy ważny jest prosty model potoku i czytelny przepływ komunikatów.

3. Kiedy nie chcesz zarządzać udostępnionym stanem zmiennym w stanie
   zablokowanym.

#### Wniosek:

`sync.Cond` to narzędzie „czekające na zmianę warunku muteksu”, podczas gdy
kanał to narzędzie „przekazujące wiadomość”. `Cond` dominuje tam, gdzie centrum
logiki stanowi sam stan i jego niezmienniki, a nie transport danych.

</details>


<details>
<summary>56. Jak jest zorganizowany `sync.Map`, kiedy zapewnia lepszą wydajność w porównaniu z mapą + mutex i gdzie jest używany w standardowej bibliotece?</summary>

#### Go

`sync.Map` to wyspecjalizowana mapa konkurencji z pakietu `sync`,
zoptymalizowana przede wszystkim pod kątem obciążeń wymagających dużej liczby
odczytów i scenariuszy, w których klucze są często odczytywane i rzadko
zmieniane.

#### Jak `sync.Map` jest zorganizowany koncepcyjnie:

1. Posiada dwuwarstwowy model dostępu:

- **część do odczytu** do szybkich odczytów, w większości bez blokad;

- **brudna część** dla aktualizacji i nowych wpisów w trakcie synchronizacji.

2. Odczyt z „gorącej” strefy odczytu często odbywa się bez wspólnego muteksu, co
   zmniejsza rywalizację.

3. Zapisy/promocje międzywarstwowe mają bardziej złożoną logikę wewnętrzną, ale
   nie mają na celu karania odczytów masowych.

#### Gdy `sync.Map` może być szybszy niż `map + mutex`:

1. **Wiele odczytów, kilka zapisów** (klasyczny odczyt – głównie obciążenie).

2. **Klucze w większości stabilne**, bez agresywnej rezygnacji.

3. **Wysoce konkurencyjny dostęp do odczytu** z wielu goroutines.

#### Kiedy więcej znaczy lepiej `map + mutex`:

1. Wpisów jest wiele lub dominują.

2. Wymaga złożonych niezmienników dla wielu kluczy.

3. Bezpieczeństwo typu jest ważniejsze (ponieważ `sync.Map` działa poprzez
   `any`).

4. Potrzebuje prostszej i bardziej oczywistej logiki, którą zespół będzie mógł
   wspierać.

#### Gdzie jest używany w bibliotece standardowej:

`sync.Map` jest używany w wewnętrznych pamięciach podręcznych i tabelach, gdzie
charakter dostępu jest bliski intensywnemu odczytowi (w szczególności w
częściach środowiska wykonawczego/standardowych pakietów do buforowania
metadanych i struktur pomocniczych). Kluczowa idea jest wszędzie taka sama:
zminimalizować blokowanie odczytów masowych.

#### Wniosek:

`sync.Map` nie jest „najlepszą mapą ogólnie”, ale narzędziem punktowym dla
określonego profilu obciążenia. Jeśli masz scenariusz obejmujący głównie
czytanie i dużą konkurencję, może to zapewnić wygraną; w innych przypadkach
proste `map + mutex` jest często bardziej przejrzyste i wydajne.

</details>


<details>
<summary>57. Czym są testy współbieżności w Go i dlaczego się je stosuje?</summary>

#### Go

Testy współbieżności w Go to testy testujące zachowanie kodu w warunkach
równoległego wykonywania goroutines, współdzielenia stanu i konkurencji zasobów.
Ich celem jest wykrycie defektów, które nie pojawiają się w scenariuszu
liniowym.

#### Co dokładnie sprawdzają poniższe testy:

1. Poprawność synchronizacji (`mutex`, `channel`, `atomic`, `WaitGroup`).

2. Brak wyścigu danych w stanie udostępnionym.

3. Odporność na scenariusze zakleszczenia/blokady na żywo.

4. Prawidłowe wykonanie goroutines (brak wycieków).

5. Przestrzeganie niezmienników pod obciążeniem konkurencyjnym.

#### Dlaczego są potrzebne:

1. **Wczesne wykrywanie błędów konkurencyjnych:** wiele z nich pojawia się tylko
   pod presją równoległości.

2. **Ograniczenie niestabilności w środowisku produkcyjnym:** testy przechwytują
   scenariusze, w których kolejność zdarzeń jest niedeterministyczna.

3. **Zapewnienie gwarancji architektonicznych:** takich jak to, że system nie
   traci zdarzeń i nie narusza spójności stanu.

4. **Bezpieczniejsza refaktoryzacja:** konkurencyjne niezmienniki pozostają
   chronione przez zestaw regresji.

#### Narzędzia i praktyki w Go:

1. `go test -race` jako obowiązkowy poziom weryfikacji.

2. Równoległe skrypty poprzez goroutines, `t.Run`, `t.Parallel`.

3. Wyraźne limity czasu/`context`, aby zapobiec zawieszaniu się testów.

4. Przebiegi obciążeniowe i wielokrotne przebiegi w celu zwiększenia ryzyka
   odtworzenia błędów niedeterministycznych.

#### Wniosek:

Konkurencyjne testy nie są „dodatkowym luksusem”, ale niezbędnym elementem
jakości usług Go. Sprawdzają nie tylko funkcjonalność, ale także poprawność
współdziałania goroutin w rzeczywistych warunkach równoległości.

</details>


<details>
<summary>58. Dlaczego Go używa `context.Context` i jak jest przekazywany przez drzewo wywołań funkcji?</summary>

#### Go

`context.Context` w Go to standardowy mechanizm zarządzania cyklem życia
żądań/operacji: anulowaniami, terminami, przekroczeniami limitów czasu i
metadanymi żądań. Pozwala wszystkim gałęziom wykonania zobaczyć pojedynczy
sygnał „stop”.

#### Dlaczego potrzebujesz `Context`:

1. **Anulowanie:** zatrzymanie pracy, która nie jest już potrzebna (klient się
   rozłączył, wystąpił błąd w pobliskim oddziale, usługa kończy się).

2. **Termin/limit czasu:** ogranicz czas wykonywania operacji (HTTP, DB,
   zewnętrzne API), aby nie zawieszać się w nieskończoność.

3. **Wartości o zakresie żądania:** przesyłaj dane żądania usługi (identyfikator
   śledzenia, token uwierzytelniania, identyfikator dzierżawy) między warstwami.

#### Jak jest przekazywany przez drzewo wywołań:

1. `ctx` jest przekazywany jako **pierwszy parametr** do funkcji, która może
   blokować lub wykonywać operacje we/wy.

2. Każde wywołanie podrzędne otrzymuje to samo `ctx` lub pochodną:

- `context.WithCancel`

- `context.WithTimeout`

- `context.WithDeadline`

- `context.WithValue`

3. Konteksty podrzędne tworzą drzewo:

- anulowanie kontekstu nadrzędnego powoduje anulowanie wszystkich kontekstów
  podrzędnych;

- terminy są dziedziczone (lub zawężane).

#### Zasady praktyczne:

1. Nie przechowuj `Context` w strukturze jako pola o długim czasie życia.

2. Nie przekazuj kontekstu `nil` (użyj `context.Background()` lub
   `context.TODO()`).

3. Nie używaj `WithValue` w przypadku parametrów biznesowych, które muszą być
   jawnymi argumentami funkcji.

#### Wniosek:

`context.Context` to zapytanie „układ nerwowy” w Go. Rozprzestrzenia kontrolę
czasu i anulowania w całym drzewie wywołań, dzięki czemu konkurencyjny kod jest
łatwy w zarządzaniu, ekonomiczny i przewidywalny w środowisku produkcyjnym.

#### Przykład:

```go
func handler(w http.ResponseWriter, r *http.Request) {
	ctx := r.Context()
	if err := service.Do(ctx); err != nil {
		http.Error(w, err.Error(), 500)
	}
}

func (s *Service) Do(ctx context.Context) error {
	ctx, cancel := context.WithTimeout(ctx, 2*time.Second)
	defer cancel()
	return s.repo.Call(ctx)
}
```

</details>


<details>
<summary>59. Czy `context.Context` jest niezmienne i co to oznacza w praktyce?</summary>

#### Go

Tak, `context.Context` jest koncepcyjnie niezmienny: po utworzeniu istniejący
kontekst nie jest „edytowany”, ale nowy kontekst pochodny jest budowany na
wierzchu kontekstu nadrzędnego.

#### Co oznacza niezmienność w przypadku `Context`:

1. Połączenia `WithCancel`, `WithTimeout`, `WithDeadline`, `WithValue` nie
   zmieniaj starego `ctx`.

2. Zwracają **nowy** kontekst potomka.

3. Kontekst nadrzędny pozostaje niezmieniony.

#### Konsekwencje praktyczne:

1. **Bezpieczna propagacja między goroutinami:** ten sam `ctx` można przekazywać
   bez ryzyka „ukrytego nadpisania” parametrów.

2. **Przejrzysty cykl życia:** Drzewo kontekstu wyraźnie pokazuje, kto
   odziedziczył po kim anulowanie/termin.

3. **Zamierzone zachowanie API:** funkcja, która otrzymała `ctx`, nie może
   podstępnie „przekręcić” jej do innych wywołań; może stworzyć jedynie
   lokalnego potomka.

4. ** Lepsza testowalność i debugowanie:** łatwiej jest dokładnie prześledzić,
   gdzie pojawił się limit czasu/anulowanie/wartość, ponieważ są to oddzielne
   węzły pochodne, a nie mutacje pojedynczego obiektu.

#### Ważne wyjaśnienie:

Niezmienność nie oznacza, że w środku nie ma dynamiki: sygnał anulowania i stan
terminu ostatecznego mogą zmieniać się w czasie. Jest to jednak zmiana **stanu
wykonania** w modelu kontekstowym, a nie „lokalna” mutacja kontraktu API
przekazanego obiektu.

#### Wniosek:

`context.Context` w Go to model łańcucha funkcyjnego: nie zmieniamy
istniejącego, lecz tworzymy jego pochodną. Zapewnia to przejrzystą kompozycję,
bezpieczną współbieżność i przewidywalne zarządzanie cyklem życia zapytań.

</details>


<details>
<summary>60. W jaki sposób użycie `context.WithCancel` pomaga uniknąć wycieków goroutine?</summary>

#### Go

`context.WithCancel` daje zarządzany sygnał zakończenia wszystkim procedurom gor
działającym w tym samym drzewie kontekstu. Jest to klucz do zapobiegania
wyciekowi gorutyny — sytuacji, w której goroutiny pomocnicze pozostają „żywe”,
gdy praca straci na znaczeniu.

#### Jak dochodzi do wycieku goroutine:

1. Procedura czeka na kanał/sieć/zegar bez warunku zatrzymania.

2. Żądanie już się zakończyło lub stało się niepotrzebne, ale pracownik o tym
   nie wiedział.

3. Takie „osierocone” goroutiny gromadzą i zużywają zasoby.

#### Rola `WithCancel`:

1. Tworzenie kontekstu podrzędnego: `ctx, cancel := context.WithCancel(parent)`.

2. Wszystkie procedury robocze mają `select` z gałęzią `case <-ctx.Done():`.

3. Kiedy zostanie wywołane `cancel()`, wszystkie zależne goroutines otrzymają
   sygnał stopu.

4. Grutyny kończą się w kontrolowany sposób, uwalniając zasoby.

#### Praktyczne zasady bezpieczeństwa:

1. Zawsze wywołuj `cancel()` (często przez `defer cancel()`), nawet po pomyślnym
   zakończeniu.

2. W każdej długotrwałej operacji pętli/blokowania sprawdź `ctx.Done()`.

3. Pomiń `ctx` wszystkie wywołania we/wy obsługujące anulowanie.

4. Połącz z `WaitGroup`/`errgroup`, aby poczekać na faktyczne zakończenie.

#### Co daje systemowi:

1. Nieobecność „wiszących” pracowników w tle.

2. Lepsze wykorzystanie procesora/pamięci pod obciążeniem.

3. Przewidywane zamknięcie i stabilniejsze działanie usługi.

#### Wniosek:

`context.WithCancel` to podstawowy mechanizm zapobiegający wyciekom w
współbieżności Go: pojedynczy wyraźny sygnał stopu, który w spójny sposób kończy
wszystkie powiązane goroutines i chroni system przed nadmiernym zużyciem
zasobów.

</details>


<details>
<summary>61. Dlaczego Go używa niestandardowych typów kluczy (np. `struct{}`) dla `context.WithValue` i jak to zapobiega kolizjom?</summary>

#### Go

W `context.WithValue` klucz musi być porównywalny, ale co najważniejsze, musi
być **unikalny w obrębie aplikacji i przestrzeni zależności**. Dlatego zaleca
się stosowanie własnych (niestandardowych) typów kluczy zamiast powszechnie
używanych `string`.

#### Dlaczego klucze `string` są niebezpieczne:

1. Różne pakiety mogą przypadkowo użyć tego samego ciągu (`"userID"`,
   `"request_id"` itp.).

2. Wartość w kontekście zostanie nadpisana lub „przyćmiona” przez inny pakiet.

3. Uzyskaj ciche, trudne do odtworzenia błędy
   routingu/uwierzytelniania/logowania.

#### Jak typ niestandardowy zapobiega kolizjom:

1. Tworzy typ klucza prywatnego w pakiecie, na przykład: `type ctxKey struct{}`
   lub `type ctxKey int`.

2. Kod zewnętrzny nie może przypadkowo użyć tego samego typu klucza i wartości.

3. W ten sposób kluczowa przestrzeń nazw zostaje odizolowana na poziomie
   typowego systemu.

#### Dlaczego często używa się `struct{}`:

1. Lekki znacznik bez ładunku.

2. Podkreśla, że ​​ważna jest tożsamość klucza, a nie jego „dane”.

3. Dobrze odpowiada idiomowi „unikalny klucz lokalny pakietu”.

#### Ogólna zasada:

1. Zadeklaruj klucze jako nieeksportowane zmienne pakietu.

2. Nie używaj „pustych” ciągów jako kluczy dla `WithValue`.

3. Przechowuj w `Context` tylko dane usług o zakresie żądania, a nie parametry
   biznesowe.

#### Wniosek:

Niestandardowe typy kluczy w `context.WithValue` to mechanizm przestrzeni nazw
bezpieczny dla typów. Niezawodnie zmniejszają ryzyko kolizji pomiędzy pakietami
i sprawiają, że wartości kontekstowe są przewidywalne w dużych bazach kodu.

#### Przykład:

```go
type requestIDKey struct{}

func withRequestID(ctx context.Context, id string) context.Context {
	return context.WithValue(ctx, requestIDKey{}, id)
}

func requestID(ctx context.Context) (string, bool) {
	v, ok := ctx.Value(requestIDKey{}).(string)
	return v, ok
}
```

</details>


<details>
<summary>62. Jaka jest różnica między `context.Value` a przekazywaniem parametrów za pomocą argumentów funkcji?</summary>

#### Go

`context.Value` i normalne argumenty funkcji mają różne cele. W kompetentnym
projekcie Go nie są one wymienne: argumenty przekazują dane biznesowe, a
`context.Value` to metakontekst o zasięgu żądania usługi.

#### Przekaż argumenty:

1. **Jawna umowa API:** wszystkie wymagane dane widoczne są w podpisie.

2. **Bezpieczeństwo typów i czytelność:** kompilator pomaga kontrolować
   poprawność.

3. **Najlepszy wybór dla logiki domeny:** parametry domeny muszą być
   przekazywane bezpośrednio.

#### `context.Value`:

1. **Niejawny kanał danych usługi:** identyfikator śledzenia, identyfikator
   żądania, oświadczenia autoryzacji, dzierżawca, metadane korelacji.

2. **Propaguje przez warstwy bez powiększania sygnatur:** przydatne w przypadku
   oprogramowania pośredniczącego, rejestrowania i obserwowalności.

3. **Mniejsza przejrzystość:** zależność wartości nie jest oczywista na
   podstawie sygnatury funkcji.

#### Dlaczego nie powinieneś zastępować argumentów `context.Value`:

1. Spada przejrzystość interfejsu API (pojawiają się „ukryte” dane wejściowe).

2. Zwiększa ryzyko błędów w czasie wykonywania z powodu asercji z `any`.

3. Testy i refaktoryzacja są skomplikowane.

#### Ogólna zasada:

1. W `Context` jest tylko to, co należy do cyklu życia żądania i jest potrzebne
   warstwom infrastruktury.

2. W parametrach funkcji - wszystko, co stanowi istotę działania
   przedsiębiorstwa.

#### Wniosek:

Argumenty tworzą wyraźną umowę domeny; `context.Value` zawiera metadane usługi
żądania. Mieszanie tych ról degraduje architekturę, więc profesjonalny kod Go
sprawia, że ​​granica między nimi jest wyraźna.

</details>


<details>
<summary>63. Jak działa alokacja stosu i sterty w Go?</summary>

#### Go

W Go rozmieszczenie danych na stosie lub stercie jest określane przez kompilator
na podstawie analizy ucieczki. Programista nie wybiera tego bezpośrednio
ręcznie, ale może napisać kod, aby zmniejszyć niepotrzebne alokacje sterty.

#### Alokacja stosu:

1. Dane znajdują się w wywołaniu funkcji (lub zarządzanym stosie goroutine).

2. Przydział i wydanie są bardzo tanie.

3. Nie ładuje bezpośrednio GC.

#### Alokacja sterty:

1. Wymagane są dane poza bieżącą ramką stosu.

2. Pamięcią zarządza moduł zbierający elementy bezużyteczne.

3. Daje większy narzut (alokacja + późniejsze wyrzucanie elementów
   bezużytecznych).

#### Co decyduje o tym, dokąd trafia wartość:

1. **Analiza ucieczki kompilatora:** jeśli wartość „ucieknie” poza funkcję
   (zwrócony zostanie wskaźnik, zapisany w długotrwałej strukturze, przechwycone
   zostanie zamknięcie itp.), trafia do sterty.

2. **Kontekst użycia:** nawet zmienna lokalna może trafić na stertę, jeśli jej
   czas życia jest dłuższy niż bieżąca ramka.

#### Dlaczego to jest ważne:

1. Więcej alokacji sterty = więcej pracy dla GC.

2. W ścieżce gorącej wpływa na opóźnienia i przepustowość.

3. Optymalizacja alokacji często daje zauważalny wzrost wydajności usług.

#### Wniosek praktyczny:

W Go kluczem nie jest „ręczne zarządzanie pamięcią”, ale zrozumienie zachowań
ucieczki. Przejrzysty projekt danych i minimalizacja niepotrzebnych wycieków w
Heap pomagają w szybkim i stabilnym pisaniu kodu produkcyjnego.

</details>


<details>
<summary>64. Jak zminimalizować alokację sterty za pomocą `sync.Pool`?</summary>

#### Go

`sync.Pool` to tymczasowy mechanizm ponownego wykorzystania obiektu, który
pozwala zmniejszyć częstotliwość alokacji sterty w obszarach gorącego kodu.
Pomysł jest prosty: nie tworzyć za każdym razem od nowa przedmiotów
krótkotrwałych, ale wyjąć je z basenu i zwrócić po użyciu.

#### Schemat podstawowy:

1. Utwórz pulę `New`, która w razie potrzeby inicjuje obiekt.

2. Na wejściu operacji: `obj := pool.Get()`.

3. Przed użyciem należy doprowadzić przedmiot do prawidłowego stanu.

4. Po zakończeniu: wyczyść pola i `pool.Put(obj)`.

#### Dlaczego to zmniejsza przydziały:

1. Część żądań otrzymuje już przydzielone obiekty.

2. Mniej nowych alokacji sterty.

3. Mniejsze obciążenie GC przy dużej częstotliwości krótkich operacji.

#### Gdzie `sync.Pool` jest szczególnie istotne:

1. Bufory (`[]byte`, `bytes.Buffer`) w procedurach serializacji/obsługi sieci.

2. Tymczasowe struktury pomocnicze w ścieżkach analizy/kodowania/dekodowania.

3. Wysoce obciążone usługi HTTP/RPC z powtarzającymi się krótkimi operacjami.

#### Ważne uwagi:

1. `sync.Pool` to pamięć podręczna, a nie przechowywanie długoterminowe;
   elementy można czyścić metodą GC.

2. Obiekt przed `Put` musi zostać doprowadzony do czystego stanu, w przeciwnym
   razie możliwy jest wyciek danych pomiędzy żądaniami.

3. Basen nie jest panaceum: na zimnych ścieżkach złożoność kodu może się nie
   opłacać.

4. Optymalizację należy potwierdzać profilowaniem, a nie intuicją.

#### Wniosek:

`sync.Pool` jest skuteczny w przypadku ponownego wykorzystania krótkotrwałych
obiektów w gorących ścieżkach, gdzie krytyczne alokacje i pauza GC są krytyczne.
Jej siła polega na ograniczaniu turbulencji alokacyjnych, jednak należy ją
stosować selektywnie i profilować.

</details>


<details>
<summary>65. Co oznaczają zmienne środowiskowe `GOGC` i `GOMEMLIMIT` i jaki mają wpływ na moduł zbierający elementy bezużyteczne?</summary>

#### Go

`GOGC` i `GOMEMLIMIT` to kluczowe parametry sterujące zachowaniem GC w Go.
Pozwalają zrównoważyć zużycie pamięci, częstotliwość usuwania śmieci i wydajność
usług.

#### `GOGC`:

1. Określa docelową szybkość wzrostu sterty przed następnym cyklem GC (w
   procentach).

2. Typowa wartość to `100` (pozwól, aby sterta w przybliżeniu podwoiła się w
   stosunku do danych „na żywo” po poprzednim GC).

3. Więcej `GOGC`:

- mniej cykli GC;

- większe zużycie pamięci;

- potencjalnie niższe obciążenie procesora GC.

4. Mniej niż `GOGC`:

- częstsze GC;

- mniejsza sterta;

- wyższy narzut montażowy.

#### `GOMEMLIMIT`:

1. Ustawia miękki górny limit pamięci, w obrębie którego środowisko wykonawcze
   stara się utrzymać proces.

2. Kiedy pamięć zbliża się do tego limitu, GC działa bardziej agresywnie, nawet
   jeśli `GOGC` pozwala na rzadsze gromadzenie danych.

3. Szczególnie przydatne w kontenerach/orkiestratorach z twardymi limitami
   pamięci.

#### Jak one współpracują:

1. `GOGC` ustawia ogólną „chciwość” wzrostu sterty.

2. `GOMEMLIMIT` działa jak bezpiecznik ograniczający nadmierny wzrost pamięci.

3. W środowisku produkcyjnym połączenie obu parametrów zapewnia najlepszą
   kontrolę nad opóźnieniami i ryzykiem OOM.

#### Podejście praktyczne:

1. Zacznij od ustawień domyślnych.

2. Pomiar `heap`, pauza GC, procesor, opóźnienie końcowe przy rzeczywistym
   obciążeniu.

3. Stopniowo dostosowuj parametry, rejestrując wpływ na SLA.

4. W przypadku kontenerów konieczne jest dopasowanie `GOMEMLIMIT` do limitu
   pamięci platformy.

#### Wniosek:

`GOGC` kontroluje częstotliwość GC poprzez cel wzrostu sterty i `GOMEMLIMIT`
ogranicza pamięć od góry. Razem tworzą praktyczne narzędzie do dostrajania
zachowania usług Go w czasie wykonywania.

</details>


<details>
<summary>66. Co to jest `runtime.SetFinalizer` i czy jest używane w bibliotece standardowej?</summary>

#### Go

`runtime.SetFinalizer` to mechanizm wiązania funkcji finalizatora z obiektem,
który może zostać wywołany przez GC, zanim obiekt zostanie ostatecznie
zwolniony. Ważne: Finalizator nie zapewnia ścisłych gwarancji czasu działania i
nie jest niezawodnym zamiennikiem jawnego `Close`/`Dispose`.

#### Co robi `SetFinalizer`:

1. Rejestruje wywołanie zwrotne dla określonego obiektu sterty.

2. Kiedy obiekt stanie się nieosiągalny, środowisko wykonawcze **może**
   uruchomić finalizator.

3. Obiekt zostanie następnie odebrany w jednym z kolejnych cykli GC.

#### Kluczowe ograniczenia:

1. **Nie ma gwarancji, „kiedy” finalizator zostanie uruchomiony.**

2. **Nie ma gwarancji, że zostanie on wykonany przed zakończeniem procesu.**

3. Finalizatory komplikują analizę cyklu życia i mogą powodować ukryte
   koszty/opóźnienia.

#### Ogólna zasada:

1. W przypadku zasobów (plików, gniazd, uchwytów, połączeń zewnętrznych) zawsze
   używaj jawnego zamknięcia (`defer obj.Close()`).

2. Finalizator jest dozwolony jedynie jako „sieć bezpieczeństwa” chroniąca przed
   błędami użytkowania, a nie jako podstawowy sposób kontrolowania zasobu.

#### Czy używany w bibliotece standardowej:

Tak, używany punktowo w niektórych miejscach niskiego poziomu jako pomocniczy
mechanizm bezpieczeństwa/diagnostyczny, ale nie jako podstawowy model
zarządzania zasobami. Ogólna filozofia biblioteki standardowej polega na
wyraźnym cyklu życia i wyraźnym zamknięciu.

#### Wniosek:

`runtime.SetFinalizer` to specjalistyczne narzędzie z miękkimi gwarancjami. W
produkcji Go jest używany ostrożnie i rzadko; jawne zarządzanie zasobami
pozostaje podstawą niezawodnego kodu.

</details>


<details>
<summary>67. Jak znaleźć wyciek pamięci za pomocą `pprof`?</summary>

#### Go

Wyszukiwanie wycieków pamięci w Przejdź przez `pprof` opiera się na porównywaniu
profili sterty w czasie: jeśli „żywe” obiekty stale rosną bez powrotu do poziomu
podstawowego, mamy oznakę wycieku lub niekontrolowanego zatrzymania referencji.

#### Podstawowa strategia diagnostyczna:

1. Włącz profilowanie (`net/http/pprof`) w usłudze.

2. Usuń wiele profili sterty:

- na początku;

- przy obciążeniu pracą;

- po „cichym” okresie.

3. Porównaj profile (`go tool pprof`, tryb różnicowy), aby znaleźć typy/stosy,
   które stale rosną.

#### Co obejrzeć w `pprof`:

1. **`inuse_space` / `inuse_objects`** — to naprawdę zostaje w pamięci.

2. **Najlepsze alokatory** i ich stosy wywołań.

3. **Wykres wywołań (`web`)** przedstawia miejsce, w którym przechowywane są
   obiekty długowieczne.

4. Dynamika po kilku cyklach GC: prawdziwy wyciek nie „wybucha”.

#### Typowe źródła wycieków:

1. Mapa globalna/skrytka podręczna bez zasad eksmisji.

2. Niewyczyszczone bufory/kolejki/kanały.

3. Procedury niekończące się, które przechowują odniesienia do dużych struktur.

4. Nie udało się zaprojektować pul lub „na zawsze” kolekcji metryk/etykiet.

#### Techniki praktyczne:

1. Uruchamiaj profile przy reprezentatywnym obciążeniu.

2. Dodaj migawki porównawcze przed/po naprawie.

3. Przyjrzyj się równolegle profilowi ​​goroutine (`goroutine`) — wycieki
   goroutine często korelują z wyciekami pamięci.

#### Wniosek:

`pprof` pozwala znaleźć wyciek pamięci nie „na oko”, ale w sposób ewidentny: ze
względu na wzrost wskaźników `inuse` i określonych stosów przechowywania.
Kluczem do sukcesu jest porównanie profili czasowych przy stabilnym,
powtarzalnym obciążeniu.

</details>


<details>
<summary>68. Jak znaleźć gorące ścieżki i zmierzyć przepustowość?</summary>

#### Go

`Hot paths` to sekcje kodu, w których program zużywa najwięcej czasu i zasobów.
Aby je poprawnie znaleźć, nie trzeba intuicji, ale profilowania pod rzeczywistym
lub zbliżonym do rzeczywistego obciążeniem.

#### Jak znaleźć gorące ścieżki:

1. **Profilowanie procesora (`pprof`):** pokazuje, gdzie zużywany jest najwięcej
   czasu procesora.

2. **Profile sterty/alloc:** pomagają znaleźć „gorące” ścieżki alokacji, które
   często powodują pośrednią degradację poprzez GC.

3. **Trace (`go tool trace`):** daje obraz harmonogramu, blokad i opóźnień
   pomiędzy goroutines i we/wy.

4. **Wykres płomienia / góra / wykres połączeń:** wizualizuj, które funkcje
   stanowią główny koszt.

#### Jak mierzyć przepustowość:

1. Zdefiniuj wskaźniki biznesowe dotyczące przepustowości:

- req/s, msg/s, zadania/s, wiersze/s itp.

2. Przeprowadź kontrolowane testy obciążenia:

- stałe wejście;

- znany profil konkurencyjny;

- stabilne środowisko startowe.

3. Usuń jednocześnie dane:

- przepustowość;

- opóźnienie (p50/p95/p99);

- CPU, pamięć, GC, rywalizacja o blokadę.

4. Porównaj zmiany „przed/po” w tych samych warunkach (najlepiej w wielokrotnych
   seriach).

#### Zasady praktyczne:

1. Optymalizuj tylko to, co potwierdzi profiler.

2. Nie zwiększaj przepustowości kosztem niekontrolowanego wzrostu opóźnień
   końcowych.

3. Po optymalizacji przeprofiluj ponownie, aby upewnić się, że wąskie gardło
   rzeczywiście zniknęło, a nie zostało przesunięte.

#### Wniosek:

Znalezienie gorących ścieżek i pomiar przepustowości to jeden cykl:
**profilowanie → hipoteza → zmiana → powtórzenie pomiaru**. W Go podejście to
jest dobrze wspierane przez standardowe narzędzia i daje solidne rezultaty
inżynieryjne.

</details>


<details>
<summary>69. Jak zoptymalizować obsługę ciągów za pomocą `strings.Builder`? Dlaczego nie możesz łączyć w pętli?</summary>

#### Go

Ciągi znaków są niezmienne w Go. Oznacza to, że każda operacja łączenia tworzy
nowy ciąg. Dlatego powtarzane w pętli `s += part` często generuje lawinę
alokacji i kopii.

#### Dlaczego łączenie w pętli jest nieefektywne:

1. Przy każdej iteracji tworzony jest nowy wiersz.

2. Stara zawartość jest kopiowana w kółko.

3. Całkowity koszt może wzrosnąć kwadratowo w przypadku dużych ilości.

4. Rosnący nacisk na GC z powodu krótkotrwałych obiektów pośrednich.

#### Jak `strings.Builder` pomaga:

1. `Builder` gromadzi dane w wewnętrznym buforze.

2. Wpisy (`WriteString`, `WriteByte`, `WriteRune`) minimalizują zbędne kopie.

3. Ostatnia linia jest generowana jednorazowo do `String()`.

4. Można nazwać `Grow(n)`, jeśli jest to konieczne, aby wstępnie zarezerwować
   pojemność i ograniczyć realokację.

#### Praktyczne zalety:

1. Mniej przydziałów.

2. Większa przepustowość w gorących ścieżkach formatowania/generowania tekstu.

3. Bardziej stabilne zachowanie opóźnień pod obciążeniem.

#### Kiedy szczególnie konieczne jest użycie:

1. Generowanie dużych ładunków (wiersze JSON/SQL/HTML/log).

2. Konstrukcja łańcucha w pętlach.

3. Wszelkie operacje, w których ciąg znaków jest tworzony z wielu fragmentów.

#### Wniosek:

Łączenie w pętli jest kosztowne ze względu na powtarzające się alokacje i
kopiowanie niezmiennych wierszy. `strings.Builder` to idiomatyczne i wydajne
narzędzie do konstruowania ciągów znaków w Go, szczególnie w miejscach
wrażliwych na wydajność.

#### Przykład:

```go
var b strings.Builder
b.Grow(1024)

for _, part := range parts {
	b.WriteString(part)
}

result := b.String()
```

</details>


<details>
<summary>70. Jak zoptymalizować serializację? </summary>

#### Go

Optymalizacja serializacji w Go to przede wszystkim praca z alokacjami, formatem
danych, ponownym wykorzystaniem bufora i redukcją odbić w gorących ścieżkach.
Najlepszy efekt daje tylko profilowane podejście, a nie „ślepe”
mikrooptymalizacje.

#### Praktyczne strategie optymalizacyjne:

1. **Wybór formatu zadania:**

- JSON jest wygodny i wszechstronny, ale cięższy niż procesor;

- Protobuf/MessagePack są często szybsze i bardziej kompaktowe dla ruchu między
  usługami.

2. **Zmniejszenie alokacji:**

- ponowne użycie `bytes.Buffer` / `[]byte` przez `sync.Pool`;

- unikaj niepotrzebnych obiektów pośrednich podczas
  porządkowania/unieszkodliwiania.

3. **Serializacja wątku:**

- użyj `Encoder/Decoder` w przypadku dużych strumieni, aby uniknąć jednoczesnego
  przechowywania całego ładunku w pamięci.

4. **Optymalizacja struktury danych:**

- usuń niepotrzebne pola;

- użyj poprawnych tagów (`omitempty`, w razie potrzeby skrótów klawiszowych);

- unikaj nadmiernie zagnieżdżonych struktur, chyba że wymaga tego logika
  biznesowa.

5. **Unikanie zbędnych odbić w ścieżce gorącej:**

- w krytycznych miejscach rozważ generowanie kodu lub ręczną zoptymalizowaną
  (de)serializację.

6. **Kontrola wielkości ładunku:**

- kompresja jest odpowiednia tylko po pomiarach, ponieważ zwiększa koszty
  procesora;

- czasami lepiej przesłać mniej danych niż „lepiej” skompresować.

#### Jak ocenić efekt:

1. Wzorce (`go test -bench`) przed/po.

2. Profile procesora/alokacji (`pprof`).

3. Metryki produkcyjne: przepustowość, opóźnienie p95/p99, sterta, GC.

#### Wniosek:

Optymalna serializacja to równowaga formatu, alokacji i złożoności kodu. W Go
najlepszą praktyką jest profilowanie, czyszczenie zbędnych kopii, ponowne
wykorzystywanie buforów i wybieranie formatu spełniającego wymagania konkretnego
systemu.

</details>


<details>
<summary>71. Jak zoptymalizować pracę z plikami?</summary>

#### Go

Optymalizacja operacji we/wy plików w Go polega na wyborze odpowiedniego wzorca
odczytu/zapisu, rozmiaru bufora, poziomu współbieżności i strategii dyskowej.
Głównym celem jest ograniczenie wywołań systemowych, zbędnych kopii i
zakleszczeń.

#### Kluczowe praktyki:

1. **Buforowane we/wy (`bufio.Reader/Writer`):** zmniejsza liczbę małych
   `read/write` i zwiększa przepustowość.

2. **Przetwarzanie wsadowe zamiast dostępu bajt po bajcie:** odczyt/zapis w
   blokach jest znacznie wydajniejszy niż małe operacje.

3. **Tworzenie dużych plików:** nie ładuj całego pliku do pamięci, jeśli można
   go przetworzyć w częściach.

4. **Właściwe postępowanie z uchwytami:** `defer file.Close()` natychmiast po
   otwarciu – podstawowa higiena w celu uniknięcia wycieków FD.

5. **Kontrola współbieżności:** równoległość jest użyteczna tylko w obrębie
   przepustowości dysku/FS; nadmierne równoległe operacje we/wy mogą zmniejszyć
   opóźnienia.

6. **Zminimalizuj zbędne kopie:** użyj `io.Copy` i ponownie wykorzystaj bufory,
   jeśli to konieczne.

7. **Profilowanie przed optymalizacją:** sprawdza, czy wąskie gardło leży po
   stronie dysku, procesora, serializacji czy synchronizacji.

#### Dodatkowe wskazówki techniczne:

1. W przypadku dzienników/zdarzeń należy wziąć pod uwagę zasady opróżniania
   (częste opróżniania = niższa przepustowość).

2. W przypadku dużych potoków należy oddzielić odczyt, przetwarzanie i zapis w
   łatwych do zarządzania etapach.

3. W przypadku krytycznych scenariuszy sprawdź ustawienia systemu plików i
   kontenera/hosta (przydział we/wy, typ wolumenu, pamięć sieciowa).

#### Wniosek:

Efektywna praca z plikami w Go to dziedzina buforowania, przesyłania
strumieniowego, kontrolowanej równoległości i pomiarów. Optymalizacja powinna
opierać się na rzeczywistym profilu obciążenia, a nie na ogólnych założeniach.

</details>


<details>
<summary>72. Jak działa przetwarzanie wsadowe i kiedy jest to właściwe?</summary>

#### Go

`Batching` to połączenie wielu małych operacji w większe pakiety (partie) w celu
zmniejszenia narzutu każdej pojedynczej operacji. W systemach o dużym obciążeniu
jest to jeden z najskuteczniejszych sposobów zwiększenia przepustowości.

#### Jak działa grupowanie:

1. Zdarzenia/rekordy gromadzą się w buforze.

2. Pakiet jest wysyłany zgodnie z jednym z wyzwalaczy:

- osiągnięty rozmiar `N`;

- przekroczenie limitu czasu `T`;

- ukończono/odebrano równo.

3. Operacja wykonywana jest poprzez jedno wywołanie „wsadowe” (baza danych,
   sieć, dysk, kolejka).

#### Dlaczego jest skuteczny:

1. **Mniej wywołań systemowych i podróży w obie strony.**

2. **Lepsze ładowanie kanału I/O** (sieć, dysk, baza danych).

3. **Mniejsze obciążenie związane z synchronizacją** w przypadku dużej liczby
   małych zadań.

#### Kiedy porcjowanie jest właściwe:

1. Masowe operacje tego samego typu (logowanie, telemetria, zbiorcze
   wstawianie/aktualizacja).

2. Scenariusze, w których przepustowość jest ważniejsza niż minimalne możliwe
   opóźnienie jednostki.

3. Integracje, w których system zewnętrzny dobrze współpracuje z żądaniami
   wsadowymi.

#### Kiedy grupowanie może być szkodliwe:

1. Rygorystyczne wymagania dotyczące opóźnienia pojedynczej operacji.

2. Niepowodzenie konfiguracji rozmiaru partii/limitu czasu, zwiększające się
   opóźnienie końcowe.

3. Wysokie ryzyko utraty dużego bloku danych bez odpowiedniej logiki
   ponawiania/usuwania danych.

#### Zasady praktyczne:

1. Ustaw **rozmiar i czas** (`N` + `T`) w tym samym czasie.

2. Wykonaj wyraźne opróżnienie przy zamykaniu.

3. Zapewnij ponowną próbę/wycofanie w przypadku częściowych lub całkowitych
   niepowodzeń żądań wsadowych.

4. Zmierz przepustowość ↔ równowagę opóźnień przy rzeczywistym obciążeniu.

#### Wniosek:

Batch to mnożnik wydajności architektury dla operacji masowych. Jego moc ujawnia
się tam, gdzie redukcja narzutu na żądanie jest ważniejsza niż natychmiastowa
reakcja na każde pojedyncze zdarzenie.

</details>


<details>
<summary>73. Kiedy generowanie kodu (`go generate`) jest lepsze niż odbicie?</summary>

#### Go

`Code generation` i `reflection` rozwiązują podobne problemy z
metaprogramowaniem, ale mają różne ceny. W Go generowanie kodu często wygrywa
tam, gdzie w produkcji potrzebna jest szybkość, bezpieczeństwo typu i
przewidywalność.

#### Kiedy `go generate` jest lepsze niż odbicie:

1. **Wydajność ścieżki gorącej jest krytyczna:** wygenerowany kod działa bez
   odbicia w czasie wykonywania, więc zwykle jest szybszy i wymaga mniejszych
   alokacji.

2. **Wymagane wysokie bezpieczeństwo typu:** błędy są wykrywane w czasie
   kompilacji, a nie w czasie wykonywania.

3. **Wymagania dotyczące dużych opóźnień/przepustowości:** serializacja,
   mapowanie, kodeki RPC, weryfikacja w żądaniach zbiorczych.

4. **Stabilny kontrakt danych:** gdy schematy są znane z góry i rzadko się
   zmieniają.

5. **Wymaga przejrzystego debugowania:** wygenerowane wywołania można profilować
   i analizować jak zwykły kod Go.

#### Kiedy refleksja jest uzasadniona:

1. Schemat jest dynamiczny i definiowany tylko w czasie wykonywania.

2. Wymaga szybkiego prototypowania lub elastyczności biblioteki uniwersalnej.

3. Niskie wymagania dotyczące wydajności, w przypadku których łatwiej jest
   zaakceptować obciążenie środowiska wykonawczego.

#### Kompromisy `go generate`:

1. Dodaje krok w kompilacji/przepływie pracy.

2. Musi obsługiwać szablony/generatory.

3. Wygenerowany kod zwiększa rozmiar repozytorium.

#### Wniosek praktyczny:

Jeśli system jest wrażliwy na wydajność, a model domyślny jest stabilny, `go
generate` jest zwykle lepszy niż odbicie. Refleksja jest właściwa tam, gdzie
główną wartością jest dynamika, a nie maksymalna efektywność działania.

</details>


<details>
<summary>74. Co to jest analiza ucieczki i jak ją sprawdzić za pomocą flag kompilatora?</summary>

#### Go

`Escape Analysis` to analiza kompilatora Go, która określa, czy wartość może
pozostać na stosie, czy też musi zostać przydzielona na stercie, ponieważ
„ucieka” z bieżącej ramki stosu.

#### Dlaczego jest to ważne:

1. Przydziały stosu są tańsze.

2. Przydziały sterty zwiększają presję GC.

3. Zrozumienie zachowań ucieczki pomaga zoptymalizować gorące ścieżki.

#### Typowe powody ucieczki:

1. Wskaźnik powrotu do wartości lokalnej.

2. Zachowanie wartości w trwałej strukturze.

3. Przejęcie zmiennej przez zamknięcie.

4. Przekazywanie wartości do kontekstów, w których kompilator nie może
   zagwarantować lokalnego cyklu życia.

#### Jak sprawdzić flagi kompilatora:

Najczęściej stosowana metoda:

1. `go build -gcflags="-m" ./...`

2. W celu uzyskania bardziej szczegółowych danych wyjściowych: `go build
   -gcflags="-m -m" ./...`

Wiadomości wyszukiwane są pod kątem takich fraz jak:

- `moved to heap`

- `escapes to heap`

Jest to bezpośredni wskaźnik, że na stosie nie pozostała żadna wartość.

#### Proces praktyczny:

1. Uruchom test porównawczy/profil i znajdź gorący fragment.

2. Sprawdź wyjście ucieczki kompilatora dla tej sekcji.

3. Refaktoryzuj lokalnie (bez pogarszania czytelności).

4. Ponowny efekt (`bench`, `pprof`, przydziały/op).

#### Wniosek:

Analiza ucieczki to „radar” kompilatora do analizy zachowań alokacyjnych.
`-gcflags="-m"` pozwala zobaczyć, gdzie dane wyciekają do sterty i podejmować
świadome decyzje dotyczące optymalizacji pamięci i wydajności.

</details>


<details>
<summary>75. Dlaczego `panic` i `recover` nie zastępują normalnej obsługi błędów?</summary>

#### Go

W Go `panic/recover` są przeznaczone do wyjątkowych, awaryjnych sytuacji, a nie
do normalnej obsługi błędów logiki biznesowej. Normalnym sposobem obsługi błędów
jest jawne zwrócenie `error` i kontrolowanie przepływu wykonywania.

#### Dlaczego `panic/recover` nie zostało zastąpione przez `error handling`:

1. **Narusza przejrzystość umowy:** w przypadku `error` sygnatura funkcji
   wyraźnie pokazuje, co może pójść nie tak; z `panic` błąd staje się ukryty.

2. **Utrudnij kontrolę przepływu:** panika rozwija stos, czyniąc zachowanie
   mniej przewidywalnym dla osoby wywołującej.

3. **Test gorszy:** testowanie scenariuszy paniki jest trudniejsze i mniej
   naturalne niż testowanie zwracanych błędów.

4. **Pogorszenie niezawodności usług:** nieprzechwycona panika w goroutine może
   zniszczyć proces lub ważną pętlę przetwarzania.

5. **`recover` ma charakter lokalny:** działa tylko w `defer` tej samej
   procedurze gor, więc nie jest to uniwersalny mechanizm błędów między
   komponentami.

#### Kiedy `panic` jest uzasadnione:

1. Naruszenie niezmienników wewnętrznych, co oznacza błąd oprogramowania.

2. Stany umownie niemożliwe („to nigdy nie powinno się zdarzyć”).

3. Krytyczne błędy inicjalizacji w przypadku nieprawidłowej kontynuacji.

#### Kiedy potrzebny jest `error`:

1. Oczekiwane awarie systemów zewnętrznych (sieć, DB, I/O).

2. Błędy sprawdzania poprawności i domeny.

3. Wszelkie sytuacje, w których osoba dzwoniąca ma wybór, jak zareagować.

#### Wniosek:

W dojrzałym kodzie Go `error` jest głównym narzędziem do zarządzanej obsługi
błędów. `panic/recover` to mechanizm awaryjny na wyjątkowe przypadki, a nie
codzienna alternatywa dla standardowej obsługi błędów.

</details>


<details>
<summary>76. Jak `errors.Is` i `errors.As` działają z zawijaniem błędów w Go i jaka jest między nimi różnica?</summary>

#### Go

We współczesnym Go błędy są często „opakowane” poprzez dodanie kontekstu za
pomocą `fmt.Errorf("...: %w", err)`. `errors.Is` i `errors.As` pozwalają
poprawnie pracować z takim łańcuchem błędów bez utraty pierwotnej przyczyny.

#### Jak działa `errors.Is`:

1. Sprawdza, czy łańcuch błędów zawiera określony błąd docelowy.

2. Używane głównie w przypadku błędów wartowniczych (`io.EOF`,
   `context.Canceled` itp.).

3. Semantyka: **„czy to (lub wersja opakowana) jest dokładnym błędem?”**

#### Jak działa `errors.As`:

1. Przeszukuje łańcuch pod kątem błędu określonego typu.

2. Jeśli zostanie znaleziony, zapisuje go do przekazanego celu (wskaźnika).

3. Semantyka: **„czy można usunąć błąd tego typu z ciągu znaków?”**

#### Kluczowa różnica:

1. `errors.Is` — błąd sprawdzania **tożsamości/równoważności**.

2. `errors.As` — **sprawdzanie typu** i dostęp do pól/metod specyficznych dla
   typu.

#### Praktyczny schemat użycia:

1. Pierwszy `errors.Is` dla znanych przypadków wartowniczych.

2. Następnie `errors.As`, jeśli wymagane są szczegóły typu niestandardowego
   (kod, metadane, kontekst).

3. Nie porównuj opakowanych błędów poprzez `==`, ponieważ w ten sposób traci się
   poprawność w łańcuchu zawijania.

#### Wniosek:

`errors.Is` odpowiada na pytanie „czy to ten sam błąd?”, a `errors.As` odpowiada
„czy jest to ten sam typ błędu?”. Razem tworzą poprawny i niezawodny model pracy
z zawijaniem błędów w Go.

#### Przykład:

```go
if err := repo.Save(ctx, x); err != nil {
	return fmt.Errorf("save user: %w", err)
}

if errors.Is(err, sql.ErrNoRows) {
	// перевірка sentinel-помилки
}

var ve *ValidationError
if errors.As(err, &ve) {
	// доступ до полів конкретного типу помилки
}
```

</details>


<details>
<summary>77. Kiedy należy używać niestandardowego typu błędu zamiast błędu wartowniczego i jakie są praktyczne konsekwencje tego wyboru dla architektury?</summary>

#### Go

`Sentinel error` i `custom error type` to różne narzędzia do modelowania błędów.
Sentinel nadaje się do prostego sygnału binarnego i typu niestandardowego - gdy
błąd niesie ze sobą kontekst strukturalny i wpływa na zachowanie kilku warstw
systemu.

#### Kiedy wystarczy błąd wartownika:

1. Wymagany jest jedynie fakt konkretnej kategorii błędu.

2. Nie ma potrzeby wypełniania dodatkowych pól.

3. Wystarczy sprawdzenie przez `errors.Is`.

#### Kiedy występuje niestandardowy typ błędu:

1. Wymaga **szczegółów strukturalnych**:

- kod błędu;

- przyczyna domeny;

- identyfikator zasobu;

- możliwość ponawiania;

- Mapowanie HTTP/gRPC.

2. Różne warstwy muszą podejmować różne decyzje na podstawie tych pól.

3. Wymagaj stabilnej ewolucji kontraktu błędów bez chaotycznego sprawdzania
   ciągów.

#### Konsekwencje architektoniczne wyboru:

1. **Błąd Sentinela**

- łatwiejszy start;

- bez kodu;

- ale słabsza ekspresja i ryzyko „rozwoju” ukrytych reguł przetwarzania.

2. **Niestandardowy typ błędu**

- jasniejsza umowa dotycząca domeny;

- lepsza integracja pomiędzy warstwami transportu/usług/domen;

- wyższe testowanie zasad przetwarzania;

- ale wymaga dyscypliny projektowej i podejścia do wersji.

#### Zalecana praktyka:

1. W przypadku prostych sygnałów globalnych — wartownik.

2. W przypadku błędów istotnych dla domeny — typ niestandardowy + `errors.As`.

3. Zawijaj mniejsze błędy przez `%w` bez utraty związku przyczynowego.

#### Wniosek:

Wybór pomiędzy typem wartowniczym a typem niestandardowym jest wyborem poziomu
wyrazistości architektury błędów. Gdy błąd wpływa na routing decyzji w systemie,
niestandardowy typ błędu zapewnia znacznie solidniejszy i skalowalny kontrakt.

</details>


<details>
<summary>78. Jak `defer` zachowuje się w pętli i jakie mogą być konsekwencje dla pamięci i wydajności?</summary>

#### Go

`defer` w Go nie jest wykonywany na końcu iteracji pętli, ale w momencie wyjścia
z otaczającej ją funkcji. Dlatego `defer` wewnątrz pętli kumuluje się i jest
wyzwalany dopiero po zakończeniu całej funkcji.

#### Jak to działa:

1. Każda iteracja dodaje nowe odroczone wywołanie do stosu odroczeń.

2. Te wywołania nie są wykonywane aż do zakończenia funkcji.

3. Przy wyjściu są uruchamiane w odwrotnej kolejności (LIFO).

#### Potencjalne konsekwencje:

1. **Opóźnione zwolnienie zasobów:** pliki, gniazda, transakcje, blokady mogą
   pozostać otwarte dłużej niż to konieczne.

2. **Większe zużycie pamięci:** wiele opóźnień wpisów w długiej pętli zwiększa
   obciążenie.

3. **Spadek wydajności:** w gorących pętlach nadmierne opóźnienia zwiększają
   czas wykonania.

4. **Ryzyko wyczerpania się zasobów:** np. „zbyt wiele otwartych plików”, jeśli
   `defer file.Close()` znajduje się w długim cyklu odczytu.

#### Kiedy jest bezpiecznie:

1. Mała liczba iteracji.

2. Krótki cykl życia funkcji.

3. Zasoby nie są rzadkie.

#### Najlepsza praktyka dotycząca pętli:

1. Umieść treść iteracji w osobnej funkcji i umieść tam `defer`.

2. Lub zamknij/zwolnij zasób jawnie na końcu każdej iteracji.

3. W przypadku zamków szczególnie ważne jest kontrolowanie czasu przetrzymywania
   sekcji krytycznej.

#### Wniosek:

`defer` w pętli to narzędzie wymagające dyscypliny: upraszcza kod, ale może
potajemnie gromadzić zasoby i obciążenie. Jeśli istnieje wiele iteracji, lepiej
upewnić się, że zasoby zostaną zwolnione w każdym kroku.

</details>


<details>
<summary>79. Jak działa funkcja `init` i czy możesz polegać na kolejności jej wykonywania?</summary>

#### Go

`init` w Go to specjalna funkcja pakietu, która jest wykonywana automatycznie
podczas inicjalizacji programu (przed `main`). Służy do wstępnej konfiguracji,
która powinna nastąpić raz przed uruchomieniem głównej logiki.

#### Jak działa inicjalizacja:

1. Importowane zależności są inicjowane jako pierwsze.

2. Następnie inicjowane są zmienne pakietu.

3. Następnie wywoływane są funkcje `init` pakietu.

4. Dopiero po zakończeniu całego drzewa inicjalizacji uruchamiany jest `main`.

#### Czy możesz polegać na zamówieniu:

1. **Między pakietami**: tak, w ramach zależności, zdefiniowana jest kolejność -
   najpierw zależności, potem pakiet konsumencki.

2. **W jednej paczce**:

- kolejność inicjalizacji zmiennych jest określona przez zależności pomiędzy
  nimi;

- w przypadku wielu `init` różnych plików w tym samym pakiecie poleganie na
  „losowej” kolejności plików tekstowych jest złym pomysłem projektowym.

3. Wniosek: istnieją podstawowe gwarancje, ale z punktu widzenia architektury
   lepiej nie budować krytycznej logiki biznesowej na złożonych, ukrytych
   łańcuchach `init`.

#### Ryzyko nadużywania `init`:

1. Ukryte skutki uboczne.

2. Cięższe debugowanie i testowanie.

3. Bardziej złożona kontrola kolejności w dużych bazach kodu.

#### Zalecenie praktyczne:

1. Utrzymuj `init` minimalizm i przewidywalność.

2. Użyj jawnych konstruktorów/funkcji `Setup` do ważnych inicjalizacji.

3. Zależności i kolejność uruchamiania należy ustalić jawnie w warstwie
   kompozycji.

#### Wniosek:

`init` w Go odbywa się automatycznie i posiada formalne gwarancje zamówienia na
poziomie wykresu importu. Jednakże w przypadku czytelnej i testowalnej
architektury lepiej jest wyraźnie określić inicjalizacje krytyczne, niż polegać
na ukrytych efektach `init`.

</details>


<details>
<summary>80. Dlaczego należy unikać zmiennych globalnych i funkcji `init` w bibliotekach?</summary>

#### Go

W kodzie biblioteki zmienne globalne i „ciężkie” funkcje `init` często powodują
niejawne zachowanie, które utrudnia integrację, testowanie i przewidywanie
aplikacji. Jest to szczególnie istotne w przypadku opakowań wielokrotnego
użytku.

#### Dlaczego zmienne globalne są złe w bibliotekach:

1. **Ukryty współdzielony stan zmienny:** Konsument biblioteki może nie
   wiedzieć, że istnieje stan globalny, który wpływa na zachowanie.

2. **Kwestie związane z konkurencyjnością:** globalne firmy łatwo stają się
   źródłem ras/konfliktów.

3. **Testowanie złożone:** testy zaczynają zależeć od kolejności wykonywania i
   skutków ubocznych poprzednich przypadków.

4. **Słaba możliwość komponowania:** trudno jest mieć wiele niezależnych
   instancji bibliotek z różnymi ustawieniami.

#### Dlaczego „ciężki” `init` jest niepożądany:

1. **Niejawne skutki uboczne importu:** wystarczy `import` i kod jest już
   wykonany.

2. **Brak wyraźnej kontroli czasu inicjalizacji:** Trudno jest kontrolować
   kolejność/warunki uruchamiania w dużej aplikacji.

3. **Pogorszona obserwowalność/możliwość debugowania:** błędy uruchamiania i
   skutki uboczne są trudniejsze do zlokalizowania.

#### Co jest zamiast tego lepsze:

1. Jawne konstruktory (`New(...)`) i struktury konfiguracyjne.

2. Projekt zorientowany na instancje bez globalnego stanu, który można
   modyfikować.

3. Jawny `Setup/Start/Close` cykl życia, jeśli jest to konieczne.

4. Minimum `init` tylko dla działań bez skutków ubocznych.

#### Wniosek:

Biblioteka powinna być przewidywalna i dostosowana do potrzeb użytkownika.
Unikanie stanu globalnego i nadmiernego `init` to inwestycja w testowalność,
skalowalność i czystość architektury kodu Go.

</details>


<details>
<summary>81. Co się stanie, jeśli serializujesz do JSON strukturę z polami zaczynającymi się od małej litery?</summary>

#### Go

W Go nie można eksportować pól strukturalnych rozpoczynających się od małej
litery (`unexported`). Pakiet `encoding/json` nie ma do nich refleksyjnego
dostępu jako pól publicznych, więc są one ignorowane podczas serializacji.

#### Co się stanie z `json.Marshal`:

1. Tylko wyeksportowane pola (pisane wielkimi literami) zostaną uwzględnione w
   formacie JSON.

2. Pola zawierające małe litery będą ignorowane.

3. Tagi `json:"..."` w nieeksportowanych polach nie „wymuszają” ich
   serializacji.

#### Konsekwencje w praktyce:

1. Niespodziewanie „pusty” lub niekompletny kod JSON.

2. Utrata ważnych danych w odpowiedziach API.

3. Trudne debugowanie błędów, jeśli programista nie wziął pod uwagę reguły
   eksportu.

#### A co z deserializacją (`json.Unmarshal`):

1. Podobnie `encoding/json` nie zapisze danych bezpośrednio w nieeksportowanych
   polach.

2. Kontrola procesu wymaga niestandardowych `MarshalJSON` / `UnmarshalJSON` ,
   oddzielnych DTO lub innych jawnych mechanizmów transformacji.

#### Ogólna zasada:

1. W przypadku pól w formacie JSON użyj wyeksportowanych nazw.

2. Trzymaj celowo nieeksportowanych danych wewnętrznych wrażliwych na domenę.

3. Oddzielne modele wewnętrzne i DTO ds. transportu, gdy wymagana jest
   szczegółowa kontrola zamówień publicznych.

#### Wniosek:

W Go serializacja JSON działa tylko z wyeksportowanymi polami struktury. Pola
zawierające małe litery w standardzie `encoding/json` nie są serializowane,
nawet jeśli są oznaczone.

</details>


<details>
<summary>82. Jakie są sposoby na uzyskanie danych z JSON w Go?</summary>

#### Go

Nie ma jednego „właściwego” sposobu pracy z JSON w Go: podejście jest wybierane
na podstawie stabilności schematu, wymagań wydajnościowych i poziomu
bezpieczeństwa typu.

#### Główne metody:

1. **Dekodowanie do struktury (`struct`)**

- najbardziej typowa i najbardziej niezawodna opcja dla znanego schematu;

- zapewnia bezpieczeństwo typu, przejrzyste kontrakty i lepszą łatwość
  konserwacji.

2. **Dekodowanie w `map[string]any`**

- jest wygodny w przypadku częściowo dynamicznych ładunków;

- elastyczny, ale mniej bezpieczny: wymaga asercji i kontroli typów.

3. **Czytanie strumieniowe przez `json.Decoder`**

- nadaje się do dużych plików JSON lub strumieni (treść HTTP, pliki);

- umożliwia pracę bez ładowania całego dokumentu do pamięci.

4. **`json.RawMessage` dla odroczonego/częściowego analizowania**

- przydatne, gdy część schematu zależy od pola „dyskryminator”;

- daje kontrolę nad etapami dekodowania.

5. **Niestandardowe `UnmarshalJSON` / `MarshalJSON`**

- w przypadku niestandardowych formatów, walidacji lub specjalnej semantyki
  biznesowej.

6. **Trzecie biblioteki / generator kodów**

- jest odpowiedni w przypadku wymagań dotyczących wysokiej wydajności lub
  szczególnych wymagań dotyczących kompatybilności.

#### Praktyczny wybór:

1. Stabilny kontrakt API → `struct`.

2. Dynamiczny lub częściowo nieznany JSON → `map` + `RawMessage`.

3. Duże ilości danych → `Decoder` (streaming).

4. Wydajność krytyczna/patologiczny JSON → profilowanie + generator
   kodów/alternatywy.

#### Wniosek:

Optymalny sposób „pobrania” danych JSON w Go zależy od charakteru schematu. W
większości przypadków produkcyjnych podstawowym wyborem są struktury typowane, a
mechanizmy dynamiczne (`map`, `RawMessage`, niestandardowe unmarshal) — w
przypadku bardziej złożonych scenariuszy.

</details>


<details>
<summary>83. Jaka jest różnica między `json.Marshal` i `json.Encoder`?</summary>

#### Go

`json.Marshal` i `json.Encoder` wykonują podobne zadanie serializacji, ale mają
inną pamięć i model we/wy. Wybór zależy od tego, czy chcesz gotowy `[]byte`, czy
przesyłany bezpośrednio do `io.Writer`.

#### `json.Marshal`:

1. Zwraca serializowany JSON jako `[]byte`.

2. Wygodny, gdy potrzebujesz:

- pobierz tablicę bajtów do dalszego przetwarzania;

- log/podpisz/kompresuj ładunek przed wysłaniem;

- pracuj z JSON w pamięci.

3. Minus: w przypadku dużych obiektów może wymagać więcej pamięci, ponieważ
   wynik jest najpierw całkowicie tworzony w buforze.

#### `json.Encoder`:

1. Zapisuje natychmiast JSON do `io.Writer` (`http.ResponseWriter`, plik,
   gniazdo).

2. Nadaje się do przesyłania strumieniowego skryptów i dużych odpowiedzi.

3. Często wygodniejsze w procedurach obsługi HTTP, ponieważ zmniejsza bufory
   pośrednie.

4. `Encode` dodaje na końcu znak nowej linii (warto o tym pamiętać).

#### Praktyczna zasada wyboru:

1. Wymagaj JSON jako wartości w kodzie → `json.Marshal`.

2. Należy natychmiast zapisać do strumienia/odpowiedzi →
   `json.NewEncoder(w).Encode(...)`.

#### Wniosek:

`Marshal` — „uformuj JSON w pamięci”, `Encoder` — „zapisz JSON do strumienia”.
Funkcjonalnie są zbliżone, ale z punktu widzenia zasobów i architektury I/O
różnica jest zasadnicza.

#### Przykład:

```go
// Marshal: отримуємо JSON у []byte
payload, err := json.Marshal(resp)
if err != nil { return err }
_ = payload

// Encoder: пишемо JSON одразу у HTTP-відповідь
w.Header().Set("Content-Type", "application/json")
if err := json.NewEncoder(w).Encode(resp); err != nil {
	return err
}
```

</details>


<details>
<summary>84. Co to jest `json.RawMessage` i kiedy jest przydatny?</summary>

#### Go

`json.RawMessage` to typ (w zasadzie `[]byte`) z pakietu `encoding/json`, który
umożliwia zapisanie fragmentu JSON „tak jak jest” bez natychmiastowego
analizowania go w określonej strukturze.

#### Co robi:

1. **Odroczone analizowanie:** najpierw można przeanalizować tylko „opakowanie”
   wiadomości, a pole złożone później, gdy znany jest wymagany typ.

2. **Częściowe dekodowanie:** analizujemy tylko te części ładunku, które są
   naprawdę potrzebne na tym etapie.

3. **Przezroczysta retransmisja:** Fragment JSON można retransmitować bez utraty
   oryginalnej reprezentacji.

#### Kiedy jest to szczególnie przydatne:

1. **Ładunki polimorficzne:** gdy typ pola zależy od dyskryminatora
   `type/kind/version`.

2. **Systemy sterowane zdarzeniami:** opakowanie zdarzenia jest stabilne, a
   treść zdarzenia ma różne schematy.

3. **Bramy integracji:** muszą odczytać metadane routingu i przekazać „treść”
   prawie bez zmian.

4. **Optymalizacja wydajności:** unikanie niepotrzebnego pełnego unmarshal dla
   dużych lub częściowo niepotrzebnych obiektów.

#### Co wziąć pod uwagę:

1. `RawMessage` nie sprawdza automatycznie semantyki — weryfikacja pozostaje w
   gestii Twojej logiki, gdy następuje `Unmarshal`.

2. Odroczona analiza komplikuje kod, jeśli jest niepotrzebnie stosowana.

#### Wniosek:

`json.RawMessage` to narzędzie do zarządzanego „późnego wiązania” danych JSON.
Jest to szczególnie cenne w protokołach polimorficznych i wieloformatowych,
gdzie rodzaj wewnętrznego ładunku jest określany dopiero w czasie wykonywania.

</details>


<details>
<summary>85. Jak zaimplementować niestandardowy organizator dla JSON? </summary>

#### Go

Niestandardowy organizator w Go jest implementowany za pomocą metody
`MarshalJSON() ([]byte, error)` w Twoim typie. Pozwala to na pełną kontrolę nad
sposobem serializacji obiektu do formatu JSON: format pola, sprawdzanie
poprawności, obliczone wartości, maskowanie itp.

#### Podejście podstawowe:

1. Dodaj metodę: `func (t MyType) MarshalJSON() ([]byte, error)`.

2. Wewnętrznie utwórz reprezentację pośrednią (często alias/strukturę DTO).

3. Zadzwoń pod numer `json.Marshal`, aby uzyskać ten widok.

4. Zwrotne bajty lub błąd.

#### Dlaczego oni to robią:

1. **Niestandardowy format wyjściowy:** np. konwersja czasu, pola wyliczeniowe,
   dziesiętne, maski.

2. **Zgodność z umową zewnętrzną:** gdy interfejs API wymaga określonego
   schematu lub konwencji nazewnictwa.

3. **Zarządzane ukrywanie danych:** nie generuj poufnych pól ani nie generuj
   zredagowanej wersji.

4. **Pola obliczone/pochodne:** zawierają wartości w formacie JSON, które nie
   występują jako „surowe” pola struktury.

#### Typowa technika bez rekurencji:

Aby uniknąć nieskończonego wywołania `MarshalJSON`, użyj typu aliasu (`type
alias MyType`) i zorganizuj alias lub oddzielne DTO.

#### Ważne wskazówki:

1. Zachowuj deterministyczną i prostą logikę zestawiania.

2. Napisz testy dotyczące przypadków brzegowych i zgodności wstecznej kontraktu
   JSON.

3. Jeśli wymagana jest symetria, zaimplementuj także `UnmarshalJSON`.

#### Wniosek:

Niestandardowy `MarshalJSON` to narzędzie do dostosowywania ekspozycji
publicznej. W produkcji stosuje się go, gdy standardowe tagi nie są
wystarczające dla semantyki kontraktu, bezpieczeństwa lub domeny.

</details>


<details>
<summary>86. Jak analizować wielotypowy kod JSON, jeśli dane wejściowe lub dowolne z pól może być tablicą `[...]` lub obiektem `{...}`?</summary>

#### Go

Gdy pole JSON ma postać „zmiennoprzecinkową” (czasami tablicę, czasem obiekt),
najbardziej niezawodnym podejściem w Go jest dekodowanie odroczone za pomocą
`json.RawMessage` lub niestandardowego `UnmarshalJSON` z rzeczywistym
rozpoznawaniem typu.

#### Strategia kanoniczna:

1. Odkoduj problematyczne pole w `json.RawMessage`.

2. Spójrz na pierwszy znaczący bajt:

- `[` → to jest tablica;

- `{` → to jest obiekt.

3. W zależności od formularza zatwierdź `json.Unmarshal` do odpowiedniego typu
   celu.

4. Normalizuj wynik do pojedynczego modelu wewnętrznego (tak, aby kod nie
   zależał od zewnętrznego schematu „płynu”).

#### Alternatywa: Niestandardowa `UnmarshalJSON`:

1. Zaimplementuj metodę na własnym typie.

2. Wewnątrz metody spróbuj parsować w `[]T`, a jeśli nie pasuje - w `T` (lub
   odwrotnie).

3. Zapisz w ujednoliconej reprezentacji, np. zawsze jako `[]T`.

#### Dlaczego to jest ważne:

1. Zewnętrzne interfejsy API są często niespójne między wersjami/punktami
   końcowymi.

2. Bezpośrednie `Unmarshal` do twardej struktury powoduje błędy takie jak
   `cannot unmarshal object into Go value of type []...`.

3. Normalizacja danych wejściowych radykalnie upraszcza resztę logiki
   biznesowej.

#### Praktyczne wskazówki:

1. Jasno udokumentuj akceptowalne formy wejściowe JSON.

2. Rejestruj nietypowe ładunki, aby diagnozować błędy kontraktów.

3. Pokryj testami oba formularze (`{}` i `[]`) + przypadki brzegowe (null, puste
   wartości, nieprawidłowy typ).

#### Wniosek:

W przypadku wielotypowego formatu JSON wzorzec „RawMessage → wykrywanie kształtu
→ cel Unmarshal → normalizacja” działa najlepiej w Go. Zapewnia to stabilne
przetwarzanie nawet przy niestabilnej umowie zewnętrznej.

</details>


<details>
<summary>87. Jak przetestować serializację (XML/JSON) w Go, gdy kolejność kluczy na mapie nie jest deterministyczna?</summary>

#### Go

Jeśli kolejność kluczy w `map` jest niedeterministyczna, testów nie można
zbudować na dosłownym porównaniu „surowych” ciągów serializacyjnych. Prawidłowym
podejściem jest porównywanie treści, a nie losowej kolejności prezentacji.

#### Solidne strategie dla JSON:

1. **Porównanie struktury w obie strony:**

- serializuj;

- deserializuj z powrotem do typu/modelu znormalizowanego;

- porównaj dane jako strukturę.

2. **Kanonizacja przed porównaniem:**

- przetwarzaj JSON w model pośredni;

- sortowanie kluczy/kolekcji;

- porównaj widok kanoniczny.

3. **Twierdzenia semantyczne zamiast równości ciągów:**

- sprawdź określone pola i niezmienniki.

#### Dla XML:

1. Podobna zasada: porównaj drzewo elementów/atrybutów, a nie surowy ciąg
   znaków.

2. Normalizuj spacje, formatowanie, kolejność atrybutów (jeśli pozwala na to
   umowa).

3. Sprawdź równoważność semantyczną analizowanych struktur.

#### Kiedy potrzebujesz złotego pliku:

1. Formularz **wyjście deterministyczne**:

- sortuj klucze przed serializacją;

- lub serializuj nie `map`, ale strukturę/uporządkowaną listę par.

2. Złoty test powinien zakończyć się niepowodzeniem tylko w przypadku zmian
   semantycznych umowy, a nie losowej kolejności kluczy.

#### Wniosek praktyczny:

Testy serializacji dla `map` nie porównują „tekstu jeden do jednego”, ale
równoważność danych. Determinizm należy albo wprowadzić jawnie (sortowanie),
albo zastosować kontrole na poziomie semantycznym.

</details>


<details>
<summary>88. Jakie są zalety i wady Protobuf w porównaniu do JSON? Czym różni się serializacja w Protobuf?</summary>

#### Go

Protobuf i JSON to dwie różne klasy formatów: JSON koncentruje się na
czytelności i wszechstronności dla człowieka, podczas gdy Protobuf koncentruje
się na zwartości, szybkości i kontraktowalności interakcji z maszyną.

#### Zalety Protobuf nad JSON:

1. **Bardziej kompaktowy rozmiar ładunku:** kodowanie binarne jest zwykle
   znacznie mniejsze niż tekstowy JSON.

2. **Wyższa wydajność serializacji/deserializacji:** mniejsze obciążenie
   związane z analizą i lepsza przepustowość w ruchu między usługami.

3. **Ścisły kontrakt oparty na pierwszym schemacie (`.proto`):** Jasny typowy
   model, generator kodu i kontrola ewolucji pola.

4. ** Lepsza kompatybilność wsteczna/przodowa dzięki regule pól i tagów.**

#### Wady Protobufa:

1. **Mniej czytelny dla oczu:** format binarny nie jest wygodny do ręcznego
   debugowania bez narzędzi.

2. **Dodatkowa infrastruktura:** `.proto`, generowanie kodu, wersjonowanie
   schematu.

3. **Próg wejścia jest wyższy niż JSON.**

#### Zalety JSON:

1. Łatwa integracja i szybki start.

2. Czytelność dla człowieka i wygoda analizy ręcznej.

3. Szeroka kompatybilność w ekosystemie internetowym.

#### Czym różni się serializacja w Protobuf:

1. Dane są kodowane nie za pomocą nazw pól, ale za pomocą znaczników
   numerycznych (`field numbers`).

2. Format jest binarny i ma różne typy na poziomie łącza.

3. Struktury są generowane na podstawie `.proto` (generowanie kodu), a nie są
   odzwierciedlane jak w typowym strumieniu JSON.

4. Ewolucja umowy wymaga dyscypliny:

- nie używaj ponownie starych tagów;

- ostrożnie zmień typy/opcjonalne/powtarzające się pola.

#### Wniosek:

JSON jest lepszy w przypadku otwartych, zorientowanych na człowieka interfejsów
API i szybkiej integracji. Protobuf jest przeznaczony dla wysokowydajnych
systemów międzyusługowych z przejrzystym schematem kontraktu, w których rozmiar
ładunku, opóźnienie i stabilność ewolucji mają kluczowe znaczenie.

</details>


<details>
<summary>89. Dlaczego należy ponownie wykorzystać `http.Client` zamiast tworzyć nowy dla każdego żądania?</summary>

#### Go

W Go `http.Client` i jego transport (`http.Transport`) zarządzają łączeniem
połączeń TCP, utrzymywaniem aktywności, sesjami TLS i innymi optymalizacjami
sieci. Jeśli dla każdego żądania utworzysz nowego klienta, korzyści te zostaną
utracone.

#### Dlaczego ponowne użycie jest ważne:

1. **Bule połączeń:** ponowne wykorzystanie już otwartych połączeń zmniejsza
   opóźnienia.

2. **Mniejsze obciążenie związane z uzgadnianiem:** mniej konfiguracji protokołu
   TCP/TLS na żądanie.

3. **Lepsza przepustowość:** bardziej stabilna przepustowość w scenariuszach z
   dużym obciążeniem.

4. **Kontrola zasobów:** Masowe tworzenie nowych klientów/transportów może
   zwiększyć liczbę gniazd i wyczerpać zasoby systemu.

#### Co się dzieje z „klientem na żądanie”:

1. Gorsza utylizacja utrzymywania przy życiu.

2. Więcej krótkotrwałych połączeń.

3. Większe opóźnienia i dodatkowe obciążenie sieci/procesora.

#### Zalecana praktyka:

1. Mają długotrwałe `http.Client` (często po jednym na usługę lub klasę polisy).

2. Skonfiguruj limity czasu i parametry `Transport` jawnie pod obciążeniem.

3. Dla różnych umów SLA/tras — Oddzielnych klientów ponownego wykorzystania, ale
   nie „nowego klienta na połączenie”.

#### Wniosek:

`http.Client` należy ponownie wykorzystać w Go, ponieważ zapewnia wydajność
sieci, mniejsze opóźnienia i lepszą stabilność pod obciążeniem. Tworzenie nowego
klienta dla każdego żądania jest typową antypraktyką w systemach produkcyjnych.

</details>


<details>
<summary>90. Dlaczego musisz zamknąć `resp.Body` po żądaniu HTTP?</summary>

#### Go

`resp.Body` w Go to zasób przesyłania strumieniowego powiązany z połączeniem
sieciowym. Jeśli nie zostanie zamknięty, klient nie będzie mógł poprawnie
przywrócić połączenia do puli ani zwolnić zasobów systemowych, co prowadzi do
degradacji usługi.

#### Dlaczego jest to istotne:

1. **Wyciek zasobów:** w niezamkniętych korpusach znajdują się uchwyty i
   gniazda.

2. **Pogorszenie ponownego wykorzystania połączeń:** funkcja keep-alive działa
   gorzej, wzrasta liczba nowych połączeń.

3. **Rosnące opóźnienia i błędy pod obciążeniem:** możliwe wyczerpanie puli
   połączeń i limitów systemowych.

4. **Niestabilne zachowanie klienta:** „zawiesza się”, przekroczenia limitu
   czasu, nieoczekiwane awarie w połączeniach o dużej częstotliwości.

#### Prawidłowy wzór:

1. Po sprawdzeniu błędu z `Do` natychmiast wykonaj: `defer resp.Body.Close()`.

2. Jeśli potrzebujesz maksymalnego ponownego wykorzystania połączeń:

- przeczytaj treść do końca (lub poprawnie ogranicz czytanie),

- , a następnie zamknij.

#### Wniosek praktyczny:

Zamknięcie `resp.Body` nie jest formalnością, ale warunkiem poprawnego działania
klienta HTTP w Go. Ma to bezpośredni wpływ na wydajność, stabilność i
efektywność wykorzystania zasobów usługi.

#### Przykład:

```go
resp, err := client.Do(req)
if err != nil {
	return err
}
defer resp.Body.Close()

body, err := io.ReadAll(resp.Body)
if err != nil {
	return err
}
_ = body
```

</details>


<details>
<summary>91. Czym `http.DefaultServeMux` różni się od niestandardowego `ServeMux`?</summary>

#### Go

`http.DefaultServeMux` to „domyślny” router globalny. Niestandardowy `ServeMux`
to osobna, jawnie utworzona instancja routera, którą zarządzasz lokalnie w
ramach określonego serwera.

#### `http.DefaultServeMux`:

1. **Globalny stan pakietu `net/http`:** rejestracja przez `http.Handle` /
   `http.HandleFunc` pisze dokładnie tam.

2. **Szybki start:** dobry do prostych przykładów i małych narzędzi.

3. **Ryzyka w większych projektach:** ukryte rejestracje z różnych pakietów,
   bardziej złożona kontrola zależności i testów.

#### Niestandardowe `ServeMux`:

1. **Kompozycja jawna:** `mux := http.NewServeMux()` i przekazanie jej do
   `http.Server{Handler: mux}`.

2. **Izolacja tras:** każdy serwer/test/instancja może mieć własną tabelę
   obsługi.

3. ** Lepsza testowalność i łatwość konserwacji:** mniej globalnych skutków
   ubocznych, łatwiejsze przeprowadzanie niezależnych testów integracyjnych.

4. **Bezpieczniejsza architektura dla monolitów i mikrousług:** routing staje
   się częścią jawnego kodu startowego.

#### Praktyczny wybór:

1. W przypadku kodu produkcyjnego niestandardowy `ServeMux` jest prawie zawsze
   lepszy.

2. `DefaultServeMux` jest najczęściej odpowiedni w przypadku bardzo prostych
   scenariuszy lub samouczków.

#### Wniosek:

Różnica między nimi polega na poziomie przejrzystości i kontroli.
`DefaultServeMux` wygodne, ale globalne; niestandardowe `ServeMux` zapewnia
izolowane, kontrolowane i czystsze architektonicznie routing.

</details>


<details>
<summary>92. Jak poprawnie wdrożyć płynne zamykanie serwera HTTP i procesu roboczego w tle w Go?</summary>

#### Go

`Graceful shutdown` w Go to kontrolowane zakończenie usługi bez utraty żądań i
bez „osieroconych” procedur. Pomysł jest prosty: przestań otrzymywać nowy
ładunek, pozwól, aby aktywna praca dobiegła końca, poprawnie zatrzymaj tło i
zamknij zasoby w przewidywalnej kolejności.

#### Sekwencja kanoniczna:

1. Przechwytywanie sygnałów zakończenia (`SIGTERM`, `SIGINT`).

2. Utwórz `context` z limitem czasu dla fazy wyłączania.

3. Zadzwoń `server.Shutdown(ctx)`:

- nowe połączenia nie są już akceptowane;

- aktywne żądania mają czas na realizację.

4. Anuluj kontekst/sygnał pracownikom działającym w tle, aby zatrzymali się.

5. Poczekaj na zakończenie procesów roboczych (`WaitGroup`/`errgroup`).

6. Zamknij zasoby zewnętrzne (baza danych, kolejki, producenci, pliki).

#### Jak zatrzymać pracownika działającego w tle:

1. Proces roboczy działa w pętli z `select`, gdzie znajduje się gałąź `case
   <-ctx.Done(): return`.

2. Podczas zamykania główny proces wywołuje funkcję anulowania.

3. Pracownik kończy bieżący chroniony krok, spłukuje/oczyszcza i wychodzi.

#### Krytyczne praktyki:

1. **Wymagane są limity czasu:** gracja nie powinna zamieniać się w wieczne
   oczekiwanie.

2. **Wyłączenie idempotentne:** powtarzające się sygnały nie zakłócają logiki
   wyłączania.

3. **Obserwowalność:** etapy zatrzymania dziennika i wskaźniki czasu trwania.

4. **Jasny porządek:** najpierw zatrzymaj pobór, następnie opróżnij w locie, a
   następnie oczyść.

#### Typowe błędy:

1. Zatrzymaj proces „na stałe” bez `Shutdown`.

2. Nie przekazuj `ctx` pracownikom/połączeniom zewnętrznym.

3. Nie czekaj na zakończenie goroutines.

4. Zapomnij o opróżnianiu buforów/kolejek przed wyjściem.

#### Wniosek:

Prawidłowe, łagodne zamknięcie w Go jest organizowane za pomocą sygnału
`context`, `server.Shutdown` i jawnego oczekiwania na wszystkie zadania w tle.
Takie podejście gwarantuje integralność żądań, przewidywalność wyników i
niezawodność działania.

</details>


<details>
<summary>93. Dlaczego porównywać `time.Time` z `.Equal()`, a nie `==`?</summary>

#### Go

W Go `time.Time` należy porównywać z `t1.Equal(t2)`, ponieważ `==` sprawdza
strukturę wartości bit po bicie, w tym pomocnicze elementy wewnętrzne (w tym
lokalizację i, pod pewnymi warunkami, monotoniczną część czasu), a nie tylko
punkt w czasie na osi czasu.

#### Dlaczego `==` może dać fałszywy wynik:

1. Dwa `time.Time` mogą reprezentować tę samą instancję, ale mają różne
   reprezentacje lokalizacji.

2. Wewnętrzne dane serwisowe mogą się różnić, chociaż moment kalendarzowy jest
   taki sam.

3. Więc `t1 == t2` może być `false` nawet jeśli punkt czasowy jest równoważny.

#### Co robi `.Equal()`:

1. Porównuje dokładnie chwilę czasową (semantykę momentu), a nie wewnętrzną
   reprezentację konstrukcji.

2. To jest prawidłowe pytanie „czy to ten sam czas?” sprawdzenie logiki
   biznesowej.

#### Kiedy `==` jest nadal odpowiedni:

1. Aby sprawdzić wartość null: `t == (time.Time{})`.

2. W przypadkach, gdy naprawdę trzeba porównać pełną tożsamość strukturalną, a
   nie tylko chwilę.

#### Wniosek praktyczny:

W zastosowanej logice synchronizacji użyj `.Equal()`. Operator `==` dla
`time.Time` jest łatwo podatny na błędy, ponieważ podczas sprawdzania
równoważności momentów porównuje więcej niż zwykle jest to zamierzone.

</details>


<details>
<summary>94. Jak działają indeksy? Jak wybrać indeksy dla tabel?</summary>

#### Go

Indeks w systemie DBMS jest pomocniczą strukturą danych (najczęściej
przypominającą drzewo B), która przyspiesza wyszukiwanie wierszy według
określonych pól bez konieczności pełnego skanowania tabeli. W rzeczywistości
indeks przechowuje uporządkowaną reprezentację kluczy i odniesień do wierszy.

#### Jak działają indeksy:

1. Zapytanie z `WHERE/JOIN/ORDER BY` może używać indeksu, aby szybko znaleźć
   odpowiedni zakres kluczy.

2. Zamiast `Seq Scan` (odczyt całej tabeli) optymalizator wybiera `Index
   Scan/Bitmap Scan`, jeśli jest to korzystne.

3. Indeksy mogą również wspierać unikalność (`UNIQUE`).

#### Cena indeksowa:

1. Każdy indeks zajmuje miejsce na dysku.

2. `INSERT/UPDATE/DELETE` stają się droższe, ponieważ trzeba zaktualizować
   indeksy.

3. Nadmiarowe indeksy spowalniają zapis i utrudniają konserwację.

#### Jak prawidłowo wybrać indeksy:

1. **Odrzuć prawdziwe prośby**, a nie „na wszelki wypadek”.

2. Pola indeksu, które często znajdują się w:

- `WHERE`

- `JOIN ON`

- `ORDER BY`

- `GROUP BY` (w razie potrzeby)

3. W przypadku indeksów złożonych należy wziąć pod uwagę kolejność kolumn
   (reguła przedrostka skrajnego lewego):

- najbardziej selektywne/częste schorzenia występują na początku.

4. Obejrzyj `EXPLAIN (ANALYZE, BUFFERS)` i potwierdź, że indeks jest
   rzeczywiście używany i przynosi zyski.

5. Regularnie przeglądaj nieskuteczne/nieużywane indeksy.

#### Podejście praktyczne:

1. Zdefiniuj najczęściej powolne żądania.

2. Dodaj minimalne wymagane indeksy.

3. Sprawdź plan przed/po.

4. Zmierz wpływ na równowagę odczytu/zapisu przy rzeczywistym obciążeniu.

#### Wniosek:

Indeks to narzędzie przyspieszające czytanie kosztem droższego pisania.
Prawidłowy dobór indeksów zawsze zależy od zapytań: tylko dla określonych
wzorców dostępu i dopiero po sprawdzeniu planu i wydajności.

#### Przykład:

```sql
-- Перевіряємо план до індексу
EXPLAIN (ANALYZE, BUFFERS)
SELECT *
FROM orders
WHERE tenant_id = 42
  AND created_at >= now() - interval '7 days'
ORDER BY created_at DESC
LIMIT 100;

-- Додаємо індекс під реальний патерн запиту
CREATE INDEX CONCURRENTLY idx_orders_tenant_created_at
  ON orders (tenant_id, created_at DESC);
```

</details>


<details>
<summary>95. Co to jest widok zmaterializowany i czym różni się od zwykłego widoku? </summary>

#### Go

`View` i `Materialized View` reprezentują zapisane zapytanie, ale różnią się
zasadniczo sposobem przechowywania wyniku i kosztem odczytu.

#### Normalny `View`:

1. To jest logiczna „tabela wirtualna” oparta na zapytaniu SQL.

2. Dane nie są fizycznie przechowywane oddzielnie.

3. Każde żądanie do widoku w rzeczywistości powoduje ponowne wykonanie bazowego
   kodu SQL.

#### `Materialized View`:

1. To jest fizycznie przechowywany wynik zapytania.

2. Odczyt jest zwykle znacznie szybszy, ponieważ nie trzeba za każdym razem
   ponownie obliczać złożonego łączenia/agregacji.

3. Dane mogą być nieaktualne do `REFRESH`.

#### Kluczowa różnica:

1. `View` = zawsze aktualne dane, ale wyższy koszt kalkulacji.

2. `Materialized View` = szybki odczyt, ale kompromis w zakresie świeżości
   danych.

#### Kiedy wybrać `Materialized View`:

1. Ciężkie zapytania analityczne i agregacje.

2. Często czytaj raporty z rzadszymi aktualizacjami.

3. Scenariusze, w których dopuszczalne jest kontrolowane opóźnienie istotności.

#### Kiedy wystarczy zwykłe `View`:

1. Wymagane są najbardziej aktualne dane w czasie rzeczywistym.

2. Żądanie nie jest zbyt drogie.

3. `View` jest używany jako abstrakcja dostępu logicznego, a nie jako pamięć
   podręczna.

#### Wniosek praktyczny:

`Materialized View` to zasadniczo zarządzana pamięć podręczna wyników SQL z
jawną aktualizacją; zwykły `View` to czysto logiczna projekcja bez
przechowywania danych. Wybór pomiędzy nimi to równowaga pomiędzy świeżością i
szybkością.

#### Przykład:

```sql
CREATE MATERIALIZED VIEW mv_daily_sales AS
SELECT date_trunc('day', created_at) AS day,
       sum(amount) AS total
FROM payments
GROUP BY 1;

-- Оновлення знімка даних
REFRESH MATERIALIZED VIEW CONCURRENTLY mv_daily_sales;
```

</details>


<details>
<summary>96. Co to jest KWAS? Skomentuj implementację ACID w PostgreSQL.</summary>

#### Go

`ACID` to cztery podstawowe właściwości systemów transakcyjnych gwarantujące
poprawność danych nawet w przypadku awarii, konkurencji i dużego obciążenia:
Atomowość, Spójność, Izolacja, Trwałość.

#### Odszyfrowanie ACID:

1. **Atomiczność:** transakcja jest albo w pełni wykonana, albo w ogóle nie
   została wykonana.

2. **Spójność:** po zatwierdzeniu dane pozostają ważne zgodnie z określonymi
   regułami i ograniczeniami.

3. **Izolacja:** transakcje równoległe nie powinny na siebie niewłaściwie
   wpływać.

4. **Trwałość:** Zatwierdzone zmiany pozostają nawet po awarii procesu/systemu.

#### Jak PostgreSQL implementuje ACID:

1. **Atomiczność:**

- dziennik transakcji zmian + mechanizmy wycofywania;

- w przypadku błędu wszystkie zmiany transakcji zostaną w całości wycofane.

2. **Konsystencja:**

- ograniczenia (`PRIMARY KEY`, `UNIQUE`, `CHECK`, `FOREIGN KEY`) i wyzwalacze;

- zatwierdzenie jest możliwe tylko wtedy, gdy nie naruszono niezmienników.

3. **Izolacja:**

- MVCC (Multi-Version Concurrency Control): czytelnicy widzą spójne wersje linii
  bez rażącego blokowania odczytów;

- obsługa poziomów izolacji (`Read Committed`, `Repeatable Read`,
  `Serializable`) z różną równowagą wydajności i rygorystyczności.

4. **Trwałość:**

- WAL (rejestrowanie z wyprzedzeniem): przed zatwierdzeniem zmiany są najpierw
  rejestrowane w dzienniku;

- po awarii odzyskiwanie odbywa się zgodnie z metodą WAL, która zachowuje
  zatwierdzony stan.

#### Wniosek praktyczny:

W PostgreSQL ACID nie jest zapewniany za pomocą „jednego przycisku”, ale poprzez
kombinację MVCC, WAL, menedżera transakcji, blokad i mechanizmów ograniczeń. To
właśnie sprawia, że ​​PostgreSQL jest niezawodnym systemem DBMS dla krytycznych
systemów transakcyjnych.

#### Przykład:

```sql
BEGIN;

UPDATE accounts
SET balance = balance - 100
WHERE id = 1;

UPDATE accounts
SET balance = balance + 100
WHERE id = 2;

COMMIT; -- або ROLLBACK при помилці
```

</details>


<details>
<summary>97. Jaka jest różnica między BAzą a Kwasem?</summary>

#### Go

`ACID` i `BASE` to dwie różne filozofie spójności i niezawodności w systemach
rozproszonych/transakcyjnych. Odzwierciedlają różne priorytety architektury:
rygorystyczność i natychmiastową spójność w porównaniu z dostępnością i
skalowalnością.

#### KWAS:

1. **Atomiczność, spójność, izolacja, trwałość**.

2. Koncentruje się na ścisłych gwarancjach transakcyjnych.

3. Korzyść — przewidywalna poprawność danych po każdym zatwierdzeniu.

4. Zwykle stosowane w finansach, księgowości, krytycznych spójnych
   scenariuszach.

#### PODSTAWA:

1. **Zasadniczo dostępne, stan miękki, ostateczna spójność**.

2. Nacisk na wysoką dostępność i skalowanie poziome.

3. Zezwala na tymczasową niespójność między węzłami.

4. Spójność osiąga się „z biegiem czasu”, niekoniecznie natychmiast.

#### Kluczowa różnica:

1. **ACID**: „lepiej poczekać, ale zachować ścisłe gwarancje”.

2. **BASE**: „najlepiej szybko reagować i być dostępnym, nawet jeśli spójność
   nie jest natychmiastowa”.

#### Praktyczne implikacje dla architektury:

1. ACID upraszcza rozumowanie dotyczące niezmienników, ale może kosztować więcej
   pod względem opóźnień/skalowania w środowisku rozproszonym.

2. BASE zapewnia stabilność i dostępność na dużą skalę, ale wymaga mechanizmów
   kompensacyjnych, idempotencji i przemyślanego projektu domeny.

#### Wniosek:

ACID i BASE nie są „dobre/złe”, ale różnymi kompromisami. Wybór zależy od tego,
co jest ważniejsze dla systemu: natychmiastowa rygorystyczność niezmienników czy
dostępność i skalowalność za cenę ostatecznej spójności.

</details>


<details>
<summary>98. Nazwij poziomy izolacji transakcji.</summary>

#### Go

Poziomy izolacji określają, jak „widoczne” są dla siebie zmiany transakcji
równoległych. Im wyższy poziom izolacji, tym mniej anomalii, ale zwykle wiąże
się to z wyższym kosztem wydajności i konkurencyjności.

#### Klasyczne poziomy izolacji (SQL):

1. **Przeczytaj niezatwierdzone**

- najniższy poziom;

- umożliwia odczyt nienaprawionych zmian (brudny odczyt).

2. **Odczyt zatwierdzony**

- odczytywane są tylko zatwierdzone dane;

- brudny odczyt jest zabroniony;

- możliwy jest odczyt jednorazowy i odczyt fantomowy.

3. **Odczyt powtarzalny**

- wielokrotne czytanie tych samych wierszy w ramach transakcji daje ten sam
  wynik;

- redukuje niektóre anomalie, ale w zależności od systemu DBMS mogą pozostać
  scenariusze fantomowe.

4. **Możliwość serializacji**

- najsurowszy poziom;

- gwarantuje wynik równoważny sekwencyjnej realizacji transakcji;

- maksymalna ochrona przed anomaliami, ale droższa od konkurencji.

#### Wniosek praktyczny:

Wybór poziomu izolacji to równowaga pomiędzy poprawnością a wydajnością. W
produkcji określa się to na podstawie niezmienników domeny: gdzie `Read
Committed` jest wystarczające i gdzie wymagane jest `Repeatable Read` lub
`Serializable`.

#### Przykład:

```sql
BEGIN;
SET TRANSACTION ISOLATION LEVEL REPEATABLE READ;

SELECT balance FROM accounts WHERE id = 1;
-- ... інші операції в межах тієї ж транзакції

COMMIT;
```

</details>


<details>
<summary>99. Do czego służą grafowe bazy danych?</summary>

#### Go

Grafowe bazy danych są potrzebne tam, gdzie główną wartością nie są pojedyncze
rekordy, ale powiązania między nimi i szybkie ominięcie wieloetapowych
zależności.

#### Co za grafowe modele baz danych:

1. **Węzły** są jednostkami.

2. **Krawędzie** — relacje między bytami.

3. **Właściwości** węzłów i krawędzi są atrybutami modelu domeny.

#### Do jakich zadań są szczególnie przydatne:

1. **Wykresy społecznościowe:** znajomi, subskrypcje, rekomendacje.

2. **Wykrywanie oszustw:** nietrywialne łańcuchy transakcji i podejrzane
   powiązania.

3. **Wykres wiedzy / wyszukiwanie semantyczne:** połączona reprezentacja wiedzy.

4. **Topologia sieci/IT:** zależności usług, trasy, wpływ incydentów.

5. **Modele ról/uprawnień:** złożone zasady dostępu z dziedziczeniem ról.

#### Dlaczego relacyjna baza danych nie zawsze wystarczy:

1. W scenariuszach łączenia wieloetapowego zapytania mogą stać się ciężkie i
   kłopotliwe.

2. Silnik wykresów jest zoptymalizowany specjalnie pod kątem żądań ścieżki
   przejścia.

3. Model „relacji jako podmiotu pierwszej klasy” sprawia, że ​​złożone przypadki
   relacji stają się bardziej naturalne.

#### Gdy baza danych wykresów jest opcjonalna:

1. Jeśli połączenia są proste i rzadko są szczegółowo sprawdzane.

2. Jeśli dominują klasyczne scenariusze CRUD/OLTP bez skomplikowanego
   przechodzenia.

3. Jeśli zespół i infrastruktura już efektywnie współpracują ze stosem
   relacyjnym.

#### Wniosek:

Grafowe bazy danych są potrzebne, gdy wartość biznesowa leży w strukturze
połączeń i wieloetapowej nawigacji po nich. Jest to wyspecjalizowane narzędzie
dla domen skoncentrowanych na relacjach, gdzie podejście zorientowane na
łączenie staje się nieskuteczne lub zbyt złożone.

</details>


<details>
<summary>100. Jeśli dane są ograniczone czasowo, z jakich baz danych powinienem korzystać?</summary>

#### Go

Jeżeli dane mają określony charakter czasowy (metryki, logi, zdarzenia,
telemetria) wskazane jest wybranie SZBD zgodnie z profilem obciążenia:
częstotliwością rejestracji, rodzajem żądań, okresem przechowywania, wymaganiami
dotyczącymi agregacji i opóźnieniami.

#### Typowe opcje:

1. **DB szeregów czasowych (TSDB)**

- przykłady: Prometheus (dla metryk), VictoriaMetrics, InfluxDB, TimescaleDB;

- mocne strony: duża szybkość przetwarzania, żądania okien czasowych, zasady
  zmniejszania próbkowania/przechowywania.

2. **PostgreSQL + podejście zorientowane na czas**

- kiedy potrzebujesz transakcyjności, ekosystemu SQL i złożonych zapytań
  łączących z danymi czasowymi;

- często łączy się z podziałem czasu.

3. **Kolumnowy magazyn OLAP**

- do analizy dużych ilości wydarzeń historycznych (ClickHouse itp.);

- strong w agregacjach i skanowaniu dużych zakresów czasu.

#### Kryteria wyboru:

1. **Telemetria z dużą ilością zapisów** → TSDB.

2. **Transakcje operacyjne + czas** → PostgreSQL (z partycjonowaniem/indeksami).

3. **Analiza historyczna na dużą skalę** → podejście kolumnowe/OLAP.

4. **Model przechowywania i kosztów**: gorące dane w szybkiej warstwie, zimne
   dane w tańszej pamięci masowej.

#### Wniosek praktyczny:

Nie ma „uniwersalnej” bazy danych dla danych ograniczonych czasowo: optymalna
jest kombinacja narzędzi dla konkretnego obciążenia. W większości systemów
działa strategia gorącej warstwy TSDB/OLTP + osobna warstwa analityczna dla
długiej historii.

</details>


<details>
<summary>101. Jak działa replikacja master-slave?</summary>

#### Go

Replikacja typu master-slave (replika podstawowa) to model, w którym jeden węzeł
akceptuje zapisy, a jeden lub więcej węzłów repliki replikuje te zmiany w celu
skalowania odczytu, nadmiarowości i zwiększonej odporności na błędy.

#### Podstawowa zasada:

1. **Master (główny)** obsługuje `INSERT/UPDATE/DELETE`.

2. Zmiany są rejestrowane w dzienniku transakcji (WAL/binlog w zależności od
   systemu DBMS).

3. **Slave (replika)** odczytuje logi i stosuje zmiany do swojej kopii danych.

4. Odczyty są często dystrybuowane do replik, zapisy pozostają na serwerze
   podstawowym.

#### Tryby replikacji:

1. **Asynchroniczny**

- primary nie czeka na potwierdzenie z repliki przed zatwierdzeniem;

- mniejsze opóźnienie nagrywania;

- możliwe opóźnienie replikacji i niespójność czasowa.

2. **Synchroniczny/quasi-synchroniczny**

- primary częściowo lub całkowicie czeka na potwierdzenie replik;

- wyższa spójność;

- potencjalnie większe opóźnienie zapisu.

#### Co robi:

1. Skalowanie obciążenia odczytu.

2. Kopia zapasowa danych na potrzeby przełączania awaryjnego.

3. Oddzielenie rekordów OLTP i scenariuszy intensywnego odczytu.

#### Typowe ryzyko:

1. **Opóźnienie replikacji** (czytnik może zobaczyć „stare” dane).

2. Złożoność przełączania awaryjnego/powrotu po awarii i ról węzłów.

3. Ryzyko rozszczepienia mózgu w przypadku nieprawidłowo zorganizowanych
   scenariuszy przełączania.

#### Wniosek praktyczny:

Replikacja master-slave to równowaga między dostępnością, skalowalnością i
spójnością. Jest skuteczny w przypadku skalowania odczytu, ale wymaga dyscypliny
w zakresie monitorowania opóźnień, przemyślanego przełączania awaryjnego i
jasnej polityki routingu żądań.

</details>


<details>
<summary>102. Co to jest sharding i jakie są jego rodzaje?</summary>

#### Go

Sharding to poziomy podział danych na kilka niezależnych węzłów (shardów) w celu
skalowania systemu poza pojedynczy serwer pod względem ilości danych, obciążenia
i przepustowości.

#### Dlaczego stosuje się sharding:

1. Nieograniczaj pojedynczego węzła (CPU/RAM/dysk/we/wy).

2. Zwiększ przepustowość zapisu/odczytu dzięki równoległemu działaniu
   fragmentów.

3. Lokalizuj gorące zestawy danych i ograniczaj konkurencję o zasoby.

#### Główne typy shardingu:

1. **Sharding na podstawie zakresu**

- dane są podzielone według zakresów kluczy (na przykład według daty lub
  przedziału identyfikatora);

- proste dla scenariuszy szeregów czasowych;

- ryzyko „gorących” zakresów.

2. **Sharding oparty na skrótach**

- shard jest określany na podstawie skrótu klucza;

- rozkłada obciążenie bardziej równomiernie;

- trudniejsze jest wykonywanie zapytań o zakres.

3. ** Fragmentowanie oparte na katalogach/wyszukiwaniu**

- oddzielny klucz map tabel/usług → fragment;

- elastyczny routing i migracje;

- dodatkowa złożoność i zależność od warstwy wyszukiwania.

4. **Sharding w oparciu o lokalizację geograficzną/dzierżawę**

- dane są udostępniane według regionu lub klienta (najemcy);

- dobry do izolacji, zgodności i architektur z wieloma dzierżawcami;

- możliwa nierównowaga między fragmentami.

#### Architektoniczne wyzwania związane z shardingiem:

1. Przywracanie równowagi danych w okresie wzrostu.

2. Żądania, połączenia i transakcje typu Cross-shard.

3. Komplikacje związane z tworzeniem kopii zapasowych/przywracaniem i
   przełączaniem awaryjnym.

4. Większa złożoność obserwowalności i wsparcia operacyjnego.

#### Wniosek:

Sharding to narzędzie skalujące, które zapewnia znaczny wzrost wydajności, ale
kosztem złożoności architektury. Wybór typu shardingu powinien opierać się na
schemacie dostępu do danych, modelu domeny i planie ewolucji systemu.

#### Przykład:

```go
func shardForUser(userID int64, shards int) int {
	if shards <= 0 {
		return 0
	}
	return int(userID % int64(shards)) // hash/range-логіку змінюють під домен
}
```

</details>


<details>
<summary>103. Podziel się z nami swoimi doświadczeniami z optymalizacją baz danych. Jakich narzędzi użyłeś?</summary>

#### Go

W przypadku rozmowy kwalifikacyjnej to pytanie zwykle wymaga **ustrukturyzowanej
historii przypadku**: kontekst → problem → działania → narzędzia → wskaźniki
przed/po. Poniżej znajduje się przykładowa silna odpowiedź, którą możesz
dostosować do własnych doświadczeń w świecie rzeczywistym.

#### Przykład:

1. **Kontekst**

- w usłudze o dużym obciążeniu odczytem/zapisem zaobserwowano pogorszenie
  opóźnienia p95/p99 w godzinach szczytu.

2. **Objawy**

- powolne żądania;

- Wzrost procesora w węźle DB;

- zwiększanie kolejek oczekiwania na blokady i żądań.

3. **Co zrobiłeś**

- zebrał najczęściej powolne żądania;

- przeanalizowałem plany wykonania;

- dodano/przebudowano indeksy na rzeczywiste `WHERE/JOIN/ORDER BY`;

- usunięto N+1 i przeniesiono niektóre ciężkie operacje do partii;

- dodano buforowanie dla przypadków gorącego odczytu;

- zoptymalizowaliśmy schemat (rodzaje pól, podział czasowy, archiwizacja starych
  danych).

4. **Narzędzia**

- `EXPLAIN (ANALYZE, BUFFERS)` / `EXPLAIN ANALYZE`;

- żądanie statystyk (`pg_stat_statements` lub podobny);

- profilowanie aplikacji (`pprof`) w celu oddzielenia wąskiego gardła bazy
  danych od warstwy aplikacji;

- metryki i dashboardy (Prometheus/Grafana);

- testy ładowania przed/po zmianach.

5. **Wynik (przykład receptury)**

- p95 został warunkowo zmniejszony o 40–60%;

- zwiększona przepustowość bez dodatkowych węzłów DB;

- ustabilizowane okresy szczytowe i zmniejszona rywalizacja o śluzy.

#### Jak odpowiedzieć najbardziej przekonująco:

1. Mów językiem pomiarów, a nie ogólnych zwrotów.

2. Wyjaśnij kompromis: co zostało przyspieszone i jakim kosztem.

3. Podkreśl powtarzalny proces: „najpierw mierzony, potem zmieniany, a następnie
   testowany”.

#### Wniosek:

Silną odpowiedzią na optymalizację bazy danych jest przypadek inżynierski
potwierdzający koncepcję wraz ze wskaźnikami i narzędziami. To właśnie ta
struktura świadczy o dojrzałości i praktycznych kompetencjach.

</details>


<details>
<summary>104. Czym `pgx` różni się od `lib/pq` pod względem wydajności i funkcjonalności?</summary>

#### Go

Oba programy `lib/pq` i `pgx` współpracują z PostgreSQL, ale należą do różnych
generacji ekosystemu Go. We współczesnych scenariuszach produkcyjnych `pgx` jest
ogólnie uważany za bardziej praktyczny wybór.

#### Główna różnica:

1. **`lib/pq`**

- klasyczny sterownik dla `database/sql`;

- stabilny, ale funkcjonalnie konserwatywny;

- mniej nowoczesnych optymalizacji i funkcji specyficznych dla PostgreSQL.

2. **`pgx`**

- nowoczesne sterowniki/narzędzia dla PostgreSQL;

- może pracować zarówno jako natywne API, jak i poprzez warstwę kompatybilną z
  `database/sql`;

- bogatszy zestaw funkcji i często lepsza wydajność pod rzeczywistym
  obciążeniem.

#### Produktywność:

1. `pgx` często wykazuje lepszą przepustowość i mniejsze opóźnienia, szczególnie
   w scenariuszach z dużym obciążeniem.

2. Powody: wydajniejsza obsługa protokołu PostgreSQL, lepsze możliwości
   przetwarzania wsadowego/kopiowania, bardziej elastyczna obsługa typów.

3. Ostateczny wniosek jest zawsze porównywany z obciążeniem pracą.

#### Funkcjonalność:

1. `pgx` zapewnia szerszy dostęp do specyfiki PostgreSQL:

- rozbudowany typowy system;

- batch/Kopiuj elementy podstawowe;

- lepsza kontrola nad zachowaniem połączeń i zapytań.

2. `lib/pq` w większości pozostaje „ledwie wystarczającym” sterownikiem do
   podstawowych zadań ze względu na `database/sql`.

#### Kiedy wybrać:

1. **`pgx`** — dla nowych projektów, dużego obciążenia, potrzeby nowoczesnych
   funkcji PostgreSQL i lepszej kontroli.

2. **`lib/pq`** — głównie starszy kod, w przypadku którego migracja nie jest
   jeszcze uzasadniona.

#### Wniosek:

`pgx` zwykle wygrywa zarówno pod względem funkcjonalności, jak i potencjału
wydajności. `lib/pq` jest historycznie ważny, ale w przypadku większości nowych
systemów Go/PostgreSQL preferowanym wyborem jest `pgx`.

</details>


<details>
<summary>105. Jak pisać testy jednostkowe w Go?</summary>

#### Go

Test jednostkowy w Go testuje małą, izolowaną jednostkę zachowania
(funkcję/metodę) z jasnymi danymi wejściowymi i oczekiwanym wynikiem. Siła tego
podejścia leży w determinizmie, szybkości i przejrzystości przyczyn upadku.

#### Podstawowe zasady jednostkowego testu jakości:

1. **Jedno zachowanie to jedna intencja testowa.**

2. **Izolacja od systemów zewnętrznych** (baza danych, sieć, czas, system
   plików).

3. **Determinizm**: Te same warunki muszą dać ten sam wynik.

4. **Czytelność i diagnostyka** komunikatów o błędach.

#### Struktura idiomatyczna w Go:

1. Plik `*_test.go`.

2. Wyświetl funkcje `func TestXxx(t *testing.T)`.

3. Ułóż → Działaj → Potwierdź wzór.

4. W przypadku wielu przypadków — testy oparte na tabelach.

#### Co należy uwzględnić:

1. Pozytywne scenariusze (szczęśliwa ścieżka).

2. Negatywne skrypty i błędy.

3. Przypadki graniczne (puste dane, zera, duże wartości, nieprawidłowe dane
   wejściowe).

4. Niezmienniki, których nie wolno naruszać w żadnych okolicznościach.

#### Praktyczne narzędzia:

1. Pakiet standardowy `testing`.

2. `go test ./...` do regularnego biegania.

3. `-race` dla witryn konkurencyjnych.

4. W razie potrzeby - `testify` (twierdzenie/wymaganie), ale bez nadmiernej
   magii.

#### Typowe błędy:

1. Testy zależne od czasu/sieci/wykonania.

2. Sprawdzanie tylko „bez paniki”, bez merytorycznych zapewnień.

3. Zbyt duże skrypty integracyjne udające testy jednostkowe.

#### Wniosek:

Pisanie testów jednostkowych w Go oznacza zaprojektowanie weryfikowalnego
zachowania: minimalnej objętości, jasnej umowy, izolacji od świata zewnętrznego
i wiarygodnych asercji. Takie podejście zapewnia szybką i stabilną ochronę przed
regresją.

#### Przykład:

```go
func TestSum(t *testing.T) {
	tests := []struct {
		name string
		a, b int
		want int
	}{
		{"pos", 2, 3, 5},
		{"zero", 0, 7, 7},
	}

	for _, tc := range tests {
		tc := tc
		t.Run(tc.name, func(t *testing.T) {
			got := Sum(tc.a, tc.b)
			if got != tc.want {
				t.Fatalf("got %d, want %d", got, tc.want)
			}
		})
	}
}
```

</details>


<details>
<summary>106. Jaka jest różnica między `t.Error` i `t.Fatal` w testach?</summary>

#### Go

`t.Error` i `t.Fatal` oznaczają test jako zakończony niepowodzeniem, ale
zachowują się inaczej w przypadku kontynuowania wykonywania.

#### `t.Error`:

1. Rejestruje błąd i oznacza test jako nieudany.

2. **Nie zatrzymuje** wykonywania bieżącego testu.

3. Przydatne, gdy chcemy zebrać kilka niezależnych kontroli w jednym przebiegu.

#### `t.Fatal`:

1. Rejestruje błąd i oznacza test jako nieudany.

2. **Natychmiast zatrzymuje** bieżący test (`FailNow`).

3. Stosuje się, gdy bez tego warunku dalsze kontrole nie mają sensu lub mogą
   powodować hałas/panikę.

#### Ogólna zasada:

1. Użyj `t.Fatal`, jeśli podstawowe założenie jest złamane (np. nie udało się
   utworzyć obiektu testowego, otrzymano `nil`, po którym następuje
   dereferencja).

2. Użyj `t.Error`, jeśli chcesz sprawdzić wiele niezależnych warunków końcowych
   i zobaczyć wszystkie odchylenia na raz.

#### Wniosek:

Różnica jest prosta i fundamentalna: `t.Error` — „napraw i kontynuuj”, `t.Fatal`
— „napraw i zatrzymaj natychmiast”. Wybór zależy od tego, czy test pozostaje
znaczący po konkretnym błędzie.

</details>


<details>
<summary>107. Czym `testify/assert` różni się semantycznie od `testify/require`?</summary>

#### Go

Różnica semantyczna pomiędzy `assert` i `require` jest taka sama jak pomiędzy
`t.Error` i `t.Fatal` w standardzie `testing`: jeden pozwala na kontynuację
testu, drugi natychmiast go zatrzymuje.

#### `testify/assert`:

1. Jeśli instrukcja zakończy się niepowodzeniem, oznacza test jako nieudany.

2. **Nie przerywa** wykonywania bieżącego testu.

3. Przydatne, gdy chcesz zebrać wiele niezależnych niespójności w jednym
   przebiegu.

#### `testify/require`:

1. Jeśli potwierdzenie się nie powiedzie, oznacza test jako nieudany.

2. **Natychmiast zatrzymuje** bieżący test (teraz niepowodzenie).

3. Wymagane w przypadku sprawdzenia wymagań wstępnych, bez którego poniższe
   kroki są nieprawidłowe.

#### Kiedy wybrać:

1. `require` — w przypadku krytycznych warunków wstępnych:

- obiekt nie jest `nil`;

- błąd nie występuje przed dalszymi działaniami;

- wejście jest przygotowane poprawnie.

2. `assert` — dla warunków końcowych i niezależnych kontroli wyniku.

#### Wniosek praktyczny:

`require` kontroluje cykl życia testu, `assert` — szczegóły diagnostyczne. Dobry
test zwykle łączy w sobie oba: `require` dla „warunków zatrzymania”, `assert`
dla dalszej kontroli treści.

</details>


<details>
<summary>108. W jaki sposób `t.Run` umożliwia uruchamianie podtestów i ich filtrowanie?</summary>

#### Go

`t.Run` umożliwia zorganizowanie pojedynczego testu w zestaw nazwanych
podtestów. Każdy podprzypadek jest wykonywany jako osobna jednostka logiczna, co
upraszcza testy tabel, diagnostykę i selektywne uruchamianie.

#### Jak działa `t.Run`:

1. W teście głównym wywoływany jest `t.Run(name, func(t *testing.T) { ... })`.

2. Każde wywołanie tworzy oddzielny podtest z własnym `t`.

3. Podtesty mogą mieć różne dane wejściowe, potwierdzenia i ustawienia.

#### Dlaczego jest to wygodne:

1. **Lepsza czytelność testów opartych na tabeli.**

2. **Precyzyjna diagnostyka:** możesz dokładnie zobaczyć, która sprawa padła.

3. **Hierarchia testów:** można zagnieżdżać `t.Run` w grupowanych scenariuszach.

4. **Kontrola współbieżności:** poszczególne podskrzynki można uruchamiać
   poprzez `t.Parallel()`.

#### Jak działa filtrowanie:

1. `go test -run <pattern>` uruchamia testy, których nazwy pasują do wzorca.

2. Ścieżka nazwy jest brana pod uwagę w podtestach (np. `TestXxx/case_name`).

3. Pozwala to na punktowe uruchomienie pojedynczego problemu bez pełnego
   zestawu.

#### Praktyczny przykład myślenia:

1. `TestParser` zawiera dziesiątki przypadków do `t.Run`.

2. Podczas debugowania uruchamiany jest tylko jeden: `go test -run
   'TestParser/invalid_header'`.

3. Uzyskaj szybszą pętlę sprzężenia zwrotnego i czystszy cykl korekcji.

#### Wniosek:

`t.Run` zamienia testy monolityczne w zarządzany system podtestów z szczegółowym
wyzwalaniem i filtrowaniem. Jest to jedno z kluczowych narzędzi wspieranego
projektowania testów w Go.

</details>


<details>
<summary>109. Jak przetestować procedury obsługi HTTP?</summary>

#### Go

Procedury obsługi HTTP w Go są testowane w izolacji, bez prawdziwego gniazda
sieciowego, przy użyciu `httptest`. Celem jest przetestowanie kontraktu warstwy
HTTP: stanu, nagłówków, treści odpowiedzi, obsługi błędów i scenariuszy
brzegowych.

#### Podejście kanoniczne:

1. Utwórz żądanie poprzez `httptest.NewRequest(...)`.

2. Utwórz rejestrator za pomocą `httptest.NewRecorder()`.

3. Osoba obsługująca połączenie: `handler.ServeHTTP(rec, req)`.

4. Sprawdź:

- `rec.Code` (kod stanu);

- nagłówki;

- body (JSON/schemat/wiadomość).

#### Co należy uwzględnić:

1. **Szczęśliwa ścieżka** (poprawne żądanie, oczekiwana odpowiedź).

2. **Błędy walidacji** (niekompletny/nieprawidłowy ładunek, parametry
   zapytania).

3. **Metody HTTP** (GET/POST/PUT/DELETE + 405, jeśli metoda nie jest dozwolona).

4. **Błędy zależności** (usługa/repozytorium zwraca błąd).

5. **Skrypty kontekstowe** (przekroczenie limitu czasu/anulowanie, jeśli logika
   to obsługuje).

#### Wskazówki architektoniczne:

1. Eksportuj logikę biznesową z procedury obsługi do warstwy usług.

2. W testach modułu obsługi próbne/fałszywe zależności usług.

3. Przetestuj sam kontrakt HTTP, a nie wewnętrzną implementację.

#### Praktyczne minimalne kontrole:

1. Poprawnie `Content-Type`.

2. Struktura odpowiedzi JSON.

3. Zgodność kodów stanu z błędami domeny.

4. Brak wycieku poufnych informacji w treści błędu.

#### Wniosek:

Test obsługi HTTP w Go to test zachowania punktu końcowego jako czarnej
skrzynki: żądanie przychodzące → wyczyść wyjście HTTP. `httptest` zapewnia
szybkie, deterministyczne i w miarę dokładne narzędzie do testowania takich
kontraktów.

#### Przykład:

```go
req := httptest.NewRequest(http.MethodGet, "/health", nil)
rec := httptest.NewRecorder()

handler.ServeHTTP(rec, req)

if rec.Code != http.StatusOK {
	t.Fatalf("status=%d", rec.Code)
}
```

</details>


<details>
<summary>110. Jak sprawdzić błędy?</summary>

#### Go

Testowanie błędów w Go powinno sprawdzać nie tylko fakt istnienia błędu, ale
także jego semantykę: typ, kategorię, łańcuch opakowania i oczekiwaną reakcję
systemu.

#### Co dokładnie sprawdzić:

1. **Występowanie/brak błędu** w konkretnym scenariuszu.

2. **Kategoria błędu** spowodowana `errors.Is` (błędy wartownicze).

3. **Typ błędu** poprzez `errors.As` (niestandardowy typ błędu z polami).

4. **Kontekst opakowania** (czy pierwotna przyczyna zostanie utracona przez
   `%w`).

5. **Efekt behawioralny**: poprawny kod stanu, ponowna próba/brak ponownej
   próby, wycofanie itp.

#### Zalecane praktyki:

1. Unikaj delikatnych kontroli pełnotekstowych `err.Error()`.

2. W przypadku stabilnych kontraktów użyj `errors.Is/As`, a nie `==` w przypadku
   opakowanych błędów.

3. W testach opartych na tabeli jawnie określ oczekiwaną klasę błędu i
   konsekwencje.

#### Co testować w negatywnych scenariuszach:

1. Błędy sprawdzania poprawności danych wejściowych.

2. Błędy zależności zewnętrznych (DB, HTTP, kolejki).

3. Przekroczenia limitu czasu/przerwanie przez `context`.

4. Stany graniczne (puste wartości, nieprawidłowe formaty, przekroczone limity).

#### Akcent architektoniczny:

1. Błąd musi być częścią kontraktu API funkcji.

2. Testy muszą wykazać, że obsługa błędów jest deterministyczna i przewidywalna.

3. Jeśli system mapuje błędy domeny na warstwę transportową, przetestuj to
   mapowanie osobno.

#### Wniosek:

Jakościowe testowanie błędów w Go polega na sprawdzaniu semantyki, a nie ciągu
komunikatu. Tego rodzaju weryfikacja sprawia, że ​​kod jest odporny na
refaktoryzację i niezawodny w produkcji.

</details>


<details>
<summary>111. Jak zwilżyć zależności zewnętrzne bez korzystania z frameworków innych firm?</summary>

#### Go

W Go zewnętrzne zależności są wyśmiewane najprościej poprzez interfejsy i własne
implementacje z podwójnym testem (stub/fake/spy), bez potrzeby stosowania
ciężkich frameworków do kpin. Jest to podejście idiomatyczne, które można dobrze
skalować i które pozostaje przejrzyste.

#### Schemat podstawowy:

1. Podświetl interfejs minimalnej zależności w warstwie konsumenta.

2. Implementacja produkcyjna działa z prawdziwą bazą danych/HTTP/kolejką.

3. W teście zastąp własną strukturę, która implementuje ten sam interfejs.

#### Testuj typy podwójne bez bibliotek innych firm:

1. **Stub** — zwraca predefiniowane dane.

2. **Fałszywe** - uproszczona „działająca” implementacja (na przykład
   repozytorium w pamięci).

3. **Spy** — przechwytuje połączenia (argumenty, numer, kolejność).

4. **Ręczna próbna wersja** — skrypt z przewodnikiem z dostosowywalnymi
   odpowiedziami/błędami.

#### Zalety tego podejścia:

1. Pełne bezpieczeństwo typów kompilatora.

2. Magia czasu działania zerowego.

3. Lepsza czytelność testów i przewidywalna ewolucja kodu.

4. Brak zewnętrznych zależności na stosie testowym.

#### Zalecenia praktyczne:

1. Spraw, aby interfejsy były małe (ze względu na zachowanie, a nie „we
   wszystkich metodach”).

2. Mot na granicy modułu, a nie wewnątrz logiki domeny.

3. W scenariuszach konkurencyjnych należy chronić podwójny test stanu (`mutex`,
   atomy).

4. Nie powielaj nadmiernie logiki produkcji w fałszywych - w przeciwnym razie
   testy staną się kruche.

#### Wniosek:

Wyśmiewanie bez frameworków w Go polega przede wszystkim na dobrym projektowaniu
zależności: mały interfejs + ręczny test-double. Podejście to jest proste,
niezawodne i rozsądne pod względem architektonicznym, co zapewnia długoterminowe
wsparcie projektu.

</details>


<details>
<summary>112. Jak używać `TestMain` do skonfigurowania środowiska testowego? </summary>

#### Go

`TestMain(m *testing.M)` to punkt wejścia dla całego zestawu testów. Umożliwia
globalną inicjalizację przed testami i gwarantuje sprzątanie po nich.

#### Kiedy `TestMain` jest właściwe:

1. Należy raz wywołać udostępnione środowisko testowe:

- testowa baza danych/kontener;

- katalogi tymczasowe;

- konfiguracje/sekrety globalne;

- zależności usług w tle.

2. Wymaga scentralizowanego usunięcia po zakończeniu wszystkich testów pakietu.

#### Podstawowy cykl życia:

1. Trwa instalacja (inicjalizacja zasobów).

2. Testy trwają przez `code := m.Run()`.

3. Trwa czyszczenie.

4. Proces kończy się poprzez `os.Exit(code)`.

#### Ważne zasady:

1. `m.Run()` należy wywołać dokładnie raz.

2. Zwrócony kod należy przekazać do `os.Exit`, w przeciwnym razie status testów
   zostanie utracony.

3. Czyszczenie należy przeprowadzić nawet w przypadku błędów konfiguracji (o ile
   to możliwe).

4. Nie wykonuj dodatkowej logiki w `TestMain`, która nie jest związana ze
   środowiskiem.

#### Praktyczne wskazówki:

1. Nie polegaj wyłącznie na `TestMain` w celu izolowania testów w pakiecie —
   często nadal konieczna jest lokalna konfiguracja/porzucenie w określonych
   testach.

2. Jeśli to możliwe, preferuj lżejsze mechanizmy (`t.Cleanup`) na poziomie
   testowym; `TestMain` użyj w prawdziwym kontekście wsadowym.

3. W testach równoległych uważnie monitoruj stan współdzielony zainicjowany w
   `TestMain`.

#### Wniosek:

`TestMain` — narzędzie do wsadowej orkiestracji środowiska testowego: jedna
konfiguracja, jedno uruchomienie wszystkich testów, jedno czyszczenie. Sprawdza
się tam, gdzie trzeba kontrolować cykl życia współdzielonych zasobów dla całego
pakietu.

</details>


<details>
<summary>113. Jak korzystać ze złotych pilników?</summary>

#### Go

`Golden files` to pliki referencyjne z oczekiwanymi wynikami, z którymi test
porównuje rzeczywiste wyniki. Podejście to jest szczególnie przydatne w
przypadku programów formatujących, generatorów kodu, serializacji i dowolnego
tekstu/struktury wyjściowej.

#### Podstawowy przepływ pracy:

1. Wygeneruj wynik za pomocą testowanej funkcji.

2. Przeczytaj odpowiedni plik `.golden`.

3. Porównaj rzeczywistą moc wyjściową ze standardem.

4. Jeśli istnieje różnica, test kończy się niepowodzeniem z powodu różnicy.

#### Typowa struktura:

1. Wejście testowe (`testdata/input/...`).

2. Standardy (`testdata/golden/...`).

3. Testy oparte na tabelach, w których każdy przypadek ma swój własny złoty
   plik.

#### Bardzo przydatna praktyka — tryb aktualizacji:

1. Dodaj flagę, np. `-update`.

2. Jeśli opcja jest włączona, test nadpisuje złote pliki nowym wynikiem.

3. Przyspiesza to obsługę testów porównawczych z uzasadnionymi zmianami
   zachowania.

#### Na co zwrócić uwagę:

1. **Wyjście determinizmu:** przed porównaniem znormalizuj kolejność danych,
   znaczniki czasu i wartości losowe.

2. **Różnica jakościowa:** w przypadku awarii testowej powinno być jasne, co
   dokładnie się zmieniło.

3. **Nie nadużywaj:** złote pliki dla dużych „czarnych skrzynek” bez kontroli
   semantycznej mogą utrudniać diagnostykę.

#### Kiedy złote pilniki są najbardziej odpowiednie:

1. Renderowanie/generowanie tekstu.

2. Transformacja JSON/XML/config.

3. Wyjście CLI.

4. Kompilatory, parsery, generatory kodu.

#### Wniosek:

Złote pliki to praktyczne narzędzie do testowania wyników kontraktów.
Zapewniając determinizm i wygodny proces aktualizacji, zapewniają szybką i
przejrzystą ochronę przed niepożądanymi regresjami w formacie wyniku.

</details>


<details>
<summary>114. Jak poprawnie przetestować kod Go, który używa `time.Now()`, aby testy były deterministyczne?</summary>

#### Go

`time.Now()` sprawia, że testy są niedeterministyczne, ponieważ zwraca
rzeczywisty bieżący czas. Aby testy były stabilne, należy wstrzyknąć czas, a nie
wczytać go bezpośrednio do logiki biznesowej.

#### Podejście kanoniczne:

1. Eksportuj źródło czasu do zależności:

- funkcja `now func() time.Time`;

- interfejs `Clock` z metodą `Now()`.

2. W produkcji przenieś zegar rzeczywisty (`time.Now`).

3. Prześlij w teście ustalony czas (fałszywy zegar).

#### Dlaczego to działa:

1. Wynik nie zależy od momentu rozpoczęcia testu.

2. Zniknęły niepewne scenariusze „czasami się zawieszają, czasem nie”.

3. Łatwo sprawdzaj przypadki Edge: terminy, TTL, daty przejścia, strefy czasowe.

#### Dodatkowe praktyki:

1. Nie porównuj wartości czasu ze „twardą” dokładnością do milisekund, chyba że
   jest to wymagane przez domenę.

2. W przypadku testów z timerami/opóźnieniami użyj kontrolowanego zegara lub
   wystarczających buforów czasu.

3. Napraw `Location/UTC` jawnie, aby uniknąć zależności środowiskowych.

#### Czego nie robić:

1. Pozostaw `time.Now()` w głębi logiki domeny bez możliwości podstawienia.

2. Ratowanie `time.Sleep` w testach spowalnia i nie gwarantuje stabilności.

#### Wniosek:

Deterministyczne testowanie taktowania w Go opiera się na odwróceniu zależności:
synchronizacja jest sygnałem wejściowym, a nie globalnym efektem ubocznym.
Wstrzykiwanie źródła zegara sprawia, że ​​testy są szybkie, powtarzalne i
architektonicznie czyste.

</details>


<details>
<summary>115. W jaki sposób `t.Parallel()` przyspiesza zestaw testów i gdzie może je zepsuć?</summary>

#### Go

`t.Parallel()` umożliwia jednoczesne uruchamianie testów (lub podtestów), co
zazwyczaj skraca całkowity czas działania w środowiskach wielordzeniowych. Ale
współbieżność bez izolacji łatwo zamienia stabilne testy w niestabilne.

#### Jak przyspiesza biegi:

1. Niezależne testy działają jednocześnie.

2. Lepsze wykorzystanie procesora i czekanie we/wy.

3. Duży zestaw małych testów działa znacznie szybciej w CI.

#### Gdzie `t.Parallel()` może złamać testy:

1. **Współdzielony stan zmienny:** zmienne globalne, współdzielone pamięci
   podręczne w pamięci, konfiguracje statyczne bez synchronizacji.

2. **Zewnętrzne zasoby współdzielone:** jeden schemat/tabela DB, jeden port,
   jeden plik, jeden tymczasowy katalog danych.

3. **Zależność kolejności wykonania:** jeśli test domyślnie oczekuje, że inny
   został już uruchomiony.

4. **Skutki uboczne dla środowiska:** zmiany w zmiennych środowiskowych, strefie
   czasowej, katalogu roboczym bez izolacji.

5. **Błędy w podtestach opartych na tabeli:** przechwytywanie zmiennych w pętli
   bez lokalnej kopii w zamknięciu.

#### Jak bezpiecznie używać:

1. Tylko równoległe, w pełni izolowane testy.

2. Unikaj globalnego stanu zmiennego lub chroń go za pomocą synchronizacji.

3. Użyj unikalnych zasobów tymczasowych (`t.TempDir`, pojedyncze urządzenia).

4. W przypadku testów DB — izolacja transakcyjna lub osobna przestrzeń
   nazw/schemat na test.

5. Uruchom zestaw z `-race`, aby wcześnie wykryć problemy z konkurencją.

#### Wniosek:

`t.Parallel()` to potężny akcelerator testów, ale tylko przy ścisłej izolacji
przypadków. Jeśli testy mają wspólny stan lub ukryte zależności, współbieżność
ujawni te defekty i sprawi, że przebieg będzie niestabilny.

</details>


<details>
<summary>116. Jak zmierzyć pokrycie kodu? </summary>

#### Go

W Go pokrycie kodu jest mierzone za pomocą wbudowanych narzędzi `go test` za
pomocą oprzyrządowania do wykonywania testów. Zapewnia to metryki pokazujące,
jaka część linii/bloków kodu została wykonana podczas przebiegu testu.

#### Podstawowe polecenia:

1. Całkowity zakres ubezpieczenia na paczkę: `go test -cover ./...`

2. Zbiór profili ubezpieczenia: `go test -coverprofile=coverage.out ./...`

3. Wyświetl statystyki podsumowujące: `go tool cover -func=coverage.out`

4. Wyróżniony raport HTML: `go tool cover -html=coverage.out`

#### Co należy zrozumieć:

1. Pokrycie pokazuje fakt, że kontrole niezmienne są przeprowadzane, a nie
   kompletne.

2. Wysoki procent nie gwarantuje braku błędów.

3. Niski procent jest sygnałem ślepych obszarów testowych.

#### Praktyczne wskazówki:

1. Analizuj pokrycie wraz z krytycznością kodu, zamiast gonić za „100%”.

2. Oddzielnie omów scenariusze negatywne i skrajne.

3. Używaj zasięgu jako wskaźnika luk, a nie celu samego w sobie.

4. W CI zapisz profil i śledź dynamikę zasięgu między PR.

#### Wniosek:

Pokrycie kodu w Go mierzy się za pomocą standardowych narzędzi (`go test` + `go
tool cover`) i jest użyteczną miarą jakości recenzji testów. Zapewnia największą
wartość w połączeniu z kontrolami semantycznymi i sensownym projektem testów.

</details>


<details>
<summary>117. Co to jest benchmarking i jak go przeprowadzić? W jaki sposób `testing.B` wdraża test porównawczy i co resetuje `b.ResetTimer`?</summary>

#### Go

`Benchmarking` w Go to pomiar wydajności kodu (czas, alokacje, przepustowość) w
kontrolowanych warunkach w celu porównania implementacji i sprawdzenia efektu
optymalizacji.

#### Jak uruchomić test porównawczy:

1. Funkcje mają postać: `func BenchmarkXxx(b *testing.B)`.

2. Uruchomienie bazy: `go test -bench=.`

3. Tylko konkretny punkt odniesienia: `go test -bench=BenchmarkParse`

4. Miara alokacji: `go test -bench=. -benchmem`

#### Jak działa `testing.B`:

1. Runner sam wybiera `b.N` (liczbę iteracji), aby uzyskać stabilny wymiar.

2. Twój kod w funkcji testowej jest wykonywany w pętli `for i := 0; i < b.N;
   i++`.

3. W rezultacie test ocenia wydajność w `ns/op`, a w przypadku `-benchmem`
   również `B/op`, `allocs/op`.

#### Co robi `b.ResetTimer`:

1. Zresetuj licznik skumulowanych pomiarów.

2. Nie liczy kodu przygotowawczego wykonanego przed ostatecznym wywołaniem
   `ResetTimer`.

3. Używany po fazie konfiguracji do pomiaru tylko „czystej” części roboczej.

#### Powiązane przydatne metody:

1. `b.StopTimer()` / `b.StartTimer()` — tymczasowo wyłącz/włącz pomiar czasu.

2. `b.ReportAllocs()` — statystyki przydziału sił.

#### Wniosek praktyczny:

Benchmark w Go nie jest jednorazowym uruchomieniem, ale narzędziem porównawczym
na tych samych warunkach. `testing.B` automatycznie skaluje iteracje, a
`b.ResetTimer` oddziela szkolenie od rzeczywistego pomiaru wydajności.

#### Przykład:

```go
func BenchmarkParse(b *testing.B) {
	input := []byte(`{"x":1}`)
	b.ResetTimer()

	for i := 0; i < b.N; i++ {
		var v map[string]int
		_ = json.Unmarshal(input, &v)
	}
}
```

</details>


<details>
<summary>118. Jak uruchamiać testy porównawcze z kontrolą czasu i liczby iteracji?</summary>

#### Go

W Go można uruchamiać testy porównawcze z kontrolą czasu trwania pomiaru i stałą
liczbą iteracji za pomocą parametrów `go test`. Jest to ważne dla powtarzalności
i prawidłowego porównania wyników.

#### Główne flagi:

1. **`-benchtime`**

- ustawia czas trwania testu porównawczego (na przykład `-benchtime=5s`);

- biegacz sam wybiera `b.N`, który będzie biegał w tym oknie czasowym.

2. **`-benchtime=Nx`**

- poprawia dokładną liczbę iteracji (na przykład `-benchtime=100000x`);

- przydatny do powtarzalnych porównań A/B tego samego `N`.

3. **`-count`**

- liczba powtórzeń (np. `-count=10`);

- pomaga ocenić stabilność i rozproszenie wyników.

4. **`-bench`**

- wybór określonych funkcji wzorcowych według wzorca.

5. **`-benchmem`**

- dodatkowo wyprowadza alokacje (`B/op`, `allocs/op`).

#### Praktyczne przykłady scenariuszy:

1. Dłuższa stabilna praca: `go test -bench=. -benchtime=5s -benchmem`

2. Naprawiono `N`: `go test -bench=BenchmarkFoo -benchtime=200000x -benchmem`

3. Wiele powtórek dla statystyk: `go test -bench=BenchmarkFoo -benchtime=2s
   -count=10`

#### Dlaczego jest to konieczne:

1. Zmniejsz hałas podczas krótkich serii.

2. Porównaj optymalizacje w tych samych warunkach.

3. Otrzymaj istotne statystycznie dane do analizy `benchstat`.

#### Wniosek:

Kontrola czasu i iteracji w testach porównawczych Go jest warunkiem wstępnym
wysokiej jakości analizy wydajności. `-benchtime` i `-count` zapewniają
stabilność pomiaru, a tryb `Nx` zapewnia ścisłą kontrolę nad liczbą wykonań.

</details>


<details>
<summary>119. W jaki sposób narzędzie `benchstat` porównuje dwa zestawy wyników testów porównawczych i jak określa znaczenie zmian?</summary>

#### Go

`benchstat` porównuje dwa (lub więcej) zestawy wyników testów porównawczych i
pokazuje, czy zmiany w metrykach (`ns/op`, `B/op`, `allocs/op`) są statystycznie
istotne, a nie losowym szumem przebiegu.

#### Jak działa porównanie:

1. Zbierz wiele przebiegów „przed” i „po” (zwykle za pośrednictwem `-count`).

2. `benchstat` grupuje wyniki według tych samych nazw testów porównawczych.

3. Oblicza wartości centralne (zwykle szacunki podobne do mediany/solidne) i
   różnicę procentową.

4. Wykonuje test statystyczny i generuje wynik `p-value`.

#### Jak określa się istotność:

1. Jeśli `p-value` jest poniżej poziomu progowego (zwykle 0,05), zmianę uznaje
   się za istotną statystycznie.

2. Jeśli `p-value` przekracza próg, różnicą może być hałas otoczenia.

3. Dlatego ważne jest, aby jednocześnie przyjrzeć się **zarówno delcie, jak i
   wartości p**.

#### Co jest potrzebne do prawidłowej analizy:

1. Te same warunki uruchamiania (maszyna, obciążenie, konfiguracja).

2. Wystarczająca liczba powtórzeń (`-count`), w przeciwnym razie wnioski będą
   kruche.

3. Brak zewnętrznych szumów (procesy w tle, dławienie termiczne, niestabilne
   środowisko CI).

#### Ogólna zasada:

1. Nie ufaj jednorazowym `go test -bench`.

2. Zbierz serię wyników przed/po.

3. Przeanalizuj `benchstat`, a następnie sprawdź, czy zmiana jest istotna dla
   wskaźników biznesowych (opóźnienie/przepustowość/SLA), a nie tylko „ładna” w
   tabeli.

#### Wniosek:

`benchstat` przekształca surowe liczby porównawcze w statystycznie rzetelne
porównanie. Pomaga odróżnić rzeczywisty efekt wydajności od losowego
rozproszenia i podejmować decyzje inżynieryjne na podstawie danych.

</details>


<details>
<summary>120. Co to jest testowanie rozmyte?</summary>

#### Go

`Fuzz testing` to zautomatyzowana metoda testowania, w której system otrzymuje
dużą ilość półlosowych lub zmutowanych danych wejściowych w celu wykrycia
awarii, paniki, nieprawidłowej obsługi przypadków brzegowych i niezmiennych
naruszeń.

#### Jak to działa w Go:

1. Ustaw funkcję fuzz (`func FuzzXxx(f *testing.F)`).

2. Dodaj wpisy początkowe (przykłady początkowe).

3. Fuzzer mutuje te wejścia i generuje nowe kombinacje.

4. Jeśli wykryje awarię lub naruszenie zasad sprawdzania, zachowaj „minimalną”
   liczbę możliwych do odtworzenia przypadków.

#### Co testy fuzz sprawdzają najlepiej:

1. Nieoczekiwane przypadki brzegowe parserów/dekoderów.

2. Panika z powodu nieprawidłowych lub „uszkodzonych” danych wejściowych.

3. Błędy logiczne w przetwarzaniu linii, bajtów, formatów, protokołów.

#### Dlaczego jest to cenne:

1. Zajmuje przestrzeń wejściową znacznie szerszą niż obudowy jednostek ręcznych.

2. Dobrze wykrywa luki w zabezpieczeniach w kodzie podobnym do parsera.

3. Dodaje odporność API na „toksyczne” ładunki ze świata zewnętrznego.

#### Zalecenia praktyczne:

1. Sformułuj jawne niezmienniki (które muszą być prawdziwe dla każdego wejścia).

2. Zacznij od powierzchni krytycznych: parsowanie, deserializacja, normalizacja.

3. Po znalezieniu przypadku dodaj go jako test regresji.

4. Połącz fuzzing z `-race` i zwykłymi testami jednostkowymi/integracyjnymi.

#### Wniosek:

Testowanie fuzz w Go to systematyczny sposób na „łamanie” kodu danymi
wejściowymi w celu znalezienia defektów, których prawie nie da się przewidzieć
ręcznie. Jest to jedno z najpotężniejszych narzędzi zwiększających niezawodność
i bezpieczeństwo przetwarzania danych.

</details>


<details>
<summary>121. Jakie są sposoby uruchamiania testów z bazy danych w CI (kontenery testowe, tworzenie doków, usługi GitHub Actions)? Jakie są zalety każdego podejścia?</summary>

#### Go

Do testów integracyjnych z DB w CI najczęściej stosuje się trzy podejścia:
`Testcontainers`, `docker-compose` i `GitHub Actions services`. Wybór zależy od
pożądanego poziomu izolacji, złożoności stosu i szybkości potoku.

#### 1) Kontenery testowe

**Podstawa:** kontenery są tworzone programowo na podstawie testów i uruchamiane
w trakcie przebiegu testowego.

**Zalety:**

1. Maksymalna bliskość kodu testowego (opisane poniżej obok testów).

2. Wysoka izolacja przypadków i przewidywalne środowisko.

3. Elastyczne zarządzanie cyklem życia bazy danych, wersjami, skryptami
   inicjującymi.

4. Wygodny do lokalnego odtwarzania skryptów CI.

#### 2) tworzenie dokera

**Esencja:** usługi (DB + zależności) opisane w `docker-compose.yml`, powstają
przed testami jako pojedyncza kompozycja.

**Zalety:**

1. Prosty i wizualny opis środowiska obejmującego wiele usług.

2. Łatwo jest dodawać pamięci podręczne, brokerów i kilka baz danych
   jednocześnie.

3. Ten sam model dla lokalnych programistów i CI.

4. Dobry wybór do zestawów integracyjnych/e2e.

#### 3) Usługi GitHub Actions

**Podstawa:** kontener DB jest deklarowany bezpośrednio w zadaniu przepływu
pracy jako kontener usług.

**Zalety:**

1. Najprostszy skrypt natywny CI dla podstawowych potrzeb.

2. Minimalny kod w testach i oddzielna aranżacja.

3. Szybki start dla jednej lub dwóch usług (Postgres, Redis itp.).

#### Porównanie praktyczne:

1. **Elastyczność i izolacja**: Kontenery testowe > tworzenie dokerów > usługi.

2. **Łatwy start**: usługi > tworzenie dokerów > Kontenery testowe.

3. **Wielousługowe stojaki kompozytowe**: docker-compose / kontenery testowe.

4. **Lakoniczny CI dla prostej bazy danych**: usługi GitHub Actions.

#### Wniosek:

Nie ma uniwersalnie „najlepszego” podejścia. W przypadku prostego CI wystarczą
usługi; docker-compose jest odpowiedni dla złożonego środowiska integracyjnego;
w przypadku najłatwiejszych w zarządzaniu i powtarzalnych testów na poziomie
kodu najsilniejszym podejściem są kontenery testowe.

</details>
