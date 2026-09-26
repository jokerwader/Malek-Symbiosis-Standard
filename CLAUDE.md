# CLAUDE.md — praca w tym repozytorium

Ten plik jest instrukcją dla Claude Code pracującego w repozytorium Malek Symbiosis Standard. Czytasz go na początku każdej sesji.

**This file is in Polish because Polish is the source language of this project.** Every rule below applies to work in both languages.

---

## Czym jest to repozytorium

To jest **specyfikacja, a nie oprogramowanie.** Nie ma tu kodu do uruchomienia, testów jednostkowych ani zależności. Są dokumenty w markdown, w dwóch językach, opisujące zestaw zasad oceny decyzji.

Skutkiem tego jest jedna rzecz, o której trzeba pamiętać przy każdej zmianie: **tekst jest tu produktem.** Zmiana słowa nie jest kosmetyką. Zmiana słowa w tym repozytorium zmienia to, co ludzie robią z decyzjami, które kogoś dotkną.

---

## TRZY REGUŁY TWARDE

Te trzy łamie się tylko wtedy, gdy autor powie to wprost w bieżącej rozmowie.

### 1. Nie zmieniasz treści zasad

**Wolno ci** usuwać niezgodność z regułą, która **już stoi** w `STANDARD.pl.md` albo `STANDARD.md`. To jest naprawa: doprowadzasz plik do zgodności z tekstem kanonicznym.

**Nie wolno ci** rozstrzygać, jak reguła ma brzmieć. To należy do autora.

Jeśli w trakcie pracy natrafisz na coś, co wymaga rozstrzygnięcia treści reguły — **zatrzymaj się i zgłoś w raporcie.** Lepiej zgłosić za dużo niż zdecydować za autora.

**Test, który to rozstrzyga:** czy potrafisz wskazać zdanie w standardzie, do którego doprowadzasz plik? Jeśli tak — to naprawa. Jeśli musisz napisać nowe zdanie w standardzie — to decyzja autora.

**Uwaga, tu się już raz pomyliliśmy.** Polecenie „rozwiąż to bezpiecznie" brzmi jak ostrożność, a bywa rozstrzygnięciem. Dopisanie obowiązkowego wiersza do przykładu odpowiada twierdząco na pytanie, czy ten wiersz jest obowiązkowy.

### 2. Każda zmiana idzie w obu językach

Polski i angielski są **oba kanoniczne** i oba muszą mówić to samo. Poprawka w jednym nie jest skończona, dopóki drugi nie nadąży.

**Polski jest językiem źródłowym.** Jeśli autor zmienił coś po polsku, przenieś to na angielski — nie odwrotnie.

**Uwaga na defekt symetryczny.** Dwa pliki mogą zgadzać się ze sobą co do znaku i oba łamać regułę trzeciego. Porównanie PL/EN takiego defektu nie wykryje. Sprawdzaj zgodność **ze standardem**, nie tylko wzajemną.

### 3. Nie publikujesz

**Żadnego `git push`, żadnego tworzenia repozytorium zdalnego, żadnej zmiany widoczności na publiczną bez wyraźnej zgody autora w bieżącej rozmowie.**

Commit lokalny jest w porządku, jeśli o niego poproszono. Wypchnięcie — nie.

**Nie kasujesz bezpowrotnie.** Plik, który ma zniknąć, przenosisz poza to repozytorium — do katalogu roboczego autora — a nie usuwasz. Autor powie gdzie.

---

## Mapa repozytorium

```
/                        pliki, których GitHub szuka w katalogu głównym
  README.md / .pl.md     wizytówka — czym to jest, skąd się wzięło, po co. NIE ZAWIERA ZASAD
  LICENSE.md             CC BY-SA 4.0, tekst prawny. Tylko angielski, świadomie. Nie tłumacz
  CITATION.cff           metadane cytowania
  CONTRIBUTING.* SECURITY.* CHANGELOG.*    pliki procesowe, oba języki
  CLAUDE.md              ten plik
  .gitattributes         normalizacja końców linii — bez tego pliki puchną przy pierwszym zapisie na innym systemie

standard/                TEKST KANONICZNY
  STANDARD.md / .pl.md   wszystkie zasady. Wobec tego mierzy się zgodność wszystkiego innego
  AGENT.md / .pl.md      warstwa wykonawcza: kiedy uruchomić ocenę bez pytania, o co zapytać, jak zapisać

guides/
  USE-WITH-CLAUDE.*      jak uruchomić. Zawiera SKRÓCONĄ KOPIĘ STANDARDU — patrz ostrzeżenie niżej
  NAME-USAGE.*           kiedy wolno powiedzieć „zgodne z MSS"
  DIAGRAMS.*             cztery diagramy mermaid

examples/                trzy pełne oceny z komentarzem, oba języki. Scenariusze wymyślone
tests/                   dziesięć person, trzydzieści scenariuszy, warianty, karta wyników
assets/                  mss-logo.png
.github/                 szablony zgłoszeń i pull requestów
```

