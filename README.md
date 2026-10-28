<div align="center">

<a href="https://galasulin.github.io/apos4-pods-landing/"><img src="docs/apos4-pods.gif" alt="APOS4 pods come apart and snap back as you scroll" width="100%"></a>

# APOS4 · pods landing page

### A product page where the APOS4 system takes itself apart and puts itself back together as you scroll, built from four real pod cut-outs and live CSS transforms.

![HTML](https://img.shields.io/badge/HTML5-single_file-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-sticky_%2B_transforms-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JS](https://img.shields.io/badge/Vanilla_JS-rAF_scroll-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![RTL](https://img.shields.io/badge/UI-Hebrew_RTL-2F8F5B?style=flat-square)
![Status](https://img.shields.io/badge/Status-portfolio_copy-555555?style=flat-square)

**[✨ Live page →](https://galasulin.github.io/apos4-pods-landing/)** · 🇮🇱 [גרסה עברית](README.he.md)

</div>

> **Portfolio copy.** A sanitized, static copy of a landing page I designed and built for the clinic network. Tracking was never added to this version; the lead form only shows a demo message, phone and WhatsApp numbers are replaced with a non-dialable `*0000`, links to the company site are disabled, and patient names in the testimonials are reduced to initials.

---

## What is special

The heart of the page is a pinned `#stage` section (`position: sticky`, 460vh tall). A `requestAnimationFrame` loop reads how far you have scrolled through it and moves four separate "pods" over the sole:

| Scroll progress | What you see |
|---|---|
| 0.00 – 0.14 | The system fully assembled |
| 0.14 – 0.42 | The pods detach and float away |
| 0.42 – 0.58 | Fully apart: the rails and the calibration matrix are visible |
| 0.58 – 0.86 | The pods return to a personal position |
| 0.86 – 1.00 | Locked |

That is the whole marketing idea in one motion: **every system is calibrated for one person.**

- The four pods were cut from the original product photo along an ellipse with feathered edges, so putting them back on the sole reproduces the original photo exactly.
- A `PODS` array holds each pod's `out` distance, `home` offset and rotation; a `K` factor shrinks the spread on mobile.
- Six configuration images (neutral, medial, lateral, anterior, back) are normalised to the same content height so switching between them is stable.
- `prefers-reduced-motion` turns the animation off.

This is the earlier, transform-based version of the idea. The later frame-sequence version is [apos4-scroll-landing](https://github.com/galasulin/apos4-scroll-landing).

## Screenshots

| Desktop | Pods apart | Mobile |
|---|---|---|
| ![hero](docs/desktop-hero.png) | ![apart](docs/stage-apart.png) | ![mobile](docs/mobile-stage.png) |

## Stack

HTML5, CSS (sticky positioning, transforms, custom properties), vanilla JavaScript (`requestAnimationFrame`), WebP assets processed with Python/Pillow, Google Fonts (Heebo, Frank Ruhl Libre). No framework, no build step.

## My role

I designed and built the page end to end: the concept of showing calibration as a take-apart animation, cutting and normalising the product images, the layout, the scroll engine and the RTL copy layout.

## Status

A working version made for the APOS4 launch. This repository is the sanitized portfolio copy.

---

<div align="center">

**Built by [Gal Asulin](https://github.com/galasulin), IT Manager**

<sub>AposTherapy and APOS names, logos and product photos belong to their owner and are shown for portfolio purposes. See <a href="LICENSE">LICENSE</a>.</sub>

</div>
