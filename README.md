# Argus Tracker — PWA

Ye ek installable web-app hai. Isme koi PHP/backend server ki zaroorat nahi — sara data
aapke hi phone/browser mein (localStorage) save hota hai. Backup/Restore feature app ke
andar hi maujood hai (⚙️ icon se).

## Netlify par deploy kaise karein (2 minute)

1. https://app.netlify.com par login/signup karein
2. "Add new site" → "Deploy manually" par click karein
3. Is poore folder (`pwa/` ke andar ki sabhi files — index.html, app.js, manifest.json,
   service-worker.js, icons/) ko seedha drag-drop kar dein
4. Netlify apna URL de dega (jaise `argus-tracker.netlify.app`) — agar chahen to
   Site settings → Domain management se naam badal sakte hain

## Phone par install kaise karein

1. Upar wala Netlify URL apne phone ke Chrome mein kholein
2. Chrome menu (⋮) → **"Add to Home screen"** / **"Install app"** dabayein
3. Ab home screen par "Argus" naam se app icon aa jayega — usi se kholenge to
   bilkul native app jaisa (bina address bar ke) khulega

## Data / Backup

- Sara data isi phone ke browser storage mein rehta hai
- Naya phone lene par: App ke andar ⚙️ (Settings) → Backup Download Karein →
  wo file naye phone par install ki gayi app mein Restore kar dein
- Same tarike se regular backup lete rehna acchi aadat hai

## Files

- `index.html` — app shell, CDN se React/Tailwind/Papa/XLSX load karta hai
- `app.js` — poora app logic (Machines, Parties, Sales, Payments, Log, Backup)
- `manifest.json` — PWA install settings (naam, icon, colors)
- `service-worker.js` — offline support
- `icons/` — app icon (192px, 512px, apple-touch-icon)
