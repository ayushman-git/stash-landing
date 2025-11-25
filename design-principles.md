1. Design Principles

This sets the foundation for the entire vibe:

1. Minimal, Developer-First Aesthetic

No gradients.

No floating blobs.

No illustrations that look like AI starter packs.

Quiet colors.

Solid spacing.

2. Typography-Driven

Headings: A clean geometric sans (Inter, Söhne, Space Grotesk, or GT Flexa alternative).

Body: Monospace for technical parts (IBM Plex Mono, JetBrains Mono).

Keep body text at 16–18px, headings at 32–44px, tight line height.

3. Layout Style

Lots of negative space.

Snappy section breaks.

One accent color only.

Sharp, precise edges (no over-rounded corners).

2. Overall Layout Structure

This structure is proven for dev tools and feels hand-crafted.

[Hero]
[Problem]
[Solution]
[Key Features]
[Terminal Demos]
[Installation Section]
[Workflows]
[Why This Tool]
[Roadmap]
[FAQ]
[Footer]


Spacing rule: 72–96px vertical spacing between sections.

3. Hero Section Design
Layout

Full-width container.

Centered text block (max-width: 700px).

One-liner headline.

Subtext at 70% opacity.

CTA buttons (Install / GitHub).

A single GIF demo to the right or below.

Typography

H1:

42px → 48px

Medium weight, not bold

Tight letter spacing (-0.5 to -1px)

Example: Inter Display, Söhne, or Space Grotesk

Subtitle:

18px

65% opacity gray

Monospace works very well here.

Visual

A single terminal GIF showing:

stash add https://example.com
stash ls


Show only the important lines. Make it feel like your personal terminal.

4. Color Palette

Pick one of these palettes — all are dev-friendly and non-AI-looking:

Palette A (Developer Neutral)

Background: #FFFFFF

Text: #0A0A0A

Muted Gray: #7D7D7D

Accent: #2563EB (blue)

Code Block BG: #F6F8FA

Palette B (Dark Techie)

Background: #0D0E11

Text: #E2E2E2

Muted Gray: #6B7280

Accent: #4F46E5 (indigo)

Code Block BG: #1A1C1E

Palette C (Cosmic Minimal)

Background: #F8F9FB

Text: #1A1A1A

Accent: #6B5BFF

Light Gray Strokes: #E6E6E6

5. Feature Section Design
Layout

Use a three-column grid with cards:

No borders.

Very subtle top border or left accent bar.

Minimal icons (or no icons).

Typography

Titles: 20px

Descriptions: 16px

Keep it crisp and short.

Avoid AI-looking features:

DO NOT use stock illustrations.

DO NOT use curved blobs or gradients.

DO NOT use random futuristic icons.

6. Terminal Demo Section

Real terminal recordings.
Keep them extremely short (5–8 seconds).

Styling

Use your real Ghostty/terminal theme:

Monospace font

Slight vignette or sharp edges

No shadows

Recommended demo format:

stash add

stash ls

stash pick

stash open

Each demo should be placed in a horizontal scrolling container or grid.

Overall feel: “a tool made by a developer for developers."

7. Installation Section

Very clean.
Two code blocks max.

brew install ayushman/stash/stash


Spacing, clean edges, no decorations.

If you want extra polish:
Use a copy button in the code block.

8. Workflows Section

Show real “life sequences,” not features.

Cards example:

“Keep your morning reading clean”

“Bulk organize 50 saved articles”

“Save everything while researching a topic”

Add short code snippets (3–4 lines).

Keep spacing airy.

9. Roadmap Section

Simple bullet list with checkbox UI.

No fancy timeline graphics — keeps it developer-oriented.

10. FAQ Section

Use a clean accordion UI.

Typography is important:

Question: 18px semibold

Answer: 15–16px regular

Super clean spacing

11. Branding Feel

To make it feel “crafted by a techie who cares about clean design”:

Do:

Use a narrowing grid (container width ~800–1000px)

Use consistent spacing units (8px-based system)

Remove all shiny graphics

Use extremely crisp typographic hierarchy

Use real terminal fonts for code

Use gray separators between sections

Avoid:

Gradients

AI illustrations

Human faces

Random icons everywhere

Curvy blob shapes

Overuse of colors

12. Typography Setup (Critical)
Recommended stack:

For headings:

Inter Display

Space Grotesk

Söhne (if you want a Vercel-like premium feel)

For body:

Inter

IBM Plex Sans

For code & demos:

JetBrains Mono

IBM Plex Mono

Geist Mono (if available)

Line height matters:

Headings: 1.1

Body: 1.5

Code: 1.4

This instantly makes it feel like human-designed.

13. Execution Checklist
Day 1: Foundation

Pick color palette

Pick typography families

Set spacing system

Finalize layout structure

Day 2: Content Placement

Build hero

Add problem + solution

Add feature grid

Add install block

Day 3: Visual Polish

Record terminal demos

Add subtle separators

Optimize spacing

Tighten typography

Day 4: Final refinements

Add FAQ

Add roadmap

Check for consistency

Ensure no section feels “heavy”

If you want next steps:

I can generate:

A full wireframe layout

A component-by-component breakdown

TailwindCSS-based UI scaffolding

