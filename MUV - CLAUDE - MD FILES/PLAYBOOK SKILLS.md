---
name: interactive-playbook-creation
description: Create professional, interactive HTML playbooks with consistent branding, responsive design, auto-save functionality, and structured learning sections. Supports case studies, worksheets, visual layouts, and downloadable formats.
version: 1.0
tags: [playbook, HTML, interactive, education, case-study, forms, responsive-design]
author: MUVIST Academy
created: 2026-03-30
---

# Interactive Playbook Creation Skill

## Overview

This skill guides the creation of professional, branded interactive HTML playbooks for educational content, case studies, training materials, and strategic frameworks. The output is a single-file HTML document with embedded CSS and JavaScript that includes auto-save functionality, responsive design, PDF export, and print capabilities.

## When to Use This Skill

Use this skill when you need to create:
- Educational playbooks or course companions
- Case study documents with interactive elements
- Training materials with worksheets and reflection sections
- Strategic frameworks with application exercises
- Marketing playbooks with campaign examples
- Any structured learning content that benefits from interactivity

## Core Architecture

### Single-File Structure

Create a complete, self-contained HTML file with:
- Embedded CSS in `<style>` tags
- Embedded JavaScript in `<script>` tags
- All functionality in one portable file
- External dependencies loaded via CDN only

### Required External Libraries

```html
<!-- Font -->
<link href="https://fonts.googleapis.com/css2?family=[BRAND_FONT]:wght@400;500;600;700&display=swap" rel="stylesheet">

<!-- PDF Export -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
```

## Brand Standards & Color System

### Typography

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: '[BRAND_FONT]', sans-serif;
    line-height: 1.6;
    color: #1a1a1a;
    background-color: #ffffff;
}

h1 { font-size: 32px; font-weight: 700; }
h2 { font-size: 24px; font-weight: 700; }
h3 { font-size: 18px; font-weight: 700; }
```

### Color Palette Structure

Define a consistent color system using hex codes with semantic naming:

```css
/* Primary Brand Colors */
--primary-color: #XXXXXX;          /* Main brand color */
--primary-dark: #XXXXXX;           /* Darker variant */
--primary-light: #XXXXXX;          /* Lighter variant */

/* Secondary Colors */
--secondary-color: #XXXXXX;        /* Accent color */
--success-color: #XXXXXX;          /* Green for positive */
--warning-color: #XXXXXX;          /* Orange for caution */
--danger-color: #XXXXXX;           /* Red for alerts */
--info-color: #XXXXXX;             /* Blue for information */

/* Neutral Colors */
--text-primary: #1a1a1a;           /* Main text */
--text-secondary: #888888;         /* Secondary text */
--background-light: #f9f9f7;       /* Light backgrounds */
--background-white: #ffffff;       /* White backgrounds */
--border-color: #d0d0d0;           /* Borders and dividers */
```

### Universal Spacing

Apply 30px spacing consistently throughout:

```css
.section {
    margin-bottom: 30px;
    padding: 30px;
}

.form-group {
    margin-bottom: 30px;
}
```

## Document Structure

### Header Component

```html
<header>
    <div class="header-content">
        <!-- Module Badge (if applicable) -->
        <div class="module-badge" style="position: absolute; left: 30px; top: 30px;">
            MODULE [NUMBER]
        </div>
        
        <!-- Tagline (if applicable) -->
        <div style="position: absolute; right: 240px; top: 51px;">
            [TAGLINE TEXT]
        </div>
        
        <!-- Brand Logo -->
        <img src="[LOGO_FILE]" alt="[BRAND NAME]" style="position: absolute; right: 30px; top: 30px; height: 40px;">
    </div>
</header>
```

### Title Section

```html
<div class="title-section">
    <img src="[SUBJECT_LOGO]" alt="[SUBJECT]" style="width: 280px; margin-bottom: 20px;">
    <h1>[PLAYBOOK TITLE]</h1>
    <p class="subtitle">[SUBTITLE OR DESCRIPTION]</p>
