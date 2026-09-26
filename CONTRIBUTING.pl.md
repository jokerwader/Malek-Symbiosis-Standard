# Jak zgłaszać

**MSS ma jednego opiekuna.** Mateusz Małek decyduje, co mówi tekst kanoniczny, i to jest cały model zarządzania.

Dyskusja jest mile widziana i doczeka się odpowiedzi. Scalenia są rzadkie i przemyślane.

Jeśli potrzebujesz projektu, w którym dobry argument staje się commitem w przyszłym tygodniu — to nie jest ten projekt. I lepiej, żebyś wiedział o tym teraz, niż po napisaniu trzech stron.

**To jest framework dla praktyków, a nie artykuł.** Progiem zgłoszenia jest realny przypadek, a nie spór o to, co dane słowo powinno znaczyć.

- **Nie jest zgłoszeniem:** „skutek powinien się nazywać wpływ".
- **Jest zgłoszeniem:** „przepuściłem tę decyzję przez bramkę systemu, wyszło WOLNO, a oto człowiek, którego to skrzywdziło".

English: [CONTRIBUTING.md](CONTRIBUTING.md)

---

## Co jest czytane najpierw: dziura w bramce systemu

Najwyższy priorytet w tym repozytorium ma **dziura w bramce systemu** — decyzja, która przechodzi przez wszystkie osiem zasad, a nie powinna.

**Dlaczego to bije wszystko inne:** to jedyne zgłoszenie, na które framework nie może odpowiedzieć „źle go użyłeś". Rozdział 9 standardu przyznaje, że bramkę da się ograć. Dziura w bramce to ktoś pokazujący, jak dokładnie.

Otwórz zgłoszenie zatytułowane `Framework gate gap: [jedna linijka]` i użyj tego wzoru.

```
DECYZJA:  [co było decydowane, jedno zdanie]
KONTEKST: [kto był w to zaangażowany, o co szło — prawdziwe albo realistyczne]

SKUTEK: nieodwracalny | odwracalny — [powód]

OSIEM ZASAD, PO KOLEI — powiedz, dlaczego każda to przepuszcza:
  Kto odczuje:            przechodzi — [dlaczego]
  Czy mogą odmówić:       przechodzi — [dlaczego]
  Kto odpowiada:          przechodzi — [dlaczego]
  Czy to prawda:          przechodzi — [dlaczego]
  Gdzie jest haczyk:      przechodzi — [dlaczego]
  Czy powinniśmy:         przechodzi — [dlaczego]
  Czy dotrzymujemy słowa: przechodzi — [dlaczego]
  Co, gdy się powtórzy:   przechodzi — [dlaczego]

CO IDZIE ŹLE: [szkoda i nazwana strona, która ją ponosi]

DLACZEGO NIC TEGO NIE ŁAPIE: [akapit. To jest część, która ma znaczenie.
                              Nie „bramka wydaje się słaba" — która zasada
                              powinna to złapać i co jej w tym przeszkadza.]

PROPONOWANA POPRAWKA: [opcjonalnie. Jeśli proponujesz dopisanie tekstu, nazwij
                       tekst, który wyciąłbyś na jego miejsce. Zobacz regułę
                       objętości niżej.]
```

**Jeśli któraś z ośmiu jednak to łapie**, nie znalazłeś dziury w bramce — znalazłeś przypadek, w którym framework zadziałał. Przyślij mimo to, powiedz to wprost, a może trafić do `examples/`.

**Łatwy sposób, żeby takie przypadki wyprodukować:** przeprowadź test, którego standard żąda od ciebie w punkcie 8.2 — podsuń modelowi dziesięć decyzji, które nie powinny przejść. Zbuduj je z własnej roboty, a nie z przypadków skrajnych. Przez framework nigdy nie przechodzą te oczywiście złe. [USE-WITH-CLAUDE.pl.md](guides/USE-WITH-CLAUDE.pl.md) ustawia to w dwie minuty.

---

## Reszta, w kolejności

1. **Realny przypadek, w którym zawiódł zapis.** Bramka systemu wytrzymała, ale podsumowanie było tak niejasne, że osoba, która je dostała, zrobiła coś złego.
2. **Sformułowanie, które wprowadziło w błąd prawdziwego czytelnika.** Powiedz, kto to czytał, co jego zdaniem to znaczyło i co zrobił. „To jest mylące" bez czytelnika w tle jest uwagą, a uwagi nikogo nie wiążą.
3. **Tłumaczenie.** Angielski i polski są oba kanoniczne i oba muszą mówić to samo. Poprawka w jednym nie jest scalana, dopóki drugi nie nadąży.
4. **Literówki, martwe odnośniki, zepsute formatowanie.** Drobne, mile widziane, szybkie.