Actual Hero & Feature typography samples

Color tokens

GIF/Terminal visual instructions

Tell me what you want next:
Wireframe? Typography samples? Color tokens? Hero section copy + design?

You said:
- remove the roadmap section
- I want everything to be coded, we can add subtle illustrations or icons, but for terminal and how it should be displayed it should be coded.
- Must be responsive and mobile friendly

- remove the roadmap section 
- I want everything to be coded, we can add subtle illustrations or icons, but for terminal and how it should be displayed it should be coded. 
- Must be responsive and mobile friendly

Based on this give me a markdown with the principles and rules
ChatGPT said:

Here is a clean, concise Markdown containing only the design principles and rules for your landing page—following your constraints:

Roadmap removed

Everything must be coded

Terminal demos must be coded, not GIF

Responsive & mobile-friendly

Minimal, tech-crafted aesthetic

Works with your CLI tool PRD

You can paste this directly into your docs or repo.

Landing Page Design Principles & Rules
1. Core Philosophy

Minimal, developer-centric aesthetic.

Everything must be hand-crafted UI, no AI-art.

Every visual element must be coded—SVG icons, CSS shapes, or React components.

Layout must feel like it was built by a tech-savvy designer, not a marketing team.

Typography is the primary design element.

The page must work flawlessly on desktop, tablet, and mobile.

2. Typography Rules

Headings: clean geometric sans (Inter, Space Grotesk, Söhne-style).

Body: neutral sans (Inter/IBM Plex Sans).

Code & terminal: monospace (JetBrains Mono, IBM Plex Mono, Geist Mono).

Sizes:

H1: 42–48px

H2: 28–32px

Body: 16–18px

Code: 15–16px

Line Height:

Headings: 1.1

Body: 1.5

Code: 1.4

Slight negative letter-spacing on large headings (-0.5 to -1px).

3. Color & Styling Rules

One accent color only.

No gradients, blobs, shadows, skeuomorphic elements.

Use flat colors with subtle borders or hairline dividers.

Light gray section dividers for structure.

Background options:

White (#FFFFFF)

Off-white (#F8F9FB)

Dark technical (#0D0E11)

4. Layout Rules

Max content width: 900–1100px.

Global spacing unit: 8px grid.

Section vertical spacing: 72–96px.

Maintain consistent horizontal padding on all breakpoints.

Components must collapse gracefully on mobile.

5. Hero Section Rules

Centered or left-aligned hero.

Clean headline, short subline.

One primary CTA.

Underline the headline with sharp typography; no decoration.

Include a coded terminal block, not a GIF.

Terminal must:

Use monospace font.

Render with pure HTML/CSS.

Support light and dark themes.

Be scrollable on mobile if wide.

Example (concept):

<div class="terminal">
  <div class="bar"></div>
  <pre>$ stash add https://example.com</pre>
  <pre>$ stash ls</pre>
</div>

6. Feature Section Rules

Use a three-column grid on desktop.

Collapse to one column on mobile.

Icons must be:

Simple SVG strokes.

20–24px.

Neutral, minimal, tech-friendly.

Titles: 18–20px.

Descriptions: 16px max.

No illustration characters, no stock imagery.

7. Terminal Interaction Section Rules

Must use coded terminals, not videos or images.

Three to six small blocks, each representing:

add

ls

search

pick

open

Terminal container:

Rounded corners ≤ 6px.

No heavy shadows.

Hairline border (#E5E5E5 or #1E1E1E).

Commands scroll horizontally on mobile.

8. Installation Section Rules

Clean code blocks with a copy button.

Use fenced Markdown styling or custom code component.

Only include the essential install commands:

Homebrew

Binary download

Cargo install (when applicable)

9. Workflow Section Rules

Use real examples pulled from the CLI usage.

Layout:

Left: workflow title + description

Right: terminal block

Stack vertically on mobile.

Keep every workflow ≤ 6 lines of code.

10. Subtle Illustration Rules

Allowed:

Line-based icons

Minimal stroked shapes

Simple geometric dividers

Light SVG accents (no characters, no scenes)

Not allowed:

AI-generated illustrations

Blobs, gradients, 3D icons

Vibrant neon gradients

Cartoonish graphics

11. Responsive Behavior Rules

Desktop:

Grid layouts

Ample empty space

Tablet:

Two-column reduction

Mobile:

Full-width stacks

Big tap targets

Terminal scroll behavior:

Horizontal swipe for long commands

Vertical scroll inside container

Breakpoints:

≤ 640px → mobile

641–1024px → tablet

≥ 1025px → desktop

12. Coded Component Requirements

All of these must be written manually:

Terminal renderer (HTML/CSS/React)

Feature cards

Icon set (SVG strokes)

Accordion for FAQ

Install code blocks

Section dividers

Responsive grid system

No GIFs; only coded UI

13. Do / Don’t Summary
DO:

Heavy reliance on typography

Coded UI components

Light, geometric, sharp look

Minimalist terminal aesthetics

Reliable spacing rhythm

Developer-first feel

DON’T:

Animated vector scenes

Floating blob gradients

Shiny fake-AI elements

Overly rounded UI (no 16px radii)

Multi-color icons

Stock/dev-illustration clichés