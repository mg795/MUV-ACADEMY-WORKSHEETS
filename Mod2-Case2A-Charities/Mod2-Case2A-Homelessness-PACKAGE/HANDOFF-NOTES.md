# Handoff: Mod 2 Case 2A, Homelessness and Rough Sleeping Charity

**For:** Jim
**From:** Marshall
**What it is:** Module 2 Charity case sheet, Scenario 2A (local homelessness and rough sleeping charity).

Read-only case sheet in the same layout as Mod 2 Case 2C (Recruitment) and the Module 1 case sheets (Conservation 1A, Hospice 1B, Construction 1C, Hotel 1D). The badge is Module 2 blue. No form fields, no browser storage.

---

## 1. Anything Marshall needs back

Nothing. Both photographs are in and the sheet is ready to publish once Marshall signs off the A4 PDF. This zip replaces the earlier placeholder version.

---

## 2. What is in this package

```
MUV - MOD 2 - CHARITY HOMELESSNESS/
    Mod.2-CaseCHARITY2A.html
    form-arrow-icon.png
    form-footer-graphic.png
    form-top-logo.png
    muv-homelessness-image-1.jpg
    muv-homelessness-image-2.jpg
standalone-email-version/
    Mod.2-CaseCHARITY2A-standalone.html      DO NOT UPLOAD
Mod2-Case2A-Homelessness-A4.pdf
Mod2-Case2A-Homelessness-SINGLE-PAGE.pdf
Mod2-Case2A-Homelessness-EMAIL-A4.pdf
Mod2-Case2A-Homelessness-EMAIL-SINGLE-PAGE.pdf
HANDOFF-NOTES.md
```

---

## 3. Where it goes

- Live server: a new folder under `/wp-content/downloadables/`.
- Suggested folder name: `muv-mod2-case-2a-homelessness`.
- Upload every file in the worksheet folder together. The HTML calls each image by filename.
- Then push the same folder to the `MUV-ACADEMY-WORKSHEETS` repo at the top level as `MUV - MOD 2 - CHARITY HOMELESSNESS`.

---

## 4. Where each image sits, top to bottom

| Position | File |
|---|---|
| Top right logo | form-top-logo.png |
| Title and every section heading | form-arrow-icon.png |
| The Belief hero (volunteer and staff member setting up a table in a library) | muv-homelessness-image-1.jpg |
| How a 30 Day Plan Becomes a Movement hero (three panel shot of a Story Evening, cards going on the board) | muv-homelessness-image-2.jpg |

Both photos are 1920 x 500 and are cropped to fill, so the sides trim a little on screen and more on phones.
| Footer | form-footer-graphic.png |

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

1. Blue Mod.2-CharityCase-2A badge top left, logo top right on the same centre line.
2. 11 arrow icons: one at the title and ten at the section headings. Week bars carry no arrow.
3. Both photographs present.
4. Click Save PDF. It should download the page.
5. Open it on a phone and check everything stacks to a single column.

---

## 8. Technical notes

- One HTML file plus 3 graphics and 2 photographs. No build step.
- Built directly on the Case 2C Recruitment sheet CSS, so the two Module 2 sheets match exactly.
- Save PDF uses `html2pdf.bundle.min.js` 0.10.1 from cdnjs, same as the other case sheets.
- Fonts from Google Fonts, Montserrat 400, 500, 600, 700.

---

## 9. Open items for Marshall, not Jim

- Photos are AI generated. The lanyards in image 1 and a few cards in image 2 carry made-up lettering. Barely readable at page size, but visible if zoomed.
- Image 2 is a three panel shot. On phones the page crops to the middle, so mostly the centre panel shows. That still reads well (the man pinning a card).
- The copy mentions "the national community history programme", "the Commemorative WWII Programme" and "the museum's non-traditional venue approach". Confirm these all refer to the same Module 1 example.
- Footer bottom padding doubled to 40px (was 20px), so the graphic and copyright sit higher. Other case sheets still use 20px.
- Filename follows the siblings: `Mod.2-CaseCHARITY2A.html`.
