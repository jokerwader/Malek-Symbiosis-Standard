# 02 — skutek nieodwracalny (jednokierunkowy), zapis pełny, jedna otwarta flaga

*Scenariusz wymyślony. Zobacz [uwagę we wstępie](README.pl.md#zanim-zaczniesz-czytać).*

English: [02-one-way.md](02-one-way.md)

---

## Sytuacja

Przewoźnik prowadzi dwanaście ciężarówek z jednej bazy regionalnej. Producent podzespołów złożył ofertę umowy na dwanaście miesięcy: cztery stałe kursy tygodniowo, jedna stawka, niezmienna przez cały okres, bez klauzuli otwierającej. Właściciel chce podpisać w tym tygodniu.

**Oferta jest dobra.** Dwie ciężarówki kupione wiosną jeszcze na siebie nie zarabiają, a cztery gwarantowane kursy tygodniowo by je pokryły. Nie ma powodu podejrzewać producenta o żadną grę — on chce stałego kosztu tak samo, jak przewoźnik chce stałej pracy.

### Ustalenie klasy skutku

Skutek jest nieodwracalny na **trzech** z czterech warunków naraz:

1. wiąże przewoźnika wobec kogoś spoza firmy (warunek 3),
2. stawki nie da się otworzyć w trakcie (warunek 1),
3. wcześniejsze wyjście kosztuje (warunek 2).

Standard mówi, że jeden warunek wystarczy. Nie ma tu krótkiego zapisu i nie ma o czym dyskutować.

---

## Zapis

```
MSS — PODSUMOWANIE
Decyzja: Podpisać dwunastomiesięczną umowę ze stałą stawką z producentem podzespołów na cztery stałe kursy tygodniowo.
Skutek: nieodwracalny — wiąże cię wobec kogoś z zewnątrz na dwanaście miesięcy, a stawki nie da się otworzyć w trakcie.

BRAMKA: WOLNO — sprawdzone: wszystkie osiem
  najbliżej zamknięcia: Co, gdy się powtórzy — jeśli zaproponujesz te same warunki wszystkim, jedna podwyżka paliwa zabierze marżę na każdej umowie, którą masz, w tym samym momencie.
  opis nieprzychylny [AI, na podstawie faktów, bez uzasadnienia właściciela]: Właściciel chce podpisać dwanaście miesięcy w tym tygodniu, bo dwie ciężarówki kupione wiosną na siebie nie zarabiają, a obietnica dana obu brygadzistom wiosną — żadnej nowej stałej trasy przed przejściem z nimi grafiku — jest wciąż niedotrzymana; podpis w tym tygodniu stawia podpis przed odpowiedzią, więc ten, kto wyląduje na szóstym dniu, zostanie o tym poinformowany, a nie zapytany, a podpisywany jest cennik, który przeczytano, i warunki ogólne, których nikt nie otworzył.

PRZEGLĄD
  Cel:       Kupujesz dwanaście miesięcy przewidywalnego obłożenia dla dwóch ciężarówek kupionych wiosną; poznasz, że się nie udało, jeśli do czwartego miesiąca to obłożenie przestanie pokrywać ich koszt miesięczny.
  Odbiorca:  Podpisuje kierownik transportu u producenta i zbuduje wokół tych czterech kursów swój tydzień produkcyjny, więc klauzula paliwowa musi stać prostymi słowami na pierwszej stronie, a nie w załączniku.
  Skutki:    Jeśli olej napędowy podrożeje dostatecznie, niesiesz stawkę, która przestaje pokrywać kurs, do końca okresu; wcześniejsze wyjście kosztuje cię opłatę za zerwanie, a ich cztery kursy tygodniowo z krótkim wyprzedzeniem, przy czym w regionie nie ma drugiego przewoźnika o takim wolumenie — ty niesiesz opłatę, oni niosą dziurę.
  Kontrola:  Właściciel podpisuje i do samego podpisu może się wycofać; po podpisie nikt w firmie nie zatrzyma tego sam.
  Spójność:  Wiosną powiedziałeś obu brygadzistom, że żadna nowa stała trasa nie wchodzi przed sprawdzeniem grafiku z nimi, a to sprawdzenie się nie odbyło.

FLAGI
  1. [przed] Obiecane brygadzistom sprawdzenie grafiku się nie odbyło, więc nie wiesz, czy cztery stałe kursy mieszczą się bez wypchnięcia kogoś na szósty dzień — zamyka właściciel, przed podpisem 3 września, zamknięta gdy obaj brygadziści przejdą grafik z wpisanymi czterema kursami i albo potwierdzą, że się mieści, albo kursy przejdą na dni, w których się mieszczą.

KIEDY WRACASZ DO SPRAWY: W trzecim i ponownie w szóstym miesiącu, a wcześniej, jeśli olej napędowy przez cztery tygodnie z rzędu utrzyma się 12 procent powyżej ceny, na której zbudowano stawkę.

WERDYKT: DZIAŁAJ PO ZAMKNIĘCIU FLAG 1

OGRANICZENIA TEJ OCENY
  Nie przeczytałeś warunków ogólnych producenta, tylko przysłany przez niego cennik.
  Nie wiesz, czy utrzymają cztery kursy tygodniowo przez swój słabszy kwartał, czy zejdą do dwóch.
  Założyłeś, że obie wiosenne ciężarówki zostaną na drodze przez pełne dwanaście miesięcy bez poważnej naprawy.
```

---

## Na co zwrócić uwagę

### Flaga jest zadaniem z terminem i z osobą odpowiedzialną

Przeczytaj ją jeszcze raz jako cztery osobne rzeczy:

| Część | Co mówi tutaj |
|-------|---------------|
| co jest nie tak | sprawdzenie grafiku się nie odbyło, więc nie wiesz, czy kursy się mieszczą |
| kto zamyka | właściciel |
| do kiedy | przed podpisem 3 września |
| co znaczy zamknięcie | obaj brygadziści przeszli grafik i albo się mieści, albo kursy się przesuwają |

Ktokolwiek może to podnieść i wykonać, nie zadając ani jednego pytania uzupełniającego.

Linijka „sprawdzić kiedyś grafik z kierowcami" byłaby uwagą — a uwagi nikogo nie wiążą.

### Flaga wyszła z bramki systemu, a nie z przeglądu

Zasada *Czy dotrzymujemy słowa* każe porównać decyzję z ostatnią rzeczą powiedzianą na głos. Coś zostało powiedziane wiosną i nie zostało dotrzymane.

**Standard jest w tej sprawie dokładny:** odejście, o którym nikomu nie powiedziano, jest flagą i **nie zamyka** bramki systemu. Gdyby decyzja zapadła zupełnie bez człowieka, bramka by się zamknęła.

Ten sam fakt pojawia się potem jeszcze raz przy Spójności w przeglądzie — bo tam jest widoczny dla kogoś, kto będzie ten zapis czytał później.

### `najbliżej zamknięcia:` nazywa jedną zasadę, jedno zdanie i jedną stronę, i jest obowiązkowe

Bramka jest otwarta, a niewiele brakowało.

*Co, gdy się powtórzy* pyta, co się stanie, jeśli zrobisz tak sto razy i jeśli inni cię skopiują. Jedna umowa ze stałą stawką jest w porządku. Zaproponuj te same warunki wszystkim, a każda umowa posypie się tego samego dnia.

To należy do zapisu i **nie zmienia werdyktu.**

**Dlaczego ten wiersz stoi przy każdym WOLNO, a nie tylko tam, gdzie coś było blisko:** najbliższej zasady nie da się wskazać, nie uszeregowawszy wszystkich ośmiu. Ten wiersz jest jedynym dowodem w zapisie, że szeregowanie się odbyło.

### Opis nieprzychylny jest w zapisie i nie napisał go właściciel

Przy skutku nieodwracalnym ten wiersz jest obowiązkowy — tak samo jak wiersz Skutki i OGRANICZENIA TEJ OCENY.

**Dwie rzeczy sprawiają, że tutaj on działa.**

**Trzyma się faktów, które już są w tym zapisie, i nie dodaje żadnego** — dwie wiosenne ciężarówki, obietnica dana brygadzistom, przeczytany cennik i nieotwarte warunki ogólne.

**Nie napisała go osoba, która chce tej decyzji.** Właściciel przekazał fakty i poprosił o opis, nie pokazując uzasadnienia — więc to, co wróciło, nie jest jego własną wyobraźnią.

Postaw to obok Celu i różnica jest widoczna: w jednym dwanaście miesięcy obłożenia dla dwóch ciężarówek, w drugim podpis z datą przed odpowiedzią i szósty dzień, który nie jest dniem właściciela.

Standard mówi, że ta różnica jest flagą — tutaj trafia w ten sam fakt, który flaga 1 już trzyma otwarty, więc nie ma czego otwierać dodatkowo.

### *Czy mogą odmówić* zostało sprawdzone i nie zamyka bramki — i warto to powiedzieć na głos

Druga zasada zamyka bramkę systemu tam, gdzie druga strona nie może powiedzieć „nie" bez straty dużo większej niż sama sprawa.

Tutaj zdanie napisane dla producenta brzmiało: *„wracają do dwóch przewoźników, którzy startowali przeciwko nam, po gorszej stawce, ale nie gorszej niż dzisiaj"* — realny koszt, ale nie taki, który jest dużo większy niż sama sprawa.

**Dwie firmy porównywalnej wielkości negocjujące stawkę to dokładnie ten przypadek, który ta zasada ma zostawić w spokoju.** Zamyka bramkę tam, gdzie strona, która miałaby odmówić, nie ma dokąd pójść — a fakt, że wszystko zostało ujawnione, na to pytanie nie odpowiada.

### Wiersz Skutki jest wypełniony, bo musi być

Przy skutku nieodwracalnym to jedyne pytanie przeglądu, którego nie wolno pominąć, i musi nazwać koszt cofnięcia **oraz** stronę, która ten koszt poniesie.

Ten nazywa obie strony: opłata za zerwanie jest twoja, dziura po czterech kursach z krótkim wyprzedzeniem jest ich.

*„Wyjście byłoby drogie"* nie spełniłoby reguły — drogie dla kogo.

### Nie ma wiersza `Powód:` pod werdyktem

Przy DZIAŁAJ PO ZAMKNIĘCIU FLAG wiersz powodu odpada, bo powód siedzi już we fladze. Powtórzenie go dałoby tylko dwa miejsca do utrzymywania w zgodzie.

### DZIAŁAJ PO ZAMKNIĘCIU FLAG nie jest miękkim „nie"

To nie jest „raczej tak" ani „na razie nie".

Mówi: **to idzie dalej, a flaga 1 jest tym, co stoi między tu a tam.**

Napisanie „NIE DZIAŁAJ, dopóki grafik nie zostanie sprawdzony" byłoby błędem — i każdy, kto przeleci to wzrokiem, odczyta jako odrzucenie.

### *Kiedy wracasz do sprawy* nie jest flagą

Ma własny wiersz, bo jest obietnicą na przyszłość, a nie warunkiem na teraz.

Mówi, ile czego i w jakim terminie — po to, żeby w piątym miesiącu nikt nie musiał ustalać, czy warunek został spełniony.

### Ograniczenia tej oceny to trzy proste przyznania

Nieprzeczytane, niewiadome, założone.

Przy skutku nieodwracalnym ocena z pustymi OGRANICZENIAMI TEJ OCENY jest nieważna — albo je wypełniasz, albo zaczynasz od nowa.

**Trzeci wiersz jest tym uczciwym:** cały układ stoi na tym, że dwie ciężarówki zostaną na drodze, a nikt tego założenia nie sprawdził, bo nie ma jak.
