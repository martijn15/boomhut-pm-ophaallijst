# 🌳 PM Ophaallijst Web App - De Boomhut

Web-based ophaallijst applicatie voor pedagogisch medewerkers. Werkt op iPhone, Android en desktop!

## ✨ Features

- ✅ **Werkt op alle devices** - iPhone, Android, desktop
- ✅ **Realtime updates** - Ziet direct wijzigingen
- ✅ **Offline capable** - Kan toegevoegd worden aan home screen
- ✅ **Piratenskip support** - Automatische detectie voor dinsdag Stint 1
- ✅ **Eenvoudige interface** - Duidelijk en gebruiksvriendelijk
- ✅ **Geen app store nodig** - Direct via browser

## 🚀 Installatie op GitHub Pages

### Stap 1: Maak GitHub Repository

1. Ga naar [GitHub](https://github.com)
2. Klik op **"New repository"**
3. Repository naam: `boomhut-pm-ophaallijst` (of eigen naam)
4. Zet op **Public**
5. Klik **"Create repository"**

### Stap 2: Upload Bestanden

1. Klik op **"uploading an existing file"**
2. Sleep `index.html` naar de browser
3. Klik **"Commit changes"**

### Stap 3: Firebase Configuratie

**BELANGRIJK:** Je moet de Firebase configuratie toevoegen!

1. Open `index.html` in een text editor
2. Zoek deze regel (rond regel 260):
   ```javascript
   const firebaseConfig = {
       apiKey: "YOUR_API_KEY",
       authDomain: "YOUR_PROJECT.firebaseapp.com",
       ...
   };
   ```

3. Vervang met jouw Firebase config:
   - Open Firebase Console
   - Ga naar Project Settings
   - Scroll naar "Your apps"
   - Kopieer de config
   
4. Plak jouw config in `index.html`

5. Upload de aangepaste `index.html` naar GitHub (commit changes)

### Stap 4: Activeer GitHub Pages

1. Ga naar repository **Settings**
2. Klik op **Pages** (linker menu)
3. Bij **Source**: selecteer **main** branch
4. Klik **Save**
5. Wacht 1-2 minuten
6. Jouw site is nu live op: `https://USERNAME.github.io/boomhut-pm-ophaallijst`

## 📱 Installatie op iPhone (als app)

### Voor iPhone gebruikers:

1. Open de link in **Safari** (niet Chrome!)
2. Klik op het **"Share"** icoon (vierkant met pijl omhoog)
3. Scroll naar beneden en klik **"Add to Home Screen"**
4. Klik **"Add"**
5. **De app staat nu op je home screen!** 🎉

De webapp opent nu in volledig scherm, zonder Safari UI!

## 📱 Installatie op Android

1. Open de link in **Chrome**
2. Klik op de **drie puntjes** (menu)
3. Klik **"Add to Home screen"**
4. Klik **"Add"**

## 🔧 Firebase Configuratie Details

### Waar vind je de Firebase config?

1. Open [Firebase Console](https://console.firebase.google.com)
2. Selecteer je project (De Boomhut)
3. Klik op het **tandwiel** icoon → **Project settings**
4. Scroll naar **"Your apps"**
5. Klik op **Web app** (</> icoon)
6. Kopieer de **firebaseConfig** object

Het ziet er zo uit:
```javascript
const firebaseConfig = {
  apiKey: "AIzaSyC...",
  authDomain: "de-boomhut-123.firebaseapp.com",
  databaseURL: "https://de-boomhut-123.firebaseio.com",
  projectId: "de-boomhut-123",
  storageBucket: "de-boomhut-123.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abc123"
};
```

### Firebase Database Rules

Zorg dat je Firebase Realtime Database regels correct staan:

```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```

**LET OP:** Dit is voor development. Voor productie gebruik betere security rules!

## 🎨 Gebruik

### Als PM:

1. Open de webapp (via link of home screen app)
2. Selecteer je naam uit de lijst
3. Selecteer de datum (standaard: vandaag)
4. Klik **"Ophaallijst Laden"**
5. Zie je ophaallijst met alle kinderen
6. **Tik op een kind** om af te vinken
7. Realtime sync met andere PMs en admin app!

### Piratenskip Kinderen:

- Worden **automatisch geladen** voor Stint 1 op dinsdag
- Herkenbaar aan **🏴‍☠️ emoji**
- Oranje border
- "Afgeleverd" in plaats van "Opgehaald"

## 🔄 Updates Maken

Als je de webapp wilt updaten:

1. Wijzig `index.html` lokaal
2. Ga naar GitHub repository
3. Klik op `index.html`
4. Klik op **pencil icoon** (Edit)
5. Plak nieuwe code
6. Klik **"Commit changes"**
7. Wacht 1 minuut → updates zijn live!

## 🐛 Troubleshooting

### "Geen ophaallijst gevonden"
- Check of de datum correct is
- Check of er planning is gemaakt in admin app voor deze datum

### "Geen vervoer toegewezen"
- Deze PM heeft geen rit op deze dag
- Check planning in admin app

### Kinderen niet zichtbaar
- Check Firebase console: `kinderen_per_dag/{datum}/`
- Check of kindIds in vervoer_verdeling staan

### Realtime updates werken niet
- Check internet verbinding
- Check Firebase Database rules (moet .read: true zijn)

### Firebase errors
- Check of firebaseConfig correct is ingevuld
- Check Firebase console voor errors

## 📊 Technologie

- **Frontend:** Vanilla JavaScript (geen frameworks!)
- **Database:** Firebase Realtime Database
- **Hosting:** GitHub Pages
- **PWA:** Installeerbaar op home screen

## 🔐 Security

**LET OP:** Deze versie heeft open database regels voor eenvoud!

Voor productie gebruik:
- Firebase Authentication
- Strikte database rules
- API keys beveiliging

## 📝 Credits

Gemaakt voor **Makerspace de Boomhut** 🌳

## ❓ Vragen?

Open een issue op GitHub of neem contact op!
