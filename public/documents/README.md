# Project Documents

Place PDF / document files here. They are served as static assets.

```
public/documents/
├── quran/    # Quran PDFs, para/juz files, tafsir
├── qaida/    # Noorani Qaida, lesson sheets
└── books/    # Islamic books, hadith collections
```

## Adding a file

1. Drop the file into the matching subfolder, e.g.
   `public/documents/books/riyad-us-saliheen.pdf`
2. Register it in `public/documents/manifest.json` so the app can list it.
3. Commit & push — Vercel serves it automatically.

## URLs

Both paths resolve to the same file (rewrite configured in `vercel.json`):

| URL | Notes |
|---|---|
| `/documents/books/riyad-us-saliheen.pdf` | **preferred** — clean path |
| `/public/documents/books/riyad-us-saliheen.pdf` | direct path |

## Supported types
`.pdf` `.docx` `.doc` `.epub` `.txt` `.md`

File naming: lowercase, hyphen-separated, no spaces (e.g. `surah-yaseen.pdf`).
