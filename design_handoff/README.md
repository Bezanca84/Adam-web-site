# Design Handoff: Adam Bezance — Agent Architect Website

## Overview

Personal website for **Adam Bezance**, a Microsoft Power Platform, Copilot Studio and M365 Copilot specialist pursuing Microsoft MVP status. The brand positions Adam as the **Agent Architect** — an authoritative, community-first expert building intelligent solutions with Microsoft AI.

The site showcases his writing, speaking, certifications, and portfolio to support an MVP nomination, and acts as a central hub for his community presence.

---

## About the Design Files

The files in this bundle are **high-fidelity design references created in HTML**. They show the intended look, typography, colour, spacing, and interactions of the website. They are **not production code to copy directly** — they are prototypes built to communicate design intent.

Your task is to **recreate these designs in your chosen production framework** (Next.js, Astro, SvelteKit, etc.) using proper component architecture, a CMS or markdown for content, and good engineering practices. Use this README and the bundled HTML files together — the README is the specification, the HTML is the visual reference.

---

## Fidelity

**High-fidelity.** Every colour value, font size, weight, spacing, shadow, glow, border radius, hover state, and animation is finalised and should be implemented pixel-precisely. The design is complete — no further design decisions are needed to ship.

---

## Brand

| Property | Value |
|---|---|
| Full name | Adam Bezance |
| Brand title | Agent Architect |
| Tagline | Building intelligent solutions with Microsoft AI |
| Specialisms | Power Platform · Copilot Studio · M365 Copilot · Power Automate · AI Builder |
| MVP status | Candidate 2026 |

---

## Design Tokens

### Colours (Obsidian & Electric Blue palette)

All colours are defined as CSS custom properties. Use these exact values.

```css
/* Backgrounds — 5-level dark scale */
--ob-canvas:    #050508;   /* Page background */
--ob-base:      #0A0A12;   /* Alternate section background */
--ob-surface:   #0F0F18;   /* Card / panel surfaces */
--ob-elevated:  #161625;   /* Tooltips, dropdowns, badges */

/* Brand accent — single electric blue */
--ob-blue:      #1D6FE8;
--ob-blue-lt:   #7BB3FF;   /* Light blue for text on dark */
--ob-blue-dim:  rgba(29, 111, 232, 0.14);   /* Tinted bg for pills/tags */
--ob-blue-brd:  rgba(29, 111, 232, 0.32);   /* Border on blue elements */

/* Borders */
--ob-border:    rgba(255, 255, 255, 0.06);  /* Resting card border */
--ob-border-md: rgba(255, 255, 255, 0.10);  /* Default/input border */
--ob-border-st: rgba(255, 255, 255, 0.16);  /* Strong border / secondary btn */

/* Foreground */
--ob-fg:        #FFFFFF;   /* Primary text */
--ob-fg-2:      #7A7A96;   /* Secondary / body copy */
--ob-fg-3:      #3E3E58;   /* Muted / meta / disabled */

/* Semantic */
--ob-gold:      #FFD700;   /* MVP badge / upcoming pill */
--ob-gold-bg:   rgba(255, 215, 0, 0.08);
--ob-gold-brd:  rgba(255, 215, 0, 0.22);

/* Effects */
--ob-glow:           0 4px 28px rgba(29, 111, 232, 0.50);   /* Button glow */
--ob-glow-card:      0 0 0 1px rgba(255,255,255,0.05), 0 8px 28px rgba(0,0,0,0.50);
--ob-glow-card-hover:0 0 0 1px rgba(29,111,232,0.35), 0 12px 36px rgba(0,0,0,0.55), 0 0 20px rgba(29,111,232,0.22);
```

### Typography

Font stack: `'Segoe UI', -apple-system, BlinkMacSystemFont, 'SF Pro Display', 'Helvetica Neue', Arial, sans-serif`  
Monospace: `'Cascadia Code', 'Cascadia Mono', Consolas, 'Courier New', monospace`

