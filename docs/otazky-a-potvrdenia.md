# Otázky a potvrdenia pre ďalšiu aktualizáciu

Stav k 9. 9. 2026: vlastník potvrdil verziu kódu a poslal aktuálnu snímku obrazovky Nastavenia. Hodnoty sú prevádzkové parametre, ktoré môže kedykoľvek meniť; nejde o pevné defaulty aplikácie.

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
| WATCH parametre | Potvrdiť, či sú hodnoty spoločné pre všetkých alebo meniteľné iba správcom. | Snímka ukazuje X/Y 1/5, 5 minút a 5 PPG, ale samotná obrazovka nepotvrdzuje rozsah účinku zmeny. |
| Harmonogram | Načítavanie 120 minút pred zápasom, označovanie 2:00, export 4:00, maily 1:25/10:54, kurzy každých 10 minút. | V ZIP-e chýba plánovač; časy sú historické podklady. |
| Sezóny/archív | Platnosť hranice 1. 8. 2026, ligy s letnou sezónou a aktuálny stav archivácie. | Audit A01/A08, význam tímového priemeru a dostupnej histórie. |
| Export | Aktuálny vzor JSON, aktívny exportér, DTO a časový význam štatistík/kurzov. | Presná schéma, uchovanie predzápasového stavu a možnosť korektnej simulácie. |
| StatePoints | Ako konkrétne GS/FS dekodéry priraďujú 1 a 2 pri DNP, chýbajúcich a nulových štatistikách. | Rozlíšenie dátovej neúplnosti od skutočného nenastúpenia. |
| Kurzy | Aktuálna čítačka, výber kancelárie a zhodnosť zdroja pre detail a filter. | Audit A04/A06; správna strana tímu a porovnateľné Start/Last. |
| Prenos mapovaní | Potvrdiť a otestovať opravu obnovy tímových väzieb v novej sezóne. | Audit A03; neoznačovať operáciu za bezchybnú len podľa úspešnej správy. |
| Klient/CMS | Aktuálne obrazovky, popisy ikon, tlačidlá a export súťažných prepojení. | Oddelenie serverovej podpory od skutočného ovládania klienta. |

## Záznam potvrdení

- **9. 9. 2026 – verzia kódu:** vlastník potvrdil, že `BBALL-AI.zip` je najaktuálnejší používaný kód a že z neho čerpáme do manuálu.
- **9. 9. 2026 – nastavenia:** vlastník poslal snímku aktuálnej konfigurácie a potvrdil, že hodnoty môže kedykoľvek meniť podľa potreby. Hodnoty sú zapísané vyššie ako dátovaná snímka, nie ako defaulty.

Pri ďalších potvrdeniach uviesť dátum, potvrdenú hodnotu a jej rozsah. Návrhy ani statické odhady nezapisovať ako potvrdené fakty.
