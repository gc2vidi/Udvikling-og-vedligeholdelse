# [10]: Embed-attribut til at slå cookies fra

## 1. Motivation
Der bliver mere og mere fokus på persondatapolitik og GDPR. Mange hjemmesider har indbygget en startformular, hvor brugeren angiver om man vil accepterer cookies helt, delvist eller udelukkende de mest essentielle. Vidi anvender cookies - både hvis en bruger logger ind (lille ikon med hængelås), så oprettes en session-cookie eller hvis brugeren opretter et projekt, uden at være logget ind, så oprettes en projekt-cookie. Dette er såkaldte "Funktionelle" cookies, som udelukkende har til formål at stille noget funktionalitet til rådighed for brugeren.

Men hvis et kort indlejres på en hjemmeside, hvor brugeren har mulighed for at afvise "Funktionelle" cookies, vil indlejrede vidikort kunne overtræde brugerens ikke-accept af disse cookies. Dette kan blive en showstopper i forhold til at bruge GC2 / Vidi på disse hjemmesider.

## 2. Foreslået løsning
Der indbygges en ny attribut i embed.js, der giver mulighed for at slå cookies fra f.eks. data-vidi-use-cookie="true"/"false", med default sat til "true".
Hvis attributten sættes til "false" sker følgende:
- brugerens mulighed for login og projekt-oprettelse disables og ikonerne fjernes fra brugerfladen
- der oprettes ikke en cookie i Vidi

## 3. Problemer med bagudkompatibilitet
Hvis defaultværdien er sat til "True", bør løsningen ikke give problemer med bagud-kompatibilitet

## 4. Sikkerhedsmæssige implikationer
Ingen

## 5. Performance-implikationer
Ingen

## 6. Dokumentationsbehov
Ja - men minimalt: beskrivelse af ny attribut i den eksisterende dokumentation af embed.js

## 7. Arbejdsnoter

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse
