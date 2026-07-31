![MSS](assets/mss-logo.png)

# Malek Symbiosis Standard

**Standard Symbiozy.** Wersja 4.5.0. Autor: Mateusz Małek.

English: [README.md](README.md) · Licencja CC BY-SA 4.0

---

## Czym to jest

MSS to **zestaw pytań, które zadajesz sobie o decyzję, zanim ją wykonasz.**

Nic więcej. Nie ma tu oprogramowania, punktacji, certyfikatu ani szkolenia. Jest lista pytań i reguła, co zrobić z odpowiedziami.

Możesz je zadawać sam. Możesz je zadawać razem ze sztuczną inteligencją — i tam ten system działa najlepiej, bo AI zadaje pytania, których człowiek sam sobie nie zadaje.

**To nie jest porada prawna i nie zastępuje prawnika.**

---

## Skąd się wzięło

MSS nie powstał jako publikacja. Powstał jako **narzędzie robocze jednej osoby**, która pracowała ze sztuczną inteligencją i zauważyła u siebie ten sam problem, który zauważa większość ludzi po kilku miesiącach takiej pracy:

**AI robi to, o co ją poprosisz.** Robi to szybko, dobrze i bez zadawania niewygodnych pytań. A decyzje, które kogoś krzywdzą, rzadko wyglądają na złe w chwili podejmowania. Wyglądają na rozsądne, opłacalne i pilne.

Pierwsze wersje wyglądały zupełnie inaczej niż ta. Były punktacje, procenty, progi i wagi. Wszystko to zostało usunięte, bo robiło jedną złą rzecz: **pozwalało nadrobić w jednym miejscu to, co się straciło w innym.** Decyzja z niską oceną etyczną i wysoką oceną biznesową wychodziła na plus. To jest dokładnie ta arytmetyka, której ten system ma nie robić.

Zostało to, co zostać musiało: **osiem pytań, na które odpowiedź brzmi „wolno" albo „nie wolno", i nic pomiędzy.**

Nazwa też się zmieniła. Wcześniejsze wersje nazywały się „scoring system" — od punktacji, której już nie ma. Dzisiejsza nazwa mówi, o co naprawdę chodzi: o **symbiozę**, czyli o to, że człowiek i AI robią razem coś, czego żadne z nich nie zrobi osobno, i że obie strony odpowiadają tym samym regułom.

<!-- DO UZUPEŁNIENIA PRZEZ AUTORA: jeśli chcesz opisać osobisty kontekst powstania — konkretną sytuację, tekst albo rozmowę, od której to się zaczęło — to jest miejsce na jeden akapit. -->

Wdrożenie produkcyjne to platforma Fibid.pl, Frostbox.pl, AutoQuote.pl oraz wielu agentów biznesowych.

---

## Co jest tutaj, a czego tutaj nie ma

To, co czytasz, jest **szkieletem**: samymi zasadami i procedurą. Na tym szkielecie zbudowana jest wersja, która pracuje w naszych aplikacjach.

Tamtej wersji tutaj nie ma i nie będzie — ale nie dlatego, że jest lepsza. Dlatego, że jest **czymś innym**. To warstwa produktowa: podłączenie do konkretnych danych, konkretne role w firmie, konkretne narzędzia, szablony pracy dla agentów. Opublikowana byłaby bezużyteczna dla kogokolwiek poza nami, a przy okazji ujawniałaby rzeczy, które do nikogo poza nami nie należą.

**Szkielet nie jest wersją okrojoną.** Zasady, które tu stoją, są dokładnie tymi, które działają u nas — co do słowa. Nie ma tu wersji demonstracyjnej, uproszczonej ani osłabionej. Brakuje wyłącznie tego, co łączy te zasady z jednym konkretnym produktem.

**Dla ciebie to znaczy tyle:** bierzesz szkielet i budujesz na nim własną warstwę, tak jak my zbudowaliśmy swoją. Zasady wystarczą, żeby zacząć od razu — reszta zależy od tego, w czym pracujesz.

---

## Po co to jest

**Cel jest jeden: żeby decyzja, która kogoś skrzywdzi, nie przeszła niezauważona.**

Nie „żeby wszyscy byli etyczni". Nie „żeby AI była bezpieczna". Tak postawione cele nie dają się sprawdzić, więc nic nie znaczą.

MSS stawia cel, który da się sprawdzić: **po decyzji zostaje zapis, z którego ktoś inny odczyta, kogo ta decyzja dotknęła i czy ten ktoś miał cokolwiek do powiedzenia.**

Z tego biorą się trzy rzeczy, których ten system pilnuje:

**Nazwać człowieka, a nie grupę.** „To dotyczy rynku" nie nazywa nikogo. Dopóki nie napiszesz, kto konkretnie straci, nie widać, że ktoś stracił.

**Sprawdzić, czy ten człowiek mógł odmówić.** Nie czy formalnie miał prawo — prawie każdy ma. Tylko ile by go to kosztowało.

**Zapisać to.** Rozmowa znika do wieczora. Zapis zostaje i można go później przeczytać, także przeciwko sobie.

---

## Trzy filary

Nazwa mówi o symbiozie, a symbioza wymaga co najmniej dwóch stron. Tutaj są trzy.

### Człowiek

**Ma odpowiedzi.** Wie, czego chce, co już raz nie wyszło i kto naprawdę stoi po drugiej stronie. Tego nie wie nikt inny i żadne narzędzie tego nie odgadnie.

### AI

**Ma pytania.** Nie dlatego, że jest mądrzejsza — dlatego, że nie jest tobą. Ty jesteś za blisko własnej decyzji, żeby ją podważyć. To nie jest zarzut wobec ciebie, tylko opis tego, jak działa każdy człowiek broniący czegoś, co sam wymyślił.

### Etyka

**Nie stoi po żadnej z tych dwóch stron.** Osiem zasad, które mogą zatrzymać decyzję, stoi po stronie ludzi, których ta decyzja dotknie — a tych ludzi zwykle nie ma w rozmowie i nikt ich nie pyta o zdanie.

---

## Jak to działa

Cała procedura ma sześć kroków i mieści się w jednym zdaniu każdy.

| Krok | Pytanie |
|------|---------|
| **1. Skutek** | Czy da się to cofnąć? |
| **2. Bramka systemu** | Osiem zasad. Wolno czy nie wolno? |
| **3. Przegląd** | Pięć pytań o jakość decyzji. |
| **4. Flagi** | Co trzeba domknąć, kto i do kiedy? |
| **5. Werdykt** | Działaj, działaj po zamknięciu flag, albo nie działaj. |
| **6. Ograniczenia** | Czego nie sprawdziłeś? |

**Najpierw czy wolno. Potem czy warto. Na końcu czego nie wiem.**

Dwie rzeczy, które odróżniają to od zwykłej listy kontrolnej:

**Bramka jest bezwarunkowa.** Zamkniętej bramki do której nie masz klucza nie otwiera nic — ani dobre uzasadnienie, ani dobre intencje, ani to, że dotąd wszystko robiłeś dobrze. Nie ma tu żadnego bilansu, w którym coś dobrego równoważy coś złego.

**Ostatnia rubryka może obalić werdykt z góry strony.** Wpisujesz do własnego dokumentu, czego nie sprawdziłeś — i to potrafi zmienić decyzję zapisaną trzy akapity wyżej. Nikt tego nie robi z przyjemnością i dlatego ta rubryka jest obowiązkowa.

---

## Jak wygląda wynik

Przy decyzji odwracalnej zobaczysz tylko krótki komentarz.

Przy decyzji nieodwracalnej zapis jest dłuższy — ale **dłuższy wyłącznie dlatego, że jej skutek jest cięższy**.

