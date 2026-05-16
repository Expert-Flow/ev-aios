# Bővítések — Mit Adhatsz Hozzá Ahogy Nősz

Ez a sablon szándékosan minimális. Három skill (`/bevezetes`, `/attekintes`, `/fejlesztes`), három pillér, két keretrendszer. A többi a TE rendszered, amit te építesz hozzá ahogy a vállalkozásod nő.

Itt felsorolom mit érdemes mérlegelni, MIKOR és MIÉRT.

---

## Domain skillek (.claude/skills/)

Ezek konkrét eljárásrendek (SOP-k, vagyis szabványos munkafolyamatok) egy-egy ismétlődő munkafolyamatra. Csak akkor építsd meg, ha **3+ alkalommal csináltad már manuálisan**, és tudod hogy néz ki jól.

### Ügyfélszerzés
- **`/ajanlat-keszites`** — egyedi árajánlat összeállítása brief alapján
- **`/lead-valasz`** — első üzenet hideg vagy meleg érdeklődőnek (lead = potenciális ügyfél)
- **`/utankoveto`** — elveszett érdeklődő visszahúzása
- **`/discovery-call-prep`** — felfedező hívás felkészülése
- **`/landing-testreszabas`** — A kész HTML-sablonba (lásd: `EV-Alap/sablonok/landing-oldal/`) beilleszti a saját szövegeidet a `context/icp.md` és `context/ajanlat.md` alapján. Kevesebb Claude-munka kell, mert nem nulláról ír oldalt, csak a helyettesítő szövegeket cseréli ki.

### Ügyfélkezelés
- **`/onboarding`** — új ügyfél bevezetése: először szerződés, aztán hozzáférések, végül bevezető beszélgetés (kickoff hívás)
- **`/heti-statusz`** — projekt státusz-email automatikus piszkozata
- **`/projekt-zaras`** — projekt lezárás + ajánlás-kérés
- **`/talalkozo-osszefoglalo`** — találkozó-átiratból (transcript) elkészíti a következő lépések listáját és egy emailt

### Háttérműködés
- **`/szamlazas`** — projektzárás után számla automatikus generálása
- **`/fizetesi-emlekezteto`** — időzített, hangolt emlékeztetők
- **`/heti-attekintes`** — operatív heti áttekintés generálása
- **`/negyedeves-tervezes`** — Q-zárás és új Q-tervezés

**Mikor építsd:** amikor a `/fejlesztes` skill javasolja, hogy egy konkrét munkafolyamat ismétlődik. Nem előtte.

---

## Új mappák

### `projektek/`
Aktív ügyfél-projektek külön fájlokkal. Egy fájl = egy projekt. Ügyfél kontaktja, a feladat határai (scope), határidők, státusz, feljegyzések.

**Mikor:** amikor egynél több aktív ügyfeled van egyszerre.

### `templates/`
Ismétlődő dokumentum-sablonok. Szerződés, NDA, ajánlat-sablon, onboarding-csomag.

**Mikor:** amikor 2-3 alkalommal írtál ugyanolyan struktúrájú dokumentumot.

### `negyedeves/`
Negyedéves áttekintések, mérhető célok, tervek. Egy fájl negyedévenként.

**Mikor:** amikor 3+ hónapja használod aktívan az AIOS-t és van értelmes mennyiségű döntés a `decisions/naplo.md`-ben.

### `tanulasi-naplo/`
Mit tanultál hetente AI-ról, vállalkozásról, ügyfelekről. Ez a "második agy" alap.

**Mikor:** azonnal ha tanuló alkat vagy. Sose ha nem.

---

## Több referencia

### `references/icp-detalt.md`
Részletes ICP profil — fájdalompontok, vásárlói út, döntési kritériumok, kifogások.

**Mikor:** amikor 5+ ügyfél után mintázatokat kezdesz látni.

### `references/eszkozok.md`
Eszközök listája kategóriánként, miért választottad őket, mikor cserélnéd le.

**Mikor:** amikor 5+ aktív eszközöd van.

### `references/szakmai-tudas.md`
A te szakmai tudásbázisod — alapelvek, módszerek, csak nálad lévő insightok.

**Mikor:** amikor szeretnél olyan tartalmat csinálni (poszt, videó, podcast), ami a saját hangodon szól.

---

## Sub-OS mappák (haladó)

Ha ügyfeleidnek is építesz AIOS-t (pl. Solo Business ügyfeleknek), érdemes lehet:

### `ugyfel-aios/`
Egy mappa minden ügyfélnek, aki saját AIOS-t kapott tőled. Itt tartod az élesbe rakott (deployolt) verziót, az ő `ev-intake.md`-jüket, az ő testreszabásukat.

**Mikor:** amikor a 3. ügyfélnek szállítasz AIOS-alapú megoldást.

---

## .claude/agents/

Claude Code AI-segédek (agentek) — önállóan futó, célzott AI-asszisztensek egy-egy konkrét feladatra. Ez a Lego-elv legmagasabb szintje.

**Mikor:** amikor 5+ skill van már, és kezded látni hogy egyes skillek "összetartoznak" egy nagyobb funkcióba.

---

## Aranyszabály

> **Csak azt építsd meg, amit a `/fejlesztes` skill javasol.**

Ne építs előre. Ne másold másokat. Az AIOS-od pontosan annyi, amennyit használsz — minden más fél.
