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
