# The Shire Post — Design System

A design system for **The Shire Post** (theshirepost.org): an evergreen, tasteful site that gives visitors the impression of a quiet rural correspondence house and private postal office. The public surface should feel intentional and complete — like the front desk of a working village post — while revealing no private content.

**Stack the site is built on:** Jekyll + Liquid templates, styled with Bootstrap 5.3.x. Open-source images and icons only.

---

## ⚠️ Brand-Safety Guardrails (read first)

The Shire Post is inspired by **generic rural English postal heritage**: old village mailrooms, hedgerow lanes, wax seals, hand-stamped notices, parish ledgers, private letters. It must **not** read as Tolkien, *The Hobbit*, *The Lord of the Rings*, *Middle-earth*, or any related franchise.

- ❌ No franchise names, places, characters, runes, maps, ring inscriptions, or character likenesses.
- ❌ No franchise-specific quotes, storylines, or visual signatures.
- ❌ No round green doors, single circular windows, dragon iconography, eye motifs, or stylized "Elvish" type.
- ✅ Generic English-village postal imagery: pillar boxes, ledgers, wax seals (plain initials or fleurons only), envelopes, hedgerows, lanterns, field paths, parish notices.
- ✅ "Shire" is used only in its generic English sense (an administrative subdivision / county).

When in doubt: would this read at a National Trust property gift shop, or only at a fan convention? Aim for the former.

---

## Index

| File | What's inside |
|---|---|
| `README.md` | This file — overview, content & visual foundations, iconography |
| `colors_and_type.css` | All design tokens: colors, type scale, spacing, radii, shadows, semantic vars |
| `SKILL.md` | Agent Skill manifest (for Claude Code use) |
| `fonts/` | Webfonts (currently links to Google Fonts CDN; see Type section) |
| `assets/` | Logos, seal marks, iconography, decorative elements |
| `preview/` | Design-system cards (color swatches, type specimens, components) |
| `ui_kits/website/` | High-fidelity HTML/JSX recreation of the public site |

---

## Content Fundamentals

### Voice & tone

The Shire Post speaks like the **clerk of a small village post office** — formal but warm, plainspoken, never folksy, never twee. The site is the front desk: helpful, deliberate, slightly old-fashioned, never performing.

- **Person:** Mostly third person ("The Post"), occasionally first-person plural ("we keep the office open Tuesdays and Fridays"). Address the visitor as "you" only when necessary (forms, instructions).
- **Tense:** Present tense. The office is always currently open or currently closed — not "founded in" or "since."
- **Casing:** Sentence case for body and most headings. Title Case is reserved for proper notices ("Office Hours", "Notice to Correspondents") and for the masthead.
- **Punctuation:** Em dashes are welcome. Serial commas. Single space after periods. No exclamation marks except in the rarest civic notice.
- **Numbers:** Spell out numbers below ten in prose ("seven letters"); use figures for postal codes, dates, box numbers, and ledger entries.
- **Dates:** "Tuesday, 12th of March" or "12 March 2026" — long form, never m/d/y.
- **No emoji.** Ever. (Use stamps, seals, and ornaments instead — see Iconography.)

### Vocabulary

| Use | Avoid |
|---|---|
| Correspondent, sender, addressee | User, customer, member |
| Letter, parcel, dispatch, notice | Message, post, content |
| The Post, the Office, the Counter | The platform, the site, the app |
| Box, pigeonhole, drawer | Inbox, folder |
| Ledger, register, day-book | Database, log, archive |
| Wax, seal, frank, postmark | Verify, authenticate, sign in |
| Office hours | Availability |
| Hold for collection | Pending |
| In transit, posted, received | Sent, delivered, read |

### Sample copy

> **Office hours.** The counter is staffed Tuesdays and Fridays. Letters posted by the close of business on Friday will be franked the same evening.

> **Holding for collection.** A small number of parcels remain in pigeonhole 14 and may be claimed by their addressees on production of the proper mark.

> **Notice to correspondents.** The Post does not at present accept overseas parcels exceeding two pounds in weight. We regret the inconvenience.

> **A private door.** Beyond this counter lies the working office. Correspondents with standing arrangements may apply at the side window.

### What we never say

- "Welcome to our website."
- "Sign up for our newsletter."
- "Join the community."
- "Discover…", "Unlock…", "Experience…"
- Anything that sounds like a SaaS landing page.

---

## Visual Foundations

### Overall mood

