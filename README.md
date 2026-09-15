# 🚗 Autókölcsönző / autóvásárlási / lízing- és értékesítési weboldal

A felhasználók számára lehetőség van elérhető autók bérlésére, vásárlására, lízingelésére vagy értékesítésére.

---

## 📋 Főbb funkciók

- Elérhető autók böngészése
- Szűrés típus és ár alapján
- Bérlési időszak kiválasztása
- Bérleti díj kiszámítása – hosszabb bérlés esetén kedvezőbb ár
- Foglalás / előfoglalás létrehozása
- Bérlési és tranzakciós előzmények megtekintése
- Értékelések és vélemények
- Hűségprogram és hűségkedvezmények
- Kapcsolattartási lehetőség
- Promóciós e-mailek és hírlevél-feliratkozás
- Cookie-k kezelése
- Autóvásárlás
- Autóbérlés
- Autólízing
- Autó eladása

---

## ⚙️ További funkciók

- Google Maps API és autókereső / lokátor
- Autóhitel és hitelkalkulátor
- Üzleti és alap felhasználói fiókok
- Üzleti ügyfelek számára külön kedvezmények
- AI-alapú autóajánlások???
- Világméretű autóipari és közlekedési hírek
- Járműelőélet és részletes járműinformációk
- Ügyfélszolgálat és hibajegykezelő rendszer
- Eladó és vevő közötti üzenetküldés
- Autószerviz és javítási lehetőségek
- Bizonylat / számla / nyugta generálása
- Késedelmi díj kezelése
- Bérleti díj számítása idő és megtett távolság alapján
- Kaució kezelése

---

# 👥 Feladatok

| Név | Szerep |
|---|---|
| Garai Márk | Backend |
| Csikós Balázs | Adatbázis |
| Oláh Zsombor | Frontend |

> Ezek lennének a fő szerepek, de ez még közben változhat + mindenki besegíthet a másikéba ha szükséges.

---

# 🧩 Részek

- Eladófelület
- Bérlőfelület
- Profil
- Beépített térkép
- Egyéb kisebb részek

---

# 🗄️ Adatbázis táblák

- Felhasználók (Profil tábla külön????)
- Járművek (Aadatok)
- Járműkategóriák
- Vélemények
- Bérlések
- Vásárlások
- Hirdetések????
- Tranzakciók???
- Üzenetek???

---

# 👤 Felhasználók

- `felhasznalo_id` – elsődleges kulcs
- `nev`
- `email`
- `telefonszam`
- `jelszo_hash`
- `szul_datum`
- `cím`
- `profil típus` (ügyfél, admin)

---

# 🚗 Járművek (Adatok)

- `jarmu_id` – elsődleges kulcs
- `kategoria_id` – idegen kulcs
- `marka`
- `modell`
- `alvazszam`
- `evjarat`
- `uzemanyag`
- `valto`
- `szin`
- `kilometerora_allas`
- `berleti_dij_naponta`
- `veteli_ar`
- `allapot`
- `elerheto`

---

# 🏷️ Járműkategóriák

- `kategoria_id` – elsődleges kulcs
- `nev`
- `leiras`

Például: személyautó, SUV, kisbusz, elektromos autó stb.

---

# ⭐ Vélemények

- `velemeny_id` – elsődleges kulcs
- `felhasznalo_id` – idegen kulcs
- `jarmu_id` – idegen kulcs
- `ertekeles` – pl. 1–5
- `cim`
- `szoveg`
- `letrehozas_datum`
- `mihez írta a véléményt`

---

# 📅 Bérlések

- `berles_id` – elsődleges kulcs
- `felhasznalo_id` – idegen kulcs
- `jarmu_id` – idegen kulcs
- `kezdet_datum`
- `veg_datum`
- `felvetel_helye`
- `leadás_helye`
- `napi_dij`
- `osszeg`
- `fizetesi_mod`
- `fizetesi_statusz`
- `berles_statusz`
- `//letrehozas_datum??`

---

# 💰 Vásárlások

- `vasarlas_id` – elsődleges kulcs
- `felhasznalo_id` – idegen kulcs
- `jarmu_id` – idegen kulcs
- `vasarlas_datum`
- `vetel_ar`
- `fizetesi_mod`
- `fizetesi_statusz`
- `vasarlas_statusz`
- `atadas_datum`
- `//letrehozas_datum??`

---

# 🔄 Működés

Az oldalra való fellépés után a felhasználó eldöntheti, hogy készít-e profilt, belép már meglévő profiljába vagy vendégként navigálja az oldalt.

Eldöntheti majd, hogy épp vásárolni szeretne autót (hitelre vagy önerőből) vagy épp a bérléshez van kedve.

Minden járműnél fel lesznek tüntetve a saját adataik melyek alapján lehet majd szűrni.

Ha jó, vagy épp rossz élménye volt bármilyen téren, a felhasználónak lehetősége lesz vélemény írására.

Az oldalba be lesz építve egy hitel-önerő kalkulátor is, hogy továbbá könnyítsük az ügyfelek dolgát.
