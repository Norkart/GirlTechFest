# GirlTechFest
Opplegg for GirlTechFest i Kristiansand

* Kart på web
    * Vector tiles
* Kartografi
* Design og UU
* Lag ditt eget kart! 
    * Bytt stil på kartet
        * Basis, datascience, aquarell,  school map
    * (??) Flytt center til skolen din
    * Endre på zoom-nivået
    * Fargelegg med dine farger!
    * Ta inn / ut ulike datalag
        * Liste med aktuelle datalag
            * bygninger, vann, m.m.
        * Fargelegg ulikt
    * (??) Ta inn andre data fra andre kilder (geojson)
    * (??) Klikk i kartet


# Webutvikling

Webutvikling handler om å lage nettsteder og applikasjoner som vi kan bruke på internett. Det er som å bygge et hus, der hver del har sin egen funksjon.

## 1. HTML (HyperText Markup Language)

HTML er grunnlaget for enhver nettside. Tenk på HTML som skjelettet til et hus. Den forteller nettleseren hva som skal vises på siden. For eksempel, hvis du vil ha en overskrift, bruker du HTML for å lage den. Du kan også bruke HTML til å sette inn tekst, bilder og lenker. Så når du besøker en nettside, er det HTML som forteller nettleseren hva den skal vise og hvor alt skal være.

## 2. CSS (Cascading Style Sheets)

Når skjelettet er bygget med HTML, er det tid for å pynte det. Det er her CSS kommer inn. CSS fungerer som maling og dekorasjoner for huset. Det bestemmer hvordan nettsiden ser ut, for eksempel hvilken farge bakgrunnen skal ha, hvilken skrifttype teksten skal bruke, og hvordan bilder skal plasseres. Med CSS kan du gjøre en nettside både fin og spennende å se på!

## 3. JavaScript

JavaScript gir liv til nettsiden. Tenk på det som lysene og bevegelsene i huset. Med JavaScript kan du lage interaktive funksjoner, som å vise en melding når du klikker på en knapp eller endre bildet som vises. Det gjør at nettsiden kan reagere på hva brukeren gjør. For eksempel, når du fyller ut et skjema, kan JavaScript hjelpe til med å sjekke om du har skrevet inn alt riktig før du sender det.

## Oppsummering

Så, når vi lager en nettside, bruker vi HTML for å lage strukturen, CSS for å pynte den, og JavaScript for å gjøre den interaktiv. Sammen skaper de en spennende og brukervennlig opplevelse på nettet!

# (TODO) Design og universell utforming
* ...

# Kartutvikling på Web med Vektortiles

Kartutvikling på web handler om å lage interaktive kart som brukere kan navigere i. Ved å bruke vektortiles kan vi lage kart som er både raske og fleksible. Her er en enkel forklaring på prosessen:

## 1. Hva er Vektortiles?

Vektortiles er små biter av kartdata som inneholder informasjon om geografiske elementer, som veier, elver, bygninger og annen infrastruktur. I motsetning til rasterbilder (som JPEG eller PNG), som er faste og kan miste kvalitet når de skaleres, er vektortiles laget av matematiske former. Dette gjør at de kan skaleres opp eller ned uten å miste kvalitet.

## 2. Hvordan Fungerer Vektortiles?

Når du navigerer på et kart, laster nettleseren inn vektortiles fra en server. Disse tilesene gir informasjon om hva som skal vises på kartet, avhengig av hvilket zoom-nivå du er på. For eksempel, når du zoomer inn, kan flere detaljer som bygninger og veier vises.

## 3. Enkel Styling av Kartet

Etter at vektortiles er lastet inn, kan du bruke CSS-lignende språk for å style kartet. Her er noen enkle måter å style vektortiles på:

- **Farger**: Endre fargene på veier, elver, og bygninger for å gjøre kartet mer visuelt tiltalende.
- **Typer**: Velg forskjellige linjetyper for veier, som stiplete eller solide, for å vise forskjeller mellom motorveier og småveier.
- **Ikoner**: Bruke ikoner for å representere steder, som restauranter eller parker, for å gjøre kartet mer informativt.

