# v0.1.0

## 1 Mapa

Mapa składa się z następujących pól:

- Trawa <div style="width: 20px; height: 20px; background-color: green;"></div>
- Woda <div style="width: 20px; height: 20px; background-color: blue;"></div>
- Skała <div style="width: 20px; height: 20px; background-color: grey;"></div>

## 2 Ruch jednostek

### 2.1 Wykonanie ruchu

- Ruch może odbywać się jedynie na sąsiadujące pole, niemożliwy jest ruch po skosie.
- Jednostka może poruszać się maksymalnie o tyle pól, ile wynosi jej **Ruch**.
- Ruch jednostkami należy wykonywać po kolei, nie można jednocześnie poruszać się kilkoma jednostkami.

  Dozwolony ruch:

  ![allowed_move.png](/assets/images/allowed_move.png)

  Niedozwolony ruch:

  ![not_allowed_move.png](/assets/images/not_allowed_move.png)

### 2.2 RUCH JEDNOSTEK LĄDOWYCH

| Żeton     | Nazwa                                      | Możliwy ruch | Koszt |
| --------- | ------------------------------------------ | ------------ | ----- |
| Piechota  | ![knight.png](/assets/images/knight.png)   | 2            | 1     |
| Strzelcy  | ![archer.png](/assets/images/archer.png)   | 2            | 1     |
| Kawaleria | ![cavalry.png](/assets/images/cavalry.png) | 3            | 2     |

Jednostki lądowe mogą poruszać się po następujących polach:

- **Trawa**
- **Jednostki Oblężnicze**
- **Jednostki Wodne**
- **Mury** – mogą wchodzić na mury jedynie z sąsiadujących **Murów, Drabin, Wież oblężniczych i Bram**
- **Drabiny**
- **Bramy** – mogą poruszać się tylko przez sojusznicze bramy (o kolorze gracza)

  Po wykonanym ruchu można wykonać akcję jednostki i należy zaznaczyć, że dana jednostka jest już **wyczerpana** (wykonała już w tej turze posunięcie).

### 2.3 RUCH JEDNOSTEK OBLĘŻNICZYCH I WODNYMI

Warunki ruchu:

- Ruch jednostki oblężniczej i wodnej, możliwy jest tylko w momencie, kiedy wewnątrz znajduje się chociaż **jedna niewyczerpana sojusznicza jednostka** i nie ma w niej **żadnej wrogiej jednostki**.
- Po wykonanym ruchu można wykonać akcję jednostki oblężniczej i należy zaznaczyć **wszystkie jednostki** wewnątrz, jako **wyczerpane**.

### 2.4 RUCH JEDNOSTEK OBLĘŻNICZYCH

| Żeton   | Nazwa                                        | Możliwy ruch | Koszt |
| ------- | -------------------------------------------- | ------------ | ----- |
| Wieża   | ![tower.png](/assets/images/tower.png)       | 1            | 4     |
| Taran   | ![ram.png](/assets/images/ram.png)           | 1            | 4     |
| Trebusz | ![trebuche.png](/assets/images/trebuche.png) | 1            | 4     |

Jednostki oblężnicze mogą poruszać się po następujących polach:

- **Trawa**
- **Jednostki Wodne**
- **Bramy** – mogą poruszać się tylko przez sojusznicze bramy (o kolorze gracza)

Obrót:

- Zamiast ruchu można dokonać obrotu.
- Dozwolone są następujące kombinacje obrotu:

![rotation_1_start.png](/assets/images/rotation_1_start.png) ![arrow.png](/assets/images/arrow.jpg){ width="100" } ![rotation_1_end_1.png](/assets/images/rotation_1_end_1.png)

![rotation_1_start.png](/assets/images/rotation_1_start.png) ![arrow.png](/assets/images/arrow.jpg){ width="100" } ![rotation_1_end_2.png](/assets/images/rotation_1_end_2.png)

![rotation_1_start.png](/assets/images/rotation_1_start.png) ![arrow.png](/assets/images/arrow.jpg){ width="100" } ![rotation_1_end_3.png](/assets/images/rotation_1_end_3.png)

![rotation_1_start.png](/assets/images/rotation_1_start.png) ![arrow.png](/assets/images/arrow.jpg){ width="100" } ![rotation_1_end_4.png](/assets/images/rotation_1_end_4.png)

### 2.5 RUCH JEDNOSTKAMI WODNYMI

| Żeton                                               | Nazwa  | Możliwy ruch | Koszt |
| --------------------------------------------------- | ------ | ------------ | ----- |
| ![ship.png](/assets/images/ship.png){ width="220" } | Statek | 3            | 4     |

- Jednostki wodne mogą poruszać się jedynie po wodzie
- Ruch jednostki wodnej jest niemożliwy, jeśli jakaś jednostka oblężnicza znajduje się na niej nie w pełni

Obrót:

- Zamiast ruchu można dokonać obrotu.
- Dozwolone są następujące kombinacje obrotu:

![rotation_2_start.png](/assets/images/rotation_2_start.png) ![arrow.png](/assets/images/arrow.jpg){ width="100" } ![rotation_2_end_1.png](/assets/images/rotation_2_end_1.png)

