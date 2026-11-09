# BOOK-59: SCISSOR, analiza fisierelor sursa din Canva (imagini, dimensiuni, linii)

Data: 9 noiembrie 2026
Carte: Scissor Skills & Tracing Activity Book for Kids Ages 3-5 (Paperback B0F8BTDX3M)

## Rezumat

* Fisierul corect este **DAGl6RZpXGw** ("Spikee - Level 1", 56 de pagini). Nu este DAGj87mfKbU. Acela e masterul de 181 de pagini.
* Dimensiunile sunt corecte. Interior 8.5x11 inch fara bleed. Coperta 17.375x11.25 inch.
* Linia de taiat a chenarului e buna pe toate paginile: neagra, 4.6 la 4.8 pt.
* Problema principala: liniile de activitate (traseele de taiat si de trasat) sunt imagini PNG la 64 pana la 203 ppi, nu vectori. Pe cel putin 15 din 21 de pagini de activitate. La tipar ies cu margini zimtate sau moi.
* Liniile de trasat sunt prea subtiri si prea deschise pentru 3 la 5 ani pe multe pagini (aprox. 1 la 2 pt, gri 50%).
* Pe 11 din 21 de pagini traseul e greu de urmarit: rupt, acoperit de desene sau amestecat cu liniile desenului.
* Spikee arata diferit de la o pagina la alta. Pe coperta si pe unele pagini nu are placi de stegozaur.
* Interiorul contine coperta fata (p.1) si spate (p.56) cu imagini pana la marginea paginii, fara bleed.

Verdict: fisierele sursa nu sunt gata pentru o editie noua sau pentru traduceri (BOOK-29 la 32). Liniile de activitate trebuie refacute inainte.

## 1. Versiunea Canva corecta

| Design | Pagini | Ce este |
|---|---|---|
| DAGl6RZpXGw "Spikee - Level 1 - Skills & Tracing Activity Book for Kids Ages 3-5" | 56 | **Interiorul publicat.** 56 de pagini, ca pe KDP (BOOK-10). Folosit si in BOOK-54 si BOOK-78. Ultima modificare cea mai recenta. |
| DAGm7kCq5FU "Cover Spikee - Level 1 ..." | 2 | **Coperta publicata.** Pagina 1 e coperta completa. Pagina 2 e goala. |
| DAGj87mfKbU "book Scissor Skills & Tracing Activity Book for Kids Ages 3-5" | 181 | Master pentru nivelurile 1 la 4. Nu e fisierul publicat (vezi BOOK-81). |
| DAGm-uvm7TU "[3-5][ENG][text][Spikey]..." | 56 | Draft vechi "Spikey". |
| DAGm_ayqifE "[3-5][ENG][H][text][Spikey]..." | 63 | Draft vechi, probabil pentru Hardcover (BOOK-28). |
| DAGpVcDVt68 "Copy of Cover Spikee ..." | 1 | Copie de coperta, format portret. Nu e coperta de tipar. |

Nu am avut acces la KDP. Potrivirea se bazeaza pe numarul de pagini, titlu si continut. Confirma in KDP ca PDF-ul interior incarcat are 56 de pagini si ca p.1 incepe cu coperta.

## 2. Dimensiuni

### Interior (DAGl6RZpXGw)

* Canvas: 816x1056 px pe toate cele 56 de pagini. In Canva asta inseamna 8.5x11 inch.
* PDF exportat: 612x792 pt (8.5x11 inch). TrimBox egal cu MediaBox, deci fara bleed.
* Trim size declarat pe KDP: 8.5x11 (BOOK-10). **Se potriveste.**

Margini verificate pe toate paginile (KDP cere minimum 0.25 inch la exterior si 0.375 inch la cotor pentru 24 la 150 de pagini):

| Pagina | Problema |
|---|---|
| 1 | Coperta fata, imagine pana la margine pe toate laturile. Fara bleed, deci risc de dunga alba sau respingere. |
| 6 | Continut la 0.29 inch de cotor (minim 0.375). |
| 21 | Continut la 0.25 inch de cotor (minim 0.375). |
| 52 | Linie verticala neagra la 0.84 inch de margine, pe toata inaltimea paginii, pana sus si jos. Pare ghidaj ramas. |
| 56 | Coperta spate, imagine pana la margine. Aceeasi problema ca la p.1. |

