# MSS — diagramy

**Wersja 4.5.0.** Standard: [STANDARD.pl.md](../standard/STANDARD.pl.md) · English: [DIAGRAMS.md](DIAGRAMS.md)

Cztery diagramy procedury, którą standard opisuje słowami:

1. **Przebieg oceny** — od decyzji do zapisu.
2. **Osiem zasad** — i co sprawia, że każda z nich zamyka bramkę.
3. **Flaga czy ograniczenie** — do której rubryki coś trafia.
4. **Trzy filary** — kto co wnosi i w jakiej kolejności.

**Standard jest kanonem.** Te diagramy są pomocą w jego czytaniu. Wszędzie tam, gdzie diagram i standard się rozejdą, **wygrywa standard.**

Renderują się natywnie na GitHubie i są tekstem — więc możesz je wersjonować i poprawiać jak każdą inną linijkę standardu.

---

## 1. Przebieg oceny

Od decyzji do zapisu.

Kolejność: SKUTEK → BRAMKA SYSTEMU → PRZEGLĄD → FLAGI → KIEDY WRACASZ → WERDYKT → OGRANICZENIA TEJ OCENY.

```mermaid
flowchart TD
    D["Decyzja, którą masz zaraz wykonać"] --> SCOPE{"Czy kogoś dotknie?<br/>Nie pytanie o fakt,<br/>nie ruch, który cofniesz jednym gestem"}
    SCOPE -->|"nie, a skutek zostaje<br/>w tej rozmowie"| OUT["Nie uruchamiaj MSS.<br/>Nadgorliwość też jest błędem"]
    SCOPE -->|"nie, ale skutek wychodzi<br/>poza tę rozmowę, punkt 1c"| TIME
    SCOPE -->|"tak"| TIME{"Punkt 1b. Czy sama zwłoka<br/>jest skutkiem nieodwracalnym?"}

    TIME -->|"tak"| ACT["Działaj teraz"]
    ACT --> LATE["Potem zapisz, w ciągu doby.<br/>Zapis musi nazwać, dlaczego nie było czasu.<br/>To jedyne odstępstwo od kolejności"]
    LATE --> C1
    TIME -->|"nie"| C1

    C1{"Punkt 1. Czy zachodzi którykolwiek z czterech?<br/>1. nie da się cofnąć<br/>2. dużo kosztuje, gdy pójdzie źle<br/>3. wiąże cię wobec kogoś spoza firmy<br/>4. ocenia człowieka lub psuje relację<br/>w sposób, którego ta osoba nie odrzuci bez kosztu"}
    C1 -->|"żaden z czterech"| TWO["Skutek odwracalny (dwukierunkowy)"]
    C1 -->|"którykolwiek z nich<br/>albo masz wątpliwość"| ONE["Skutek nieodwracalny (jednokierunkowy)"]

    NOTE0["Nieodwracalny jest nazwą całej klasy,<br/>a nie samego warunku 1. Obejmuje wszystkie cztery,<br/>nie tylko techniczne cofnięcie, i jeden wystarczy.<br/>Wiążąca oferta, którą technicznie da się wycofać,<br/>jest nieodwracalna przez warunek 3"]
    C1 -.- NOTE0

    TWO --> C1C{"Punkt 1c. Którykolwiek z czterech?<br/>1. dotknie kogoś trzeciego i nie da się cofnąć<br/>2. powtórzy się bez ciebie<br/>3. wykona się bez ciebie<br/>4. ktoś prosił o pominięcie sprawdzenia"}
    C1C -->|"żaden z czterech"| SHORT["Krótki zapis jest dozwolony"]
    C1C -->|"którykolwiek z nich"| FULL["Wymagany zapis pełny"]
    ONE --> FULL

    SHORT --> GATE
    FULL --> GATE
    GATE{"Punkt 2. BRAMKA SYSTEMU.<br/>Wszystkie osiem zasad, przy każdym skutku.<br/>WOLNO albo NIE WOLNO. Trzeciej możliwości nie ma"}

    GATE -->|"NIE WOLNO"| NA["Nazwij zasadę i stronę, w którą uderza.<br/>Dopisz, co musiałoby się zmienić.<br/>Skutek nieodwracalny: opis nieprzychylny<br/>i kto go napisał"]
    NA --> STOP["WERDYKT: NIE DZIAŁAJ"]
    STOP --> DEAD["Zamkniętej bramki systemu nic nie odwraca.<br/>Ani dobry przegląd, ani to,<br/>że dotąd wszystko robiłeś dobrze"]

    GATE -->|"WOLNO"| GL["Napisz: sprawdzone wszystkie osiem.<br/>Pod spodem, zawsze: najbliższa zasada<br/>i zdanie o nazwanej stronie.<br/>Skutek nieodwracalny: opis nieprzychylny<br/>i kto go napisał"]
    GL --> REV["Punkt 3. PRZEGLĄD, pięć pytań.<br/>Skutek nieodwracalny: Skutki zawsze obowiązkowe,<br/>z kosztem cofnięcia i tym, kto go poniesie"]
    REV --> FL["Punkt 4. FLAGI. Flaga to zadanie z terminem<br/>i z osobą odpowiedzialną. Cztery części, numerowane.<br/>Rodzaj ustala skutek, a nie ty"]
    FL --> BACK["KIEDY WRACASZ DO SPRAWY:<br/>co musi się wydarzyć - ile czego i w jakim terminie.<br/>Pojedynczy krok, po co nie ma wracać: wiersz odpada"]
    BACK --> V{"Punkt 4. WERDYKT,<br/>odczytywany z trzech linii. Znikąd indziej"}

    V -->|"bramka systemu mówi NIE WOLNO - zawsze,<br/>niezależnie od reszty"| STOP
    V -->|"otwarta flaga [przed] dla tego etapu"| PAF["DZIAŁAJ PO ZAMKNIĘCIU FLAG, numery.<br/>Bez powodu: powód jest już we fladze"]
    V -->|"pozostałe przypadki"| PROC["DZIAŁAJ, z powodem"]

    STOP --> LIM
    PAF --> LIM
    PROC --> LIM
    LIM["Punkt 5. OGRANICZENIA TEJ OCENY, część obowiązkowa.<br/>Czego nie sprawdziłeś, czego nie wiesz,<br/>co założyłeś. Skutek nieodwracalny bez nich: nieważne"]

    LIM --> LCHK{"Czy cokolwiek, co tam wpisałeś,<br/>da się sprawdzić przed decyzją?"}
    LCHK -->|"tak - liczy się do werdyktu<br/>tak samo jak flaga"| V
    LCHK -->|"nie"| REC["Punkt 6. Zapisz, krótko albo pełno,<br/>jak rozstrzygnął punkt 1c. W krótkim zapisie<br/>werdykt pojawia się tylko przy NIE DZIAŁAJ"]

    NOTE1["Wolno, a mimo to nie warto, jest normalnym wynikiem.<br/>Zapisujesz to jako NIE DZIAŁAJ, z powodem,<br/>a każde NIE DZIAŁAJ niesie zdanie mówiące,<br/>co dokładnie musiałoby się zmienić"]
    V -.- NOTE1

    classDef stop fill:#7a1f1f,color:#ffffff,stroke:#c96a6a,stroke-width:1px
    classDef aside fill:none,stroke-dasharray:4 4
    class STOP,DEAD stop
    class NOTE0,NOTE1,OUT aside
```

