# [27]: Mulighed for central vedligehold af baggrundskort

## 1. Motivation

På nuværende tidspunkt skal baggrundskort vedligeholdes i konfigurationer. 
Når man efterhånden får mange konfigurationer, så er det en ret omstændelig opgave, at skulle åbne alle konfigurationer for at vedligholde baggrundskort når der f.eks. kommer ny ortofotos.

## 2. Foreslået løsning

Mulighed for at have en liste af baggrundskort som ligger udenfor konfigurationer, men kan hentes af konfigurationer. Gerne mulighed for flere lister, det er ikke altid ønskeliget med de samme baggrundskort i alle konfigurationer.

Dette bør kunne gøre med JSON Reference. Det er noget, som skal processeres i Node, men css filerne bliver allerede hentet gennem Node.

Der kan defineres i JSON fil med en række baselayers opsaetninger:

```json
{
  "opsaetning1":[
    {
      "type": "wms",
      "url": "https://api.dataforsyningen.dk/forvaltning2?token=eaca82e1cb411d78e841c7eba8ec1bbc",
      "layers": [
          "Basis_kort",
          "Stednavne_basiskort",
          "Husnummer"
      ],
      "id": "Basis_kort",
      "name": "Basis kort"
    },
    {
      "type": "gc2",
      "id": "luftfotoserier.geodanmark_2020_12_5cm",
      "name": "Luftfoto 2020",
      "db": "baselayers",
      "host": "https://dk.gc2.io"
    }
  ]
}
````

Det er så muligt at hentet den ind i config'en således:

```json
{
  "schemata": [
        "extent",
        "tag:udgivet"
  ],
  "baseLayers": {"$ref": "https://....#/opsaetning1"},
}
````

## 3. Problemer med bagudkompatibilitet

## 4. Sikkerhedsmæssige implikationer

## 5. Performance-implikationer

## 6. Dokumentationsbehov

Er dokumenteret her: 027: RELEASED Mulighed for central vedligehold af baggrundskort.md 

## 7. Arbejdsnoter

[https://github.com/vivocha/jsonref](https://github.com/whitlockjc/json-refs)

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse

GEOsmeden++  
Kerteminde++
