# 🏰 Jørgens byggeplass

En liten stjernetavle-app for barn: tørr hele dagen = 1 stjerne. Når Jørgen har samlet 10 stjerner, har han bygget hele riddertårnet og vunnet premien (en leke-gravemaskin). En gravemaskin «graver» og bygger tårnet høyere for hver stjerne.

Appen er én frittstående HTML-fil uten avhengigheter. Den lagrer fremgangen lokalt i nettleseren, fungerer offline, og kan legges til på hjemskjermen som en vanlig app.

---

## 🚀 Ta den i bruk (GitHub Pages)

### Alternativ A – uten terminal (dra og slipp)
1. Lag et nytt, tomt repo på GitHub (f.eks. `byggeplass`). Hold det **Public**.
2. På repo-siden: **Add file → Upload files**, og dra inn alle filene i denne mappen (`index.html`, `manifest.webmanifest`, de tre `icon-*.png`, og `.nojekyll`).
3. **Commit changes**.

### Alternativ B – med Git i terminal
```bash
cd byggeplass-repo
git init
git add .
git commit -m "Jørgens byggeplass"
git branch -M main
git remote add origin https://github.com/<brukernavn>/byggeplass.git
git push -u origin main
```

### Skru på Pages
1. Gå til **Settings → Pages**.
2. Under **Build and deployment → Source**: velg **Deploy from a branch**.
3. Branch: **main**, mappe: **/ (root)**. Trykk **Save**.
4. Vent ~1 minutt. Lenken vises øverst på Pages-siden, typisk:
   `https://<brukernavn>.github.io/byggeplass/`

---

## 📱 Legg til på hjemskjerm

**iPhone (Safari):** Åpne lenken → trykk Del-knappen → **Legg til på Hjem-skjerm**.

**Android (Chrome):** Åpne lenken → meny (⋮) → **Installer app** / **Legg til på startskjerm**.

> 💡 Åpne lenken **én gang mens du har nett** før du legger den til, så ikonet og skrifttypen lastes inn. Etterpå fungerer den også uten nett.

---

## 🔄 Oppdatere appen senere
Bytt ut `index.html` (eller andre filer) og commit/push på nytt. Pages oppdateres automatisk. Det kan ta et øyeblikk før telefonen henter den nye versjonen.

---

## 💾 Lagring og personvern
- All fremgang lagres lokalt på telefonen via nettleserens `localStorage` — ingenting sendes til noen server.
- Dataene ligger på **den telefonen appen brukes på**. Brukes appen på to telefoner, får hver sin egen telling.
- «For mamma og pappa»-panelet har **Angre siste** og **Nullstill runde**.

---

## 🛠️ Tilpasning
Alt ligger i `index.html`:
- **Antall stjerner til premie:** endre `var GOAL = 10;` i `<script>`.
- **Tekst (navn, premie, overskrifter):** søk i HTML-en, f.eks. «Jørgens byggeplass» eller «vunnet en gravemaskin».
- **Farger:** justeres i `<style>` (bygul `#F5B921`, stein `#C3BBA9`, flagg `#E2483B`).
- **Lyd:** av/på-knappen øverst til høyre; innstillingen huskes.

---

## 📂 Filer
| Fil | Hva det er |
| --- | --- |
| `index.html` | Hele appen (HTML + CSS + JS) |
| `manifest.webmanifest` | Gjør appen installerbar (navn, ikoner, fullskjerm) |
| `icon-512.png` / `icon-192.png` | App-ikoner (Android / manifest) |
| `icon-180.png` | App-ikon for iPhone (apple-touch-icon) |
| `.nojekyll` | Hindrer at GitHub Pages omformer filene |
