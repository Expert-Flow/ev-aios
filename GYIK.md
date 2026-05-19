# GYIK — Gyakori kérdések és hibaelhárítás

Ha elakadsz, itt keresd a választ először. A kérdések abban a sorrendben vannak, ahogy egy kezdő általában találkozik velük.

---

## Hol tartok? — Az út két lépése

```
1. EV-Alap          →   tisztázod ki vagy, kinek, mit adsz el
   (külön repó)         10 kérdés, kb. 60-90 perc
        │
        ▼  a kész fájlokat átmásolod
        │
2. EV-AIOS          →   ez itt: az AI operációs rendszered
   (ez a repó)          /bevezetes, majd hetente /attekintes + /fejlesztes
```

Ha az EV-Alap-ot még nem csináltad meg és nem tudod 60 másodperc alatt megmondani ki vagy és kinek dolgozol — előbb azt járd végig. Ha tiszta, kezdj itt.

---

## Telepítés és indulás

### Mi az a terminál, és hogyan nyitom meg?

A terminál egy szövegalapú felület, ahol parancsokkal beszélsz a géppel. Kezdetben furcsa, pár nap alatt megszokod.

- **Mac:** nyomd a `Cmd + Space` gombot, írd be: `Terminal`, nyomj Entert.
- **Windows:** Start menü, írd be: `Parancssor`, nyomj Entert.

### A `claude` parancsot beírtam, de „command not found" a válasz

Ez azt jelenti, hogy a Claude Code még nincs telepítve a gépeden. Telepítsd innen: [claude.com/claude-code](https://claude.com/claude-code). A telepítés után zárd be és nyisd újra a terminált, majd próbáld újra.

### A `cd ~/Desktop/EV-AIOS` parancs „No such file or directory" hibát ad

A letöltött mappa nem ott van, ahol a parancs keresi. Nézd meg a Finderben (Mac) vagy a Fájlkezelőben (Windows), hova csomagoltad ki, és írd át az útvonalat. Ha az Asztalon van, de a mappa neve más (pl. `EV-AIOS-main`), akkor `cd ~/Desktop/EV-AIOS-main`.

### Hogyan futtatok egy skillt?

A Claude Code-ban (miután elindult a `claude` paranccsal) írd be a skill nevét perjellel: `/bevezetes`, majd nyomj Entert. A Claude ekkor elindítja a skillt és vezetni kezd.

---

## A `/bevezetes` interjú

### Nem értek egy kérdést — mit tegyek?

Írd be a Claude-nak, hogy „nem értem ezt a kérdést" vagy „mondj rá egy példát". A skill átfogalmazza vagy példát ad. Nincs rossz válasz — a cél a tisztázás, nem a vizsga.

### A `context/` mappa üres. Ez baj?

Nem. A `context/` fájlokat (`en-magam.md`, `icp.md`, `ajanlat.md`, `szemelyes.md`, `prioritasok.md`) a `/bevezetes` skill tölti fel az interjú alapján. Indulás előtt üresek — ez normális.

### Elrontottam valamit az interjúban. Újrakezdhetem?

Igen. Szerkeszd kézzel az `ev-intake.md` fájlt, vagy futtasd újra a `/bevezetes`-t. A skill megkérdezi, hogy a meglévő fájlokat felülírja, egybeolvassza vagy érintetlenül hagyja.

### Mennyi időt vegyek rá?

Számíts 60-90 percre. Nem kell egyben végigcsinálni — több ülésre is oszthatod.

---

## A heti ritmus

### Mikor melyik skillt futtassam?

- **1. nap:** `/bevezetes` — egyszeri beállítás.
- **7. nap:** `/attekintes` — első heti audit. Megmutatja, melyik réteg hiányzik a rendszeredből.
- **14. naptól hetente:** `/fejlesztes` — egy automatizálás, megtervezve.

A `/attekintes` csak elemez, semmit nem ír át (egy napló-bejegyzést kivéve). Bátran futtasd.

### Mi van, ha kihagyok egy hetet?

Semmi baj. Az AIOS nem büntet. Folytasd ott, ahol abbahagytad — futtass egy `/attekintes`-t, hogy lásd hol tartasz.

---

## Általános

### Mi a különbség az EV-Alap és az EV-AIOS között?

Az **EV-Alap** tisztázza, hogy ki vagy és kinek dolgozol — ez az alap. Az **EV-AIOS** (ez a repó) erre az alapra épít egy működő AI-rendszert. Az EV-Alap egyszeri, az EV-AIOS folyamatosan használt.

### Feltölthetem a kitöltött repót GitHubra?

Csak ha a repó **privát**. A `context/` fájlok a kitöltés után a személyes és üzleti adataidat tartalmazzák. Publikus repóba ne kerüljenek.

### Még nem találom a választ

Nézd meg a [glosszáriumot](glosszarium.md) a fogalmakhoz, vagy írd meg a Claude-nak a problémát a saját szavaiddal — gyakran ő is segít.
