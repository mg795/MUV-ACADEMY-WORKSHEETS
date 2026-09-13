---
name: muvist-workbooks
description: Create standardized HTML workbooks and worksheets for MUVIST Academy. Use this skill when creating workbooks, worksheets, scenario documents, learning materials, or any educational HTML document for MUVIST Academy. Triggers include: "create a MUVIST workbook", "make a worksheet", "build a scenario document", "MUVIST educational material", or any mention of MUVIST learning content.
license: Proprietary. For MUVIST Academy use only.
---

# MUVIST Workbook Creation Skill

## When to Use This Skill

Trigger this skill for:
- Creating MUVIST Academy workbooks or worksheets
- Building scenario documents or case studies
- Educational materials for MUVIST courses
- Any structured learning content for MUVIST Academy
- Module materials, lesson plans, or student resources

Before creating any MUVIST workbook, **read this entire skill file** to ensure compliance with brand standards.

---

## Quick Start Checklist

When creating a MUVIST workbook:

1. ✅ Load Montserrat font from Google Fonts
2. ✅ Set up page structure (max-width: 1200px, centered)
3. ✅ Add header with module badge, tagline, and logo
4. ✅ Use form-arrow-icon.png for all section headers
5. ✅ Apply sage green (#809364) to all section titles
6. ✅ Include Save PDF button above footer
7. ✅ Add complete footer with copyright and worksheet info
8. ✅ Verify all spacing follows 30px universal rule
9. ✅ Test responsive breakpoints (768px, 1024px)
10. ✅ Ensure all required image files are referenced

---

## Core Design System

### Typography

**Font Import (Required):**
```html
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet">
```

**Font Sizes:**
- Body: 13px, weight 400, line-height 1.6
- H1 (Main Title): 32px, weight 700, sage green
- H2 (Section Headers): 18px, weight 700, sage green
- Subtitle: 16px, weight 500, medium gray
- Card Titles: 14-15px, weight 700
- Buttons: 14px, weight 600

### Color Palette

**Primary Colors:**
```css
--sage-green: #809364;      /* Section headers, primary brand */
--module-red: #b6141c;       /* Module badge */
--button-green: #b3bf8f;     /* Primary buttons */
--button-hover: #9faa7a;     /* Button hover state */
```

**Text Colors:**
```css
--dark-text: #1a1a1a;        /* Body text */
--medium-gray: #4a4a4a;      /* Subtitles */
--light-gray: #888;          /* Meta text */
```

**Background Colors:**
```css
--cream: #f9f9f7;            /* Section backgrounds */
--light-sage: #d9e4d0;       /* Card headers */
--light-blue: #e8f2f7;       /* FAQ cards */
```

**Border Colors:**
```css
--border-gray: #d0d0d0;      /* Standard borders */
--light-border: #e0e0e0;     /* Subtle dividers */
--faq-header: #2c5f7f;       /* FAQ card header bar */
```

### Spacing System

**Universal Rule: 30px Total Spacing**
- Between sections: 30px top margin + 15px bottom margin on headers
- Left/right content padding: 30px
- Card gaps: 20px
- Paragraph spacing: 15px
- Title to content: 10px (via margin-bottom: -20px on title-section)

---

## Page Structure Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[Title] - MUVIST Academy</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            font-size: 13px;
            font-weight: 400;
            color: #1a1a1a;
            line-height: 1.6;
            background: #f5f5f5;
        }

        .page {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            box-shadow: 0 0 20px rgba(0,0,0,0.1);
        }

        .content {
            padding: 30px;
        }

        /* Add all component styles here */
    </style>
</head>
<body>
    <div class="page">
        <!-- Header, Content, Actions, Footer -->
    </div>
    <script>
        function downloadPDF() {
            const element = document.querySelector('.page');
            const opt = {
                margin: 0,
                filename: 'MUVIST_[Name].pdf',
                image: { type: 'jpeg', quality: 0.98 },
                html2canvas: { scale: 2, useCORS: true },
                jsPDF: { unit: 'in', format: 'letter', orientation: 'portrait' }
            };
            html2pdf().set(opt).from(element).save();
        }
    </script>
</body>
</html>
```

---

## Component Library

### 1. Header (Required for All Workbooks)

**CSS:**
```css
.header {
    position: relative;
    padding: 30px;
    min-height: 120px;
}

.module-badge {
    position: absolute;
    left: 0;
    top: 30px;
    background: #b6141c;
    color: white;
    font-size: 18px;
    font-weight: 700;
    padding: 15px 25px 15px 20px;
    border-radius: 0 25px 25px 0;
}

