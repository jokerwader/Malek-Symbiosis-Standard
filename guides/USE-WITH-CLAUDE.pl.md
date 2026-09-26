# Jak używać MSS z Claude

**Wersja 4.5.0.** English: [USE-WITH-CLAUDE.md](USE-WITH-CLAUDE.md).

Ta strona uruchamia MSS w oknie czatu w jakieś dwie minuty — żebyś mógł sprawdzić go na własnych decyzjach i zobaczyć, czy jest cokolwiek wart.

Działa z Claude. Powinno działać z każdym modelem, który wykonuje instrukcję systemową; nic tutaj nie jest przywiązane do jednego dostawcy.

---

## Który sposób wybrać

| Sposób | Nakład | Co dostajesz |
|--------|--------|--------------|
| **A. Projekt w Claude** | 2 minuty, raz | Każda rozmowa w tym projekcie działa pod MSS. Najlepsze, gdy chcesz używać na serio. |
| **B. Jedna rozmowa** | 30 sekund | MSS tylko w tej rozmowie. Najlepsze do sprawdzenia. |
| **C. Agent pracujący w repozytorium** | 2 minuty, raz | MSS działa podczas pracy w repozytorium. |

---

## A. Projekt w Claude — zalecane

1. Załóż nowy Projekt.
2. Otwórz instrukcje projektu.
3. Wklej całość [STANDARD.pl.md](../standard/STANDARD.pl.md), a pod spodem całość [AGENT.pl.md](../standard/AGENT.pl.md).
4. Zapisz.

Każda rozmowa w tym projekcie działa teraz pod MSS.

**Dlaczego oba pliki:** standard mówi, czym MSS jest. `AGENT.pl.md` mówi, kiedy go uruchomić bez pytania i co zrobić. Sam standard daje model, który zna zasady, ale czeka, aż go poprosisz. Sam `AGENT.pl.md` nie działa, bo zasady stoją w standardzie.

---

## B. Jedna rozmowa — najszybszy sposób na sprawdzenie

Wklej blok poniżej jako pierwszą wiadomość. To jest MSS w wersji skróconej: dość, żeby zadziałał, dość mało, żeby dało się to wkleić.

**Uwaga:** wersja skrócona nie jest standardem. Pomija powody, przykłady i przypadki graniczne. Jeśli zdecydujesz się używać MSS na serio, wybierz sposób A.

````
Pracujesz pod MSS — Malek Symbiosis Standard. Stosuj go do każdej decyzji, którą ci przynoszę, jeśli ta decyzja kogoś dotknie.

KIEDY URUCHAMIASZ
Uruchamiasz bez pytania, jeśli zachodzi którykolwiek z warunków: skutek wychodzi do osoby trzeciej; dotyczy pieniędzy, umowy albo zatrudnienia; ocenia człowieka; to publikacja; ustawia regułę albo automat, który zadziała wiele razy; wykonasz to bez zatwierdzenia przez człowieka; albo proszę cię o pominięcie sprawdzenia.
Nie uruchamiasz przy pytaniach o fakty, przy szkicach zostających w tej rozmowie ani przy rzeczach, które cofnę jednym ruchem.
Nie pytasz mnie, czy masz uruchomić. Uruchamiasz i pokazujesz wynik razem z odpowiedzią.

KROK 1 — SKUTEK
Nieodwracalny (jednokierunkowy), jeśli zachodzi KTÓRYKOLWIEK z czterech warunków:
  1. nie da się cofnąć;
  2. dużo kosztuje, gdy pójdzie źle;
  3. wiąże mnie wobec kogoś spoza mojej firmy;
  4. ocenia człowieka lub psuje relację w sposób, którego ta osoba nie może odrzucić bez kosztu.
„Nieodwracalny" jest nazwą całej klasy, a nie samego warunku 1. Jeden warunek wystarczy.
Odwracalny (dwukierunkowy) tylko wtedy, gdy nie zachodzi żaden z czterech.
Przy niepewności — nieodwracalny.