</div>
```

### Footer Component

```html
<footer>
    <div style="text-align: center; margin-bottom: 15px;">
        <img src="[FOOTER_GRAPHIC]" alt="" style="height: 40.5px;">
    </div>
    <p style="text-align: center; font-size: 11px; color: #888;">
        [BRAND NAME] | [TAGLINE] | [COPYRIGHT YEAR]
    </p>
    <p style="text-align: center; font-size: 10px; color: #888; margin-top: 5px;">
        © [YEAR] [COMPANY NAME]. All rights reserved. Proprietary course material.
    </p>
</footer>
```

## Content Section Patterns

### Pattern 1: Introduction with Logo + Text

```html
<div class="section">
    <div class="section-header">
        <img src="form-arrow-icon.png" alt="">
        <h2>[Section Title]</h2>
    </div>
    
    <div style="display: flex; align-items: flex-start; gap: 30px; margin: 30px 0;">
        <img src="[LOGO]" alt="[SUBJECT]" style="width: 280px; flex-shrink: 0;">
        <div>
            <p>[Content text...]</p>
        </div>
    </div>
</div>
```

### Pattern 2: Highlight Box (Belief Statements / Key Messages)

```html
<div class="highlight-box">
    <strong>[Label]:</strong> [Message text...]
</div>

<!-- CSS -->
<style>
.highlight-box {
    background: #f9f9f7;
    border-left: 4px solid [BRAND_COLOR];
    padding: 20px;
    margin: 20px 0;
    border-radius: 4px;
}
</style>
```

### Pattern 3: Comparison Table (Old vs New / Before vs After)

```html
<table class="comparison-table">
    <thead>
        <tr>
            <th>Old Approach</th>
            <th>New Approach</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>[Old way description]</td>
            <td>[New way description]</td>
        </tr>
    </tbody>
</table>

<!-- CSS -->
<style>
.comparison-table {
    width: 100%;
    border-collapse: collapse;
    margin: 30px 0;
}

.comparison-table th {
    background: [HEADER_COLOR];
    color: white;
    padding: 15px;
    text-align: left;
}

.comparison-table td {
    padding: 15px;
    border: 1px solid #e0e0e0;
}
</style>
```

### Pattern 4: Team/Roles Side-by-Side Blocks

```html
<div style="display: grid; grid-template-columns: repeat(5, 1fr); gap: 15px; margin: 30px 0;">
    <div style="background: #f9f9f7; padding: 20px; border-radius: 4px; border-top: 4px solid [COLOR]; text-align: center;">
        <p style="font-weight: 700; color: [COLOR]; margin-bottom: 10px; font-size: 13px;">[Role Title]</p>
        <p style="color: #1a1a1a; font-size: 13px;">[Role Description]</p>
    </div>
    <!-- Repeat for each role -->
</div>
```

### Pattern 5: Two-Column Comparison with Visual Separation

```html
<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 30px; margin: 30px 0;">
    <div style="background: #f9f9f7; padding: 25px; border-radius: 4px; border-top: 4px solid [COLOR_1];">
        <h3 style="color: [COLOR_1]; font-size: 20px; font-weight: 700; margin-bottom: 20px; text-align: center;">Column 1 Title</h3>
        <ul style="list-style: none; padding-left: 0; line-height: 2;">
            <li style="padding: 10px 0; border-bottom: 1px solid #e0e0e0;">• Item 1</li>
            <li style="padding: 10px 0;">• Item 2</li>
        </ul>
    </div>
    <div style="background: #f9f9f7; padding: 25px; border-radius: 4px; border-top: 4px solid [COLOR_2];">
        <!-- Column 2 content -->
    </div>
