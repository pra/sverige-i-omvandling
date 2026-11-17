# Sverige i omvandling

**Samhällsförändring, ekonomisk utsatthet och politiska möjligheter 1970–2026**

Webbsidan: **https://pra.github.io/sverige-i-omvandling/**

Underlaget beskriver hur Sverige har förändrats sedan 1970 och hur förändringen syns i partisympatierna 2026. Det tar upp näringsstruktur, utbildning, invandring, kollektiva skydd, geografi och ekonomisk utsatthet. Utifrån detta prövas vilka vägar till en majoritet som finns för S, V och MP. Sidan inleds med en överblick i två delar och följs av fjorton fördjupningar.

## Innehåll

| Sökväg | Innehåll |
|---|---|
| `index.html` | Den fristående webbsidan. All data, d3 och ritkoden är inbäddade, så sidan fungerar även nedladdad och utan nätverk. |
| `data/DATAKATALOG.md` | **Börja här.** Beskriver varje datafil: källa, antal rader, kolumner och hur den är härledd. |
| `data/webb/` | De dataset som sidans siffror och diagram läses ur, en CSV per dataset. |
| `data/huvuddata.xlsx` | Samma dataset som flikar i en Excel-bok. |
| `data/panel/` | Kommunpanelen: 290 kommuner och 277 stabila kommunenheter. Den innehåller valresultat 1973–2026, näringsstruktur 1970–2024, indikatorer för utsatthet och skydd, yrkesanalyser, regressionsresultat och en kommunreferens med SKR:s kommungrupper. |
| `data/scb_uttag/` | Uttag ur SCB:s statistikdatabas och Kolada. För stora tabeller står klartexterna i en separat `*_koder.csv`. |
| `data/ocr/` | Tabeller ur Folk- och bostadsräkningarna 1970 och 1980, tolkade med OCR ur skannade volymer. Kolumnen `status` anger om raden klarar tabellens kontrollsummor. |
| `data/manuellt/` | Tabeller som har skrivits av för hand ur rapporter: facklig organisationsgrad och kollektivavtal (Kjellberg), Valu 2026, SOM-undersökningens flyktingfråga och Institutet för Framtidsstudiers studie av SD:s väljare. Första raden i varje fil anger källan. |

Alla CSV-filer är UTF-8, kommaseparerade och har punkt som decimaltecken. Kommunkoderna är fyrsiffriga strängar, så den inledande nollan ska behållas.

## Källor

- **SCB, Statistikdatabasen** (https://www.statistikdatabasen.scb.se): RAMS/BAS, yrkesregistret, AKU, ULF/SILC, partisympatiundersökningen (PSU), befolkning, utbildning, inkomster, företagsregistret, lönestrukturstatistiken och valdeltagandeundersökningen.
- **SCB, Folk- och bostadsräkningarna 1970 och 1980** (skannade tryckta volymer, tolkade med OCR).
- **Kolada** (https://www.kolada.se): kommunala nyckeltal.
- **Valmyndigheten** (https://www.val.se): riksdagsval 1973–2026.
- **Trafikanalys** (https://www.trafa.se): fordon i trafik.
- **Anders Kjellberg** (Lunds universitet och Arena Idé): facklig organisationsgrad och kollektivavtalstäckning.
- **Medlingsinstitutet** (https://www.mi.se): kollektivavtalstäckning.
- **SVT/Valu 2026**: vallokalsundersökningen vid riksdagsvalet 2026.
- **SOM-institutet, Göteborgs universitet**:
  - [Svenska trender 1986–2025](https://www.gu.se/sites/default/files/2026-03/Svenska%20trender%201986-2025.pdf)
  - [Svenska trender 1986–2022, tabellappendix](https://www.gu.se/sites/default/files/2023-04/1.%20Svenska%20trender%201986-2022%20-%20Tabellappendix.pdf)
  - [Svenska stad-land-trender 1986–2025](https://www.gu.se/sites/default/files/2026-09/Svenska%20stad-land-trender%201986-2025.pdf)
- **Jylhä, Rydgren och Strimling (2018)**: *Sverigedemokraternas väljare. Vilka är de, var kommer de ifrån och vart är de på väg?* Institutet för Framtidsstudier (https://www.iffs.se), Forskningsrapport 2018/2.

Rapporterna i PDF-format ingår inte i repot. De uppgifter som har hämtats ur dem finns i `data/manuellt/`, och varje fil anger källa och sidnummer.

## Förbehåll

- PSU, Valu, ULF/SILC och SOM är urvalsundersökningar. Felmarginalen för delgrupper är 2–5 procentenheter.
- Kommunsambanden är ekologiska och säger inget direkt om enskilda väljare.
- Mandatberäkningen är förenklad: nationell modifierad uddatalsmetod med fyraprocentsspärr. Den återger valet 2022 exakt.
- Siffrorna för 1970–1980 bygger på OCR och har kontrollerats mot tabellernas radsummor. Ungefär 10 % av kommunenheterna uteslöts eftersom de inte klarade kontrollen.
- Avsnittet om politiska möjligheter innehåller bedömningar som bygger på data. Vilken väg som är rätt beror också på vad partierna vill uppnå.