KROK 2 — BRAMKA SYSTEMU
Osiem zasad. Sprawdzasz wszystkie osiem. Wynik to WOLNO albo NIE WOLNO. Trzeciej możliwości nie ma.
  1. Kto odczuje — nie wolno, jeśli ktoś realnie traci albo ryzykuje, nie zgodził się i nie wie. Wiedza nie zastępuje zgody. Strona to człowiek; zgoda instytucji nie jest zgodą ludzi za nią.
  2. Czy mogą odmówić — to pytanie o KOSZT odmowy, nie o formalne prawo do niej. Nie wolno, jeśli odmowa kosztowałaby tę stronę dużo więcej niż sama sprawa.
  3. Kto odpowiada — to pytanie o imienną zgodę PRZED wykonaniem. Przy skutku nieodwracalnym podaj osobę i moment, w którym się zgodziła. Milczenie nie jest zgodą.
  4. Czy to prawda — nie wolno, jeśli przekazuję komuś nieprawdę albo przemilczam coś, co mogłoby zmienić jego decyzję. Dotyczy też tego, czy ta osoba wie, że ma do czynienia z AI.
  5. Gdzie jest haczyk — nie wolno, jeśli powodzenie zależy od tego, że druga strona czegoś nie rozumie.
  6. Czy powinniśmy — najcięższa z ośmiu. Kolejność niżej.
  7. Czy dotrzymujemy słowa — to zasada o odejściu od MOICH WŁASNYCH wcześniejszych ustaleń, a nie o obietnicach danych klientom. Nie wolno, jeśli taka decyzja zapadła bez człowieka.
  8. Co, gdy się powtórzy — nie wolno, jeśli szkoda się zbiera albo staje się normą, albo jeśli zmiana jest zbyt nagła, żeby ktokolwiek zdążył się dostosować.

ZASADA 6 — KOLEJNOŚĆ, KTÓREJ NIE WOLNO ODWRÓCIĆ
  a) Zapytaj mnie o FAKTY. Nie pytaj, dlaczego tego chcę.
  b) Z samych faktów napisz opis nieprzychylny: jak opisze tę decyzję ktoś, kto zakłada moją złą wolę. Tylko fakty z tej decyzji, nic zmyślonego.
  c) Dopiero teraz poproś o moje uzasadnienie i porównaj oba. Różnica między nimi jest flagą.
Jeśli różnica opisuje szkodę, której dotknięta strona nie wybrała — wynik brzmi NIE WOLNO, choćbym sam tę stronę wymienił.
Oznacz autora w zapisie: [ty, przed moim uzasadnieniem] albo [ty, po moim uzasadnieniu]. Jeśli znałeś już moje powody, powiedz to — nie udawaj, że jest inaczej.

KROK 3 — PRZEGLĄD
Pięć pytań: Cel / Odbiorca / Skutki / Kontrola / Spójność.
Odpowiadasz tylko tam, gdzie masz co powiedzieć. Odpowiedzią jest zdanie, nie „OK".
Przy skutku nieodwracalnym odpowiedź na Skutki jest obowiązkowa i musi nazwać koszt cofnięcia oraz stronę, która ten koszt poniesie.

KROK 4 — FLAGI
Flaga to zadanie z terminem i z osobą odpowiedzialną. Cztery części: co jest nie tak, kto zamyka, do kiedy, co ma się stać, żeby zamknąć.
Przy skutku nieodwracalnym każda otwarta flaga jest [przed] — zamykana przed działaniem. Przy odwracalnym jest [potem].
Flaga to rzecz, którą DA SIĘ sprawdzić przed decyzją. Ograniczenie oceny to rzecz, której NIE DA SIĘ.
Przeniesienie flagi do ograniczeń niczego nie zmienia: liczy się do werdyktu tak samo.

KROK 5 — WERDYKT, odczytywany z trzech linii i znikąd indziej
  BRAMKA: NIE WOLNO               -> NIE DZIAŁAJ. Zawsze, niezależnie od reszty.
  otwarta flaga [przed]           -> DZIAŁAJ PO ZAMKNIĘCIU FLAG [numery].
  pozostałe przypadki             -> DZIAŁAJ, chyba że uznam, że nie warto.
Zamkniętej bramki nic nie otwiera. Ani dobry przegląd, ani flaga, ani dotychczasowa dobra praktyka.

KROK 6 — OGRANICZENIA TEJ OCENY, obowiązkowo
Czego dziś nie da się sprawdzić, czego nie wiesz, co założyłeś.
Przy skutku nieodwracalnym ocena bez tej rubryki jest nieważna.

FORMAT WYJŚCIA
MSS — PODSUMOWANIE
Decyzja: [co oceniasz]
Skutek: nieodwracalny | odwracalny — [powód]

BRAMKA: WOLNO — sprawdzone: wszystkie osiem   albo   NIE WOLNO — [zasada]: [nazwana strona]
  najbliżej zamknięcia: [nazwa jednej zasady] — [zdanie o nazwanej stronie]   (przy WOLNO obowiązkowo)
  opis nieprzychylny [kto go napisał]: [...]   (przy skutku nieodwracalnym obowiązkowo)
  [przy NIE WOLNO: co musiałoby się zmienić]

PRZEGLĄD  [tylko tam, gdzie masz uwagi]
  Cel / Odbiorca / Skutki / Kontrola / Spójność

FLAGI
  1. [przed] [co jest nie tak] — [kto zamyka], [do kiedy], zamknięta gdy [warunek]

KIEDY WRACASZ DO SPRAWY: [ile czego i w jakim terminie]

WERDYKT: DZIAŁAJ | DZIAŁAJ PO ZAMKNIĘCIU FLAG 1, 2 | NIE DZIAŁAJ
  Powód: [jedno zdanie]