</div>
```

### Pattern 6: Image Gallery Grid

```html
<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 20px; margin: 30px 0;">
    <img src="[IMAGE_1]" alt="[DESCRIPTION]" style="width: 100%; height: auto; border-radius: 4px;">
    <img src="[IMAGE_2]" alt="[DESCRIPTION]" style="width: 100%; height: auto; border-radius: 4px;">
    <img src="[IMAGE_3]" alt="[DESCRIPTION]" style="width: 100%; height: auto; border-radius: 4px;">
    <img src="[IMAGE_4]" alt="[DESCRIPTION]" style="width: 100%; height: auto; border-radius: 4px;">
</div>
```

### Pattern 7: Results/Metrics Grid with Colored Cards

```html
<div class="results-grid">
    <div class="result-card" style="background: [COLOR_1];">
        <div class="result-number">[METRIC]</div>
        <div class="result-label">[Label]</div>
        <div class="result-description">[Description]</div>
    </div>
    <!-- Repeat for each metric -->
</div>

<!-- CSS -->
<style>
.results-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    margin: 30px 0;
}

.result-card {
    padding: 30px;
    border-radius: 4px;
    color: white;
    text-align: center;
}

.result-number {
    font-size: 48px;
    font-weight: 700;
    margin-bottom: 10px;
}

.result-label {
    font-size: 18px;
    font-weight: 600;
    margin-bottom: 10px;
}
</style>
```

### Pattern 8: Two-Tone Cards (3x2 Grid for Lessons/Principles)

```html
<div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; margin: 30px 0;">
    <div style="border: 1px solid #d0d0d0; border-radius: 4px; overflow: hidden;">
        <div style="background: [HEADER_COLOR]; padding: 20px; text-align: center;">
            <p style="font-weight: 700; color: #1a1a1a; font-size: 15px; margin: 0;">[Lesson Number & Title]</p>
        </div>
        <div style="background: white; padding: 20px; text-align: center;">
            <p style="color: #1a1a1a; margin: 0; line-height: 1.6;">[Lesson description]</p>
        </div>
    </div>
    <!-- Repeat for each lesson -->
</div>
```

### Pattern 9: Checklist with Colored Cards

```html
<div class="checklist-grid">
    <div class="checklist-card" style="background-color: [COLOR_1];">
        <input type="checkbox" id="check-1" class="card-checkbox">
        <label for="check-1">
            <div class="card-title">[Item Title]</div>
            <div class="card-description">[Item description]</div>
        </label>
    </div>
    <!-- Repeat for each checklist item -->
</div>

<!-- CSS -->
<style>
.checklist-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    margin: 30px 0;
}

.checklist-card {
    padding: 25px;
    border-radius: 4px;
    position: relative;
    color: white;
}

.card-checkbox {
    position: absolute;
    top: 15px;
    right: 15px;
    width: 24px;
    height: 24px;
    cursor: pointer;
}

.card-title {
    font-weight: 700;
    font-size: 16px;
    margin-bottom: 10px;
}
</style>
```

### Pattern 10: Testimonials/Reflections Side-by-Side

```html
<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 30px; margin: 30px 0;">
    <div style="background: #f9f9f7; padding: 40px 30px; border-radius: 4px; border-top: 4px solid [COLOR]; text-align: center;">
        <p style="font-size: 16px; line-height: 1.6; margin-bottom: 30px; color: #1a1a1a;">"[Quote text]"</p>
        <p style="font-weight: 700; color: #1a1a1a; margin-bottom: 5px;">[Name],</p>
        <p style="color: #1a1a1a;">[Title/Role]</p>
    </div>
    <!-- Second testimonial -->
</div>
```

### Pattern 11: Case Study with Image + Two Columns

```html
<div class="section">
    <div class="section-header">
        <img src="form-arrow-icon.png" alt="">
        <h2>[Case Study Title]</h2>
    </div>
    
    <img src="[CASE_IMAGE]" alt="[DESCRIPTION]" style="width: 100%; height: auto; border-radius: 4px; margin-bottom: 30px;">
    
    <div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 30px;">
        <div>
            <h3 style="color: [COLOR]; font-size: 18px; font-weight: 700; margin-bottom: 15px;">[Column 1 Title]</h3>
            <p>[Content...]</p>
        </div>
        <div>
            <div style="background: #f9f9f7; padding: 25px; border-radius: 4px; border-top: 4px solid [COLOR];">
                <h3 style="color: [COLOR]; font-size: 16px; font-weight: 700; margin-bottom: 15px;">[Column 2 Title]</h3>
                <p>[Content...]</p>
            </div>
        </div>
    </div>
