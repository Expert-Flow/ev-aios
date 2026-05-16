# Kapcsolatok

Ez a fájl regiszterel minden eszközt és rendszert, amit az AIOS-od elér VAGY el kéne érnie. A `/bevezetes` tölti ki a Q4-Q7 alapján. A `/attekintes` ellenőrzi mi van bekötve és mi nincs.

---

> **A "Hozzáférés módja" mező lehetséges értékei:**
> - **MCP** — beépített csatlakozó (gyors, biztonságos). Pl. a Számlázz.hu-hoz van ilyen. (MCP = közvetlen csatlakozó az AIOS és egy külső eszköz között — pl. Számlázz.hu.)
> - **API kulcs** — egy hosszú titkos kód, amit be kell másolnod. Egy kicsit körülményes, de sok eszközhöz megy. (API kulcs = hosszú titkos kód, amit be kell másolnod, hogy a rendszerek beszéljenek egymással.)
> - **Kézi** — nincs technikai csatlakozó. Te magad másolod át az adatokat.
> - **Natív** — a Claude Code alapból tudja, semmit nem kell konfigurálnod.

---

## Formátum minden bejegyzéshez

```
### [Eszköz neve]
- **Mire való**: [egy mondat]
- **Pillér**: [Ügyfélszerzés / Ügyfélkezelés / Háttérműködés / Több]
- **Státusz**: [Bekötve / Nincs bekötve / Tervezett]
- **Hozzáférés módja**: [MCP / API kulcs / Kézi / Natív]
- **Utolsó frissítés**: ÉÉÉÉ-HH-NN
```

---

## Példa bejegyzés (törölheted)

### Számlázz.hu
- **Mire való**: számla kiállítás ügyfeleknek
- **Pillér**: Háttérműködés
- **Státusz**: Nincs bekötve
- **Hozzáférés módja**: API kulcs (még nem szerezve)
- **Utolsó frissítés**: 2026-05-02

---

## Bejegyzések

[A `/bevezetes` ide ír a Q4-Q7 alapján.]
