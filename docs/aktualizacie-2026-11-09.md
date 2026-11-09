# Audit manuálu BBALL podľa e-mailov vývojára – 9. 11. 2026

Znovu prejdená korešpondencia s Petrom Škantárom (SOTEC s.r.o.) od januára 2025 do 9. 11. 2026. Automatické kontrolné maily (`bballdev100`), faktúry a volejbal sa nepočítali. Pri rozpore platí novší e-mail (pravidlo vlastníka). Nový zdrojový kód ani APK sa nekontrolovali. Septembrový `BBALL-AI.zip` sa použil iba na porovnanie jednej nezrovnalosti (GS naprieč súťažami).

## Rozsah čítania

| Obdobie | Spôsob |
| --- | --- |
| marec – 9. 11. 2026 | všetky vlákna so Škantárom prečítané celé |
| december 2025 – február 2026 | zoznam a obsah všetkých vlákien; celé tie, ktoré menia pravidlá manuálu (kurzy, handicap, notifikácie, export, sledovaní hráči, BetsAPI, nasadenia) |
| 2023 – november 2025 | zoznam a obsah všetkých vlákien; celé iba tie, ktoré menili text manuálu (archivácia) |

Reklamácie konkrétnych zápasov, ktoré nemenia pravidlá, sú zapracované iba vtedy, keď z nich vyplýva všeobecné správanie aplikácie.

## Opravené nesprávne alebo zastarané tvrdenia

| Manuál pred auditom | Novší e-mail | Kapitola |
| --- | --- | --- |
| AVG10 nemá hranicu „pred týmto zápasom“, môže použiť novšie výsledky | 7. 11. 2026: skóre sa načíta iba z predchádzajúcich zápasov k vyhodnocovanému zápasu | 7, 27 |
| nočné označovanie o 2:00 | 3. 2. 2026: označovanie v noci o 3:00 | 5 |
| archivácia pozastavená, musí sa ešte prejsť | 13. 5. 2025: archivácia upravená a spustená na teste (do 2. 4. 2025, 40 dní) | 27 |
| kurzy bez rozlíšenia zdroja; mobilná kapitola: „kurzy z BetsAPI (Tipsport, inak priemer)“ | 29. 1. a 1.–4. 3. 2026: FS kurzy z Flashscore (Tipsport/priemer), GS kurzy z BetsAPI; BetsAPI iba pre GS | 9, 10, mobilná kap. 3 |
| čierna bodka (mobilná kapitola) = zmena zostavy v noci | 6.–7. 11. 2026: hlavne zmena PPG, AVG10 po zápase a nové sledované hráčky v noci | 8, mobilná kap. 3 |
| TOP/TOP2 „aj“ vs. „alebo“ ako neriešený rozpor | pravidlo vlastníka: platí novší e-mail; pri chýbajúcich štatistikách „aj“ (29. 10.), pri dostupných „alebo“ + minúty/PPG (12. 3., 20. 3., 28. 4.) | 5 |

## Doplnené chýbajúce pravidlá