</div>
```

### Pattern 12: FAQ Grid (2x2 with Light Backgrounds)

```html
<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 30px; margin: 30px 0;">
    <div style="background: #e8f4f8; padding: 30px; border-radius: 4px; border-top: 4px solid [DARK_COLOR]; text-align: center;">
        <p style="font-weight: 700; color: #1a1a1a; margin-bottom: 15px; font-size: 15px;">Q: [Question]</p>
        <div style="width: 120px; height: 1px; background: [DARK_COLOR]; margin: 0 auto 20px;"></div>
        <p style="color: #1a1a1a; line-height: 1.6; margin: 0;">A: [Answer]</p>
    </div>
    <!-- Repeat for each FAQ -->
</div>
```

### Pattern 13: Call-to-Action Box with Icon

```html
<div style="display: flex; align-items: center; gap: 20px; padding: 20px; background: #f9f9f7; border-radius: 4px; margin-top: 30px; margin-bottom: 5px;">
    <img src="[ICON_FILE]" alt="[DESCRIPTION]" style="width: 80px; height: 80px; flex-shrink: 0;">
    <div style="border-left: 2px solid #ccc; padding-left: 20px;">
        <h3 style="color: [COLOR]; font-size: 18px; font-weight: 700; margin-bottom: 10px;">[CTA Heading]</h3>
        <p style="color: #1a1a1a; line-height: 1.6; margin: 0;">[CTA description and links]</p>
    </div>
</div>
```

## Interactive Worksheet Components

### Form Group Structure

```html
<div class="form-group">
    <label>[Question or Prompt]</label>
    <div class="hint">[Helpful hint or explanation]</div>
    <textarea id="[UNIQUE_ID]" placeholder="[Placeholder text]"></textarea>
</div>

<!-- CSS -->
<style>
.form-group {
    margin-bottom: 30px;
}

.form-group label {
    display: block;
    font-weight: 600;
    margin-bottom: 8px;
    color: #1a1a1a;
}

.hint {
    font-size: 13px;
    color: #888;
    margin-bottom: 10px;
    font-style: italic;
}

.form-group textarea {
    width: 100%;
    min-height: 120px;
    padding: 15px;
    border: 1px solid #d0d0d0;
    border-radius: 4px;
    font-family: '[BRAND_FONT]', sans-serif;
    font-size: 14px;
    resize: vertical;
}
</style>
```

### Multi-Step Worksheet Pattern

```html
<div class="section">
    <div class="section-header">
        <img src="form-arrow-icon.png" alt="">
        <h2>[Worksheet Title]</h2>
    </div>
    
    <div class="info-box">
        <img src="form-arrow-icon.png" alt="">
        <div>
            <strong>[Instructions Title]:</strong> [Instructions text]
        </div>
    </div>
    
    <!-- Step 1 -->
    <div class="form-group">
        <label>Step 1: [Step Title]</label>
        <div class="hint">[Guidance for this step]</div>
        <textarea id="step-1" placeholder="[Example or prompt]"></textarea>
    </div>
    
    <!-- Repeat for each step -->
