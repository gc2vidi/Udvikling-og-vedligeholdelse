# [2]: Embed kort med liste over vector features

## 1. Motivation
Med `embed.js` kan der indlejres et Vidi kort i en hvilken som helst hjemmeside. I mange tilfælde er det ønskelig at have et kort og en medfølgende liste. F.eks. hvis man ønsker at vise et kort over børnehaver i kommunen med tilhørende liste over børnehavernes navne, adresser og kontaktoplysninger. Den nye lovgivning ang. tilgængelighed på offentlige hjemmesider bestemmer også, at et kort ikke kan stå alene, når formålet er navigation – i dette tilfælde finde ud af hvor børnehaverne er placeret.

Nedenfor ses et eksempel på et kort med liste. Eksemplet viser rammeområder med tilhørende liste.
![](https://d3dehtdmp2rwcw.cloudfront.net/ms_269878/5Q5j0VZAuTgzgWMSPWbt4FI2C9jE5n/Glostrup%2B%2BRammer%2Bfor%2Blokalplanl%25C3%25A6gningen%2B2020-06-10%2B12-54-43.png?Expires=1591786800&Signature=Skm5I553TQAyD4VClPZ7KVV5RMHi80m2cza9e7cOHViJcSxKITxoIF-ZBD9jpiSzLulAHYZS3p70Cappu8FP8pqBnFRvm6t9~5JU2~OopC1VmMEPjOtOW3ibPhFBDq5cmStnJxH3Ezbzm7hjufWWIUfTPbuenl5VCK~T~jXw~kTDHBeY~X9JDMOmdLs8uVNLzUkjmfpq8Q19R8rrBUCSFhxLrMUo2YgX7K-1EMaDoC2n114rdwvh7T7rVxlQje69TLj-hes2o95QGr8ipxMUzIMjsL4sYfzwkocOEX0ELPkNhHnNEiN-I4fpQ3zZu380iof5kAq7-DQc0bFjwYwrCA__&Key-Pair-Id=APKAJBCGYQYURKHBGCOA)

## 2. Foreslået løsning
Når man indsætter et kort med `embed.js` skal det være muligt at angive et lag, som skal vises i en tilhørende liste. Laget, som også skal vises i listeform, skal være med i projektet som vektorlag. 

Vidi eksisterende liste-modul skal anvendes. Nedenfor ses liste-modulet:

![](https://d3dehtdmp2rwcw.cloudfront.net/ms_269878/xNQcVdgIDn3olPO2Dr9IlqCZ1qLPf3/MapCentia%2BVidi%2B2020-06-10%2B21-25-58.png?Expires=1591817400&Signature=E9FEWIKh9v7mZ-Wwr1erfEHWQltpAHD2Ic7zqpeZCnYaAOhMe31mT9LyC35YJqHGCbgN2YuHQOPXOC4GE6qLizjcOoXBOrzvigv9Wl~eEXptE5Zs90tIX80AvJ-MYVK0-cDMyNsxbyk9ELYrD92wJutn4~ESh8nCtihsDWabVZ2JiW4CojGMk4pYKMWvRufpL0v8VJwy7Geu3KJIckfeD-F4a3PwyrnzPix73Wa1X5JfgMk8dCbVUwRvdBPFUqPdkBLSj0qwDTTSpr-c4sZgiz5bDLMDB9QIGWk4W0wkIcUL7zmm0yG~9HvD15a4C0h-bvvNKE6owEqCCXUSb3y5cQ__&Key-Pair-Id=APKAJBCGYQYURKHBGCOA)

**Forbedrings ønsker:**

Listen bør blive slået fra når laget slukkes, så den forsvinder fra brugerfladen. Og så skal det komme frem igen når laget tændes igen. Alternativt kan det gøres konfigurerbart, så der er i meta er en checkbox: "Tabel/Liste slukkes sammen med laget." Det kan evt. også udføres ved at der laves en "fold tabel ind" knap i brugerfladen.

Der skal i meta kunnne angives en bredde af listen, felt med bredde i %.

Der skal i meta kunne angives en transparens for tabellen, så man kan se kortet under tabellen.

## 3. Problemer med bagudkompatibilitet
Ingen.

## 4. Sikkerhedsmæssige implikationer
Ingen.

## 5. Performance-implikationer
Ingen.

## 6. Dokumentationsbehov
Dokumentationen er udvides med den nye funktion.

## 7. Arbejdsnoter

## 8. Issue tracker

## 9. Tilslutning til udviklingsønske
Interessen tilgendegives ved at skrive kundenavn og angive + for interesse og ++ for deltagelse i financieringen.

GeoFyn++  
MapCentia ++  
