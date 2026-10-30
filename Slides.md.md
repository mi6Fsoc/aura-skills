---
name: website-grade-slides
description: creates premium slide decks that replicate or evolve the visual language of a provided reference deck, especially sleek website-like business presentations with custom grids, modern ui cards, bold section dividers, and executive storytelling. use when aura.build needs to build a new presentation, redesign an existing deck, or transform notes, documents, or rough slides into a visually sophisticated deck for investor pitches, partner proposals, product strategy, market analysis, compliance overviews, or enterprise sales presentations where a generic powerpoint look is not acceptable.
keywords: ui-design, design-system, visual-design, layout, typography, best-practices, components, documentation
---

# Operating principle
Treat the deck as a product UI system, not a sequence of bullet slides. Reverse-engineer the visual language from the user's reference deck first, then apply it consistently across the full presentation.

## Required implementation
Use the `slides` skill to create the final deck.
Use PptxGenJS for deck generation unless the request is a tiny text-only edit.
Default to a 16:9 canvas and preserve the reference deck ratio when one is supplied.
If the user provides a reference PPTX, treat it as the visual source of truth.
If the user asks for "the same design or better," preserve the reference deck's DNA but improve hierarchy, whitespace, pacing, and polish.
When external facts or images are used, add `[Sources]` blocks in speaker notes for non-trivial claims and externally sourced assets.

## Workflow
1. Read all uploaded assets and identify the story, required slide count, fixed brand elements, and whether the goal is faithful replication or a refined evolution of the reference style.
2. If a reference deck is provided, inspect it before designing. Extract recurring background colors, typography, spacings, card geometry, borders, radii, footer placement, section-divider patterns, and illustration style.
3. Build a mini design system before placing content: page ratio, typography scale, palette, card components, section dividers, hero slides, process slides, and table/comparison patterns.
4. Rewrite raw copy into presentation copy. Use one idea per slide, short headlines, concise support text, and structured modules instead of long paragraphs.
5. Compose the slides using the design system.
6. Tighten the presentation. Remove clutter, normalize spacing, fix every overflow, and make every slide feel intentionally art-directed.

## Design language
For decks like the reference system, use the following visual language unless the user's brand rules override it.

### Core feel
- Make the deck feel like a premium SaaS website or enterprise microsite.
- Prefer confident asymmetry, strong visual hierarchy, floating cards, clean grids, and restrained but vivid gradients.
- Favor fewer, larger elements over many small ones.
- Preserve a sense of motion using diagonals, scan lines, dot grids, connectors, and strong sectional transitions.
- Make every slide feel designed, not assembled.

### Palette
Use a restrained palette with one dominant dark brand color, one warm signal color, one soft neutral tint, and white.

Suggested palette from the reference style:
- deep violet: `#6100A5`
- night violet: `#1F0046`
- soft lilac background: `#F5EFFD`
- lilac panel fill: `#E9C8FF`
- vivid orange: `#FF7B00`
- white: `#FFFFFF`
- red for risk or pain points: `#DC2626`
- green for positive or compliance states: `#16A34A`

Use orange and lilac as accents, not competing full themes on the same slide.
Keep backgrounds mostly light lilac or full violet.
Do not introduce extra colors unless data visualization requires them.


### Reference-specific layout behavior
For decks modeled on the reference style, use three primary background modes:
- light canvas: pale lilac background for most content slides
- dark canvas: full deep-violet background for timelines, process flows, or major transition moments
- hero canvas: vivid orange field with violet scan lines for cover and closing slides

Use full-bleed color only on opener, timeline, and closing moments. Keep most analytical slides on the light canvas.

### Cover and closing treatment
- Use a full-bleed orange background.
- Add dense horizontal violet scan lines entering from the right side.
- Let the scan field taper into a violet mass or corner form near the lower-right.
- Use very large white headline text.
- Keep supporting copy minimal.
- For the opener, allow one simple monoline gesture such as an arrow.
- For the closer, use oversized closing text with almost poster-like simplicity.

### Footer and corner behavior
- Keep a small brand mark or anchor at bottom-left.
- Keep a partner or secondary mark at bottom-right when appropriate.
- Align both to the same baseline across the deck.
- Add a subtle dotted micro-grid near the top-right on many light slides.
- Keep these elements quiet; they should create brand continuity without competing with the main content.

### Typography
- Prefer `Helvetica Neue`. If unavailable, use a close neo-grotesk fallback such as `Inter`, `Arial`, or `Aptos`.
- Use bold, compact titles with clear size jumps.
- Keep section titles very large and left-aligned.
- Keep body copy tight and readable.
- Avoid thin weights, novelty fonts, or center-aligned body text.
- Treat text like UI copy: crisp, short, and high-signal.

Suggested scale:
- cover or section title: 28-44 pt
- main content title: 18-28 pt
- card title: 11-15 pt
- body: 8.5-12 pt
- micro labels or footers: 6.5-8 pt

