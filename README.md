# Stash Landing Page

A modern, responsive landing page for Stash - a fast, local-first CLI article manager built in Rust.

## Design

Inspired by [rollups.com](https://rollups.com/), featuring:
- Dark green color scheme with geometric patterns
- Clean, spacious layout with generous whitespace
- Terminal mockups showcasing CLI workflows
- Responsive design for all devices
- Smooth animations and hover effects

## Tech Stack

- **SvelteKit** - Modern web framework
- **Tailwind CSS v4** - Utility-first styling
- **TypeScript** - Type safety
- **Bun** - Fast package manager and runtime

## Project Structure

```
src/
├── lib/
│   └── components/
│       ├── Hero.svelte           # Hero section with install buttons
│       ├── InstallButtons.svelte # Platform-specific install commands
│       ├── UseCases.svelte       # Two ways to use Stash
│       ├── InAction.svelte       # Workflow demonstrations
│       ├── Features.svelte       # Key features grid
│       ├── SocialProof.svelte    # GitHub stats and trust indicators
│       ├── FAQ.svelte            # Expandable FAQ accordion
│       └── Footer.svelte         # Footer with links
├── routes/
│   ├── +layout.svelte            # Layout with SEO meta tags
│   └── +page.svelte              # Main landing page
└── app.css                       # Custom styles and theme
```

## Sections

1. **Hero** - Large headline, subheadline, install buttons for macOS/Windows/Linux, terminal preview
2. **Use Cases** - Quick Save workflow and Power User features
3. **In Action** - Four workflow examples with terminal mockups
4. **Features** - Six key features in a grid layout
5. **Social Proof** - GitHub stats and tech stack badges
6. **FAQ** - Common questions with accordion
7. **Footer** - Links to documentation, GitHub, and resources

## Development

Start the development server:

```bash
bun run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

## Building

Create a production build:

```bash
bun run build
```

Preview the production build:

```bash
bun run preview
```

## Features

- ✅ Responsive design (mobile, tablet, desktop)
- ✅ Copy-to-clipboard for install commands
- ✅ Smooth scroll behavior
- ✅ Terminal mockups with syntax highlighting
- ✅ Interactive FAQ accordion
- ✅ SEO optimized with meta tags
- ✅ Dark theme with custom color palette
- ✅ Hover effects and animations

## Customization

To customize for your own CLI tool:

1. Update colors in `src/app.css` (@theme section)
2. Replace install commands in `InstallButtons.svelte`
3. Update GitHub links in `Footer.svelte` and `SocialProof.svelte`
4. Modify content in each component to match your tool's features
5. Update meta tags in `+layout.svelte`

## License

MIT
