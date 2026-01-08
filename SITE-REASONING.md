# Michael Ofei Personal Site — Reasoning & Context

## The Tension This Site Resolves

Ofei Studios philosophy: "Products, not personal brand." No LinkedIn, no Twitter, no performative presence. Let the work speak for itself.

But there's a gap. Ideas like the Lens Method need a home — somewhere with provenance, where the thinking can live and be referenced. Without a personal site, these ideas either get published elsewhere (giving away ownership) or stay trapped in documents.

The insight: what I'm rejecting isn't "having a website" — it's the performative personal brand. The constant posting, the engagement farming, the self-promotion disguised as thought leadership.

What I actually want is closer to Paul Graham's site or Patrick Collison's bookshelf: a place to think in public, publish when there's something worth sharing, and let ideas compound over time.

## What This Site Is

- **A place to think in public** — essays when I have something worth sharing
- **No schedule, no newsletter** — RSS only for those who want to follow
- **Static HTML** — no CMS, no database, just files I can edit directly
- **Terminal aesthetic** — Red Sands palette from Apple Terminal, monospace fonts, retro/nostalgic feel

## What This Site Is Not

- A personal brand vehicle
- A content marketing funnel
- A place to post for engagement
- A portfolio to impress anyone

## Design Decisions

### Red Sands Palette (Apple Terminal)
```
Background: #7A251E (deep rust red)
Foreground: #D7C9A7 (warm tan/cream)
Yellow: #E7B000 (headings, dates, accents)
Green: #00BB00 (links, hover states)
```

### Why This Aesthetic
- Matches my daily working environment (Claude Code in terminal)
- Feels retro and distinctive — not another minimal white site
- Monospace font signals "thinking in code" without being a developer blog
- Low friction to maintain — just HTML files

### Structure
```
ofei-site/
├── index.html          # Home
├── about.html          # About
├── projects.html       # Projects
├── feed.xml            # RSS
└── essays/
    ├── index.html      # Essays listing
    └── the-lens-method.html
```

## Technical Stack

- **Pure static HTML/CSS** — no build step, no framework
- **RSS feed** — standard XML, manually updated
- **Hosting options**: GitHub Pages (free), Vercel, or Netlify
- **Editing workflow**: Edit HTML directly, push to git

## First Essay: The Lens Method

The Lens Method is the first essay because:
1. It's a framework I developed and want to own
2. It demonstrates the kind of thinking this site will house
3. Having it here establishes provenance before potentially writing about it elsewhere

## How to Add New Essays

1. Create new HTML file in `/essays/` (copy structure from existing essay)
2. Add entry to `/essays/index.html`
3. Add entry to `/feed.xml`
4. Optionally add to home page "Recent Essays"

## The Compounding Effect

Each essay builds:
- A body of work that demonstrates editorial perspective
- Ideas with clear provenance and ownership
- A reference point for conversations and collaborations
- Something that exists independent of any platform

## Inspirations

- Paul Graham's essays site (plain, content-focused)
- Patrick Collison's bookshelf (personal without being performative)
- Seth Godin's blog (consistency without pressure)
- Terminal aesthetics (Claude Code, retro computing)

---

*This site exists because some ideas need a home, and that home should be mine.*
