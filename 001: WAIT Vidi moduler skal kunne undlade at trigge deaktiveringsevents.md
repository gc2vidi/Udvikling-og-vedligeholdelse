# [1]: Vidi moduler skal kunne undlade at trigge deaktiveringsevents

## 1. Motivation

Når der skiftes mellem moduler (lagtræ, baggrunds, tegning mv.) udløses en stop- og oprydningshandling som alle moduler lytter til. Det enkelte modul skal så sørge for at deaktivere og rydde op efter sig. Det betyder, at to eller flere moduler ikke kan være aktive på samme tid. Dette har gjort det mere enkelt at skrive moduler, da man ikke skal tage stilling til hvilke moduler, som ikke fungerer sammen ens eget module og derfor skal deaktiveres. Men det har den store ulempe, at hvis man fx laver en konfliktsøgning og gerne vil have skiftet baggrundskort, bliver konfliktsøgningen deativeret og nulstillet.   

## 2. Foreslået løsning
En række moduler skal beskrives som "passive". Dvs. at de ikke ændrer klik-i-kortet-handlingen eller aktiverer tegneværktøjer. Af standardmodulerne er det: Lagtræ, baggrundskort, signatur og projekter. Af extensions kan nævnes Koordinater.

På en eller måde skal passive moduler undertrykke stop- og oprydningshandlingen, der bliver udløst ved skift mellem moduler. Det er vigtigt, at denne undertrykkelse er placeret i modulets kode, således modul-forfatteren selv kan implementere undertrykkelsen. Handlingen (kaldet off:all) bliver udløst ved klikket på selve module-ikonet og ikke indefra modulet. Så der er intet kode i modulet, som har med off:all handlingen at gøre.

Her bliver der lyttet til off:all handlingen: https://github.com/mapcentia/vidi/blob/master/browser/modules/bindEvent.js#L510-L537

En mulig løsning er, at modulet placerer en data-attribute i "#side-panel ul li a", (fx data-no-off-event="true") således ovenstående kode kan læse denne og lade være med at udløse off:all

En ide er at vise en toast pop-up med en meddelse om at moduler bliver deaktiveret, når et "aktivt" module aktiveres.

## 3. Problemer med bagudkompatibilitet
Ingen hvad angår extensions eller GC2.

## 4. Sikkerhedsmæssige implikationer
Ingen.

## 5. Performance-implikationer
Ingen.

## 6. Dokumentationsbehov
Extension developer dokumentationen skal opdateres.

## 7. Arbejdsnoter

## 8. Issue tracker

## 9. Tilslutning til udviklingsønske
Interessen tilgendegives ved at skrive kundenavn og angive + for interesse og ++ for deltagelse i financieringen.

Geo Fyn ++  
Kerteminde +  
MapCentia ++
