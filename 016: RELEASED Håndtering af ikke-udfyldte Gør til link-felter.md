# 016: Håndtering af ikke-udfyldte Gør til link-felter

## 1. Motivation
Det er i dag muligt at gøre et felts indhold (en URL) klikbar ved at sætte flueben ved "Gør til link".
Det fungerer fint, når feltet er udfyldt med en URL, MEN det fungerer ikke ved ikke-udfyldte felter.

## 2. Foreslået løsning
Det foreslås, at hvis feltet for et givent objekt ikke er udfyldt, så vises feltet ikke i info-boksen og vektor-tabel.   

Endvidere foreslås det, at der tilføjes en ny felt-egenskab kaldet 'Template' hvori, der kan angives en mustache template, som bliver rendered i pop-up/tabel i stedet for den rå værdi. Derved kan der dannes links med link-tekst samt title og aria-label attributter, der indeholder værdier fra andre felter. Dette er nødvending for at danne links, som lever op til konventionerne for best-practice og tilgængelighed. En link-template for fx lokalplaner kunne se således ud:    

```html
<a href="{{doklink}}" target="_blank" title="Link til lokalplan {{plannavn}} {{plannr}} som pdf" aria-label="Link til lokalplan {{plannavn}} {{plannr}} som pdf">{{plannr}} {{plannavn}}</a>
```

## 3. Problemer med bagudkompatibilitet
Ingen

## 4. Sikkerhedsmæssige implikationer
Ingen

## 5. Performance-implikationer
Ingen

## 6. Dokumentationsbehov
Dokumentation: https://vidi.readthedocs.io/da/latest/pages/standard/92_gc2_meta_information.html#template

## 7. Arbejdsnoter
Ingen

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse
Geo Fyn ++

Kerteminde ++
