![MSS](assets/mss-logo.png)

# Malek Symbiosis Standard

**Standard sprawdzania decyzji, zanim wpłyną na innych ludzi.** Wersja 4.5.0. Autor: Mateusz Małek.

English: [README.md](README.md) · Licencja: [CC BY-SA 4.0](LICENSE.md)

---

## Czym jest MSS

MSS to zestaw pytań, które zadajesz przed podjęciem decyzji mogącej wpłynąć na inną osobę.

Możesz korzystać z MSS samodzielnie albo razem z AI. Współpraca z AI jest szczególnie przydatna, ponieważ model może zadać pytania, o których nie pomyślisz przy ocenie własnej decyzji.

MSS nie jest programem, punktacją, certyfikatem ani szkoleniem. To zapisana procedura. Nie zastępuje porady prawnej.

---

## Skąd się wzięło

Najpierw napisaliśmy MSS jako narzędzie pracy jednej osoby korzystającej z AI. Zauważyliśmy częsty problem:

**AI zwykle robi to, o co je prosisz.** Działa szybko i rzadko zadaje niewygodne pytania, jeśli mu tego nie polecisz. Decyzja szkodliwa dla innych może więc wyglądać rozsądnie, opłacalnie i pilnie, kiedy nikt jej nie podważa.

Pierwsze wersje używały punktów, procentów, progów i wag. Usunęliśmy je. Wysoki wynik biznesowy mógł równoważyć niski wynik etyczny i sprawiać, że szkodliwa decyzja wyglądała na dopuszczalną.

MSS używa teraz ośmiu pytań. Każde z nich może zatrzymać decyzję. Dobry wynik w jednym miejscu nie usuwa problemu wykrytego w innym.

Nazwa odnosi się do **symbiozy**. Ty dostarczasz fakty i bierzesz odpowiedzialność. AI zadaje pytania i pokazuje inny punkt widzenia. Obie strony stosują te same zasady.

MSS działa produkcyjnie na platformach Fibid.pl, Frostbox.pl i AutoQuote.pl oraz w kilku agentach biznesowych.

---

## Do czego służy MSS

Cel jest prosty: **nie pozwolić, aby decyzja krzywdząca człowieka przeszła niezauważona.**

MSS wymaga trzech rzeczy:

1. **Nazwij osoby, których dotyczy decyzja.** Nie ukrywaj ich pod określeniami takimi jak „rynek” albo „użytkownicy”.
2. **Sprawdź, czy mogą odmówić.** Formalne prawo do odmowy nie wystarcza, jeśli odmowa kosztowałaby znacznie więcej niż zgoda.
3. **Zostaw zapis.** Inna osoba powinna móc sprawdzić, kogo dotyczyła decyzja, co sprawdzono i czego nadal nie wiadomo.

MSS nie gwarantuje etycznej decyzji. Pomaga zauważyć brakujące fakty i pominięte osoby.

---

## Jak działa MSS

| Krok | O co pytasz |
|---|---|
| **1. Skutek** | Czy można bezpiecznie cofnąć wynik decyzji? |
| **2. Bramka systemu** | Czy wszystkie osiem wymaganych zasad pozwala podjąć decyzję? |
| **3. Przegląd** | Czy decyzja jest przydatna, jasna, kontrolowana i spójna? |
| **4. Flagi** | Co trzeba sprawdzić, kto to zrobi i do kiedy? |
| **5. Werdykt** | Działać, poczekać na zamknięcie flag czy nie działać? |
| **6. Ograniczenia** | Czego nie można było sprawdzić przed decyzją? |

Kolejność ma znaczenie. Najpierw sprawdzasz, czy wolno podjąć decyzję. Potem oceniasz, czy warto ją podjąć. Na końcu zapisujesz, czego nadal nie wiesz.

Przy decyzji odwracalnej zapis może być krótki. Decyzja nieodwracalna wymaga pełnego zapisu.

---

## Od czego zacząć

Nie musisz czytać wszystkich plików.

- Aby wypróbować MSS w rozmowie, otwórz [Jak używać MSS z Claude](guides/USE-WITH-CLAUDE.pl.md).
- Aby przeczytać wszystkie zasady, otwórz [STANDARD.pl.md](standard/STANDARD.pl.md).
- Aby powiedzieć modelowi, kiedy ma rozpocząć ocenę, użyj [MODEL-INSTRUCTION.pl.md](standard/MODEL-INSTRUCTION.pl.md) razem ze standardem.
- Aby zobaczyć pełne przykłady, otwórz [examples/](examples/).
- Aby sprawdzić, czy różne modele rozumieją MSS tak samo, otwórz [tests/](tests/).

Pozostałe przydatne pliki:

- [DIAGRAMS.pl.md](guides/DIAGRAMS.pl.md) — cztery diagramy procedury;
- [NAME-USAGE.pl.md](guides/NAME-USAGE.pl.md) — kiedy wolno powiedzieć „zgodne z MSS”;
- [CONTRIBUTING.pl.md](CONTRIBUTING.pl.md) — jak zgłosić problem albo zaproponować zmianę;
- [CHANGELOG.pl.md](CHANGELOG.pl.md) — co zmieniło się między wersjami.

---

## Co publikujemy

To repozytorium zawiera pełne zasady i pełną procedurę MSS. Nie jest to wersja demonstracyjna ani skrócona.

Nasze aplikacje dodają własne dane, role, narzędzia i sposoby pracy. Nie publikujemy tej warstwy, ponieważ ma sens tylko wewnątrz tych aplikacji. Możesz zbudować własną warstwę wokół tych samych opublikowanych zasad.

---

## Licencja i nazwa

Możesz kopiować, zmieniać i wykorzystywać tekst komercyjnie na warunkach [CC BY-SA 4.0](LICENSE.md). Musisz podać autora i zachować tę samą licencję.

Określenia **„zgodne z MSS”** używaj tylko wtedy, gdy wdrożysz wszystkie osiem zasad bramki systemu bez wyjątków. Jeśli używasz tylko części MSS, napisz **„na podstawie MSS”** i wymień pominięte elementy. Szczegóły znajdziesz w [NAME-USAGE.pl.md](guides/NAME-USAGE.pl.md).

Autor: **Mateusz Małek** · Cytowanie: [CITATION.cff](CITATION.cff)
