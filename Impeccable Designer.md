---
keywords: design-system, ui-design, visual-design, best-practices, typography, color, animation, responsive
---

impeccable
When to use: When you want production-grade, distinctive frontend design that avoids the "AI slop" aesthetic — recognizable AI defaults like Inter everywhere, gradient text, side-stripe alert borders. Use craft mode to build, teach mode to set up design context, extract mode for reusable components.

Core Principle
"A distinctive interface should make someone ask 'how was this made?' not 'which AI made this?'"

Three Modes
craft — Shape-then-build. Confirm design context first, then implement. teach — Explore the codebase, ask focused UX questions, write .impeccable.md Design Context file. extract — Pull reusable components from existing UI.

Context Protocol (ALWAYS first)
Before any design work:

Check current instructions for existing Design Context
Read .impeccable.md from project root if it exists
If neither exists: run teach mode — explore codebase, ask focused UX questions, write context
Absolute Bans (most recognizable AI tells)
Side-stripe borders — border-l-4 or border-r-4 on cards/alerts. Completely forbidden.
Gradient text fills — background-clip: text rainbow gradients. Forbidden.
Reflex fonts — Inter, DM Sans, Fraunces used reflexively without rationale. Pick fonts with intentionality.
Typography
Font selection is a 4-step process anchored in brand voice, not designer reflex:

What is the brand's personality? (clinical, playful, authoritative, warm...)
What typographic tradition matches that? (humanist sans, geometric, transitional serif...)
Which specific typefaces embody it with distinctive character?
Validate against the "reflex fonts" list — if it's on there, find a better reason to use it or pick another
Color
OKLCH color space for perceptual uniformity
Tint neutrals toward brand hue (never pure gray)
60-30-10 rule for visual weight
Theme (light/dark) must derive from actual user context, not defaults
Layout
4pt spacing scale with semantic tokens
gap for sibling spacing (not margins)
Vary spacing rhythmically — embrace intentional asymmetry
Grid breaks are intentional design moves, not accidents
Seven Reference Domains
When deeper guidance is needed, the full skill has reference files for: typography, color/contrast, spatial design, motion design, interaction design, responsive design, and UX writing.

design-taste
When to use: Enforcing premium anti-cliché UI patterns. Counteracting common AI-generated design signatures. Building SaaS dashboards, marketing sites, or any interface that should feel like it cost money to design.

Core Metrics (tunable)
Design Variance: 8/10 — push for distinctiveness
Motion Intensity: 6/10 — present but purposeful
Visual Density: 4/10 — breathable, not sparse
Hard Bans
Element	Banned	Use Instead
Font	Inter	Geist, Outfit, Cabinet Grotesk, Satoshi
Color	AI Purple/Blue aesthetic	Intentional brand palette
Black	#000000 (pure)	Near-blacks: #0A0A0A, #0F0F0F
Effects	Neon glows, custom mouse cursors	Subtle shadows, intentional depth
Content	"John Doe", "99.99% uptime"	Real-feeling specificity
Icons	Emojis as UI elements	Lucide, Heroicons, Phosphor
The Motion-Engine Bento Architecture
Modern SaaS dashboards that feel "alive":

White cards (#ffffff) on light gray backgrounds (#f5f5f5)
rounded-[2.5rem] on outer containers, rounded-[1.5rem] on inner cards
Diffusion shadows: box-shadow: 0 8px 32px rgba(0,0,0,0.08)
Five card archetypes with perpetual micro-interactions:
Intelligent List — items with subtle entrance staggers
Command Input — typing indicator, focus ring glow
Live Status — pulsing indicator, real-time number ticks
Wide Data Stream — sparkline with animated drawing
Contextual UI — hover-reveal secondary actions
Hero Section Rule
NEVER use h-screen. ALWAYS use min-h-[100dvh] to prevent layout jumping on mobile browsers.

Animation Stack
Framer Motion for complex interactions
Spring physics: stiffness: 100, damping: 20
Hardware acceleration via transform and opacity only
Isolate perpetual micro-animations in their own components
Pre-Flight Checklist
 No Inter unless explicitly justified
 No AI purple/blue palette
 No pure #000000
 No h-screen hero sections
 min-h-[100dvh] used instead
 All animations use transform/opacity
 Empty, loading, and error states all handled
 Mobile layout tested and non-broken