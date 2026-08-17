# Sehal — Brand Document

> **Version 1.0.**
> This is the source of truth for Sehal's visual identity. Anything that disagrees with it
> is out of date.
>
> The companion visual board is at **[sehalapp.github.io/brand](https://sehalapp.github.io/brand/)**;
> production vectors are in [assets/](./assets/).

---

## 1. What Sehal is

Sehal (`sehal.app`) is a **mobile-first SaaS platform for small and medium businesses** —
sales, customers, invoices, payments, CRM, financials and daily operations in one app.

**Positioning.** For the owner of a small or medium business, Sehal is the operating app
that turns sales, customers, invoices and payments into one straight line — so the day
runs itself instead of being reconstructed at night.

**Tagline.** *The easiest way to manage your business.*

### 1.1 Brand idea

**Control · Flow · Simplicity.**

| | Means | Shows up as |
|---|---|---|
| **Control** | The owner can see and change anything, at any moment | Plain numbers, no hidden state, one primary action per screen |
| **Flow** | The work moves in one continuous line, nothing dropped in the handoff | The mark's constant path width; four-tap task completion |
| **Simplicity** | A non-technical shopkeeper is fluent on day one | No jargon, no configuration before value, generous whitespace |

### 1.2 Personality

Smart · powerful · premium · serious · technological · international · confident · minimal.

The test: **would this sit credibly beside Stripe, Linear or Vercel, and still be
operable by someone who has never used a SaaS product?** If a decision fails either
half, it is wrong.

---

## 2. Logo

The mark is a **rounded-square tile with an interlocking S cut out of it**. Two strokes
pass through each other and close into the letter — a link, not a letter drawn once. It
says the parts of a business are joined: a sale is already an invoice, an invoice is
already a balance.

The artwork is final. Refinement is geometric only; do not redesign the idea.

### 2.1 Construction

| Parameter | Value |
|---|---|
| Tile | `682.5 × 682.5` — square |
| Corner radius | `102.32` — **15 % of the tile** |
| Counter (the S) | **open** — cut out, takes the ground colour |
| Colours in the artwork | **one** — Sehal Green |
| Wordmark cap height | `627` |
| Mark height | `1.089 × cap height` |
| Mark → wordmark gap | `127.55` (`0.187 × mark height`) |
| Lockup ratio | **4.155 : 1** |

**The counter is the single most important fact about this mark.** The S is not painted
on; it is absent. The mark is one shape in one colour, and whatever sits behind it shows
through the letter. That is why §2.5 forbids green grounds, mid-tones and photographs —
they do not fail cosmetically, they erase the S.

### 2.2 Assets

All in [`assets/`](./assets/), generated from the masters in
`design/assets/{icon,logo-light,logo-dark}.svg`. The wordmark is **outlines**; no live text.

| File | Use |
|---|---|
| `sehal-logo-horizontal.svg` / `-inverse.svg` | **Primary lockup.** Default in every context |
| `sehal-logo-horizontal-mono.svg` | Single-ink (`currentColor`) |
| `sehal-logo-stacked.svg` / `-inverse.svg` | Narrow or square slots |
| `sehal-mark.svg`, `sehal-mark-mono.svg` | Standalone mark — open counter |
| `sehal-wordmark.svg` / `-inverse.svg` | Beside a partner logo, or in running text |
| `sehal-appicon.svg`, `sehal-appicon-light.svg` | 1024² app icon — counter **filled**, square |

**Lockup metrics** (so it can be rebuilt, never re-eyeballed):

- Horizontal: mark and wordmark share a baseline box; gap = `0.187 × mark height`.
  Total ratio **4.155 : 1**.
- Stacked: mark height = `1.465 × cap height`, gap = `0.293 × cap height`, both centred.

### 2.3 Colour of the mark

The tile is **Sehal Green `#2FBF71`** on every ground. It does not invert and does not
shift between themes. The wordmark is the only part that flips: **Slate 900 `#0F172A`** on
light grounds, **Slate 50 `#F8FAFC`** on dark.

In single-ink contexts the whole lockup is one colour and the counter still reads, because
it is a hole rather than a second ink.

### 2.4 Clear space and minimum size

**Clear space = ¼ of the mark height** on all four sides — `170.6` units at master scale.
The mark is square, so it sets the measure; no cap-height arithmetic is needed. Nothing —
type, rule, image edge, another logo, the pattern — enters that band.

| Asset | Screen | Print |
|---|---|---|
| Horizontal lockup | **116 px** wide | 30 mm |
| Stacked lockup | 76 px wide | 20 mm |
| Mark alone | **28 px** | 7 mm |

Below 28 px the cut counter closes up and the tile reads as a plain green square. Under
28 px, use the mark at 28 px inside a padded container — never a shrunken lockup.

### 2.5 Don'ts

1. **Never place the mark on green.** The counter fills in and the S disappears entirely.
2. **Never place it on a mid-tone, a gradient or a photograph.** The open counter needs a
   flat plate to read against — use Slate 950 or Slate 50.
3. Don't fill the counter to "fix" a bad ground. The only artwork with a filled counter is
   the app icon, where there is no ground at all.
4. Don't recolour the tile. Sehal Green, or one ink colour.
5. Don't stretch, squash, skew or rotate. Scale proportionally only.
6. Don't add shadow, glow, bevel, outline, gradient or any 3D treatment.
7. Don't re-typeset the wordmark or rebuild the lockup by hand — see §4.

---

## 3. Colour

Six brand colours. One of them is green; the other five are the room it stands in.

### 3.1 Brand palette

| Role | Hex | Job |
|---|---|---|
| **Sehal Green** | `#2FBF71` | The only accent. Primary actions, the mark, the one thing on screen that wants to be pressed. Never two jobs on one view. |
| **Slate 950** | `#020617` | Primary dark ground — app icon, hero, presentation, business card. Also the ink that sits *on* green. |
| **Slate 900** | `#0F172A` | Primary ink on light grounds; raised surface on dark grounds. |
| **Slate 600** | `#475569` | Secondary text on light. Labels, captions, metadata. |
| **Slate 50** | `#F8FAFC` | Light ground, and the ink on dark grounds. |
| **White** | `#FFFFFF` | Cards and sheets raised off Slate 50. Not a page ground. |

**Slate + Green is the signature combination.** Prefer dark slate grounds with the green
mark. On green grounds, text and marks are **Slate 950 — never white**.

### 3.2 Required derivative — Green 700

`#2FBF71` fails as text on every light ground. Light mode still needs a green for links,
active tab labels and inline emphasis, so the system defines exactly one derived tint:

| Token | Hex | Derivation | Measured |
|---|---|---|---|
| **Green 700** | `#1A7F4F` | Same hue (147.5°) and saturation as Sehal Green, lightness 0.467 → 0.32 | **4.79:1** on Slate 50 · **5.01:1** on White |

It is **text-only**. Fills, the mark and the app icon stay `#2FBF71` in both modes, so the
brand colour never shifts. On dark grounds, green text is `#2FBF71` itself (8.46:1), or
`#5FD693` (11.07:1) where it sits inside a busy card.

### 3.3 Interface scale

Not brand colours — the intermediate slates the UI needs for borders, disabled states and
dark surfaces. Extend here; never by inventing a new hue.

`50 #F8FAFC` · `100 #F1F5F9` · `200 #E2E8F0` · `300 #CBD5E1` · `400 #94A3B8` ·
`500 #64748B` · `600 #475569` · `700 #334155` · `800 #1E293B` · `900 #0F172A` ·
`950 #020617`

### 3.4 Measured pairings

WCAG 2.1, computed **2026-08-16**. Body text must clear 4.5:1; text at 24 px+ or 19 px
bold must clear 3:1.

| Foreground | Ground | Ratio | |
|---|---|---|---|
| Slate 950 `#020617` | Sehal Green | **8.46:1** | ✅ use this on green |
| Slate 900 `#0F172A` | Sehal Green | **7.49:1** | ✅ |
| White `#FFFFFF` | Sehal Green | **2.38:1** | ❌ never white on green |
| Sehal Green | White | **2.38:1** | ❌ green is not a light-mode text colour |
| Sehal Green | Slate 50 | **2.28:1** | ❌ |
| Sehal Green | Slate 950 | **8.46:1** | ✅ green text is a dark-mode privilege |
| Sehal Green | Slate 900 | **7.49:1** | ✅ |
| Slate 900 | Slate 50 | **17.06:1** | ✅ |
| Slate 600 | Slate 50 | **7.24:1** | ✅ |
| Slate 50 | Slate 900 | **17.06:1** | ✅ |
| Green 700 `#1A7F4F` | Slate 50 | **4.79:1** | ✅ |

---

## 4. Typography

Two families. No third.

| Role | Family | Designer | Weights | Licence |
|---|---|---|---|---|
| **Brand & headlines** | **Vend Sans** | Bloom Type — Baptiste Guesnon & Bold Scandinavia | Medium 500, SemiBold 600 | SIL OFL 1.1 |
| **Interface & body** | **Manrope** | Mikhail Sharanda | Regular 400, Medium 500, SemiBold 600 | SIL OFL 1.1 |

**Vend Sans** is variable `300–700` (v1.611); the brand uses 500/600. It carries a
**slashed zero** (`zero`), `tnum`, `case`, `frac` and two stylistic sets.

**Manrope** is variable `200–800` (v4.504); the brand uses 400/500/600. Semi-condensed,
so a dense table fits a phone without dropping to a smaller size. `tnum` verified present
and decimal columns align — measured 2026-08-17.

**Why these two sit together:** Vend Sans' x-height is `0.546 em`, Manrope's is `0.540 em`
— near-identical, so display and body align optically with no per-face correction. Vend
Sans' cap height is `0.700 em`.

**Both must be bundled and actually loaded**, not left to a system fallback. Vend Sans is
**not on any CDN** — it ships from Bloom Type's release, so the font file must be vendored
alongside the product, not linked.

**The wordmark is set in Manrope**, not in the display face. The exact settings from the
master artwork:

| Setting | Value |
|---|---|
| Family | **Manrope** |
| Style | **ExtraBold** (800) |
| Size | 860 pt |
| Leading | 1032 pt |
| Tracking | **−37** |

It is then **converted to outlines**, and the outlines are the logo.

> ⚠️ **Do not rebuild it by re-setting the type.** Manrope ships in several builds and they
> do not agree: re-setting these exact values using the Google Fonts variable build renders
> roughly 10 % wider than the artwork. The settings above document what was used; they are
> not a recipe for regenerating it. **Use the file.**

### 4.1 Scale — ratio 1.25

| Step | Size / line | Family & weight | Tracking |
|---|---|---|---|
| Display 1 | 52 / 54 | Vend Sans 600 | −3.5 % |
| Display 2 | 36 / 40 | Vend Sans 600 | −3 % |
| Heading | 26 / 31 | Vend Sans 600 | −2.5 % |
| Subhead | 20 / 26 | Vend Sans 500 | −2 % |
| Body | 16 / 26 | Manrope 400 | 0 |
| Small | 14 / 22 | Manrope 400 | 0 |
| Label | 11 / 16 | Manrope 600 | +14 %, uppercase |

Nothing between steps. If a size feels wrong, the problem is weight or spacing.

### 4.2 Rules

- Tracking is a function of size: negative and increasing with size; uppercase labels
  reverse it to +14 %.
- **`tabular-nums` always** in tables, totals and any column of figures.
- **Turn on Vend Sans' slashed zero (`zero`) wherever a figure can be mistaken for a
  letter** — reference codes, invoice numbers, one-time codes. This is the disambiguation
  Manrope cannot provide, so codes set in the display face get it for free.
- **Never rely on glyph shape alone in an identifier a user reads back aloud.** `I`/`l` are
  plain stems in Manrope — as they are in most grotesques. Space or group such codes, or
  restrict the alphabet that generates them.
- The wordmark is **not type**: it is artwork. Never set live, never letterspaced.

---

## 5. Shape and space

| Token | Value | Use |
|---|---|---|
| `radius-xs` | 6 px | Chips, tags |
| `radius-sm` | 10 px | Buttons, inputs |
| `radius-md` | 14 px | Cards |
| `radius-lg` | 20 px | Sheets, modals |
| `radius-full` | 9999 px | Pills, avatars |
| App icon corner | 22.37 % | Apple squircle — applied by the OS, never baked in |

**Depth is carried by a 1 px border and a surface step — never by a shadow.** No bevels,
no glassmorphism, no gradients, no 3D. Flat, geometric, generous whitespace, precise grids.

Minimum touch target 44 px. One primary action per view.

---

## 6. Pattern and border

### 6.1 Derivation

The mark is an **S** of constant width that never thins through a turn (§2.1). The pattern
is that same S repeated and **interlocked** — each link hooks through the next, so the
chain reads as one continuous run rather than a row of separate marks.

The **border** is not a second device. It is the same drawing at a different crop: one row
of the chain instead of a field.

Master artwork: `design/Asset 1.svg` (Illustrator pattern swatch). The three paths in that
file are one link at x-offsets `−22.65`, `77.35`, `177.35` — i.e. the same link spaced
`100` apart, with a neighbour either side so the tile clips complete.

### 6.2 Geometry

One unit governs everything: the **link `L`**.

| Parameter | Value |
|---|---|
| Horizontal repeat | `L` |
| Vertical repeat | `L` (square tile) |
| Chain band within the tile | middle `0.57 L`; the rest is clear |
| Tile | `L × L` |
| Reference tile | `100 × 100` at `L = 100` |

Tile it at a fixed `L` — never stretch it to fit a box. A non-uniform scale destroys the
constant width, which is the one thing the pattern exists to say.

### 6.3 Densities

Scale the tile; never re-draw it.

| Density | `L` | Fill | Use |
|---|---|---|---|
| **Coarse** | 100 | Sehal Green | Covers, slide backs, the border band |
| **Medium** | 55 | Slate 700 | Texture on a Slate 900 surface |
| **Fine** | 30 | Green @ 55 % | Edges, card corners |
| **Backdrop** | 120 | Green @ 11 % | Behind headlines only, or the empty half of a layout |

**Never two densities in one composition.**

### 6.4 Rules

- **Solid, never outlined.** The chain is a filled ribbon at one weight — no stroke, no
  gradient, no drop-out.
- **Tint with group opacity, not per-path opacity.** The links overlap where they
  interlock; per-path alpha doubles up at those crossings and prints a visible lattice.
  Set `opacity` on the group (or change the fill), never `fill-opacity` on each path.
- **Never behind body text** — only behind headlines, in the empty half of a layout, or
  as a band.
- Never rotate the chain to a diagonal. It runs horizontally, or vertically at exactly 90°
  for an edge.

### 6.5 The border

A band **one link (`L`) deep**, full-bleed, carrying the coarse density at 55 %. Rotate it
90° for a vertical edge.

**Where it may go.** The top or bottom edge of a cover, slide or email header; the leading
edge of a feature card, where it replaces the accent rail; a full-bleed divider between
two sections; the reverse of the business card.

**Where it may not.** All four sides as a frame — it becomes ornament and the composition
loses its direction. Never around the logo (it enters the clear space of §2.4), never
between rows of a table, never behind running text.

---

## 7. Brand principles

1. **One line, end to end.** The product's promise and the mark's geometry are the same
   claim: the work moves through without being dropped. Anything that introduces a seam —
   a re-entry, a reconciliation, a second source of truth — is off-brand.
2. **Green is a verb.** It marks the one thing that moves the business forward. If two
   things on a screen are green, one of them is wrong.
3. **Contrast is measured, not eyeballed.** Record the ratio next to the rule that
   depends on it, with a date, so the next person cannot undo it by accident.
4. **Depth comes from a border, not a shadow.** Flat is a constraint, not a style —
   it keeps the interface legible on a cheap phone in daylight.
5. **The palette is authored, not generated.** Every value in §3 is chosen and measured.
   Editing an individual token to make one screen look better is a bug, not a customisation.

---

## Appendix — asset index

```
brand/
  BRAND.md            this document — the source of truth
  index.html          the visual board (self-contained, fonts embedded)
  assets/
    sehal-logo-horizontal.svg          sehal-logo-horizontal-inverse.svg
    sehal-logo-horizontal-mono.svg
    sehal-logo-stacked.svg             sehal-logo-stacked-inverse.svg
    sehal-mark.svg                     sehal-mark-mono.svg
    sehal-wordmark.svg                 sehal-wordmark-inverse.svg
    sehal-appicon.svg                  sehal-appicon-light.svg
```