![rotation_2_start.png](/assets/images/rotation_2_start.png) ![arrow.png](/assets/images/arrow.jpg){ width="100" } ![rotation_2_end_2.png](/assets/images/rotation_2_end_2.png)

## 3 AKCJA JEDNOSTEK

### 3.1 AKCJA JEDNOSTEK LĄDOWYCH

**Piechota** - w ramach akcji może zlikwidować sąsiednią, przeciwną jednostkę lądową.

**Kawaleria** - w ramach akcji może zlikwidować sąsiednią, przeciwną jednostkę lądową.

**Łucznicy** - w ramach akcji może spróbować zlikwidować przeciwną jednostkę lądową, która znajduje się w zasięgu.

Warunki likwidacji wrogiej jednostki:

- Odległość przeciwnika **mniejsza/równa 2**
- Wyrzucenie **5 lub 6 na kostce**

Warunki strzału

- Przed strzałem należy zadeklarować w którą jednostkę strzelamy.
- Strzelec nie może strzelać do jednostki, jeśli między strzelcem a jednostką znajduje się mur.
- Jeśli jednostka znajduje się na **murze lub wieży**, a przeciwna jednostka nie, odległość jest **o 1 mniejsza**.
- Jeśli **przeciwna** jednostka znajduje się na **murze lub wieży**, a strzelec nie, odległość jest **o 1 większa**.

### 3.2 AKCJA JEDNOSTEK OBLĘŻNICZYCH

Warunki akcji jednostki oblężniczej:

- Akcja jednostki oblężniczej, możliwa jest tylko w momencie, kiedy wewnątrz znajduje się chociaż **jedna niewyczerpana sojusznicza jednostka** i nie ma w niej **żadnej wrogiej jednostki**.
- Po akcji, **wszystkie jednostki** wewnątrz, są oznaczane jako **wyczerpane**.

  **Wieża** – nie posiada akcji

  **Taran** – w ramach akcji może spróbować zniszczyć sąsiadujący **mur** lub inną **budowle**

- Aby zniszczyć **mur** należy wyrzucić **5 lub 6 na kostce**.
- Aby zniszczyć **inna budowlę** należy wyrzucić **4, 5 lub 6 na kostce**.
- Można próbować zniszczyć wszystkie budowle poza Zamkiem i obozem.
- Po zniszczeniu budowli należy usunąć jej żeton, oraz ewentualnie wszystkich innych jednostek, które się na niej znajdowały.
- Taran musi być skierowany poziomo do budowli, którą ma zniszczyć

![ram_example_1.png](/assets/images/ram_example_1.png)

Trebusz – w ramach akcji może spróbować zniszczyć inną jednostkę, która jest w zasięgu.

- Trebusz musi być skierowany poziomo w stronę strzału.
- Rzuty **4,5,6** trafiają cel, który znajduje się na danej kratce (Tak jak na rysunku poniżej), nawet jeśli jest to sojusznik.
- Po zniszczeniu jednostki należy usunąć jej żeton, oraz ewentualnie wszystkich innych jednostek, które się na niej znajdowały.

![trebuche_example_1.png](/assets/images/trebuche_example_1.png)

## 4 BUDYNKI

| Żeton    | Nazwa                                        | Koszt | Maksymalna odległość budowy |
| -------- | -------------------------------------------- | ----- | --------------------------- |
| Zamek    | ![castle.png](/assets/images/castle.png)     | -     | -                           |
| Koszary  | ![barracks.png](/assets/images/barracks.png) | 8     | 5                           |
| Warsztat | ![workshop.png](/assets/images/workshop.png) | 8     | 5                           |
| Port     | ![port.png](/assets/images/port.png)         | 8     | 5                           |
| Obóz     | ![camp.png](/assets/images/camp.png)         | 32    | 20                          |
| Mur      | ![walls.png](/assets/images/walls.png)       | 4     | 10                          |
| Brama    | ![gate.png](/assets/images/gate.png)         | 4     | 10                          |
| Drabina  | ![ladder.png](/assets/images/ladder.png)     | 1     | 10                          |

### 4.1 ZAMEK

W ramach **akcji** pozwala wybudować dowolny **budynek**, lub pozyskać **4 monety**.

- Aby wybudować budynek, należy zapłacić jego **koszt**.
- Nowo wybudowana budowla, musi spełniać zasadę **maksymalnej odległości** od zamku.
- Nie ma możliwości wybudowania nowego zamku.
- Wszystkie budynki, można budować tylko i wyłącznie na **trawie**.
- Aby port mógł spełniać swoją akcję, powinien on być wybudowany w sąsiedztwie wody. Warto, aby obóz również był w sąsiedztwie wody.

### 4.2 KOSZARY

W ramach akcji pozwalają stworzyć maksymalnie **2 jednostki lądowe**.

- Aby stworzyć jednostki, należy zapłacić ich **koszt**.
- Nowopowstałe jednostki muszą znajdować się **w sąsiedztwie** koszar.
- Jednostkę można ustawić na tych polach na które może się ona normalnie ruszać.

