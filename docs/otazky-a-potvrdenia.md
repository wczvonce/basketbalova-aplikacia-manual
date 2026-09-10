# Otázky a potvrdenia pre ďalšiu aktualizáciu

Stav k 10. 9. 2026: spracovaných sedem komentovaných videí a čítacia kontrola PC administrácie. Ovládanie, legenda, história a mobilný export sú doplnené do kapitol 30 a 31. Hodnoty nastavení môže vlastník kedykoľvek meniť; nejde o pevné defaulty aplikácie.

## Konkrétne doplnenia od vlastníka

- **Prostredie uzavreté:** vlastník potvrdil TEST ako hlavnú verziu manuálu, pripravovanú na produkčné nasadenie. Otvoril zodpovedajúce testovacie CMS; staré produkčné CMS nie je referenciou nových funkcií.
- **Farby uzavreté analýzou APK:** ružová TOP2, zelená TOP, biela pri bežných binárnych dátach WATCH, svetložltá bez všetkých troch označení. Biela je tiež fallback pri niektorých neúplných hodnotách. Predbežná spomienka vlastníka bola opravená podľa klienta.
- **A uzavreté analýzou APK:** prepína upozornenie na súpisku sledovaného tímu (ExistLineup), nezaraďuje jeho zápasy automaticky medzi TOP.
- **Ukážka dát:** dodať JSON uložený vo videu (`BBALL_JOE_HEL_20260909.json`). Pomôže overiť schému; pre index 2241 % bude podľa obsahu potrebný aj surový záznam historického zápasu Salon Vilpas - Helsinki Seagulls z 18. 3. 2026.

Rovnaký ZIP netreba posielať znova. Pre chýbajúce časti má význam úplný aktuálny zdroj mobilu/CMS, exportéra a plánovača. Inštalačný súbor môže pomôcť overiť verziu a ovládanie, ale nenahradí zdrojové súbory ani nedokazuje serverový harmonogram.

## Potvrdená snímka konfigurácie

| Parameter | Hodnota na snímke z 9. 9. 2026 |
| --- | --- |
| TOP | X/Y 8/10; A/B 4/5; priemer 15 minút |
| TOP2 | X/Y 4/5; A/B 8/10; priemer 5 PPG |
| WATCH | X/Y 1/5; priemer 5 minút; priemer 5 PPG |
| Všeobecné prahy | náhrada N = 80 %; rozdiel oslabenia P = 30 %; pokles kurzu S = 100 % |
| Obnovovanie detailu | 1 minúta |
| Prepínače | celá zostava pred zápasom zapnutá; FS notifikácie vypnuté; iba TOP zapnuté; prijímanie notifikácií zapnuté |
| OpenAI model | `gpt-5-mini` |

Snímka slúži na doloženie konkrétneho stavu v čase. Pri ďalšej zmene nastavení sa manuál nemusí prepisovať, pokiaľ sa nemení význam polí alebo logika aplikácie.

## Údaje potrebné na úplné prevádzkové overenie

Tieto body nebránia oprave manuálu podľa kódu; uzavrú sa, keď bude dostupná príslušná časť aplikácie alebo potvrdenie správcu.

| Téma | Čo treba overiť | Dopad |
| --- | --- | --- |
| TOP/WATCH a minúty | Je zámer počítať súpisky aj pri DNP a pri chýbajúcich načítaných štatistikách preskočiť prahy? | Potvrdí, či ide o zamýšľané pravidlo alebo požiadavku na opravu aplikácie. |
| TOP2 | Je zámer vyžadovať Starter, vlastné X/Y a A/B a samostatný PPG prah? | Vysvetlí rozdiel oproti starému výberu podľa najvyššieho PPG. |
| Náhrada | Potvrdiť hranicu troch evidovaných zápasov a opraviť nesprávne ukladanú identitu náhradníka. | Audit A02; manuál zatiaľ opisuje skutočnú hranicu. |
| WATCH parametre | APK odosiela WATCH PPG cez UserApi.saveParam ako používateľský parameter, serverový prepočet ZIP-u číta systémové parametre. Overiť prepojenie endpointu a práva. | Hlavné TEST CMS obsahuje aj prah PPG. Bez obsluhy serverového endpointu nie je potvrdená synchronizácia ani účinok mobilnej zmeny. |
| Harmonogram | Načítavanie 120 minút pred zápasom, označovanie 2:00, export 4:00, maily 1:25/10:54, kurzy každých 10 minút. | V ZIP-e chýba plánovač; časy sú historické podklady. |
| Sezóny/archív | Platnosť hranice 1. 8. 2026, ligy s letnou sezónou a aktuálny stav archivácie. | Audit A01/A08, význam tímového priemeru a dostupnej histórie. |
| Export | Aktuálny vzor JSON, aktívny exportér, DTO a časový význam štatistík/kurzov. | Presná schéma, uchovanie predzápasového stavu a možnosť korektnej simulácie. |
| StatePoints | Ako konkrétne GS/FS dekodéry priraďujú 1 a 2 pri DNP, chýbajúcich a nulových štatistikách. | Rozlíšenie dátovej neúplnosti od skutočného nenastúpenia. |
| Kurzy | Aktuálna čítačka, výber kancelárie a zhodnosť zdroja pre detail a filter. | Audit A04/A06; správna strana tímu a porovnateľné Start/Last. |
| Prenos mapovaní | Potvrdiť a otestovať opravu obnovy tímových väzieb v novej sezóne. | Audit A03; neoznačovať operáciu za bezchybnú len podľa úspešnej správy. |
| Klient/CMS | Legenda, farby, A a hlavné postupy overené aj z APK; chýba úplný pôvodný klient/CMS projekt a testy GS operácií. | Dekompilácia nie je úplný zdroj a mala čiastkové chyby. |

## Záznam potvrdení

- **10. 9. 2026 – APK 1.0.35.0:** skopírované z telefónu bez zmien dát; staticky potvrdené farby a A, zúžená diagnostika 2241 % a identifikovaná používateľská cesta zápisu WATCH PPG. [Podrobnosti](audit-apk-2026-09-10.md).

- **10. 9. 2026 – hlavná verzia:** vlastník potvrdil, že aktuálna TEST verzia je hlavná pre manuál a neskôr má byť produkčná. V jej CMS boli overené aj WATCH PPG, výber používateľa exportu a posledný export; tieto rozdiely oproti starej produkcii už nie sú otvorené chyby.

- **10. 9. 2026 – videá a CMS:** potvrdené prepínanie zoznamov, detail domácich/hostí, história cez názov tímu, PairMatch, R, hlásenie mobilného JSON exportu, mobilná administrácia gestom a legenda. PC formuláre kontrolované bez zmien. Podrobné časové odkazy: [doplnkový audit](audit-2026-09-10.md).

- **9. 9. 2026 – verzia kódu:** vlastník potvrdil, že `BBALL-AI.zip` je najaktuálnejší používaný kód a že z neho čerpáme do manuálu.
- **9. 9. 2026 – nastavenia:** vlastník poslal snímku aktuálnej konfigurácie a potvrdil, že hodnoty môže kedykoľvek meniť podľa potreby. Hodnoty sú zapísané vyššie ako dátovaná snímka, nie ako defaulty.

Pri ďalších potvrdeniach uviesť dátum, potvrdenú hodnotu a jej rozsah. Návrhy ani statické odhady nezapisovať ako potvrdené fakty.
