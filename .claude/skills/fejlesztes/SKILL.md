# /fejlesztes — Heti 3Ms Interjú (Pillér-fókusszal)

## Leírás
Heti gondolkodási skill. Egy választott pilléren keresztül átfut a 3Ms-en (Mindset → Method → Machine), és a végén egy konkrét, megépíthető automatizálási darabot ad.

**Egy futás = egy automatizálás. Egy hét = egy futás.**

## Mit csinál
- Felteszi a választott pillér kérdést (1 a 3-ból)
- Végigvezet a 3Ms-en abban a pillér-kontextusban
- A végén kimenet: 1 db scope-olt automatizálási darab + automatikusan logolja `decisions/naplo.md`-be

## Mit NEM csinál
- Nem épít több automatizálást egyszerre (szándékos limit: egy hét = egy darab)
- Nem implementálja az automatizálást (azt a felhasználó vagy egy másik Claude Code session csinálja)
- Nem ad ötletet előzetesen — a 3Ms-en KELL átfutni, különben az ötlet hype-vezérelt lesz
- Nem ugorja át a Mindset-et akkor sem, ha "nyilvánvaló" mit kéne építeni

## Fázisok

### 1. fázis — Pillér választás

Kérdezd:

> **"Ezen a héten melyik pilléren dolgozunk?**
> 
> 1) Ügyfélszerzés
> 2) Ügyfélkezelés
> 3) Háttérműködés"

Ha a felhasználó habozik, javasold az `/attekintes` legutóbbi kimenetét referenciaként:

> "A múlt héti audit szerint a leggyengébb cella az [X × Y] volt — érdemes lehet ott elindulni."

Ha nincs előző audit, kérdezd:

> "Mi az ami a legjobban nyomaszt mostanában? Az új ügyfelek hiánya? A meglévők kezelése? Az adminmunka?"

A választott pillért rögzítsd a session memóriájában — minden további kérdés EBBEN a kontextusban értelmezendő.

### 2. fázis — Mindset interjú

A választott pillér kontextusában fuss át a 3 Mindset elemen:

**Default Shift**:
> "Ezen a héten az [pillér]-ben milyen feladatot csináltál 3+ alkalommal? És előtte: kell ezt egyáltalán így csinálni?"

Ha a felhasználó megnevez egy feladatot, mielőtt továbbmész:
> "Várj — szerinted ennek a feladatnak egyáltalán léteznie kell? Ha nem, miért? Ha igen, miért?"

**Function Breakdown**:
> "Bontsuk le ezt a feladatot funkciókra. Lépésről lépésre, mi történik közben? Melyik funkció a tényleges nyűg?"

**Curiosity Rule**:
> "Tudsz olyan AI-eszközről vagy módszerről, amit láttál a múlt héten/hónapban és itt érdekes lehet? Ne válassz még — csak hozd fel."

### 3. fázis — Method interjú

**Find Constraint**:
> "Mi a szűk keresztmetszet konkrétan? Időhiány? Inkonzisztencia? Felejtés? Energia? Tudáshiány?"

**EAD ellenőrzés** (ebben a sorrendben):

1. > "**Eliminálható** ez a feladat egészében? Ha holnap nem csinálnád, mi történne? A világ végét jelenti vagy egy elkerülhető rituálé?"
2. > "Ha nem eliminálható: **automatizálható-e** AI-jal vagy klasszikus workflow-val? Egyértelmű szabályok mentén megy?"
3. > "Ha nem automatizálható: **delegálható-e**? Emberhez (pl. VA) vagy AI-asszisztenshez?"

**Map Process**:
> "Írjuk le 5-10 lépésben, ahogy MA manuálisan csinálod. Ha 5-nél kevesebb, valószínűleg túl egyszerűsíted. Ha 10-nél több, túl bonyolult — bontsd két részre."

**Pick Autonomy Level**:
> "Suggest (javasol, te döntesz), Execute with approval (megcsinálja, de jóváhagyást kér), vagy Autonomous (önállóan fut)? **Most kezdő szint javaslata: Suggest vagy Execute with approval.** Csak akkor menj autonomous-re, ha 10+ alkalommal hibátlanul futott a felügyelet alatt."

**Tie to KPI**:
> "Milyen mérhető mutató javul ettől? Konkrétan: ennyi → ennyi? (Pl. 'ajánlat-készítés 2 óra → 20 perc' vagy 'lead-válaszidő 24 óra → 1 óra'.) Ha nincs mérhető mutató, ne építsd meg."

### 4. fázis — Machine interjú

**Lego Principle**:
> "Bontsuk fel kis darabokra. Min. 3, max 7 modul. Mit csinál mindegyik?"

**Validation Chain**:
> "Hol kell ellenőrizni a kimenetet, mielőtt továbbmegy? Mi a 'csendes hiba' kockázat — hol futhat tovább rosszul anélkül, hogy észrevennéd?"

**Bike Method**:
> "Manuálisan stabilan működik már ez a folyamat? Vagy 'majd a rendszer megoldja'? Ha az utóbbi: **fix-eljük előbb manuálisan**, és csak akkor automatizáljuk, ha 3 alkalommal egymás után hibátlanul lement."

**Intern Rule**:
> "Hogy adnád át ezt egy gyakornoknak az első napján? Ne 'okos kollégaként' bánj az AI-jal — gyakornokként. Ugyanolyan precízen prompt-olj."

**Kill Switch**:
> "Hol és hogyan állítható le, ha elszáll? Konkrétan: rossz outputot küld 50 ügyfélnek — hogy állítod meg 30 másodpercen belül?"

### 5. fázis — Kimenet generálás

Generálj egy struktúrált tervet:

```markdown
## Heti automatizálás: [név]

**Pillér**: [Ügyfélszerzés / Ügyfélkezelés / Háttérműködés]
**Constraint**: [egy mondat]
**EAD szint**: [E / A / D]
**Autonómia**: [Suggest / Execute with approval / Autonomous]
**KPI**: [most → cél]

### Modulok (Lego)
1. [modul név] — [mit csinál] — [eszköz: ?]
2. [modul név] — [mit csinál] — [eszköz: ?]
3. ...

### Validation chain
- [hol kell check] — [hogyan]

### Kill switch
- [hogyan állítjuk le] — [hol a kapcsoló]

### Becsült build idő
[X óra]

### Következő lépés (most, ma)
[konkrét, ma megtehető]

### Sikermérce 4 hét múlva
[konkrét állapot, amit elérnénk]
```

### 6. fázis — Naplózás

Append-old a `decisions/naplo.md` "Aktív bejegyzések" szekciójához:

```
- **YYYY-MM-DD** | /fejlesztes futtatva | Pillér: [X] | Automatizálás: [név] | KPI: [most→cél]
```

### 7. fázis — Záró és számonkérés

Írd ki:
- A teljes terv markdown formátumban
- Egy mondat: "Következő `/fejlesztes`-kor (jövő hét) az első kérdésem lesz: 'megépítetted a [név]-et? Ha nem, miért?'"

Ez a számonkérés szándékos. A `/fejlesztes` lényege a kiszállítás, nem a tervezés.

## Kimenet

Egy darab scope-olt, építhető automatizálás. Egy hét munkája. Nem ötletbörze — implementációs terv.
