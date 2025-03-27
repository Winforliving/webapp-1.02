# Interaktív Póker Chart Megjelenítő Webapp (v1.02)

Ez a webapp egy dinamikus, interaktív póker stratégia megjelenítőt biztosít, amely képes Holdem Resources Calculator (HRC) exportált range-ek kezelésére és vizualizálására.

## Funkciók

- **Chart Grid**: 13x13-as interaktív póker kéz mátrix megjelenítése
- **Action Bar**: Különböző játékhelyzetek dinamikus navigálása
- **Breadcrumb**: Navigációs útvonal követése és visszalépés
- **HRC Import**: JSON fájlok importálása és feldolgozása
- **Floptimal-stílusú navigáció**: Akciók és döntési pontok közötti lépkedés
- **Node-alapú navigáció**: Komplex stratégiák közötti váltás

## Technológiák

- **Frontend**: Next.js (Turbopack)
- **UI**: React.js
- **Stílusok**: Tailwind CSS
- **Animációk**: Framer-motion
- **Állapotkezelés**: Zustand

## Indítás

Az alkalmazás elindításához futtasd a következő parancsot:

```bash
cd webapp
npm install
npm run dev
```

Az alkalmazás alapértelmezetten a [http://localhost:3000](http://localhost:3000) címen lesz elérhető.

## Verziótörténet

### v1.02
- Javítva: Helyesen kezeli a navigációt a teljes akció-sorozatokon keresztül
- Hozzáadva: Utolsó jelentős akció követése a pozíció váltásoknál
- Javítva: Az akciók után megfelelő stratégiák betöltése minden pozícióra
- Optimalizálva: Jobb teljesítmény a Chart Grid megjelenítésénél

## Használat

1. Importáld a HRC által exportált JSON fájlokat
2. Válassz egy kezdeti pozíciót az Action Bar-on
3. Navigálj a különböző akciók és döntési pontok között
4. Használd a Breadcrumb-ot a korábbi helyzetekhez való visszalépéshez

---

Kifejlesztve pókerrel foglalkozó szakemberek részére, akik a játékdöntéseik és stratégiáik vizualizációját és elemzését szeretnék hatékonyan elvégezni.