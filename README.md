# Basketbalová aplikácia: manuál BBALL

Prehľadávateľný slovenský manuál na obsluhu aplikácie BBALL.

[Otvoriť webový manuál](https://wczvonce.github.io/basketbalova-aplikacia-manual/)

Aktualizácia z 8. 9. 2026 vychádza zo statického auditu dodaného `BBALL-AI.zip`.
Opravuje pravidlá TOP/TOP2/WATCH, výpočet oslabenia, náhrady hráčov,
notifikácie, CSV importy a výklad histórie. Zachováva pôvodné obrazové
podklady a rozlišuje overený kód od starších prevádzkových poznámok.

- [Technický audit a zdrojové miesta](docs/audit-2026-09-08.md)
- [Otázky a potvrdenia](docs/otazky-a-potvrdenia.md)

Vlastník 9. 9. 2026 potvrdil, že ZIP obsahuje najaktuálnejší používaný kód
a je hlavným zdrojom pre tento manuál. ZIP však obsahuje iba časť serverového
projektu; aktuálne hodnoty účtu, harmonogram úloh a konečný JSON export zostávajú
nepotvrdené. Audit nie je potvrdením bezchybnosti celej aplikácie.
Samotná aplikácia sa v tomto repozitári neopravuje.

## Lokálne otvorenie

Otvoriť `index.html` v prehliadači. Inštalácia balíkov ani server nie sú potrebné.
Vyhľadávanie, obsah a vložené obrázky fungujú lokálne. Externé odkazy vyžadujú internet.

## Aktualizácia

Obsah, štýly a vyhľadávanie sú v `index.html`. GitHub Pages publikuje koreň
vetvy `main`. Pri úpravách zachovať existujúce identifikátory kapitol,
zdrojové poznámky a pôvodné obrázky. Pred publikovaním skontrolovať odkazy,
vyhľadávanie s diakritikou aj bez nej, mobilné zobrazenie a tlač.

Zdrojový ZIP, produkčné dáta a prihlasovacie údaje sem nepatria. Audit uvádza
názvy zdrojových súborov, metódy a čísla riadkov vzhľadom na identifikovaný ZIP,
nie verejnú kópiu aplikácie.
