# CLAUDE.md — zasady pracy w repozytorium Malek Symbiosis Standard

Ten dokument wyjaśnia, jak Claude Code ma pracować w tym repozytorium. Przeczytaj go przed rozpoczęciem każdej sesji.

Dokument jest po polsku, ponieważ polski jest językiem źródłowym projektu. Wszystkie poniższe zasady obowiązują jednak zarówno w polskich, jak i w angielskich plikach.

---

## Co znajduje się w tym repozytorium

To repozytorium zawiera instrukcje, a nie program. Nie ma tu aplikacji, zależności ani testów jednostkowych. Są tu dokumenty Markdown w języku polskim i angielskim. Opisują one zasady oceny decyzji, które mogą wpłynąć na innych ludzi.

Tekst jest głównym produktem tego repozytorium. Dlatego zmiana jednego słowa może zmienić sposób, w jaki czytelnik podejmie ważną decyzję. Każdą zmianę tekstu traktuj równie uważnie jak zmianę kodu w działającym programie.

---

## Trzy zasady, od których nie wolno odstąpić

Możesz odstąpić od poniższych zasad tylko wtedy, gdy autor wyraźnie poprosi o to w bieżącej rozmowie.

### 1. Nie decyduj samodzielnie o treści zasad MSS

Możesz poprawić plik, jeśli jego treść jest niezgodna z zasadą, która już znajduje się w `standard/STANDARD.pl.md` albo `standard/STANDARD.md`. W takim przypadku doprowadzasz plik do zgodności z tekstem kanonicznym.

Nie możesz samodzielnie ustalać, jak powinna brzmieć nowa zasada ani zmieniać znaczenia istniejącej zasady. Takie decyzje podejmuje autor.

Jeśli podczas pracy znajdziesz problem, którego rozwiązanie wymaga decyzji o treści zasady:

1. nie zmieniaj tej zasady;
2. opisz problem w raporcie końcowym;
3. wskaż, jakiej decyzji autora potrzebujesz.

Aby ustalić, czy możesz wprowadzić zmianę, odpowiedz na pytanie: **czy możesz wskazać istniejące zdanie w standardzie, z którym uzgadniasz dany plik?**

- Jeśli tak, możesz poprawić plik.
- Jeśli nie i musisz dopisać nowe zdanie do standardu, zaczekaj na decyzję autora.

**Przykład:** polecenie „rozwiąż to bezpiecznie” nie zawsze oznacza zwykłą poprawkę. Dodanie obowiązkowego pola do przykładu rozstrzyga, że to pole jest wymagane. Taką decyzję może podjąć tylko autor.

### 2. Wprowadzaj każdą zmianę w obu językach

Polska i angielska wersja dokumentacji są równie ważne. Muszą mieć to samo znaczenie. Zmiana nie jest ukończona, dopóki nie została wprowadzona w obu wersjach językowych.

Polski jest językiem źródłowym. Jeśli autor zmienił polski tekst, dostosuj do niego wersję angielską. Nie zmieniaj polskiego tekstu na podstawie angielskiej wersji.

Samo porównanie wersji polskiej z angielską nie wystarcza. Obie wersje mogą zawierać ten sam błąd. Dlatego sprawdzaj także, czy zmieniany dokument jest zgodny ze standardem.

### 3. Nie publikuj zmian

Bez wyraźnej zgody autora w bieżącej rozmowie nie wolno:

1. wykonywać `git push`;
2. tworzyć zdalnego repozytorium;
3. zmieniać widoczności repozytorium na publiczną;
4. publikować plików w innym miejscu.

Możesz utworzyć lokalny commit, jeśli otrzymasz takie polecenie.

Nie usuwaj plików bezpowrotnie. Jeśli plik ma zniknąć z repozytorium, przenieś go do katalogu roboczego wskazanego przez autora. Jeśli autor nie podał katalogu, poproś go o wskazanie miejsca.

---

## Układ repozytorium

### Katalog główny

- `README.md` i `README.pl.md` — przedstawiają projekt, jego cel i historię. Nie zawierają zasad MSS.
- `LICENSE.md` — zawiera prawny tekst licencji CC BY-SA 4.0. Plik celowo istnieje tylko po angielsku. Nie tłumacz go.
- `CITATION.cff` — zawiera dane potrzebne do cytowania projektu.
- `CONTRIBUTING.md`, `CONTRIBUTING.pl.md`, `SECURITY.md`, `SECURITY.pl.md`, `CHANGELOG.md` i `CHANGELOG.pl.md` — opisują sposób pracy nad projektem i jego historię.
- `CLAUDE.md` — dokument, który właśnie czytasz.
- `.gitattributes` — zapewnia jednakowy zapis końców linii na różnych systemach operacyjnych.

### `standard/` — tekst kanoniczny

- `STANDARD.md` i `STANDARD.pl.md` — zawierają wszystkie zasady MSS. Pozostałe dokumenty muszą być z nimi zgodne.
- `AGENT.md` i `AGENT.pl.md` — wyjaśniają modelowi AI, kiedy rozpocząć ocenę, jakie pytania zadać i jak zapisać wynik.

