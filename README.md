# Strona Schronisko Łapa

**Plik:** `starter/index.html`  
**Dokumentacja Bootstrapa:** [Link do Bootstrapa](https://getbootstrap.com/docs/6.0/getting-started/install/)

Piszesz w `<body>`, nad pierwszym `<script>`. Skryptów na dole pliku nie zmieniasz. Po każdym kroku zapisz plik i odśwież przeglądarkę.

Strona składa się z czterech części, w tej kolejności:

1. `nav` — pasek na górze
2. `section#start` — wstęp na całą szerokość okna
3. `section#psy` — karty
4. `section#kontakt` — formularz

Tło dawaj na `section`, a `div.container` wkładaj **do środka** sekcji. Dzięki temu kolor sięga krawędzi okna, a tekst zostaje w węższej kolumnie.

---

## Ściąga

Z tych tabelek bierz liczby, gdy przy klasie jest napisane „patrz tabelka”.

### Ekrany

Siatka ma zawsze **12 kolumn**. Klasa `col-lg-7` znaczy: od breakpointu `lg` element zajmuje 7 z 12.

| Skrót       | Od jakiej szerokości | Przykład                           |
| ----------- | -------------------- | ---------------------------------- |
| brak skrótu | zawsze, od 0         | `col-12` — 12/12 na każdym ekranie |
| `sm`        | 576px                | `col-sm-6` — połowa od 576px       |
| `md`        | 768px                | `col-md-6` — połowa od 768px       |
| `lg`        | 992px                | `col-lg-4` — 4/12 od 992px         |
| `xl`        | 1200px               | `col-xl-3` — 3/12 od 1200px        |
| `xxl`       | 1400px               | `col-xxl-2` — 2/12 od 1400px       |

### Odstępy

Litera mówi, **co** odsuwasz. Liczba mówi, **o ile** — poziom z tabeli.

| Litera | Znaczenie                            |
| ------ | ------------------------------------ |
| `m`    | margin, odstęp na zewnątrz           |
| `p`    | padding, odstęp w środku             |
| `t`    | góra (top)                           |
| `b`    | dół (bottom)                         |
| `s`    | lewa strona (start)                  |
| `e`    | prawa strona (end)                   |
| `x`    | lewo i prawo                         |
| `y`    | góra i dół                           |
| `g`    | gap, odstęp między kolumnami w `row` |

| Poziom | Wielkość                                                        |
| ------ | --------------------------------------------------------------- |
| `0`    | 0                                                               |
| `1`    | 0.25rem = 4px                                                   |
| `2`    | 0.5rem = 8px                                                    |
| `3`    | 1rem = 16px                                                     |
| `4`    | 1.5rem = 24px                                                   |
| `5`    | 3rem = 48px                                                     |
| `auto` | przeglądarka sama dobiera odstęp, zwykle wypycha element na bok |

`mb-3` = margin-bottom, poziom 3 = 1rem (16px). `py-5` = padding góra i dół, poziom 5 = 3rem (48px).

### Kolory

W miejsce `{kolor}` wstawiasz nazwę z pierwszej kolumny.

| Nazwa       | Tło            | Tekst            | Przycisk        |
| ----------- | -------------- | ---------------- | --------------- |
| `primary`   | `bg-primary`   | `text-primary`   | `btn-primary`   |
| `secondary` | `bg-secondary` | `text-secondary` | `btn-secondary` |
| `success`   | `bg-success`   | `text-success`   | `btn-success`   |
| `danger`    | `bg-danger`    | `text-danger`    | `btn-danger`    |
| `warning`   | `bg-warning`   | `text-warning`   | `btn-warning`   |
| `info`      | `bg-info`      | `text-info`      | `btn-info`      |
| `light`     | `bg-light`     | `text-light`     | `btn-light`     |
| `dark`      | `bg-dark`      | `text-dark`      | `btn-dark`      |
| `white`     | `bg-white`     | `text-white`     | —               |

Jasna wersja tła: `bg-success-subtle` (do nazwy koloru dopisz `-subtle`). Ciemniejszy tekst na takim tle: `text-success-emphasis` (dopisz `-emphasis`). Na ciemnym tle (`bg-dark`, `bg-success`) dawaj jasny tekst: `text-white`. Przygaszony biały: `text-white-50`.

### Czcionki

`fs-1` jest największy, `fs-6` najmniejszy. `display-*` jest jeszcze większy i służy do tytułu strony.

| Klasa         | Co robi                           | Wielkość       |
| ------------- | --------------------------------- | -------------- |
| `display-5`   | wielki tytuł strony               | 3rem = 48px    |
| `display-6`   | duży tytuł                        | 2.5rem = 40px  |
| `fs-1`        | rozmiar 1                         | 2.5rem = 40px  |
| `fs-2`        | rozmiar 2                         | 2rem = 32px    |
| `fs-3`        | rozmiar 3                         | 1.75rem = 28px |
| `fs-4`        | rozmiar 4                         | 1.5rem = 24px  |
| `fs-5`        | rozmiar 5                         | 1.25rem = 20px |
| `fs-6`        | rozmiar 6, zwykły tekst           | 1rem = 16px    |
| `lead`        | wstęp pod tytułem, większy akapit | 1.25rem = 20px |
| `fw-bold`     | pogrubienie                       | grubość 700    |
| `fw-semibold` | półgrube                          | grubość 600    |
| `fst-italic`  | kursywa                           | —              |

---

## Krok 1. Navbar

Utwórz `nav` z klasami:

- `navbar` — włącza pasek nawigacji
- `navbar-expand-lg` — od breakpointu **lg** (992px, tabelka ekranów) linki są w jednym rzędzie; węższe okno pokazuje hamburger
- `navbar-dark` — jasne linki, do ciemnego tła
- `bg-success` — tło w kolorze **success** (zielony, tabelka kolorów)
- `sticky-top` — pasek zostaje u góry podczas przewijania

Wewnątrz `nav` ma być jeden `div` z klasą `container` (węższa kolumna na środku okna). W tym kontenerze, po kolei:

1. Link `a` z klasą `navbar-brand` (nazwa strony, większa niż zwykły link), atrybut `href="#start"`, tekst **Schronisko Łapa**.
2. Przycisk `button` z klasą `navbar-toggler` (przycisk hamburgera) i atrybutem `type="button"`.
   - `data-bs-toggle="collapse"` — klik otwiera i zamyka zwijane menu
   - `data-bs-target="#mainNav"` — które menu otworzyć
   - wewnątrz przycisku jeden `span` z klasą `navbar-toggler-icon` (ikona trzech kresek)
3. `div` z `id="mainNav"` i klasami `collapse navbar-collapse` (`collapse` chowa menu, `navbar-collapse` układa je w pasku).
   - wewnątrz lista `ul` z klasami `navbar-nav ms-auto`
     - `navbar-nav` — lista linków paska
     - `ms-auto` — margin-start `auto` (tabelka odstępów), wypycha listę na prawą stronę
   - w liście trzy elementy `li` z klasą `nav-item` (jedna pozycja menu)
   - w każdym `li` jeden link `a` z klasą `nav-link` (wygląd linku w pasku):
     - tekst **Start**, `href="#start"`
     - tekst **Psy**, `href="#psy"`
     - tekst **Kontakt**, `href="#kontakt"`

`id` menu i `data-bs-target` przycisku wskazują ten sam element: `mainNav`.

**Odśwież.** Zielony pasek na górze, po prawej trzy jasne linki. Zwęź okno poniżej 992px — zostaje przycisk z kreskami. Po kliknięciu widać Start, Psy i Kontakt.

---

## Krok 2. Sekcja Start

Pod navbarem utwórz `section` z `id="start"` i klasami:

- `bg-success-subtle` — jasne tło success (pastel; do nazwy koloru dopisane `-subtle`)
- `text-center` — tekst na środku
- `py-5` — padding góra i dół, poziom 5 = 3rem (48px)

Wewnątrz sekcji utwórz `div` z klasą `container`. W kontenerze:

1. `h1` z tekstem **Schronisko Łapa** i klasami:
   - `display-5` — wielki tytuł, 3rem (48px), tabelka czcionek
   - `fw-bold` — pogrubienie, grubość 700
   - `text-success` — zielony tekst, kolor success
2. `p` z jednym zdaniem o adopcji psów i klasami:
   - `lead` — większy akapit wstępu, 1.25rem (20px)
   - `text-success-emphasis` — ciemniejszy zielony, czytelny na jasnym tle `-subtle`
   - `mb-0` — margin-bottom poziom 0, czyli 0 (bez odstępu pod akapitem)

**Odśwież.** Jasnozielony pas na całą szerokość, na środku duży gruby zielony tytuł i pod nim większe zdanie.

---

## Krok 3. Trzy karty

Pod sekcją `#start` utwórz `section` z `id="psy"` i klasami:

- `bg-light` — jasnoszare tło, kolor light
- `py-5` — padding góra i dół, poziom 5 = 3rem (48px)

Wewnątrz sekcji `div.container`, a w nim:

1. `h2` z tekstem **Nasze psy** i klasami:
   - `fs-2` — rozmiar czcionki 2 = 2rem (32px)
   - `fw-semibold` — półgrube, grubość 600
   - `text-success` — zielony tekst
   - `mb-4` — margin-bottom, poziom 4 = 1.5rem (24px)
2. `div` z klasami `row g-3`
   - `row` — rząd siatki
   - `g-3` — gap między kolumnami, poziom 3 = 1rem (16px)
3. w tym rzędzie trzy kolumny — każda to `div` z klasami `col-12 col-md-6 col-lg-4`
   - `col-12` — zawsze 12/12, cała szerokość
   - `col-md-6` — od **md** (768px) połowa, 6/12
   - `col-lg-4` — od **lg** (992px) jedna trzecia, 4/12

W każdej kolumnie jest jedna karta. Karta to `div` z klasami `card h-100`.

- `card` — ramka karty
- `h-100` — wysokość 100% kolumny, karty w rzędzie są równo wysokie

Wewnątrz karty, w tej kolejności:

1. `img` z klasą `card-img-top` (obrazek na górze karty, na pełną jej szerokość)
   - adres: `https://picsum.photos/400/200?random=1` (w kolejnych kartach zmień numer przy `random`)
   - atrybut `alt` równy imieniu psa
2. `div` z klasą `card-body` (środek karty z odstępem w środku), a w nim:
   - `h5` z klasami `card-title fs-4 text-success` — imię psa
     - `card-title` — tytuł karty
     - `fs-4` — 1.5rem (24px)
     - `text-success` — zielony
   - `p` z klasami `card-text fs-6` — krótki opis
     - `card-text` — akapit w karcie
     - `fs-6` — zwykły tekst, 1rem (16px)
   - link `a` z tekstem **Adoptuj**, `href="#kontakt"` i klasami przycisku z tabeli poniżej
     - `btn` — wygląd przycisku
     - druga klasa to kolor z tabelki kolorów

| Karta | `random` | Imię  | Opis                                                                     | Przycisk                      |
| ----- | -------- | ----- | ------------------------------------------------------------------------ | ----------------------------- |
| 1     | `1`      | Burek | Spokojny pies, lubi spacery i dzieci. Ma 4 lata i jest już zaszczepiony. | `btn btn-info` (błękitny)     |
| 2     | `2`      | Luna  | Energiczna suczka do aktywnego domu. Uwielbia biegać i aportować.        | `btn btn-primary` (niebieski) |
| 3     | `3`      | Reks  | Starszy pies, szuka spokojnego miejsca. Najchętniej leży przy kanapie.   | `btn btn-warning` (żółty)     |

**Odśwież i zwęź okno.**

- od 992px (`lg`): trzy karty w jednym rzędzie
- od 768px (`md`) do 991px: dwie karty, trzecia pod nimi
- węziej niż 768px: jedna pod drugą
- między kartami jest odstęp 16px (`g-3`) także po przeniesieniu karty do następnego rzędu
- trzy przyciski mają trzy różne kolory

---

## Krok 4. Sekcja kontaktu

Pod sekcją `#psy` utwórz `section` z `id="kontakt"` i klasami:

- `bg-dark` — ciemne tło, kolor dark
- `text-white` — biały tekst, bo na `bg-dark` domyślny czarny tekst by zniknął
- `py-5` — padding góra i dół, poziom 5 = 3rem (48px)

Wewnątrz sekcji `div.container`, a w nim:

1. `h2` z tekstem **Napisz do nas** i klasami:
   - `fs-2` — 2rem (32px)
   - `text-warning` — żółty tekst, kolor warning
   - `mb-4` — margin-bottom, poziom 4 = 1.5rem (24px)
2. `div` z klasami `row g-3` (`g-3` = odstęp 1rem między kolumnami)
3. w rzędzie dwie kolumny:
   - lewa: `div` z klasami `col-12 col-lg-7`
     - `col-12` — na wąskim oknie cała szerokość
     - `col-lg-7` — od **lg** (992px) siedem dwunastych szerokości
   - prawa: `div` z klasami `col-12 col-lg-5`
     - `col-lg-5` — od **lg** pięć dwunastych; 7 + 5 = 12

W lewej kolumnie utwórz `div` z klasą `card` (biała karta, formularz zostaje czytelny na ciemnym tle), a w niej `div` z klasą `card-body`. Formularz z kroku 5 wchodzi do tego `card-body`.

W prawej kolumnie dwa akapity:

1. `p` z tekstem adresu: Schronisko Łapa, ul. Polna 12, 00-001 Warszawa, klasy:
   - `fs-5` — 1.25rem (20px)
   - `fw-bold` — pogrubienie
   - `mb-2` — margin-bottom, poziom 2 = 0.5rem (8px)
2. `p` z godzinami (odwiedziny wtorek–niedziela, 10:00–16:00) i zdaniem, że odpiszecie na e-mail, klasy:
   - `fs-6` — 1rem (16px)
   - `text-white-50` — biały tekst o połowie krycia, przygaszony na `bg-dark`
   - `fst-italic` — kursywa
   - `mb-0` — bez marginesu pod spodem

Na oknie od 992px formularz stoi obok adresu. Węziej obie kolumny są pod sobą, formularz na górze.

---

## Krok 5. Formularz

W `card-body` lewej kolumny utwórz `form` z klasą `needs-validation` (skrypt na dole pliku szuka tej klasy) i atrybutem `novalidate` (zostają czerwone ramki Bootstrapa, bez dymków przeglądarki).

Każde pole składa się z trzech rzeczy, w tej kolejności: `label`, pole, `div` z klasą `invalid-feedback` (czerwony komunikat, widać go po wysłaniu). Atrybut `for` etykiety ma ten sam napis co `id` pola. Każde pole poniżej ma atrybut `required`.

### Imię i e-mail w jednym rzędzie

W formularzu utwórz `div` z klasami `row g-3` (rząd, odstęp 1rem). W nim dwie kolumny, każda `div` z klasami `col-12 col-md-6`:

- `col-12` — na wąskim oknie pole na całą szerokość
- `col-md-6` — od **md** (768px) połowa, imię i e-mail obok siebie

Lewa kolumna:

- `label` z klasą `form-label` (etykieta nad polem), `for="imie"`, tekst **Imię**
- `input` z klasą `form-control` (wysokość i ramka pola), `type="text"`, `id="imie"`, `name="imie"`
- `div.invalid-feedback` z tekstem **Podaj imię**

Prawa kolumna:

- `label.form-label`, `for="email"`, tekst **E-mail**
- `input.form-control`, `type="email"`, `id="email"`, `name="email"`
- `div.invalid-feedback` z tekstem **Podaj e-mail**

### Temat

Pod rzędem utwórz `div` z klasami `mb-3 mt-3`:

- `mt-3` — margin-top, poziom 3 = 1rem (16px)
- `mb-3` — margin-bottom, poziom 3 = 1rem (16px)

Wewnątrz:

- `label.form-label`, `for="temat"`, tekst **Temat**
- `select` z klasą `form-select` (lista rozwijana w stylu pola), `id="temat"`, `name="temat"`
  - pierwsza `option`: tekst **Wybierz temat**, `value=""`, atrybuty `selected` i `disabled`
  - kolejna `option`: tekst **Adopcja**, `value="adopcja"`
  - kolejna `option`: tekst **Wolontariat**, `value="wolontariat"`
  - kolejna `option`: tekst **Inne**, `value="inne"`
- `div.invalid-feedback` z tekstem **Wybierz temat**

### Wiadomość

Pod tematem utwórz `div` z klasą `mb-3` (margin-bottom 1rem). Wewnątrz:

- `label.form-label`, `for="wiadomosc"`, tekst **Wiadomość**
- `textarea` z klasą `form-control`, `id="wiadomosc"`, `name="wiadomosc"`, `rows="4"`, `minlength="10"`
- `div.invalid-feedback` z tekstem **Wiadomość musi mieć co najmniej 10 znaków**

### Zgoda

Pod wiadomością utwórz `div` z klasami `form-check mb-3`:

- `form-check` — checkbox z etykietą w jednej linii
- `mb-3` — margin-bottom 1rem

Wewnątrz:

- `input` z klasą `form-check-input`, `type="checkbox"`, `id="zgoda"`, `name="zgoda"`
- `label` z klasą `form-check-label`, `for="zgoda"`, tekst **Wyrażam zgodę na kontakt**
- `div.invalid-feedback` z tekstem **Zaznacz zgodę**

### Przycisk

Na końcu formularza `button` z `type="submit"` i klasami `btn btn-success`:

- `btn` — wygląd przycisku
- `btn-success` — zielony, kolor success

Tekst przycisku: **Wyślij**.

Skrypt na dole pliku po kliknięciu „Wyślij” dodaje formularzowi klasę `was-validated`. Od tej klasy widać czerwone komunikaty. Własnego JavaScriptu nie dopisuj.

**Odśwież i sprawdź:**

1. Puste „Wyślij” zostawia stronę w miejscu. Pod każdym polem jest czerwony tekst po polsku.
2. E-mail `bez-malpy` (bez `@`) zostaje czerwony.
3. Wiadomość krótsza niż 10 znaków pokazuje komunikat o długości.
4. Pusta zgoda pokazuje **Zaznacz zgodę**.
5. Od 768px (`md`) imię i e-mail stoją w jednym rzędzie. Węziej są jedno pod drugim.
6. Sekcja kontaktu jest ciemna, nagłówek żółty, formularz na białej karcie, adres biały i pogrubiony, godziny kursywą i przygaszone.

---

## Krok 6. Oddanie

Zanim oddasz plik, każdy punkt ma być widoczny w przeglądarce.

1. Navbar jest zielony (`bg-success`) i zostaje na górze przy przewijaniu.
2. Po zwężeniu poniżej 992px hamburger się otwiera i pokazuje Start, Psy, Kontakt.
3. Klik „Psy” przewija do kart. Klik „Kontakt” i „Adoptuj” przewija do formularza.
4. Start ma jasnozielone tło na całą szerokość, wielki pogrubiony tytuł i większy akapit pod nim.
5. Sekcja psów jest jasnoszara. Trzy karty: zdjęcie, zielone imię, opis, przycisk. Przyciski: zielony, niebieski, żółty. Od 992px trzy obok siebie, poniżej 768px jedna pod drugą. Między nimi jest odstęp.
6. Kontakt ma ciemne tło i biały tekst. Nagłówek jest żółty. Formularz jest w białej karcie. Od 992px karta zajmuje 7/12, adres 5/12.
7. Pusty submit zostawia stronę w miejscu i pokazuje polskie komunikaty.
8. E-mail bez `@` jest czerwony. Zgoda jest wymagana.
9. Teksty są o schronisku (Burek, Luna, Reks).
