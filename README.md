# 🏡 House Search Notebook

A private, offline, single-file web tool that guides you through searching for and buying a house. No internet connection required, no accounts, no data ever leaves your device.

---

## Quick Start

1. Download `house-search-notebook.html`
2. Open it in any modern browser (Chrome, Firefox, Safari, Edge)
3. Start filling in your details — everything saves automatically

That's it. No installation, no dependencies, no setup.

---

## Features

### 📋 Eight guided sections

| # | Section | What you do |
|---|---------|-------------|
| 1 | **Your Values** | Reflect on what matters most to you in a home and neighbourhood |
| 2 | **Countries & Cities** | Note which places you'd consider living in and why |
| 3 | **Search Filters** | Define concrete filters (bedrooms, price, type, tenure) to use on property portals |
| 4 | **Criteria & Weights** | List what you'll score each house on and assign importance weights |
| 5 | **Rate Houses** | Add houses, score each criterion 1–5 stars, add per-criterion notes |
| 6 | **Comparison** | Bar charts and score table comparing all houses by weighted score |
| 7 | **Mortgage Calculator** | Calculate monthly repayments for any price, deposit, rate, and term |
| 8 | **Purchase Checklist** | 40 tasks across 6 stages tracking your purchase from offer to move-in |

### ⚖️ Decision matrix scoring

Criteria are scored 1–5 stars and weighted by importance (1–10). The final score for each house is:

```
Score (out of 10) = Σ(stars × weight) / Σ(weights) × 2
```

This means a criterion with weight 10 influences the final score ten times more than one with weight 1.

### 💾 Auto-save

All text, tags, filters, criteria, house ratings, notes, and checklist ticks are saved automatically to your browser's `localStorage`. Your data persists between sessions without any manual saving.

### ⌨️ Keyboard shortcuts

| Key | Action |
|-----|--------|
| `→` or `]` | Go to next section |
| `←` or `[` | Go to previous section |
| `M` | Toggle the sidebar |
| `1` – `8` | Jump directly to that section |
| `?` | Return to the intro / help page |
| `Esc` | Deselect current input field |

> Shortcuts are disabled while typing in a text field or textarea.

---

## Section Details

### Search Filters (Section 3)

Comes pre-loaded with sensible defaults (click **Load default filters**):

- Min / max bedrooms
- Min / max price (£)
- Property types
- Min floor area
- Tenure (Freehold / Leasehold)
- Garden required
- Parking required
- Chain preference
- Listed within X months
- Minimum EPC rating

You can remove any filter or add your own custom ones.

### Criteria & Weights (Section 4)

Click **Load suggested criteria** to get 15 pre-defined criteria:

> Location / commute, Garden, Natural light, Room size & layout, Condition of property, Street & neighbourhood feel, Parking, Storage, Kitchen quality, Bathroom quality, Heating system, Noise level, Flood risk, School catchment, Local amenities

Each criterion has a weight slider (1–10). The weight label updates in plain English (e.g. "Essential", "Critical", "Moderate") as you drag.

### Rate Houses (Section 5)

- Add a house using the inline form at the top (no popup dialogs)
- Each house shows a ratings table with one row per criterion
- Score each criterion using the ★ star buttons
- Add specific notes for each criterion in the adjacent text box
- A weighted score badge updates live as you rate
- Add general notes about the property at the bottom

### Mortgage Calculator (Section 7)

Fields default to sensible values (£250,000 price, £25,000 deposit, 4.5% rate, 25-year term). Change any values then click **Calculate** to see:

- Monthly payment
- Loan amount and LTV ratio
- Total interest and total amount repaid
- Number of payments

Supports both **repayment** (capital + interest) and **interest-only** mortgages.

### Purchase Checklist (Section 8)

40 pre-defined tasks across six stages with a progress bar:

1. Before making an offer
2. Making an offer
3. Conveyancing & legal
4. Survey
5. Mortgage
6. Insurance & moving

---

## Data & Privacy

- **All data is stored locally** in your browser's `localStorage` under the key `hsn_v3`
- **Nothing is transmitted** — the file has zero network requests
- **Works offline** — once downloaded, no internet connection is needed
- To **back up your data**: open the browser console (`F12`) and run:
  ```js
  copy(localStorage.getItem('hsn_v3'))
  ```
  Then paste into a text file for safe-keeping.
- To **restore data**: open the console and run:
  ```js
  localStorage.setItem('hsn_v3', '<paste your backup here>')
  location.reload()
  ```
- To **clear all data** and start fresh:
  ```js
  localStorage.removeItem('hsn_v3')
  location.reload()
  ```

---

## Browser Compatibility

Works in any modern browser. 

No browser extensions or plugins required.

---

## File Structure

The entire application is a **single HTML file** with no external dependencies:

```
house-search-notebook.html    ← everything: HTML, CSS, and JavaScript
```

All styles are embedded in a `<style>` block and all logic in a `<script>` block. The file can be emailed, copied to a USB stick, or shared as an attachment and will work immediately on any device.

---

## Author Credit

This code was developed with the aid of AI tools and may contain mistakes.
This file is provided for personal use. Feel free to modify it to suit your own house search.
