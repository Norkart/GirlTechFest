*TODO*
* Lage codepen-startpunkt
* Lage codepen-jukselapp for 2D-kart og 3D-kartet
* Printing - hvordan? 
* "laste ned zip-fil" - noe vits?
* Full gjennomtesting av opplegget

# GirlTechFest
Opplegg for GirlTechFest i Kristiansand

Nå skal du lære hvordan kart på web fungerer. Du skal lage ditt eget kart med dine egne farger. Kanskje får du til å lage et 3D-kart også!

Vi skal jobbe i nettleseren. Oppgavene ligger under. Følg oppgavene steg for steg. Husk å lese oppgavene nøye. Programmering må være helt nøyaktig og riktig for at datamaskinen skal skjønne det. Spør en av veilederne hvis du står fast. 

# Lag ditt eget kart!

## Oppgave1: Lag ditt eget kart
I denne oppgaven skal du sette opp webkartet og sette startpunktet til skolen din.

Vi skal bruke en kode-editor i nettleseren som heter CodePen. Gå inn linken her for å åpne første oppgave [LINK]. Det skal se omtrent slik ut:
![alt text](image.png)

Startpunktet for kartet er satt i kode-linjen:
```
center: [7.995611, 58.146722], 
```

Dette er koordinater i grader [ØST, NORD]. Under er en del koordinater for skoler i Kristiansand
```
center: [EE, NN],  // Fagerholt skole
center: [EE, NN],  // International School of Kristiansand
center: [EE, NN],  // Lovisenlund skole
center: [EE, NN],  // Wilds Minne skole
center: [EE, NN],  // Todda
```

Bytt ut senterpunktet til din egen skole! Kan du endre zoom-nivå også?

## Oppgave2: Bytt stil på kartet
Nå skal vi endre på designen til kartet. Det kan vi enkelt gjøre ved å bruke design og data som andre har laget for oss. 

Datagrunnlaget og designen (kartografien) hentes i denne linjen
```
style: 'https://api.maptiler.com/maps/basic/style.json?key=2Gpu1OQBPRJaorLakLSs', 
```
Her er en liste med flere forskjellige ferdig-stiler. Bytt ut og test de forskjellige. Husk at du bare kan ha 1 stil av gangen. 

```
style: 'https://api.maptiler.com/maps/dataviz/style.json?key=2Gpu1OQBPRJaorLakLSs',

style: 'https://api.maptiler.com/maps/aquarelle/style.json?key=2Gpu1OQBPRJaorLakLSs',

style: 'https://api.maptiler.com/maps/toner-v2/style.json?key=2Gpu1OQBPRJaorLakLSs',

style: 'https://api.maptiler.com/maps/outdoor-v2/style.json?key=2Gpu1OQBPRJaorLakLSs',

```
_For å bruke ferdig-stiler fra MapTiler må du ha en egen nøkkel. Vi har lagd ferdig en gratis-nøkkel som brukes på GirlTechFest. Den vil dessverre ikke fungere etter festen. Men du kan lage din egen gratisnøkkel på https://www.maptiler.com/_

## Oppgave4: Fargelegg kartet ditt
Kartet du har lagd fargelegges direkte i nettleseren. Det betyr at vi kan endre på designen til de delene av kartet vi bestemmer. 

Vi kan bestemme fargen til ulike datasett ved å legge til koden under. Her bestemmer vi fargen til ulike datalag, fks "building" blir til "rgba(100,0,0,0.7)". rgba er en måte å fortelle datamaskinen om farge: Red Green Blue og Alpha. Nummeret er et tall mellom 0 og 100 - og forteller _hvor mye_ av hver farge det skal være. Alpha er mellom 0.0 og 1.0 og forteller hvor stor _prosent_ gjennomsiktighet det skal være. Noen farger kan du også skrive på engelsk (_pink, red, green_). Helt nederst i dokumentet er det en liste med mange ulike farger og mer teori om farger i kart.

1. Kopier koden under og lim den inn på en ny linje etter _linje 42_. 
2. Prøv ulike farger på de ulike datalagene

```javascript
let veifarge = 'green';
map.on('load', function () {
    map.setPaintProperty('building', 'fill-color', 'rgba(100,0,0,0.7)'); // Bygninger
    map.setPaintProperty('water', 'fill-color', 'rgba(1,0,0,0.8)'); // Vann
    map.setPaintProperty('landcover', 'fill-color', 'red'); // Skog

    map.setPaintProperty('road_minor', 'line-color', veifarge); // Veier
    map.setPaintProperty('road_major', 'line-color', veifarge); // Veier
    map.setPaintProperty('road_tunnel', 'line-color', veifarge); // Veier
    map.setPaintProperty('road_motorway', 'line-color', veifarge); // Veier
    map.setPaintProperty('bridge', 'line-color', veifarge); // Veier
    
    map.setPaintProperty('railway', 'line-color', 'pink'); // Veier

});
``` 

