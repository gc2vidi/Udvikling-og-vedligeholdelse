# [28]: Fuldskærm af embed kort indlejret i anden hjemmeside (IOS)

## 1. Motivation

Når der er indlejret et embed kort i en hjemmeside, så kan man på Android og PC bruge knappen fuldskærmsvisning. Men på IOS virker den funktionalitet ikke, der sker bare ingenting når man trykker på knappen.

## 2. Foreslået løsning

Den valgte metode er at tjekke om browser APIet document.documentElement.requestFullscreen er defineret. Hvis ikke, så vises knappen ikke. Er APIet ikke defineret kan browseren ikke gå i fuldskærm og det gør det ikke på IOS.   

Vi antager, at hvis APIet eksisterer, så virker det som forventet. Det er tjekket på IOS/Safari/Chrome og Android/Chrome.

## 3. Problemer med bagudkompatibilitet

Ingen.

## 4. Sikkerhedsmæssige implikationer

Ingen.

## 5. Performance-implikationer

Ingen.

## 6. Dokumentationsbehov

Ingen. Kan være, at det skal nævnes i manualen.

## 7. Arbejdsnoter

## 8. Issue tracker  

## 9. Tilsagn/tilkendegivelse

GEOsmeden ++
