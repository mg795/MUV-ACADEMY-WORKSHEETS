---
name: muvist-workbooks
description: Design and build standardized HTML workbooks and worksheets for MUVIST Academy following established brand standards. Use this skill when creating any workbook, worksheet, scenario document, or educational resource for MUVIST Academy. Triggers include requests to create workbooks, worksheets, learning materials, scenario documents, or any educational HTML document for MUVIST Academy.
---

# MUVIST Academy Workbook Design Standards

This document encapsulates the complete design system for creating standardized HTML workbooks and worksheets for MUVIST Academy. All workbooks should follow these standards for visual consistency and brand alignment.

## Core Typography

**Primary Font:** Montserrat (Google Fonts)
- Import all weights: 400, 500, 600, 700
- Use: `@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap');`

**Font Usage:**
- Body text: 13px, weight 400, line-height: 1.6
- Section headers (h2): 18px, weight 700
- Main title (h1): 32px, weight 700
- Subtitle text: 16px, weight 500
- Card titles: 14-15px, weight 700
- Buttons: 14px, weight 600

## Color Palette

**Brand Colors:**
- Sage Green (primary brand color): `#809364`
- Module Badge Red: `#b6141c`
- Button Green: `#b3bf8f`
- Button Green Hover: `#9faa7a`
- Dark Text: `#1a1a1a`
- Medium Gray: `#4a4a4a`
- Light Gray: `#888`
- Border Gray: `#d0d0d0`
- Light Border: `#e0e0e0`
- Background Cream: `#f9f9f7`
- Light Sage Background: `#d9e4d0`
- FAQ Card Background: `#e8f2f7`
- FAQ Header Bar: `#2c5f7f`

