LABL — Shelf Ticket Studio

Software by Medicines R Us · v1.23

LABL is a browser-based tool for producing branded shelf tickets and price labels for Medicines R Us pharmacies. It runs entirely in the browser — no install, no login, no server — and prints straight to A4 or "Save as PDF".

Live: https://medicines-r-us.github.io/ticket-studio/

What it does
Two label types
Contemporary — clean outlined label with a shelf-fold tab and the brand dot.
Legacy — bold coloured panel with the SAVE circle and big % OFF / multibuy block.
Brand system — the official Medicines R Us palette (14 colours) and fonts (Poppins, Nunito, Open Sans), with per-label colour selection.
Pricing — shows RRP, Our Price and Special together when entered, with automatic % OFF and SAVE, plus multibuy ("3 for $10") and price-per-unit.
Shelf-ready — a perforated fold-and-hook tab on every label and perforated cut guides between labels so all stores cut on the same lines.
Sizes — 2, 4, 8 or 16 labels per A4. The price auto-scales to fill each label.
Copies — print any number of each label.
Bulk tools — select all / select many, then bulk-change colour, copies, price fields, etc., or delete in one go.
Validation — a green/red dot flags whether a typed "% off" matches the maths.
Barcodes — EAN-13 / Code 128 from the product's APN.
Batches — save a batch to a file, re-load it later, or copy a share link a pharmacy can open and print (the "event" library — no account needed).
How to use
Add products — either use the Import (MIRA / Z Software) panel (paste or upload a CSV; a Download example button shows the exact format), or add labels manually.
Choose the label type, size, price size and per-label colours.
Print / Save as PDF — prints at true A4 (set the printer to 100%, no scaling).
Optionally Save batch / Copy share link to re-print or send to a store.
Import format

CSV/TSV with a header row (columns are loosely matched, any order):

brand, desc, size, copies, rrp, price, promo, pct, qty, for, colour, flash, barcode

Use the in-app Download example button for a ready-made template.

Deploying / updating

The app is a single index.html served by GitHub Pages. To update, edit or re-upload index.html in this repo and commit — Pages redeploys within ~1 minute at the same URL.

To embed on the intranet (e.g. ZohoSites), use one Custom HTML block:

html
<iframe src="https://medicines-r-us.github.io/ticket-studio/"
        style="width:100%;height:100vh;min-height:800px;border:0;"
        title="LABL"></iframe>

The intranet page never needs changing again — it always shows the latest index.html.

Notes
Fonts and the barcode library load from public CDNs (Google Fonts, cdnjs), so browsers need internet access.
The app is intentionally a "printer": product data, pricing, name-splitting and batch preparation are done upstream (in Claude, from MIRA) and imported here. Automated emailing and a direct integration are planned as a separate service.
Versioning

The version number in the app header increments with each change (currently v1.23).
