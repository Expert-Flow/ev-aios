# EV-AIOS — AI Operációs Rendszer Egyéni Vállalkozóknak

> *Hungarian solo entrepreneur AI Operating System starter kit for Claude Code. Inspired by [Nate Herk's AIS-OS](https://github.com/nateherkai/AIS-OS) and adapted for the Hungarian solo service provider market by [Solo Business](https://solobusiness.hu).*

A te személyes AI-rendszered Claude Code-ban: egy mappa-csomag, ami a Claude-ot a vállalkozásod **gondolkodótársává** alakítja. Magyar egyéni vállalkozóknak — jogászoknak, könyvelőknek, coachoknak, fotósoknak, terapeutáknak, fordítóknak.

A sablon a `/bevezetes` interjún keresztül személyre szabódik, majd két visszatérő skill (`/attekintes` és `/fejlesztes`) tartja építés alatt hétről hétre. Az "AIOS" a mi saját rövidítésünk erre a rendszerre (AIOS = AI Operációs Rendszer — a mi saját szavunk erre a sablonra). Szabadon felhasználható (MIT-licenc).

---

## Mielőtt letöltöd — szükséged van-e először az EV-Alap-ra?

Az EV-AIOS `/bevezetes` skill Q1-e ezt kérdezi: **"Ki vagy, mit adsz el, kinek?"**

Ha **nem tudod 60 másodperc alatt válaszolni** erre — vagy ha válaszolsz, de te magad sem hiszed teljesen — akkor MIELŐTT letöltöd ezt a repo-t, először csináld végig az **[EV-Alap](https://github.com/Expert-Flow/EV-Alap)** brand discovery repo-t.

Az EV-Alap egy 10 kérdéses interjú 4 fázisban (TE, ÜGYFÉL, HANG, AJÁNLAT — ebben a sorrendben), kb. 60-90 perc. A végén egy átemelhető fájl-csomagot ad, amit egy az egyben beolvasol ide. Az EV-AIOS akkor lesz **pontos és hangolt**, ha alatta már tiszta identitás és ICP (ideális ügyfél-profil) áll.

> **Önteszt:** Ha az `ev-intake.md` Q1-et kitöltöd 30 másodperc alatt világosan és magabiztosan — kezdj itt. Ha homályosabb, mint szeretnéd — előbb [EV-Alap](https://github.com/Expert-Flow/EV-Alap), aztán EV-AIOS.

---

## Ellenőrző kérdés

> **"Miközben nem ülsz a géped előtt, az AI rendszered figyel valamit, ami a vállalkozásodban történik — és kimenetet készít, ami gyorsabb és pontosabb, mint amit te magad csinálnál."**

Például: éjszaka megérkezik egy ügyfélkérdés Messengeren. Az AIOS-od reggelre kész egy válasz-vázlatot a TE hangoddal — te csak átolvasod és elküldöd.

Vagy: minden héten péntek 16:00-kor magától kiszámolja az aktuális bevételeket, megmondja melyik ügyfélnek lejár a fizetési határideje, és megírja az emlékeztető emailt.

Minden tervezési döntés ezen a próbán múlik. Ha egy réteg, skill, vagy sablon nem járul hozzá ehhez, nem kerül be.

---

## Két gondolkodási keret + Három téma

### A 3Ms — Hogyan gondolkodj az AI-ról

A keret 3 lépcsője:

- **Gondolkodásmód (Mindset)** — Az első kérdés mindig: *"Milyen mértékben lehet AI-t használni itt?"*
- **Módszer (Method)** — A munkáidat lebontod kis darabokra, és minden darabra eldöntöd: kihagyható, gépesíthető vagy emberi.
- **Gép (Machine)** — Kis, ellenőrizhető, megbízható darabokból építkezel — nem nagy, "okos" rendszerekből.

Részletek: [references/3ms-keretrendszer.md](./references/3ms-keretrendszer.md). A `/fejlesztes` skill ezen vezet végig hetente.

*(A 3Ms keret Nate Herk munkája — itt magyar fordításban szerepel. © 2026 Nate Herk.)*

### A három pillér — Hol alkalmazd

| # | Pillér | Mit jelent |
|---|---|---|
| 1 | **Ügyfélszerzés** | Minden ami ügyféllé válás előtt történik |
| 2 | **Ügyfélkezelés** | Minden ami az ügyfélkapcsolat alatt történik |
| 3 | **Háttérműködés** | Pénzügy, admin, időbeosztás, tudásmenedzsment |

Részletes lebontás: [references/harom-piller.md](./references/harom-piller.md). A `/fejlesztes` minden héten egy pillérre fókuszál.

### Hogyan kapcsolódik a kettő

A 3Ms a **HOGYAN**. A három pillér a **HOL**. Egy hét = egy pillér + egy 3Ms-en átfutott automatizálási darab.

---

## A három skill

| Skill | Típus | Mikor futtasd |
|---|---|---|
| `/bevezetes` | Bevezető varázsló (egyszeri) | 1. nap, letöltés után. 7 kérdés interjú. Generálja az 1. napi fájl-csomagot + kitölti a `CLAUDE.md`-t. |
| `/attekintes` | Visszatérő audit | 7. nap, aztán hetente. 4 K (Kontextus, Kapcsolatok, Képességek, Ritmus) × Három pillér mátrix. Csak olvas, nem ír. |
| `/fejlesztes` | Visszatérő építés | 14. nap, aztán hetente. 3Ms interjú egy pillérre. Egy futtatás = egy automatizálás. |

---

## Gyors kezdés

1. **Töltsd le a repo-t.** GitHub zöld **Code** gomb, majd **Download ZIP**. Csomagold ki a mappádba (pl. Asztalra).

2. **Még előtte: ha nincs Claude Code-od**, telepítsd innen: [claude.com/claude-code](https://claude.com/claude-code).

3. **Nyisd meg a Terminált.** (A Terminál egy szövegalapú felület, ahol parancsokkal beszélsz a géppel — kezdetben furcsa, de pár nap alatt megszokod.)
   - Mac-en: nyomd a `Cmd + Space` gombot, írd be: `Terminal`, nyomj Entert.
   - Windows-on: Start menü, írd be: `Parancssor` (vagy PowerShell), nyomj Entert.

4. **Lépj be a letöltött mappába.** Másold be (a `~` a saját felhasználói mappádat jelenti, így bárhonnan működik):
   ```
   cd ~/Desktop/EV-AIOS
   ```

5. **Indítsd a Claude Code-ot:**
   ```
   claude
   ```

6. **Töltsd ki az `ev-intake.md`-t.** Vagy egyszerűbben: indítsd a `/bevezetes`-t, és a Claude végigkérdezi élőben (te csak válaszolsz). Kb. 60-90 perc, megszakítható-folytatható.

7. **Használd egy hetet.** Hozz valós kérdéseket, döntéseket. A döntéseket az AI a `decisions/naplo.md`-be naplózza.

8. **7. nap:** futtasd `/attekintes`-t. Megnézed milyen "rétegek" hiányoznak a rendszeredből.

9. **14. nap:** futtasd `/fejlesztes`-t. Megépítesz EGY automatizmust egy témára.

10. **3. héttől:** heti `/fejlesztes` rituálé. Egy automatizmus / hét.

> **Elakadtál?** Nézd meg a [GYIK.md](GYIK.md)-t (gyakori kérdések, hibaelhárítás) és a [glosszárium](glosszarium.md)-ot (fogalmak magyarul).

---

## Repo struktúra

```
EV-AIOS/
├── README.md
├── GYIK.md                          ← Gyakori kérdések + hibaelhárítás (ha elakadsz)
├── glosszarium.md                   ← Minden fogalom egy mondatban magyarázva
├── CLAUDE.md                        ← Az operátori manuálod (a /bevezetes tölti ki)
├── BOVITESEK.md                     ← Mit adj hozzá ahogy nősz
├── LICENSE
├── .gitignore
├── ev-intake.md                     ← A /bevezetes forrás-fájlja. Bármikor szerkeszd, újrafuttasd.
├── kapcsolatok.md                   ← Minden rendszer nyilvántartása, amit az AIOS elér
├── context/                         ← Rólad, a vállalkozásodról (a /bevezetes tölti)
├── references/
│   ├── 3ms-keretrendszer.md         ← Operátori agy (Nate Herk 3Ms)
│   ├── harom-piller.md              ← Domain térkép (Solo Business 3 pillér)
│   └── voice.md                     ← Szó szerinti hangminták (a /bevezetes tölti)
├── decisions/
│   └── naplo.md                     ← Döntésnapló, amit csak hozzáfűzöl (sose írsz át)
├── archives/                        ← Régi cuccok. Ne töröld. Ide mozgasd.
└── .claude/
    └── skills/
        ├── bevezetes/SKILL.md
        ├── attekintes/SKILL.md
        └── fejlesztes/SKILL.md
```

A `BOVITESEK.md`-ben olvasd el, mit érdemes hozzáadni ahogy nősz (`projektek/`, `templates/`, domain skillek, sub-OS mappák stb.).

---

## Licenc + Attribúció

Szabadon felhasználható (MIT-licenc).

A The Three Ms of AI™ Nate Herk védjegye. © 2026 Nate Herk. A keret magyar fordításban, attribúcióval szerepel ebben a repo-ban — szabadon használható, de ne csomagold át sajátként.

A három pillér (Ügyfélszerzés / Ügyfélkezelés / Háttérműködés) a [Solo Business](https://solobusiness.hu) saját kerete.

Eredeti angol AIS-OS: [github.com/nateherkai/AIS-OS](https://github.com/nateherkai/AIS-OS)
