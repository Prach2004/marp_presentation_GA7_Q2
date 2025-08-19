---
marp: true
theme: product-docs
paginate: true
footer: "Page $current / $total"
math: katex
style: |
  /* Deck-level tweaks via Marp directives */
  .callout {
    border-left: 6px solid #0f766e;
    padding: .6rem 1rem;
    background: #f8fafc;
  }
---

<!-- _class: lead -->
# Product Documentation with Marp
### Maintainable • Version-controlled • Multi-format

*Contact:* 24f1001831@ds.study.iitm.ac.in

---

# Why Marp for Product Docs?
- *Single source of truth* (Markdown) → PDF/PPTX/HTML
- *Git-friendly:* diffs, reviews, PRs
- *Theming & branding:* custom CSS themes
- *Automation-ready:* CI exports on release

> Tip: Keep screenshots/diagrams in /assets and reference them relatively.

---

<!-- _color: white -->
![bg](assets/bg.jpg)

# Architecture Overview (Background)
- High-level services & interfaces
- Environments (dev/stage/prod)
- Deployment topology & dependencies

Use the background slide for big-picture illustrations.

---

# Custom Theme + Directives
- Using custom theme: **product-docs**
- Page numbers via paginate: true and footer
- Inline brand accent: <span class="brand">highlighted text</span>
- Local slide tweaks via style: in front matter or _class

<div class="callout">
This box uses a custom <code>.callout</code> style defined in the <code>style</code> directive.
</div>

---

# Algorithmic Complexity (Math)
- Sorting: $T(n) = O(n \log n)$  
- Hash lookup: $O(1)$ average, $O(n)$ worst  
- Combined pipeline:
$$
T(n) = O(n \log n + m)
$$

---

# CLI (Build & Export)
```bash
# Live preview (serves slides at http://localhost:8080)
marp --theme-set theme.css slides.md --server

# Export to PDF and PPTX
marp --theme-set theme.css slides.md -o slides.pdf
marp --theme-set theme.css slides.md -o slides.pptx

# Export to HTML
marp --theme-set theme.css slides.md -o index.html
