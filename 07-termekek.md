# Termékek, alapanyagok és kedvezmények

A termékeket az admin állítja be. Ez az oldal azt írja le, **hogyan vannak felépítve** a termékek,
hogy érthető legyen a rendelés, a vágás és a készlet működése. Árak itt nincsenek: az aktuális árat a
rendelés felvételekor a rendszer automatikusan beírja a tételhez (átírható).

## Felépítés

- **Kategória** → **termék** → **változat**. Pl. *Tűzifa* → *Akác* → *40 cm*.
- A tételhez a rendszer a változat **árát**, **ÁFÁ-ját**, **egységét** és **súlyát** veszi.
- **Lépésköz:** egyes termékek csak a lépésköz többszörösében rendelhetők (pl. pellet 15 kg-os zsákonként).
- **Számlanév:** a számlán a termék hosszabb, hivatalos neve jelenik meg, pl. „Akác tűzifa (ömlesztett m³) - 40 cm”.
- **Tűzifa jelölés:** a tűzifa termékek számítanak bele a **napi vágási limitbe**, ezek jelennek meg vágandóként
  a **Vágás** oldalon, és ezekből lesz szórt m³ a napfejlécben.
- **Gyártható:** a gyártható termékek a **Gyártás** oldalon rögzíthetők (alapanyagból készülnek).
- **Rejtett** termék: nem választható új rendelésnél, de a régi rendelésekben megmarad.
- **Figyelmeztetési szint:** ha a rendelés után megmaradó készlet ez alá esik, a tétel sora narancs lesz
  ([06-beallitasok.md](06-beallitasok.md)).

## Termékek kategóriánként

### Tűzifa
| Termék | Egység | Változatok | Megjegyzés |
| --- | --- | --- | --- |
| **Cser**, **Bükk**, **Kőris**, **Gyertyán**, **Akác** | szórt űrméter (szórt m³) | **40 cm**, **35 cm**, **30 cm**, **25 cm** | Tűzifa, gyártható (vágáskor keletkezik), ÁFA 5%. Fafaj-kódok: CS, B, MK, GY, A. |
| **Hálózott raklapos tűzifa** | # (raklap) | **Bükk**, **Cser**, **Kőris**, **Akác**, **Gyertyán**, **Gyüjtő** | Gyártható, 1 raklap kb. 1300 kg. |
| **Faaprítási hulladék (raklap)** | # (raklap) | – | |

A naptár és a vágás rövidítése pl. „8m3 Kőris 30”: 8 szórt m³ kőris, 30 cm-es hasábokkal.

### Pellet (kg)
| Termék | Lépésköz | ÁFA |
| --- | --- | --- |
| **HS pellet** | 15 kg | 5% |
| **Vostok pellet** | 15 kg | 5% |
| **Napraforgó pellet** | 25 kg | 27% |

### Brikett (kg, 10 kg-os lépésköz)
- **Móra brikett**
- a cég saját márkás brikettje (gyártható)
- **Woody brikett** (rejtett, már nem választható)

### Gyújtós
- **PEPO ÖKO faforgács alágyújtós**
- **PEPO szilárd alágyújtós**
- **Puhafa gyújtós** (zsák, gyártható)
- PEPO dobozos (rejtett)

### Egyéb
- **Keményfa füstölő fűrészpor** (zsák, gyártható)
- **Bográcsozó fa** (zsák, gyártható, ÁFA 5%)
- több **PEPO** kiegészítő termék (db, ÁFA 27%)

## Alapanyagok és átváltás

Az alapanyag az, amiből a termék készül. Készre jelöléskor, illetve gyártás rögzítésekor a rendszer
**levonja az alapanyagot** és **hozzáadja a terméket** a készlethez. A levonás: **mennyiség × átváltási arány**.

Alapanyagok:
- **Cser**, **Bükk**, **Kőris**, **Gyertyán**, **Akác**, **Hárs** (tömör m³);
- **Hálózott bográcsozó**, **Hálózott hárs** (raklap).

| Termék | Mit von le |
| --- | --- |
| 1 szórt m³ tűzifa (bármely fafaj) | 0,5 tömör m³ ugyanabból a fafajból |
| 1 raklap hálózott raklapos tűzifa | 0,85 tömör m³ a változat fafajából |
| 1 zsák bográcsozó fa | 0,025 tömör m³ bükk, **vagy** 0,03 raklap hálózott bográcsozó |
| 1 zsák puhafa gyújtós | 0,025 tömör m³ hárs, **vagy** 0,03 raklap hálózott hárs |
| 1 raklap hálózott bográcsozó (alapanyag) | 0,85 tömör m³ bükk |
| 1 raklap hálózott hárs (alapanyag) | 0,85 tömör m³ hárs |

Ezért a tűzifánál a **Készlet** oldalon a **Nyitott rendelések után** oszlopban „—” áll: a tűzifa a vágáskor
keletkezik az alapanyagból, így az alapanyag készlete a fontos.

## Kedvezmények

A kedvezményeket a rendszer **automatikusan** számolja a rendelésnél. Összegeket itt nem írunk, a pontos
értéket a rendelés mutatja.

- **Szállítási kedvezmény 8-16 / 16-24 / 24-32:** ha a rendelésben a tűzifa összesen
  - 8–15,9 m³, **1 fuvar** szállítási díjából,
  - 16–23,9 m³, **2 fuvar** szállítási díjából,
  - 24–31,9 m³, **3 fuvar** szállítási díjából

  kap kedvezményt, egy felső határig. A kedvezmény soha nem több, mint a szállítási díj, és a szállítási sorokra oszlik el.
- **Raklapos pellet ár:** a **HS pellet** és a **Vostok pellet** egységára **1050 kg-tól** kedvezményes (raklapos ár).

## Városok és szállítási díj

- A rendszerben kb. 140 település van. Mindegyikhez tartozik **szállítási díj** (fuvaronként) és **menetidő**.
- A szállítási díj a kiválasztott cím városából jön, a menetidő a rendelés hosszát adja ([06-beallitasok.md](06-beallitasok.md)).
- Ha egy település hiányzik, vagy rossz a díja, szólj az adminnak.

## Raktárhelyek

- **Fő készlet**: a telephely készlete. Az alapértelmezett hely.
- Egy **külső raktárhely** is van (külső telephely). Ide **Mozgatás**sal kerül át az áru, és a **Külső gyártás** oldalon
  rögzíthető az ottani gyártás ([19-keszlet.md](19-keszlet.md), [22-gyartas.md](22-gyartas.md)).
