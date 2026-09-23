# Handoff: Mod 2 Case 2D, Independent Fitness Studio or Personal Training Business

**For:** Jim
**From:** Marshall
**What it is:** Module 2 SME case sheet, Scenario 2D (independent fitness studio or PT business).

Read-only case sheet in the same layout as Case 2A (Homelessness), 2B (Veterans) and 2C (Recruitment). The badge is Module 2 blue. No form fields, no browser storage.

---

## 1. Anything Marshall needs back

Nothing. Both photographs are in and the sheet is ready to publish once Marshall signs off the A4 PDF.

---

## 2. What is in this package

```
MUV - MOD 2 - FITNESS/
    Mod.2-CaseSME2D.html
    form-arrow-icon.png
    form-footer-graphic.png
    form-top-logo.png
    muv-fitness-image-1.jpg
    muv-fitness-image-2.jpg
standalone-email-version/
    Mod.2-CaseSME2D-standalone.html      DO NOT UPLOAD
Mod2-Case2D-Fitness-A4.pdf
Mod2-Case2D-Fitness-SINGLE-PAGE.pdf
Mod2-Case2D-Fitness-EMAIL-A4.pdf
Mod2-Case2D-Fitness-EMAIL-SINGLE-PAGE.pdf
HANDOFF-NOTES.md
```

---

## 3. Where it goes

- Live server: a new folder under `/wp-content/downloadables/`.
- Suggested folder name: `muv-mod2-case-2d-fitness`.
- Upload every file in the worksheet folder together. The HTML calls each image by filename.
- Then push the same folder to the `MUV-ACADEMY-WORKSHEETS` repo at the top level as `MUV - MOD 2 - FITNESS`.

---

## 4. Where each image sits, top to bottom

| Position | File |
|---|---|
| Top right logo | form-top-logo.png |
| Title and every section heading | form-arrow-icon.png |
| The Belief hero (owner trainer welcoming an older man with a knee support at the door) | muv-fitness-image-1.jpg |
| How a 30 Day Plan Becomes a Movement hero (new member arm in arm with her mother, class behind) | muv-fitness-image-2.jpg |
| Footer | form-footer-graphic.png |

Both photos are 1920 x 500 and are cropped to fill, so the sides trim a little on screen and more on phones. Image 2 is anchored slightly left (`object-position: 40% center`) so the mother and daughter stay in frame on phones.

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

1. Blue Mod.2-SMECase-2D badge top left, logo top right on the same centre line. No tagline above the badge.
2. 11 arrow icons: one at the title and ten at the section headings. Week bars carry no arrow, matching the other case sheets.
3. Both photographs present.
4. Click Save PDF. It should download the page.
5. Open it on a phone and check everything stacks to a single column.

---

## 8. Technical notes

- One HTML file plus 3 graphics and 2 photographs. No build step.
- Built on the Case 2C CSS unchanged, so it matches the set exactly.
- Save PDF uses `html2pdf.bundle.min.js` 0.10.1 from cdnjs, same as the other case sheets.

---

## 9. Open items for Marshall, not Jim

- Photos are AI generated. No visible lettering, but check hands and faces at full zoom before sign off.
- Header tagline ("Movement Marketing: Extend Reach, Reduce Costs") left off to match 2C and the Module 2 Workbook, even though it is in the source doc.
- Filename follows the siblings: `Mod.2-CaseSME2D.html`.
