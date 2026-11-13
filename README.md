# Order Book – felhasználói kézikönyv

Ez a kézikönyv az **Order Book** rendeléskezelő rendszer munkatársi használatát írja le
(tűzifa, pellet, brikett rendelések felvétele, ütemezése, vágása, kiszállítása, számlázása és a készlet kezelése).

A kézikönyv elsősorban **AI asszisztenseknek** készült: a munkatársak az asszisztenstől kérdeznek
(„hogyan rögzítek egy beszerzést?”, „miért nem látom a rendelést a vágás oldalon?”), az asszisztens pedig
ezekből a fájlokból válaszol. Emberek is olvashatják, minden oldal önállóan érthető.

- **Célközönség:** irodai munkatársak, diszpécserek, vágók, sofőrök, raktárosok, könyvelők.
  Az adminisztrátori beállítások kezelése (termékek, városok, felhasználók, integrációk) **nem** része a kézikönyvnek;
  a munkatársaknak hasznos jelenlegi értékeket a [06-beallitasok.md](06-beallitasok.md) és a [07-termekek.md](07-termekek.md) foglalja össze.
- **Nyelv:** magyar. A gombok és menüpontok nevei **félkövérrel**, pontosan úgy szerepelnek, ahogy a
  felületen megjelennek. Az admin átnevezhet feliratokat, ezért egy-egy gomb neve kissé eltérhet.
- **Mire nem jó:** nem helyettesíti az admint. Ha valami hiányzik a menüből, az jellemzően jogosultság kérdése
  (lásd [03-jogosultsagok.md](03-jogosultsagok.md)).

## Tartalom

| Fájl | Miről szól |
|------|-----------|
| [00-asszisztens-utmutato.md](00-asszisztens-utmutato.md) | Hogyan használja egy AI asszisztens ezt a kézikönyvet |
| [01-attekintes.md](01-attekintes.md) | A rendszer egésze, a rendelés életútja, állapotok, jelek |
| [02-fogalomtar.md](02-fogalomtar.md) | Fogalmak és rövidítések (m3, alapanyag, sztornó, Fő készlet…) |
| [03-jogosultsagok.md](03-jogosultsagok.md) | Ki mit lát és mit csinálhat |
| [04-menu-testreszabasa.md](04-menu-testreszabasa.md) | A menü testreszabása |
| [05-kepek.md](05-kepek.md) | Képernyőképek a felületről (képtár, AI asszisztensek ebből mutassanak képet) |
| [06-beallitasok.md](06-beallitasok.md) | A rendszer jelenlegi beállításai: munkaidő, rendelés hossza, limitek, színek, e-mail, ÁFA |
| [07-termekek.md](07-termekek.md) | Termékek, változatok, alapanyagok és átváltás, kedvezmények, városok, raktárhelyek |
| [10-naptar.md](10-naptar.md) | Naptár: rendelések, napi jegyzetek, vágási limit, „Nap tele”, szabadnapok |
| [11-rendeles-felvetele.md](11-rendeles-felvetele.md) | Új rendelés és szerkesztés: ügyfél, szállítás, tételek, ütemezés, mentés |
| [12-rendeles-megtekintese-es-torlese.md](12-rendeles-megtekintese-es-torlese.md) | Rendelés megtekintése, másolás, törlés, kuka |
| [13-ugyfelek-es-kereses.md](13-ugyfelek-es-kereses.md) | Ügyfélkeresés, ügyféloldal, összevonás, fotók, híváslista |
| [14-webshop-rendelesek.md](14-webshop-rendelesek.md) | Webshopból érkező rendelések feldolgozása |
| [15-vagas.md](15-vagas.md) | Vágás oldal: vágás megkezdése, készre jelölés |
| [16-kiszallitas.md](16-kiszallitas.md) | Kiszállítás oldal: kiszállítottnak jelölés, fotók, GPS, km óra |
| [17-szamlazas.md](17-szamlazas.md) | Számla, előlegszámla, végszámla, sztornó (Számlázz.hu) |
| [18-szallitolevelek.md](18-szallitolevelek.md) | Szállítólevél készítése, aláírt példányok feltöltése |
| [19-keszlet.md](19-keszlet.md) | Készlet oldal, jövőbeli tételek, raktárhelyek, mozgatás |
| [20-keszlet-hozzaadas.md](20-keszlet-hozzaadas.md) | Beszerzések rögzítése, gyors hozzáadás, dokumentum-sor |
| [21-eladas.md](21-eladas.md) | Közvetlen raktári eladás, számlázás, előleg rendelések |
| [22-gyartas.md](22-gyartas.md) | Gyártás és külső gyártás rögzítése |
| [23-elozmenyek-es-vezerlopult.md](23-elozmenyek-es-vezerlopult.md) | Készletmozgás-riportok és bevételi vezérlőpult |
| [24-fuvarosok.md](24-fuvarosok.md) | Külső fuvarosok naptára |
| [25-szabadsag.md](25-szabadsag.md) | Saját szabadságok és szabadságkérelmek |
| [26-jegyzetek.md](26-jegyzetek.md) | Napi jegyzetek és jegyzetsablonok |
| [27-emailek.md](27-emailek.md) | Milyen e-maileket küld a rendszer és mikor |
| [28-nyomtatas.md](28-nyomtatas.md) | Direkt nyomtatás |
| [29-gyik-es-hibaelharitas.md](29-gyik-es-hibaelharitas.md) | Gyakori kérdések és hibák |

## Karbantartás

A kézikönyvet a rendszer fejlesztése során folyamatosan frissítjük: minden felhasználót érintő változásnál
a megfelelő oldal is módosul. Ez a repó az éles rendszerrel együtt frissül.