Pliki `STANDARD` i `AGENT` znajdują się w jednym katalogu, ponieważ użytkownik przekazuje je modelowi razem.

### `guides/` — instrukcje dla użytkownika

- `USE-WITH-CLAUDE.md` i `USE-WITH-CLAUDE.pl.md` — opisują uruchomienie MSS. Zawierają skróconą kopię standardu.
- `NAME-USAGE.md` i `NAME-USAGE.pl.md` — wyjaśniają, kiedy można użyć określenia „zgodne z MSS”.
- `DIAGRAMS.md` i `DIAGRAMS.pl.md` — zawierają cztery diagramy Mermaid.

### Pozostałe katalogi

- `examples/` — zawiera trzy wymyślone przykłady pełnej oceny, w obu językach.
- `tests/` — zawiera dziesięć opisów osób, trzydzieści scenariuszy, warianty i kartę wyników.
- `assets/` — zawiera logo MSS.
- `.github/` — zawiera formularze zgłoszeń i szablon pull requesta.

W plikach w katalogu `tests/` celowo nie ma oczekiwanych werdyktów. Powód opisuje `tests/README.pl.md`. Nie dodawaj takich werdyktów.

### Ważna kopia zasad w instrukcji uruchomienia

Pliki `USE-WITH-CLAUDE` zawierają skrócony fragment standardu, który użytkownik może wkleić do rozmowy z modelem. Te same zasady są tam opisane innymi słowami.

Po każdej zmianie zasady sprawdź, czy trzeba również zmienić ten fragment. Bez tego instrukcja uruchomienia może zacząć mówić coś innego niż standard.

---

## Kiedy stosować MSS podczas pracy w tym repozytorium

Stosuj pełną ocenę MSS, gdy podejmujesz decyzję dotyczącą:

1. dodania, usunięcia albo zmiany znaczenia zasady w plikach `STANDARD.*`;
2. opublikowania czegokolwiek poza tym repozytorium;
3. treści przykładu, ponieważ ludzie będą się z niego uczyć;
4. nazwy projektu;
5. licencji projektu.

Nie stosuj pełnej oceny przy poprawianiu literówki, naprawianiu odnośnika, zmianie formatowania ani podczas samego czytania plików.

Pełna procedura znajduje się w `standard/STANDARD.pl.md`. Jej kolejność to: skutek, bramka systemu, przegląd, flagi, termin powrotu do sprawy, werdykt i ograniczenia oceny.

Wynik rzeczywistej oceny roboczej umieść w raporcie z wykonanej pracy. Nie zapisuj go w plikach repozytorium. Katalog `examples/` służy wyłącznie do przechowywania wymyślonych scenariuszy.

---

## Sprawdzenia wymagane przed zakończeniem pracy

Jeśli zmiana nie ogranicza się do poprawienia literówki, wykonaj wszystkie sprawdzenia opisane poniżej.

### 1. Odnośniki, znaki graficzne i pary językowe

Uruchom:

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

Prawidłowy wynik zawiera:

- `martwe: 0`;
- `emotikony: 0`;
- żadnego wiersza zaczynającego się od `BRAK PL:`.

Lista `BEZ_PL` zawiera celowe wyjątki:

- `LICENSE.md` pozostaje po angielsku, ponieważ tłumaczenie prawnego tekstu licencji mogłoby zmienić jego znaczenie;
- `CLAUDE.md` i `.github/PULL_REQUEST_TEMPLATE.md` są wewnętrznymi plikami roboczymi, a nie częścią standardu.

Nie dodawaj nowych wyjątków do listy `BEZ_PL` bez zgody autora.

Lista `PARY` łączy trzy angielskie pliki testowe z polskimi plikami, które mają inne nazwy. Nie zmieniaj tych nazw. Polskie nazwy są celowe, a poprawność odnośników jest sprawdzana osobno.

### 2. Diagramy Mermaid

Po każdej zmianie w `guides/DIAGRAMS.md` albo `guides/DIAGRAMS.pl.md`, także po zmianie samej etykiety, uruchom:

```bash
npx -y @mermaid-js/mermaid-cli -i guides/DIAGRAMS.md -o /dev/null 2>&1 | tail -5
```

Możesz zamiast tego zainstalować pakiety `mermaid` i `jsdom` w katalogu tymczasowym, a następnie sprawdzić każdy blok za pomocą `mermaid.parse()`.

Prawidłowy wynik dla każdej wersji językowej to cztery poprawne bloki i zero błędów.

### 3. Numery wersji

Uruchom:

```bash
grep -rn "version\|Wersja\|Version" --include="*.md" --include="*.cff" . | grep -oE "[0-9]+\.[0-9]+\.[0-9]+" | sort -u
```

Każdy aktualny dokument musi podawać ten sam numer wersji. Starsze numery mogą pozostać tylko we wpisach historycznych w plikach `CHANGELOG`.

---

## Zasady pisania tekstu

Pisz dla osoby, która ma podstawowe wykształcenie, prowadzi małą firmę i nie zna specjalistycznego słownictwa.

1. Pisz krótkimi zdaniami.
2. W każdym zdaniu przedstawiaj jedną myśl.
3. Zwracaj się bezpośrednio do czytelnika. Pisz „sprawdzasz” i „wpisujesz” zamiast „należy sprawdzić” i „należy wpisać”.
4. Nie używaj emotikonów.
5. Nie twórz metafor, które czytelnik może rozumieć na kilka sposobów. Możesz zachować powszechne zwroty, takie jak „gdzie jest haczyk” i „widzimisię”.
6. Gdy zdanie zawiera kilka warunków, przedstaw je jako numerowaną listę zamiast długiego ciągu połączonego słowami „albo” i „oraz”.
7. Jeśli dwie osoby mogą rozsądnie zrozumieć zdanie na różne sposoby, napisz je ponownie bardziej bezpośrednio.

### Stałe oznaczenia objaśnień

W całym standardzie używaj tych samych trzech oznaczeń:

- `**Dlaczego:**` — wyjaśnia powód istnienia zasady;
- `**Przykład:**` — pokazuje, jak zastosować zasadę i rozstrzyga możliwą niejasność;
- `**Uwaga:**` — wskazuje błąd, który czytelnicy popełniają najczęściej.

### Ograniczenie liczby zasad

Ograniczamy liczbę zasad, a nie liczbę słów. Jeśli dodajesz nową zasadę, musisz usunąć inną zasadę. Możesz bez takiej zamiany dodawać objaśnienia oznaczone jako `Dlaczego:`, `Przykład:` albo `Uwaga:`.

Pełne wymagania znajdują się w `CONTRIBUTING.pl.md`.

---

## Terminy, których nie wolno zastępować synonimami

Poniższe określenia mają w projekcie ściśle ustalone znaczenie. Używaj ich zawsze w podanej formie, nawet jeśli synonim brzmi naturalniej.

| Polski termin | Angielski termin | Znaczenie |
|---|---|---|
| bramka systemu | framework gate | osiem zasad sprawdzanych przed podjęciem decyzji |
| zamyka bramkę systemu | closes the framework gate | powoduje wynik NIE WOLNO |
| WOLNO / NIE WOLNO | ALLOWED / NOT ALLOWED | dwa możliwe wyniki sprawdzenia bramki systemu |
| skutek nieodwracalny (jednokierunkowy) | irreversible (one-way) consequence | klasa obejmująca cztery warunki, a nie tylko brak możliwości cofnięcia |
| skutek odwracalny (dwukierunkowy) | reversible (two-way) consequence | skutek, który nie spełnia żadnego z czterech warunków nieodwracalności |
| opis nieprzychylny | unfavourable description | opis oparty wyłącznie na faktach, napisany z założeniem złej woli autora decyzji |
| najbliżej zamknięcia | closest to closing | obowiązkowy wiersz przy każdym wyniku WOLNO |
| flaga | flag | zadanie zawierające problem, osobę odpowiedzialną, termin i warunek zamknięcia |
| `[przed]` / `[potem]` | `[before]` / `[after]` | rodzaj flagi ustalany na podstawie skutku decyzji |
| ograniczenia tej oceny | limits of this assessment | obowiązkowa część zapisu wskazująca braki wiedzy i sprawdzenia |
| co musiałoby się zmienić | what would have to change | zdanie wymagane przy werdykcie NIE DZIAŁAJ |
| przegląd | review | pięć pytań o jakość decyzji |
| werdykt | verdict | DZIAŁAJ, DZIAŁAJ PO ZAMKNIĘCIU FLAG albo NIE DZIAŁAJ |

Nie zmieniaj nazw ośmiu zasad ani ich kolejności.

**Po polsku:** Kto odczuje · Czy mogą odmówić · Kto odpowiada · Czy to prawda · Gdzie jest haczyk · Czy powinniśmy · Czy dotrzymujemy słowa · Co, gdy się powtórzy

**Po angielsku:** Who feels it · Can they refuse · Who answers for it · Is it true · Where is the catch · Should we · Do we keep our word · What if it repeats

---

## Co musi zawierać raport końcowy

Po zakończeniu pracy podaj cztery części:

1. **Wprowadzone zmiany.** Wymień każdy zmieniony plik i wyjaśnij powód zmiany.
2. **Problemy pozostawione do decyzji autora.** Opisz wszystko, czego nie zmieniłeś, ponieważ wymagało to decyzji o treści zasady. Jeśli nie znalazłeś takich problemów, napisz to wprost.
3. **Wyniki sprawdzeń.** Podaj rzeczywiste wyniki kontroli odnośników, emotikonów, par językowych, diagramów Mermaid i numerów wersji. Podawaj liczby, a nie samo zapewnienie, że kontrola się powiodła.
4. **Niewykonane czynności.** Wymień wszystko, czego nie zrobiłeś, i wyjaśnij dlaczego.

Jeśli polecenie zakończy się błędem, pokaż ten błąd w raporcie. Nie przedstawiaj częściowego wyniku jako pełnego sukcesu.