</div>
```

## Auto-Save Functionality

### localStorage Implementation

```javascript
// Auto-save all form fields on blur
document.addEventListener('DOMContentLoaded', function() {
    const formFields = document.querySelectorAll('textarea, input[type="text"]');
    
    formFields.forEach(field => {
        // Load saved data
        const savedValue = localStorage.getItem(field.id);
        if (savedValue) {
            field.value = savedValue;
        }
        
        // Save on blur
        field.addEventListener('blur', function() {
            localStorage.setItem(field.id, field.value);
            showToast('Progress saved');
        });
    });
    
    // Handle checkboxes
    const checkboxes = document.querySelectorAll('input[type="checkbox"]');
    checkboxes.forEach(checkbox => {
        const savedState = localStorage.getItem(checkbox.id);
        if (savedState === 'true') {
            checkbox.checked = true;
        }
        
        checkbox.addEventListener('change', function() {
            localStorage.setItem(checkbox.id, checkbox.checked);
        });
    });
});
```

### Toast Notification

```javascript
function showToast(message) {
    const toast = document.createElement('div');
    toast.className = 'toast';
    toast.textContent = message;
    document.body.appendChild(toast);
    
    setTimeout(() => toast.classList.add('show'), 10);
    setTimeout(() => {
        toast.classList.remove('show');
        setTimeout(() => toast.remove(), 300);
    }, 2000);
}

// CSS
<style>
.toast {
    position: fixed;
    bottom: 30px;
    right: 30px;
    background: #4CAF50;
    color: white;
    padding: 15px 25px;
    border-radius: 4px;
    opacity: 0;
    transition: opacity 0.3s;
    z-index: 1000;
}

.toast.show {
    opacity: 1;
}
</style>
```

## Action Buttons

### Button Group Structure

```html
<div class="actions">
    <button type="button" onclick="clearForm()">Clear Form</button>
    <button type="button" onclick="saveForm()">Save Progress</button>
    <button type="button" onclick="downloadPDF()">Download PDF</button>
    <button type="button" onclick="window.print()">Print</button>
</div>

<!-- CSS -->
<style>
.actions {
    display: flex;
    gap: 15px;
    justify-content: center;
    margin: 30px 0;
    flex-wrap: wrap;
}

.actions button {
    background: [BUTTON_COLOR];
    color: white;
    border: none;
    padding: 12px 30px;
    border-radius: 4px;
    font-size: 14px;
    font-weight: 600;
    cursor: pointer;
    transition: background 0.3s;
}

.actions button:hover {
    background: [BUTTON_HOVER_COLOR];
}
</style>
```

### Button Functions

```javascript
function clearForm() {
    if (confirm('Are you sure you want to clear all form data? This cannot be undone.')) {
        document.querySelectorAll('textarea, input[type="text"]').forEach(field => {
            field.value = '';
            localStorage.removeItem(field.id);
        });
        
        document.querySelectorAll('input[type="checkbox"]').forEach(checkbox => {
            checkbox.checked = false;
            localStorage.removeItem(checkbox.id);
        });
        
        showToast('Form cleared');
    }
}

function saveForm() {
    document.querySelectorAll('textarea, input[type="text"]').forEach(field => {
        localStorage.setItem(field.id, field.value);
    });
    
    document.querySelectorAll('input[type="checkbox"]').forEach(checkbox => {
        localStorage.setItem(checkbox.id, checkbox.checked);
    });
    
    showToast('Progress saved successfully');
}

