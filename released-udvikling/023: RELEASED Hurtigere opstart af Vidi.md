# [23]: Hurtigere opstart af Vidi 

## 1. Motivation
Vidi fjerner først load-screen (de dansende prikker) når alt er loadet - herunder lag, baggrundskort og lagtræ. Det kan tage lang tid og brugeren ved ikke rigtig
om den er gået i stå eller om start-processen stadig er i gang  

## 2. Foreslået løsning
Load-screen skal fjernes så snart koden er hentet og lag/lagtræ hentes i baggrunden. På den måde kan brugeren se, at der sker noget og kortet er interaktivt med
det samme. Lagttræet skal forsynes med et progress-bar, så brugeren kan se, at metadata afventes.

## 3. Problemer med bagudkompatibilitet
Umiddelbart ingen

## 4. Sikkerhedsmæssige implikationer
Ingen

## 5. Performance-implikationer
Forbedret opstartshastighed

## 6. Dokumentationsbehov
Ingen

## 7. Arbejdsnoter

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse
MapCentia++