## 4. Bruke Kartbiblioteker

Det finnes mange biblioteker, som **Mapbox** eller **Leaflet**, som gjør det lettere å jobbe med vektortiles og styling. Disse bibliotekene gir ferdige verktøy for å laste inn vektortiles, håndtere interaktivitet, og style kartet.

## Oppsummering

Ved å bruke vektortiles kan du lage raske og skalerbare kart på weben. Med enkel styling kan du tilpasse kartet slik at det blir både informativt og estetisk. Dette gir en bedre brukeropplevelse og lar folk enkelt navigere i geografisk informasjon.


# (TODO) Lag ditt eget kart!

## Oppgave1: Lag ditt eget kart
* Gå inn på ... 
* Trykk deg rundt i kartet

## Oppgave2: Bytt stil på kartet
* Endre på tilejson

## Oppgave3: Endre startposisjon
* Bytt center og zoom 
** Her er listen med posisjonen til skoler

## Oppgave4: Fargelegg kartet ditt
* Sånn fargelegger du bygninger, veger, vann
* Prøv deg frem med forskjellige farger. Bruk eksemplene i slutten for å få inspirasjon! 


# Lag et 3D-kart!

## Oppgave1: Vis kartet i 3D
* Åpne URL'en... 

## Oppgave2: Endre på tilt og zoom
* Klarer du bytte center til skolen din?

## Oppgave3: Gjør bygningene høyere
* Skaleringsfaktor

## Oppgave4: La vannet bli høyere
* Sette høyde på vann

## Oppgave5: Fargelegg med alpha
* Bruk fargene fra første del. 
* Sett alpha og se hva som skjer

## Ta et skjermbilde og skriv ut!
* Printscreen og print? 


# (TODO) Lag ditt eget 3D-kart!
* Lag et 3D-kart!
    * Fargelegg
    * Høyere bygninger
    * Velg ut noen bygninger
    * La vannet være i 3D

# Farger og webkoder
Farger må beskrives i koder for at datamaskinen skal forstå det. Under er noen ferdige fargekoder som bruker rgba-koder for å beskrive fargene. RGBA er Red Green Blue Alpha. Alpha er hvor gjennomsiktig fargen skal være. 

Det finnes mange ferdige paletter med farger for kart. Disse er egnet for å vise data i kart på en riktig måte. Vi har brukt http://colorbrewer2.org/ til å hente ut noen vanlige fargepaletter i tillegg til regnbuefargene. 

## Regnbuefarger

<div style="width:100px; height:100px; background-color:rgba(255, 0, 0, 1);"></div>
`rgba(255, 0, 0, 1)` - Rød

<div style="width:100px; height:100px; background-color:rgba(255, 127, 0, 1);"></div>
`rgba(255, 127, 0, 1)` - Oransje

<div style="width:100px; height:100px; background-color:rgba(255, 255, 0, 1);"></div>
`rgba(255, 255, 0, 1)` - Gul

<div style="width:100px; height:100px; background-color:rgba(0, 255, 0, 1);"></div>
`rgba(0, 255, 0, 1)` - Grønn

<div style="width:100px; height:100px; background-color:rgba(0, 0, 255, 1);"></div>
`rgba(0, 0, 255, 1)` - Blå

<div style="width:100px; height:100px; background-color:rgba(75, 0, 130, 1);"></div>
`rgba(75, 0, 130, 1)` - Indigo

<div style="width:100px; height:100px; background-color:rgba(139, 0, 255, 1);"></div>
`rgba(139, 0, 255, 1)` - Fiolett

### Sekvensiell palett - gul-grønn-blå
Egnet til: Visning av data som har en naturlig rekkefølge, for eksempel fra lav til høy verdi

<div style="width:100px; height:100px; background-color:rgba(255, 255, 204, 1);"></div>
`rgba(255, 255, 204, 1)`

<div style="width:100px; height:100px; background-color:rgba(199, 233, 180, 1);"></div>
`rgba(199, 233, 180, 1)`

<div style="width:100px; height:100px; background-color:rgba(127, 205, 187, 1);"></div>
`rgba(127, 205, 187, 1)`

