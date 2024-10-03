# GirlTechFest
Opplegg for GirlTechFest i Kristiansand

* Om webutvikling. client/server
* Kart på web
    * Vector tiles
* Kartografi
* Design og UU

* Lag ditt eget kart! 
    * Bytt stil på kartet
        * Basis, datascience, aquarell,  school map
    * Flytt center til skolen din
    * Endre på zoom-nivået
    * Fargelegg med dine farger!
    * Ta inn / ut ulike datalag
        * Liste med aktuelle datalag
            * bygninger, vann, m.m.
    * (??) Ta inn andre data fra andre kilder (geojson)
    * (??) Klikk i kartet
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
