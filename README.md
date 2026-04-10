# ALTR-Proxy — Trading Card Sheet Generator

> A lightweight, browser-based tool to generate print-ready A4 PDF sheets for [Altered TCG](https://www.altered.gg/) proxy cards.

---

## What it does

ALTR-Proxy lets you paste a decklist, instantly preview your cards arranged on A4 sheets (9 cards per page), and export a ready-to-print PDF — all without installing anything.

Card images are fetched automatically from the official Altered database (`img.altered-db.com`) using each card's unique identifier.

---

## Features

- **Decklist input** — Accepts standard formats: `4 CARD_ID`, `4x CARD_ID`, or bare `CARD_ID` (quantity defaults to 1)
- **Live preview** — A4 sheets update in real time as you type, displayed at 80% scale
- **9 cards per sheet** — Cards are laid out in a 3×3 grid at standard TCG size (63 × 88 mm)
- **PDF export** — One-click PDF generation via jsPDF, saved as `altr-proxy-sheets.pdf`
- **Cut guides** — Optional dashed cut lines, togglable separately for the preview and the PDF
- **Summary stats** — Shows total card count and number of sheets at a glance
- **No backend** — Fully client-side, runs from a single HTML file

---

## Usage

1. Open `index.html` in any modern browser.
2. Paste your decklist in the left panel, one card per line:
   ```
   1 ALT_CORE_B_AX_02_C
   3 ALT_CORE_B_BR_15_R2
   ```
3. Watch the A4 sheets render live in the preview area.
4. Toggle cut guides on/off as needed.
5. Click **Generate PDF** to download your print sheet.

---

## Card ID format

Cards use the Altered TCG internal identifier format:

```
ALT_<SET>_<FACTION>_<CARD>_<RARITY>
```

Example: `ALT_CORE_B_AX_02_C`

---

## Tech stack

| Library | Purpose |
|---|---|
| [jsPDF 2.5.1](https://github.com/parallax/jsPDF) | PDF generation |
| [DM Sans / DM Mono](https://fonts.google.com/) | Typography |
| Vanilla JS | All logic — no framework |
| Github Pages | Display a repository as website |
| Netlify | Worker to manage CORS |

---

## Project structure

```
ALTR-Proxy/
├── index.html          # Entire application (single file)
└── assets/
    └── github-142-svgrepo-com.svg
```

---

## License

This project is unofficial and not affiliated with Altered / Equinox. Card images are property of their respective owners.
