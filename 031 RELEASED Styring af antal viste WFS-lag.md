# [31]: [Styring af antal viste WFS-lag]

## 1. Motivation

I dag vises alle tabeller, views og materialized views i WFS-tjenesterne, hvilket kan være uoverskueligt fx i QGIS.
Mange tabeller, views og materialized views kan være mellemregninger eller til internt brug.

## 2. Foreslået løsning

Det foreslås, at der i GC2 Admin gives mulighed for at angive at en tabel, view eller materialized view IKKE skal vises/distribueres.

Der tilføjes et OWS tjekboks i GC2 Admin. Hvis den ikke er tjekket af, vil laget ikke optræde i WFS/WMS. Som standard på nye lag er boksen tjekket af.

<img width="321" alt="image" src="https://github.com/gc2vidi/Udvikling-og-vedligeholdelse/assets/3850918/f5947598-2912-4f25-8be7-6f331b041ee6">

## 3. Problemer med bagudkompatibilitet
Ingen.

## 4. Sikkerhedsmæssige implikationer
Ingen.

## 5. Performance-implikationer
Ingen.

## 6. Dokumentationsbehov
Skal dokumenteres i manualen.

## 7. Arbejdsnoter
Er implementeret i Bullseye

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse
Geo Fyn ++   
Kerteminde ++   