Quiet, dry, warm. Paper and ink first; ornament second. Imagine the printed matter pinned inside the door of a village post office: a price list, an opening-hours card, a faded notice about parcel handling — all on cream stock, with a single deep red seal.

### Colour

A small, disciplined palette built around **paper**, **ink**, and **wax**. All swatches defined as OKLCH in `colors_and_type.css`. Saturations stay low (chroma ≤ 0.13). Nothing is pure white or pure black.

**Surfaces** — warm parchment whites
- `paper` `oklch(0.965 0.013 82)` — primary background. Like uncoated cream stock.
- `paper-deep` `oklch(0.93 0.018 80)` — sidebars, cards, table headers.
- `paper-edge` `oklch(0.88 0.022 78)` — borders, rules, the edge of a notice card.

**Ink** — warm blue-black, never pure
- `ink` `oklch(0.22 0.02 255)` — primary text.
- `ink-soft` `oklch(0.40 0.018 255)` — secondary text, captions.
- `ink-faint` `oklch(0.58 0.014 255)` — placeholder text, disabled.

**Wax** — sealing-wax red, the only saturated colour
- `wax` `oklch(0.43 0.13 28)` — seals, the masthead rule, primary buttons.
- `wax-deep` `oklch(0.34 0.11 28)` — pressed/hover state for `wax`.

**Hedge** — muted field green, used sparingly
- `hedge` `oklch(0.46 0.06 145)` — links on paper-deep, "office open" indicator, ledger ticks.

**Brass** — aged metal accent, used very sparingly
- `brass` `oklch(0.68 0.08 82)` — decorative ornaments, scroll dividers.

Backgrounds are flat colour. **No gradients.** Subtle paper texture is allowed as an extremely low-opacity SVG noise overlay (see `assets/paper-noise.svg`), but flat cream stock is the default and is preferred.

### Type

| Role | Family | Source | Notes |
|---|---|---|---|
| Display / masthead | **IM Fell English** | Google Fonts | 17th-c. English letterpress revival. Used for the masthead, page titles, large notices. Always set in `font-feature-settings: "liga", "dlig"`. Never below 28px. |
| Body serif | **Lora** | Google Fonts | Long-form reading. Notices, paragraphs, captions. Falls back to Georgia. |
| Mono / ledger | **JetBrains Mono** | Google Fonts | Postal codes, box numbers, dates in ledgers, form field labels. Lowercase + tabular-nums. |

Type scale: 12 / 13 / 14 / 16 (base) / 18 / 22 / 28 / 36 / 48 / 64. Line-height: 1.5 for body Lora, 1.15 for IM Fell English display.

Headings are set in **sentence case** in IM Fell English, with a subtle small-caps `eyebrow` of JetBrains Mono above (e.g. `ɴᴏᴛɪᴄᴇ ɴᴏ. 042`). Avoid heading weights above 500 — IM Fell carries the weight visually on its own.

### Spacing & layout

8-pt spacing scale: `2 / 4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 96 / 128`.

Layouts are **narrow and centred** — a single readable column with generous outer margin, like a printed handbill pinned to a noticeboard. Max content width 720px for prose, 1040px for forms and listings. Multi-column grids only when there is genuine tabular content (ledgers, hours tables).

**Rules and dividers** are the primary structural device. A 1-px `ink` rule beneath the masthead. Hairline `paper-edge` rules between notices. Never use cards-with-shadows where a hairline rule will do.

### Corners, borders, shadows

- **Radii:** `0` is the default. The Shire Post does not round things. The single exception is `radius-stamp: 2px` used on form inputs and primary buttons — barely there. Wax seals use `radius-full` (circles only).
- **Borders:** Always `1px solid var(--paper-edge)` or `1px solid var(--ink)`. Never dashed except for the cut-out edge of a tear-off slip (`--border-dashed: 1px dashed var(--ink-faint)`).
- **Shadows:** Almost none. One token only — `shadow-card`: a very soft `0 1px 0 var(--paper-edge), 0 8px 24px -16px rgba(34, 30, 28, 0.18)`. Reserved for the hovering notice that sits over a folded letter. Buttons and cards are flat.

### Animation & interaction

The Post moves like a clerk's hand: deliberately, briefly, and not very far.

