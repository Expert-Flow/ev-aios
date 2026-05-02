# EV-AIOS — AI Operációs Rendszer Egyéni Vállalkozóknak

> *Hungarian solo entrepreneur AI Operating System starter kit for Claude Code. Inspired by [Nate Herk's AIS-OS](https://github.com/nateherkai/AIS-OS) and adapted for the Hungarian solo service provider market by [Expert Flow](https://expertflow.hu).*

Egy ingyenes, MIT-licenszelt sablon, ami a Claude Code-ot a személyes **AI Operációs Rendszereddé (AIOS)** alakítja. **Célközönség**: magyar egyéni vállalkozók és szolgáltatók (jogászok, könyvelők, coachok, fotósok, terapeuták, fordítók, dizájnerek, szövegírók, virtuális asszisztensek).

A sablon a `/bevezetes` interjú során személyre szabódik, majd két visszatérő gondolkodási skill (`/attekintes`, `/fejlesztes`) tartja építés alatt hétről hétre.

---

## A litmusz teszt

> **"Miközben nem ülsz a géped előtt, az EV-AIOS-od megfigyel egy valós eseményt és kimenetet készít, ami gyorsabb és pontosabb, mint amit te magad készítenél."**

Minden tervezési döntés ezen a teszten múlik. Ha egy réteg, skill, vagy sablon nem járul hozzá ehhez, nem kerül be.

---

## Két keret + Három pillér

### A 3Ms — Operátori agy (HOGYAN gondolkodj)

| M | Egy mondatban |
|---|---|
| **Mindset** | Default Shift, Function Breakdown, Curiosity Rule. *Milyen mértékben lehet AI-t használni itt?* |
| **Method** | Find Constraint → EAD (Eliminate, Automate, Delegate) → Map Process → Pick Autonomy → Tie to KPI |
| **Machine** | Lego Principle, Validation Chain, Bike Method, Intern Rule, Kill Switch. *Boring is beautiful. Workflows beat agents.* |

Részletes lebontás: `references/3ms-keretrendszer.md`. A `/fejlesztes` skill ezen vezet végig hetente.

> *A The Three Ms of AI™ Nate Herk védjegye. © 2026 Nate Herk. Itt magyar fordításban szerepel attribúcióval.*

### A három pillér — Domain térkép (HOL alkalmazd)

| # | Pillér | Mit jelent |
|---|---|---|
| 1 | **Ügyfélszerzés** | Minden ami ügyféllé válás előtt történik |
| 2 | **Ügyfélkezelés** | Minden ami az ügyfélkapcsolat alatt történik |
| 3 | **Háttérműködés** | Pénzügy, admin, időbeosztás, tudásmenedzsment |

Részletes lebontás: `references/harom-piller.md`. A `/fejlesztes` minden héten egy pillérre fókuszál.

### Hogyan kapcsolódik a kettő

A 3Ms a **HOGYAN**. A három pillér a **HOL**. Egy hét = egy pillér + egy 3Ms-en átfutott automatizálási darab.

---

## A három skill

| Skill | Típus | Mikor futtasd |
|---|---|---|
| `/bevezetes` | Setup varázsló (egyszeri) | 1. nap, klónozás után. 7 kérdés interjú. Generálja az 1. napi fájl-csomagot + kitölti a `CLAUDE.md`-t. |
| `/attekintes` | Visszatérő audit | 7. nap, aztán hetente. Four Cs × Három pillér mátrix. Read-only. |
| `/fejlesztes` | Visszatérő építés | 14. nap, aztán hetente. 3Ms interjú egy pillérre. Egy futás = egy automatizálás. |

---

## Quick start

1. **Klónozd** vagy fork-old ezt a repo-t egy munkamappába a gépeden.
2. **Nyisd meg Claude Code-ban**: `cd ev-aios && claude`
3. **Töltsd ki az `ev-intake.md`-t** (7 kérdés, 60 mp/kérdés). Vagy futtasd a `/bevezetes`-t üresen, és interaktívan végigkérdezi.
4. **Használd egy hétig.** Hozz valós kérdéseket, döntéseket. Logold a `decisions/naplo.md`-be.
5. **7. nap:** futtasd `/attekintes`-t. Olvasd a Four Cs × pillér mátrixot. Válassz ki egy hiányt.
6. **14. nap:** futtasd `/fejlesztes`-t. A 3Ms interjú egy építhető automatizálást ad. Építsd meg.
7. **3. héttől:** heti `/fejlesztes` rituálé. Egy automatizálás hetente.

---

## Repo struktúra

```
EV-AIOS/
├── README.md
├── CLAUDE.md                        ← Az operátori manuálod (a /bevezetes tölti ki)
├── BOVITESEK.md                     ← Mit adj hozzá ahogy nősz
├── LICENSE
├── .gitignore
├── ev-intake.md                     ← A /bevezetes forrás-fájlja. Bármikor szerkeszd, újrafuttasd.
├── kapcsolatok.md                   ← Minden rendszer regisztere, amit az AIOS elér
├── context/                         ← Rólad, a vállalkozásodról (a /bevezetes tölti)
├── references/
│   ├── 3ms-keretrendszer.md         ← Operátori agy (Nate Herk 3Ms)
│   ├── harom-piller.md              ← Domain térkép (Expert Flow 3 pillér)
│   └── voice.md                     ← Verbatim hangminták (a /bevezetes tölti)
├── decisions/
│   └── naplo.md                     ← Append-only döntésnapló
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

MIT Licenc.

A The Three Ms of AI™ Nate Herk védjegye. © 2026 Nate Herk. A keret magyar fordításban, attribúcióval szerepel ebben a repo-ban — szabadon használható, de ne csomagold át sajátként.

A három pillér (Ügyfélszerzés / Ügyfélkezelés / Háttérműködés) az [Expert Flow](https://expertflow.hu) saját kerete.

Eredeti angol AIS-OS: [github.com/nateherkai/AIS-OS](https://github.com/nateherkai/AIS-OS)
