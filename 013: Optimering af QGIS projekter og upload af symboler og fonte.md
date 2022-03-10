# [13]: Optimering af QGIS projekter og upload af symboler og fonte

## 1. Motivation
Mange anvender QGIS Server integrationen i GC2, som giver muligheden for at opsætte projekter i QGIS Desktop og derefter genbruge projekterne  i GC2. Det virker sådant set fint, men der et par ting, som bør forbedres:

1. Store projekt-filer med mange layer definitions (QLR) kan reducere performance i QGIS Server. En løsning er, at brugeren opdeler sit projekt i mindre projekter. Men dette er besværligt og ofte bliver det ikke optimalt, da det ofte er er urealistisk at lave et projekt pr. lag. Derfor bør QGS filen opsplites automatisk i ét lag pr. QGS på serveren.
2. Symboler og fonte, som anvendes i et QGIS projekt skal også være på serveren. På GC2 serveren findes QGIS standard symboler (dem, som kommer med installationen af QGIS) samt de mest almindelige Windows truetype fonte. Men anvender man symboler og fonte ud over de nævnte, skal disse manuelt placeres på GC2 serveren, hvilket den almindelige bruger ikke er i stand til. Derfor bør brugeren kunne uploade symboler og fonte sammen med sin QGS fil.  

## 2. Foreslået løsning
1. Der indsættes en funktion før QGS filen parses i GC2. Funktionen opsplitter QGS filen i flere og sender videre til parse-funktionen. Derved skal der ikke laves noget om i sidste nævnte funktion. Der skal dog tages hånd om composite layers, som anvender den samlede QGS file.
2. Der skal kunne vælges truetype font-filer og svg-filer i QGIS upload i GC2 Admin. På serveren placeres uploadede font-filer i `/app/wms/fonts`. Symboler er lidt mere besværlige, da symbol-folderen ikke kan bruger-defineres i QGIS Server. I GC2 findes den i `/usr/share/qgis/svg`, så uploadede symboler skal placeres her. I QGS filen er path til svg-filer relativ, men ofte vil man i QGIS Desktop placere sine symboler i underfoldere. Fx hvis man henter Mapbox Maki symboler, vil man lægge dem i en folder fx kaldet `mapbox-maki`. I QGS-filen vil den relative sti fremgå således: ```<prop v="mapbox-maki/animal-shelter.svg" k="name"/>```. Så på GC2 serveren skal folder-strukturen også have denne underfolder: `/usr/share/qgis/svg/mapbox-maki`. Udfordringen er at oprette folderen `mapbox-maki` på serveren og få placeret svg-filerne her i. En måde er, at brugeren pakker folderen i en zip-fil og uploader, på serveren udpakkes filen og underfolderen skabes. En anden måde er, at brugeren embeder svg-symboler i projektet, så upload helt undgås. Her skal performance dog tjekkes mellem embedning og ikke. 

## 3. Problemer med bagudkompatibilitet
For 1 vil vil der ikke være problemer med eksisterende QGIS lag. Dog skal QGS filer gen-uploades for, at opdelingen sker. For 2 vil font upload ikke have nogen konsekvenser, da font-folderen allerede er et Docker volume og vil persist ved re-deployment. Symboler findes ikke i et volume og der skal foretages en migration. En løsning vil være at placere svg folderen i `app/wms/svg` og symlinke til `/usr/share/qgis/svg`. Derved bliver svg-fileren en del af GC2 installationen.

## 4. Sikkerhedsmæssige implikationer
Ingen

## 5. Performance-implikationer
Vil skabe bedre performance i QGIS lag.

## 6. Dokumentationsbehov
Skal dokumenteres i GC2 vejledningen.

## 7. Arbejdsnoter

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse
MapCentia++

## Forfatter
Martin Høgh, MapCentia   

