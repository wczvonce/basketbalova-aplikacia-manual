# Aktualizácia manuálu BBALL – 30. 10. 2026

Porovnané posledné dva e-maily Petra Škantára k téme BBALL TEST – PPG a WATCH (Bendigo Ž : TOW): 29. 10. 2026 o 22:51 a 30. 10. 2026 o 11:33, čas Slovenska. Ide o dokumentovanie potvrdení vývojára, nie o audit novej aplikácie.

| Téma | Stav pred kontrolou | Úprava |
| --- | --- | --- |
| WATCH bez webových štatistík | Výnimka už v kapitole 5 bola | Doplnené potvrdenie: pri dostupných štatistikách všetky tri podmienky, bez nich iba X/Y |
| Dopočítané PPG | Výnimka bola opísaná technicky | Kapitoly 5, 29 a 30 výslovne hovoria, že sa nepoužíva na zaradenie medzi sledovaných |
| Dátum výpočtu PPG | Hranica 1. 8. 2026 už bola uvedená | Potvrdenie a príklad Sowah M.: jediný zápas v období s nulou bodov |
| História detailu | Nová úprava nebola uvedená | Kapitoly 27 a 30: od 1. 8. 2026 pre URL zápasov, posledné zápasy jednotlivých hráčov aj tímu |
| TOP/TOP2 bez štatistík | Septembrový audit uvádza X/Y alebo A/B | Kapitola 5 a otvorené otázky uvádzajú novšie potvrdenie X/Y aj A/B a výslovne označujú rozpor |
| Prehľad | Končil pred poslednými dvoma správami | Aktualizovaný úvod, päta, kapitola 32, README a otvorené otázky |

## Hranice potvrdenia

- Správa z 29. 10. vysvetľuje PPG a podmienky; obmedzenie histórie vtedy iba navrhuje. Až správa z 30. 10. potvrdzuje vykonanie úpravy.
- Nepotvrdzuje sa nové číslo verzie, produkčné nasadenie, zmena tímového AVG10 ani zmazanie starších dát.
- Pri TOP/TOP2 nie je známe, či rozdiel „aj“ / „alebo“ znamená novú implementáciu alebo nepresnú formuláciu e-mailu. Je potrebné doplňujúce potvrdenie alebo aktuálny kód.
- Pôvodné obrázky, skripty, identifikátory kapitol a historické audity zostávajú zachované.