function downloadPDF() {
    const element = document.getElementById('content');
    const buttons = document.querySelector('.actions');
    
    // Hide buttons for PDF
    buttons.style.display = 'none';
    
    const opt = {
        margin: 10,
        filename: '[PLAYBOOK_NAME].pdf',
        image: { type: 'jpeg', quality: 0.98 },
        html2canvas: { scale: 2 },
        jsPDF: { unit: 'mm', format: 'a4', orientation: 'portrait' }
    };
    
    html2pdf().set(opt).from(element).save().then(() => {
        buttons.style.display = 'flex';
        showToast('PDF downloaded');
    });
}
```

## Responsive Design

### Media Query Breakpoint

```css
@media (max-width: 768px) {
    /* Header adjustments */
    .module-badge {
        font-size: 14px;
        padding: 10px 20px 10px 15px;
    }
    
    .title-section h1 {
        font-size: 24px;
    }
    
    /* Grid stacking */
    .results-grid,
    .checklist-grid {
        grid-template-columns: 1fr;
    }
    
    /* All multi-column grids stack */
    .section div[style*="grid-template-columns: repeat(2, 1fr)"],
    .section div[style*="grid-template-columns: repeat(3, 1fr)"],
    .section div[style*="grid-template-columns: repeat(5, 1fr)"] {
        grid-template-columns: 1fr !important;
    }
    
    /* Flex columns stack */
    .section div[style*="display: flex"] {
        flex-direction: column !important;
    }
    
    /* Logo adjustments */
    .section div[style*="display: flex"] img[src*="logo"] {
        max-width: 100% !important;
        margin-bottom: 20px;
    }
    
    /* Button adjustments */
    .actions {
        flex-direction: column;
    }
    
    .actions button {
        width: 100%;
    }
}
```

## Print Styles

```css
@media print {
    /* Hide interactive elements */
    .actions,
    .toast,
    input[type="checkbox"]:not(:checked)::before {
        display: none !important;
    }
    
    /* Ensure content fits */
    .section {
        page-break-inside: avoid;
    }
    
    /* Adjust colors for print */
    body {
        background: white;
    }
    
    /* Show form values */
    textarea {
        border: 1px solid #ccc !important;
        min-height: auto !important;
    }
}
```

## Content Organization Best Practices

### Recommended Section Order

1. **Header** - Branding and navigation context
2. **Title Section** - Subject logo, main title, subtitle
3. **Introduction** - What it is, overview, context
4. **Case Study/Content Sections** - Main educational content organized logically:
   - Challenge/Problem
   - Approach/Shift
   - Team/Stakeholders
   - Tools/Resources
   - Examples/Evidence
   - Results/Impact
5. **Interactive Application**:
   - Framework/Engine explanation
   - Application worksheet (5-7 steps)
   - Reflection questions
6. **Learning Consolidation**:
   - Key lessons/principles
   - Checklist
7. **Additional Context**:
   - Risks/Ethics considerations
   - Testimonials/Reflections
   - Failure cases (what not to do)
8. **FAQ** - Common questions
9. **Call-to-Action** - Next steps, additional resources
10. **Action Buttons** - Save, download, print, clear
11. **Footer** - Copyright, attribution

### Visual Hierarchy Rules

- **Spacing**: Maintain consistent 30px spacing between major elements
- **Grouping**: Related content should be visually grouped with background colors or borders
- **Contrast**: Use colored borders/backgrounds to differentiate section types:
  - Green/sage: Positive, growth, lessons
  - Blue: Information, facts, FAQs
  - Orange: Caution, warnings, important notes
  - Red: Risks, failures, alerts
  - Neutral: General content, worksheets

### Typography Hierarchy

```
H1 (32px) - Main page title only
H2 (24px) - Major section headers
H3 (18px) - Subsection headers, column titles
Body (14-16px) - Main content
Small (11-13px) - Hints, footnotes, captions
```

## Image Handling

### Image Sizing Guidelines

- **Logos**: 40-80px height, maintain aspect ratio
- **Subject logos**: 280px width (reduce to 100% on mobile)
- **Header graphics**: Specified height (e.g., 40.5px)
- **Content images**: 100% width, auto height, maintain aspect ratio
- **Icons**: 60-80px square

### Image Placement

```html
<!-- Full-width image -->
<img src="[IMAGE]" alt="[DESCRIPTION]" style="width: 100%; height: auto; border-radius: 4px; margin-bottom: 30px;">

<!-- Sized image with scaling -->
<img src="[IMAGE]" alt="[DESCRIPTION]" style="width: 130%; margin-left: -15%; height: auto; display: block;">

<!-- Grid of images -->
<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 20px;">
    <img src="[IMAGE_1]" style="width: 100%; height: auto; border-radius: 4px;">
    <img src="[IMAGE_2]" style="width: 100%; height: auto; border-radius: 4px;">
