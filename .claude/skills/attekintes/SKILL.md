# /attekintes — Heti Audit (Four Cs × Három Pillér)

## Leírás
Heti rendszer-felülvizsgálat. Két dimenzión értékeli az AIOS-t:

1. **Four Cs** — architektúra rétegei (Context, Connections, Capabilities, Cadence)
2. **Három pillér** — domain területek (ügyfélszerzés, ügyfélkezelés, háttérműködés)

A kettő keresztezve egy 4×3-as mátrixot ad. Minden cellához egy státusz: ✅ kész / 🟡 részleges / 🔴 hiányzó.

**Read-only skill** — csak elemez, nem változtat fájlokat (kivéve a végén egy bejegyzést a `decisions/naplo.md`-ben).

## Mit csinál
- Beolvassa a `context/`, `kapcsolatok.md`, `references/`, `decisions/naplo.md`, és a `.claude/skills/` mappa tartalmát
- Értékeli minden Four Cs réteget mind a három pillér kontextusában
- Ad egy "AIOS érettség" pontszámot 0-12 között (12 cella, 1 pont per ✅, 0.5 per 🟡)
- Javasol 1-3 konkrét hiányt a következő hétre
- Bejegyzést tesz a `decisions/naplo.md`-be

## Mit NEM csinál
- Nem épít skilleket (azt a `/fejlesztes` teszi)
- Nem javít fájlokat
- Nem ad értékelést a vállalkozásról általában — csak az AIOS-rendszerről
- Nem javasol 3-nál több lépést egyszerre (a fókusz fontosabb)

## Fázisok

### 1. fázis — Adatgyűjtés
Olvasd be:
- `context/` minden fájlt
- `kapcsolatok.md`
- `references/` minden fájlt
- `decisions/naplo.md`
- `.claude/skills/` listája (milyen domain skillek vannak már a 3 alapon kívül)

### 2. fázis — Mátrix kitöltés

Töltsd ki a 4×3-as mátrixot:

|                  | Ügyfélszerzés | Ügyfélkezelés | Háttérműködés |
|------------------|---------------|---------------|---------------|
| **Context**      | ✅/🟡/🔴      | ✅/🟡/🔴      | ✅/🟡/🔴      |
| **Connections**  | ✅/🟡/🔴      | ✅/🟡/🔴      | ✅/🟡/🔴      |
| **Capabilities** | ✅/🟡/🔴      | ✅/🟡/🔴      | ✅/🟡/🔴      |
| **Cadence**      | ✅/🟡/🔴      | ✅/🟡/🔴      | ✅/🟡/🔴      |

**Definíciók**:

- **Context** — az AIOS tudja-e mit csinálsz ezen a pilléren?
  - ✅ ha a `context/` fájlokban explicit infó van erről a pillérről
  - 🟡 ha általános, de pillér-specifikus részlet hiányzik
  - 🔴 ha nincs említve

- **Connections** — bekötött eszköz van-e ezen a pilléren?
  - ✅ ha legalább 1 eszköz "Bekötve" státuszban a `kapcsolatok.md`-ben
  - 🟡 ha "Tervezett" vagy "Nincs bekötve" de ismert
  - 🔴 ha semmi nincs említve

- **Capabilities** — van-e már skill ami ezen a pilléren működik?
  - ✅ ha van legalább 1 domain skill ezen a pilléren
  - 🟡 ha az alap 3 (`/bevezetes`/`/attekintes`/`/fejlesztes`) érinti, de nincs domain skill
  - 🔴 soha — az alap 3 mindig érinti, ezért minimum 🟡

- **Cadence** — fut-e magától valami rendszeresen ezen a pilléren?
  - ✅ ha van automatizálás ami magától fut (cron, webhook, scheduled task)
  - 🟡 ha van skill, de manuálisan kell hívni
  - 🔴 ha nincs cadence

### 3. fázis — Pontszám és diagnózis
- **Pontszám**: hány ✅ van? (1 pont) + hány 🟡 (0.5 pont) = `X / 12`
- **Erősség**: melyik pilléren és melyik rétegben állsz a legjobban?
- **Gyengeség**: melyik a leggyengébb cella?
- **Trend** (ha van korábbi audit a `decisions/naplo.md`-ben): nőtt / stagnál / csökkent?

### 4. fázis — Javaslat
Adj **1-3 konkrét lépést** a következő hétre. Minden lépés egy darab — ne dump-olj 10 ötletet. 

Formátum:

```
**Javaslat 1:** [Cella] — [konkrét lépés]
Miért: [egy mondat]
Skill: [ez `/fejlesztes`-be való vagy önálló task]
```

Példa:
> **Javaslat 1:** Connections × Háttérműködés — kösd be a Számlázz.hu API-t MCP-n keresztül.
> Miért: a számlázás manuálisan most a legnagyobb időrabló a Q7 alapján.
> Skill: önálló task — építsd meg ezen a héten.

### 5. fázis — Naplózás

Append-old a `decisions/naplo.md` "Aktív bejegyzések" szekciójához:

```
- **YYYY-MM-DD** | /attekintes futtatva | Pontszám: X/12 | Top javaslat: [első javaslat egy mondatban]
```

### 6. fázis — Záró
Írd ki:
- A teljes mátrixot
- A pontszámot és trendet
- Az 1-3 javaslatot
- Egy mondatot: "A következő `/fejlesztes`-en érdemes a [legjobb javaslat pillére] pillérre fókuszálni."

## Kimenet
Egy értelmes, hetente nézhető riport, ami megmutatja merre nősz és hol akadsz el. Nem ítélet — irányjelző.
