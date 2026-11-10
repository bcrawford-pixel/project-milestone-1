# project-milestone-3
# Portfolio Website — Milestone 3: Accessible & Designed

## 1. Accessibility Fixes (WAVE & Contrast)

* **Home Page (`index.html`)**: Added missing `alt` attributes to all portfolio imagery and main profile photos so screen readers properly convey visual context.
* **Projects Page (`projects.html`)**: Fixed form control accessibility by linking explicit `<label>` elements to search and category filter inputs using matching `for` and `id` attributes.
* **About/Contact Page (`about.html`)**: Corrected heading hierarchy by ensuring all sections follow a sequential `<h1>` $\rightarrow$ `<h2>` $\rightarrow$ `<h3>` order without skipping levels.
* **Contrast Compliance (All Pages)**: Replaced low-contrast secondary text (`#767676`) with high-contrast text (`#595959` / `--text-muted`) to ensure all text and background color combinations exceed the WCAG AA minimum contrast ratio of 4.5:1 (verified with WebAIM Contrast Checker).

---

## 2. Visual Design & Gestalt Principles

* **Common Region**: Applied the Common Region principle by enclosing discrete content sections (such as project items, profile cards, and the contact form) inside defined white container cards (`.content-card`, `.form-card`) with unified background colors (`var(--card-bg)`), subtle borders (`var(--border-color)`), and consistent border radii (`var(--border-radius)`).
* **Proximity**: Applied the Proximity principle inside `.form-group` by setting a tight vertical gap (`6px`) between labels and their input fields to visually link them, while placing larger bottom margins (`20px`) between separate inputs to distinguish distinct fields.
* **Similarity**: Applied the Similarity principle by giving all primary call-to-action buttons (`.btn-primary`) and interactive navigation links consistent navy blue background colors (`var(--header-bg)`), font typography, and focus ring outlines across all three pages.
* **Consistent Color Palette**: Established a centralized design system in `styles.css` using CSS custom properties (`:root`). All three pages (`index.html`, `projects.html`, `about.html`) reference identical color variables for headers (`#2d4059`), gold accents (`#d39b62`), card backgrounds (`#ffffff`), and text colors (`#1f2933`).

---

## 3. Accessible Form Implementation

The contact form on `about.html` includes the following accessible features:
* Grouped form controls enclosed within a semantic `<fieldset>` and `<legend>`.
* Explicit `<label>` elements connected to every `<input>` and `<textarea>` using matching `for` and `id` attributes.
* `aria-required="true"` on mandatory input fields.
* An accessible error state utilizing `aria-invalid="true"` and `aria-describedby="email-error"`, backed by visual text and styling (`.form-error`) that does not rely solely on color to indicate invalid input.
