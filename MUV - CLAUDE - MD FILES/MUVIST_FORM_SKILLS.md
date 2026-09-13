---
name: muvist-forms
description: Design and build interactive HTML forms for Muvist Academy following established brand standards. Use this skill when creating any form, worksheet, audit, or interactive tool for Muvist Academy. Triggers include requests to create forms, worksheets, self-assessments, checklists, or any interactive HTML document for Muvist Academy.
---

# Muvist Academy Forms Design Standards

This skill encapsulates the complete design system for creating interactive HTML forms for Muvist Academy. All forms should follow these standards for visual consistency and brand alignment.

## Core Typography

**Primary Font:** Montserrat (Google Fonts)
- Import all weights: 400, 500, 600, 700
- Use: `@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap');`

**Font Usage:**
- Body text: 13px, weight 400
- Labels/headings: 13-14px, weight 700
- Section titles: Use weight 700
- Main title (h1): 32px, weight 700
- Buttons: 14px, weight 600

## Color Palette

**Brand Colors:**
- Sage Green (headers, section titles): `#809364`
- Module Badge Red: `#b6141c`
- Button Green: `#b3bf8f`
- Button Green Hover: `#9faa7a`
- Dark Text: `#1a1a1a`
- Medium Gray: `#4a4a4a`
- Light Gray: `#888`
- Border Gray: `#d0d0d0`
- Light Border: `#e0e0e0`
- Background Cream: `#f9f9f7`

