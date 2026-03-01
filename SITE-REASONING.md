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
├── index.html                     # Home
├── about.html                     # About
├── projects.html                  # Projects
├── feed.xml                       # RSS
├── essays/
│   ├── index.html                 # Essays listing
│   └── [essay].html               # Individual essays
└── tools/
    ├── index.html                 # Tools listing
    ├── content-library-valuation.html  # Tool: valuation calculator
    └── through-line-guide.html         # Tool: through-line worksheet
```

### Two Page Types: Essays vs. Tools

**Essays** use a narrow, reading-focused layout:
- `max-width: 680px` centered body
- Standard article typography
- Inline visuals (CSS-only diagrams, charts)
- Newsletter signup before footer

**Tool pages** use a full-width, immersive layout:
- Full-width body with no max-width constraint
- Section-based structure with alternating backgrounds
- `.section { width: 100%; padding: 0 48px; }`
- `.section-inner { max-width: 1200px; }` for wide content (calculators, grids)
- `.section-narrow { max-width: 720px; }` for text blocks
- Hero section with centered headline
- Interactive elements (forms, toggles, calculators)
- The experience should feel distinct from reading an essay — like opening a different kind of page

Tool pages follow the Content Library Valuation page (`tools/content-library-valuation.html`) as the reference template. Every new tool should use this full-width section approach.

### Tool Page Anatomy

Every tool page follows a four-part experience:

1. **Orient** — Topbar (back link) → Hero (centered title, subtitle, lead text) → Stats/How-it-works bar (3-4 numbers summarizing the experience). The reader should understand what the tool does and what they'll get within 5 seconds.

2. **Input** — The working area where users provide their data. Section-based with alternating backgrounds (`--bg` and `--bg-dark`). Interactive elements (forms, textareas, calculators) sit inside wider containers (`section-inner` at 1200px), while explanatory text uses narrower containers (`section-narrow` at 720px). Each input phase gets its own labeled section (Step 1, Step 2, etc.).

3. **Output** — Where the tool gives something back. Score bars, verdicts, results cards, generated prompts. This is the payoff for the input work. Should feel like a reward, not just a summary.

4. **Extend** — Newsletter signup (centered, `max-width: 480px`) + footer with links to related essays and tools. The newsletter CTA is always centered with `text-align: center` and `justify-content: center` on the form.

### Tool Page Design Principles

- **Every tool links to its parent essay.** The essay explains the thinking; the tool makes it actionable. Link in the hero ("Based on the ideas in...") and in the footer.
- **Auto-assist where possible.** Don't make users do all the work manually. Suggest, pre-fill, extract, synthesize. The Through-Line Guide's "Suggest from answers" button is the model: it bridges the gap between input and creative synthesis.
- **Nothing is saved or sent.** All tools run client-side in the browser. State this explicitly in the hero. This builds trust and removes friction.
- **Placeholder text teaches.** The placeholder examples in form fields are as important as the instructions. They show users exactly what good input looks like. Use a consistent, non-marketing B2B example throughout each tool (e.g., "customer onboarding" for the through-line guide).
- **AI prompt generation is a standard output.** Every tool should generate a tailored AI prompt from the user's inputs. Branded as "AI prompt" (not Claude-specific) for universality. This extends the tool's value beyond the page itself.

### Current Tool Pages

| Tool | File | Parent Essay | Key Features |
|------|------|-------------|--------------|
| Content Library Valuation | `tools/content-library-valuation.html` | The Content Library | 5-view calculator, results cards, stats bar |
| Through-Line Development Guide | `tools/through-line-guide.html` | Why Helpful Content Gets Forgotten | 4 questions, auto-suggest, 5-test scoring, AI prompt generator |

### How to Add New Tools

1. Create new HTML file in `tools/` directory (copy section structure from existing tool)
2. Follow the four-part anatomy: Orient → Input → Output → Extend
3. Link to parent essay in hero and footer (use `../essays/` relative paths)
4. Add entry to `tools/index.html`
5. Include Clicky analytics and newsletter signup
6. Include AI prompt generation section if the tool collects structured input

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

## Audience and Content Perspective

**The reader:** A professional creator navigating the AI shift. Content strategists, editors, writers, marketers — people who've been doing this long enough to have taste and instincts, but who feel the ground moving under their feet. Not beginners looking for tutorials. Mid-career people asking: *What's still valuable about what I do?*

**The unique angle:** Michael answers this from three places at once — a decade-deep editorial leader, a storytelling student (psychology, triggers, narrative mechanics), and a builder shipping software with AI tools. That combination is rare. Most content strategy voices don't build products. Most builder voices don't have deep editorial chops. Most storytelling writers don't run content teams at scale.

**The territory:** What survives when AI can produce anything. Each essay answers this from a different angle — owned synthesis (Lens Method), thesis-driven thinking (Why Helpful Content Gets Forgotten), psychological mechanics (Story Triggers), craft and taste (Building a Mirror), rich human context (Voice Prompting). The consistency is in the lens, not the subject matter.

**The content library framing:** The website is not a blog with a publishing cadence. It's a library of crystallized thinking that grows at the pace of genuine insight. Each essay is a durable asset that can be deployed to other formats and platforms (podcasts, X articles, LinkedIn, workshops, talks) without starting from scratch. The library compounds — each new piece strengthens the whole body of work.

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