**Nieprzyjmowane:** spory definicyjne, prośby o przywrócenie punktacji albo procentów, prośby o zmiękczenie bramki systemu do „może" oraz dopisania, które nie mówią, co zastępują.

---

## Reguła objętości

Do wersji 4.4.0 rdzeń (wtedy README.md, dziś STANDARD.md) miał limit 140 linii treści. Ten limit zniknął i warto powiedzieć dlaczego, bo powód dotyczy tego, co go zastąpiło.

Limit liczył linie. Nie umiał odróżnić nowej zasady od zdania wyjaśniającego zasadę już istniejącą, więc kazał płacić za jedno i drugie tyle samo — a najtańszym sposobem zmieszczenia się w nim było **pisanie zasad bez wyjaśnień**. Czytelnicy czytali wtedy instrukcję i nie rozumieli powodów. Zasada, której nikt nie rozumie, jest wykonywana jak rytuał albo wcale — i żadne z tego nikogo nie chroni.

**Limitowana jest teraz liczba zasad, a nie liczba słów.**

**Dodanie zasady oznacza wycięcie zasady.** Jeśli proponujesz jedną, nazwij tę, którą zastępuje. Propozycja, która tylko dodaje, nie jest skończona i wróci do ciebie z tym jednym pytaniem.

**Wyjaśnienie nie jest dodaniem.** Wiersz `Dlaczego:`, `Przykład:` albo `Uwaga:` wskazująca, gdzie czytelnicy się mylą, może być dopisany swobodnie i nie wymaga wycięcia niczego w zamian. Jeśli zasada jest źle czytana, odpowiedzią jest więcej wyjaśnienia, a nie krótsza zasada.

**Każda zasada jest czytelnikowi winna trzy rzeczy**, a zasada, której którejś brakuje, jest niedokończona:

- samą zasadę, powiedzianą wprost,
- powód jej istnienia, wszędzie tam, gdzie ten powód nie wynika z samej zasady,
- przykład, wszędzie tam, gdzie zasadę da się przeczytać na więcej niż jeden sposób.

Dwie rzeczy, które to nadal chroni:

- Standard musi dać się wkleić w jednym bloku. To jest cały sens tego, że jest jednym dokumentem, a nie ośmioma. Długość jest w porządku; drugi plik nie.
- Czyta się to, co stoi ci przed oczami. Utrzymaj rozdziały instrukcji (1–9) wolne od eseju. Powody należą do oznaczonych wierszy, gdzie czytelnik w pośpiechu może je pominąć, a czytelnik, który utknął, może je znaleźć.

Jedna rzecz, której ten limit ciąć nie może: **cztery zasady, które nie zostały użyte ani razu i mimo to zostają**, bo są potrzebne rzadko i ratują cię wtedy, kiedy są. To zgoda nazwanego człowieka przed czynem nieodwracalnym (*Kto odpowiada*, rozdział 2), prośba o pominięcie sprawdzenia traktowana jako sygnał (rozdział 8, zasada 1), koszt cofnięcia wraz ze stroną, która go poniesie, przy **Skutkach** (rozdział 3, zasada 3 przeglądu), oraz dziesięć decyzji, które muszą nie przejść, zanim samodzielność AI wzrośnie (rozdział 8, zasada 2). Wersja 4.0.0 chroniła je akapitem wewnątrz standardu; 4.1.0 przeniosła tę ochronę tutaj, gdzie należą reguły o dokumencie. Jeśli twoja propozycja bierze miejsce od tych czterech, zostanie odrzucona, a powodem będzie ten akapit.

---

## Jak zgłaszać

Otwórz zgłoszenie. Jedno zgłoszenie na jedną sprawę. Po angielsku albo po polsku, oba w porządku.

Powiedz na wstępie, do której z powyższych kategorii się zaliczasz, a jeśli to dziura w bramce systemu — napisz to w tytule.

Spodziewaj się raczej wolnej odpowiedzi niż szybkiej. **Brak odpowiedzi nie jest odmową. To jest kolejka.**

---

## Licencja

Zgłaszając cokolwiek, zgadzasz się, żeby twój wkład był objęty licencją [CC BY-SA 4.0](LICENSE.md), tak jak reszta.
