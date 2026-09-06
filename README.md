# Ausia Islamic Education App

Modern, soft-3D **glassmorphic** Islamic education web app — fully responsive (mobile → 4K).

🔗 **Live:** https://ausia-islamic-education.vercel.app

## Features
- 🕌 Auto-updating **Hijri + Gregorian** date
- 🕐 Daily Prayer Schedule (Fajr → Isha) with active-prayer highlight
- 🧭 Qibla Direction with animated compass
- 📖 Reading Section — Quran, Qaida, Dua, Prayers, Allah Names, Prophet Names, Hadiths, Pillars of Islam
- 🏆 Events poster with CTA
- 🛠️ Tools — Zikr Counter, Zakat Calculator, Qibla Direction
- 📚 Islamic Books slider
- 📱 Glass bottom navigation (mobile)

## Design
Glassmorphism · gradient background with floating blobs · frosted rounded cards · colorful soft-3D icon tiles.

### Color Palette
| Color | Hex |
|---|---|
| Soft Periwinkle Blue | `#AFC8F5` |
| Lavender | `#AFA7E8` |
| Soft Purple | `#8F82D9` |
| Light Blue/Lavender BG | `#E9F0FA` |
| Soft White | `#F8FAFC` |
| Primary Blue | `#5275D9` |

## Responsive Breakpoints
`≤360px` · `480px+` · `768px+` (tablet) · `980px+` (laptop) · `1400px+` · `1800px+` (4K) · landscape phones · `prefers-reduced-motion`

## Documents

PDFs and documents live in `public/documents/`:

```
public/documents/
├── manifest.json   # registry the app reads
├── quran/          # Quran PDFs
├── qaida/          # Noorani Qaida, lessons
└── books/          # Islamic books, hadith
```

Served at `/documents/<category>/<file>.pdf`. `public/` is the Vercel output directory, so `index.html` lives there too.

**To add a document:** drop the file in the right subfolder → add an entry to
`manifest.json` → push. Reading tiles and the Books slider pick it up automatically.

Helpers available in the app: `docUrl(file)`, `loadDocs()`, `getDocs(cat)`,
`docExists(file)`, `openDoc(file)`.

## Tech
Single-file static app — pure HTML + CSS + vanilla JS. No build step.

## Deploy
Auto-deployed to Vercel on push to `main`.