**Diagram uwidacznia dwie reguły, które proza musi powtarzać dwa razy.**

**Nic późniejszego nie otwiera NIE WOLNO.** Żadna strzałka tam nie wraca, a reguła werdyktu wskazuje na to po raz drugi od dołu. Dobry przegląd tego nie cofnie.

**OGRANICZENIA TEJ OCENY działają odwrotnie.** Pisze się je na końcu, a mają strzałkę wracającą do werdyktu — bo wiersz o czymś, co dało się sprawdzić, a czego nie sprawdziłeś, liczy się dokładnie tak jak flaga. Ostatnia rubryka twojego własnego dokumentu potrafi zmienić werdykt trzy linijki wyżej.

---

## 2. Osiem zasad i co sprawia, że każda z nich zamyka bramkę

**Sprawdzasz wszystkie osiem, przy każdym skutku.**

Fakty po lewej nie wybierają, które zasady mają zastosowanie. One **zaostrzają wymaganie** przy zasadzie, którą i tak już sprawdzasz.

```mermaid
flowchart LR
    RULE["Każdy skutek, za każdym razem:<br/>sprawdzasz wszystkie osiem"]

    subgraph EIGHT["Osiem zasad i stała próba wewnątrz każdej"]
      direction TB
      P1["KTO ODCZUJE<br/>wypisz strony, a przy każdej:<br/>zgodziła się / wie i się nie zgadza / nie wie nic"]
      P2["CZY MOGĄ ODMÓWIĆ<br/>jedno zdanie na stronę:<br/>co się z nią stanie, jeśli powie nie"]
      P3["KTO ODPOWIADA<br/>człowiek, którego da się wskazać<br/>z imienia albo z roli"]
      P4["CZY TO PRAWDA<br/>przy każdej stronie: czy dostaje prawdę<br/>i czy wie, z kim ma do czynienia"]
      P5["GDZIE JEST HACZYK<br/>opowiedz jej całość w myślach,<br/>do samego końca"]
      P6["CZY POWINNIŚMY<br/>odejmij możemy i opłaca się, powiedz, co zostaje.<br/>Potem opis nieprzychylny"]
      P7["CZY DOTRZYMUJEMY SŁOWA<br/>porównaj z ostatnim ustaleniem<br/>powiedzianym na głos"]
      P8["CO, GDY SIĘ POWTÓRZY<br/>sto razy oraz inni robiący<br/>to samo, bo ty tak zrobiłeś"]
    end

    RULE --> EIGHT

    subgraph FIRE["Fakty, które ZAOSTRZAJĄ wymaganie"]
      direction TB
      T1["Skutek jest nieodwracalny (jednokierunkowy)"]
      T2["Szkoda jest rzeczywista"]
      T3["Odmowa kosztuje tę stronę dużo więcej<br/>niż sama sprawa"]
      T4["Podpisał kto inny niż ten,<br/>kto poniesie skutek"]
      T5["AI to napisała, zrobiła<br/>albo działa sama"]
      T6["W decyzji nie ma człowieka w ogóle"]
      T7["Odszedłeś od własnego ustalenia<br/>i nigdy tego nie powiedziałeś na głos"]
      T8["To reguła, cennik, próg<br/>albo coś automatycznego"]
      T9["Powodzenie zależy od tego, że druga strona<br/>czegoś nie rozumie"]
      T10["Zmiana jest nagła"]
    end

    T1 -->|"nazwany człowiek zgadza się przed wykonaniem,<br/>wraz z momentem. Brak jednego z dwóch<br/>zamyka bramkę systemu"| P3
    T1 -->|"opis nieprzychylny<br/>wchodzi do zapisu"| P6
    T2 -->|"każde nie wie nic<br/>zamyka bramkę systemu"| P1
    T3 -->|"zamyka bramkę systemu, choćby wszystko<br/>zostało w pełni ujawnione"| P2
    T3 -->|"zamienia każde wie i się nie zgadza<br/>w zamkniętą bramkę systemu"| P1
    T4 -->|"wypisz obu i schodź w dół do pierwszego człowieka,<br/>który niesie to bez własnej decyzji"| P1
    T5 -->|"każda strona musi wiedzieć,<br/>że ma do czynienia z AI"| P4
    T5 -->|"pilnuj nazwanego człowieka ostrzej"| P3
    T6 -->|"zamyka bramkę systemu"| P7
    T7 -->|"odejście nigdy niepowiedziane na głos<br/>i nieuzgodnione na nowo zamyka tę zasadę"| P7
    T8 -->|"oceniaj wszystkie razy, kiedy to zadziała,<br/>liczone w ludziach, których dosięgnie"| P8
    T9 -->|"zamyka bramkę systemu"| P5
    T10 -->|"nagłość liczy się wobec tego,<br/>ile czasu naprawdę było"| P8

    P5 -.->|"jeśli to działa dalej tylko dlatego,<br/>że i tak nie mają wyboru,<br/>to odpowiada ta zasada, a nie haczyk"| P2

    NOTE2["Żadna strzałka tutaj nie pozwala pominąć zasady.<br/>Strzałka dokłada wymaganie do zasady,<br/>którą i tak sprawdzasz. Osiem zasad to sprawdzenie.<br/>Fakty rozstrzygają tylko, która z nich zamyka bramkę"]
    RULE -.- NOTE2

    classDef aside fill:none,stroke-dasharray:4 4
    class NOTE2 aside
```