<div style="width:100px; height:100px; background-color:rgba(65, 182, 196, 1);"></div>
`rgba(65, 182, 196, 1)`

<div style="width:100px; height:100px; background-color:rgba(44, 127, 184, 1);"></div>
`rgba(44, 127, 184, 1)`

### Sekvensiell palett: Lilla til rød
Egnet til: Data med en naturlig progresjon, for eksempel intensitet av fenomen, eks. populasjonstetthet, bygningshøyder, vanntemperatur

<div style="width:100px; height:100px; background-color:rgba(247, 244, 249, 1);"></div>
`rgba(247, 244, 249, 1)`

<div style="width:100px; height:100px; background-color:rgba(231, 225, 239, 1);"></div>
`rgba(231, 225, 239, 1)`

<div style="width:100px; height:100px; background-color:rgba(212, 185, 218, 1);"></div>
`rgba(212, 185, 218, 1)`

<div style="width:100px; height:100px; background-color:rgba(201, 148, 199, 1);"></div>
`rgba(201, 148, 199, 1)`

<div style="width:100px; height:100px; background-color:rgba(223, 101, 176, 1);"></div>
`rgba(223, 101, 176, 1)`

### Divergerende palett: Rød til blå
Egnet til: Visualisering av data som går fra én ekstrem til en annen, f.eks. temperaturavvik eller politiske målinger.

<div style="width:100px; height:100px; background-color:rgba(103, 0, 31, 1);"></div>
`rgba(103, 0, 31, 1)` - Rød

<div style="width:100px; height:100px; background-color:rgba(178, 24, 43, 1);"></div>
`rgba(178, 24, 43, 1)`

<div style="width:100px; height:100px; background-color:rgba(214, 96, 77, 1);"></div>
`rgba(214, 96, 77, 1)`

<div style="width:100px; height:100px; background-color:rgba(244, 165, 130, 1);"></div>
`rgba(244, 165, 130, 1)`

<div style="width:100px; height:100px; background-color:rgba(253, 219, 199, 1);"></div>
`rgba(253, 219, 199, 1)`

<div style="width:100px; height:100px; background-color:rgba(209, 229, 240, 1);"></div>
`rgba(209, 229, 240, 1)`

<div style="width:100px; height:100px; background-color:rgba(146, 197, 222, 1);"></div>
`rgba(146, 197, 222, 1)`

<div style="width:100px; height:100px; background-color:rgba(67, 147, 195, 1);"></div>
`rgba(67, 147, 195, 1)`

<div style="width:100px; height:100px; background-color:rgba(33, 102, 172, 1);"></div>
`rgba(33, 102, 172, 1)`

<div style="width:100px; height:100px; background-color:rgba(5, 48, 97, 1);"></div>
`rgba(5, 48, 97, 1)` - Blå

### Kvalitativ palett: Myke pastellfarger
Egnet til: Visualisering av kategoriske data som har lik vekt, f.eks. ulike grupper eller klasser i et datasett.

<div style="width:100px; height:100px; background-color:rgba(179, 226, 205, 1);"></div>
`rgba(179, 226, 205, 1)`

<div style="width:100px; height:100px; background-color:rgba(253, 205, 172, 1);"></div>
`rgba(253, 205, 172, 1)`

<div style="width:100px; height:100px; background-color:rgba(203, 213, 232, 1);"></div>
`rgba(203, 213, 232, 1)`

<div style="width:100px; height:100px; background-color:rgba(244, 202, 228, 1);"></div>
`rgba(244, 202, 228, 1)`

<div style="width:100px; height:100px; background-color:rgba(230, 245, 201, 1);"></div>
`rgba(230, 245, 201, 1)`

<div style="width:100px; height:100px; background-color:rgba(255, 242, 174, 1);"></div>
`rgba(255, 242, 174, 1)`

<div style="width:100px; height:100px; background-color:rgba(241, 226, 204, 1);"></div>
`rgba(241, 226, 204, 1)`

<div style="width:100px; height:100px; background-color:rgba(204, 204, 204, 1);"></div>
`rgba(204, 204, 204, 1)`
