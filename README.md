<div align="center">

# Zeenat Ansari — Portfolio

**A cinematic, editorial personal portfolio built with HTML, CSS, GSAP & Lenis.**

No framework. No build step. Just open it and it runs.

//ching

</div>

---

## About

This is the personal portfolio of **Zeenat Ansari**, a third-year BCA student at Mumbai University aspiring to become an AI Engineer. The site is designed as a full-bleed cinematic experience — inspired by luxury editorial campaigns and premium product pages — rather than a conventional developer portfolio template.

**Sections:** Hero · About · Currently Working On · Education · Skills · Projects · Academic Performance · GitHub · Experience · Achievements · Contact

---

## Tech Stack

| Layer | Tool |
|---|---|
| Markup & styling | HTML5, CSS3 (custom properties, no framework) |
| Typography | Bebas Neue, Space Grotesk, Inter — via Google Fonts |
| Scroll-triggered animation | [GSAP](https://gsap.com/) + ScrollTrigger |
| Smooth scrolling | [Lenis](https://lenis.darkroom.engineering/) |

All dependencies load via CDN — no `npm install`, no bundler, no build step.

---

## Folder Structure

```
zeenat-portfolio/
├── index.html            # entire site — markup, styles, and scripts
├── assets/
│   └── zeenat-hero.png    # hero portrait
└── README.md
```

> `index.html` and `assets/` must stay together in the same directory — the hero image path is relative.

---

## Configuration

Everything below lives inside `index.html`. Search for the relevant text to find each block.

**Colors & type** — all design tokens are CSS variables at the top of the `<style>` block:
```css
:root{
  --bg:#090909;         /* background */
  --accent:#C1121F;      /* crimson accent */
  --text:#F5F3F0;        /* primary text */
  --text-dim:#8c8c8c;    /* secondary text */
}
```

**Hero photo** — replace `assets/zeenat-hero.png` (keep the filename, or update the `<img src="...">` in the hero section).

**Resume download** — link a PDF by adding it to `assets/` and updating the resume button script near the bottom of the file:
```js
['resumeBtnNav','resumeBtnHero','resumeBtnContact'].forEach(id=>{
  const el = document.getElementById(id);
  if(el) el.setAttribute('href', 'assets/resume.pdf');
  if(el) el.setAttribute('download', '');
});
```

**Contact links** — update the email/GitHub/LinkedIn/Instagram links inside `<section id="contact">`.

**Contact form submission** — the form currently confirms locally with no backend. Point its `action` at a service like [Formspree](https://formspree.io/) or [Web3Forms](https://web3forms.com/) to receive real submissions.

**GitHub / LeetCode stats** — the GitHub section uses static placeholder numbers. Swap in [GitHub Readme Stats](https://github.com/anuraghazra/github-readme-stats) or call the GitHub API directly for live data.

**Projects & achievements** — each project card is a `<article class="project">` block; each achievement is a `.t-item` block. Duplicate one and edit the content to add more.

---

## Accessibility & Performance

- Honors `prefers-reduced-motion` — animation is disabled for users who request it
- Semantic HTML throughout (`header`, `nav`, `section`, `article`, `footer`)
- Visible focus states on all interactive elements
- Fully responsive — desktop, tablet, and mobile layouts

---

## License

This project is personal work by Zeenat Ansari. Feel free to reference the structure for your own portfolio, but please don't reuse the content or imagery as-is.

---

<div align="center">

© 2026 Zeenat Ansari · Designed & Developed by Zeenat Ansari

</div>
