# Redis Brand Design System

The single source of truth for the Redis brand: **developer-first, fast, confident.**
Tokens, components, an icon library, voice, and a presentation deck template.

> Built from the Redis Brand Brief. This project is the live, buildable expression of
> that brief — `styles/` (tokens + components), `assets/` (logo, icons, fonts),
> `preview/` (design-system cards), `decks/` (presentation template), and
> `ui_kits/` (high-fidelity recreations of Redis surfaces).

---

## 1. What this is & who it's for

The Redis Design System is the source of truth for everyone building on the Redis
brand — product marketing, sales/CS, engineers shipping demos, and the partner
ecosystem. It is **developer-first, fast, and confident.** Tokens, not pixels;
show, don't tell.

### Principles
1. **Fast feels good.** If it doesn't feel instant, it doesn't feel Redis.
2. **One signal, one moment.** Hyper red, TT Trailers, and the Yellow accent are loud
   on purpose — one at a time. One primary action, one display headline, one accent per view.
3. **Code is content.** Code blocks are hero imagery, not afterthoughts. Real, copyable
   snippets; default code to dark with Space Mono.
4. **Maker, not marketer.** Talk like a senior engineer, never like a sales deck.
5. **Tokens, not pixels.** If it isn't a token, it isn't on-brand.

### Sources
Built from the **Redis Brand Brief** plus the official brand assets supplied by the team:
- **Tokens + components** \u2014 the authoritative `tokens.css` and `components.css` (now
  `styles/tokens.css` + `styles/components.css`). These define the real button geometry
  (rounded rectangles), radius scale, semantic tokens (`--bg`, `--fg`, `--action`\u2026), and the
  full component set.
- **Logos** \u2014 official script wordmark + mark, one SVG per color (red / white / midnight / black).
- **TT Trailers** \u2014 the licensed display face (woff2 / woff / otf in `assets/fonts/`).
- **Icon library** \u2014 the official duotone + white icon set.

No production codebase or Figma file was attached, so the **UI kits** and the **deck template**
are representative recreations that apply the real system \u2014 not 1:1 copies of shipping screens.

---

## 2. Content fundamentals (voice & tone)

> **Full guidelines: [`redis-verbal-identity.md`](redis-verbal-identity.md)** (Verbal Identity v1.0).
> Also usable as a standalone Agent Skill — consult it for any Redis copy.

**Positioning: "Fast apps fast."** The word for speed is always **"fast," never "speed."**
We are the **Expert Builder** — we built the world's fastest in-memory database, and we talk
to developers as peers.

**Three voice attributes:**
- **Direct** — clear, candid, active. Cut fluff ("In order to" → "To"), get to the point, state
  the benefit. Not blunt or oversimplified.
- **Relatable** — informal, understanding, supportive. Write dev-to-dev; name the challenge, then
  the solution. Not slangy or chipper.
- **A little irreverent** — cocky, proud, cheeky. Used *selectively* (headlines, intros, social);
  dialed down in product UI. Not headstrong, verbose, or punny.

**Show, don't tell — name a concrete thing.**
- ✗ "Unleash the power of real-time data with our cutting-edge platform."
- ✓ "Reads at 1 million ops per second, with sub-millisecond P99."

### Conventions
- **Headlines:** sentence case — **with periods in decks, without periods on web/digital assets.**
- **Eyebrows / chips:** ALL CAPS, Space Mono, ≤12px. ("REAL-TIME", "OPEN SOURCE")
- **CTAs:** verb-first, no jargon — "Try Redis", "Get a demo", "Talk to an expert".
- **Numbers:** always concrete — "1.2M ops/sec" beats "massive throughput". Proof points:
  sub-millisecond performance, 99.999% uptime, Active-Active, 24/7 support from the people who build Redis.
- **Punctuation:** em dashes fine; Oxford comma; **never exclamation marks.**
- **Person:** "you" for the audience, "we" for Redis — avoid third-person "Redis" statements unless
  needed for clarity.
