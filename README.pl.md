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
