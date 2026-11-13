# Jogosultságok – ki mit lát

Minden felhasználó egyedi jogosultságokat kap, általában egy előre beállított csomagból
(pl. „Iroda”, „Vágó”, „Sofőr”). **Jogosultságot csak az admin adhat vagy vehet el.**
Ha egy oldal nem látszik a menüben, vagy egy gomb hiányzik, valószínűleg nincs hozzá jogosultságod.

> Tipp: a menü testreszabásánál elrejtett oldalak a **Rejtett oldalak** csoportban vannak, ezek nem jogosultsági kérdések.
> Lásd [04-menu-testreszabasa.md](04-menu-testreszabasa.md).

## Oldal-jogosultságok

| Jogosultság | Mit enged |
|-------------|-----------|
| **Vezérlőpult** | Vezérlőpult megnyitása |
| **Naptár** | Teljes naptár ügyfélnevekkel, napi jegyzetek, vágási limit, „Nap tele”, szabadnap felvétele |
| **Rendelések** | Rendelés felvétele, szerkesztése, törlése, számlázás, szállítólevél, ügyféladatok szerkesztése |
| **Rendelések — csak megtekintés** | Rendelések megnyitása olvasásra, számlák és PDF-ek megtekintése |
| **Keresés** | Keresés oldal és ügyféloldal (a kereséshez a **Rendelések** jog is kell) |
| **Kiszállítás** | Kiszállítás oldal, kiszállítottnak jelölés, GPS mentése, km óra rögzítése |
| **Kiszállítási fotó — feltöltés / törlés** | Fotó feltöltése a kiszállításról, illetve törlése |
| **Vevőfotók (megtekintés)**, **Vevőfotó — feltöltés / törlés** | Ügyfélfotók (pl. a lerakodás helye) |
| **Hasítandó** | Vágás oldal: vágás megkezdése, készre jelölés |
| **Webshop rendelések** | Webshop Rendelések oldal |
| **Értékelő e-mail** | Értékelés kérő e-mail küldése és jelölése |
| **Készlet** | Készlet oldal és exportja |
| **Készlet hozzáadás** | Beszerzések rögzítése és a dokumentum-sor |
| **Készlet hozzáadás — szerkesztés** | Meglévő beszerzések javítása (bármikor), gyors hozzáadások kiegészítése |
| **Készlet hozzáadás - Gyors hozzáadás** | Gyors hozzáadás fül |
| **Készlet eladás** | Eladás oldal: új eladás |
| **Készlet eladás — előzmények** | Eladások előzményei és exportja |
| **Készlet eladás - előleg rendelések** | Előlegszámlás eladások, befejezés, végszámla |
| **Készlet eladás - bármely eladás érvénytelenítése** | Bármelyik eladás érvénytelenítése bármikor (enélkül csak a saját eladás, 15 percen belül) |
| **Gyártás**, **Gyártás — előzmények**, **Gyártás — előzmények törlése** | Napi gyártás, előzmények megtekintése, régi bejegyzések törlése |
| **Külső gyártás** és alpontjai (mozgatás, előzmények, előzmények törlése) | Gyártás külső helyen és készletmozgatás helyek között |
| **Előzmények** | Készletmozgás-riport |
| **Híváselőzmények** | Híváslista |
| **Jegyzetek (admin)** | Napi jegyzetek mentése és sablonok használata |
| **Szabadságkérelmek** | Mások szabadságkérelmeinek elbírálása |
| **Fuvaros naptár** | Külső fuvarosoknak a saját rendeléseik |
| **Aláírt szállítójegyek feltöltése** | Aláírt jegyek tömeges feltöltése |

## Gyakori helyzetek

- **Látom a naptárt, de nem tudok napi jegyzetet menteni.** A mentéshez a **Jegyzetek (admin)** jog kell.
- **A Keresés oldal megnyílik, de nem talál semmit / hibát ad.** A kereséshez a **Rendelések** jog is kell.
- **Nem tudok rendelést törölni.** Törölni csak **Rendelések** joggal lehet, és csak akkor, ha nincs a rendeléshez
  aktív szállítólevél (lásd [18-szallitolevelek.md](18-szallitolevelek.md)).
- **Csak olvasni tudom a rendelést.** Csak **Rendelések — csak megtekintés** jogod van.
- **A Saját szabadságok oldal nem nyílik.** A felhasználódnak egy dolgozóhoz kell kapcsolódnia; ezt az admin állítja be.

## Admin funkciók (nem munkatársi feladat)

Termékek, alapanyagok, városok és szállítási díjak, kedvezmények, fizetési módok, fuvarosok, járművek, beszállítók,
felhasználók, e-mail sablonok, nyomtató, integrációk, leltár, kuka. Ezekhez az admin kell.
