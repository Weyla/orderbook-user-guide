# Gyakori kérdések és hibaelhárítás

## Nem látok egy oldalt vagy gombot
- Valószínűleg nincs hozzá jogosultságod ([03-jogosultsagok.md](03-jogosultsagok.md)), szólj az adminnak.
- Lehet, hogy elrejtetted a menüben: nézd meg a **Rejtett oldalak** csoportot, vagy a **Fiók beállítások**at.
- Telefonon és tableten sok gomb a **⋯** vagy **⋮** menüben van, vagy a kártyára koppintva jelenik meg.

## Rendelések
- **Nem találom a rendelést a naptárban.** Webshop rendelés és még nincs ütemezve (→ **Webshop Rendelések**), törölték
  (→ admin, kuka), vagy más héten van. Keresd meg a **Keresés** oldalon a **Bármely mező**vel (pl. rendelésszám).
- **Véletlenül töröltem egy rendelést.** Azonnal szólj az adminnak, a kukából vissza tudja állítani (alapból 2 napig).
- **Nem tudom törölni a rendelést.** Aktív szállítólevél tartozik hozzá: előbb azt kell érvényteleníteni.
- **Nem tudom csökkenteni a tétel mennyiségét.** A mennyiség már szállítólevélen szerepel; előbb a szállítólevelet érvénytelenítsd.
- **Nem jó a szállítási díj.** Ellenőrizd a címet (**Szállítási cím** / **Számlázási cím** / **Egyéb**) és a várost, mert a díj
  a város szerint számolódik. Átírható kézzel is.
- **A szabad időpont kereső nem talál semmit.** 90 napon belül nincs megfelelő nap (minden nap tele, a vágási limit
  betelt, vagy az ügyfél kérése nem fér bele). Próbálj más időpont-kérést, vagy tedd be kézzel (**Elhelyezés erre a napra**).
- **Mentés sikertelen — hálózati hiba.** Nem mentődött. Ellenőrizd a kapcsolatot, és mentsd újra.

## Vágás és kiszállítás
- **A rendelés nincs a Vágás oldalon.** Nincs ütemezve, már ki van szállítva, múltbeli dátumú, túl messze van
  (**További rendelések betöltése**), vagy egy szűrő rejti el (**Kész rendelések elrejtése**, **Vágást nem igénylő rendelések elrejtése**).
- **Nincs Vágás megkezdése gomb.** A rendelésben nincs tűzifa; használd a **⋮** → **Készre jelölés**t.
- **Véletlenül készre / kiszállítottnak jelöltem.** Vágás oldal: **Vissza: Rendelés felvéve**. Kiszállítottnál: rendelés
  szerkesztése → **Állapot**. A készletmozgások visszavonódnak.
- **Nem látom a rendelést a Kiszállítás oldalon.** Másik fuvaroshoz tartozik (**Összes fuvaros**), vagy későbbi napra esik.

## Készlet
- **Rossz a készlet.** Nézd meg a **Készlet** → **Export** vagy az **Előzmények** → **Részletek** nézetben, melyik mozgás
  okozza. Gyakori ok: elmaradt **Készre jelölés**/**Kiszállítva**, duplán rögzített beszerzés, rossz helyre rögzített beszerzés.
  Javítás: a beszerzés szerkesztése, a gyártás bejegyzés módosítása, vagy szólj az adminnak (leltár).
- **Tűzifánál „—” van a Nyitott rendelések után oszlopban.** Ez szándékos: a tűzifa a vágáskor keletkezik.
- **Nem tudom törölni a beszerzést.** Csak a létrehozó törölheti, és csak a szállítás napján. Egyébként szerkesztéssel javítsd.

## Számlák
- **Nem indul a számlakészítés.** Nem mentett módosítás van a rendelésen: előbb ments.
- **Hiba a számla létrehozásakor.** Ellenőrizd a vevő nevét, számlázási címét, irányítószámát, adószámát. Ha továbbra is hibás, szólj az adminnak.
- **Rossz számlát állítottam ki.** **Sztornó**, majd készíts újat. Kiállított számlát törölni nem lehet.
- **Nincs Végszámla lehetőség.** Nincs érvényes előlegszámla.

## Szállítólevelek
- **A jegy létrehozása bizonytalan / nem enged újat.** Töltsd újra az oldalt. Ha a rendszer nem rendezi, használd a
  **Függő létrehozási kérés megszakítása** gombot, vagy szólj az adminnak.
- **Az OCR nem ismerte fel a sorszámot.** Írd be kézzel `ÉÉÉÉ-előtag-szám` formában, majd **Ellenőrzés**.
- **Az aláírt példány nem tölthető fel.** A jegy érvénytelenítve van, vagy a fájl nem PDF/JPG/PNG, vagy 20 MB-nál nagyobb.

## E-mailek
- **Az ügyfél nem kapta meg az e-mailt.** Ellenőrizd az e-mail címet a rendelésen (melyik e-mail van kiválasztva), a spam
  mappát, és hogy a rendszer nincs-e teszt módban (admin).

