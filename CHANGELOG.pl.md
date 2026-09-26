# Historia zmian

Istotne zmiany w Malek Symbiosis Standard.

Format według [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), wersjonowanie według [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

**Uwaga o zakresie tego pliku.** Wpisy od wersji 4.4.0 są tutaj po polsku w całości. Starsze wpisy — 4.0.0 do 4.3.3 — są wyłącznie po angielsku w [CHANGELOG.md](CHANGELOG.md) i tam zostają. To jest świadoma decyzja: historia zmian jest zapisem technicznym, a dwa równoległe zapisy historyczne rozjeżdżają się prędzej czy później i wtedy nie wiadomo, który jest prawdziwy. Podsumowanie tego, co działo się wcześniej, znajdziesz niżej.

**Uwaga o słownictwie.** Każdy wpis używa słów, które obowiązywały w opisywanej przez niego wersji. Tam, gdzie nazwa zmieniła się później, mówi o tym wpis, który ją zmienił.

---

## [4.5.0] — <!-- DO UZUPEŁNIENIA PRZEZ AUTORA -->

**Zasady wyprowadzone z README.** Do tej pory README było specyfikacją: zaczynało od tego, czym MSS jest, i przechodziło od razu we wszystkie zasady, rozdział po rozdziale. Jeden plik obsługiwał dwóch odbiorców i żadnego nie obsługiwał dobrze. Ktoś, kto decydował, czy to jest warte jego czasu, musiał przeczytać specyfikację; ktoś, kto to wdrażał, za każdym razem przedzierał się przez wstęp.

**Żadna zasada się nie zmieniła.** Każda zasada w 4.5.0 mówi dokładnie to, co mówiła w 4.4.0, w tej samej kolejności i tymi samymi słowami. Zmieniło się to, w którym pliku stoi.

### Dodane

- **[STANDARD.pl.md](standard/STANDARD.pl.md) i [STANDARD.md](standard/STANDARD.md).** Pełna specyfikacja: cztery mechanizmy, skutek, bramka systemu, przegląd, flagi, werdykt, zapis, odmowa, dwie zasady ogólne i to, czego framework nie załatwia. To jest tekst kanoniczny i to jest to, co wkleja się modelowi.
- **Polskie wersje wszystkiego, co czyta człowiek:** [DIAGRAMS.pl.md](guides/DIAGRAMS.pl.md), [NAME-USAGE.pl.md](guides/NAME-USAGE.pl.md), [SECURITY.pl.md](SECURITY.pl.md), [CONTRIBUTING.pl.md](CONTRIBUTING.pl.md) oraz wszystkie cztery pliki w `examples/`. Diagramy mermaid przetłumaczone etykieta po etykiecie i sprawdzone ponownie: 4 bloki, 0 błędów, w obu językach, na identycznych numerach linii.

### Zmienione — 18 września 2026

- **Główny plik `CLAUDE.md` zmienił nazwę na `AGENT.md`.** Instrukcja repozytorium nie jest już opisana jako plik przeznaczony wyłącznie dla Claude Code. Z tego samego pliku mogą korzystać Claude, ChatGPT, Cline i inne narzędzia, które odczytują instrukcje z repozytorium. Zawartość została napisana pełnymi zdaniami i prostym językiem. Zasady MSS nie zmieniły się.
- **Instrukcje uruchomienia wskazują teraz główny plik `AGENT.md`.** Najpierw wkleja się do niego standard, a następnie wykonawczy plik `standard/AGENT.pl.md`.

### Zmienione

- **README jest teraz wizytówką i niczym więcej.** Odpowiada po kolei na cztery pytania — czym to jest, skąd się wzięło, po co jest i jak działa — a potem wskazuje plik, który niesie zasady. Zawiera jeden kompletny krótki zapis, żeby czytelnik zobaczył wynik bez czytania specyfikacji, oraz tabelę mówiącą, który plik jest dla kogo.
- **README mówi, skąd MSS się wziął.** Nic w repozytorium wcześniej tego nie mówiło. Punktacja, od której projekt wziął starą nazwę, została usunięta, bo pozwalała nadrobić niską ocenę etyczną wysoką oceną biznesową — a to jest dokładnie ta arytmetyka, której framework ma odmawiać. Jeden akapit osobistego kontekstu jest oznaczony do uzupełnienia albo wycięcia przez autora.
- **Każde odwołanie mówiące „rdzeń" mówi teraz „standard"** i wskazuje na `STANDARD.pl.md`, w `AGENT.pl.md`, `USE-WITH-CLAUDE.pl.md`, `DIAGRAMS.pl.md`, `NAME-USAGE.pl.md`, `CONTRIBUTING.pl.md` i we wszystkich `examples/`. `USE-WITH-CLAUDE` każe teraz wkleić `STANDARD.pl.md`, a nie `README.pl.md`.
- **Repozytorium ułożone pod publikację.** Pliki, których GitHub szuka w katalogu głównym, tam zostają — README, LICENSE, CITATION.cff, CONTRIBUTING, SECURITY, CHANGELOG. Reszta przeniesiona do `standard/` (tekst kanoniczny i plik wykonawczy, trzymane razem, bo wkleja się je razem), `guides/` (jak uruchomić, używanie nazwy, diagramy) oraz `assets/`. Dodany `.gitattributes`, żeby kopia na Windowsie i kopia na Linuksie dawały ten sam plik, oraz `.github/` z dwoma formularzami zgłoszeń — dziura w bramce systemu i sformułowanie, które wprowadziło w błąd prawdziwego czytelnika — plus szablon pull requesta pytający o oba języki i o zasadę, którą zmiana zastępuje.
- **Nowy rozdział w README mówi, co jest opublikowane, a co nie.** To, co tu stoi, jest szkieletem: zasady i procedura. Warstwa, która pracuje we własnych aplikacjach autora, jest zbudowana na tym szkielecie i nie jest publikowana — nie dlatego, że jest lepsza, tylko dlatego, że jest podłączeniem produktowym, bezużytecznym dla kogokolwiek innego. Zasady w tym repozytorium są tymi samymi zasadami co w tamtej warstwie, co do słowa; nie ma tu wersji demonstracyjnej.

### Uwaga o strukturze dwóch plików

Do wklejenia są nadal dwa pliki, a nie jeden: standard, potem `AGENT.pl.md`. Są osobne, bo odpowiadają na różne pytania — standard mówi, jakie są zasady, a `AGENT.pl.md` mówi, kiedy model ma je uruchomić bez pytania. Scalenie dałoby jedno wklejenie zamiast dwóch, ale oznaczałoby też, że czytelnik szukający zasad musi przeczytać warunki wyzwalania. Jeśli ta zamiana okaże się później warta zrobienia, to jedno scalenie i jedno przekierowanie.

---

## [4.4.0] — <!-- DO UZUPEŁNIENIA PRZEZ AUTORA -->

Wszystkie pliki w repozytorium przepisane tak, żeby dały się zrozumieć za pierwszym czytaniem przez kogoś, kto ich nigdy nie widział. **Żadna zasada się nie zmieniła.** Każda zasada w 4.4.0 mówi to, co mówiła w 4.3.3; zmieniło się to, że teraz mówi także **dlaczego** i pokazuje, **jak to wygląda**.

Test czytelnika przeprowadzony na 4.3.3 dał dwa razy ten sam werdykt: instrukcja była wykonywana, powody nie były rozumiane. Wszystko, co mówiło *co zrobić*, czytało się gładko. Wszystko, co mówiło *dlaczego*, trzeba było czytać dwa razy albo wychodziło odwrotnie. Własna lektura autora to potwierdziła: „czytam i trochę nie wiem co czytam".

### Dodane

- **[USE-WITH-CLAUDE.pl.md](guides/USE-WITH-CLAUDE.pl.md) i [USE-WITH-CLAUDE.md](guides/USE-WITH-CLAUDE.md).** Trzy sposoby uruchomienia MSS — Projekt w Claude, pojedyncza rozmowa albo Claude Code — z gotowym do wklejenia blokiem skróconym dla czatu, ze sprawdzeniem, czy instrukcja została w ogóle podjęta, i z wprost napisanym opisem tego, co w oknie czatu nie działa: brak pamięci między rozmowami, brak możliwości zweryfikowania tego, co się modelowi mówi, i to, że nic nie powstrzymuje przed otwarciem nowego czatu bez instrukcji. Plik odsyła też do testu, którego wymaga punkt 8.2 standardu, i prosi o jego wyniki.

### Zmienione

- **Limit 140 linii rdzenia wycofany.** Liczył linie, więc nie umiał odróżnić nowej zasady od zdania wyjaśniającego zasadę już istniejącą i kazał płacić za jedno i drugie tyle samo — przez co najtańszym sposobem zmieszczenia się w nim było pisanie zasad bez wyjaśnień. Limit został zastąpiony w [CONTRIBUTING.pl.md](CONTRIBUTING.pl.md) limitem **liczby zasad**: dodanie zasady nadal wymaga wycięcia zasady, ale `Dlaczego:`, `Przykład:` i `Uwaga:` można dokładać swobodnie.
- **Każda zasada, którą da się przeczytać na dwa sposoby, ma teraz przykład.** Rozpracowane przypadki stoją wewnątrz samych zasad, a nie tylko w `examples/`: wiążąca oferta, którą technicznie da się wycofać, a która jest nieodwracalna przez warunek 3; podwyżka cennika nieodwracalna przez warunek 2; umowa o grafik podpisana przez właściciela, a odczuwana przez kierowcę; jedyny dostawca, dla którego odmowa kosztuje więcej niż zgoda; narzędzie do masowej wysyłki oceniane jako przekazanie zamiast jako zastosowanie.
- **Trzy znaczniki przechodzą przez cały tekst i są zadeklarowane na górze.** `Dlaczego:` dla powodu istnienia zasady, `Przykład:` dla przypadku rozstrzygającego, który odczyt jest właściwy, `Uwaga:` dla miejsca, w którym czytelnicy najczęściej się mylą.
- **Osiem zasad ponumerowanych, każda z własnym nagłówkiem.** Wcześniej szły jednym ciągiem. Test czytelnika wykazał, że siedem z ośmiu jest rozumianych inaczej, niż są zdefiniowane, bo nazwy brzmią jak zdrowy rozsądek i odpowiada się na nie z samej nazwy. Cztery z nich — *Czy mogą odmówić*, *Kto odpowiada*, *Czy powinniśmy*, *Czy dotrzymujemy słowa* — zaczynają się teraz od **Uwagi na odczyt**, która odcina błędny odczyt, zanim zacznie się reguła.
- **Rozdziały mają nagłówki mówiące, co w nich jest**, a nie tylko numer.
- **Nowy rozdział otwierający mówi, czym jest ten dokument, kiedy go używać, kiedy nie i jak jest zbudowany**, zanim padnie jakakolwiek zasada.
- **Zdania niosące dwie myśli zostały rozdzielone, a słowa, których nikt nie używa, wymienione.** „Strata niewspółmierna do sprawy" to teraz „strata dużo większa niż sama sprawa", w całym tekście i w obu językach.
- **`AGENT.pl.md` i `AGENT.md` mówią, czym są, zanim powiedzą, co robić.** Oba zaczynają od stwierdzenia, że standard mówi, czym MSS jest, a plik wykonawczy mówi, kiedy uruchomić go bez pytania — bo żaden nie działa bez drugiego, a czytelnik decydujący, czy je wkleić, musi to wiedzieć najpierw.
- **`DIAGRAMS`, `NAME-USAGE`, `SECURITY`, `CONTRIBUTING` i wszystkie cztery pliki w `examples/` przepisane w tym samym rejestrze.**

### Naprawione

- **Punkt 1a miał nagłówek nazywający kategorię, a nie zadanie.** Teraz brzmi *Zasady klasyfikacji decyzji* i każda z jego siedmiu reguł mówi, na które pytanie odpowiada.
- **„Nieodwracalny" był zdefiniowany jednym zdaniem niosącym cztery warunki połączone spójnikiem „albo".** Cztery warunki są teraz listą numerowaną, a uwaga, że „nieodwracalny" jest nazwą całej klasy, a nie samego warunku 1, ma dwa rozpracowane przykłady zamiast jednej wtrąconej frazy.

---

## Wersje wcześniejsze: 4.0.0 – 4.3.3

Pełne wpisy są po angielsku w [CHANGELOG.md](CHANGELOG.md). W skrócie, co się w nich wydarzyło:

**4.0.0** — przepisanie od zera. Punktacja, procenty i progi usunięte. Osiem zasad bramki dostało nazwy zamiast kodów `E1`–`E7`. Rdzeń skrócony ze 148 linii do 140.

**4.1.0** — wiersz `najbliżej zamknięcia:` uczyniony obowiązkowym przy każdym WOLNO. Naprawiona przewrotna zachęta w podziale flaga/ograniczenia: wcześniej opłacało się wpisywać wszystko do ograniczeń, bo flagi blokowały, a ograniczenia nie — czyli system karał za uczciwość.

**4.2.0** — **najważniejsza zmiana merytoryczna całej serii 4.x**: opis nieprzychylny musi napisać ktoś inny niż osoba chcąca decyzji, a zapis nazywa autora. Bez tego fakty i ocenę pisała ta sama osoba i próba niczego nie sprawdzała. Naprawiona sprzeczność w zasadzie *Czy dotrzymujemy słowa*. Dodane diagramy.

**4.3.0 – 4.3.3** — siedem decyzji terminologicznych autora: „bramka" → „bramka systemu", „najgorszy uczciwy opis" → „opis nieprzychylny" (poprzednia nazwa była oksymoronem), „droga powrotu" → „co musiałoby się zmienić", „jednokierunkowy" → „nieodwracalny (jednokierunkowy)", flaga zdefiniowana pozytywnie jako zadanie z terminem i osobą odpowiedzialną, „OGRANICZENIA" zawsze doprecyzowane. Plus usunięcie sześćdziesięciu dwóch wymyślonych metafor, które dawały się czytać na dwa sposoby. Wersje 4.3.1–4.3.3 domykały miejsca, w których reguła z 4.2.0 nie została przeprowadzona przez pliki poza rdzeniem.