Trzy pełne przykłady, z komentarzem linijka po linijce, są w [examples/](examples/).

---

## Gdzie co jest

| Plik | Dla kogo | Co zawiera |
|------|----------|------------|
| **[STANDARD.pl.md](standard/STANDARD.pl.md)** | dla wdrażających i dla AI | **Wszystkie zasady.** Pełna specyfikacja: skutek, osiem zasad, przegląd, flagi, werdykt, zapis. |
| [AGENT.pl.md](standard/AGENT.pl.md) | dla AI | Kiedy model ma uruchomić ocenę sam z siebie i o co zapytać, zanim oceni. |
| [USE-WITH-CLAUDE.pl.md](guides/USE-WITH-CLAUDE.pl.md) | dla ciebie, teraz | Jak to uruchomić w oknie czatu. Dwie minuty. |
| [examples/](examples/) | dla każdego | Trzy pełne oceny z komentarzem. |
| [DIAGRAMS.pl.md](guides/DIAGRAMS.pl.md) | dla wzrokowców | Cztery diagramy procedury. |
| [NAME-USAGE.pl.md](guides/NAME-USAGE.pl.md) | dla wdrażających | Kiedy wolno powiedzieć „zgodne z MSS". |
| [CONTRIBUTING.pl.md](CONTRIBUTING.pl.md) | dla zgłaszających | Co przysłać i jak. |
| [tests/](tests/) | dla sprawdzających | Trzydzieści scenariuszy do przepuszczenia przez model. Bez zapisanych oczekiwanych werdyktów. |

**Nie musisz czytać wszystkiego.** Jeśli chcesz tylko sprawdzić, czy to działa — idź od razu do [USE-WITH-CLAUDE.pl.md](guides/USE-WITH-CLAUDE.pl.md). Jeśli chcesz wiedzieć, co dokładnie mówią zasady — do [STANDARD.pl.md](standard/STANDARD.pl.md).

---

## Wypróbuj

Uruchomienie w oknie czatu zajmuje dwie minuty: **[Jak używać MSS z Claude](guides/USE-WITH-CLAUDE.pl.md)**.

Potem podsuń mu własną decyzję. Najlepiej taką, co do której nie jesteś pewien.

---

## Czego to nie załatwia

**Etyki nie da się zamknąć w regułach.** To zdanie nie jest skromnością, tylko ostrzeżeniem — i stoi także w samym standardzie.

Osiem zasad da się ograć sprytnym uzasadnieniem. Jeszcze łatwiej przez naciągnięcie klasyfikacji skutku albo przez samą nazwę decyzji, bo nazwa to jedno słowo i nikt jej nie sprawdza.

**MSS nie daje gwarancji. Daje tyle, że oszukać jest trudniej i że zostaje zapis.**

Jeśli znajdziesz decyzję, która przechodzi przez wszystkie osiem zasad, a nie powinna — **to jest najcenniejsza rzecz, jaką można temu projektowi przysłać.** Jak to zgłosić, mówi [CONTRIBUTING.pl.md](CONTRIBUTING.pl.md).

---

## Licencja i nazwa

**Tekst** jest na licencji [CC BY-SA 4.0](LICENSE.md): wolno kopiować, zmieniać i używać komercyjnie, pod warunkiem podania autora i zachowania tej samej licencji.

**Nazwa** to osobna sprawa. „Zgodne z MSS" wolno powiedzieć tylko przy wdrożeniu wszystkich ośmiu zasad, bez wyjątków. Wdrożenie częściowe opisuje się jako „na podstawie MSS" i mówi, czego się nie wzięło — szczegóły w [NAME-USAGE.pl.md](guides/NAME-USAGE.pl.md).

Autor: **Mateusz Małek**. Cytowanie: [CITATION.cff](CITATION.cff). Historia zmian: [CHANGELOG.pl.md](CHANGELOG.pl.md).