Restul paginilor respecta marginile.

### Coperta (DAGm7kCq5FU)

* Canvas: 1669x1080 px. PDF exportat: 1251x810 pt, adica 17.375x11.25 inch.
* Calcul: 2 x 8.5 + 2 x 0.125 bleed = 17.25. Cotor = 0.125 inch.
* Cotor KDP la 56 de pagini: hartie alba 0.126 inch (56 x 0.002252). Color premium 0.131 inch (56 x 0.002347).
* **Se potriveste cu hartie alba, alb-negru.** Daca pe KDP e setat interior color premium, coperta e mai ingusta cu aprox. 0.006 inch. Confirma tipul de hartie in KDP.
* Cotorul nu are text. Corect, KDP nu permite text pe cotor sub 79 de pagini.
* Zona de cod de bare (dreapta jos pe spate) are doar frunze de fundal. Nu se pierde nimic important.

Observatie: interiorul are elemente color (p.1, p.56, emoji, iconite). Daca cartea e tiparita alb-negru, acestea ies in tonuri de gri.

## 3. Rezolutia imaginilor (DPI)

Metoda: export PDF "pro" din Canva, apoi `pdfimages -list`. Am ignorat imaginile sub 0.25 inch patrati (iconite mici).

| Rezolutie efectiva | Imagini |
|---|---|
| 300 ppi sau mai mult | 314 |
| 250 la 299 ppi | 15 |
| 150 la 249 ppi | 29 |
| sub 150 ppi | 19 |

### Linii de activitate salvate ca imagini (cea mai importanta problema)

Traseele de taiat si trasat nu sunt desenate ca forme vectoriale in Canva. Sunt PNG-uri transparente. Le-am extras si verificat una cate una.

| Pagina | Activitate | Rezolutie traseu |
|---|---|---|
| 19 | Leaf Race Tracing | **64 ppi** |
| 47 | Dino Footprint Follow | **75 ppi** |
| 27 | Rainbow Arc Path | **80 ppi** |
| 13 | Tall Mountain Line | **96 ppi** |
| 35 | Curvy Water Stream | **97 ppi** |
| 21 | Dino-Maze Rescue (labirint) | 118 ppi |
| 25 | Spiral Slide with Leafy | 118 ppi |
| 43 | Leafy's Loop Lesson | 123 ppi |
| 41 | Spiral Snail Adventure | 132 ppi |
| 39 | Volcano Circle Dash | 134 ppi |
| 17 | Tiny Steps Trail | 137 ppi |
| 37 | Zig-Zag Hill Trek | 145 ppi |
| 49 | The Big Loop to the Finish | 160 ppi |
| 15 | Tree Climb Challenge | 181 ppi |
| 33 | Curvy Path in the Valley | 203 ppi |

Dovada: `BOOK-59-p19-zoom-300dpi.png`. La 300 dpi traseul de pe p.19 are trepte vizibile. Chenarul de dedesubt e vector si e curat.

Paginile 6, 11, 23, 29, 31 si 45 nu au aparut cu trasee raster. Nu le-am extras individual.

### Alte imagini sub 150 ppi

* p.1 si p.56: fundalul de frunze 832x1248 px la 82 la 91 ppi si ilustratia la 125 ppi. Sunt copertele din interior.
* Coperta separata: fundal 80 la 90 ppi, ilustratia principala 123 ppi. La zoom 300 dpi personajul arata acceptabil (stil desenat, contur gros). Frunzele de fundal sunt moi.
* p.3: amprentele de dinozaur pe cartonase, 155 la 169 ppi. Acceptabil.

KDP recomanda 300 ppi. Imaginile decorative la 120 la 200 ppi ies acceptabil in stil coloring. Liniile de activitate nu, pentru ca copilul trebuie sa le urmareasca exact.

## 4. Liniile de taiat si de trasat

