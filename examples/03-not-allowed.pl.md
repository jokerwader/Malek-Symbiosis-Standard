# 03 — zamknięta bramka systemu

*Scenariusz wymyślony. Zobacz [uwagę we wstępie](README.pl.md#zanim-zaczniesz-czytać).*

English: [03-not-allowed.md](03-not-allowed.md)

---

**To jest przykład, dla którego cały ten framework istnieje.**

Wszystko w poniższej decyzji jest atrakcyjne. Przychód jest realny, prawnicy dali zielone światło, kontrola jest czysta, a przegląd najmocniejszy z trzech przykładów.

Bramka systemu jest zamknięta, więc nic z tego się nie liczy.

---

## Sytuacja

Aplikacja do obróbki zdjęć ma wersję darmową i płatną. Wzrost wyhamował, rachunek za serwery nie, a wersja płatna go nie pokrywa.

**Propozycja na stole:** włączyć płatny dodatek o nazwie Auto-Cleanup domyślnie na wszystkich istniejących darmowych kontach, jako czternastodniową próbę. Po czternastu dniach konto zaczyna być obciążane miesięcznie, chyba że użytkownik dodatek wyłączy. Powiadomienie idzie przez aktualizację regulaminu w aplikacji i jeden baner, który da się zamknąć.

**Dwie rzeczy są prawdziwe i warto je powiedzieć wprost:**

- Dział prawny potwierdził, że okres wypowiedzenia i zmiana regulaminu są zgodne z prawem na każdym rynku, na którym aplikacja działa. **To nie jest propozycja złamania prawa.**
- Finanse wyliczyły z tego znaczącą część przychodu następnego kwartału. **To nie jest złe uzasadnienie biznesowe.**

### Ustalenie klasy skutku

Skutek jest nieodwracalny z trzech osobnych powodów:

1. pieniądze schodzą z kart ludzi,
2. zmiana odpala się na każdym darmowym koncie bez zatwierdzania każdego z osobna,
3. zwrot nie cofa tego, że ktoś został obciążony bez własnej woli.

Punkty 1c i 8 standardu nie zostawiają tu miejsca: zapis pełny, bez wersji krótkiej i bez wersji, w której sprawdzenie się pomija, bo kwartał jest napięty.

---

## Zapis

```
MSS — PODSUMOWANIE
Decyzja: Włączyć dodatek Auto-Cleanup domyślnie na wszystkich istniejących darmowych kontach, jako czternastodniową próbę, która zaczyna naliczać opłatę, jeśli konto jej nie wyłączy.
Skutek: nieodwracalny — zabiera pieniądze ludziom spoza firmy i odpala się na każdym darmowym koncie bez ciebie.

BRAMKA: NIE WOLNO — Gdzie jest haczyk: dotychczasowi użytkownicy wersji darmowej
  opis nieprzychylny [AI, na podstawie faktów, bez uzasadnienia zespołu]: Rachunek za serwery płacą ci, którzy najpewniej tego nie zauważą — konta, które otworzyły aplikację raz do jednej poprawki i nie wróciły w tym roku, dostają dodatek, o który nikt nie prosił, jeden baner do zamknięcia i obciążenie czternaście dni później; wyliczona przez finanse część przychodu następnego kwartału jest prognozą tego, ilu nie przeczyta powiadomienia, prawników zapytano, czy powiadomienie jest zgodne z prawem, a nie czy ktokolwiek by się na to zgodził, a pierwszy tydzień na pięciu procentach pokazuje, ilu się poskarży, zanim reszta zostanie włączona.
  Prognoza trzyma się tylko wtedy, gdy większość z nich nie przeczyta powiadomienia. Nic, co wpiszesz w baner, tego nie zmieni, bo baner nie jest tym, co jest nie tak. Zmienić trzeba działanie: wypuścić dodatek wyłączony i obciążać tylko te konta, które go włączą.

PRZEGLĄD
  Cel:       Chcesz, żeby dodatek udźwignął rachunek za serwery przez cztery kwartały; poznasz, że się nie udało, jeśli w trzecim miesiącu płaci dalej mniej niż jedna piąta przekonwertowanych kont.
  Odbiorca:  Każde istniejące darmowe konto, a większość tych ludzi otworzyła aplikację raz do jednej poprawki i nie wróciła w tym roku — czyli ten sam fakt, który sprawia, że prognoza działa, sprawia też, że powiadomienie nie dociera.
  Skutki:    Obciążenia lądują na prawdziwych kartach; każde możesz zwrócić, ale zwrot nie cofa tego, że ktoś został obciążony bez własnej woli — ci ludzie niosą zaskoczenie i czas stracony na odzyskiwanie pieniędzy, ty niesiesz zwroty, opłaty za chargeback i ocenę w sklepie.
  Kontrola:  Szef produktu może to wyłączyć jednym wydaniem, a wdrożenie jest etapowane na pięciu procentach przez pierwszy tydzień.

WERDYKT: NIE DZIAŁAJ
  Powód: Przychód pojawia się tylko wtedy, gdy ludzie, którzy go płacą, tego nie zauważą, a żadne lepsze sformułowanie tego nie naprawi — zmienić trzeba działanie: wypuścić dodatek domyślnie wyłączony i obciążać tylko te konta, które go włączą.

OGRANICZENIA TEJ OCENY
  Nie sprawdziłeś, jaka część darmowych kont ma w ogóle podpiętą kartę, więc nie wiesz, ilu faktycznie zostałoby obciążonych.
  Nie wiesz, czy wersja włączana ręcznie pokryje rachunek za serwery w ogóle, a to jest liczba, od której to teraz zależy.
  Założyłeś, że odczyt prawny jest prawidłowy na każdym rynku, na którym działacie; przyjąłeś go i nie sprawdziłeś.
```

---

## Odmowa, wypisana

Jeśli ktoś z zespołu — albo AI pracująca z nim — dostanie polecenie zbudowania tego i tego nie zrobi, standard daje słowa. **Odmowa bez nazwanej zasady i nazwanej strony nie jest odmową, tylko widzimisię.**

```
Nie napiszę tekstów wdrożeniowych do włączenia Auto-Cleanup domyślnie, bo narusza to zasadę Gdzie jest haczyk: dotychczasowi użytkownicy wersji darmowej.
Zamiast tego mogę napisać wersję włączaną ręcznie — ten sam dodatek, wypuszczony wyłączony, z jednym ekranem mówiącym, ile kosztuje i co robi.
Jeśli widzisz to inaczej — powiedz, która zasada twoim zdaniem tu nie działa.
```

Standard każe potem obrócić ten sam test przeciwko własnej odmowie.

**Opis nieprzychylny tej odmowy:** *to nie ty musisz dowieźć wynik kwartału, więc powiedzenie „nie" nic cię nie kosztuje.*

To jest uczciwe i **nie jest odpowiedzią na zarzut.** Zarzut nie brzmi, że liczba jest wysoka. Zarzut brzmi, że **ta liczba zależy od tego, że ludzie nie czytają.** Jeśli wersja włączana ręcznie dowiezie tę liczbę, nie ma tu już czego odmawiać.

---

## Na co zwrócić uwagę

### Przegląd jest dobry i nic nie zmienia

Przeczytaj cztery wiersze przeglądu osobno, a wygląda to na dobrze poprowadzoną decyzję: cel konkretny, sygnał porażki to liczba z datą, kontrola czysta, wdrożenie etapowane.

Standard mówi bez ogródek, ile to jest warte wobec zamkniętej bramki: **zamkniętej bramki systemu nic nie odwraca** — ani dobry przegląd, ani to, że dotąd wszystko robiłeś dobrze.

**Przegląd jest w zapisie celowo,** żebyś zobaczył, jak nie ratuje decyzji.

### Legalne i etyczne to nie to samo sprawdzenie, a bramka jest tym drugim

Nikt w tym scenariuszu nie proponuje niczego bezprawnego. **Bramka systemu nie pyta, czy prawo ci pozwala.**

*Gdzie jest haczyk* zadaje jedno pytanie: czy to działa tylko dlatego, że druga strona czegoś nie rozumie?

Powiedz każdemu użytkownikowi wersji darmowej całość do końca — *za czternaście dni zaczniemy obciążać twoją kartę, chyba że tu klikniesz* — a prognoza się sypie.

**To jest test, który wypada negatywnie — i wypada na własnych liczbach tego planu**, a nie na czyimkolwiek podejrzeniu wobec kogokolwiek.

### Jedna zamknięta zasada wystarczy, więc nazywa się tylko jedną

*Kto odczuje* też zamknęłoby tę bramkę: ludzie, którzy nigdy się nie zgodzili i nie wiedzą, są tymi, którzy tracą pieniądze.

Nie ma potrzeby ich piętrzyć. Zapis nazywa zasadę, która zamknęła bramkę, i stronę, w którą uderza, i na tym kończy.

**Dokładanie kolejnych nazw nie czyni odmowy bardziej ostateczną.** Ona już jest ostateczna.

### Opis nieprzychylny jest w zapisie i nie napisał go zespół

Szablon oznacza każdy wiersz pod bramką warunkiem, na którym ten wiersz wisi:

| Wiersz | Warunek, na którym wisi |
|--------|------------------------|
| `najbliżej zamknięcia:` | werdykt — WOLNO |
| co musiałoby się zmienić | werdykt — NIE WOLNO |
| opis nieprzychylny | klasa skutku — nieodwracalny, **niezależnie od tego, jak wypadł werdykt** |

Dlatego ten zapis go zawiera, a 01 nie — powodem jest klasa skutku, a nie odmowa.

**Działa tutaj tak samo, jak w 02.** Trzyma się faktów, które już są w tym zapisie, i nie dodaje żadnego: rachunek za serwery, konta, które otworzyły aplikację raz i nie wróciły, baner i czternaście dni, wyliczona przez finanse część przychodu, pięć procent w pierwszym tygodniu. I nie napisali go ludzie, którzy chcą tej decyzji.

**Jedna rzecz, którą robi, ujawnia się dopiero przy odmowie.** Wiersz bramki nazywa *Gdzie jest haczyk* i kończy, bo jedna zamknięta zasada wystarczy. Bez tego wiersza nic w zapisie nie pokazywałoby, że zasada *Czy powinniśmy* — najcięższa z ośmiu do przeprowadzenia — została w ogóle przeprowadzona.

### Brak flag

Nie ma czego trzymać otwartego. **Flaga jest warunkiem nałożonym na coś, co idzie dalej, a to nie idzie dalej.**

Dopisanie „flaga 1: poprawić treść powiadomienia" byłoby próbą przerobienia zamkniętej bramki systemu na listę zadań — czyli dokładnie tym ruchem, przed którym bramka istnieje.

Sekcja FLAGI nie jest wypisana, tak samo jak KIEDY WRACASZ DO SPRAWY — bo nie ma do czego wracać, dopóki samo działanie nie będzie inne.

### Zmienić trzeba działanie, a nie słowa

Standard przewiduje ten przypadek: czasem żadne przepisanie nie pomoże, bo zmienić trzeba to, co się robi.

Więc wiersz powodu nie mówi „napisać jaśniejsze powiadomienie". Mówi: wypuścić to domyślnie wyłączone.

**To jest mniejszy biznes — i jest to biznes, który wytrzymuje wyjaśnienie.**

### Ograniczenia tej oceny niosą teraz następną robotę

Drugi wiersz jest tym, który teraz ma znaczenie: **nikt nie policzył, czy wersja włączana ręcznie pokryje rachunek.**

Decyzja o zatrzymaniu zapadła bez tej liczby, a zapis mówi to na głos, zamiast sugerować, że wersja zatrzymana była oczywiście w porządku.

Ten wiersz jest następną robotą do wykonania.
