# E-mailek – mit küld a rendszer és mikor

A rendszer 5 sablon alapján küld e-mailt. A sablonok szövegét az admin szerkeszti. Az e-mailben a rendelés **mentett**
adatai szerepelnek (név, időpont, ajánlott idősáv, tételek, összeg, fizetési mód stb.).

| E-mail | Kinek | Mikor |
|--------|-------|-------|
| **Rendelés beérkezett** | ügyfél | Amikor a webshopból új rendelés érkezik |
| **Rendelés visszaigazolás** | ügyfél | **Mentés és visszaigazolás** gombra; újraküldhető |
| **Emlékeztető** | ügyfél | Automatikusan, alapból a kiszállítás előtt 2 nappal, reggel 9-kor; kézzel is küldhető |
| **Értékelő e-mail** | ügyfél | Kiszállítás után a felugró ablakból, vagy a rendelésből / eladásból |
| **Fuvaros értesítés** | külső fuvaros | Amikor a rendelése először **Szállításra kész** lesz |

A számlát nem ezek az e-mailek küldik: azt a Számlázz.hu küldi, ha a számlánál **E-mail küldés: Igen** van beállítva.

## Visszaigazolás és emlékeztető részletesen

1. A rendelés mentésekor a **Mentés és visszaigazolás** gomb elküldi a visszaigazolást, és a rendelést visszaigazoltnak jelöli.
   Ha az e-mail nem megy ki, a rendelés akkor is mentődik, és a rendszer jelzi a hibát.
2. A visszaigazolt rendelésekre az emlékeztető automatikusan kimegy a beállított nappal a kiszállítás előtt (jelenleg 2 nappal előtte, 17:00 körül).
3. Ha a kiszállítás túl közel van (alapból 5 napon belül), amikor visszaigazolod, nem megy automatikus emlékeztető,
   mert az ügyfél frissen kapta a visszaigazolást.
4. Nem megy emlékeztető a nem visszaigazolt, a már kiszállított és az **Emlékeztető tiltása** jelölésű rendelésre.

A rendelés szerkesztőjében, a **Mentett rendelési adatok** részben:
- **Rendelés-visszaigazolás újraküldése** – pl. időpont-módosítás után (előbb ments!),
- **Emlékeztető küldése** – azonnal kiküldi az emlékeztetőt,
- **Emlékeztető tiltása** – erre a rendelésre ne menjen automatikus emlékeztető (más e-mailt nem tilt).

## Értékelés kérés

Ügyfelenként egyszer érdemes kérni. Az ügyfélen látszik az állapot (**Kérés elérhető** / **Kérés elküldve**).
Küldéshez **Értékelő e-mail** jog és e-mail cím kell. Kiszállításkor a rendszer magától felajánlja (lásd [16-kiszallitas.md](16-kiszallitas.md)).

## Teszt mód

Az admin a rendszert „teszt” módba teheti. Ilyenkor minden e-mail egy teszt címre megy, az ügyfél nem kapja meg.
Ha az ügyfél azt mondja, nem kapott e-mailt, nézd meg a spam mappát, ellenőrizd az e-mail címet a rendelésen, és szólj az adminnak.
