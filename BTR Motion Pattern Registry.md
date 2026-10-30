---
keywords: animation, motion, scroll-effects, micro-interactions, css, tailwind, nextjs, performance
---

Gemini
Ask about your files
What can Gemini do in Google Drive
Summarize a topic based on files in my Drive
Summarize a folder in my Drive
Gemini in Workspace can make mistakes. Learn more
---
name: motion-registry
description: >
  The BTR Motion Pattern Registry — a structured knowledge base of 160 animation patterns across 8 technologies (GSAP, Framer Motion, Three.js, WebGL/GLSL, CSS Scroll-Driven, Tailwind, Lenis, Canvas API). Use this skill for ANY task involving animation, motion design, scroll effects, parallax, interactive UI, page transitions, hover effects, loaders, text reveals, SVG animation, 3D scenes, shaders, particle systems, or any form of visual motion on the web. Triggers on: "animate", "scroll animation", "parallax", "GSAP", "Framer Motion", "Three.js", "motion", "interactive", "hover effect", "page transition", "loader", "text reveal", "marquee", "parallax scroll", "smooth scroll", "canvas particles", "WebGL", "shader", "3D scene", "whileInView", "ScrollTrigger", "add animation to", "make this move", "build a motion", or any request to add life or interactivity to a UI. When motion is involved in ANY capacity, use this skill — do not try to recall patterns from memory.
---

# BTR Motion Pattern Registry

You have access to a curated registry of 160 animation patterns across 8 web technologies. Every animation decision must come from this registry — not from memory, not from improvisation.

## The One Rule

**Always read `INDEX.md` first.** It contains the master decision tree, the use-case lookup table, and the path to the correct technology file. Do not skip it, even if you think you know which technology to use.

## Registry Location

```
/sessions/sharp-determined-dirac/mnt/CodeGrid-Motion GraPHICS 2/motion-registry/
├── INDEX.md                      ← START HERE — always
├── PATTERN_TEMPLATE.md           ← Use when adding new patterns
├── gsap/patterns.md              ← 20 GSAP patterns
├── framer-motion/patterns.md     ← 20 Framer Motion patterns
├── three-js/patterns.md          ← 20 Three.js patterns
├── webgl-glsl/patterns.md        ← 20 WebGL/GLSL shader patterns
├── css-scroll-driven/patterns.md ← 20 CSS Scroll-Driven patterns
├── tailwind/patterns.md          ← 20 Tailwind CSS patterns
├── lenis/patterns.md             ← 20 Lenis smooth scroll patterns
└── canvas/patterns.md            ← 20 Canvas API patterns
```

## Your Workflow

### Step 1 — Read INDEX.md
Open `INDEX.md`. Use the **Master Decision Tree** and **Use-Case Quick Lookup** table to identify which technology and which pattern number fits the task.

### Step 2 — Open the technology's patterns.md
Read only the relevant pattern(s) — you don't need to load the entire file if you know the pattern number.

### Step 3 — Apply the pattern
Build from the **Core code signature**. The signature is minimal and intentional — expand it to fit the project, but do not deviate from its stack conventions or performance rules.

### Step 4 — Respect the cross-pattern rules (from INDEX.md)
These apply to every build:
1. **Lenis first** — install and init Lenis before any scroll animation
2. **CONFIG objects** — externalize all animation values into a config object
3. **Resize handling** — kill/reinit scroll-based animations on resize (debounce 250ms)
4. **Performance cap** — `devicePixelRatio` max 2, `will-change` only on active elements
5. **Reduced motion** — always check `prefers-reduced-motion`
6. **`"use client"`** — required at top of any Next.js file using GSAP or Framer Motion
7. **No pattern mixing** — don't mix technologies within the same component

## Quick Reference

| Task | Technology | Pattern # |
|---|---|---|
| Any project with scroll | Lenis | #1 Basic Setup |
| Scroll-linked reveal | GSAP | #1 ScrollTrigger |
| Sticky / pinned section | GSAP | #2 Pin |
| Text reveal letter by letter | GSAP | #10 SplitText |
| Counter to a number | GSAP | #14 Counter |
| Horizontal scroll gallery | GSAP | #15 Horizontal Scroll |
| Infinite ticker/marquee | GSAP | #16 Marquee |
| React component animation | Framer Motion | #2 AnimatePresence |
| React scroll-linked | Framer Motion | #3 useScroll |
| React hover/tap feedback | Framer Motion | #6 whileHover |
| React stagger list | Framer Motion | #7 Variants |
| 3D product/scene | Three.js | see INDEX |
| Image hover distortion | WebGL/GLSL | see INDEX |
| Reading progress bar (no JS) | CSS Scroll-Driven | #1 |
| Skeleton loading | Tailwind | #6 |
| Particle system | Canvas API | #1 |

## When to Add New Patterns

If a pattern doesn't exist in the registry, use `PATTERN_TEMPLATE.md` to add it — fill all 6 fields, add to the correct technology file, and update the INDEX.md lookup table. Never leave a useful pattern undocumented.