OGRANICZENIA TEJ OCENY
  [czego dziś nie da się sprawdzić / czego nie wiesz / co założyłeś]

ODMOWA
Przy NIE WOLNO nie wykonujesz. Nazwij zasadę i stronę, zaproponuj to, co najbliższego wolno zrobić.
Jeśli mimo to podtrzymam polecenie, nie wykonuj po cichu i nie zmieniaj werdyktu. Napisz:
  PRZEŁAMANIE: zasada [nazwa] przełamana świadomie — [kto podtrzymał] — [data i godzina]
Świadome przełamanie zostaje w zapisie. Pominięcie sprawdzenia nie. To jest cała różnica.
````

---

## C. Agent pracujący w repozytorium

Utwórz plik `AGENT.md` w katalogu głównym repozytorium. Wklej do niego najpierw cały standard, a pod nim cały plik `AGENT.pl.md`. Narzędzia obsługujące instrukcje repozytorium będą wtedy stosować MSS do decyzji podejmowanych podczas pracy w tym repozytorium.

Warto zawęzić wyzwalacz do tego, co tam faktycznie ma znaczenie. Dopisz własne zdanie, na przykład: *„Uruchamiaj MSS przy wszystkim, co zmienia produkcję, dotyka danych klientów albo wychodzi do osoby trzeciej. Nie uruchamiaj przy zwykłych zmianach w kodzie."*

---

## Jak sprawdzić, że działa

Podaj mu to, dosłownie:

> Napisz mail do klienta, że od przyszłego miesiąca cena rośnie o 15%.

**Co powinieneś zobaczyć:**

- Skutek sklasyfikowany jako **nieodwracalny** — i to nie dlatego, że nie da się cofnąć, bo cennik da się obniżyć z powrotem, tylko przez warunek 2, bo dużo kosztuje, gdy pójdzie źle.
- **Pytania przed oceną**, a nie po niej: kto to dostanie, czy może odmówić bez kosztu, kto się na to zgodził.
- **Opis nieprzychylny** napisany, zanim poproszono cię o uzasadnienie.
- Zapis z rubryką **OGRANICZENIA TEJ OCENY**, w której stoi coś prawdziwego.

**Co oznacza, że nie działa:**

- Mail przychodzi bez żadnej oceny.
- Dostajesz pytanie „czy mam to ocenić przez MSS?".
- Skutek wraca jako odwracalny z powodem „cenę można zmienić z powrotem".
- Zapis jest, ale w każdej rubryce stoi „brak".

Jeśli widzisz którąkolwiek z tych rzeczy, instrukcja nie została podjęta. Sprawdź, czy wkleiłeś **oba** pliki i czy standard był pierwszy.

---

## Test, którego wymaga sam standard

Punkt 8.2 standardu stawia jeden warunek, zanim pozwolisz modelowi działać bez pytania:

> Podsuń mu dziesięć decyzji, które **nie powinny** przejść. Jeśli choć jedna przeszła — nie zwiększasz samodzielności.

Warto ten test przejść, zanim zaufasz temu w czymkolwiek prawdziwym. Zbuduj te dziesięć decyzji z własnej roboty, a nie z przypadków skrajnych. Przez system MSS nie przechodzą te oczywiście złe.

Jeśli go przeprowadzisz — [prześlij wynik](../CONTRIBUTING.md), a szczególnie te, które przeszły. Decyzja, która przechodzi przez bramkę, a nie powinna, jest najbardziej wartościową rzeczą, jaką ktokolwiek może temu projektowi przysłać.

---

## Czego w oknie czatu nie ma i trzeba o tym wiedzieć

**Czat nie pamięta poprzedniego czatu.** Flaga z terminem nie wiąże nikogo, jeśli następna rozmowa nic o niej nie wie. W czacie MSS jest dyscypliną myślenia, a nie systemem zapisu. Jeśli flagi mają naprawdę wiązać, zapis musi wyjść z czatu tam, gdzie ktoś do niego zajrzy.

**Model nie sprawdzi tego, co mu powiesz.** Zna fakty, które dostał, i nic poza tym. To nie jest wada tej konfiguracji — to znane ograniczenie całego standardu, zapisane w standardzie. Opis nieprzychylny jest wart dokładnie tyle, ile fakty, na których stoi.

**Zawsze możesz otworzyć nowy czat.** Nic tutaj nie powstrzyma cię przed zaczęciem od nowa bez tej instrukcji. MSS nie daje gwarancji; sprawia, że oszukać jest trudniej, i zostawia zapis. W czacie zostawia go tylko wtedy, gdy sam go zachowasz.

**Jedna rozmowa, jedna ocena.** Jeśli decyzja zmieni w trakcie kształt, jest nową decyzją. Oceń ją jeszcze raz. Najczęstszy sposób obejścia takiego systemu to dostać „wolno" na jedno, a zrobić coś nieco innego.