.header-tagline {
    position: absolute;
    right: 240px;
    top: 51px;
    font-size: 13px;
    font-weight: 700;
    color: #1a1a1a;
    text-align: right;
    white-space: nowrap;
    line-height: 1;
}

.logo {
    position: absolute;
    right: 30px;
    top: 30px;
}

.logo img {
    height: 40px;
    width: auto;
}

.title-section {
    margin-top: 98px;
    margin-bottom: -20px;
    text-align: left;
}

.title-section h1 {
    font-size: 32px;
    color: #809364;
    font-weight: 700;
    display: flex;
    align-items: center;
    gap: 12px;
    justify-content: flex-start;
    margin-bottom: 8px;
}

.header-icon {
    height: 48px;
    width: auto;
}

.subtitle {
    font-size: 16px;
    color: #4a4a4a;
    font-weight: 500;
    margin-top: 8px;
}
```

**HTML:**
```html
<div class="header">
    <div class="module-badge">MODULE 1</div>
    <div class="header-tagline">Movement Marketing; Extend Reach, Reduce Cost.</div>
    <div class="logo">
        <img src="form-top-logo.png" alt="Muvist Academy">
    </div>
    <div class="title-section">
        <h1>
            <img src="form-arrow-icon.png" alt="" class="header-icon">
            SCENARIO TITLE
        </h1>
        <p class="subtitle">Subtitle text</p>
    </div>
</div>
```

### 2. Section Header (Use for All Sections)

**CSS:**
```css
.section-header {
    display: flex;
    align-items: center;
    gap: 12px;
    margin: 30px 0 15px 0;
}

.section-header h2 {
    color: #809364;
    font-size: 18px;
    font-weight: 700;
}

.section-icon {
    height: 44px;
    width: auto;
}
```

**HTML:**
```html
<div class="section-header">
    <img src="form-arrow-icon.png" alt="" class="section-icon">
    <h2>Section Title</h2>
</div>
```

### 3. Info Table (Organization Details)

**When to Use:** Display structured key-value pairs

**CSS:**
```css
.info-table {
    width: 100%;
    border-collapse: collapse;
    margin: 15px 0;
}

.info-table td {
    padding: 12px 15px;
    border: 1px solid #d0d0d0;
}

.info-table td:first-child {
    background: #f9f9f7;
    font-weight: 700;
    width: 30%;
}
```

**HTML:**
```html
<table class="info-table">
    <tr>
        <td>Organisation type</td>
        <td>Value</td>
    </tr>
</table>
```

### 4. Hero Image Section

**When to Use:** Large impactful images for beliefs, movements, key statements

**CSS:**
```css
.movement-hero {
    position: relative;
    width: 100%;
    height: 350px;
    margin: 20px 0;
    overflow: hidden;
    border-radius: 4px;
}

.movement-hero img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

@media (max-width: 768px) {
    .movement-hero {
        height: 250px;
    }
}
```

**HTML:**
```html
<div class="movement-hero">
    <img src="hero-image.jpg" alt="Description">
</div>
```

### 5. Week Plan Sections (Green Header Bars)

**When to Use:** Multi-week plans with grouped activities

**CSS:**
```css
.week-section {
    margin: 30px 0 0 0;
}

.week-header {
    background: #809364;
    color: white;
    padding: 12px 20px;
    font-size: 15px;
    font-weight: 700;
    margin-bottom: 0;
}

