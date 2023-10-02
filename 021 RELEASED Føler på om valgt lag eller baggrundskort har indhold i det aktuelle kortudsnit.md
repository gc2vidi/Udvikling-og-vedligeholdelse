# [21]: Føler på om valgt lag eller baggrundskort har indhold i det aktuelle kortudsnit

## 1. Motivation
I dag er der ikke en funktionalitet, som giver mulighed for at gøre brugeren opmærksom på, at det lag eller baggrundskort der netop er valgt ikke har et indhold i det aktuelle kortvindue.
Konsekvensen er, at brugeren kan få en fornemmelse af, at løsningen fejler.

## 2. Foreslået løsning
Det foreslås, at der for lag og baggrundskort skal kunne slås en funktion til fx i Meta, som man håndterer, at en bruger - når denne tænder for et baggrundskort (fx et ikke kommune-dækkende luftfoto) eller lag bliver informeret om, at "Det valgte lag/baggrundskort har intet indhold i det aktuelle kortudsnit". 

Det kan evt. implementeres ved:
- At der vises en midlertidig tekstboks med informationen.
- At lagkontrollen er dynamisk, når der zoomes ind, så baggrundskort eller lag, som ikke har indhold i det aktuelle kortudsnit ikke vises. 

## 3. Problemer med bagudkompatibilitet
Ingen.   

## 4. Sikkerhedsmæssige implikationer
Ingen.   

## 5. Performance-implikationer
Ingen.   

## 6. Dokumentationsbehov
Skal dokumenteres på https://geocloud2.readthedocs.io/da/latest/

## 7. Arbejdsnoter

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse
Geo Fyn ++