**`STANDARD` i `AGENT` leżą razem, bo wkleja się je razem.** Rozdzielenie ich do dwóch katalogów byłoby porządkiem kosztem tego, jak się ich używa.

**W `tests/` nie ma zapisanych oczekiwanych werdyktów.** To jest konstrukcja, nie przeoczenie — powód stoi w `tests/README.pl.md`. Nie dopisuj ich.

### Ostrzeżenie o duplikacie

`USE-WITH-CLAUDE` zawiera **skrócony blok standardu do wklejenia**. To jest kopia reguł innymi słowami.

**Przy każdej zmianie reguły sprawdź, czy ten blok też jej nie potrzebuje.** To jest jedyne miejsce w repozytorium, w którym ta sama reguła stoi dwa razy, i jedyne, które da się po cichu rozjechać ze standardem.

---

## MSS obowiązuje w tym repozytorium

Repozytorium opisujące zasady oceny decyzji, w którym decyzje podejmuje się bez tych zasad, jest bezwartościowe.

**Uruchamiasz MSS** przy decyzjach dotyczących:

- **treści zasad** — dodanie, usunięcie albo zmiana znaczenia czegokolwiek w `STANDARD.*`;
- **publikacji** — cokolwiek, co wychodzi poza to repozytorium;
- **przykładów** — bo są publikowane i ludzie się z nich uczą;
- **nazwy i licencji** — bo wiążą wobec ludzi z zewnątrz.

**Nie uruchamiasz** przy literówkach, martwych odnośnikach, formatowaniu ani przy czytaniu plików.

Pełna procedura jest w `STANDARD.pl.md`. Skrótowo: skutek → bramka systemu → przegląd → flagi → werdykt → ograniczenia oceny.

**Zapis dołączasz do raportu z pracy, nie do plików repozytorium.** Realne oceny robocze nigdy nie trafiają do `examples/` — tam idą wyłącznie scenariusze wymyślone.

---

## Sprawdzenia przed zakończeniem pracy

Wykonaj **wszystkie**, jeśli ruszałeś cokolwiek poza literówką.

### Odnośniki, emotikony, parzystość

```bash
python -c "
import glob,os,re
files=sorted(glob.glob('**/*.md',recursive=True))+sorted(glob.glob('*.cff'))
bad=tot=0
for f in files:
    d=os.path.dirname(f)
    for m in re.finditer(r'\]\(([^)]+)\)',open(f,encoding='utf-8').read()):
        t=m.group(1)
        if t.startswith(('http','#','mailto')): continue
        tot+=1; p=t.split('#')[0]
        if p and not os.path.exists(os.path.normpath(os.path.join(d,p))):
            bad+=1; print('MARTWY:',f,'->',t)
print('odnosniki:',tot,' martwe:',bad)
print('emotikony:',sum(1 for f in files for l in open(f,encoding='utf-8') for ch in l if ord(ch)>0x2500))
BEZ_PL={'LICENSE.md','CLAUDE.md','.github/PULL_REQUEST_TEMPLATE.md'}
PARY={'tests/PERSONAS.md':'tests/PERSONY.pl.md',
      'tests/SCENARIOS.md':'tests/SCENARIUSZE.pl.md',
      'tests/SCORESHEET.md':'tests/KARTA-WYNIKOW.md'}
for f in files:
    if f.endswith('.cff') or '.pl.' in f: continue
    n=f.replace(os.sep,'/')
    if n in BEZ_PL or n in PARY.values(): continue
    p=PARY.get(n, f.replace('.md','.pl.md'))
    if not os.path.exists(p): print('BRAK PL:',n)
"
```

Oczekiwane: **martwe 0, emotikony 0, zero wierszy BRAK PL.**

Wyjątki na liście `BEZ_PL` są świadome. `LICENSE.md` to tekst prawny CC BY-SA i tłumaczenie kanonicznej licencji tworzy ryzyko, nie wygodę. `CLAUDE.md` i szablon pull requesta są plikami roboczymi, nie częścią standardu. **Nie dopisuj do tej listy niczego bez zgody autora** — to jest furtka, przez którą parzystość PL/EN cicho przestaje obowiązywać.

Lista `PARY` obsługuje trzy pliki w `tests/`, których polskie wersje mają inne nazwy niż angielskie. Nie zmieniaj tych nazw — `SCENARIUSZE.pl.md` czyta się po polsku lepiej niż `SCENARIOS.pl.md`, a odnośniki i tak są sprawdzane osobno.

### Diagramy mermaid

Po każdej zmianie w `guides/DIAGRAMS.pl.md` albo `guides/DIAGRAMS.md` — także po zmianie samej etykiety.