To odpowiada na pytanie, które ludzie faktycznie mają — **ile z tego dotyczy mojego przypadku** — a odpowiedź brzmi: wszystkie osiem dotyczy każdego przypadku.

Fakty po lewej zmieniają nie to, *które* zasady mają zastosowanie, tylko **która z nich zmienia się ze sprawdzenia w odmowę.** Każda strzałka dokłada wymaganie. Żadna go nie zdejmuje.

**Warto przeczytać uważnie trzy fakty, które sięgają po dwie zasady każdy.** Skutek nieodwracalny, odmowa kosztująca drugą stronę dużo więcej niż sama sprawa, oraz AI w robocie.

---

## 3. Flaga czy ograniczenie tej oceny

**Rozstrzyga jedno pytanie, a odpowiedź nie należy do ciebie.**

```mermaid
flowchart TD
    R["Coś w decyzji, czego nie rozstrzygnąłeś"] --> Q{"Czy ktoś inny mógłby to rozstrzygnąć<br/>przed twoją decyzją? Jeden telefon,<br/>jedno zapytanie, jedno spojrzenie w dokument"}

    Q -->|"tak, a ty tego nie zrobiłeś"| F["To jest FLAGA, punkt 4:<br/>zadanie z terminem i z osobą odpowiedzialną"]
    Q -->|"nie: cudza przyszła reakcja,<br/>stan rynku, założenie,<br/>którego dziś nikt nie zweryfikuje"| L["To jest OGRANICZENIE TEJ OCENY, punkt 5"]
    Q -->|"tak, ale wpisałeś to<br/>do OGRANICZEŃ TEJ OCENY"| ESC["Nadal liczy się do werdyktu<br/>dokładnie tak jak flaga.<br/>Wpisanie tego tam niczego nie zmienia"]
    ESC --> F

    F --> PARTS{"Czy ma wszystkie cztery części?<br/>co jest nie tak, kto zamknie,<br/>do kiedy - data albo zdarzenie,<br/>co ma się stać, żeby zamknąć"}
    PARTS -->|"którejś brakuje"| REM["To jest uwaga, a nie flaga.<br/>Uwagi nikogo nie wiążą"]
    PARTS -->|"wszystkie cztery, a warunek zamknięcia to zdarzenie,<br/>które ktoś inny stwierdzi, nie pytając ciebie"| KIND{"Jaki jest skutek?"}

    KIND -->|"nieodwracalny (jednokierunkowy)"| B1["Każda otwarta flaga jest [przed]"]
    KIND -->|"odwracalny (dwukierunkowy)"| TWQ{"Czy dotyczy etapu,<br/>który sam jest nieodwracalny?"}
    TWQ -->|"nie"| A1["[potem]"]
    TWQ -->|"tak"| B2["[przed], dla tamtego etapu"]

    B1 --> STAGE{"Czy ta flaga [przed] dotyczy etapu,<br/>o którym decydujesz teraz?"}
    B2 --> STAGE
    STAGE -->|"tak"| BLOCK["BLOKUJE.<br/>WERDYKT: DZIAŁAJ PO ZAMKNIĘCIU FLAG, numery"]
    STAGE -->|"nie, należy do późniejszego etapu"| CARRY["Nie zatrzymuje tego, co robisz teraz.<br/>Zostaje otwarta do tamtego etapu"]

    A1 --> NOBLOCK["Nie blokuje werdyktu"]
    CARRY --> NOBLOCK
    L --> LNB["Nie blokuje werdyktu.<br/>Ale przy skutku nieodwracalnym (jednokierunkowym)<br/>ocena bez tej rubryki jest nieważna"]

    classDef stop fill:#7a1f1f,color:#ffffff,stroke:#c96a6a,stroke-width:1px
    classDef aside fill:none,stroke-dasharray:4 4
    class BLOCK stop
    class REM aside
```

