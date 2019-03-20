# 4ME102
Poznámky ke kurzu 4ME102

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
- [3. Přednáška](#3.Přednáška)
- [4. Přednáška](#4.Přednáška)
---

- [1. Úkol](##Úkol1)









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

# 2.Přednáška

## Digitální fotografie

- sken na bubnový skener ( Digitalizovaná fotka)
- financováno armádou pro satelitní fotografie

### CCD Snímač

- Bell Labs - první snímače
- Kodak - první digitální fotoaparát ( studentský projekt )
    - utajovaný v rámci politiky Kodak ( ohrožuje filmový business )

### Elektronický analogový fotoaparát

- Elektronický snímač ukládaný na analogové médium ( floppy disk)

### Digitální zrcadlovka

- armádní projekt z Canon F1 s externí výpočetní jednotkou (1.2Mpx s kompresí) - vyrobil Kodak

- __Pro veřejnost__ - vydalo Fuji, ovšem nikdy v prodeji
- __komerční__ - vydal - Di-cam
- __První komerčně úspěšná__ byl Kodak DCS 100 ( z těla Nikon F3) - opět s výpočetní jednotkou

- 1996 - CF karty
- 1999 - APS-C formát čipu
- 2003 - záskává většinu na trhu nad Analogem

### Světlo a barvy
- Spektrum
- Viditelnost
- Neviditelné spektrum

### Fototechnika
- __objektiv__
    - ohnisková vzdálenost (1/f=1/u+1/v)

    ![](https://www.jaroslavsvoboda.eu/vyuka/multitech/img/ohniskova-vzdalenost.gif)

- __světelnost__
    - bezrozměrné číslo

### Snímače

    - všechny jsou černobílé a barvu dělí filtrem
    - CCD - staré
    - CMOS - název výrobní technologie čipu
    - NMOS - paralelní technologie Panasonic ( jiná struktura)
    - QIS - rostoučí nová technologie

- __CMOS__
    - BSI/BI - back imuminated ( zlepšuje světelnost)

- __QIS__
    - technologie založená na miniaturizaci na rozměru fotonu
    - obraz se skládá z 1000 snímků na binární bázi pro složení pixelu

    - v současné době pouze technologie bez průmyslového využití

- __Velikost čipu__

#### __Čtení barvy__ 
- __Bayerův Filtr__
    - by Kodak - Maska GRGB na čipu -> snižuje rozlišení
    - __Debayering__ - rekonstrukce pixelu z dat snímače - interpolace barev
        - řeší i hrany ( color bleading)
- Foveon X3
- __3CCD/3CMOS__
    - založeno na hranolu rozkládající obraz na 3
    - každý celý snímač má jednu barvu


### Digitální reprezentace obrazu

- vektorová grafika
- rastrová (bitmapová) grafika

__PIXEL__

    - pixel nemá fizický rozměr - jedná se o uložený 1 bod
    - většinou je lidsky důležité pouze rozlišení na plochu (PPI - pixelů na palec - obsah na palec)

- __Barevná hloubka__ - určuje počet bitů dedikovaných pro barevnou informaci ( na kanál (dělitená 3) / na pixel )
    - kompenzace malé barevné hloubky (__Dethering__) kombinuje okolní barvy -> rozostřuje

# 3.Přednáška

## Barva
- Subtraktivní a aditivní barva

### Barevný model
- HSV (Hue, Saturation, Value)
    - kuželový/válcový model
    - (trojuhelník a kolečko v editingu)
- HSL (Hue, Saturation, Lightness)
- Y'CbCr
    - Y' - jasová složka - Luma
    - Cb - chroma - od žluté do modrý
    - Cr - chroma - od zelený
    - způsob vhodný pro kompresy
- Lab

### chroma subsampling (podvzorkování barev)
- J (Y'):a(řádek):b(sloupec):alfa -> 4:2:0:0

### Gamma
- vyrovnávání barvy vůči lidskému vnímání

### Barevný prostor
- sRGB
    - 1996 na CRT monitory - globálně kompatibilní - barevně omezen
- AdobeRGB (víc zelený)
    - 1998 - měl by pokrýt CMYK standard pro tisk 1:1 monitor:tisk
    - 77%
- Pro Photo RGB (10bit)
    - je větší, 90% viditelného spektra

- NTSC - prostor barev, který je třeba reprodukovat

### Barevná teplota [K]

# Obrazové formáty

## RAW
- není formát -> zúpůsob zaznamenání konkrétního modelu fotoaparátu
- jedná se o uložená data z čipu -> existuje i ztrátová komprese
    - různé bitové hloubky 16bit (středoformát), 14(nekomprimované foto), 12bit (kompresní foto)


## DNG
- pokus o standardizaci RAW ( 2004 - Adobe)
- jde o TIFF s přidanými metadaty

## TIFF
- 1986 ( Aldus -> dnes Adobe)
- 1992 - poslední update ( verze 6 )
- Dosahuje MAX.4GB -> extrémně bezztrátová
- do 32bit -> umožňuje průhlednost, ale omezuje zbytek

## GIF
- 1996
- 8Bit na pixel -> 256 barev celkem 
[Space Jam](https://www.warnerbros.com/archive/spacejam/movie/jam.htm)

## PNG (Portable Network Grapgicks)
- vytvořen pro účely grafiky
- rozšíření APNG ( animované zatím bez podpory)

## JPG/JPEG (v komprimaci JFIF)

### JPEG Komprese

1. Převod do Y'CbCr
2. Podvzorkování na 4:2:0
3. převedení bit-hloubky z 0-255 na -128-128
4. rozdělení na bloky 8x8
5. DCT = diskrétní kosinová transformace (typ II) na každý blok
    - složení obrazce 8x8 pomocí složení z knihovny 64 modifikací cos
    > DCT koeficien - určuje váhu se kterou danou hodnotu promítáme

    ![DCT](https://jaroslavsvoboda.eu/vyuka/multitech/img/dct.gif)
6. Kvantizace - ztrátová
    - zaokrouhlování hodnoty na nejbližší celé číslo
7. Zig-Zag (cik-cak) seřazení dat
    - řazení hodnot podle ZIG-ZAG (od nejvýraznějších po nejjemnější)
8. RLE komprimace
    - přepíše stejné hodnoty do počtů
9. Huffmanovo nebo Aritmetické kódováni
    - patentované kódování
10. EOB za poslední nenulovou hodnotou

### JPEG2000
- funguje uplně jinak -> Vlnková komprese -> užití ve videu

### HEIF (AVC, HEVC)
- aplikace video komprese na jeden snímek

### WEBP
- Google formát založen na Web rodině formátu
- Otevřený ( bez licenčního omezení)
- umožňuje průhlednost

### AVIF
- vývoj Aliance pro Open Media - NETFLIX
- podporuje HDR a široké možnosti videa (alfa, animace, atd.)

### Vektorová grafika
- .eps - kombinace rasteru vektoru, podpora všeho
- .il - Adobe Illustrator - podporován i mimo adobe
- .svg

## Monitory
- CRT
- LCD
    - TN
    - IPS - nejzoršířenější
    - VA
    - PLS
- OLED/AMOLED
    - každý pixel svítí (nejsou podsvícené)

#### Vlastnosti monitory
- barevná hlobka 6.8,18 [barvy](http://www.tftcentral.co.uk/)
- FRC - framerade
- rozlišení ( pixelová hustota)

#### Konektory
- VGA - analog 1920x1550/60hz
- DVI-D - 2560x1600/60hz
- HDMI - záleží jaké 1.2, 2.0, 2.1 - dělá subsampling na všech vstupech, které překroší tok
- Display Port - VESA Standard - Daisy-chaining jinak podobný HDMI- jde poslad po USB/MHL




# Cvičení 1

## jpeginfo
- JPEG komprese je v různých souborových formátech ( JFIF, Exif )

## IMAGE MAGICK
- nainstalovat


# Cvičení 2

>magick compare -metric PSNR landscape.jpg conprim_15.jpg metric.png
>
>magick composite composite_blur.jpg comprim_15.jpg -compose difference rozdil.png
>
>magick convert -quality 15% composite_blur.jpg comprim_15.jpg
>
>magick convert landscape.jpg blurmap.jpg -compose Blur -set option:compose:args 10 -composite composite_blur.jpg
>
>magick montage -label "%f" *.jpg -shadow -tile 3x -geometry 500x500+10+10 kolac.jpg
>
>magick convert -delay 5/100 horse-*.jpg horse.gif
>
>magick convert -background red -fill green -font /usr/share/fonts/truetype/dejavu/DejaVuSans.ttf -pointsize 800 label:"Želva" zelva.jpg
>
>exiv2 -pt *jpg | grep NIKON > test
>
>exiv2 -pt medo-akt3.jpg
>
>exiv2 -M"set Exif.Image.Software Zelva" medo-akt3.jpg

# 4.Přednáška

Zvuk - Akustika

# Cvičení 3/4

FFMPEG
- podporuje externí knihovny

vždy potřebuje zadaný kodek
- pokud nemá přednastaveí pro konkrétní formát
- často jsou přednastavéné staré

> -c:a (codec pro audio)
>
> -c:v (codec pro video)

__nastavení kodeku__

Konstant bitrate

-  -b:a 128k -b:v 5000k

VBR

- -vbr 3 nebo -qscale:a 2

Avrage bitrate/Constant rate factor

- -crf 23 (0 = téměř bezztrátový)

Průchody ( multiple passes)
- pass 2 filename
- pass 1 -an /dev/null && \ 
     - ( -an je kódování videa .. běží jen na posledním průvhodu )

__Metadata__

>-metadata ...

__Obecné parametry__ ( bez zadání je často ukládá sám)

>-ar 44100 
>
>-chanels 2
>
>-ac 2 (pro downmix z více kanálů)
>
>-cutoff 15000 ( je low pass filter )

## AAC

>ffmpeg -i imput.wav -c:a libfdk_aac -b:a 128k out.m4a
>
>ffmpeg -i imput.mp4 -c:v copy -c:a libfdk_aac -b:a 128k out.m4a (-c:v copy dělá přímou kopii video součásti)

__profily__

>-profile:a aac_low ( default - je normálně užívané a je fajn)
>
>-profile:a aac_ld
>
>-profile:a aac_eld
>
>-profile:a aac_he (high-eficiency (drastická koprese))
>
>-profile:a aac_he_v2

__VBR__

ffmpeg -i imput.wav -c:a libfdk_aac -vbr 5 -b:a 128k out.m4a

(kvalita je na kanál - bitrate je na kanál)

Progresivní ( umožňuje přehrávání jako stream - remuxuje, nekoprimuje)

> -movflags +faststart

## MP3
libmp3lame

>ffmpeg -i imput.wav -codec:a libmp3lame -qscale:a 3 output.mp3
>
>ffmpeg -i imput.wav -codec:a libmp3lame -b:a 256k output.mp3 (nastavení -q:a 0-3)
>
>ffmpeg -i imput.wav -codec:a libmp3lame -b:a -abr output.mp3

## Opus
libopus

>ffmpeg -i imput.wav -codec:a libopus -b:a -q:a 10 output.ogg

---

funguje !!!

>/home/adam/bin/ffmpeg -i /mnt/d/obraz/audio/2L-111_15_stereo-44k-16b.flac -c:a libfdk_aac -b:a 128k  /mnt/d/obraz/audio/out.aac
bach na mnt musí bejt od root

# Úkol1

1) Zkomprimujte zvuk z 2L-111_mch-96k-24b_15.flac do formátu Opus, aby byl mono a menší než 760000 bajtů a měl stejnou vzorkovací frekvenci jako zdroj. Soubor pojmenujte "mono", vyberte vhodnou příponu a označte se jako vydavatel v metadatech. Použitý příkaz napište do souboru ukol1.

2) Zkomprimujte dolby_truehd_channel_check_lossless-DWEU.mkv do formátu AAC, tak aby měl shodnou vzorkovací frekvenci s CD. Toho docilte pomocí SoX Resampler Library. Výsledný soubor bude mít layout 5.1 se surround kanály na straně. Zároveň prohoďte pravý a levý přední kanál. Zvolte vhodný bitrate, aby byl zvuk dostatečně kvalitní. Soubor pojmenujte "cd", vyberte vhodnou příponu a označte KME jako poskytovatele vysílání v metadatech. Použitý příkaz napište také do souboru ukol1.

3) Zkomprimujte zvuk z 2L-111_stereo-352k-24b_15.flac do formátu Opus, aby měl vzorkovací frekvenci 48000Hz. Výsledný soubor by měl obsahovat cover z původního souboru. Soubor pojmenujte "48000", vyberte vhodnou příponu a do metadat uložte název původního souboru. Použitý příkaz napište také do souboru ukol1.

Na konci budete mít 3 zvukové soubory a jeden textový.Vše zabalte do archivu a vložte do odevzdávárny.

Soubory lze stáhnout z http://www.lindberg.no/hires/test/?C=N;O=D a https://www.demo-world.eu/download-2d-trailers/?file=dolby_truehd_channel_check_lossless-DWEU.mkv&pic=dolby_truehd_channel_check_lossless.jpg















## Khal Akademy - výpisky
---

### Information Theory
- jednoduché diskrétní datové svazky je obtimální řadit podle uřití a nejpouživanějšímu přiřadit nejkratší znak ( zprávu)
- data lze ukládat nejen v akci, ale i v neakci ( v mezerách)

__Morseova abeceda__ - Implementovala mezery jako informaci pro zkrácení každé předné zprávy. Umožňující vynález elektrického telegramu. ( urychlylo komunikaci na úrovni 50x)

__Limit diskrétní informace ( Symbol rate ) [n]__ - pro informaci vyslanou na větší vzdálenost nelze rozlišit příliž krátké změny. 

__Rozměr (symbol definition) [s]__ lze rozšířit o výce jak 2 typy informace - Síla pulzu
 - vzniká problém v rozlišení - je ovlivněn rušením a vyžaduje dostatečný rozdíl