Esantion: toate cele 21 de pagini de activitate (6, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37, 39, 41, 43, 45, 47, 49). Randate la 300 dpi. Grosimea masurata automat pe linii (transformata de distanta pe schelet).

### Chenarul (linia de taiat exterioara)

* Pe toate cele 20 de pagini cu chenar: linie neagra intrerupta, 19 la 20 px la 300 dpi, adica **4.6 la 4.8 pt**.
* Peste minimul de 2 pt din BOOK-10. Contrast maxim. **OK.**
* Fiecare pagina are 2 sau 3 iconite de foarfeca. Nu e clar de unde incepe copilul. Recomand o singura foarfeca la punctul de start.

### Traseele din interior

Repere pentru 3 la 5 ani (estimare, practica uzuala la caiete de grafomotricitate): linie de trasat de cel putin 3 pt, neagra sau gri inchis, cu punct de start marcat. Linie de taiat de cel putin 3 pt, neintrerupta de desene.

| Pagina | Traseu | Grosime / contrast | Lizibilitate | Verdict |
|---|---|---|---|---|
| 6 | Warm-up: dreapta, zig-zag, cerc | Groase, negre | Clar, fara desene peste | OK |
| 11 | Dreapta | Linia de taiat 2.9 pt neagra. Linia de trasat nu se distinge, apare doar o linie verticala subtire de 1.9 pt | Activitatea "trace the dotted line" nu are linie punctata vizibila | Problema |
| 13 | Diagonala pe munte | Neagra, raster 96 ppi | Se amesteca cu hasurile muntelui | Problema |
| 15 | Trapez in jurul copacului | Subtire, aprox. 1 pt | Clar ca forma, dar subtire | Mediu |
| 17 | Zig-zag (trepte) | Neagra, raster 137 ppi | Segmente acoperite de fluturi si pietre. Traseul se rupe | Problema |
| 19 | Curba frunzei | Neagra, raster 64 ppi | Zimtat la tipar | Problema |
| 21 | Labirint | Gri deschis, subtire, raster 118 ppi | Peretii abia se vad. Si prea greu pentru p.21 (BOOK-80) | Problema |
| 23 | Arc catre Chompy | Neagra, groasa | Clar | OK |
| 25 | Toboganul | 4.3 la 4.8 pt negru, raster 118 ppi | Clar. Margini usor moi. Forma nu e spirala, cum spune titlul | OK minor |
| 27 | Arcul curcubeului | Neagra, raster 80 ppi | Liniute rare, amestecate cu liniile curcubeului | Problema |
| 29 | Cerc in jurul cuibului | Neagra, groasa | Clar | OK |
| 31 | Pod cu bucle | Linie punctata de aprox. 1 pt cu segmente groase decalate peste | Confuz: doua stiluri de linie care nu se suprapun | Problema |
| 33 | Drum ondulat | Subtire, raster 203 ppi | Merge paralel cu marginile drumului desenat | Mediu |
| 35 | Paraul | Neagra, raster 97 ppi | Liniute rare, sageti gri printre ele, fundal gri | Problema |
| 37 | Zig-zag pe munte | 1.7 la 2 pt, gri 50%, raster 145 ppi | Forma clara, dar subtire si deschisa | Mediu |
| 39 | Cerc in vulcan | Cerc interior punctat foarte subtire, cerc exterior gri | Doua cercuri, sageti turcoaz, linii de crater peste | Problema |
| 41 | Spirala melcului | Aprox. 1.5 pt, raster 132 ppi | Forma clara. Subtire | Mediu |
| 43 | Bucle | Neagra, raster 123 ppi | Traseu fragmentat, goluri mari | Problema |
| 45 | Cercuri concentrice | Subtire | Clar, fara desene peste | Mediu |
| 47 | Contur de amprenta | Liniute negre pe umplutura gri 50%, raster 75 ppi | Contrast slab. Consum mare de cerneala | Problema |
| 49 | Bucla finala | Neagra, raster 160 ppi | Traseu fragmentat, forma de bucla nu se citeste | Problema |

