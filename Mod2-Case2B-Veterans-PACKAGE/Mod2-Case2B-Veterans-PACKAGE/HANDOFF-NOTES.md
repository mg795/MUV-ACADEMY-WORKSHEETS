# Handoff: Mod 2 Case 2B, Veterans Charity

**For:** Jim
**From:** Marshall
**What it is:** Module 2 Charity case sheet, Scenario 2B (local veterans welfare charity).

Read-only case sheet in the same layout as Mod 2 Case 2A (Homelessness) and Case 2C (Recruitment). The badge is Module 2 blue. No form fields, no browser storage.

---

## 1. Anything Marshall needs back

Nothing. Both photographs are in and the sheet is ready to publish once Marshall signs off the A4 PDF. This zip replaces the earlier placeholder version.

---

## 2. What is in this package

```
MUV - MOD 2 - CHARITY VETERANS/
    Mod.2-CaseCHARITY2B.html
    form-arrow-icon.png
    form-footer-graphic.png
    form-top-logo.png
    muv-veterans-image-1.jpg
    muv-veterans-image-2.jpg
standalone-email-version/
    Mod.2-CaseCHARITY2B-standalone.html      DO NOT UPLOAD
Mod2-Case2B-Veterans-A4.pdf
Mod2-Case2B-Veterans-SINGLE-PAGE.pdf
Mod2-Case2B-Veterans-EMAIL-A4.pdf
Mod2-Case2B-Veterans-EMAIL-SINGLE-PAGE.pdf
HANDOFF-NOTES.md
```

---

## 3. Where it goes

- Live server: a new folder under `/wp-content/downloadables/`.
- Suggested folder name: `muv-mod2-case-2b-veterans`.
- Upload every file in the worksheet folder together. The HTML calls each image by filename.
- Then push the same folder to the `MUV-ACADEMY-WORKSHEETS` repo at the top level as `MUV - MOD 2 - CHARITY VETERANS`.

---

## 4. Where each image sits, top to bottom

| Position | File |
|---|---|
| Top right logo | form-top-logo.png |
| Title and every section heading | form-arrow-icon.png |
| The Belief hero (three panel shot of a veteran mentor and a volunteer setting up a Bridge Desk in a Jobcentre) | muv-veterans-image-1.jpg |
| How a 30 Day Plan Becomes a Movement hero (three panel shot of a Bridge Evening at mixed tables) | muv-veterans-image-2.jpg |
| Footer | form-footer-graphic.png |

Both photos are 1920 x 500 and are cropped to fill, so the sides trim a little on screen and more on phones.

---

## 5. The PDFs

- `-A4.pdf` is for printing, 4 pages, about 0.5MB.
- `-SINGLE-PAGE.pdf` is one long page for screen and download links, about 0.5MB.
- The `-EMAIL-` versions are the same pages with lighter photos, about 0.3MB, for attaching to emails.
- The PDFs are snapshots. They do not update if the HTML changes. Send changes back rather than editing a PDF.

---

## 6. The email version of the HTML

`standalone-email-version/` holds one file with every graphic inside it, for attaching to emails. Do not upload it to the server.

---

## 7. Visual check once it is live

1. Blue Mod.2-CharityCase-2B badge top left, logo top right on the same centre line.
2. 11 arrow icons: one at the title and ten at the section headings. Week bars carry no arrow.
3. Both photographs present.
4. Click Save PDF. It should download the page.
5. Open it on a phone and check everything stacks to a single column.

---

## 8. Technical notes

- One HTML file plus 3 graphics and 2 photographs. No build step.
- Built directly on the Case 2A Homelessness sheet CSS, so the Module 2 case sheets match exactly.
- Save PDF uses `html2pdf.bundle.min.js` 0.10.1 from cdnjs, same as the other case sheets.
- Fonts from Google Fonts, Montserrat 400, 500, 600, 700.

---

## 9. Open items for Marshall, not Jim

- Photos are AI generated. Both are three panel shots, so on phones the page crops to the middle panel. Both centre panels read well (the pair at the desk, the older and younger veteran talking).
- Image 2: the younger man's jumper carries a small polo player logo, and a few people have lanyards with made-up lettering. Barely visible at page size, but worth a Vary (Region) if you want it clean.
- The "Movement Marketing: Extend Reach, Reduce Costs" line from the source is left off, matching the other Module 2 case sheets.
- The copy mentions "the national community history programme" and "the intergenerational bridge mechanic". Confirm both point to the Module 1 example attendees already know.
- Filename follows the siblings: `Mod.2-CaseCHARITY2B.html`.