**W tym drzewie jest jedno prawdziwe pytanie** — da się sprawdzić przed decyzją czy nie. Wszystko po nim wynika już bez żadnego twojego osądu.

**Gałąź środkowa jest tu sednem.** Przeniesienie sprawdzalnej rzeczy do OGRANICZEŃ TEJ OCENY jej nie zmiękcza. Liczy się jak flaga niezależnie od tego, gdzie ją wpiszesz.

**Dolny wiersz jest tym, na co reagujesz:**

| Co masz | Co to robi |
|---------|-----------|
| flaga `[przed]` dla etapu, o którym decydujesz teraz | zatrzymuje werdykt |
| flaga `[przed]` dla późniejszego etapu | zostaje otwarta do tamtego etapu, teraz nic nie zatrzymuje |
| flaga `[potem]` | nigdy nie blokuje |
| prawdziwe ograniczenie tej oceny | nigdy nie blokuje |

---

## 4. Trzy filary i kto pisze opis nieprzychylny

Kto co wnosi i w jakiej kolejności.

**Kolejność jest tu mechanizmem, a nie sposobem prezentacji.**

```mermaid
flowchart TD
    subgraph WHO["Trzy filary"]
      direction LR
      H["CZŁOWIEK<br/>ma odpowiedzi:<br/>czego chcesz, co już raz nie wyszło,<br/>kto naprawdę stoi po drugiej stronie"]
      AI["AI<br/>ma pytania, których sam sobie nie zadasz,<br/>bo jesteś za blisko własnej decyzji,<br/>żeby ją podważyć"]
      E["ETYKA<br/>nie stoi po żadnej ze stron, osobno od obu:<br/>osiem zasad bramki systemu stoi po stronie ludzi,<br/>których ta decyzja dotknie"]
    end

    AUTH["KTO PISZE OPIS NIEPRZYCHYLNY<br/>ktoś, kto nie ma udziału w wyniku:<br/>dostaje fakty, nigdy nie widzi twojego uzasadnienia"]

    AI -->|"1. pytania, zadane wprost.<br/>Nie: dlaczego chcesz to zrobić"| H
    H -->|"2. odpowiedzi. Dopóki nikt nie pytał,<br/>nic nie pokazywało braku. Teraz to jest<br/>czynne kłamstwo i jest w zapisie"| FACTS["FAKTY"]
    FACTS -->|"3. fakty i nic poza nimi"| AUTH
    AUTH -->|"4. opis nieprzychylny: jak opisze to ktoś,<br/>kto zakłada twoją złą wolę,<br/>wyłącznie z faktów tej decyzji"| DESC["OPIS<br/>zapis nazywa, kto go napisał"]
    H -->|"5. dopiero teraz: uzasadnienie<br/>osoby, która chce tej decyzji"| JUST["UZASADNIENIE"]

    DESC --> GAPN
    JUST --> GAPN["6. RÓŻNICA między nimi.<br/>Różnica jest flagą"]
    GAPN --> WHOSE{"7. Kto traci w tej różnicy?"}
    WHOSE -->|"szkoda, której ta strona nie wybrała"| CLOSED["Bramka systemu jest zamknięta,<br/>choćbyś wymienił ją trzy razy z imienia"]
    WHOSE -->|"cokolwiek innego"| OPEN["Flaga, a ocena idzie dalej"]

    E --> GATEN["BRAMKA SYSTEMU<br/>osiem zasad, przy każdym skutku"]
    CLOSED --> GATEN
    OPEN --> GATEN

    LIMITN["Gdzie to się kończy:<br/>ten, kto pisze opis, zna tylko fakty,<br/>które dostał, i nic o reszcie"]
    AUTH -.- LIMITN
    LIMITN -.->|"dlatego działa razem z krokiem 1,<br/>a nie zamiast niego"| AI

    CIRCLE["Jeśli opis pisze osoba, która chce decyzji,<br/>fakty i werdykt mają tego samego autora,<br/>a próba nic nie sprawdza.<br/>Krok 3 jest tym, co temu zapobiega"]
    AUTH -.- CIRCLE

    classDef stop fill:#7a1f1f,color:#ffffff,stroke:#c96a6a,stroke-width:1px
    classDef aside fill:none,stroke-dasharray:4 4
    class CLOSED stop
    class LIMITN,CIRCLE aside
```

**Numery na strzałkach są całym tym diagramem.**

Opis powstaje z faktów w **kroku 4**, zanim twoje uzasadnienie w ogóle pojawi się w rozmowie w **kroku 5**. Krytyk, który przeczytał twoją wersję, tylko ją powtórzy.

Przy pracy z AI kroki 3 i 4 razem to jedno zapytanie — i to właśnie czyni niezależnego autora w ogóle osiągalnym.

**Dwa przerywane pola mówią, gdzie to przestaje działać.** Ten, kto pisze opis, nie wie nic ponad to, co powiedziałeś. Dlatego niosą to kroki 1 i 2: pytanie jest tym, co zamienia przemilczenie w czynne kłamstwo, na które ktoś może później wskazać.