No web fonts required — these are system fonts.

| Role | Size | Weight | Line Height | Tracking |
|---|---|---|---|---|
| Hero title | `clamp(56px, 7.5vw, 96px)` | 800 | 0.97 | -0.04em |
| Section title | `clamp(32px, 3.5vw, 48px)` | 800 | 1.1 | -0.03em |
| H2 (About) | `clamp(26px, 3vw, 40px)` | 800 | 1.15 | -0.03em |
| Card title (featured) | 18px | 700 | 1.3 | -0.02em |
| Card title | 16px | 700 | 1.3 | -0.015em |
| Body large | 17–19px | 400 | 1.65–1.7 | 0 |
| Body | 16px | 400 | 1.6 | 0 |
| Body small | 13–14px | 400 | 1.5–1.55 | 0 |
| Nav links | 14px | 500 | — | 0 |
| Eyebrow / label | 11px | 700 | — | 0.12em (uppercase) |
| Meta / caption | 11–12px | 400–600 | — | 0.08em (uppercase) |
| Pill / badge | 10–12px | 600–700 | — | 0.03–0.07em |

### Spacing (4px grid)

| Token | Value | Usage |
|---|---|---|
| `space-1` | 4px | — |
| `space-2` | 8px | Inline gaps |
| `space-3` | 12px | Item gaps |
| `space-4` | 16px | — |
| `space-6` | 24px | Element gaps |
| `space-8` | 32px | — |
| `space-12` | 48px | Component gaps |
| `space-16` | 64px | — |
| `space-section` | 96px | Between page sections (padding-top & bottom) |
| Nav height | 68px | Fixed nav bar |
| Nav padding-x | 40px | Horizontal page padding |

### Border Radius

| Token | Value | Usage |
|---|---|---|
| `radius-sm` | 6px | — |
| `radius-md` | 10px | Buttons, small cards |
| `radius-lg` | 14px | Cards, speaking cards, cert cards |
| `radius-xl` | 20px | About photo |
| `radius-full` | 9999px | Pills, badges, nav CTA |

### Motion

| Property | Value |
|---|---|
| Hover transition duration | 220ms |
| Hover easing | `cubic-bezier(0.4, 0, 0.2, 1)` |
| Scroll reveal duration | 600ms |
| Scroll reveal easing | `cubic-bezier(0.0, 0.0, 0.2, 1)` |
| Scroll reveal translate | `translateY(28px)` → `translateY(0)` + `opacity: 0` → `1` |
| Reveal threshold | 10% of element in viewport |
| Stagger delays | 100ms, 200ms, 320ms |

---

## Layout

- **Max page width:** 1400px (centred)
- **Content column:** 1200px (for section grids)
- **Narrow column:** 720px (CTA section)
- **Page padding:** 40px horizontal
- **Sections alternate** between `--ob-canvas` (default) and `--ob-base` (alt)

---

## Screens & Sections

### 1. Navigation Bar

**Layout:** Fixed, full-width, 68px tall. Flex row: logo (left, `margin-right: auto`) + links + CTA (right). Padding: `0 40px`.

**Scroll behaviour:** Transparent at top. On scroll >30px: `background: rgba(5,5,8,0.90)` + `backdrop-filter: blur(18px)` + `border-bottom: 1px solid rgba(255,255,255,0.06)`. Transition: `220ms ease`.

**Logo mark:**
- 36×36px, `border-radius: 8px`
- Background: `#1D6FE8`, box-shadow: `0 4px 28px rgba(29,111,232,0.50)`
- Text: "AB", 13px, weight 800, white

**Logo text:**
- Name: "Adam Bezance" — 14px, weight 700, `#FFFFFF`, tracking -0.01em
- Subtitle: "AGENT ARCHITECT" — 9px, weight 700, tracking 0.12em, uppercase, `#3E3E58`

