# 041: Mulighed for at anvende vektortiles som baggrundskort
1. Motivation

Skærmkort kommer som vektor tiles. Samt kan man anvendes OSM tiles fra MapTiler og egne bagrundskort.

2. Foreslået løsning

MapLibre implementeres i Vidi gennem Leaflet/MapLibre bindingen, så vektortiles og styling json kan anvendes.

3. Problemer med bagudkompatibilitet

Print kan blive et problem da MapLibre anvende WebGL, som kræver adgang til en GPU. Det kan være, at en software GPU kan løse problemet.    

4. Sikkerhedsmæssige implikationer
5. Performance-implikationer
6. Dokumentationsbehov
7. Arbejdsnoter
8. Issue tracker
9. Tilsagn/tilkendegivelse
GEOsmeden ++
MapCentia ++