.week-content {
    background: #f9f9f7;
    padding: 25px 20px;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

.day-item {
    margin: 0;
    padding: 0;
    font-size: 13px;
    line-height: 1.6;
}

.day-item strong {
    color: #1a1a1a;
    font-weight: 700;
    display: block;
    margin-bottom: 8px;
}

@media (max-width: 1024px) {
    .week-content {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 768px) {
    .week-content {
        grid-template-columns: 1fr;
    }
}
```

**HTML:**
```html
<div class="week-section">
    <div class="week-header">Week 1: Title</div>
    <div class="week-content">
        <div class="day-item">
            <strong>Day 1 to 2: Activity.</strong>
            Description text.
        </div>
    </div>
</div>
```

### 6. Timeline Visualization (Numbered Circles)

**When to Use:** Show progression, milestones, outcomes (3-5 items)

**Circle Colors (Required Sequence):**
1. Red: #b6141c
2. Orange: #e67e22
3. Sage: #809364
4. Blue: #005a8d
5. Light Blue: #5dade2

**CSS:**
```css
.timeline-container {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 20px;
}

.timeline-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    flex: 1;
    position: relative;
}

.timeline-circle {
    width: 90px;
    height: 90px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-size: 48px;
    font-weight: 700;
    margin-bottom: 20px;
    position: relative;
    z-index: 2;
}

.circle-1 { background: #b6141c; }
.circle-2 { background: #e67e22; }
.circle-3 { background: #809364; }
.circle-4 { background: #005a8d; }
.circle-5 { background: #5dade2; }

.timeline-arrow {
    position: absolute;
    top: 45px;
    left: 50%;
    width: 100%;
    height: 0;
    display: flex;
    align-items: center;
    z-index: 1;
}

.timeline-arrow::after {
    content: '';
    width: 100%;
    height: 4px;
    background: currentColor;
}

.timeline-arrow::before {
    content: '';
    position: absolute;
    right: -8px;
    top: 50%;
    transform: translateY(-50%);
    border-left: 12px solid currentColor;
    border-top: 8px solid transparent;
    border-bottom: 8px solid transparent;
}

.arrow-1 { color: #b6141c; }
.arrow-2 { color: #e67e22; }
.arrow-3 { color: #809364; }
.arrow-4 { color: #005a8d; }

.timeline-text {
    text-align: center;
    font-size: 13px;
    line-height: 1.5;
    max-width: 180px;
    color: #1a1a1a;
}

@media (max-width: 1024px) {
    .timeline-container {
        flex-wrap: wrap;
        gap: 40px;
    }
    .timeline-item {
        flex: 0 0 calc(50% - 20px);
    }
    .timeline-arrow {
        display: none;
    }
}

@media (max-width: 768px) {
    .timeline-item {
        flex: 0 0 100%;
    }
    .timeline-circle {
        width: 70px;
        height: 70px;
        font-size: 36px;
    }
}
```

**HTML:**
```html
<div class="timeline-container">
    <div class="timeline-item">
        <div class="timeline-circle circle-1">1</div>
        <div class="timeline-arrow arrow-1"></div>
        <div class="timeline-text">Description</div>
    </div>
    <!-- Last item has no arrow -->
    <div class="timeline-item">
        <div class="timeline-circle circle-5">5</div>
        <div class="timeline-text">Final item</div>
    </div>
</div>
```

### 7. Benefits Card Grid (2x2)

**When to Use:** Display 4 key benefits with header/body separation

**CSS:**
```css
.benefits-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    margin: 20px 0;
}

.benefit-card {
    border: 1px solid #d0d0d0;
    border-radius: 4px;
    overflow: hidden;
}

.benefit-card-header {
    background: #d9e4d0;
    padding: 15px 20px;
    border-bottom: 1px solid #d0d0d0;
}

.benefit-card-title {
    font-size: 14px;
    font-weight: 700;
    color: #1a1a1a;
    text-align: center;
    margin: 0;
}

.benefit-card-body {
    background: white;
    padding: 20px;
}

.benefit-card-text {
    font-size: 13px;
    line-height: 1.6;
    color: #1a1a1a;
    text-align: center;
    margin: 0;
}

@media (max-width: 768px) {
    .benefits-grid {
        grid-template-columns: 1fr;
    }
}
```

**HTML:**
```html
<div class="benefits-grid">
    <div class="benefit-card">
        <div class="benefit-card-header">
            <div class="benefit-card-title">Title</div>
        </div>
        <div class="benefit-card-body">
            <p class="benefit-card-text">Description</p>
        </div>
    </div>
</div>
```

### 8. Customer Cards (3-Column)

**When to Use:** Display 3 items in a row with simple title + description

**CSS:**
```css
.customers-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    margin: 20px 0;
}

.customer-card {
    background: #d9e4d0;
    padding: 25px 20px;
    border-radius: 4px;
}

.customer-card-title {
    font-size: 14px;
    font-weight: 700;
    color: #1a1a1a;
    text-align: center;
    margin-bottom: 15px;
}

.customer-card-divider {
    width: 60px;
    height: 2px;
    background: #1a1a1a;
    margin: 15px auto;
}

.customer-card-text {
    font-size: 13px;
    line-height: 1.6;
    color: #1a1a1a;
    text-align: center;
    margin: 0;
}

@media (max-width: 1024px) {
    .customers-grid {
        grid-template-columns: 1fr;
    }
}
```

**HTML:**
```html
<div class="customers-grid">
    <div class="customer-card">
        <div class="customer-card-title">Title</div>
        <div class="customer-card-divider"></div>
        <p class="customer-card-text">Text</p>
    </div>
</div>
```

### 9. FAQ Card Grid (2x2)

**When to Use:** Q&A format content, 2-4 items

**CSS:**
```css
.faq-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    margin: 20px 0;
}

.faq-card {
    background: #e8f2f7;
    border-radius: 4px;
    overflow: hidden;
}

.faq-header {
    background: #2c5f7f;
    height: 8px;
}

.faq-content {
    padding: 30px 25px;
    text-align: center;
}

.faq-question {
    font-weight: 700;
    color: #1a1a1a;
    font-size: 15px;
    margin-bottom: 15px;
    line-height: 1.4;
}

.faq-divider {
    width: 60px;
    height: 2px;
    background: #2c5f7f;
    margin: 15px auto;
}

.faq-answer {
    color: #1a1a1a;
    font-size: 13px;
    line-height: 1.6;
}

@media (max-width: 768px) {
    .faq-grid {
        grid-template-columns: 1fr;
    }
}
```

**HTML:**
```html
<div class="faq-grid">
    <div class="faq-card">
        <div class="faq-header"></div>
        <div class="faq-content">
            <div class="faq-question">Q: Question?</div>
            <div class="faq-divider"></div>
            <div class="faq-answer">A: Answer.</div>
        </div>
    </div>
</div>
```

### 10. Info Box / Description Box

**Info Box (Callouts):**
```css
.info-box {
    background: #f9f9f7;
    border: 1px solid #d0d0d0;
    border-radius: 4px;
    padding: 15px;
    margin: 15px 0;
    line-height: 1.6;
}

.info-box strong {
    font-weight: 700;
    color: #1a1a1a;
}
```

**Description Box (After images):**
```css
.movement-description {
    background: #f5f5f5;
    border: 1px solid #d0d0d0;
    border-radius: 4px;
    padding: 25px 30px;
    margin: 20px 0;
    font-size: 15px;
    line-height: 1.7;
    color: #1a1a1a;
}
```

---

## Buttons & Actions

**Actions Container:**
```css
.actions {
    padding: 20px 30px;
    background: #f9f9f7;
    display: flex;
    gap: 12px;
    justify-content: center;
    margin-top: 30px;
    border: none;
}

.actions button {
    padding: 12px 24px;
    border: 1px solid #b3bf8f;
    background: white;
    border-radius: 4px;
    font-family: 'Montserrat', sans-serif;
    font-size: 14px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.2s;
    color: #1a1a1a;
}

.actions button:hover {
    background: #f5f5f5;
    border-color: #b3bf8f;
}

.actions button.primary {
    background: #b3bf8f;
    color: white;
    border-color: #b3bf8f;
}

.actions button.primary:hover {
    background: #9faa7a;
    border-color: #9faa7a;
}
```

**HTML:**
```html
<div class="actions">
    <button type="button" class="primary" onclick="downloadPDF()">Save PDF</button>
</div>
```

**PDF Function:**
```javascript
function downloadPDF() {
    const element = document.querySelector('.page');
    const opt = {
        margin: 0,
        filename: 'MUVIST_DocumentName.pdf',
        image: { type: 'jpeg', quality: 0.98 },
        html2canvas: { scale: 2, useCORS: true },
        jsPDF: { unit: 'in', format: 'letter', orientation: 'portrait' }
    };
    html2pdf().set(opt).from(element).save();
}
```

---

## Footer (Required)

**CSS:**
```css
.footer {
    padding: 20px;
    background: white;
    text-align: center;
    display: flex;
    flex-direction: column;
    gap: 15px;
    align-items: center;
}

.footer-graphic {
    height: 30px;
    width: auto;
}

.footer-copyright {
    font-size: 10px;
    color: #666;
    line-height: 1.5;
    max-width: 800px;
}

.footer-worksheet {
    font-size: 10px;
    color: #666;
    line-height: 1.5;
    margin-top: 10px;
}
```

**HTML:**
```html
<div class="footer">
    <div class="footer-content">
        <img src="form-footer-graphic.png" alt="" class="footer-graphic">
    </div>
    <div class="footer-copyright">
        <strong>MUVIST Academy, Movement Marketing Education and Services</strong><br>
        [Document Type] | Module [X] Scenario<br>
        © 2026 MUVIST Ltd. All rights reserved.<br>
        [Additional text]<br>
        For permissions or licensing enquiries: become@muvist.com | +44 (0)330 043 5663 | www.muvist.com
    </div>
    <div class="footer-worksheet">
        MUVIST Academy · Quick Check Worksheet · Lesson [X] Module [X] · © 2026 MUVIST Ltd. All rights reserved. Reproduction for internal organisational use only.
    </div>
</div>
```

---

## Required Assets

**All workbooks MUST include these files in the same directory:**
1. `form-top-logo.png` - MUVIST Academy logo (40px height)
2. `form-footer-graphic.png` - Footer branding graphic (30px height)
3. `form-arrow-icon.png` - Universal icon for section headers (44px for sections, 48px for title)

---

## Responsive Breakpoints

**Tablet (max-width: 1024px):**
- Week content: 2 columns
- Timeline: 2 items per row, hide arrows
- Customer cards: Stack to single column

**Mobile (max-width: 768px):**
- All grids: Single column
- Hero images: 250px height
- Timeline circles: 70px diameter, 36px font
- Week content: Single column
- Benefits grid: Single column
- FAQ grid: Single column

---

## Component Selection Decision Tree

**Choose Timeline when:**
- 3-5 sequential steps
- Need numbered progression
- Want visual flow with arrows

**Choose Benefits Grid when:**
- Exactly 4 items
- Need header/body separation
- Want bordered cards

**Choose Customer Cards when:**
- Exactly 3 items
- Simple title + description
- All same background color

**Choose Week Plan when:**
- Multi-week structure
- Activities grouped by time
- 2-3 items per week

**Choose FAQ Grid when:**
- Q&A format
- 2-4 questions
- Need visual question/answer separation

**Choose Hero Image when:**
- Key belief statements
- Movement/transformation moments
- Need emotional visual impact

---

## Critical Rules (Non-Negotiable)

1. **ALWAYS** use Montserrat font family
2. **ALWAYS** use sage green (#809364) for section headers
3. **ALWAYS** set title-section margin-bottom: -20px
4. **NEVER** add border-top to footer
5. **ALWAYS** use form-arrow-icon.png for section icons
6. **ALWAYS** include Save PDF button above footer
7. **ALWAYS** make grids responsive (single column on mobile)
8. **ALWAYS** use correct timeline circle color sequence
9. **NEVER** use 4-column layouts (max 3 columns)
10. **ALWAYS** include complete footer with copyright

---

## Quality Verification Checklist

Before delivering, verify:
- [ ] Montserrat font loaded
- [ ] Module badge at left: 0, top: 30px
- [ ] Tagline at right: 240px, top: 51px
- [ ] Logo at right: 30px, top: 30px
- [ ] Title margin-bottom: -20px
- [ ] All headers sage green (#809364)
- [ ] Section icons 44px, title icon 48px
- [ ] Timeline uses correct color sequence
- [ ] Grids responsive (single column mobile)
- [ ] Save PDF button present
- [ ] Footer has no border-top
- [ ] All 3 image files referenced
- [ ] PDF download function included
- [ ] Mobile tested (768px breakpoint)

---

## Common Errors to Avoid

❌ **DON'T:** Add border-top to footer (creates grey line)  
✅ **DO:** Leave footer border: none

❌ **DON'T:** Forget margin-bottom: -20px on title-section  
✅ **DO:** Always set negative margin for 10px gap

❌ **DON'T:** Make timeline arrows visible on mobile  
✅ **DO:** Hide arrows at 1024px breakpoint

❌ **DON'T:** Use 4-column benefit grids  
✅ **DO:** Always use 2x2 grid (2 columns)

❌ **DON'T:** Forget 8px blue header on FAQ cards  
✅ **DO:** Include faq-header div with #2c5f7f background

❌ **DON'T:** Stack week content vertically by default  
✅ **DO:** Use 3-column grid, responsive to 2 then 1

❌ **DON'T:** Use different green shades  
✅ **DO:** Stick to #809364 (headers) and #b3bf8f (buttons)

---

## Workflow for Creating a MUVIST Workbook

1. **Read this entire skill file first**
2. Set up HTML structure with header, content, actions, footer
3. Add Montserrat font and html2pdf.js library
4. Create header with module badge, tagline, logo, title
5. Add content sections using appropriate components
6. Include Save PDF button above footer
7. Add complete footer with copyright
8. Verify responsive breakpoints
9. Test PDF download functionality
10. Run quality checklist

---

## Notes for Skill Usage

- This skill was developed from MUVIST Module 1 Scenario 1C workbook
- All measurements are calibrated for brand consistency
- Components are modular and reusable
- Prioritize visual hierarchy through sage green headers
- Focus on scannability through card-based layouts
- Maintain professional appearance through spacing
- Ensure brand consistency through standardized colors
- Support responsive design for all devices

**When in doubt, refer to this skill file rather than improvising.**

---

**Skill Version:** 1.0  
**Last Updated:** March 2026  
**Source:** MUVIST Module 1 Scenario 1C Development  
**Maintained By:** MUVIST Academy Design Team
