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

<div style="width:100px; height:100px; background-color:#FF0000;"></div>
`#FF0000` - Rød

<div style="width:100px; height:100px; background-color:#FF7F00;"></div>
`#FF7F00` - Oransje

<div style="width:100px; height:100px; background-color:#FFFF00;"></div>
`#FFFF00` - Gul

<div style="width:100px; height:100px; background-color:#00FF00;"></div>
`#00FF00` - Grønn

<div style="width:100px; height:100px; background-color:#0000FF;"></div>
`#0000FF` - Blå

<div style="width:100px; height:100px; background-color:#4B0082;"></div>
`#4B0082` - Indigo

<div style="width:100px; height:100px; background-color:#8B00FF;"></div>
`#8B00FF` - Fiolett

### Sekvensiell palett - gul-grønn-blå
Egnet til: Visning av data som har en naturlig rekkefølge, for eksempel fra lav til høy verdi

<div style="width:100px; height:100px; background-color:#FFFFCC;"></div>
`#FFFFCC`

<div style="width:100px; height:100px; background-color:#C7E9B4;"></div>
`#C7E9B4`

<div style="width:100px; height:100px; background-color:#7FCDBB;"></div>
`#7FCDBB`

<div style="width:100px; height:100px; background-color:#41B6C4;"></div>
`#41B6C4`

<div style="width:100px; height:100px; background-color:#2C7FB8;"></div>
`#2C7FB8`

### Sekvensiell palett: Lilla til rød
Egnet til: Data med en naturlig progresjon, for eksempel intensitet av fenomen, eks. populasjonstetthet, bygningshøyder, vanntemperatur

<div style="width:100px; height:100px; background-color:#F7F4F9;"></div>
`#F7F4F9`

<div style="width:100px; height:100px; background-color:#E7E1EF;"></div>
`#E7E1EF`

<div style="width:100px; height:100px; background-color:#D4B9DA;"></div>
`#D4B9DA`

<div style="width:100px; height:100px; background-color:#C994C7;"></div>
`#C994C7`

<div style="width:100px; height:100px; background-color:#DF65B0;"></div>
`#DF65B0`

### Divergerende palett: Rød til blå
Egnet til: Visualisering av data som går fra én ekstrem til en annen, f.eks. temperaturavvik eller politiske målinger.

<div style="width:100px; height:100px; background-color:#67001F;"></div>
`#67001F` - Rød

<div style="width:100px; height:100px; background-color:#B2182B;"></div>
`#B2182B`

<div style="width:100px; height:100px; background-color:#D6604D;"></div>
`#D6604D`

<div style="width:100px; height:100px; background-color:#F4A582;"></div>
`#F4A582`

<div style="width:100px; height:100px; background-color:#FDDBC7;"></div>
`#FDDBC7`

<div style="width:100px; height:100px; background-color:#D1E5F0;"></div>
`#D1E5F0`

<div style="width:100px; height:100px; background-color:#92C5DE;"></div>
`#92C5DE`

<div style="width:100px; height:100px; background-color:#4393C3;"></div>
`#4393C3`

<div style="width:100px; height:100px; background-color:#2166AC;"></div>
`#2166AC`

<div style="width:100px; height:100px; background-color:#053061;"></div>
`#053061` - Blå

### Kvalitativ palett: Myke pastellfarger
Egnet til: Visualisering av kategoriske data som har lik vekt, f.eks. ulike grupper eller klasser i et datasett.

<div style="width:100px; height:100px; background-color:#B3E2CD;"></div>
`#B3E2CD`

<div style="width:100px; height:100px; background-color:#FDCDAC;"></div>
`#FDCDAC`

<div style="width:100px; height:100px; background-color:#CBD5E8;"></div>
`#CBD5E8`

<div style="width:100px; height:100px; background-color:#F4CAE4;"></div>
`#F4CAE4`

<div style="width:100px; height:100px; background-color:#E6F5C9;"></div>
`#E6F5C9`

<div style="width:100px; height:100px; background-color:#FFF2AE;"></div>
`#FFF2AE`

<div style="width:100px; height:100px; background-color:#F1E2CC;"></div>
`#F1E2CC`

<div style="width:100px; height:100px; background-color:#CCCCCC;"></div>
`#CCCCCC`