---
name: shire-post-design
description: Use this skill to generate well-branded interfaces and assets for The Shire Post (theshirepost.org), an evergreen rural-postal correspondence-house website. Contains design guidelines, colour and type tokens, fonts, assets, and a Bootstrap 5.3 UI kit for the public site.
user-invocable: true
---

Read the `README.md` file within this skill first — it contains brand-safety rules, content fundamentals (voice/tone/vocabulary), visual foundations, and the iconography approach. Then explore the other files:

- `colors_and_type.css` — every design token (colour, type, spacing, radii, shadows, motion). Import this before component CSS.
- `assets/` — wordmark, sealmark, paper-noise overlay. **No figurative artwork** is permitted; only typography, rules, seals, fleurons, and open-licence photography.
- `preview/` — design-system specimens (palettes, type scale, components). Useful as visual reference.
- `ui_kits/website/` — five-page Bootstrap 5.3 recreation of the public site (`index.html`, `apply.html`, `side-window.html`, `incorrect-mark.html`, `not-found.html`) plus `site.css`. The reference for any new page on the site.

## Hard rules

1. **Brand safety.** This site must not read as a Tolkien, *Hobbit*, *Lord of the Rings*, *Middle-earth* or fan-franchise property. No franchise names, places, characters, runes, ring inscriptions, maps, or visual signatures. No round green doors, single circular windows, dragon iconography, eye motifs, or stylised "Elvish" type. "Shire" is used only in its generic English sense.
2. **No emoji, ever.** Use Unicode typographic ornaments (`❦ ❧ ¶ § † ‡ ✦`) set in IM Fell English.
3. **No gradients, no backdrop-blur, no glassmorphism.** Flat paper, ink rules, and the occasional sealing-wax red accent.
4. **No fake AI/SaaS landing-page voice.** Read the Content Fundamentals section before writing copy. The Post speaks as the clerk of a small village post office: formal, warm, plainspoken, never twee.
5. **Open-source images and icons only.** Phosphor Icons (regular weight) from CDN for unavoidable functional cases; Unsplash / Wikimedia / public-domain for photography.
6. **No backend.** The PRD forbids authentication, authorisation, and data storage. "Login" and "apply" forms are static redirects to slip pages.
7. **Use `noindex, nofollow`** on every page. `robots.txt` is not a privacy mechanism.

## When invoked

If the user asks for design or production code without further context, ask:

- Which surface? (A new page on the public site, a new partial, an asset, or something else?)
- Is the work for production (Jekyll/Liquid/Bootstrap) or a throwaway mockup?
- Any photographic imagery to anchor it to, or should you fall back to typographic placeholders?

For visual artifacts (mocks, slides, prototypes), copy assets out and produce static HTML. For production code, copy assets into the Jekyll project and lift the tokens from `colors_and_type.css`.

Always check your draft against the brand-safety rules above before delivering.
