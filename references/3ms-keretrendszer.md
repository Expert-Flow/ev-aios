# A 3Ms Keretrendszer — Operátori Agy AI-munkához

> *A The Three Ms of AI™ Nate Herk védjegye. © 2026 Nate Herk. Itt magyar fordításban szerepel attribúcióval. Nate eredetije: github.com/nateherkai/AIS-OS*

A 3Ms az a gondolkodási keret, ahogy operátorként (vállalkozóként, aki használja az AI-t, nem fejleszti) az AI-hoz nyúlsz. Három M, egymásra épülve, ebben a sorrendben:

1. **Gondolkodásmód (Mindset)**
2. **Módszer (Method)**
3. **Gép (Machine)**

A `/fejlesztes` skill ezen a háromon vezet végig hetente, egy választott pillér kontextusában (lásd `harom-piller.md`).

---

## M1 — Gondolkodásmód (Mindset)

Hogyan állsz hozzá az AI-hoz, mielőtt bármit csinálnál.

### Alapértelmezett kérdés-csere (Default Shift)
Az alapértelmezett kérdésed ne az legyen: "hogyan csináljam meg?". Az alapértelmezett kérdésed legyen: **"milyen mértékben lehet AI-t használni itt?"**. Ez a gondolkodási mód-váltás. Minden új feladatnál, minden új projektnél ez az első kérdés.

### Feladat-lebontás (Function Breakdown)
Ne egész munkaköröket próbálj automatizálni. Bontsd le funkciókra. Egy ügyfélszolgálati munkakör nem egy dolog — válaszadás, kategorizálás, eszkaláció, követés, archiválás. Némelyik automatizálható, némelyik nem. **A funkciók szintjén történik a tényleges előrelépés.**

### Kíváncsisági szabály (Curiosity Rule)
Maradj kíváncsi. Az AI gyorsabban változik, mint ahogy követni tudod, ezért nem lehet "megtanulni" — folyamatosan kell kísérletezned. Heti egy új eszköz/módszer kipróbálása nem opció, hanem kötelező.

---

## M2 — Módszer (Method)

Ha megvan a Gondolkodásmód, hogyan döntöd el konkrétan, **mit** automatizálj.

A teljes Módszer sorrendje:

1. **Szűk keresztmetszet keresése** (Find Constraint)
2. **Selejtez / Automatizál / Delegál** — SAD (angolul EAD)
3. **Folyamat-térkép** (Map Process)
4. **Önállósági szint választása** (Pick Autonomy Level)
5. **Mérhető célhoz kötés** — KPI (Tie to KPI)

### Szűk keresztmetszet keresése (Find Constraint)
Mi a szűk keresztmetszet? Hol akadsz el? Mi az, ami hetente vagy naponta megfojt? Az automatizálás csak akkor ér valamit, ha a szűk keresztmetszetet oldja fel — nem akkor, ha egy random feladatot kapcsol AI-ra.

### SAD: Selejtez / Automatizál / Delegál (EAD: Eliminate, Automate, Delegate)
**Ebben a sorrendben.**

1. **Selejtez (Eliminate)** — Egyáltalán szükséges ez a feladat? Ha nem, töröld. A nem-megcsinált munka mindig olcsóbb, mint az automatizált munka.
2. **Automatizál (Automate)** — Ha szükséges, automatizálható-e? AI-jal vagy klasszikus munkafolyamattal.
3. **Delegál (Delegate)** — Ha nem automatizálható, delegálható-e? Emberhez vagy AI-asszisztenshez.

A legtöbb EV (egyéni vállalkozó) elrontja: rögtön az "automatizál"-on kezd. **Először selejtezd**, ami selejtezhető.

### Folyamat-térkép (Map Process)
Térképezd fel a folyamatot lépésről lépésre, mielőtt automatizálnád. Ha nem tudod leírni manuálisan 5-10 lépésben, nem tudod automatizálni se.

### Önállósági szint választása (Pick Autonomy Level)
Mennyire legyen önálló az AI?

- **Javasol (Suggest)** — javasol, te döntesz
- **Jóváhagyással végrehajt (Execute with approval)** — végrehajt, de minden lépésnél jóváhagyást kér
- **Önállóan fut (Autonomous)** — teljesen önállóan fut, csak végeredményt jelent

A legtöbb EV-nek a **Javasol** vagy **Jóváhagyással végrehajt** szint a megfelelő. Ne ugorj **Önállóan fut**-ra csak mert "menő".

### Mérhető célhoz kötés (Tie to KPI)
Kösd egy konkrét, mérhető mutatóhoz (KPI). Ha nem mérhető, nem tudod hogy működik-e. Példák:

- Ajánlat-készítés időtartama (most 2 óra, cél 20 perc)
- Érdeklődő-válaszidő (most 24 óra, cél 1 óra)
- Heti adminmunka (most 5 óra, cél 1 óra)

---

## M3 — Gép (Machine)

Ha tudod **mit** automatizálsz, **hogyan** építsd meg, hogy ne omoljon össze.

### Lego-elv (Lego Principle)
Kis, cserélhető darabokból építkezz. Ne egyetlen 47-lépéses munkafolyamat legyen. Inkább 5 darab 8-10 lépéses munkafolyamat, ami egymással kommunikál. **A cserélhetőség = túlélés.**

### Ellenőrzési lánc (Validation Chain)
Minden lépés ellenőrizze az előzőt. Ha valami elromlik, kapj jelet, ne hibás végeredményt. Ez a különbség aközött, hogy az AI-d "néha furcsa dolgokat csinál" és aközött, hogy megbízhatóan szállít.

### Bicikli-módszer (Bike Method)
Először kerékpározz, aztán szerelj rá motort. Soha ne automatizálj olyat, ami manuálisan se működik. Ha az ügyfél-onboarding manuálisan se konzisztens, ne automatizáld — fixáld először.

### Gyakornok-szabály (Intern Rule)
Úgy bánj az AI-jal, mint egy gyakornokkal. Pontos utasítás, ellenőrzés, visszacsatolás. Nem "okos kolléga", hanem "lelkes, de tapasztalatlan beosztott". Ez a hozzáállás megóv a túlbízástól.

### Vészkapcsoló (Kill Switch)
Mindig legyen kikapcsoló gomb. Ha valami elszáll (rossz email kimegy 200 ügyfélnek, hibás számla generálódik), le tudd állítani gyorsan. Egy automatizálás vészkapcsoló nélkül időzített bomba.

---

## Az alaptétel

> **"Az unalmas a szép. A munkafolyamatok jobbak, mint az AI-segédek."**
> *("Boring is beautiful. Workflows beat agents.")*

Az unalmas, kiszámítható munkafolyamat majdnem mindig jobb, mint egy "okos" önállóan futó AI-segéd. Ez ellentétes az iparági divattal. De az ügyfeleidnek nem lenyűgöző AI kell — megbízható eredmény.

Kezdd unalmasan. Egészítsd ki önállóbb működéssel csak akkor, ha az unalmas szilárdan áll.
