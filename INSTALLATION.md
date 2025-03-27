# Telepítési Útmutató - Webapp 1.02

Ez az útmutató végigvezet a póker chart megjelenítő webapp telepítésén és futtatásán.

## Előfeltételek

- Node.js (18.x vagy újabb)
- npm (9.x vagy újabb)
- Git

## Telepítés

### 1. Klónozd le a projektet

```bash
git clone https://github.com/Winforliving/webapp-1.02.git
cd webapp-1.02
```

### 2. Telepítsd a függőségeket

```bash
npm install
```

### 3. Indítsd el a fejlesztői szervert

```bash
npm run dev
```

Az alkalmazás most elérhető a böngészőben a http://localhost:3000 címen (vagy más porton, ha a 3000-es port foglalt).

## A projekt struktúrája

```
webapp/
├── public/            # Statikus fájlok
├── src/               # Forráskód
│   ├── app/           # Next.js app könyvtár
│   ├── components/    # React komponensek
│   │   ├── ActionBar/ # Pozíció és akció választást kezelő komponensek
│   │   ├── ChartGrid/ # A póker kezek 13x13-as megjelenítése
│   │   ├── Breadcrumb/ # Navigációs útvonal
│   │   └── Tooltip/   # Információ megjelenítés a kezekről
│   ├── store/         # Zustand állapotkezelés
│   │   └── rangeStore.ts # A fő állapotkezelő store
│   ├── types/         # TypeScript típusdefiníciók
│   └── utils/         # Segédfüggvények és eszközök
├── tailwind.config.ts # Tailwind CSS konfiguráció
└── next.config.ts     # Next.js konfiguráció
```

## HRC fájlok importálása

Az alkalmazás képes a Holdem Resources Calculator által exportált JSON fájlok importálására. Ezek a fájlok tartalmazzák a póker stratégiákat különböző helyzetekre.

1. Exportáld a stratégiát a HRC-ből JSON formátumban
2. Az alkalmazásban használd a "Import" funkciót a fájl betöltéséhez
3. Válaszd ki a megfelelő pozíciót és stack méretet

## Hibaelhárítás

Ha problémákat tapasztalsz:

1. Ellenőrizd, hogy a Node.js és npm a megfelelő verziókat használja-e
2. Ellenőrizd a böngésző konzolon megjelenő hibaüzeneteket
3. Próbáld újra telepíteni a függőségeket a `npm ci` paranccsal
4. Ha a fejlesztői szerver nem indul el, ellenőrizd, hogy nincs-e konfliktus a portokkal

## Kapcsolat

Ha további segítségre van szükséged, kérdéseket vagy észrevételeket a GitHub issues szekciójában tehetsz fel.