</div>
```

## Advanced Patterns

### Expandable Sections (Optional)

```javascript
function toggleSection(id) {
    const section = document.getElementById(id);
    section.classList.toggle('collapsed');
}

// CSS
<style>
.collapsible-section {
    max-height: 1000px;
    overflow: hidden;
    transition: max-height 0.3s ease;
}

.collapsible-section.collapsed {
    max-height: 0;
}
</style>
```

### Progress Tracking

```javascript
function calculateProgress() {
    const fields = document.querySelectorAll('textarea, input[type="text"]');
    let completed = 0;
    
    fields.forEach(field => {
        if (field.value.trim().length > 0) {
            completed++;
        }
    });
    
    return Math.round((completed / fields.length) * 100);
}

// Display in header or footer
function updateProgress() {
    const progress = calculateProgress();
    document.getElementById('progress').textContent = `Progress: ${progress}%`;
}
```

## Testing Checklist

Before delivering the playbook, verify:

- [ ] All sections render correctly on desktop
- [ ] All sections stack properly on mobile (< 768px)
- [ ] All form fields auto-save on blur
- [ ] Clear form function works with confirmation
- [ ] Save progress button provides feedback
- [ ] PDF download generates correctly
- [ ] Print layout is clean (no interactive elements)
- [ ] All images load and display at correct sizes
- [ ] Color contrast meets accessibility standards (4.5:1 minimum)
- [ ] All interactive elements have hover states
- [ ] Toast notifications appear and disappear correctly
- [ ] Footer text is accurate and complete
- [ ] All brand colors match specifications
- [ ] Typography is consistent throughout
- [ ] Spacing is uniform (30px standard)

## Common Customizations

### Changing Grid Layouts

To change from 3-column to 2-column:
```css
/* Change this */
grid-template-columns: repeat(3, 1fr);

/* To this */
grid-template-columns: repeat(2, 1fr);
```

### Adding New Form Fields

```html
<div class="form-group">
    <label>[New Field Label]</label>
    <div class="hint">[Optional hint]</div>
    <textarea id="new-field-[NUMBER]" placeholder="[Placeholder]"></textarea>
</div>
```

Fields with unique IDs will automatically be included in auto-save.

### Custom Color Themes

Replace the color variables at the top of the CSS block with your brand colors, then use those variable names throughout the document for consistency.

## File Naming Convention

```
[client-name]-[subject]-playbook.html
Examples:
- acme-marketing-playbook.html
- techcorp-onboarding-playbook.html
- nonprofit-fundraising-playbook.html
```

## Delivery Format

Provide to client:
1. **HTML file** - Complete, self-contained playbook
2. **Asset folder** - All images used (logos, graphics, photos)
3. **README** - Brief instructions on:
   - How to open the file (double-click or drag to browser)
   - How to use auto-save feature
   - How to download PDF
   - How to print
   - Browser compatibility (Chrome, Firefox, Safari, Edge)

## Browser Compatibility

Tested and working on:
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

Requires JavaScript enabled for interactive features.

---

## Quick Start Template

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[PLAYBOOK TITLE]</title>
    <link href="https://fonts.googleapis.com/css2?family=[FONT]:wght@400;500;600;700&display=swap" rel="stylesheet">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
    
    <style>
        /* Copy core CSS here */
    </style>
</head>
<body>
    <div id="content">
        <header>
            <!-- Header content -->
        </header>
        
        <div class="container">
            <div class="title-section">
                <!-- Title content -->
            </div>
            
            <!-- Add sections here -->
        </div>
        
        <footer>
            <!-- Footer content -->
        </footer>
    </div>
    
    <div class="actions">
        <!-- Action buttons -->
    </div>
    
    <script>
        /* Copy JavaScript here */
    </script>
</body>
</html>
```

---

**End of Skill Document**

For questions or improvements to this skill, contact the skill maintainer or submit updates via the skills repository.