**Color Application Rules:**
- All section titles and headers: Sage green (#809364)
- Module badge background: Red (#b6141c) with white text
- Primary action buttons: Green (#b3bf8f)
- All button borders and hover states: Green (#b3bf8f)
- Body text: Dark (#1a1a1a)
- Subtitles/descriptions: Medium gray (#4a4a4a)

## Page Structure

**Container (.page):**
```css
max-width: 1200px;
margin: 0 auto;
background: white;
box-shadow: 0 0 20px rgba(0,0,0,0.1);
```

**Content (.content):**
```css
padding: 30px;
```

## Header Structure

**Module Badge:**
- Position: `position: absolute; left: 0; top: 30px;`
- Style: Red background (#b6141c), white text, rounded right edge
- Font: 18px, weight 700
- Padding: 15px 25px 15px 20px
- Border radius: 0 25px 25px 0

**Tagline ("Movement Marketing; Extend Reach, Reduce Cost."):**
- Position: `position: absolute; right: 240px; top: 51px;`
- Font: 13px, weight 700
- Color: Dark text (#1a1a1a)
- Text align: right
- White-space: nowrap
- Line-height: 1

**MUVIST Academy Logo:**
- Position: `position: absolute; right: 30px; top: 30px;`
- Height: 40px
- Width: auto (maintains aspect ratio)
- File: form-top-logo.png

**Title Section:**
- Margin-top: 98px
- Margin-bottom: -20px (creates 10px gap to content below)
- Text-align: left
- Main title (h1): 32px, sage green (#809364), weight 700
- Icon before title: 48px height, 12px gap
- Subtitle: 16px, medium gray (#4a4a4a), weight 500
- Title and subtitle: left-aligned

**Header HTML Template:**
```html
<div class="header">
    <div class="module-badge">MODULE [NUMBER]</div>
    <div class="header-tagline">Movement Marketing; Extend Reach, Reduce Cost.</div>
    <div class="logo">
        <img src="form-top-logo.png" alt="Muvist Academy">
    </div>
    <div class="title-section">
        <h1>
            <img src="form-arrow-icon.png" alt="" class="header-icon">
            [SCENARIO TITLE]
        </h1>
        <p class="subtitle">[Subtitle text]</p>
    </div>
</div>
```

## Section Headers

**Standard Section Header:**
- Display: flex, align-items: center
- Icon: 44px height (form-arrow-icon.png)
- Gap between icon and text: 12px
- Text: h2, sage green (#809364), weight 700, 18px
- Margin: 30px top, 15px bottom (creates 30px total spacing from elements above)

**Section Header HTML:**
```html
<div class="section-header">
    <img src="form-arrow-icon.png" alt="" class="section-icon">
    <h2>Section Title</h2>
</div>
```

## Component Patterns

### 1. Info Table (Organization Details)

**Use Case:** Display structured information in a two-column table format

**Styling:**
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

**HTML Example:**
```html
<table class="info-table">
    <tr>
        <td>Label</td>
        <td>Value</td>
    </tr>
</table>
```

### 2. Hero Image Section

**Use Case:** Large impactful images for key beliefs or movement statements

**Styling:**
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

/* Responsive */
@media (max-width: 768px) {
    .movement-hero {
        height: 250px;
    }
}
```

**HTML Example:**
```html
<div class="movement-hero">
    <img src="hero-image.jpg" alt="Description">
</div>
```

### 3. Week Plan Sections (Green Header Bars)

**Use Case:** Multi-week plans with activities grouped by week

**Styling:**
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

/* Responsive */
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

**HTML Example:**
```html
<div class="week-section">
    <div class="week-header">Week 1: Title</div>
    <div class="week-content">
        <div class="day-item">
            <strong>Day 1 to 2: Activity Title.</strong>
            Activity description text.
        </div>
        <!-- More day items -->
    </div>
</div>
```

### 4. Timeline Visualization (Numbered Circles)

**Use Case:** Show progression or milestones with numbered circles and connecting arrows

**Styling:**
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
    position: relative;
}

.timeline-arrow::before {
    content: '';
    position: absolute;
    right: -8px;
    top: 50%;
    transform: translateY(-50%);
    width: 0;
    height: 0;
    border-left: 12px solid currentColor;
    border-top: 8px solid transparent;
    border-bottom: 8px solid transparent;
    z-index: 1;
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

/* Responsive */
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

**HTML Example:**
```html
<div class="timeline-container">
    <div class="timeline-item">
        <div class="timeline-circle circle-1">1</div>
        <div class="timeline-arrow arrow-1"></div>
        <div class="timeline-text">First milestone description</div>
    </div>
    <!-- More timeline items -->
    <div class="timeline-item">
        <div class="timeline-circle circle-5">5</div>
        <div class="timeline-text">Final milestone (no arrow after last item)</div>
    </div>
</div>
```

### 5. Benefits Card Grid (2x2 Layout)

**Use Case:** Display key benefits in a structured card grid with headers and descriptions

**Styling:**
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

/* Responsive */
@media (max-width: 768px) {
    .benefits-grid {
        grid-template-columns: 1fr;
    }
}
```

**HTML Example:**
```html
<div class="benefits-grid">
    <div class="benefit-card">
        <div class="benefit-card-header">
            <div class="benefit-card-title">Benefit Title</div>
        </div>
        <div class="benefit-card-body">
            <p class="benefit-card-text">Benefit description text.</p>
        </div>
    </div>
    <!-- More benefit cards -->
</div>
```

### 6. Customer Cards (3-Column Layout)

**Use Case:** Simple cards with titles and descriptions, all on sage background

**Styling:**
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

/* Responsive */
@media (max-width: 1024px) {
    .customers-grid {
        grid-template-columns: 1fr;
    }
}
```

**HTML Example:**
```html
<div class="customers-grid">
    <div class="customer-card">
        <div class="customer-card-title">Card Title</div>
        <div class="customer-card-divider"></div>
        <p class="customer-card-text">Card description text.</p>
    </div>
    <!-- More customer cards -->
</div>
```

### 7. FAQ Card Grid (2x2 Layout)

**Use Case:** Frequently asked questions in card format with visual separation

**Styling:**
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
    text-align: center;
}

/* Responsive */
@media (max-width: 768px) {
    .faq-grid {
        grid-template-columns: 1fr;
    }
}
```

**HTML Example:**
```html
<div class="faq-grid">
    <div class="faq-card">
        <div class="faq-header"></div>
        <div class="faq-content">
            <div class="faq-question">Q: Question text?</div>
            <div class="faq-divider"></div>
            <div class="faq-answer">A: Answer text.</div>
        </div>
    </div>
    <!-- More FAQ cards -->
</div>
```

### 8. Description Box

**Use Case:** Highlighted text sections with background and border

**Styling:**
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

### 9. Info Box (Before You Start, Important Note)

**Use Case:** Callout boxes for important information

**Styling:**
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

## Button Standards

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
```

**All Buttons:**
```css
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
```

**Primary Button (Save PDF, Submit, etc.):**
```css
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

**Button HTML:**
```html
<div class="actions">
    <button type="button" class="primary" onclick="downloadPDF()">Save PDF</button>
</div>
```

## Footer Standards

**Footer Content:**
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
```

**Footer Graphic:**
```css
.footer-graphic {
    height: 30px;
    width: auto;
}
```

**Copyright Text:**
```css
.footer-copyright {
    font-size: 10px;
    color: #666;
    line-height: 1.5;
    max-width: 800px;
}
```

**Worksheet Footer:**
```css
.footer-worksheet {
    font-size: 10px;
    color: #666;
    line-height: 1.5;
    margin-top: 10px;
}
```

**Footer HTML Template:**
```html
<div class="footer">
    <div class="footer-content">
        <img src="form-footer-graphic.png" alt="" class="footer-graphic">
    </div>
    <div class="footer-copyright">
        <strong>MUVIST Academy, Movement Marketing Education and Services</strong><br>
        [Document Type] | Module [X] Scenario<br>
        © 2026 MUVIST Ltd. All rights reserved.<br>
        [Additional copyright text]<br>
        For permissions or licensing enquiries: become@muvist.com | +44 (0)330 043 5663 | www.muvist.com
    </div>
    <div class="footer-worksheet">
        MUVIST Academy · Quick Check Worksheet · Lesson [X] Module [X] · © 2026 MUVIST Ltd. All rights reserved. Reproduction for internal organisational use only.
    </div>
</div>
```

## Spacing Standards

**Universal Spacing Rules:**
- Section spacing: 30px between major sections (achieved with 30px top margin + 15px bottom margin on section headers)
- Content padding: 30px left/right throughout
- Card gaps: 20px
- Paragraph spacing: 15px margin top/bottom
- Title to content: 10px gap (achieved with negative margin on title-section)

## Required Assets

All workbooks require these image files in the same directory:
1. `form-top-logo.png` - MUVIST Academy logo (header)
2. `form-footer-graphic.png` - Footer graphic
3. `form-arrow-icon.png` - Universal icon for section headers and title

## PDF Download Functionality

**Required Library:**
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
```

**Download Function:**
```javascript
function downloadPDF() {
    const element = document.querySelector('.page');
    const opt = {
        margin: 0,
        filename: 'MUVIST_[DocumentName].pdf',
        image: { type: 'jpeg', quality: 0.98 },
        html2canvas: { scale: 2, useCORS: true },
        jsPDF: { unit: 'in', format: 'letter', orientation: 'portrait' }
    };
    html2pdf().set(opt).from(element).save();
}
```

## Responsive Design

**Mobile Breakpoint: max-width: 768px**
- Week content grid: Stack to single column
- Benefits grid: Stack to single column
- FAQ grid: Stack to single column
- Timeline: Stack vertically, hide arrows
- Customer cards: Stack to single column
- Hero images: Reduce height to 250px
- Header adjustments: Stack elements vertically

**Tablet Breakpoint: max-width: 1024px**
- Week content: 2 columns
- Timeline: 2 columns per row
- Customer cards: Stack to single column

## Complete HTML Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[Document Title] - MUVIST Academy</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
    <style>
        /* All CSS from this document */
    </style>
</head>
<body>
    <div class="page">
        <!-- Header -->
        <div class="header">
            <div class="module-badge">MODULE [X]</div>
            <div class="header-tagline">Movement Marketing; Extend Reach, Reduce Cost.</div>
            <div class="logo">
                <img src="form-top-logo.png" alt="Muvist Academy">
            </div>
            <div class="title-section">
                <h1>
                    <img src="form-arrow-icon.png" alt="" class="header-icon">
                    [DOCUMENT TITLE]
                </h1>
                <p class="subtitle">[Subtitle]</p>
            </div>
        </div>

        <!-- Content -->
        <div class="content">
            <!-- Sections go here using patterns from this document -->
        </div>

        <!-- Actions -->
        <div class="actions">
            <button type="button" class="primary" onclick="downloadPDF()">Save PDF</button>
        </div>

        <!-- Footer -->
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
    </div>

    <script>
        function downloadPDF() {
            const element = document.querySelector('.page');
            const opt = {
                margin: 0,
                filename: 'MUVIST_[DocumentName].pdf',
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

## Quality Checklist

Before delivering any MUVIST workbook, verify:
- [ ] Montserrat font loaded from Google Fonts
- [ ] All colors match brand palette
- [ ] Module badge positioned at left: 0, top: 30px
- [ ] Tagline positioned at right: 240px, top: 51px
- [ ] Logo positioned at right: 30px, top: 30px, height: 40px
- [ ] Title section margin-bottom: -20px for 10px gap to content
- [ ] Section icons: 44px for sections, 48px for main title
- [ ] Green header bars (#809364) for week sections
- [ ] Timeline circles use correct color sequence
- [ ] Benefits cards use 2-column grid
- [ ] Customer cards use 3-column grid
- [ ] FAQ cards have blue header bars and light blue backgrounds
- [ ] All buttons have green borders (#b3bf8f)
- [ ] Primary button has green background
- [ ] Footer has no border-top
- [ ] All three image files referenced correctly
- [ ] PDF download functionality implemented
- [ ] Responsive design for mobile and tablet
- [ ] All spacing follows 30px universal rule

## Common Mistakes to Avoid

1. **DO NOT** add border-top to footer - creates unwanted grey line
2. **DO NOT** use different shades of green - stick to #b3bf8f for buttons and #809364 for headers
3. **DO NOT** forget to set margin-bottom: -20px on title-section
4. **DO NOT** make timeline arrows visible on mobile - hide them at tablet breakpoint
5. **DO NOT** use 4-column layout for benefits - always 2x2 grid
6. **DO NOT** forget the 8px blue header bar on FAQ cards
7. **DO NOT** use border-bottom on week-header - content flows directly
8. **DO NOT** forget to make grids responsive - single column on mobile

## Component Selection Guide

**Use Timeline Visualization when:**
- Showing progression or milestones (3-5 steps)
- Need visual flow with numbered stages
- Want to emphasize sequence and order

**Use Benefits Card Grid when:**
- Displaying 4 key benefits or features
- Need header/body separation
- Want professional bordered appearance

**Use Customer Cards when:**
- Displaying 3 items in a row
- Simple title + description format
- All content on same background

**Use Week Plan Sections when:**
- Multi-week structured plans
- Activities grouped by time periods
- Need expandable content areas

**Use FAQ Cards when:**
- Q&A format content
- Want visual distinction between question and answer
- 2-4 FAQ items to display

**Use Hero Images when:**
- Key belief statements
- Movement or transformation moments
- Need visual impact and emotional connection

## Notes

This design system was developed through iterative refinement based on MUVIST Academy Module 1 Scenario 1C workbook. Every measurement, color, and spacing value has been carefully calibrated for visual consistency and brand alignment. Adherence to these standards ensures professional, cohesive workbooks across all MUVIST Academy educational materials.

The system prioritizes:
- **Visual hierarchy** through consistent use of sage green for headers
- **Scannability** through card-based layouts and structured grids
- **Professional appearance** through controlled spacing and typography
- **Brand consistency** through standardized colors and components
- **Responsive design** for accessibility across devices
- **Reusability** through modular component patterns

---

**Document Version:** 1.0  
**Last Updated:** March 2026  
**Created From:** MUVIST Module 1 Scenario 1C Workbook Development  
**Maintained By:** MUVIST Academy Design Team
