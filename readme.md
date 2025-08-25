# Natours

**Natours** is a modern, responsive landing page for a fictional nature tour company, built using advanced CSS techniques. It features smooth animations, a background video, interactive cards, a dynamic form, and a fixed navigation bar, all designed to teach cutting-edge CSS - SASS.

---

### What I learned

1. `clip-path`: Property creates a clipping region that sets what part of an element should be shown. Parts that are inside the region are shown, while those outside are hidden.

---

### How CSS Works A Look Behind the Scenes

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
