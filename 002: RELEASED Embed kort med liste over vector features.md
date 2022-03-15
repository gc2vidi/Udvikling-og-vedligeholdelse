# [2]: Embed kort med liste over vector features

## 1. Motivation
Med `embed.js` kan der indlejres et Vidi kort i en hvilken som helst hjemmeside. I mange tilfælde er det ønskelig at have et kort og en medfølgende liste. F.eks. hvis man ønsker at vise et kort over børnehaver i kommunen med tilhørende liste over børnehavernes navne, adresser og kontaktoplysninger. Den nye lovgivning ang. tilgængelighed på offentlige hjemmesider bestemmer også, at et kort ikke kan stå alene, når formålet er navigation – i dette tilfælde finde ud af hvor børnehaverne er placeret.

## 2. Foreslået løsning
Når man indsætter et kort med `embed.js` skal det være muligt at angive et lag, som skal vises i en tilhørende liste. Laget, som også skal vises i listeform, skal være med i projektet som vektorlag. 

**Forbedrings ønsker:**

Listen bør blive slået fra når laget slukkes, så den forsvinder fra brugerfladen. Og så skal den komme frem igen når laget tændes igen. Alternativt kan det gøres konfigurerbart, så der er i meta er en checkbox: "Tabel/Liste slukkes sammen med laget." Det kan evt. også udføres ved at der laves en "fold tabel ind" knap i brugerfladen.

Der skal i meta kunnne angives en bredde af listen, felt med bredde i %.

Der skal i meta kunne angives en transparens for tabellen, så man kan se kortet under tabellen.

**Kommentarer**
Ang. transparens så ligger tabellen ikke ovenpå kortet, men pladsen bliver fordelt mellem kort og liste. Det vil være sværere at placere listen ovenpå kortet, da den i såfald vil skjule kort-navigations-knapperne.

Bredde/højde styres i config og ikke i Meta.

## 3. Problemer med bagudkompatibilitet
Ingen.

## 4. Sikkerhedsmæssige implikationer
Ingen.

## 5. Performance-implikationer
Ingen.

## 6. Dokumentationsbehov
Er dokumenteret: https://vidi.readthedocs.io/da/latest/pages/standard/91_run_configuration.html#vectortable

## 7. Arbejdsnoter

## 8. Issue tracker

## 9. Tilslutning til udviklingsønske
Interessen tilgendegives ved at skrive kundenavn og angive + for interesse og ++ for deltagelse i financieringen.

GeoFyn++  
MapCentia ++  
Kerteminde ++
