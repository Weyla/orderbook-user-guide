# A rendszer jelenlegi beállításai (munkatársaknak)

Ezeket az értékeket az admin állítja be, és bármikor módosíthatja. Az oldal a **jelenlegi** értékeket írja le,
hogy érthető legyen, miért viselkedik így a naptár, az ütemezés vagy az e-mail. Ha valami eltér ettől,
akkor valószínűleg átállították: kérdezd meg az admint.

## Naptár és munkaidő

| Beállítás | Jelenlegi érték | Mit jelent |
| --- | --- | --- |
| Naptár látható ideje | 07:30–16:00 | Ennyi látszik a naptárban (**Teljes nap** gombbal az egész nap). |
| Idősáv | 10 perc | A naptár rácsa és a húzás ennyi percre ugrik. |
| Első kiszállítás | 08:00 | Az **Első kiszállítás** gomb erre az időre teszi a rendelést; ennél korábbra a kereső nem tesz rendelést. |
| Utolsó kiszállítás | 15:00 | A szabad időpont kereső 08:00 és 15:00 között keres helyet (ha az ügyfél nem kért mást). |
| Rendelések közti szünet | 15 perc | Új rendelés elhelyezésekor ennyi szünet marad az előző rendelés vége után. |
| Ráillesztés | 60 perc | Ha egy rendelést egy másik vége közelébe húzol (60 percen belül), a rendszer annak végéhez igazítja. |
| Hétvége | piros (#c01c28) fejléc | Hétvégére alapból nem kerül rendelés (**Hétvége mutatása** gombbal látszik). |

## Rendelés hossza a naptárban

Kiszállításnál a rendelés hossza:

> **menetidő oda-vissza × fuvarok száma** + **30 perc fuvaronként** (rakodás) + **10 perc minden teljes 1500 kg után**
> (+ a rendelésnél választott **Extra idő**)

- A menetidőt a város határozza meg (a városlistában az admin tartja karban).
- **Személyes átvételnél**, vagy ha nincs város vagy fuvar, a rendelés alapból **1 óra** hosszú.
- Egy teherautó jelenleg **4000 kg**-ot visz: a webshop rendeléseknél e szerint számolja a rendszer, hány fuvar kell.

## Ajánlott idősáv az ügyfélnek („Rec:”)

A naptárkártyákon és az ütemezésnél látszó **Ajánlott** / „Rec:” idősáv az, amit az ügyfélnek mondunk:
a tervezett érkezés **±90 perc**, 5 percre kerekítve, de nem korábban, mint **08:00**. Ez kerül a visszaigazoló e-mailbe is.

## Napi limitek

| Beállítás | Jelenlegi érték | Mit jelent |
| --- | --- | --- |
| Napi vágási limit | 25 m³ | Egy napra ennyi tűzifa (szórt m³) fér. A napfejléc pl. „22/25 m³”. Napra szabott eltérés a Nap nézet **Vágási limit** gombjával. |

**Napfejléc színek:**
- narancs (#ffcc87): **Nap tele** jelölésű nap;
- piros (#ffb2b2): elérte a napi vágási limitet;
- piros (#c01c28): hétvége.

**Kiszállított rendelés** a naptárban szürke (#9a9996).

## Oldalak beállításai

| Beállítás | Jelenlegi érték | Mit jelent |
| --- | --- | --- |
| **Kiszállítás** oldal | 3 nap | Ennyi nap rendelései látszanak előre. |
| **Vágás** oldal | 20 rendelés | Ennyi rendelés töltődik be először (**További rendelések betöltése** mutat többet). |
| Készlet figyelmeztetés | narancs (#ffbe6f) / piros (#ff8888) | A rendelés **Tételek** sorában: ha a rendelés után megmaradó készlet a terméknél beállított figyelmeztetési szint alá esik, a sor narancs, ha negatív lenne, piros. |

## E-mailek

| Beállítás | Jelenlegi érték | Mit jelent |
| --- | --- | --- |
| Emlékeztető | 2 nappal a kiszállítás előtt, 17:00 körül | A visszaigazolt rendelésekre automatikusan kimegy. |
| Emlékeztető minimum | 5 nap | Ha a visszaigazolás **5 napnál közelebbi** kiszállításra megy ki, emlékeztető nem megy (a visszaigazolás elég friss). |

Részletek: [27-emailek.md](27-emailek.md).

## ÁFA és szállítás a számlán

- ÁFA kulcsok: **0%, 5%, 18%, 27%**; alapértelmezett: **27%**.
- A tűzifa és a pellet jellemzően **5%**, a napraforgó pellet és a legtöbb kiegészítő termék **27%** (lásd [07-termekek.md](07-termekek.md)).
- **A szállítás ÁFÁ-ja automatikus:** a szállítási sor a rendelésben lévő termékek ÁFÁ-ját követi
  (**Automatikus** az **ÁFA %** mezőben). Kézzel felülírható.
- A szállítási sor a számlán így jelenik meg: **„Házhozszállítás - <város>”**.
- A **0 Ft-os szállítási sor** nem kerül a számlára.

## Fizetési módok

- **Készpénz** (alapértelmezett új rendelésnél)
- **Online** (átutalás, kártya, webshopos fizetés)

## Fuvarosok

- **Saját autó**: a cég saját járműve, a sofőr a **Kiszállítás** oldalon dolgozik.
- **Külső fuvarosok**: ők a **Fuvaros naptár** oldalon látják a nekik kiosztott rendeléseket ([24-fuvarosok.md](24-fuvarosok.md)).

## Jogosultság-sablonok

Az admin ezekből a sablonokból indul ki, amikor új munkatársat vesz fel: **Vágó**, **Rendelés felvevő**, **Sofőr**, **Fuvaros**.
Hogy ki mit lát, lásd [03-jogosultsagok.md](03-jogosultsagok.md).
