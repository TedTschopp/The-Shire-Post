# The Shire Post — Website UI Kit

A click-through high-fidelity recreation of the public site. Five pages cover the full public surface area called for by the PRD.

| Page | File | What it demonstrates |
|---|---|---|
| Home / The Counter | `index.html` | Masthead, shopfront nav, hero with sealmark, notice list, office-hours ledger, colophon |
| Apply / Post a letter | `apply.html` | Long-form application form (text inputs, textarea, select) — fully simulated, no submission |
| Side window | `side-window.html` | Fake login form (correspondent's mark + private word). On submit, redirects to the "incorrect mark" slip |
| Returned slip | `incorrect-mark.html` | The 401-equivalent. A tear-off slip telling the visitor the mark wasn't recognised. No real auth performed |
| No such pigeonhole | `not-found.html` | The 404. Postal metaphor: "return to sender — addressee unknown" |

## Stack notes

- Each page is plain HTML so it maps 1:1 to a Jekyll `_layouts/default.html` + page-specific includes. In production:
  - The masthead, nav, and colophon become `_includes/masthead.html`, `_includes/nav.html`, `_includes/colophon.html`.
  - `apply.html` and `side-window.html` become Liquid pages whose form `action` simply points at a static "incorrect mark" / "applied" slip page.
- **Bootstrap 5.3.3** is loaded from jsDelivr CDN. We use very little of it directly — only the grid + a few utilities (`d-flex`, `gap-*`, `mt-*`). Our own `site.css` overrides typography and `.btn`.
- **Phosphor Icons** are imported via CDN in `site.css` but the kit does not currently use any icons — typographic ornaments do the work.
- **No JavaScript**. The login submit is a plain `<form action="incorrect-mark.html" method="get">` — credentials never leave the page. This is intentional: no backend, no auth, no data storage.
- Every page sets `<meta name="robots" content="noindex, nofollow">`. The PRD notes `robots.txt` is not a privacy mechanism — `noindex` is.

## Brand-safety review (per PRD)

- ❌ No Tolkien/Hobbit/LotR names, places, characters, runes, ring inscriptions.
- ❌ No round green doors, single round windows, dragon imagery, eye motifs.
- ✅ "Shire" used only in its generic English sense in the wordmark; not in any place-name.
- ✅ All imagery is typographic (sealmark) or stippled placeholder (no figurative art at all in this kit). Real photographs are to be sourced from open-licence libraries per `assets/IMAGE_CREDITS.md`.

## Open questions for the user

1. The wordmark currently reads "The Shire Post" in IM Fell English. Acceptable, or should we workshop a more abstract mark?
2. The sealmark contains the phrase "BY · HAND · &amp; · BY · FOOT" as its outer arc text. Is this OK, or should it be a Latin tag, a date, or town initials?
3. The PRD calls for open-source photography. Do you have a preferred photographer / collection, or should we curate from Unsplash + Wikimedia?
4. The "office hours" indicator currently shows a live "open / closed" state based on day of week. Want it to be a real client-side check, or static text only?
