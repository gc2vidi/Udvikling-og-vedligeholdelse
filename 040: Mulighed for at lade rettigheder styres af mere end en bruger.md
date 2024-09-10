# [40]: Mulighed for at lade rettigheder styres af mere end en bruger/rolle
## 1. Motivation

Man kan i øjeblikket sætte en bruger til at arve rettigheder fra en anden bruger. 

Det ville være en fordel, hvis man kan sætte en bruger til at arve rettigheder fra flere brugere. Det vil give muligheden for at arbejde mere struktureret med rettighedsstyring. Så kan man lave forskellige roller alt efter dataområde, og tildele en bruger en eller flere roller i systemet. Hvis der så kommer nye lag til i et område, så skal de bare tilføjes rollen, og de brugere der har den rolle vil så automatisk få redigeringsadgang.

## 2. Foreslået løsning
Kunne det laves således, at i stedet for at tjekke én nedarving, så loopes der igennem et array af tildelte roller og hvis en af dem giver lov til den ønskede request stoppes der og requesten udføres.   

På den måde skal der ikke laves om på den grundlæggende mekanik.

Jeg tænker det vil være en fin løsning. Det er mest for at få muligheden for at have flere roller til forskellige brugergruppe, som kan kombineres. Hvis der f.eks. er write rettighed til et lag i en af rollerne. Så får brugeren write rettighed til laget uanset hvad de andre tildelte roller har af rettigheder.

## 3. Problemer med bagudkompatibilitet

## 4. Sikkerhedsmæssige implikationer

## 5. Performance-implikationer

## 6. Dokumentationsbehov

## 7. Arbejdsnoter

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse
GEOsmeden ++  
MapCentia ++  