```bash
npx -y @mermaid-js/mermaid-cli -i guides/DIAGRAMS.md -o /dev/null 2>&1 | tail -5
```

Alternatywnie zainstaluj `mermaid` i `jsdom` w katalogu tymczasowym i przepuść każdy blok przez `mermaid.parse()`. Oczekiwane: **4 bloki, 0 błędów**, w obu plikach.

### Wersje

```bash
grep -rn "version\|Wersja\|Version" --include="*.md" --include="*.cff" . | grep -oE "[0-9]+\.[0-9]+\.[0-9]+" | sort -u
```

Wszystkie pliki deklarujące wersję muszą deklarować **tę samą**. Wpisy historyczne w `CHANGELOG` są wyjątkiem — tam stare numery zostają.

---

## Konwencje pisania

### Rejestr

Piszemy **dla osoby z wykształceniem podstawowym**, prowadzącej małą firmę, bez cierpliwości do teorii.

- Zdania krótkie. Jedna myśl na zdanie.
- Druga osoba: „sprawdzasz", „wpisujesz", nie „należy sprawdzić".
- **Zero emotikon.** W całym repozytorium.
- **Zero wymyślonych metafor.** Żywe idiomy („gdzie jest haczyk", „widzimisię") zostają. Obraz, który trzeba rozpakować i który da się rozpakować inaczej — nie.
- Wyliczenie numerowane zamiast zdania ze spójnikami „albo/oraz".

**Kryterium rozstrzygające:** czy dwóch kompetentnych czytelników może zrozumieć to zdanie inaczej? Jeśli tak — przepisz wprost.

### Trzy znaczniki

Przechodzą przez cały tekst i są zadeklarowane na górze `STANDARD`:

- `**Dlaczego:**` — powód istnienia reguły
- `**Przykład:**` — przypadek rozstrzygający, który odczyt jest właściwy
- `**Uwaga:**` — miejsce, w którym czytelnicy najczęściej się mylą

### Reguła objętości

**Limitowana jest liczba zasad, nie liczba słów.** Dodanie zasady wymaga wycięcia zasady. `Dlaczego:`, `Przykład:` i `Uwaga:` można dokładać swobodnie.

Pełna reguła w `CONTRIBUTING.pl.md`.

---

## Słownik terminów wiążących

Te słowa mają w tym repozytorium jedno znaczenie. **Nie zastępuj ich synonimami**, nawet gdy zdanie brzmiałoby lepiej.

| Polski | English | Znaczenie |
|--------|---------|-----------|
| bramka systemu | framework gate | osiem zasad sprawdzanych przed decyzją |
| zamyka bramkę systemu | closes the framework gate | daje wynik NIE WOLNO |
| WOLNO / NIE WOLNO | ALLOWED / NOT ALLOWED | wynik bramki, zerojedynkowy |
| skutek nieodwracalny (jednokierunkowy) | irreversible (one-way) consequence | klasa obejmująca **cztery** warunki, nie tylko cofnięcie |
| skutek odwracalny (dwukierunkowy) | reversible (two-way) consequence | żaden z czterech warunków |
| opis nieprzychylny | unfavourable description | opis z założeniem złej woli, wyłącznie z faktów |
| najbliżej zamknięcia | closest to closing | wiersz obowiązkowy przy każdym WOLNO |
| flaga | flag | zadanie z terminem i osobą odpowiedzialną, cztery części |
| `[przed]` / `[potem]` | `[before]` / `[after]` | rodzaj flagi, ustalany przez skutek |
| ograniczenia tej oceny | limits of this assessment | rubryka obowiązkowa |
| co musiałoby się zmienić | what would have to change | zdanie wymagane przy NIE DZIAŁAJ |
| przegląd | review | pięć pytań o jakość |
| werdykt | verdict | DZIAŁAJ / DZIAŁAJ PO ZAMKNIĘCIU FLAG / NIE DZIAŁAJ |

**Osiem zasad** — nazwy nietykalne, w obu językach:

Kto odczuje · Czy mogą odmówić · Kto odpowiada · Czy to prawda · Gdzie jest haczyk · Czy powinniśmy · Czy dotrzymujemy słowa · Co, gdy się powtórzy

Who feels it · Can they refuse · Who answers for it · Is it true · Where is the catch · Should we · Do we keep our word · What if it repeats

---

## Format raportu z pracy

Na koniec sesji podaj:

1. **Co zmieniłeś** — plik po pliku, z powodem.
2. **Co zgłaszasz, a czego nie ruszyłeś** — wszystko, co wymagało decyzji autora.
3. **Wynik sprawdzeń** — odnośniki, emotikony, parzystość PL/EN, mermaid, wersje. Liczby, nie zapewnienia.
4. **Czego nie zrobiłeś i dlaczego.**

Jeśli coś nie działa — napisz to wprost razem z wyjściem polecenia. Nie zaokrąglaj w górę.
