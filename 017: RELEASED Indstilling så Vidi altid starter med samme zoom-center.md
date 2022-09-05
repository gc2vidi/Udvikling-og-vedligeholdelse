# [017]: Indstilling så Vidi altid starter med samme zoom/center

## 1. Motivation
En config styrer zoom/center på Vidi, så hvis man har flere configs, der skal starte med nøjagtig samme zoom/center skal man være påpasselig med at sætte kortets zoom og center, så de alle er ens. Det er kan være besværligt, så det foreslås, at der laves en indstilling i config, der sætter start zoom/center.

## 2. Foreslået løsning
Der laves en ny indstilling kaldet `initZoomCenter` der indeholder z, x og y, der svarer til det, der ses i URL ankeret. Noget lignede `/15/9.5389/56.5799/`. Vidi vil med denne indstilling i config altid starte med denne zoom/center. Ved embedding på hjemmesider vil knappen, der sætter default zoom/center bruge indstillingen, således brugeroplevelsen er ens med og uden brug af indstillingen.

## 3. Problemer med bagudkompatibilitet
Ingen.

## 4. Sikkerhedsmæssige implikationer
Ingen.

## 5. Performance-implikationer
Ingen.

## 6. Dokumentationsbehov
Skal dokumenteres. https://vidi.readthedocs.io/da/latest/pages/standard/91_run_configuration.html#initzoomcenter

## 7. Arbejdsnoter

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse
MapCentia+   
Fureø Kommune+

