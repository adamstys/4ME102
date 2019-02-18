# 4ME102 - Multimediální Technologie


cca 13 přednášek

rozhodně se jedná o práci na 13 přednášek

  <p style="color:#FF0000";>
  Docházka je poviná s 1 omluvou!!!
  </p>

Začíná to úvodem do teorie informace, a komprese, což je prakticky celá první přednáška


# Úvod

- [1. Prednaska](#1.Přednáška)
    - [Entropie](##Entropie)
    - [Komprese](##Komprese)
    - [Výpočetní hardware](##Výpočetní_hardware)

- [2. Přednáška](#2.Přednáška)










## Bodování
- 35b - domácí úkoly - kodování, FFMPEG, ...
- 20b test
- 35b - ústní - pokud budem v průběhu dělat to co máme, tak by neměla být další příprava za potřebí
- 20b - aktivita
    - opravy chyb v prezentacích
    - relevantně nová informace jakéhokoliv druhu k tématu
    - vlastní aktivita jakéhokoliv druhu


Práce se bude ochomítat okolo kódování multimédií v FFMPEGu -> budou DÚ

- přehled v informatice [Khal Akademy](https://www.khanacademy.org/join/5YESQNKT) - ( [KA_výpisky](##KhalAkademy-výpisky) který dostanete do mailu a měly byste splnit do 3. týdne
- dodatečné zdroje je doporučeno hledat na [Youtube](www.youtube.com) a prezentace naleznete [stránkách vyučujícího](https://www.jaroslavsvoboda.eu/)

### Seminárka

- jelikož jde o další praktickej předmět je seminárka publikována veřejně
    1. wiki - sepsat normostranu na wiki k jakémukoliv příbuznému technickému tématu
    2. OpenSource - spolupráce na Open Source projektu a o včetně pomoci s propagací, či jinou čiností v rámci takového projektu ( nemusí být technická)

# 1.Přednáška
- jedná se především o představení komprese a zadání úkolu

__Digitál vs. Analog ( Diskrétní vs. spojité hodnoty)__

> There are 10 types of people in the world
…
Those who know binary and those who don’t. 

Přepočet binárního kódu do decimální soustavy - pouze číselně

Bit vs. Bajt

__Ztrátová vs. Bezztrátová komprese ( reorganizace vs. aproximace)__

Komprese vřdy probíhá v zájmu odstranění redundance ( množství duplicitních informací)

-> Jak nacpat co největší množství informace do co nejméně dat

Hranice pro __ztrátovou__ kompresi je smyslové vnímání ( nesmí to bejt hnusný)
Hranicí pro __bezztrátovou__ kompresi je Entropie

## Entropie

učebnice : [Odkaz](https://popelka.ms.mff.cuni.cz/~lessner/mw/index.php/U%C4%8Debnice/Informace/Informace,_entropie_a_fyzika)

 - střední (průměrná) hodnota informace jednoho kódovaného znaku
    - značí limit pro bezztrátovou kompresi - většího komprese nelze dosáhnou při zachování dat.

> B. Pascal na konci dopisu: Omlouvám se, že je můj dopis tak dlouhý, neměl jsem čas napsat kratší

- komprese vyžaduje velký výpočetní výkon i datovou propustnost a způsobuje zpoždění
    - pro časově kritické operace se proto nepoužívá

Dělení nosičů informace podle procesu

- __Informace__ - uživatelsky čitelný obsah (Křeslo)
- __Symboly__ - používají se k zakódování informace (hromada dílů s manuálem)
- __Data__ - skládají se ze symbolů (Nesrozumitelná hromada dílů)
- __Zpráva__ - je nosičem dat (balík)

## Komprese

- __Hoffmanovo kódování__ - Nejčasteji vyskytovaný znak je uložen nejkratším řetězcem bitů.

- __Run-Lenghth encoding__ - komprese po sobě jdoucích znaků z AAAAA je 5A
- __Lempel-Ziv-Welch 84 (LZW)__
- __Lempel-Ziv-Markov-Chain Algorithm (LZMA)__ - 7-Zip
- __DEFLATE__ - ZIP

### Ztrátová komprese

- Mnohonásobně účinější, než bezztrátová ( 60% vs. 8% )
- Analizují data a následně maže člověkem nepostřehnutelné části
- transparentnost = mez, kdy člověk není schopen rozeznat originál a ztrátově komprimovanou kopii

__Kodeky a kontejnery__

- standardy a systémy na kódování a dekódování dat

__Standard__ je vydáván institucí : [ITU](https://www.itu.int/en/Pages/default.aspx) / [ISO](https://www.iso.org/home.html)

__Kódovací formát__ - je formát zakódovaného média
__Kodek__ - je implementace kódování - SW/HW proces kódování/dekódování
__Kontejner__ - balík obsahující více datových svazků - video, zvuk, titulky

#### Weberův-Fechnerův Zákon

- intenzita smyslového vjemu je logaritimicky závislá na intenzitě fyzikálního podnětu
- smyslové vnímání není ve svém rozsahu lineární, ovšem klesá rychleji
- Při velké intenzitě věmu tělo nerozpozní menší rozdíly

#### DECIBEL
- logaritmická jednotka - log10

#### SHANNONŮV-NYQUISTŮV TEORÉM
 - pro reprodukci děje se musí samplovací frekvence = minimálně 2x rychlost samotného děje

![aliasing](https://www.jaroslavsvoboda.eu/vyuka/multitech/img/aliasing2.png)

Pokud je frekvence nižší mohou vznikat sčítací obrazce

## Výpočetní_hardware

- CPU ( počítačový procesor) - je schopen spracovat libovolná data po malých balíčcích v lineárních proudech velmi rychle a efektivně
- GPU ( grafický procesor) - Je omezen na [ASIC](https://en.wikipedia.org/wiki/Application-specific_integrated_circuit) , ovšem zvládne masivní paralelní výpočty a má vlastní velmi rychlou dedikovanou paměť

### Další zdroje

- __YouTube__ - https://www.youtube.com/playlist?list=PLzH6n4zXuckpKAj1_88VS-8Z6yn9zX_P6
- __Khal Akademy__
    - https://www.khanacademy.org/computing/computer-science/informationtheory
    - https://www.khanacademy.org/computing/computer-science/how-computers-work2

Je na to vlastní předmět na matice - nechtěl bych
- 4IZ410 - Teorie informace a inference - prof. RNDr. Jiří Ivánek, CSc.

## Khal Akademy - výpisky

### Information Theory
- jednoduché diskrétní datové svazky je obtimální řadit podle uřití a nejpouživanějšímu přiřadit nejkratší znak ( zprávu)
- data lze ukládat nejen v akci, ale i v neakci ( v mezerách)

__Morseova abeceda__ - Implementovala mezery jako informaci pro zkrácení každé předné zprávy. Umožňující vynález elektrického telegramu. ( urychlylo komunikaci na úrovni 50x)

__Limit diskrétní informace ( Symbol rate ) [n]__ - pro informaci vyslanou na větší vzdálenost nelze rozlišit příliž krátké změny. 

__Rozměr (symbol definition) [s]__ lze rozšířit o výce jak 2 typy informace - Síla pulzu
 - vzniká problém v rozlišení - je ovlivněn rušením a vyžaduje dostatečný rozdíl


# 2.Přednáška





