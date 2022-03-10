# [13]: Optimering af QGIS projekter og upload af symboler og fonte

## 1. Motivation
Mange anvender QGIS Server integrationen i GC2, som giver muligheden for at opsætte projekter i QGIS Desktop og derefter genbruge projekterne  i GC2. Det virker sådant set fint, men der et par ting, som bør forbedres:

1. Store projekt-filer med mange layer definitions (QLR) kan reducere performance i QGIS Server. En løsning er, at brugeren opdeler sit projekt i mindre projekter. Men dette er besværligt og ofte bliver det ikke optimalt, da det ofte er er urealistisk at lave et projekt pr. lag. Derfor bør QGS filen opsplites automatisk i ét lag pr. QGS på serveren.
2. Symboler og fonte, som anvendes i et QGIS projekt skal også være på serveren. På GC2 serveren findes QGIS standard symboler (dem, som kommer med installationen af QGIS) samt de mest almindelige Windows truetype fonte. Men anvender man symboler og fonte ud over de nævnte, skal disse manuelt placeres på GC2 serveren, hvilket den almindelige bruger ikke er i stand til. Derfor bør brugeren kunne uploade symboler og fonte sammen med sin QGS fil.  

## 2. Foreslået løsning

## 3. Problemer med bagudkompatibilitet

## 4. Sikkerhedsmæssige implikationer

## 5. Performance-implikationer

## 6. Dokumentationsbehov

## 7. Arbejdsnoter

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse

## 10. Forfatter
Martin Høgh, MapCentia   

MapCentia++