Total: 4 OK, 1 OK minor, 5 Mediu, 11 Problema.

## 5. Consistenta vizuala si progresia

Consistenta:

* Spikee are cel putin 4 stiluri diferite: gri realist (p.3, p.8), pui verde fara placi pe coperta, pui cu creasta rotunda fara placi (p.15, 19, 33, 37, 41), stegozaur cu placi (p.13, 31, 35, 47). Pe multe pagini nu se vede ca e stegozaur.
* Pe p.11 personajul principal arata ca un T-Rex. Textul spune ca e Spikee.
* Stilul ilustratiilor variaza: contur gros curat (p.29, 41), schita in creion gri (p.25, 27, 43), desen realist (p.3). Unele pagini au jumatate din desene gri deschis si jumatate negre.
* Elemente comune bune: acelasi chenar, aceeasi bordura cu labute, aceeasi structura titlu, instructiuni, activitate, "Dino Fact".
* Activitatile sunt pe pagini impare, iar pe verso sunt ghicitori sau glume. Taierea nu distruge alta activitate. Verso-ul pierde insa ghicitoarea. Detaliat in BOOK-10.

Progresia:

* Ordinea pe forme e acoperita de BOOK-80 (labirint prea devreme, 3 linii ondulate la rand).
* Din punct de vedere vizual, dificultatea nu creste constant. Paginile usoare (23, 29) vin dupa labirintul greu (21). Paginile cu cele mai confuze trasee (43, 49) sunt la final, unde copilul ar trebui sa aiba succes.

## 6. Recomandari

1. Refa toate traseele de activitate ca forme vectoriale in Canva (Line sau Shape, cu stil intrerupt). Alternativ, PNG la minimum 300 ppi la dimensiunea de pe pagina.
2. Un singur standard de linie pe toata cartea: trasat 3 la 4 pt, negru sau gri 70%, punctat; taiat 4 pt, negru, intrerupt. Punct de start verde si o singura foarfeca.
3. Scoate desenele care acopera traseele (p.13, 17, 27, 35, 39). Pune desenele decorative in gri deschis, traseul in negru.
4. Refa p.11 (linie de trasat lipsa), p.31 si p.39 (doua stiluri de linie suprapuse), p.43 si p.49 (traseu rupt).
5. P.47: inlocuieste umplutura gri cu contur simplu.
6. Decide un singur design pentru Spikee si foloseste-l peste tot, inclusiv pe coperta.
7. Interior: decide daca p.1 si p.56 (copertele) raman in interior. Daca raman, adauga bleed (canvas 8.625x11.25) sau lasa margine alba de 0.25 inch. Sterge linia de pe p.52. Muta continutul de pe p.6 si p.21 la 0.375 inch de cotor.
8. Confirma in KDP tipul de hartie si cerneala. Regenereaza coperta cu KDP Cover Calculator daca nu e alb-negru pe hartie alba.
9. Fa toate acestea in fisiere noi sau dupa BOOK-80, ca sa nu refaci paginile de doua ori. Traducerile (BOOK-29 la 32) se fac dupa.

## 7. Ce nu am putut verifica

* PDF-ul efectiv incarcat in KDP si setarea de hartie si cerneala. Nu am acces la KDP. BOOK-10 verifica PDF-ul din KDP.
* Pragurile de 3 pt pentru trasat sunt o estimare din practica uzuala, nu o regula KDP.
* O copie tiparita. Efectul real al imaginilor la 64 la 100 ppi se vede cel mai bine pe hartie.

## Fisiere

* `BOOK-59-p19-zoom-300dpi.png`: traseu raster 64 ppi fata de chenar vector.
* `BOOK-59-p47-contrast.png`: contur de taiat pe umplutura gri.

## Surse

* KDP Help, Paperback trim size, bleed si margini: https://kdp.amazon.com/help/topic/G201834180
* KDP Help, Paperback cover (latime cotor): https://kdp.amazon.com/help/topic/G201953020
* Canva: DAGl6RZpXGw (interior), DAGm7kCq5FU (coperta), exportate PDF "pro" pe 9 noiembrie 2026.
