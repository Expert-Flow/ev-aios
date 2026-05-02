# A 3Ms Keretrendszer — Operátori Agy AI-munkához

> *A The Three Ms of AI™ Nate Herk védjegye. © 2026 Nate Herk. Itt magyar fordításban szerepel attribúcióval. Nate eredetije: github.com/nateherkai/AIS-OS*

A 3Ms az a gondolkodási keret, ahogy operátorként (vállalkozóként, aki használja az AI-t, nem fejleszti) az AI-hoz nyúlsz. Három M, egymásra épülve: **Mindset → Method → Machine**.

A `/fejlesztes` skill ezen a háromon vezet végig hetente, egy választott pillér kontextusában (lásd `harom-piller.md`).

---

## M1 — Mindset (Gondolkodásmód)

Hogyan állsz hozzá az AI-hoz, mielőtt bármit csinálnál.

### Default Shift
Az alapértelmezett kérdésed ne az legyen: "hogyan csináljam meg?". Az alapértelmezett kérdésed legyen: **"milyen mértékben lehet AI-t használni itt?"**. Ez a gondolkodási mód-váltás. Minden új feladatnál, minden új projektnél ez az első kérdés.

### Function Breakdown
Ne egész munkaköröket próbálj automatizálni. Bontsd le funkciókra. Egy ügyfélszolgálati munkakör nem egy dolog — válaszadás, kategorizálás, eszkaláció, követés, archiválás. Némelyik automatizálható, némelyik nem. **A funkciók szintjén történik a leverage.**

### Curiosity Rule
Maradj kíváncsi. Az AI gyorsabban változik, mint ahogy követni tudod, ezért nem lehet "megtanulni" — folyamatosan kell kísérletezned. Heti egy új eszköz/módszer kipróbálása nem opció, hanem kötelező.

---

## M2 — Method (Módszer)

Ha megvan a Mindset, hogyan döntöd el konkrétan, **mit** automatizálj.

### Find Constraint
Mi a szűk keresztmetszet? Hol akadsz el? Mi az, ami hetente vagy naponta megfojt? Az automatizálás csak akkor ér valamit, ha a constraint-et oldja fel — nem akkor, ha egy random feladatot kapcsol AI-ra.

### EAD: Eliminate, Automate, Delegate
**Ebben a sorrendben.**

1. **Eliminate** — Egyáltalán szükséges ez a feladat? Ha nem, töröld. A nem-megcsinált munka mindig olcsóbb, mint az automatizált munka.
2. **Automate** — Ha szükséges, automatizálható-e? AI-jal vagy klasszikus workflow-val.
3. **Delegate** — Ha nem automatizálható, delegálható-e? Emberhez vagy AI-asszisztenshez.

A legtöbb EV (egyéni vállalkozó) elrontja: rögtön az automate-en kezd. **Először elimináld**, ami eliminálható.

### Map Process
Térképezd fel a folyamatot lépésről lépésre, mielőtt automatizálnád. Ha nem tudod leírni manuálisan 5-10 lépésben, nem tudod automatizálni se.

### Pick Autonomy Level
Mennyire legyen önálló az AI?

- **Suggest** — javasol, te döntesz
- **Execute with approval** — végrehajt, de minden lépésnél jóváhagyást kér
- **Autonomous** — teljesen önállóan fut, csak végeredményt jelent

A legtöbb EV-nek a **suggest** vagy **execute with approval** szint a megfelelő. Ne ugorj autonomous-re csak mert "menő".

### Tie to KPI
Kösd egy konkrét mutatóhoz. Ha nem mérhető, nem tudod hogy működik-e. Példák:

- Ajánlat-készítés időtartama (most 2 óra → 20 perc)
- Lead-válaszidő (most 24 óra → 1 óra)
- Heti adminmunka (most 5 óra → 1 óra)

---

## M3 — Machine (Gép)

Ha tudod **mit** automatizálsz, **hogyan** építsd meg, hogy ne omoljon össze.

### Lego Principle
Kis, cserélhető darabokból építkezz. Ne egyetlen 47-lépéses workflow legyen. Inkább 5 darab 8-10 lépéses workflow, ami egymással kommunikál. **A cserélhetőség = túlélés.**

### Validation Chain
Minden lépés ellenőrizze az előzőt. Ha valami elromlik, kapj jelet, ne hibás végeredményt. Ez a különbség aközött, hogy az AI-d "néha furcsa dolgokat csinál" és aközött, hogy megbízhatóan szállít.

### Bike Method
Először kerékpározz, aztán szerelj rá motort. Soha ne automatizálj olyat, ami manuálisan se működik. Ha az ügyfél-onboarding manuálisan se konzisztens, ne automatizáld — fixáld először.

### Intern Rule
Úgy bánj az AI-jal, mint egy gyakornokkal. Pontos utasítás, ellenőrzés, visszacsatolás. Nem "okos kolléga", hanem "lelkes, de tapasztalatlan beosztott". Ez a hozzáállás megóv a túlbízástól.

### Kill Switch
Mindig legyen kikapcsoló gomb. Ha valami elszáll (rossz email kimegy 200 ügyfélnek, hibás számla generálódik), le tudd állítani gyorsan. Egy automatizálás kill switch nélkül időzített bomba.

---

## Az alaptétel

> **"Boring is beautiful. Workflows beat agents."**

Az unalmas, determinisztikus munkafolyamat majdnem mindig jobb, mint egy "okos" autonóm ágens. Ez ellentétes az iparági hype-pal. De az ügyfeleidnek nem lenyűgöző AI kell — megbízható eredmény.

Kezdd unalmasan. Egészítsd ki autonómiával csak akkor, ha az unalmas szilárdan áll.
