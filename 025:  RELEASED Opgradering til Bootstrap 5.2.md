# [25]:  Opgradering til Bootstrap 5.2

## 1. Motivation
Nu anvendes Bootstrap 3.4 med en tidlig version af MDB theme plus nogle andre projekter fx snackbar.js. Der er lavet en del css hacks og eksplicitte styles for at få ting til at se pæne ud. Dynamisk ændring af css gennem eksterne filer er derfor vanskeliggjort, da brugeren ikke blot kan se i Bootstrap dokumentationen, men skal bruge en web-inspector for at se hvordan regler er defineret.

## 2. Foreslået løsning
Opgradering til Bootstrap 5.2 (5.3, som nok når at blive klar) uden brug af 3. parts themes. Brug af Bootstrap css klasser i så vid udstrækning som muligt og undgå eksplicitte styles i HTML'en. Undgå brugen af custom widgets - fx brug offcanvas komponenten til modul-panel og attribut-dialog.

## 3. Problemer med bagudkompatibilitet
Kan give problemer med bruger-styles-sheets, som skal skrives om. Men det bliver meget lettere.

## 4. Sikkerhedsmæssige implikationer
Ingen.

## 5. Performance-implikationer
Ingen.

## 6. Dokumentationsbehov
Billeder af GUI elementer skal fornyes.

## 7. Arbejdsnoter

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse

MapCentia ++  

