# [19]: Resultatvisning som enkelt konfliktsøger

## 1. Motivation
I dag er det muligt i et VIDI-kort at søge sin adresse og matrikel i kortet og zoome til denne. Samtidig kan man lægge et eller flere lagtemaer i kortet, hvorved brugeren selv kan foretage en fortolkning af, om brugerens søgning er omfattet af lagtemaet og hvis temaet er kategoriseret, så også hvilken kategori, brugerens adresse/matrikel falder ind under. Samtidig er det muligt at lave en popup-infoboks eller en infoboks som mouse over, som så muliggør at brugeren kan få yderligere informationer om det lagtema, som kortet viser.   

Brugerens svar sker, som nævnt ved en fortolkning af kortet eller ved et ekstra klik (popup-infoboks). Det ville være mere hensigtmæssigt og elegant, hvis brugeren automatisk får svar på det der gælder for borgeren specifikt for det lagtema, der ønskes kommunikeret på hjemmesiden eller i kortet.   

En case kunne være, at en kommune under en side om lokalplanlægning på hjemmesiden, ønsker at muliggøre at borgeren ved en enkel søgning kan finde den lokalplan, som borgeren er omfattet og hurtig kunne lede borgeren videre til det relevante plandokument.   

Andre cases kunne være at hjælpe en seniorborger til at finde information om plejedistrikt og relevante info herom, eller søge distrikt i kommunens varmeplan og med link til energiselskabet i distriktet.

## 2. Foreslået løsning
At få udviklet en extension til VIDI, der muliggør, at fx en borger kan søge sin adresse eller matrikel i et søgefelt og automatisk få et svar på, hvad der for det enkelte tema, gælder for borgeren. Et eksempel kunne være, at en kommune ønsker, at borgeren skal kunne fremsøge, hvilken lokalplan som borgeren evt. er omfattet af.

Ved en søgning på borgerens adresse kunne et svar se ud som følger:

 

Som tabel:   
|Lokalplan|Anvendelse specifik|Link til dokument|
|---|---|---|
|L.116 - Hareskovby|Boligområde|[Link til lokalplan Hareskovby]()|

Som tekst:   
"Du er omfattet af lokalplan L.116 – Hareskovby. [Klik her for at se lokalplan]()."   

Svaret må gerne komme i relation til kortet, som automatisk zoomer til den lokalplan, som adressen eller matriklen intersecter med. Dette vil give svaret en ekstra dimension, i og med at borgeren kan se hele afgræsningen af lokalplanen og samtidig en marker for den adresse eller matrikel (måske centroide) som der er søgt med.

### Yderligere krav til løsningen

- Det skal være muligt, at borgeren kan få et svar som returnerer flere features fra samme lagtema, hvis adressen eller matriklen intersecter med flere features i lagtemaet.

- Svaret skal kunne bestå af sammensætninger af variable, baseret på forekomster i tabellen, samt egen tekst. Eksempel: ’Du er omfattet af lokalplan {{L.116}} – {{Hareskovby}}. Klik {{her}} for at se lokalplan’. Tuborgklammerne angiver steder hvor teksten er en variabel.

## 3. Problemer med bagudkompatibilitet

Ingen

## 4. Sikkerhedsmæssige implikationer

Ingen

## 5. Performance-implikationer

Ingen

## 6. Dokumentationsbehov

Skal dokumenteres

## 7. Arbejdsnoter

Kan laves som template + extension

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse
