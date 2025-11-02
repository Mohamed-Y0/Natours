# Natours ( UNDERDEVELOPMENT )

**Natours** is a modern, responsive landing page for a fictional nature tour company, built using advanced CSS techniques. It features smooth animations, a background video, interactive cards, a dynamic form, and a fixed navigation bar, all designed to teach cutting-edge CSS - SASS.

---

### What I learned

1. `clip-path`: Property creates a clipping region that sets what part of an element should be shown. Parts that are inside the region are shown, while those outside are hidden.

2. `$color-primary: #333` To Define Color Variable in SCSS, To use it `color: $primary-color;`

3. `lighten()` and `darken()`: Sass provides built-in functions, to adjust the lightness of a color. These functions are particularly useful for creating color variations, such as hover states or different shades within a color palette.

---

## Theory Lectures

### #1 - How CSS Works A Look Behind the Scenes.

**1. CSS Behind the Scenes (Overview)**

Load & Parse HTML:

- Browser reads the HTML and builds the **DOM (Document Object Model)**.

Load & Parse CSS _(happens while parsing HTML)_:

- CSS is processed in two steps:
  1.  **Resolve conflicting CSS declarations** → apply the _cascade_.
  2.  **Process final CSS values** → compute actual styles.
- The result is the **CSSOM (CSS Object Model)**.

Combine DOM + CSSOM:

- Together they form the **Render Tree**.

Layout & Visual Formatting Model:

- Browser calculates **where elements go and how big they are**.

Painting & Rendering:

- Final **rendered website** is drawn on the screen.

---

### #2 - Introduction to Sass & NPM.

**1. What Is Sass**

Sass: CSS preprocessor that extends CSS by adding features like variables, nesting, and mixins, which make web styling more efficient and manageable

- SASS Source Code ---Sass Compiler---> Compiled CSS Code

Main Features:

- Variables: for reusable values such as colors, font-sizes, spacing, etc.

- Nesting: to nest selectors inside of one another, allowing us to write less code.

- Operators: for mathematical operations right inside of CSS.

- Partials and imports: to write CSS in different files and importing them all into one single file.

- Mixins: to write reusable pieces of CSS code.

- Functions: similar to mixins, with the difference that they produce a value that can than be used.

- Extends: to make different selectors inherit declarations that are common to all of them.

- Control directives: for writing complex code using conditionals and loops (not covered in this course).

Syntax:

- SASS Syntax

```sass
.nav
  list-style: none
  display: flex

  & li
    font-size: 18px
    margin-left: 30px
```

- SCSS Syntax

```scss
.nav {
  list-style: none;
  display: flex;

  & li {
    font-size: 18px;
    margin-left: 30px;
  }
}
```

---

### Advanced CSS & SASS.

---

### What I learned

**This lecture explains how to organize Sass files into a scalable, professional folder structure used in real-world projects.**
The focus is on maintainability, clean structure, and importing partial Sass files into one main file.

1. **SASS Architecture Goal:**
   Organize all Sass code into multiple folders and partial files, then import them into a single main Sass file for maintainability.

2. **Partial Files (`_file.scss`):**
   Files that start with `_` are _partials_ — they are not compiled into CSS alone, but imported into a main file.

3. **Main Entry File (`main.scss`):**
   The only Sass file compiled to CSS — used to import all partials.

4. **Folder Structure Concept:**
   Sass files should be grouped into folders such as:

   - `base/` (resets, typography, global styles)
   - `layout/` (header, footer, grid, navigation)
   - `components/` (buttons, cards, forms)
   - `abstracts/` (variables, mixins, functions)
   - `pages/` (page-specific styles)
   - `themes/` (optional for color themes)
   - `vendors/` (external libraries)

5. **Imports:**
   Use `@import` (or modern `@use` / `@forward`) to load partials into the main file.

6. **Maintainability is Key:**
   Folder structure ensures scalability, readability, and easy collaboration for professional CSS/Sass development.

---

## Theory Lectures

### #1 - Why We Use SASS Architecture

**1. Goal of Architecture**

- Keep code **organized, clean, and scalable**
- Avoid one giant stylesheet
- Make maintenance easier as project grows
- Follow professional standards used in real projects

---

### #2 - Folder Structure & Partial Setup

**Step-by-Step Concept**

- Create a main `sass` folder
- Inside it, create structure such as:

```
sass/
 ├─ abstracts/
 │   ├─ _variables.scss
 │   ├─ _mixins.scss
 │   └─ _functions.scss
 ├─ base/
 │   ├─ _base.scss
 │   ├─ _reset.scss
 │   └─ _typography.scss
 ├─ layout/
 │   ├─ _header.scss
 │   ├─ _footer.scss
 │   └─ _grid.scss
 ├─ components/
 ├─ pages/
 └─ main.scss
```

- Each file handles a **specific responsibility**
- Every folder contains partial files (`_file.scss`)
- Import all partials into `main.scss`

---

### #3 - Imports

- Use imports to bring everything together
- Example:

```scss
@use "abstracts/variables";
@use "abstracts/mixins";
@use "base/base";
@use "layout/header";
@use "components/buttons";
```

---

### Advanced CSS & SASS.

The lecture emphasizes that structuring Sass properly is essential for **professional-level CSS development** and working in teams/projects.

---
