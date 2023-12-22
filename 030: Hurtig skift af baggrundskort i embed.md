# [30]: Hurtig skift af baggrundskort i embed

## 1. Motivation

Det ville være rart hvis man kunne have mulighed for en simpel/hurtig skift af baggrundskort i embed. Det er efterhånden mange steder nærmest en standard, at have en knap, som kan skifte mellem baggrundskort uden at skulle åbne en menu. 

## 2. Foreslået løsning

Der laves en knap, som skifter mellem baggrundskort, som er mærket med f.eks. en quickacces parameter i configurationen, og der skiftes så imellem kortene i den rækkefølge de står i konfigurationen, så det ikke kun er begrænset til 2 man kan skifte imellem.

Det er lavet sådan, at der er to muligheder:
- En "toggle" knap, som toggler mellem de to første definerende baselayers i config.
- Og en "skuffe", hvorfra man vælge mellem et vilkårligt antal kort. Udvælgelsen sker med en ny property på de enkelte baselayer definitioner.

Kun én widget kan vises adgangen og ingen bliver vist i default.tmpl, som har en regel med `display:none` poå class `baselayer-tool`. Valg af widget sker ved brug af `baselayerDrawer:true|false` i config.

## 3. Problemer med bagudkompatibilitet
Ingen.

## 4. Sikkerhedsmæssige implikationer
Ingen.

## 5. Performance-implikationer
Ingen.

## 6. Dokumentationsbehov
Er dokumenteret her: 

## 7. Arbejdsnoter
<del>Er delvis implementeret, hvor de to øverste baselayers kan toggles.</del>

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse
GEOsmeden ++    
Geo Fyn ++
