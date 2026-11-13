# A rendszer áttekintése

Az Order Book egy webes rendeléskezelő. Böngészőből használható számítógépen, tableten és telefonon.
Minden munkatárs csak azokat az oldalakat látja, amelyekhez jogosultsága van.

## Fő oldalak (bal oldali menü)

| Menüpont | Mire való |
|----------|-----------|
| **Vezérlőpult** | Bevételi és rendelési statisztikák |
| **Naptár** | Az összes rendelés időpont szerint; innen veszünk fel új rendelést |
| **Fuvaros naptár** | Külső fuvarosoknak: a hozzájuk rendelt következő rendelések |
| **Keresés** | Ügyfelek keresése, új ügyfél felvétele |
| **Kiszállítás** | A következő napok kiszállításai, kiszállítottnak jelölés |
| **Vágás** | A vágócsapat munkalistája: vágás megkezdése, készre jelölés |
| **Webshop Rendelések** | A webshopból érkezett, még feldolgozandó rendelések |
| **Eladás** | Közvetlen raktári eladás (rendelés nélkül) |
| **Aláírt jegyek** | Aláírt szállítólevél-példányok tömeges feltöltése |
| **Készlet hozzáadás** | Beszerzések (bejövő áru) rögzítése |
| **Készlet** | Aktuális készlet és jövőbeli igények |
| **Előzmények** | Ki- és bejövő készletmozgások riportja |
| **Gyártás** / **Külső gyártás** | Napi gyártás rögzítése |
| **Mozgatás** | Készlet mozgatása raktárhelyek között |
| **Híváslista** | Beérkező hívások listája |
| **Jegyzetek** | Napi jegyzetek és sablonok |
| **Szabadságkérelmek** | Szabadságkérelmek elbírálása |
| **Saját szabadságok** | Saját szabadságkeret és kérelmek |

Telefonon alul egy rövid menüsor látszik (alapból **Naptár**, **Új**, **Kiszállítás**), a többi oldal a **Menü** alatt van.
A menü sorrendje és tartalma a **Fiók beállítások** oldalon testreszabható
(lásd [04-menu-testreszabasa.md](04-menu-testreszabasa.md)).

## Egy rendelés életútja

```
Felvétel ──► (Vágás alatt) ──► Szállításra kész ──► Kiszállítva
 Naptár /      Vágás oldal       Vágás oldal          Kiszállítás oldal
 Webshop
```

1. **Rendelés felvéve** – a rendelést felvették (telefonon a naptárból vagy a webshopból érkezett).
   Ilyenkor még semmi nem mozdul a készletben.
2. **Vágás alatt** – a vágócsapat elkezdte a rendelés tűzifáját vágni (**Vágás megkezdése**). Készletet nem mozgat.
3. **Szállításra kész** – a vágás kész (**Készre jelölés**). Ekkor a rendszer:
   - a kész tűzifát **hozzáadja** a termékkészlethez,
   - a felhasznált **alapanyagot levonja** (pl. a rönk mennyiségét),
   - ha a rendelés külső fuvaroshoz tartozik, e-mailt küldhet a fuvarosnak.
4. **Kiszállítva** – a sofőr kiszállította (**Kiszállítva** gomb a Kiszállítás oldalon). Ekkor a rendszer
   **levonja** a kiszállított termékeket a készletből. Ha be van kapcsolva, a webshopban is lezárja a rendelést,
   és felajánlhatja az értékelő e-mail küldését.

Fontos részletek:

- Egy lépés kihagyható. Ha egy rendelést rögtön kiszállítottnak jelölnek, a rendszer a „kész” és a „kiszállított”
  készletmozgást is elvégzi, így a készlet akkor is helyes.
- Visszafelé is lehet lépni (pl. **Vissza: Rendelés felvéve**). Ilyenkor a rendszer a megfelelő készletmozgásokat
  **visszavonja**, így semmi nem duplázódik.
- A tűzifát nem igénylő rendelések (pl. csak pellet vagy brikett) a vágás lépést kihagyhatják.
- A rendelés állapota a rendelés szerkesztésekor kézzel is átállítható (**Állapot** mező); a készlethatás ugyanaz.
- A **Vágásra vár** egy régi állapot, csak régi rendeléseknél jelenhet meg.

## Jelek a naptárban és a kártyákon

| Jel | Jelentés |
|-----|----------|
| 🕓 | Vágásra vár (régi állapot) |
| 🪓 | Vágás alatt |
| ✅ | Szállításra kész |
| 📦 | Kiszállítva |
| ‼️ | Problémás ügyfél |
| 💵 | Fizetve |
| 💸 | Részben fizetve (Kiszállítás oldal) |
| ● zöld | Számla kiállítva |
| ● kék | Előlegszámla kiállítva |
| ● narancs | Végszámla kiállítva |
| 🏖 | Szabadnap (valaki szabadságon van) |
| 📋 | Napi jegyzet |
| 📍 | Az ügyfélnek mentett GPS koordinátája van (Kiszállítás oldal) |

A naptárban a **?** gomb (telefonon a **⋯** menüben) megnyitja a **Naptár jelmagyarázat** ablakot.

## Szállítás vagy személyes átvétel

- **Szállítás** – mi visszük ki a saját autónkkal (az alapértelmezett fuvaros). Van szállítási díj,
  ajánlott érkezési idősáv és a naptárban az autó idejét foglalja.
- **Személyes átvétel** – az ügyfél jön érte, vagy külső fuvaros viszi. Nincs szállítási díj, nincs ajánlott idősáv,
  és nem foglalja a saját autónk idejét a naptárban.
- Ha egy rendeléshez **nem alapértelmezett (külső) fuvarost** választanak, a rendszer automatikusan
  **Személyes átvétel**-re vált, mert a külső fuvaros az ügyfél saját szervezésű szállítása.

## Készlet röviden

- A készlet egy „főkönyv”: minden mozgás (beszerzés, gyártás, vágás, kiszállítás, eladás, leltár) egy sor.
- A **Fő készlet** az alapértelmezett raktár. Lehetnek **külső helyek** is (pl. egy külső telephely).
- A rendelések mindig a Fő készletből fogyasztanak.
- Részletek: [19-keszlet.md](19-keszlet.md).

## Törlés

A törölt rendelés a **kukába** kerül, nem tűnik el azonnal. Az admin visszaállíthatja. Alapból 2 nap után
véglegesen törlődik. Részletek: [12-rendeles-megtekintese-es-torlese.md](12-rendeles-megtekintese-es-torlese.md).