**Nav links:** "About", "Blog", "Speaking", "Certifications", "Contact" — 14px, weight 500, `#7A7A96`. Hover → `#FFFFFF`, 120ms transition.

**CTA button:** "Let's Talk" — 13px, weight 700, padding `8px 20px`, `border-radius: 9999px` (pill), background `#1D6FE8`, white text, `box-shadow: 0 4px 28px rgba(29,111,232,0.50)`. Hover: `opacity: 0.88`, `translateY(-1px)`.

---

### 2. Hero Section

**Layout:** Full viewport height (`min-height: 100vh`). Flex column, centred. Padding: `(nav-height + 80px) 40px 100px`.

**Background:**
- Base: `#050508`
- Glow blobs (3 layered radial gradients, `position: absolute, pointer-events: none`):
  - `radial-gradient(ellipse 65% 55% at 65% 25%, rgba(29,111,232,0.22) 0%, transparent 60%)`
  - `radial-gradient(ellipse 50% 65% at 15% 80%, rgba(29,111,232,0.10) 0%, transparent 55%)`
  - `radial-gradient(ellipse 40% 50% at 85% 70%, rgba(100,150,255,0.08) 0%, transparent 50%)`
- Grid overlay: `opacity: 0.018`, `52px × 52px` grid, 1px lines, `rgba(255,255,255,1)`

**Content stack** (centred, `max-width: 1000px`, `gap: 26px`):

1. **Eyebrow pill:** "⭐ Microsoft MVP Candidate 2026" — 11px, weight 700, tracking 0.10em, uppercase. Background `rgba(255,215,0,0.08)`, color `#FFD700`, border `1px solid rgba(255,215,0,0.22)`, `border-radius: 9999px`, padding `6px 16px`.

2. **Hero title:** "Building the Future with Microsoft AI." — `clamp(56px, 7.5vw, 96px)`, weight 800, tracking `-0.04em`, line-height `0.97`, color `#FFFFFF`. Has `<br>` after each line: "Building the / Future with / Microsoft AI."

3. **Sub-headline:** "Power Platform · Copilot Studio · M365 Copilot. From automating enterprise workflows to architecting intelligent agents — I share everything I learn." — `clamp(16px, 1.8vw, 19px)`, weight 400, color `#7A7A96`, `max-width: 540px`, line-height 1.65.

4. **Tech pills** (flex row, gap 9px, centred):
   - "Power Platform", "Copilot Studio", "M365 Copilot", "Power Automate"
   - Each: `padding: 5px 14px`, `border-radius: 9999px`, background `rgba(29,111,232,0.14)`, color `#7BB3FF`, border `1px solid rgba(29,111,232,0.32)`, 12px, weight 600.

5. **CTA buttons** (flex row, gap 12px):
   - Primary "Read the Blog →": `padding: 14px 32px`, `border-radius: 10px`, background `#1D6FE8`, white, 16px, weight 700, glow `0 4px 28px rgba(29,111,232,0.50)`. Hover: `opacity: 0.88`, `translateY(-1px)`.
   - Secondary "Speaking & Events": same padding/radius, background `rgba(255,255,255,0.04)`, white, border `1px solid rgba(255,255,255,0.16)`. Hover: border → `rgba(29,111,232,0.32)`, `translateY(-1px)`.

6. **Stats row** (flex, gap 48px, centred, `padding-top: 36px`, `border-top: 1px solid rgba(255,255,255,0.06)`):
   - 4 stats: "47 / Articles Published", "12 / Speaking Events", "8 / Certifications", "6+ / Years in Platform"
   - Number: 38px, weight 800, tracking -0.04em, color `#1D6FE8`
   - Label: 11px, weight 600, tracking 0.08em, uppercase, color `#3E3E58`

---

### 3. About Section

**Layout:** Background `#050508`. Section padding `96px 40px`. Max-width `1200px` centred.

**Grid:** `grid-template-columns: 1fr 1.6fr`, gap `72px`, aligned centre.

