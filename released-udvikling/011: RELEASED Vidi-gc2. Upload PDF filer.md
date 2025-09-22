# [11]: Vidi-gc2. Upload PDF filer

## 1. Motivation

På nuværende tidspunkt, kan der kun uploades billeder, der er behov for også at kunne uploade PDF eller andre filer i Vidi. De skule så også også kunne downloades fra info boksen i vidi bagefter. Det vil give mulighed for eks. at gemme vejledninger olign. på objekter.

## 2. Foreslået løsning  
Tilføj muligheden for upload af PDF og adnre filer, det vil sikkert også kræve tilpasninger af GC2. Tilføjelse af pdf som type på feltniveau, kan så bruges på bytea felttyper som billeder og video.

Der er fundet en løsning, som ikke kræver ændringer til GC2, da Vidi aflæser filens MIME type (filtype) og anvender denne til at bestemme hvordan feltet i både editor, feature-info og tabel skal skabes.   
Derved kan der uploades alle typer af filer til et "bytea" felt. Vidi indholder en liste over image MIME types og applikation MIME types. Disse MIME types er dem, som en browser (typisk) kan vise/indlejre i en web-app. Hvis en filtype ikke findes på listen, vil der vises en boks med et link til download af filen.   

Det skal bemærkes, at det kan være, at ikke alle browsere kan vise alle listens filformater. Fx er Word og Open Document på listen, men det kræver en udvidelse til browseren (som typisk er findes på Windows PC'ere)

Her ses en uploaded PDF:
![image](https://github.com/gc2vidi/Udvikling-og-vedligeholdelse/assets/3850918/4436a5a7-1a58-4dc8-8e02-78e8e1958e5c)


Her ses med en Excel fil, som ikke kan vises:
![image](https://github.com/gc2vidi/Udvikling-og-vedligeholdelse/assets/3850918/36aebe17-7be7-4dbc-b2ff-3d1b36d560fd)

Når der anvendes et bytea felt skal GC2 struktur feltet "Indhold" ikke sættes eller sættes til "Plain", da Vidi selv finder ud af indholdet. Hvis "Indhold" sættes, vil dette overrule filens MIME type og dette kan skabe fejl (fx hvis den sættes til "Image" og der en PDF i feltet).    

Filens navn er en ikke en del af indholdet i filen, så når filen downloades vil den have et standard navn. Dog bestemmes filnavnets extension ud fra MIME typen, så fx et PDF filnavn vil få extension .pdf.

## 3. Problemer med bagudkompatibilitet
Ingen

## 4. Sikkerhedsmæssige implikationer
Ingen

## 5. Performance-implikationer
Ved at åbne op for alle type filer, kan der uploades store filer (fx videoer). Da filerne bliver base64 encoded i browseren kan store filer få browseren til at crache. Derfor er der indledningsvis sat en max filstørrelse på 5MB.

## 6. Dokumentationsbehov
GC2 "Indhold" option skal dokumenteres jf. ovenstående. Listen af understøttede MIME types skal være tilgængelig.

## 7. Arbejdsnoter
Her findes listen over MIME types: https://github.com/mapcentia/vidi/blob/bootstrap5/browser/modules/constants.js

## 8. Issue tracker

## 9. Tilslutning til udviklingsønske
Interessen tilgendegives ved at skrive kundenavn og angive + for interesse og ++ for deltagelse i financieringen.

GEOsmeden ++