### 4.3 WARSZTAT

W ramach akcji pozwalają stworzyć maksymalnie **1 jednostkę oblężniczą**.

- Aby stworzyć jednostkę, należy zapłacić jej **koszt**.
- Nowopowstała jednostka musi znajdować się **w sąsiedztwie** warsztatu.
- Jednostkę można ustawić na tych polach na które może się ona normalnie ruszać.

### 4.4 PORT

W ramach akcji pozwala stworzyć maksymalnie **1 jednostkę wodną**.

- Aby stworzyć jednostkę, należy zapłacić jej **koszt**.
- Nowopowstała jednostka musi znajdować się **w sąsiedztwie** portu.
- Jednostkę można ustawić jedynie na wodzie.

### 4.5 OBÓZ

W ramach akcji pozwala wykonać jedną z akcji **koszar, warsztatu lub portu**.

### 4.6 MUR, BRAMA I DRABINA

Te budynki nie posiadają akcji.

- Mur oraz brama, blokują możliwość przejścia wrogich jednostek.
- Mur (tak jak wieża oblężnicza) daje przewagę strzelcom, którzy się na nim znajdują.
- Na mur można wejść jedynie z innego **muru, drabiny, bramy lub wieży oblężniczej**.
- Przez bramę mogą przechodzić jedynie sojusznicze jednostki.

## 5 PRZEJMOWANIE ZAMKU I OBOZU

Wrogie zamki i obozy można przejąć.

- Aby przejąć wrogi zamek lub obóz, w ich sąsiedztwie muszą znajdować się przynajmniej **3 jednostki lądowe** osoby przejmującej i nie może znajdować się żadna jednostka lądowa właściciela zamku / obozu.
- Po przejęciu zamku, wszystkie należące do niego budynki (poza obozem), należą teraz do gracza przejmującego i może z nich korzystać jak ze swoich.

## 6 PRZYGOTOWANIE DO GRY

### 6.1 STANDARDOWY TRYB GRY

1. Gracze otrzymują po 64 monety.
2. Pierwszy gracz stawia zamek.
3. Drugi gracz stawia zamek w odległości minimum 16 pól od wrogiego zamku.
4. Drugi gracz rozpoczyna rozgrywkę turową.

### 6.2 TRYB OBLĘŻENIA

W tym trybie gry zamek zamiast swojej standardowej akcji, produkuje tylko **jedną monetę dziennie**.

Gracz atakujący musi jak najszybciej zdobyć zamek, ponieważ gracz broniący ciągle będzie się bogacił.

1. Gracz broniący i atakujący otrzymują po 64 monety.
2. Gracz broniący stawia zamek.
3. Gracz broniący buduje dowolną liczbę budynków, zgodnie ze standardowymi zasadami.
4. Gracz atakujący stawia 2 darmowe obozy w odległości minimum 16 pól od wrogiego od zamku.
5. Gracz atakujący rozpoczyna rozgrywkę turową.

## 7 ROZGRYWKA TUROWA

Każdy gracz w swojej turze wykonuje po kolei następujące akcje:

- Ruch i akcja jednostek.
- Akcja budynków.

## 8 WARUNKI WYGRANEJ

Gracz wygrywa w jednym z przypadków:

- Przeciwnik wykonał 3 tury, w których nie posiadał żadnego zamku ani obozu.
- Przeciwnik po zakończeniu swojej tury nie posiada żadnej jednostki lądowej.

## 9 SĄSIEDZTWO

Jednostki sąsiadują między sobą jedynie po bokach, natomiast budynki sąsiadują ze sobą również po skosie.

### 9.1 PRZYKŁADY SĄSIEDZTWA

![neighbourhood_1.png](/assets/images/neighbourhood_1.png)
/// caption
Piechota może zaatakować strzelców.
///

![neighbourhood_1.png](/assets/images/neighbourhood_2.png)
/// caption
Poprawne ustawienie jednostki po wytworzeniu.
///

![neighbourhood_1.png](/assets/images/neighbourhood_3.png)
/// caption
Poprawne ustawienie statku po wytworzeniu.
///

![neighbourhood_1.png](/assets/images/neighbourhood_4.png)
/// caption
Niepoprawnie wybudowane budynki.
///

![neighbourhood_1.png](/assets/images/neighbourhood_5.png)
/// caption
Niepoprawnie wybudowane budynki.
///

### 9.2 PRZYKŁADY BRAKU SĄSIEDZTWA

![neighbourhood_1.png](/assets/images/neighbourhood_6.png)
/// caption
Piechota nie może zaatakować strzelca.
///

![neighbourhood_1.png](/assets/images/neighbourhood_7.png)
/// caption
Niepoprawne ustawienie jednostki / statku po wytworzeniu.
///

![neighbourhood_1.png](/assets/images/neighbourhood_8.png)
/// caption
Poprawnie wybudowane budynki.
///

## 10 ODLEGŁOŚĆ MIĘDZY BUDYNKAMI I JEDNOSTKAMI

![distance.png](/assets/images/distance.png)
