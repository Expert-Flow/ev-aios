# EV-AIOS Bevezető Kérdőív

Ez a fájl az AI Operációs Rendszered forrásdokumentuma. Töltsd ki gépeléssel, hangbevitellel (Wispr Flow / Mac diktálás / Whisper), vagy futtasd a `/bevezetes` skillt egy vezetett beszélgetéshez. Bárhogy is csinálod, ezt a fájlt olvassa be a `/bevezetes` és ebből generálja le az 1. napi alapfájl-csomagot.

**Kemény limit: 7 kérdés.** Minden kérdés 60 másodperc alatt megválaszolható. Ne túlgondold — bármikor szerkesztheted és újrafuttathatod a `/bevezetes`-t.

---

## Q1 — Ki vagy, mit adsz el, kinek?

Identitás, ajánlat, ICP (ideális ügyfél). Egy bekezdés mindegyikre elég.

```
[A te válaszod]
```

---

## Q2 — Illessz be 1-2 saját szöveget, amit nemrég írtál. Ne szerkeszd át.

Egy email, egy LinkedIn poszt, egy Messenger üzenet, egy dokumentum — bármi, ami úgy hangzik, ahogy te beszélsz, amikor nem próbálkozol. **Verbatim illeszd be.** Ne gépeld be Claude-dal beszélgetés közben — a chat-formájú minták rosszabbak, mint a semmilyen minta (hangelszennyeződés).

```
[Minta 1 — verbatim]
```

```
[Minta 2 — verbatim]
```

---

## Q3 — Mi a 2-3 legnagyobb prioritásod a következő 90 napra?

Negyedéves prioritások. Nem éves álmok. Olyan dolgok, amik ha július végéig nem készülnek el, akkor azt fogod mondani: "elpazaroltam Q2-t".

```
1. [Prioritás 1]
2. [Prioritás 2]
3. [Prioritás 3]
```

---

## Q4 — Hová jön be a bevétel és hol követed nyomon?

Több válasz is mehet. Számlázz.hu? Billingo? KBOSS? Banki kivonat? Excel táblázat? Stripe? Wise?

```
[A te válaszod]
```

---

## Q5 — Hol kommunikálsz ügyfelekkel, partnerekkel és a külvilággal nap mint nap?

Email (melyik — Gmail / Outlook / saját domain)? Messenger? WhatsApp? Viber? Slack? Telefon? Személyes találkozók?

```
[A te válaszod]
```

---

## Q6 — Hol élnek a találkozó-felvételek, jegyzetek és fontos dokumentumok?

Granola? Otter? Fireflies? Saját Whisper? Google Drive? Notion? Dropbox? OneDrive? Egy mappa az asztalodon, amit egyszer majd rendszereznél? Papír alapú füzet?

```
[A te válaszod]
```

---

## Q7 — Mi az az egy feladat ami elviszi a heted, és hol követed jelenleg a munkáidat?

A legnagyobb időrabló vagy ismétlődő robotmunka. Plusz hol élnek a feladatok/projektek (ClickUp / Asana / Trello / Notion / Linear / füzet / fejben).

```
[A te válaszod]
```

---

Amikor ez a fájl ki van töltve, futtasd a `/bevezetes`-t (vagy újra), és a varázsló legenerálja az 1. napi alapfájl-csomagot: `context/`, `references/voice.md`, kitöltött `kapcsolatok.md`, és kitöltött `CLAUDE.md`.
