# Aktualizácia manuálu BBALL – 29. 10. 2026

Spracované správy Petra Škantára za 29. 8. – 29. 10. 2026. Ide o aktualizáciu dokumentácie podľa potvrdení vývojára, nie o nový audit zdrojového kódu či APK. Hlavné prostredie manuálu: TEST. Testovacie opravy nie sú automaticky potvrdené v prevádzke.

## Čo bolo zapracované a kam

| Dátum správy | Zmena / vysvetlenie | Kapitoly index.html |
| --- | --- | --- |
| 14. 9. | Android 17, prevádzková 1.0.36.1 | 1 |
| 18. 9. | TEST 1.0.37.0: ukladanie TOP X/Y; serverové úpravy náhrad a prepojení/párovania; vysvetlenie histórie percent a stránkovania | 1, 7, 12, 30, 31 |
| 28. 9.; 17.–18. 10. | Prevádzková 1.0.38.0, oddelenie účtov a spôsob distribúcie TEST/prevádzka | 1 |
| 9. 10. | Nasadené čistenie starých označení sledovaných hráčov v TEST prostredí | 5, 29 |
| 27. 10. | Vysvetlenie rozdielu medzi notifikáciou a posledným indexom; starší stav kontroly piatich zápasov | 2, 6, 8, 29 |
| 29. 10. | TEST 1.0.40.0: čierna bodka na 4. pozícii, TOP/TOP2 porovnanie indexov; rozšírené minimum piatich zápasov pri GS/FS | 1, 2, 3, 6, 8, 29, 30 |

### 1. Prostredia a verzie
- Kapitola 1: doplnená tabuľka 1.0.36.1 (prevádzka), 1.0.37.0 (test), 1.0.38.0 (prevádzka), 1.0.40.0 (test).
- Android 17: vývojár 14. 9. oznámil aktualizáciu a optimalizáciu oboch prostredí.
- Oddelenie účtov bolo potvrdené 17. 10.; distribúcia používa jednu aplikáciu v testovacom režime Google Play podľa vysvetlenia z 18. 10. Nie je zaručená súčasná dostupnosť oboch inštalačiek.
- Pri zmene prostredia na rovnakom telefóne odporučil vývojár 4. 10. opätovnú inštaláciu, prípadne vymazanie dát. Heslá ani celé e-maily sa do verejného manuálu nepridávajú.

### 2. Nastavenia a serverové opravy zo septembra
- Kapitola 30: pôvodné upozornenie na ukladanie TOP X/Y v APK 1.0.35.0 označené ako historický nález; 18. 9. bola oznámená úprava v TEST 1.0.37.0.
- Kapitoly 7 a 12: doplnené potvrdenia úprav náhrad hráčov a kopírovania prepojení/párovania. Vývojár uviedol, že nálezy nemali vplyv na správnu funkčnosť. Bez nového kódu netvrdíme nezávislé overenie.
- Kapitola 30: stránkovanie upozornení vývojár označil za funkčné, neoznámil jeho opravu.
- Kapitola 30: historických 2241,00 % vysvetlených konkrétnym doloženým výpočtom 18,80 / 83,9 ≈ 22,41 %. Nejde o potvrdenie hromadnej opravy historických dát.
- Kapitoly 28 a 31: zrušené zastarané všeobecné tvrdenie o nepotvrdených/opravou nedotknutých nálezoch; pôvodné auditné súbory zostali historické.

### 3. Čistenie sledovaných hráčov – 9. 10., TEST
- Kapitola 5: nahradený aktuálne formulovaný popis ponechávania starých značiek historickým vysvetlením.
- Pridaný potvrdený postup: určenie aktívnych tímov; odstránenie značiek neaktívnych tímov; odstránenie značiek tímu bez zápasov; nahradenie starých značiek novými po vyhodnotení tímu so zápasmi.
- Kapitola 29: doplnená diagnostika starých TOP2 označení.
- Správa nemení samotné prahy TOP/TOP2/WATCH a neuvádza číslo novej mobilnej verzie.

### 4. Minimum piatich zápasov – 29. 10.
- Kapitoly 2 a 3: doplnené minimum 5 zápasov aspoň jedného tímu aj pre 2. a ďalšie štvrtiny GS/FS, prípadne pozápasové vyhodnotenie FS.
- Kapitoly 6 a 29: dopad na vyhodnotenie a diagnostiku; upozornenie na zaujímavý zápas sa naďalej posiela iba pred zápasom alebo v 1. štvrtine.
- Stav opísaný 27. 10. (bez minima pri neskorších častiach GS) je historický a bol prekonaný potvrdením z 29. 10.
- Oprava oznámená spolu s TEST 1.0.40.0; produkčné nasadenie a presný SQL výber nového minima správa nepotvrdzuje.

### 5. Posledný index a čierna bodka – TEST 1.0.40.0
- Kapitoly 6 a 8: notifikácia obsahuje hodnoty pri odoslaní, zoznam posledné vyhodnotenie. Príklad Capiata Bulls – San Alfonzo: 33,55 % : 0 % v 1. štvrtine, neskôr 0 % : 0 %.
- Kapitola 8: čierna bodka na štvrtej pozícii zľava znamená zmenu indexu oproti notifikácii. Bežný zaujímavý zápas porovnáva TOP; zaujímavý TOP zápas porovnáva TOP2.
- Nie je to iba indikátor nočnej zmeny zostavy: Bendigo Ž – Townsville Ž zmenilo 36,55 % na 37,04 % pri rovnakých chýbajúcich PPG. Bez zmeny indexu v príklade Espanol Osorno – CD Puerto Varas bodka nebola.
- Kapitola 30: doplnený riadok legendy; odlíšené od čierneho kruhu štatistík hráča.
- Kapitola 29: doplnený diagnostický postup.

## Zdrojové správy
Identifikácia podľa dátumu a témy, bez zverejnenia súkromných tiel správ:
- 14. 9. 2026: „Aktualizacia app pre Android 17 a prevadzkova app“.
- 18. 9. 2026: „Re: BBALL aplikácia – kontrola potenciálnych chýb z auditu“.
- 28. 9. 2026: odpoveď k dostupnosti prevádzkovej aplikácie 1.0.38.0.
- 4. 10. 2026: odporúčanie k výmene prostredia v telefóne.
- 9. 10. 2026 a 17.–18. 10. 2026: vlákno „Reklamácia BBALL – Ormanspor – Istanbul, ružové TOP2 hráčky pri údaji 1/5“.
- 27. 10. 2026: „Fwd: Reklamácia BBALL – testovacia verzia: podmienka minimálne 5 zápasov“ a „Fwd: Reklamácia BBALL – testovacia verzia: Capiata Bulls – San Alfonzo“.
- 29. 10. 2026, 16:28: „Re: Reklamácia BBALL – testovacia verzia: Capiata Bulls – San Alfonzo“ (TEST 1.0.40.0).

## Hranice
Pôvodné obrázky, existujúce identifikátory kapitol a historické audity zostávajú zachované. Nová kapitola 32 je pridaná na konci, aby sa neposunuli automatické odkazy na pôvodné kapitoly. Neoverené návrhy nie sú zapísané ako hotové funkcie. Nové správy nepotvrdzujú zmenu štatistických prahov WATCH, synchronizácie jeho parametrov ani opravu všetkých starších auditných nálezov.