**Color Application Rules:**
- All section titles: Sage green (#809364)
- Module badge background: Red (#b6141c) with white text
- Primary action button: Green (#b3bf8f)
- All button borders and hover states: Green (#b3bf8f)
- Body text: Dark (#1a1a1a)
- Hints/descriptions: Medium gray (#4a4a4a)

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
- **Critical Alignment:** Baseline must align with the bottom of the letter "M" in "muvist" in the logo text
- Text align: right
- White-space: nowrap
- Line-height: 1

**Muvist Academy Logo:**
- Position: `position: absolute; right: 30px; top: 30px;`
- Height: 40px
- Width: auto (maintains aspect ratio)
- File: form-top-logo.png

**Title Section:**
- Margin-top: 98px
- Text-align: left
- Main title (h1): 32px, sage green (#809364), weight 700
- Icon before title: 48px height, 12px gap
- Subtitle: 16px, medium gray (#4a4a4a), weight 500
- Title and subtitle: left-aligned (justify-content: flex-start)

## Content Sections

**UNIVERSAL PADDING RULE:**
- **30px is the TOTAL spacing between ALL elements**
- Achieved by: 15px padding/margin on top + 15px padding/margin on bottom = 30px total
- Left padding: 30px (from page edge)
- Right padding: 30px (from page edge)
- Between components: 15px margin-top + 15px margin-bottom = 30px total gap
- This creates consistent 30px visual rhythm throughout the entire form

**Section Spacing:**
- Left/right padding throughout: 30px
- Vertical spacing between sections: 30px total (15px + 15px)

**Section Headers:**
- Icon: 44px height, aligned with text
- Text: h2, sage green (#809364), weight 700
- Gap between icon and text: 12px
- **CRITICAL SPACING RULE:** Spacing above and below section headers must be equal
  - Margin-top: [equal value]
  - Margin-bottom: [equal value]
  - This includes the space from any object/text above the header to the header itself, and from the header to the content below

**Info Boxes ("Before you start", "Important note"):**
- Icon: 26px height
- Background: light cream (#f9f9f7)
- Border: 1px solid #d0d0d0
- Border-radius: 4px
- Padding: 15px
- Strong tags: weight 700, dark text
- Line-height: 1.6

## Form Field Standards

**Text Inputs:**
- Width: 100%
- Padding: 12px
- Border: 1px solid #d0d0d0
- Border-radius: 4px
- Font: 14px Montserrat
- Focus state: border color changes to sage green

**Textareas:**
- Min-height: 120px
- Width: 100%
- Padding: 12px
- Border: 1px solid #d0d0d0
- Border-radius: 4px
- Font: 14px Montserrat, weight 400
- Resize: vertical

## Quadrants Section (if applicable)

**Grid Layout:**
- Display: grid
- Grid-template-columns: repeat(2, 1fr)
- Gap: 20px
- Responsive: Stack vertically on mobile (max-width: 768px)

**Quadrant Styling:**
- Border: 1px solid #d0d0d0
- Border-radius: 4px
- Overflow: hidden

**Quadrant Headers:**
- Background: light cream (#f9f9f7)
- Padding: 12px 15px
- Border-bottom: 1px solid #d0d0d0

**Quadrant Number/Title:**
- Font: 13px, weight 700
- Color: sage green (#809364)
- Margin-bottom: 8px

**Hint Text:**
- Font: 13px, weight 400
- Color: medium gray (#4a4a4a)
- Line-height: 1.5

## Reusable Component Patterns

The following patterns can be mixed and matched in any MUVIST form based on content needs:

### Pattern 1: Label-Description-Input Grid
**When to use:** Rating scales, scoring grids, assessments with numerical inputs
**Example uses:** Signal strength checks, competency ratings, feature scoring

### Pattern 2: Checkbox Selection Grid  
**When to use:** Multiple choice selections, option choosing, verdict/decision sections
**Example uses:** Plan selection, readiness assessments, configuration choices

### Pattern 3: Quadrants Grid
**When to use:** Four-section organizational frameworks, categorization exercises
**Example uses:** SWOT analysis, portfolio mapping, strategic planning

### Pattern 4: Simple Text Input
**When to use:** Open-ended responses, descriptions, narrative inputs
**Example uses:** Organization descriptions, goal statements, reflection responses

All patterns follow the same core standards (typography, colors, spacing) but serve different interaction purposes.

## Component Pattern: Label-Description-Input Grid (for ratings, scores, assessments)

**Use Case:** When you need rows with a label/description on the left and an input field on the right (e.g., rating scales, scoring grids, assessment checklists)

**Container:**
- Margin: 20px 0

**Each Row:**
- Display: grid
- Grid-template-columns: 1fr auto
- Gap: 15px
- Padding: 12px 0
- Border-bottom: 1px solid #e0e0e0
- Align-items: end (aligns input field with description baseline)

**Border Management:**
- Last row: no border-bottom
- If there's a summary/total row, remove border from second-to-last row (use `:nth-last-child(2)`)

**Label Section:**
- Font-size: 13px
- Color: #1a1a1a
- Line-height: 1.4

**Label Header (Strong Tag):**
- Color: sage green (#809364)
- Font-weight: 700
- Display: block
- Margin-bottom: -2px (tightens spacing with description)
- Line-height: 1.2
- **CRITICAL:** Very tight spacing between header and description - no visible gap

**Input Section:**
- Font-size: 13px
- Font-weight: 400
- White-space: nowrap
- Display: flex
- Align-items: baseline (aligns label, input, and suffix)
- Gap: 8px
- Padding-bottom: 0

**Input Field:**
- Width: 40px (adjust as needed)
- Text-align: center
- Padding: 4px
- Border: none
- Border-bottom: 1px solid #1a1a1a (underline style)
- Background: transparent
- Font: 13px Montserrat, weight 400
- Focus: border-bottom 2px solid #809364

**Summary/Total Row (if applicable):**
- Background: #f9f9f7
- Font-weight: 700
- Margin-top: 0 (no gap above)
- Border-top: 2px solid #809364
- Padding-top: 12px
- Display: grid (same as other rows)
- **CRITICAL:** Labels on both left and right must align on same baseline

**Info/Guide Box (if applicable):**
- Background: #f9f9f7
- Padding: 15px
- Border-radius: 4px
- Font: 13px
- Text-align: center
- Line-height: 1.6
- Strong tags: sage green color

## Component Pattern: Checkbox Selection Grid (for options, choices, verdicts)

**Use Case:** When you need multiple choice options displayed side-by-side or in a grid (e.g., assessment verdicts, plan selection, option choosing)

**Grid Layout:**
- Display: grid
- Grid-template-columns: repeat(3, 1fr) [or 2, or 4, depending on number of options]
- Gap: 30px
- Responsive: Stack vertically on mobile (grid-template-columns: 1fr)

**Each Option Box:**
- Background: white
- Border: 1px solid #d0d0d0
- Border-radius: 4px
- Transition: all 0.2s
- Hover: border-color changes to sage green (#809364)

**Content Structure:**
- Padding: 15px

**Header Section:**
- Display: flex
- Align-items: center
- Gap: 12px
- Margin-bottom: 8px

**Checkbox:**
- Width: 20px
- Height: 20px
- Cursor: pointer
- Margin: 0
- Flex-shrink: 0
- **Positioned in header, horizontally with title**

**Title (Strong tag):**
- Color: sage green (#809364)
- Font: 14px, weight 700
- **On same line as checkbox**

**Body/Description Text (Paragraph):**
- Font: 13px, weight 400
- Color: medium gray (#4a4a4a)
- Line-height: 1.6
- Margin: 0
- Padding-left: 0
- **CRITICAL:** Text aligns with LEFT EDGE of checkbox, not indented

## Button Standards

**Actions Section Spacing:**
- Margin-top: 30px (matches general left/right padding)

**All Buttons:**
- Padding: 12px 24px
- Border: 1px solid #b3bf8f (green)
- Background: white
- Border-radius: 4px
- Font: 14px Montserrat, weight 600
- Cursor: pointer
- Transition: all 0.2s

**Button Hover:**
- Background: #f5f5f5
- Border-color: #b3bf8f (stays green)

**Primary Button (Save Your Audit):**
- Background: #b3bf8f
- Color: white
- Border-color: #b3bf8f

**Primary Button Hover:**
- Background: #9faa7a
- Border-color: #9faa7a

**Button Container:**
- Padding: 20px 30px
- Background: #f9f9f7
- Display: flex
- Gap: 12px
- Justify-content: center

## Footer Standards

**Footer Content:**
- Padding: 20px
- Background: white
- Text-align: center
- Display: flex
- Flex-direction: column
- Gap: 15px
- Align-items: center

**Footer Graphic:**
- Height: 30px
- Width: auto
- File: form-footer-graphic.png

**Copyright Text:**
- Font: 10px
- Color: #666
- Line-height: 1.5
- Max-width: 800px
- **Line break after "reserved."**

## Page Structure

**Container (.page):**
- Max-width: 1200px
- Margin: 0 auto
- Background: white
- Box-shadow: 0 0 20px rgba(0,0,0,0.1)

**Content (.content):**
- Padding: 30px

## Responsive Design

**Mobile Breakpoint (max-width: 768px):**
- Quadrants: Stack vertically (grid-template-columns: 1fr)
- Verdict options: Stack vertically (grid-template-columns: 1fr)
- Header adjustments as needed
- Maintain all spacing and color standards

## Required Assets

All forms require these image files in the same directory:
1. `form-top-logo.png` - Muvist Academy logo (header)
2. `form-footer-graphic.png` - Footer graphic
3. `form-arrow-icon.png` - **THE UNIVERSAL ICON for all clipart/icon substitution**

**CRITICAL ICON RULE:** 
- **ALWAYS use `form-arrow-icon.png` to replace ANY clipart, emoji, or icon elements**
- This includes: section header icons, info box icons, callouts, decorative graphics
- **NOT for bullet points** - use standard text bullets for lists
- Never use emoji (📋, 📌, 🎯, etc.) or Unicode symbols - replace with form-arrow-icon.png
- Size varies by usage: 48px for main title, 44px for section headers, 26px for info boxes

## Interactive Features

**Auto-save to localStorage:**
- Save on blur events
- Restore on page load
- Key format: `muvist-form-[form-name]-[field-name]`

**Signal Strength Auto-calculation:**
- Validate input: 1-5 range
- Calculate total automatically
- Display total out of 25

**Toast Notifications:**
- Position: fixed, bottom 30px, right 30px
- Background: #1a1a1a
- Color: white
- Padding: 15px 20px
- Border-radius: 4px
- Font: 14px

**Download/Print Functions:**
- PDF download via html2pdf.js library from CDN
- Print functionality with standard window.print()

## Critical Spacing & Alignment Rules

1. **UNIVERSAL ICON SUBSTITUTION:** Always use form-arrow-icon.png to replace emoji/clipart (NOT for bullet points - use standard text bullets)
2. **UNIVERSAL 30px TOTAL SPACING:** All spacing between components = 30px total (achieved by 15px top + 15px bottom). Left/right page padding = 30px.
3. **Section Headers:** Spacing above and below must be equal (15px + 15px = 30px total)
4. **Label-Description-Input Grids:** Zero visible gap between strong tag headers and description text
5. **Label-Description-Input Grids:** Input fields align at baseline with description text
6. **Summary/Total Rows:** No margin-top, sits directly against border-top
7. **Checkbox Grid Body Text:** Aligns with left edge of checkbox (no additional padding)
8. **Tagline:** Right-aligned at right: 240px with 15px gap from logo
9. **Line Spacing:** Use negative margins (-2px) where needed to achieve tight spacing within components

## HTML Structure Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[Form Title] - Muvist Academy</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* Apply all standards from this skill */
    </style>
</head>
<body>
    <div class="page">
        <!-- Header -->
        <div class="header">
            <div class="module-badge">[Module Number]</div>
            <div class="header-tagline">Movement Marketing; Extend Reach, Reduce Cost.</div>
            <div class="logo">
                <img src="form-top-logo.png" alt="Muvist Academy">
            </div>
            <div class="title-section">
                <h1><img src="form-arrow-icon.png" alt="" class="header-icon">[Form Title]</h1>
                <p class="subtitle">[Subtitle]</p>
            </div>
        </div>

        <!-- Content sections as needed -->
        
        <!-- Actions -->
        <div class="actions">
            <button type="button" onclick="clearForm()">Clear Form</button>
            <button type="button" class="primary" onclick="saveAudit()">Save Your [Form Type]</button>
            <button type="button" onclick="downloadPDF()">Download PDF</button>
            <button type="button" onclick="window.print()">Print</button>
        </div>

        <!-- Footer -->
        <div class="footer">
            <div class="footer-content">
                <img src="form-footer-graphic.png" alt="" class="footer-graphic">
            </div>
            <div class="footer-copyright">
                © [Year] Muvist Academy. All rights reserved.<br>
                [Additional copyright text]
            </div>
        </div>
    </div>
</body>
</html>
```

## Quality Checklist

Before delivering any Muvist form, verify:
- [ ] Montserrat font loaded from Google Fonts
- [ ] All colors match brand palette
- [ ] Module badge positioned at left: 30px, top: 30px
- [ ] Tagline positioned at top: 51px, centered, aligned with "M" baseline
- [ ] Logo positioned at right: 30px, top: 30px, height: 40px
- [ ] Section icons: 44px for sections, 48px for main title, 26px for info boxes
- [ ] If using Label-Description-Input Grid: zero gap between labels and descriptions
- [ ] If using Label-Description-Input Grid: inputs align at baseline with descriptions
- [ ] If using Label-Description-Input Grid: no border under second-to-last row if summary row exists
- [ ] If using Label-Description-Input Grid: summary/total row has no margin-top
- [ ] If using Checkbox Selection Grid: checkboxes visible and on same line as titles
- [ ] If using Checkbox Selection Grid: body text aligns with left edge of checkbox
- [ ] All buttons have green borders (#b3bf8f)
- [ ] All button hovers maintain green borders
- [ ] Footer includes line break after "reserved."
- [ ] All three image files referenced correctly
- [ ] Auto-save functionality implemented (if applicable)
- [ ] Responsive design for mobile
- [ ] PDF download and print functions working (if applicable)

## Common Mistakes to Avoid

1. **DO NOT** use inline styles for label-description gaps - use margin-bottom: -2px on strong tags
2. **DO NOT** add padding-left to checkbox grid body text - it aligns with checkbox edge
3. **DO NOT** position tagline by guessing - use exact top: 51px
4. **DO NOT** use different greens - stick to #b3bf8f for buttons and #809364 for text/headers
5. **DO NOT** add margin-top to summary/total rows - it should be 0
6. **DO NOT** use border-bottom on the row before a summary row - remove with nth-last-child(2)
7. **DO NOT** make checkbox and title stack vertically - keep horizontal in flex layout
8. **DO NOT** change button border colors on hover - keep green (#b3bf8f)

## Notes

This design system was established through iterative refinement and represents the precise specifications for Muvist Academy forms. Every measurement, color, and spacing value has been carefully calibrated for visual consistency and brand alignment. Adherence to these standards ensures professional, cohesive forms across all Muvist Academy materials.

---

## Footer Lock

**REQUIRED FOOTER TEXT FOR ALL WORKSHEETS:**

MUVIST Academy · Quick Check Worksheet · Lesson (enter the applicable lesson number) Module (enter the applicable Module number) · © 2026 MUVIST Ltd. All rights reserved. Reproduction for internal organisational use only.

**Implementation:**
- This footer must appear at the bottom of every Quick Check Worksheet
- Replace "(enter the applicable lesson number)" with the actual lesson number
- Replace "(enter the applicable Module number)" with the actual module number
- Font: 10px Montserrat
- Color: #666
- Text-align: center
- Line-height: 1.5
- Position below the standard footer graphic and copyright text