### Grid and spacing
- Use a 12-column mental grid even when the final layout is asymmetric.
- Keep generous outer margins.
- Reserve a consistent footer lane for logos or page anchors.
- Snap card edges and text blocks to shared guides.
- Use consistent vertical rhythm.
- Leave more empty space than a normal corporate deck. Empty space is part of the design.

## Signature components
Recreate these components consistently.

### 1. Window card
- Use a rounded rectangle.
- Use a thin violet border.
- Add a slim top strip with an orange-to-lilac gradient.
- Add a tiny circular control near the top-right.
- Use a white or pale interior.
- Use this for benefits, metrics, pain points, feature groups, and structured text.

### 2. KPI stat tile
- Use a compact card with a strong numeral.
- Add a small supporting label.
- Create crisp separation between value and descriptor.
- Optionally use a subtle gradient header or tint block.

### 3. Section divider
- Place a very large title on the left.
- Place an oversized illustration or abstract 3D object on the right.
- Keep supporting text minimal.
- Use strong whitespace.
- Do not clutter the slide.

### 4. Dark process timeline
- Use a full violet background.
- Run a white or pale line horizontally across the slide.
- Add gradient or color-coded nodes.
- Keep step labels short.
- Reduce copy aggressively.

### 5. Agenda or navigation tile grid
- Use numbered tiles.
- Create strong contrast between active and inactive states.
- Keep radius and spacing consistent.
- Make it feel like a dashboard module, not standard SmartArt.

### 6. Comparison table or quadrant
- Keep table chrome minimal.
- Use tinted headers and bold highlights.
- Increase whitespace around the most important row or column.
- If the table feels crowded, split it across multiple slides.

## Signature motifs
Use these motifs sparingly but consistently:
- horizontal scan lines or speed lines
- dotted micro-grid in a corner, usually top-right
- bold hero color fields
- angled or rising arrow gestures
- floating abstract 3D forms in the orange-violet family
- small footer logos aligned to a shared baseline

## Slide archetypes
Default to these archetypes when planning the deck:
- cover hero
- agenda or chapter menu
- thesis or positioning slide
- stats or partner-logo slide
- section divider
- problem slide with pain-point card
- solution slide with 2-4 feature cards
- process timeline
- compliance or monitoring diagram
- market insight slide
- quadrant or comparison table
- proof or differentiation grid
- next steps
- thank-you or closing hero

## Better-than-reference rules
When the user wants the same design or better, improve the deck in these ways without losing the reference DNA:
- reduce text density by 20-40%
- increase whitespace and card padding
- strengthen contrast between headline, support copy, and evidence
- turn dense paragraphs into structured modules
- make one visual idea dominant on each slide
- use fewer borders, but more intentional ones
- sharpen alignment so slides feel engineered
- use subtle depth only when it improves clarity
- upgrade charts and tables to feel like product UI
- vary slide archetypes while keeping the design system consistent

## Copy rules
- Write headlines that make claims, not labels.
- Keep subheads short and specific.
- Use bullets only when scanning improves.
- Prefer 3-5 crisp points over exhaustive lists.
- Turn jargon into concrete business language.
- Split a long idea across two slides instead of shrinking the text.

## Hard bans
Never do the following unless the user explicitly asks:
- generic PowerPoint templates
- default SmartArt
- dense bullet dumps
- mixed icon styles
- clipart or cheesy 3D graphics
- rainbow palettes
- center-aligning everything
- small text squeezed into every corner
- long unreadable tables
- default chart styling
- ornamental gradients with no structural purpose

## If the user supplies a reference deck
Treat the reference deck as a design system to reverse-engineer.
Extract and preserve:
- page ratio
- recurring backgrounds
- title placement
- footer behavior
- card geometry
- illustration style
- process-slide behavior
- section-divider style
- table styling
- color temperature and contrast behavior

Do not copy mistakes from the reference.
If the reference is visually strong but occasionally crowded, keep the aesthetic and fix the crowding.

## If the user does not supply a reference deck
Still design in this house style:
- premium fintech or enterprise website feel
- light lilac surfaces plus vivid violet-orange accents
- web-style cards and modules
- strong section openers
- high-contrast titles
- consistent footer anchors
- restrained motion cues

## Quality bar before delivery
Verify all of the following before finishing:
- the deck feels like one coherent design system
- every slide has a clear focal point
- all text fits without crowding
- recurring components are visually identical across slides
- titles, margins, and footers are consistent
- slide pacing alternates well between dense and light moments
- no slide feels like a placeholder or default layout
- the result looks closer to a premium product website than to a standard corporate deck

## Default response behavior
When asked to create a deck, do not stop at an outline unless the user explicitly asks for one.
Produce the actual slide deck.
If the request is ambiguous, make grounded design decisions that preserve polish and storytelling.
When exact data is missing, use clearly marked placeholders instead of weakening the visual system.