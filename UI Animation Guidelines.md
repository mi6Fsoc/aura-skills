---
keywords: animation, motion, transitions, micro-interactions, ux-design, ui-design, best-practices, performance
---

ui-animation
When to use: Designing, implementing, or reviewing motion in any UI — springs, gestures, drag interactions, entrance/exit reveals, easing selection, duration guidelines, clip-path techniques, performance debugging.

Trigger Phrases
"Add animations to", "make this feel smooth", "review my animations", "add a swipe gesture", "this feels stiff", "animate the transition"

Core Principles
Purpose over decoration — Motion earns its place by providing: feedback, orientation, continuity, or deliberate delight. Keyboard actions should never trigger animation.

Interruptible and input-driven — The best animations respond to user input and can be interrupted mid-flight. Predetermined sequences feel robotic.

Asymmetric timing — Exit animations must be faster than entry. Entering: 200–300ms. Exiting: 150–200ms. Things that leave should leave quickly.

Implementation hierarchy: CSS transitions > WAAPI > CSS keyframes > JavaScript animation

Only animate transform and opacity. Layout properties and transition: all are forbidden.

Easing Reference
Use Case	Curve	Duration
Button feedback, dropdowns	cubic-bezier(0.22, 1, 0.36, 1)	100–250ms
Slides, drawers	cubic-bezier(0.25, 1, 0.5, 1)	200–300ms
Spring-feel	Framer Motion spring: stiffness 300, damping 30	—
Subtle hover	ease-out	150ms
Avoid ease-in for UI. Reference easing.dev for custom curves.

Motion Direction Logic
Elements visible in both states transition in place — no teleporting. Rules:

Overlays emerge from their trigger element
Tabs slide in the direction matching their position in the tab list
Modals expand from center or from trigger
Lists stagger from top to bottom (entry), no stagger needed for exit
Anti-Patterns
transition: all — animates unexpected properties
Scaling from zero — use opacity + slight translateY instead
Permanent will-change — apply only during animation, remove after
Static cuts between related views
Hover-only animations without @media (hover: hover) gate
Five-Step Checklist
Does this animation serve a purpose? (feedback/orientation/continuity/delight)
Choose easing and duration from the reference above
Select implementation: CSS transition, WAAPI, or Framer Motion
Validate: can it be interrupted? Does it work at reduced motion?
Check on real device — desktop perception ≠ mobile perception