- **"Redis":** always spelled out and capitalized; **never a pun, verb, or personification**
  ("Redis, set, go" ✗); never "Redises". Abbreviate freely: docs, devs, apps, Gen AI.
- **Emoji:** never — let tone carry the mood.
- **Retired phrases:** "Real time, right now", "If it's real-time, it's Redis", "The real/best/
  original Redis." Prefer "See how fast feels" / "Get Redis from the ones who built it."

### AI copy prompt (paste as a system message)
> You write copy for Redis. Positioning: "Fast apps fast" — always say "fast," never "speed."
> Voice = Direct + Relatable, with a little irreverence on headlines/social (less in product):
> clear and active, dev-to-dev, confident and a little cocky, never corporate. Cut fluff; name the
> challenge then the benefit; use concrete numbers and real product names. Sentence-case headlines
> (periods in decks, none on web). "you" for the reader, "we" for Redis. Never exclamation marks,
> never emojis, never "Redis" as a pun or verb. See redis-verbal-identity.md for the full rules.

---

## 3. Visual foundations

**Overall vibe.** Confident, high-contrast, engineering-forward. Crisp white or deep
Midnight surfaces, one loud Hyper-red signal, code treated as hero imagery. Nothing
decorative for its own sake. The feeling target is *instant* — interactions resolve in a
single frame.

