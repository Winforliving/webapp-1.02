# Változásnapló

Az összes jelentős változtatás ebben a fájlban van dokumentálva.

## [1.02] - 2025-03-27

### Javítva
- Kijavítva a pozíció kattintás utáni helytelen stratégia betöltés
- A rendszer most már a legutolsó jelentős akció alapján tölti be a stratégiát az első jelentős akció helyett
- Javítva a node betöltési logika a pozíció váltásoknál

### Hozzáadva
- Új `lastSignificantAction` állapot a Store-ban, amely követi és tárolja a legutolsó Raise vagy Call akciót
- Jobb hibaüzenetek és logolás a konzolban a hibakereséshez
- Optimalizált debuggolási információk a fejlesztői konzolban

### Változtatva
- A `jumpToPosition` függvény most az utolsó jelentős akciót használja a stratégiák betöltéséhez
- A `selectAction` függvény most már mindig frissíti az `lastSignificantAction` mezőt új jelentős akció esetén
- A `resetFirstSignificantAction` függvény most az `lastSignificantAction` mezőt is visszaállítja

### Technikai részletek
- Amikor EP pozíció 2bb Raise-t hajt végre és MP Call-t tesz, majd HJ pozícióra kattintunk, a rendszer most már helyesen a "LJ C 1600" akció ellen tölti be a stratégiát, nem pedig az "EP R 1600" akció ellen
- Az akciók követése konzisztensebbé vált, ami lehetővé teszi a komplex döntési fák pontosabb követését

## [1.01] - 2025-03-26

### Hozzáadva
- Alapvető Chart Grid megjelenítés
- Action Bar komponens a pozíciók közötti navigációhoz
- Breadcrumb komponens a megtett lépések követéséhez
- HRC JSON fájl importálási képesség
- Node-alapú navigáció implementálása

### Implementált
- Zustand store a komplex állapotkezeléshez
- Tailwind CSS a stílusokhoz
- Framer-motion animációk
- Teljes típusdefiníciók TypeScript-ben

## [1.00] - 2025-03-24

### Hozzáadva
- Projekt inicializálása Next.js keretrendszerrel
- Alapvető projektstruktúra létrehozása
- Függőségek és fejlesztői eszközök telepítése