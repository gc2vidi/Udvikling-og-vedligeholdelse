# [9]: Up- og download funktionalitet i Vidi

## 1. Motivation
Igennem GeoDanmark GeoFA projektet, som anvender GC2/Vidi, er der blevet udviklet ny funktionalitet.
Blandt andet er det muligt let at uploade- og downloade data i Csv, GML, GeoJSON, Geopackages, Shp og Tab, hvilket uden de store omkostninger bør kunne implementeres i Vidi.
Ligeledes er der udviklet en mulighed for at tilknytte et eller flere fotos til objekter, herunder angive primær-foto og copyright oplysninger. Dette er større og vil kræve en udredning.

## 2. Foreslået løsning
Der laves en extension til Vidi, som gør det muligt at trække filer ind i et upload felt. Det kan enten være en zip-file med mange filsæt (også i undermapper) 
eller en enkelt fil (fx en GeoPackages, eller en Shape-file med sidecar files). Funktionaliteten tages fra GeoFA editoren.

Uploadede filer importeres i databasen og tilføjes lagtræet i en "Upload" gruppe. Minimal opsætning sker automatisk, så lag kan ses og klikkes på.

Filer importeres til et dertil oprette schema og gives et unikt navn. Brugeren kan gemmes lagtræet i et projekt, så der kan vendes tilbage til lagene eller opsætningen kan deles med andre.

Hvis man er logget ind som sub-user, kan man overveje om filer skal importeres ind i tilhørende schema og have "Read/write" sikring på.

## 3. Problemer med bagudkompatibilitet
Ingen.

## 4. Sikkerhedsmæssige implikationer
Ingen.

## 5. Performance-implikationer
Ingen.

## 6. Dokumentationsbehov
Skal dokumenteres i manualen.

## 7. Arbejdsnoter
Download af data er implementeret i Ny Vidi. Kan gøres fra lagtræet.

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse
Geo Fyn ++