| E-mail | Doplnenie | Kapitola |
| --- | --- | --- |
| 9. 11. 2026 | GS zmenil štruktúru widgetov, automatická identifikácia súťaží upravená a nasadená | 21 |
| 9. 11. 2026 | FS zmenil štruktúru zostáv, zostavy sa pri niektorých zápasoch nenačítali, oprava sa pripravuje | 3, 29 |
| 8. 11. 2026 | mobilný JSON = obsah detailu, index aktuálneho zápasu v ňom chýba | 24 |
| 5. 11. 2026 | obnovenie hesla z aplikácie cez administráciu | 1, mobilná kap. 1 |
| 3. 11. 2026 | 1.0.50.0 prevádzka, test v Google Play pozastavený, nasadenie nad existujúcou prevádzkovou DB | 1 |
| 2. 11. 2026 | ligy s dekodérom Manual treba identifikovať každú sezónu, GS mení ExternalId | 13 |
| 27. 5. 2026 | detail FS po opakovanom čítaní ukazuje hráčov po zápase (Period 100) | 3 |
| 5.–7. 5. 2026 | podmienka 6, resp. 5 + 6 hráčov sa pri Period 100 nekontroluje; zápas môže byť v Zaujímavých bez notifikácie | 3 |
| 29. 4. – 6. 5. 2026 | Application pool, Rapid-Fail Protection, limit testovacej DB 10 GB | 26, 29 |
| 24.–27. 4. 2026 | sivá a modrá nula, náhradníci, modré PPG = dopočítané | 29, 30, mobilná kap. 6 |
| 24. 4. 2026 | hráči GS nie sú prepojení medzi súťažami | 5, 18 |
| 19.–20. 4. 2026 | Zaujímavé a parametre sú pre prihláseného používateľa | 29 |
| 8.–11. 4. 2026 | FS 1. štvrtina 7 minút čistého hracieho času; pridaní hráči pre GS aj FS | 2, 3 |
| 25. 3. 2026 | po načítaní 1. štvrtiny sa FS zápas prestane sledovať | 3 |
| 11. 3. 2026 | pôvodný handicap FS (kandidáti s rozdielom kurzov ≤ 0,09, extrémy) | 9 |
| 4. 3. 2026 | oprava vymenených kurzov iba pre FS | 9 |
| 28. 2. 2026 | formát textu notifikácie | 6 |
| 26. 2. 2026 | aktuálny handicap FS (najmenší rozdiel kurzov) | 9 |

## Zosúladenie celého manuálu

- Vety o TEST verzii ako hlavnej a „pripravovanej do prevádzky“ prepísané podľa stavu od 3. 11. 2026: úvod stránky, kapitoly 1, 2, 5, 23, 28, 30, 31, 32, README a otvorené otázky.
- Pri opravách potvrdených v septembri a októbri iba pre TEST je uvedené, že by mali byť v prevádzke od nasadenia 3. 11. 2026; zoznam nasadených opráv vývojár neuviedol.
- Kapitola 1: kurzy GS z BetsAPI, FS z Flashscore (predtým všetky z BetsAPI).
- Kapitola 5: doplnená novšia snímka nastavení z 8. 11. 2026 (podľa vlastníka).
- Mobilná kapitola: pravidlo TOP/TOP2 „aj“ obmedzené na hráčov bez webových štatistík, doplnené nasadenie z 3. 11.

## Otvorené body

- **GS naprieč súťažami:** e-mail 27. 3. 2026 hovorí, že vyhľadávanie zápasov GS tímov naprieč súťažami je vypnuté v teste aj prevádzke. `BBALL-AI.zip` (september 2026) však v `StaMatchStorage.GetLastMatchesForMarkPlayers`, `GetLastMatches` a `GetScoreMatches` spája GS tímy cez `InternalId` (`StaTeam.GetColumnTeamJoin`). Počet zápasov hráča (`GetCountMatchesForPlayers`) sa sčítava podľa ExternalId hráča, takže GS hráčovi sa rátajú iba zápasy jeho súťaže. Treba potvrdiť aktuálny stav.
- **TOP/TOP2 pri chýbajúcich štatistikách:** „X/Y aj A/B“ podľa e-mailu 29. 10. 2026, na konkrétnom hráčovi neoverené.
- **Oprava zostáv FS** po zmene z 8. 11. 2026 a **index v mobilnom JSON-e:** zatiaľ neoznámené ako hotové.
- **Bez odpovede vývojára (8. 11. 2026):** kópia JSON zápasu do Supabase pri každej notifikácii; reklamácia neskoro načítaných zostáv siedmich zápasov.

## Hranice

Heslá a prihlasovacie údaje z e-mailov sa do verejného manuálu nepridávajú. Pôvodné obrázky, identifikátory kapitol a historické audity ostali zachované. Nová kapitola 33 je na konci, aby sa neposunuli odkazy na pôvodné kapitoly.
