# Handoff: Community History Programme Playbook Companion

**For:** Jim
**From:** Marshall
**What it is:** The Module 2 playbook companion (Mod.2-2.5), built on the Alderney playbook companion from Module 1.

It is the Module 2 sibling of `alderney-tourism-playbook.html`. Same layout, footer, disclaimer and buttons. Unlike Alderney it has no course line above the badge and no coloured accent bars or lines on its boxes, tabs or part headers (removed at Marshall's request). The badge and part tags are Module 2 blue (`#005a8d`) instead of Module 1 red. It is fillable: Part 3 has five Yes / Not yet choices plus an optional notes box per step, saved in the browser.

---

## 1. Anything Marshall needs back

The live link once it is up, so it can go into the Module 2 lesson page.

---

## 2. What is in this package

```
MUV - MOD 2 - PLAYBOOK COMPANION/
    community-history-playbook.html
    form-top-logo.png
    form-arrow-icon.png
    form-check-mark-icon.png
    form-footer-graphic.png
    muv-community-history-image-1.jpg
    muv-community-history-image-2.jpg
    muv-community-history-image-3.jpg
    muv-community-history-mcafrika-image.jpg
standalone-email-version/              DO NOT UPLOAD
    community-history-playbook-standalone.html
Community-History-Playbook-A4.pdf
Community-History-Playbook-SINGLE-PAGE.pdf
Community-History-Playbook-EMAIL-A4.pdf
Community-History-Playbook-EMAIL-SINGLE-PAGE.pdf
HANDOFF-NOTES.md
```

---

## 3. Where it goes

- Live server: a new folder under `/wp-content/downloadables/`.
- Suggested folder name: `mod2-playbook-companion` (mirrors `mod1-playbook-companion`).
- Upload every file in the worksheet folder together. The HTML calls each image by filename, so they must sit in the same directory as the HTML.
- Then push the same folder to the `MUV-ACADEMY-WORKSHEETS` repo at the top level.
- Fastest route on GitHub: Add file, Upload files, drag the unzipped folder in.

---

## 4. Where each image sits, top to bottom

| Position | File |
|---|---|
| Logo, top right | form-top-logo.png |
| Arrow on title and every section heading | form-arrow-icon.png |
| Key Lessons, left photo (veteran with pupils in a shopping centre) | muv-community-history-image-1.jpg |
| Key Lessons, right photo (veteran and pupil at a table) | muv-community-history-image-2.jpg |
| Client and Stakeholder Reflections, wide photo (shopping centre blending into beach) | muv-community-history-image-3.jpg |
| Failure case banner (McAfrika stand on a snowy Oslo street) | muv-community-history-mcafrika-image.jpg |
| Need more ideas box | form-check-mark-icon.png |
| Footer | form-footer-graphic.png |


---

## 5. The PDFs

- `Community-History-Playbook-A4.pdf` (8 pages, about 1.1MB): for printing. Part 3 starts on a fresh page.
- `Community-History-Playbook-SINGLE-PAGE.pdf` (about 1.1MB): best for reading on screen and as a download link.
- `-EMAIL-` versions (about 0.95MB): lighter photos, for attaching to emails.

The PDFs are snapshots. They do not update if the HTML changes. Send changes back rather than editing a PDF.

---

## 6. The email version of the HTML

`standalone-email-version/community-history-playbook-standalone.html` (about 650KB) has every image inside it, so it survives being attached and forwarded. Do not upload it to the server, or the live copy and the emailed copy drift apart.

---

## 7. Visual check once it is live

1. Logo top right, blue Mod.2-2.5 badge top left, no course line above it (removed on purpose).
2. 15 arrow icons: one at the title and one at each of the 13 section headings, plus the small ones in the info boxes.
3. The five Part tabs under the title jump to each part.
4. Participation Journey Map, Impact at a Glance and Movement Engine all render (they are code, not images). The Movement Engine is a rectangular loop with an arrow halfway across each gap and a rectangular blue hub in the middle.
5. Every photograph present.
6. Tick a choice, type a note, reload: both are still there. Clear Form empties them.
7. Download PDF saves the page with the buttons hidden.
8. Open it on a phone and check everything stacks to a single column.

---

## 8. Technical notes

- One HTML file plus 8 images. No build step, nothing to install.
- The three infographics are inline SVG and HTML, not image files. A wonky diagram is a code issue, not a missing file.
- Save PDF uses `html2pdf.bundle.min.js` 0.10.1 from cdnjs, same as every other worksheet.
- Fonts from Google Fonts, Montserrat 400, 500, 600, 700.
- localStorage prefix: `muvist-community-history-`.

---

## 9. Open items for Marshall, not Jim

1. Title: the brief says "Alderney Community History Playbook" but the content is not about Alderney. Built as "Community History Programme Playbook Companion" with "Turning a Story into Participation" beneath. One line to change if Alderney was intended.
2. McAfrika image is in. It shows the McDonald's logo and the Olympic rings, both protected marks, and has some garbled AI text on the sign. Worth a final check before it goes live.
3. Pupil quote says "serving soldier" while the programme is about veterans. Left as written.
4. "Tabs" in the brief read as the header lozenge from Alderney, plus new Part tabs under the title.
5. Optional notes boxes added under each Part 3 step. Remove if you want choices only.