**Left — Photo block:**
- Photo placeholder: `aspect-ratio: 3/4`, `border-radius: 20px`, background `linear-gradient(135deg, rgba(29,111,232,0.12), rgba(29,111,232,0.04))`, border `1px solid rgba(29,111,232,0.32)`, `box-shadow: 0 0 32px rgba(29,111,232,0.25), ...card-shadow`
- Placeholder text "AB": 80px, weight 800, tracking -0.05em, color `#1D6FE8`, opacity 0.25
- **Badge** (absolute, `bottom: -14px, right: -14px`): background `#161625`, border `1px solid rgba(255,255,255,0.16)`, `border-radius: 14px`, padding `14px 18px`. Number "47": 26px, weight 800, `#1D6FE8`. Label "ARTICLES": 10px, weight 600, tracking 0.08em, uppercase, `#3E3E58`.

**Right — Content:**
- Eyebrow: "About Me" — electric blue, 11px, 700, 0.12em uppercase
- H2: "Agent Architect, community builder, Microsoft AI nerd." — `clamp(26px, 3vw, 40px)`, weight 800, tracking -0.03em, line-height 1.15, white
- Two body paragraphs: 17px, `#7A7A96`, line-height 1.7
- **Tag pills:** same style as hero pills. Primary tags use blue, secondary use `rgba(255,255,255,0.04)` bg with `#7A7A96` text and `rgba(255,255,255,0.10)` border
- CTA: same primary button style, smaller — `font-size: 14px, padding: 11px 24px`

---

### 4. Blog Section

**Layout:** Background `--ob-base` (`#0A0A12`). Same section padding.

**Header:** Eyebrow "Latest Writing", title "From the Blog", sub "Practical guides, deep-dives, and hard-won lessons from the trenches of Microsoft AI."

**Grid:** `grid-template-columns: 1.4fr 1fr 1fr`, gap `20px`.

**Card (base style):**
- Background: `#0F0F18`, border `1px solid rgba(255,255,255,0.06)`, `border-radius: 14px`
- Box-shadow: `0 0 0 1px rgba(255,255,255,0.05), 0 8px 28px rgba(0,0,0,0.50)`
- Padding: 22px (28px for featured)
- Transition: `all 220ms ease`
- Hover: border → `rgba(29,111,232,0.32)`, `translateY(-3px)`, box-shadow → `0 0 0 1px rgba(29,111,232,0.35), 0 12px 36px rgba(0,0,0,0.55), 0 0 20px rgba(29,111,232,0.22)`

**Card contents (flex column, gap 12px):**
- **Category badge:** background `rgba(29,111,232,0.14)`, color `#7BB3FF`, border `rgba(29,111,232,0.32)`, 10px, weight 700, tracking 0.07em, uppercase, pill
- **Title (featured):** 18px, weight 700, tracking -0.02em, line-height 1.3, white
- **Title (small):** 16px, weight 700, tracking -0.015em
- **Excerpt:** 13–14px, `#7A7A96`, line-height 1.5–1.55, clamped to 2–3 lines (`-webkit-line-clamp`)
- **Meta:** "3 Jun 2026 · 12 min read" — 12px, `#3E3E58`

**Footer:** Centred secondary button "View all articles →", `margin-top: 48px`.

---

### 5. Certifications Section

**Layout:** Background `#050508`. Same section padding.

**Grid:** `grid-template-columns: repeat(4, 1fr)`, gap `16px`.

**Cert card:**
- Same base card style, padding `28px 20px`
- Flex column, centred, gap `14px`, text-align centre
- **Icon container:** 56×56px, `border-radius: 10px`, background `rgba(29,111,232,0.14)`, centred SVG icon in blue tones
- **Name:** 14px, weight 700, white, line-height 1.35
- **"Certified" label:** 10px, weight 700, tracking 0.08em, uppercase, `#1D6FE8`

