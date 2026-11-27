# My Assessment Tracker — Plan

## Overview

Build a single-file HTML/CSS/JS dashboard page titled **"My Assessment Tracker"**.
The page uses a dark header bar, bold colorful summary cards, an assessment status card,
and an interactive preparation checklist — all with sample data, no framework, no build step.

**Output file:** `assessment-tracker.html` (workspace root `c:\Users\laila\`)
**Stack:** Plain HTML5 + CSS + vanilla JavaScript (single file)
**Style:** Bold and colorful — vibrant accent colors per card, dark header bar

---

## Sub-Tasks

---

### Sub-Task 1 — Page Shell
**Status:** [x] done

**Intent:**
Set up the single HTML file with the dark header bar and a CSS grid that the cards
and checklist will slot into.

**Expected Outcomes:**
- `assessment-tracker.html` exists and opens in a browser
- A dark top bar renders with the title "My Assessment Tracker" in white
- An empty content area below is ready to receive cards and the checklist
- Google Font (Poppins) is loaded via `<link>`

**Todo:**
1. Create `assessment-tracker.html` with standard HTML5 boilerplate
2. Add a `<header>` with dark background (#1a1a2e) and white title text
3. Define a CSS grid/flex layout for the main content area
4. Link Poppins font from Google Fonts

**Relevant Context:** None — greenfield file.

---

### Sub-Task 2 — Summary Cards: Students Registered & Tasks Remaining
**Status:** [x] done

**Intent:**
Add two of the three summary cards, each with a distinct vibrant accent color,
an emoji icon, a large sample number, and a descriptive label.

**Expected Outcomes:**
- "Students Registered" card — blue left-border accent, value `32`
- "Tasks Remaining" card — orange left-border accent, value `7`
- Cards sit side-by-side in a flex row with shadow and hover lift

**Todo:**
1. Create a `.cards-row` flex container inside `<main>`
2. Build a reusable `.card` CSS class (shadow, bold left-border accent, hover lift)
3. Add "Students Registered" card — blue accent (#3a86ff), sample value `32`, icon 🎓
4. Add "Tasks Remaining" card — orange accent (#fb5607), sample value `7`, icon 📝

**Relevant Context:** Sub-Task 1 must be complete (`.cards-row` goes inside `<main>`).

---

### Sub-Task 3 — Assessment Status Card
**Status:** [x] done

**Intent:**
Add the third summary card showing the current assessment phase with a colored
status badge, giving the teacher an instant read on where the class is in the cycle.

**Expected Outcomes:**
- "Assessment Status" card — purple accent (#8338ec)
- Displays a green pill badge labeled "In Progress"
- Sub-label reads "Grading Phase — Week 3"
- Card slots naturally into the existing `.cards-row`

**Todo:**
1. Add the "Assessment Status" card to `.cards-row` — purple accent, icon 📊
2. Style a `.badge` element as a rounded pill (green background, white text)
3. Set badge text to "In Progress" and sub-label to "Grading Phase — Week 3"

**Relevant Context:** Sub-Task 2 must be complete (card joins the same row).

---

### Sub-Task 4 — Preparation Checklist
**Status:** [x] done

**Intent:**
Add an interactive checklist below the cards so the teacher can tick off each
preparation step as it is completed.

**Expected Outcomes:**
- A titled section "Preparation Checklist" appears below the cards
- 8 sample items are listed as checkbox labels
- Ticking an item crosses out its text and mutes its color (via JS)
- A progress counter updates live (e.g. "3 / 8 complete")

**Todo:**
1. Add `<section class="checklist">` below `.cards-row` in `<main>`
2. Render 8 items as `<label><input type="checkbox"> text</label>`:
   - Publish assignment brief
   - Communicate submission deadline
   - Distribute grading rubric
   - Collect all submissions
   - Run plagiarism / integrity check
   - Grade all submissions
   - Write individual feedback
   - Release grades to students
3. Write JS: on checkbox change, toggle `.item-done` class (line-through + muted color)
4. Add a live `<span>` counter that shows "X / 8 complete"

**Relevant Context:** Sub-Task 1 must be complete (`<main>` container exists).

---

### Sub-Task 5 — Sample Data & Visual Polish
**Status:** [x] done

**Intent:**
Confirm all sample data looks realistic and do a final pass on spacing, color
contrast, and mobile responsiveness so the page looks complete and polished.

**Expected Outcomes:**
- All card values and labels are consistent and realistic
- Cards stack vertically on screens narrower than 600px (`@media` query)
- Hover animation (translateY + shadow deepens) works on all cards
- Font sizes, padding, and color contrast pass a visual review

**Todo:**
1. Verify sample data: 32 students, 7 tasks, "Grading Phase — Week 3 / In Progress"
2. Add `@media (max-width: 600px)` rule so `.cards-row` switches to `flex-direction: column`
3. Add CSS hover transition (`transform: translateY(-4px)`, deeper box-shadow)
4. Final review: font sizes, line heights, padding, color contrast across all sections

**Relevant Context:** All previous sub-tasks must be complete.