- Durations: `100ms` (state changes), `200ms` (hover transitions), `400ms` (page-level reveals). Never longer than 400ms.
- Easing: a single curve, `cubic-bezier(0.2, 0.0, 0.0, 1.0)` — a confident settle. No springs, no bounces.
- Hover state for links: underline appears (or thickens from hairline to 2px). No colour change.
- Hover state for buttons: `wax` → `wax-deep`, no movement, no scale.
- Press state: 1px translateY down, restore in 80ms.
- No parallax. No scroll-jacking. No fade-in-on-scroll for marketing flourishes — only used sparingly for revealing a notice.

### Imagery

The Post's imagery is **photographic, warm, daylit, and quiet**. No illustrations of people. No franchise iconography. Subjects:

- Pillar boxes and post-office shopfronts (generic, modern or vintage).
- Old envelopes, wax seals (with plain initials, fleurons, or generic crests — never franchise sigils).
- Ledgers, blotters, ink pots, stamps and stamping equipment.
- Hedgerows, country lanes, drystone walls, gates, field paths.
- Hands holding letters (no faces, no full figures).

Tone: warm-grade colour with slight grain. Avoid hyper-saturated or HDR processing. If colour is hard to control, **fall back to duotone in `ink` + `paper`**.

Use open-licensed sources only (Unsplash, Wikimedia, public domain). Always credit in `image_credits.md`.

### Backgrounds and surfaces

Flat `paper`. Occasionally a `paper-deep` band for a sidebar or footer. Optional, very low-opacity paper texture overlay (`background-image: url(assets/paper-noise.svg); opacity: 0.4; mix-blend-mode: multiply`). Never used over imagery.

### Transparency & blur

The Post does not use frosted glass, glassmorphism, or backdrop-blur. Modals (e.g. the "incorrect mark" notice after a fake login) use an opaque `paper` card on a `rgba(34, 30, 28, 0.45)` dim. No blur.

### Layout fixtures

- A **masthead** sits at the top of every page, fixed in flow (not sticky): the wordmark "The Shire Post" centred in IM Fell English at ~48px, with a 1px `ink` rule below.
- A **colophon footer** with office hours, a postmark date, and the building's notional address. Always present.
- A small `paper-edge` rule separates body content from the colophon.

### Density

Generous. Body paragraphs at 16/24px reading size in Lora. List items at 14px with 12px vertical rhythm. Forms have 16-px label margins and 12-px input padding. Tables (the ledger) are denser — 13/20px JetBrains Mono.

---

## Iconography

The Shire Post uses **almost no icons.** A village post office does not have icons; it has stamps, rules, and printed glyphs. When iconography is required, follow this order of preference:

1. **Typographic ornaments and dingbats.** Unicode fleurons (`❦ ❧ ☙`), pilcrows (`¶`), section marks (`§`), daggers (`† ‡`), and ASCII rules (`———`). These are part of the typesetter's drawer and are always preferred. Set in IM Fell English at the surrounding font size.
2. **Phosphor Icons (regular weight, 1.5px stroke)** from CDN, for the unavoidable functional cases: a small envelope on a "post a letter" link, a key on a private door, a clock on office hours, a magnifying glass on search. Phosphor's regular weight reads as engraved/etched and pairs cleanly with serif type. Loaded from `https://unpkg.com/@phosphor-icons/web@2.1.1/src/regular/style.css` and used as `<i class="ph ph-envelope-simple"></i>`. Sized `1em` and coloured `currentColor`.
3. **Custom seal/postmark SVGs** in `assets/marks/`. These are circular postmark-style stamps — a date, a town name, a number — drawn with **plain typography arranged in a circle**, no figurative artwork. They are decorative, not functional, and never used as button glyphs.

**Substitution flagged:** This system links Phosphor Icons from CDN rather than bundling them. The set is open-source (MIT). If the site is to be served offline-capable, vendor the icon font into `fonts/`.

**Emoji are forbidden** anywhere in product UI. They do not belong in a Victorian post office.

**The Shire Post wordmark / sealmark** lives in `assets/`:
- `assets/wordmark.svg` — "The Shire Post" set in IM Fell English with a hairline rule.
- `assets/sealmark.svg` — circular postmark-style seal: "✦ THE SHIRE POST ✦ ESTABLISHED" with a central fleuron. The seal contains **no franchise iconography** — only typography, a date, and a fleuron.

---

## A note to the user

Built blind to your real brand assets — there is no logo file, no photography library, and no existing site to reference. Everything here is a first proposal grounded in the PRD's "rural village post" direction. **Please flag** anything that drifts toward a fantasy/franchise aesthetic so I can pull it back, and share any photographic or seal/stamp imagery you'd like to anchor the system to.