**Certifications shown:**
1. PL-900 Power Platform Fundamentals
2. PL-200 Power Platform Functional Consultant
3. PL-400 Power Platform Developer
4. AI-102 Azure AI Engineer Associate

---

### 6. Speaking Section

**Layout:** Background `#0A0A12`. Same section padding.

**Header:** Eyebrow "Speaking & Events", title "On Stage & On Air", sub "Conferences, webinars, podcasts and community events where I've shared the platform story."

**Grid:** `grid-template-columns: repeat(3, 1fr)`, gap `16px`.

**Speaking card:**
- Same base card style, padding `24px`
- **Type label:** 10px, weight 700, tracking 0.08em, uppercase, `#1D6FE8`
- **Upcoming pill:** (shown alongside type) — background `rgba(255,215,0,0.08)`, color `#FFD700`, border `rgba(255,215,0,0.25)`, 10px, weight 700, tracking 0.06em, uppercase, `border-radius: 9999px`, padding `2px 9px`
- **Talk title:** 16px, weight 700, tracking -0.015em, white, line-height 1.3
- **Event name:** 13px, weight 500, `#7A7A96`
- **Meta (date · location):** 12px, `#3E3E58`, flex row gap 8px
- Hover: same card hover as blog cards

**Speaking entries:**
1. Conference (Upcoming) — "Extending Copilot Studio with Custom AI Actions" / Microsoft Power Platform Conference / Oct 2026 / Las Vegas, NV
2. Webinar — "M365 Copilot Governance Deep Dive" / Microsoft Community Live / Apr 2026 / Online
3. Podcast — "The Future of Agentic AI in Enterprise" / Power Platform Podcast / Mar 2026 / Online
4. Conference — "Zero-Code Agents: Copilot Studio for Business Users" / European Power Platform Conference / Jun 2026 / Dublin, IE
5. Community — "Power Platform User Group — AI Builder Masterclass" / PPUG London / Feb 2026 / London, UK
6. Workshop — "Hands-On: Build and Deploy a Copilot in 90 Minutes" / Microsoft Ignite After-Party / Nov 2025 / Chicago, IL

---

### 7. Contact / CTA Section

**Layout:** Background `#0A0A12`. Glow overlay: `radial-gradient(ellipse 55% 75% at 50% 50%, rgba(29,111,232,0.14) 0%, transparent 70%)`. Max-width `720px` centred, text-align centre.

**Content:**
- **Eyebrow pill:** "Let's Build Something" — blue pill (same as hero eyebrow but blue instead of gold)
- **Title:** "Got a project, talk, or question?" — `clamp(32px, 4vw, 52px)`, weight 800, tracking -0.035em, line-height 1.05
- **Sub:** 18px, `#7A7A96`, line-height 1.6
- **Buttons:** Primary "Send me a message →" (`href="mailto:adam@bezance.ai"`), Secondary "Download my one-pager"
- **Social links:** LinkedIn, GitHub, Twitter/X, YouTube — 13px, `#3E3E58`, hover → `#7A7A96`

---

### 8. Footer

**Layout:** Background `#050508`, `border-top: 1px solid rgba(255,255,255,0.06)`. Padding `32px 40px`. Flex row, space-between, wrap.

**Left:** 28×28px blue mark ("AB", weight 800) + "Adam Bezance · Agent Architect" — 13px, weight 600, `#7A7A96`.

**Centre:** Nav links (About / Blog / Speaking / Contact) — 13px, `#3E3E58`, hover → `#7A7A96`.

**Right:** "© 2026 Adam Bezance" — 12px, `#3E3E58`.

---

## Interactions & Behaviour

### Scroll-triggered reveals

All section content fades in on scroll. Implementation:

```js
const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.classList.add('visible');
      observer.unobserve(e.target);
    }
  });
}, { threshold: 0.10 });

document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
```