# Lag et 3D-kart!
Til nå har vi bare sett kartet rett ovenfra i 2D. Kartdata er ofte 3D-data. Nå skal vi se kartet i perspektiv og sette 3D-høyder på datalagene.

## Oppgave1: Vis kartet i 3D
Først må vi bytte tilbake til den ferdige "basic"-stylen for kartet.
Endre tilbake til denne linjen helt i starten av koden din
```
style: 'https://api.maptiler.com/maps/basic/style.json?key=2Gpu1OQBPRJaorLakLSs', 
```

For å vise perspektiv (3D) så må vi tilte og vri kartet. Det gjør vi rett under der du satt senterpunktet til kartet. Vi legger til "pitch" og "bearing" for å få dette til. Legg til "pitch: 60," og "bearing: -60," i koden din rett under "center"-linjen. Det skal se cirka slik ut:

```javascript
var map = new maplibregl.Map({
    container: 'map', // ID til elementet der kartet skal vises
    style: 'https://api.maptiler.com/maps/basic/style.json?key=2Gpu1OQBPRJaorLakLSs', // Grunnleggende MapTiler stil
    center: [7.995611, 58.146722], // Kristiansand
    pitch: 60, // pitch in degrees
    bearing: -60, // bearing in degrees
    zoom: 15 // Zoomnivå
});
```
Nå kan du rotere og "vri" på kartet ved å trykke "ctrl" og museklikk i kartet. Du kan også bruke høyre-musetast og bevege deg rundt. 

![alt text](image-1.png)


## Oppgave2: Legg til 3D-visning av datalag
Nå skal vi få bygningene til å bli i 3D. Da må vi legge til et ekstra datalag og design (style). Denne koden legger du rett under koden der du bestemte farger. Hvis det krasjer - er det helt naturlig. Da kan du se på [jukselappen_3D_bygninger]

```javascript
// Legg til 3D-effekt (extrusion) for bygninger
map.addLayer({
    'id': '3d-buildings',
    'source': 'openmaptiles',
    'source-layer': 'building',
    'type': 'fill-extrusion',
    'paint': {
        'fill-extrusion-color': 'rgba(100,0,0,1)',
        'fill-extrusion-height':  ["*", ["get", "render_height"], 1],
        'fill-extrusion-opacity': 1.0
    }
});
```
Når du har fått inn bygningene i 3D. Prøv å endre på fargen! Klarer du å endre hvor høye bygningene blir skalert? (_tips: render_height. Bytt 1 med 5_)

## Oppgave3: La vannet bli høyere
Kartet trenger ikke bare vise det som er realistisk. Vi kan også legge til 3D-effekt på andre datalag. Nå skal vi legge til 3D-effekt på vannet(!). Da kan vi sette en fast høyde på vannet og se hva som skjer. Prøv deg frem med forskjellig opacity, color og height. Hva kan du bruke dette til? 

Legg til koden direkte under 3D-bygnings-koden din
```javascript
// Legg til 3D-effekt (extrusion) for vann
map.addLayer({
    'id': '3d-water',
    'source': 'openmaptiles',
    'source-layer': 'water',
    'type': 'fill-extrusion',
    'paint': {
        'fill-extrusion-color': 'silver',
        'fill-extrusion-height': 20, // Fast høyde for vann
        'fill-extrusion-base': 0,
        'fill-extrusion-opacity': 1
    }
});
```

## Ta et skjermbilde og skriv ut!
* Printscreen og print? 



# Teori og oppslag
## Webutvikling

Webutvikling handler om å lage nettsteder og applikasjoner som vi kan bruke på internett. Det er som å bygge et hus, der hver del har sin egen funksjon.

### 1. HTML (HyperText Markup Language)

HTML er grunnlaget for enhver nettside. Tenk på HTML som skjelettet til et hus. Den forteller nettleseren hva som skal vises på siden. For eksempel, hvis du vil ha en overskrift, bruker du HTML for å lage den. Du kan også bruke HTML til å sette inn tekst, bilder og lenker. Så når du besøker en nettside, er det HTML som forteller nettleseren hva den skal vise og hvor alt skal være.

### 2. CSS (Cascading Style Sheets)

Når skjelettet er bygget med HTML, er det tid for å pynte det. Det er her CSS kommer inn. CSS fungerer som maling og dekorasjoner for huset. Det bestemmer hvordan nettsiden ser ut, for eksempel hvilken farge bakgrunnen skal ha, hvilken skrifttype teksten skal bruke, og hvordan bilder skal plasseres. Med CSS kan du gjøre en nettside både fin og spennende å se på!

### 3. JavaScript

JavaScript gir liv til nettsiden. Tenk på det som lysene og bevegelsene i huset. Med JavaScript kan du lage interaktive funksjoner, som å vise en melding når du klikker på en knapp eller endre bildet som vises. Det gjør at nettsiden kan reagere på hva brukeren gjør. For eksempel, når du fyller ut et skjema, kan JavaScript hjelpe til med å sjekke om du har skrevet inn alt riktig før du sender det.

### Oppsummering

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