**Color.** Built on four families (all CSS vars in `styles/tokens.css`):
- **Hyper** (#FF4438 base / #D1281E rich) — primary actions and the single signature moment.
- **Midnight** (#091A23) — dark surfaces and primary text.
- **Dusk** — cool gray-blue neutrals for lines, muted text, sunken surfaces.
- **Accents** (Yellow #DCFF1E, Purple #C795E3, Sky #80DBFF) — one highlight at a time, sparingly.
Never invent colors; pull from the scale, or derive in OKLCH matching the existing chroma if a
tint is truly missing.

**Type.** Three families: **TT Trailers** (display — **always all-caps**, tight tracking, *marketing /
web / social headlines only*, ≤8 words — **never in presentation decks** (the deck template does not
use it; use Space Grotesk Medium 500 for all deck headlines), **never lowercase/mixed case, never**
body, and **never** falls back to Anton; apply only via the `.rd-display` class, which locks
`text-transform: uppercase` to the font), **Space Grotesk**
(everything else; **Medium 500 is the heaviest weight — never Bold/SemiBold** for headlines
outside the display spots), **Space Mono** (code, eyebrows, tags). Sentence-case
headlines ending in a period; eyebrows ALL CAPS ≤12px; never smaller than 24pt on slides.

**Spacing & layout.** 4px base scale (`--rd-space-*`). Generous whitespace; content sits on a
≤1200px max width with 24px gutters. Decks use a 1920×1080 canvas with a ~120px safe edge.

**Backgrounds.** Flat and committed — solid White, solid Midnight, or a full Hyper-red field
(covers/dividers only). **No bluish-purple gradients, no noisy textures, no decorative
illustration washes.** Imagery, when present, is real product UI or code — not stock photography.
Code blocks act as the primary "imagery."

**Corners & cards.** Radii from `--rd-radius-*`: small UI uses sm/md (8–12px), cards use lg
**Radii are small and squared:** xs 2, sm 4, md 5 (buttons + inputs), lg 8 (cards), xl 12 (CTA
bars), pill 999 (tags only). **Buttons are rounded rectangles — not pills.** Cards are a clean
white (or Midnight) surface with a 1px Dusk border and **no shadow**; on hover the border
darkens to `--fg`. Feature cards flip to a solid Midnight fill; accent cards to solid Yellow. No
colored left-border-accent cards (the one exception: toasts carry a 3px left accent rule).

**Borders over shadows.** The system leans on hairline borders (`--border` = Dusk-03 on light /
Dusk-07 on dark), not elevation. Shadows appear only on overlays (the modal uses
`0 24px 48px rgba(9,26,35,.25)`). Inputs focus to a Midnight border + a soft blue focus ring.

**Motion.** Fast and confident. Durations: fast 120ms, base 200ms, slow 360ms. Easing
`--rd-ease-out` (cubic-bezier(.16,1,.3,1)) for enters, `--rd-ease-in-out` for moves. Fades and
short translates — **no bounces, no decorative loops.** Hover = color shift (red deepens to rich)
or border darkens; press = `translateY(1px)`. Respect `prefers-reduced-motion`.

**Transparency & blur.** Used sparingly: modal scrims are Midnight at 55% with a 4px backdrop
blur. Otherwise surfaces are opaque.

**Theming.** Light by default; add `.theme-dark` to flip semantic tokens to Midnight. One theme
per surface — don't mix White and Midnight regions arbitrarily.

---

## 4. Iconography

- **Use the official Redis icon library — never hand-draw inline SVG icons.** Each icon is a
  64×64 SVG with baked-in colors. Two variants are provided: **duotone** (navy `#163341` shapes
  with a hyper-red `#FF4438` accent) for **light** backgrounds, and **white** for **midnight/dark**.
- Reference as an image and size with width/height — do not override the fill:
  `<img src="assets/icons/duotone/database.svg" width="48" alt="">` (light) /
  `assets/icons/white/database.svg` (dark).
- A curated working subset lives under `assets/icons/duotone/` and `assets/icons/white/`; the full
  200+ library (both variants) is in the source `All icons/` folder. See
  `assets/icons/manifest.json` for the installed list and naming.
- **No emoji** as icons. No unicode-glyph icons. Logos and the mark live in `assets/`.

---

## 5. Index (manifest of this project)

**Foundations / CSS**
- `colors_and_type.css` — convenience entry point (imports fonts + tokens).
- `styles/tokens.css` — colors, type, spacing, radius, motion. **Source of truth.**
- `styles/fonts.css` — font loading (Google Fonts + TT Trailers `@font-face`).
- `styles/components.css` — buttons, cards, forms, tags, code, table, toast, modal, CTA, nav.
- `styles/deck.css` — 1920×1080 slide system + White / Midnight / Hyper themes.

**Assets**
- `assets/redis-logo.svg` + `-white/-midnight/-black.svg`, `assets/redis-mark.svg` + variants —
  official wordmark + mark (script logo), one SVG per color. Hyper red on light, white on dark.
- `assets/icons/duotone/`, `assets/icons/white/` — official icon library (curated subset).
- `assets/icons/manifest.json` — icon library list + usage.
- `assets/fonts/` — licensed TT Trailers (installed: woff2 / woff / otf).

**Design-system cards** (shown in the Design System tab)
- `preview/*.html` — color, type, spacing, component, and brand specimens.

**Presentation**
- `decks/Redis Deck Template.html` — the deck template + sample layouts (see `decks/`).

**UI kits** (high-fidelity recreations)
- `ui_kits/redis-website/` — marketing site (home, product, pricing, docs).
- `ui_kits/redis-console/` — Redis Cloud / Insight-style management console.

**Meta**
- `CLAUDE.md` — project rules applied to every AI request here.
- `SKILL.md` — makes this folder usable as a downloadable Claude Agent Skill.
- `redis-verbal-identity.md` — full Redis verbal identity (voice, messaging, editorial style).
  Doubles as the `redis-verbal` Agent Skill — consult before writing any Redis copy.

---

## 6. Hard rules (do / don't)
- ✅ Tokens for every color/size/gap. ❌ No hardcoded hex.
- ✅ Library icons (duotone on light, white on dark). ❌ No hand-drawn icons.
- ✅ TT Trailers for marketing/web display only, **always all-caps** (via `.rd-display`). ❌ Never in decks, never lowercase, body copy, or redistributing the font.
- ✅ One accent, one primary action, one display headline per view.
- ✅ One theme per deck; text ≥24pt on slides. ❌ No mixing White + Midnight in one deck.
- ✅ Concrete numbers and real product names. ❌ No buzzwords or exclamation points.