```css
.reveal {
  opacity: 0;
  transform: translateY(28px);
  transition: opacity 600ms cubic-bezier(0,0,0.2,1),
              transform 600ms cubic-bezier(0,0,0.2,1);
}
.reveal.visible { opacity: 1; transform: translateY(0); }
.reveal-delay-1 { transition-delay: 100ms; }
.reveal-delay-2 { transition-delay: 200ms; }
.reveal-delay-3 { transition-delay: 320ms; }
```

Grid siblings use staggered delays: first card `.reveal`, second `.reveal.reveal-delay-1`, third `.reveal.reveal-delay-2`.

Wrap in `@media (prefers-reduced-motion: no-preference)` — show content immediately for reduced-motion users.

### Navigation scroll glass

```js
const nav = document.getElementById('nav');
window.addEventListener('scroll', () => {
  nav.classList.toggle('scrolled', window.scrollY > 30);
});
```

### Card hover

All cards (blog, cert, speaking): `transform: translateY(-3px)` + border and shadow change. Use CSS transitions, not JS.

### Button hover

Primary: `opacity: 0.88` + `translateY(-1px)`.
Secondary: `border-color` → brand blue + `translateY(-1px)`.

---

## Assets

### Logo

Three SVG files provided in `assets/`:

| File | Description |
|---|---|
| `logo-mark.svg` | Gradient hexagon with "AB" monogram + node dots at vertices |
| `logo-full.svg` | Mark + wordmark "ADAM BEZANCE" + subtitle "AGENT ARCHITECT" |
| `logo-white.svg` | Solid white mark for use on coloured backgrounds |

The logo mark is a **hexagonal shape** referencing agent network topology — six white circles at the vertices represent connected nodes. Gradient runs: `#50E6FF → #0078D4 → #7B5EA6 → #C239B3` (kept from original brand; the Obsidian palette update uses the mark as-is since the gradient logo still works on the dark canvas).

### Icons

No custom icon set. Use **Fluent System Icons** (Microsoft's open-source library): `https://github.com/microsoft/fluentui-system-icons`. Regular weight, 20px or 24px SVG. Colour: `currentColor`.

### Photography

Not yet provided. The About section has an "AB" placeholder — replace with a professional headshot. Recommended treatment: cool-shifted, desaturated, dark-mode native. `aspect-ratio: 3/4`.

---

## Pages to Build

The current design covers the **homepage** only. Additional pages needed:

| Page | Notes |
|---|---|
| Blog index | Card grid, pagination, category filter |
| Blog post | Narrow reading column (720px), large headline, code blocks in monospace |
| Speaking detail | Individual talk page with abstract, slides embed, recording |
| Resources / downloads | Card grid with file type badges and download CTAs |
| About (extended) | Long-form bio, timeline, community contributions list |

---

## Technical Recommendations

- **Framework:** Next.js (App Router) or Astro — both suit a content/portfolio site with good static generation
- **CMS:** Contentful, Sanity, or Markdown + MDX for blog posts and speaking entries
- **CSS approach:** CSS custom properties (matching the token structure in this handoff), with Tailwind or vanilla CSS modules
- **Fonts:** No web font downloads required — system font stack only
- **Animation:** Use the Intersection Observer pattern above, or a library like Framer Motion if using React
- **Accessibility:** All interactive elements need visible focus rings (suggest `outline: 2px solid #1D6FE8; outline-offset: 2px`). Respect `prefers-reduced-motion`.

---

## Files in this Package

| File | Description |
|---|---|
| `README.md` | This document — full design specification |
| `index.html` | Complete high-fidelity homepage mockup |
| `logo-mark.svg` | Brand mark — gradient hexagon |
| `logo-full.svg` | Full wordmark |
| `logo-white.svg` | White mark variant |
| `colors.css` | Color token CSS custom properties |
| `typography.css` | Type scale CSS custom properties |
| `spacing.css` | Spacing, radius, layout token CSS custom properties |
| `effects.css` | Shadows, glows, blur, motion token CSS custom properties |
