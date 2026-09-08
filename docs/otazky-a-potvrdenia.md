# Otázky a potvrdenia pre ďalšiu aktualizáciu

Stav k 8. 9. 2026: manuál opisuje overený dodaný kód. Nižšie uvedené odpovede zatiaľ neboli potvrdené. Nepotvrdené číselné príklady sa nepovažujú za nastavenia účtu.

## Otázky položené vlastníkovi

1. **Nasadená verzia:** Je `BBALL-AI.zip` totožný s verziou, ktorá sa aktuálne používa, alebo ide o novší/testovací podklad? Potrebné na označenie platnosti manuálu pre prevádzku.
2. **Aktuálne nastavenia:** TOP X/Y, A/B a minúty; TOP2 X/Y, A/B a PPG; N % pre náhradu, P % pre rozdiel oslabenia a S % pre pokles kurzu. Kód ich číta z účtu; pôvodné čísla 8/10, 4/5, 15, 80/30/30 ich nedokazujú.

Odpovede možno doplniť sem ako dátované potvrdenie a premietnuť do kapitol 5 až 7. Neuvádzať heslá, prístupové tokeny ani iné prihlasovacie údaje.

## Údaje potrebné na úplné prevádzkové overenie

Tieto body nebránia oprave manuálu podľa kódu; uzavrú sa, keď bude dostupná príslušná časť aplikácie alebo potvrdenie správcu.

| Téma | Čo treba overiť | Dopad |
| --- | --- | --- |
| TOP/WATCH a minúty | Je zámer počítať súpisky aj pri DNP a pri chýbajúcich načítaných štatistikách preskočiť prahy? | Potvrdí, či ide o zamýšľané pravidlo alebo požiadavku na opravu aplikácie. |
| TOP2 | Je zámer vyžadovať Starter, vlastné X/Y a A/B a samostatný PPG prah? | Vysvetlí rozdiel oproti starému výberu podľa najvyššieho PPG. |
| Náhrada | Potvrdiť hranicu troch evidovaných zápasov a opraviť nesprávne ukladanú identitu náhradníka. | Audit A02; manuál zatiaľ opisuje skutočnú hranicu. |
| WATCH parametre | Systémové X/Y, minúty a PPG. | Sú spoločné a v dodávke nemajú uložené aktuálne hodnoty. |
| Harmonogram | Načítavanie 120 minút pred zápasom, označovanie 2:00, export 4:00, maily 1:25/10:54, kurzy každých 10 minút. | V ZIP-e chýba plánovač; časy sú historické podklady. |
| Sezóny/archív | Platnosť hranice 1. 8. 2026, ligy s letnou sezónou a aktuálny stav archivácie. | Audit A01/A08, význam tímového priemeru a dostupnej histórie. |
| Export | Aktuálny vzor JSON, aktívny exportér, DTO a časový význam štatistík/kurzov. | Presná schéma, uchovanie predzápasového stavu a možnosť korektnej simulácie. |
| StatePoints | Ako konkrétne GS/FS dekodéry priraďujú 1 a 2 pri DNP, chýbajúcich a nulových štatistikách. | Rozlíšenie dátovej neúplnosti od skutočného nenastúpenia. |
| Kurzy | Aktuálna čítačka, výber kancelárie a zhodnosť zdroja pre detail a filter. | Audit A04/A06; správna strana tímu a porovnateľné Start/Last. |
| Prenos mapovaní | Potvrdiť a otestovať opravu obnovy tímových väzieb v novej sezóne. | Audit A03; neoznačovať operáciu za bezchybnú len podľa úspešnej správy. |
| Klient/CMS | Aktuálne obrazovky, popisy ikon, tlačidlá a export súťažných prepojení. | Oddelenie serverovej podpory od skutočného ovládania klienta. |

## Záznam potvrdení

Zatiaľ bez odpovedí. Pri doplnení použiť dátum, potvrdenú verziu/prostredie, hodnotu a zdroj potvrdenia. Návrhy ani statické odhady nezapisovať ako potvrdené fakty.
