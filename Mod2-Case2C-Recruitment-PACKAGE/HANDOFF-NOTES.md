# Handoff: Mod 2 Case 2C, Local Recruitment and Staffing Agency

**For:** Jim
**From:** Marshall
**What it is:** Module 2 SME case sheet, Scenario 2C (local recruitment and staffing agency).

Read-only case sheet in the same layout as the Module 1 case sheets (Hotel 1D, Construction 1C, Hospice 1B, Conservation 1A). The badge is Module 2 blue. No form fields, no browser storage.

---

## 1. Anything Marshall needs back

Nothing. Both photographs are in and the sheet is ready to publish once Marshall signs off the A4 PDF.

---

## 2. What is in this package

```
MUV - MOD 2 - RECRUITMENT/
    Mod.2-CaseSME2C.html
    form-arrow-icon.png
    form-footer-graphic.png
    form-top-logo.png
    muv-recruitment-image-1.jpg
    muv-recruitment-image-2.jpg
standalone-email-version/
    Mod.2-CaseSME2C-standalone.html      DO NOT UPLOAD
Mod2-Case2C-Recruitment-A4.pdf
Mod2-Case2C-Recruitment-SINGLE-PAGE.pdf
Mod2-Case2C-Recruitment-EMAIL-A4.pdf
Mod2-Case2C-Recruitment-EMAIL-SINGLE-PAGE.pdf
HANDOFF-NOTES.md
```

---

## 3. Where it goes

- Live server: a new folder under `/wp-content/downloadables/`.
- Suggested folder name: `muv-mod2-case-2c-recruitment`.
- Upload every file in the worksheet folder together. The HTML calls each image by filename.
- Then push the same folder to the `MUV-ACADEMY-WORKSHEETS` repo at the top level as `MUV - MOD 2 - RECRUITMENT`.

---

## 4. Where each image sits, top to bottom

| Position | File |
|---|---|
| Top right logo | form-top-logo.png |
| Title and every section heading | form-arrow-icon.png |
| The Belief hero (agency team with a tradesperson on site) | muv-recruitment-image-1.jpg |
| How a 30 Day Plan Becomes a Movement hero (electrician and his boss over coffee) | muv-recruitment-image-2.jpg |
| Footer | form-footer-graphic.png |

Both photos are 1920 x 500 and are cropped to fill, so the sides trim a little on screen and more on phones.

---

## 5. The PDFs

- `-A4.pdf` is for printing, 4 pages, about 0.6MB.
- `-SINGLE-PAGE.pdf` is one long page for screen and download links, about 0.6MB.
- The `-EMAIL-` versions are the same pages with lighter photos, about 0.45MB, for attaching to emails.
- The PDFs are snapshots. They do not update if the HTML changes. Send changes back rather than editing a PDF.

---

## 6. The email version of the HTML

`standalone-email-version/` holds one file with every graphic inside it, for attaching to emails. Do not upload it to the server.

---

## 7. Visual check once it is live

1. Blue Mod.2-SMECase-2C badge top left, logo top right on the same centre line. No tagline above the badge.
2. 10 arrow icons: one at the title and nine at the section headings. Week bars carry no arrow, matching the Module 1 case sheets.
3. Both photographs present.
4. Click Save PDF. It should download the page.
5. Open it on a phone and check everything stacks to a single column.

---

## 8. Technical notes

- One HTML file plus 3 graphics and 2 photographs. No build step.
- Built on the Hotel 1D case sheet CSS. Added: the numbered "Three Things to Keep Top of Mind" cards, a blue-edged "Do not forget" box and print break rules.
- Save PDF uses `html2pdf.bundle.min.js` 0.10.1 from cdnjs, same as the other case sheets.
- Fonts from Google Fonts, Montserrat 400, 500, 600, 700.

---

## 9. Open items for Marshall, not Jim

- Photos are AI generated (Midjourney). The chalkboard menu and the small logo on the fleece in image 2 contain made-up lettering. Barely readable at page size, but visible if zoomed.
- Header tagline removed and logo centred on the badge line, as on the Module 2 Workbook. Module 1 case sheets still carry the tagline.
- Filename follows the siblings: `Mod.2-CaseSME2C.html`.
