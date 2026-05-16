# /bevezetes — EV-AIOS Bevezető Varázsló

## Leírás
Ez a skill az EV-AIOS első futtatásához szükséges. Beolvassa az `ev-intake.md` fájlt, megválaszolja a hiányzó kérdéseket egy interaktív interjún keresztül, majd legenerálja az 1. napi alapfájl-csomagot.

Bármikor újrafuttatható egy szerkesztett `ev-intake.md`-ből.

## Mit csinál
- Beolvassa az `ev-intake.md`-t és ellenőrzi, melyik kérdés van kitöltve
- Hiányzó kérdéseket interjú formájában feltesz a felhasználónak
- A válaszok alapján legenerálja a következő fájlokat:
  - `context/en-magam.md` (Q1-ből az identitás-rész — vagy EV-Alap-ból átemelve)
  - `context/icp.md` (Q1-ből az ICP-rész — vagy EV-Alap-ból átemelve)
  - `context/ajanlat.md` (Q1-ből az ajánlat-rész — vagy EV-Alap-ból átemelve)
  - `context/szemelyes.md` (Q2 + Q3 alapján)
  - `context/prioritasok.md` (Q3 alapján)
  - `references/voice.md` (Q2 alapján — szó szerinti hangminta)
  - `kapcsolatok.md` (Q4-Q7 alapján kitöltve)
  - `CLAUDE.md` (helyettesítő szövegek kitöltve)

## Mit NEM csinál
- Nem ír felül kézzel szerkesztett context fájlokat figyelmeztetés nélkül
- Nem tölti ki a `decisions/naplo.md`-t (azt a `/fejlesztes` és `/attekintes` teszi)
- Nem épít domain skilleket (azt a `BOVITESEK.md` szerint a felhasználó dönti el)
- Nem ad pontszámot, audit-ot vagy javaslatot — ez tisztán bevezető skill

## Fázisok

### 1. fázis — Bemenet (intake) ellenőrzés
Olvasd be az `ev-intake.md`-t. Listázd ki, melyik Q1-Q7 kérdés van kitöltve és melyik nem (a `[A te válaszod]` helyettesítő szöveg = nincs kitöltve).

**Konfliktuskezelés EV-Alap-ról áthozott fájlokra:** Mielőtt elindulsz, nézd meg, létezik-e már `context/en-magam.md`, `context/icp.md`, vagy `context/ajanlat.md`. Ha igen, olvasd be a tartalmukat és csak akkor frissítsd, ha az új információ értelmesen kiegészíti. Ha tartalom-konfliktus van (pl. a Q1 más identitást mond, mint az `en-magam.md`), kérdezz a felhasználótól: melyik az érvényes verzió.

Ha minden ki van töltve, ugorj a 3. fázisra.

### 2. fázis — Hiányzó kérdések interjúja
Egyenként kérdezd végig a hiányzó kérdéseket. **Egyszerre EGY kérdés.** Várj válaszra. A választ mentsd vissza az `ev-intake.md`-be (str_replace-szel a helyettesítő szöveg helyére).

**Speciális szabály a Q2-re**: HA a felhasználó NEM illeszt be szó szerinti szöveget, hanem leírja "mit szokott írni", JELEZD hogy ez kevert hang és kérj újra:

> "Ez nem egy szó szerinti minta — ez egy leírás róla. Kérlek illessz be tényleges, nyers szöveget: egy emailt, posztot, üzenetet pontosan abban a formában, ahogy elküldted/megírtad. Ne fogalmazd át, ne tisztázd. A nyers, hibákkal együtt jobb, mint a kitisztított."

A hangmintának autentikusnak KELL lennie, különben a `references/voice.md` használhatatlan lesz.

### 3. fázis — Fájlgenerálás

A teljes bemenet alapján generáld le az alábbi fájlokat. **Minden fájlnál először ellenőrizd, létezik-e már. Ha létezik és tartalmaz EV-Alap-ról áthozott vagy kézzel szerkesztett tartalmat, NE írd felül — építs rá vagy kérdezz.**

**`context/en-magam.md`** — Q1 első része: identitás.
- Ki vagyok (szakma, tapasztalat, hány éve csinálod)
- Hol állok ezen a piacon
- Mit jelent ez emberileg

Ha létezik már (EV-Alap-ból), CSAK akkor frissítsd, ha az új Q1-ből kiderül valami, ami értelmesen hozzáad.

**`context/icp.md`** — Q1 ICP-része: kinek dolgozol.
- Ki az ideális ügyfeled (cég-méret, élethelyzet, szakma)
- Mit szeretne, mitől szenved
- Hol találod meg

Ha létezik már (EV-Alap-ból), CSAK akkor frissítsd, ha új Q1 hozzáad.

**`context/ajanlat.md`** — Q1 ajánlat-része: mit veszek meg tőled.
- Mit adsz el (szolgáltatás, csomag, termék)
- Áron, formátumban, határidőben
- Mi az értéke az ügyfélnek

Ha létezik már (EV-Alap-ból), CSAK akkor frissítsd, ha új Q1 hozzáad.

**`context/szemelyes.md`** — Q2 + Q3 alapján következtetett személyes profil:
- Kommunikációs stílus észrevételek
- Mire fókuszál a következő 90 napban
- (Ha az intake-ből kiderül) értékek, motivációk

**`context/prioritasok.md`** — Q3 tisztán, plusz minden prioritáshoz:
- Mi a definíciója a "kész"-nek
- Mi a kapcsolat a három pillérrel (ügyfélszerzés / ügyfélkezelés / háttérműködés)

**`references/voice.md`** — Q2 szó szerinti mintái. ALATTUK megfigyelt jellemzők:
- Hangnem (formális/informális)
- Mondatszerkezet (rövid/hosszú)
- Gyakori szavak/kifejezések
- Írásjelhasználat
- "Mit NE csinálj a hangom utánzásakor"

**`kapcsolatok.md`** — Q4-Q7 alapján minden megemlített eszköz külön bejegyzéssel a megadott formátumban (Mire való / Pillér / Státusz / Hozzáférés / Frissítés).

**`CLAUDE.md`** — A meglévő helyettesítő szövegekkel ellátott fájl frissítése:
- `{{Neved}}` helyébe a Q1-ből kinyert név kerül
- `{{megnevezett prioritás}}` helyébe a Q3 első prioritása kerül
- "Tudásbázis" szekcióba: Q1 + Q3 szintézis, hivatkozva a `context/` 5 fájlra
- "Kapcsolatok" szekcióba: kapcsolatok.md tömör összefoglalója

**Konfliktuskezelés**: ha valamelyik `context/` fájl már létezik (pl. az EV-Alap-ból áthozott), olvasd be a tartalmát és csak akkor frissítsd, ha az új információ értelmesen kiegészíti. Ha tartalom-konfliktus van, kérdezz a felhasználótól:

> "A `[fájlnév]` már tartalmaz adatot. Felülírjam, egybeolvasszam (a régit megtartva, az újat hozzáadva), vagy hagyjam érintetlenül?"

### 4. fázis — Záró összefoglaló

Írd ki:
- Melyik fájlok jöttek létre / frissültek
- Mit ajánlasz következő lépésnek (általában: "használd egy hetet, aztán futtasd `/attekintes`-t a 7. napon")
- Egy mondatos emlékeztető: "Bármikor szerkesztheted az `ev-intake.md`-t és újrafuttathatod a `/bevezetes`-t."

## Kimenet
Egy működő, kitöltött AIOS, készen az 1. napi használatra.
