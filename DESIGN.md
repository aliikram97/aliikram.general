---
name: Ali Ikram — AI Specialist & Founder
description: An executive's personal site built on restraint and typographic craft — warm off-white paper, a serif editorial voice, and a single navy action.
colors:
  bg: "#f5f0e0"
  ventures-bg: "#f9eecd"
  intro-bg: "#ffeebd"
  about-bg: "#f8e6b4"
  experience-bg: "#fbe6a7"
  projects-bg: "#f9e29f"
  skills-bg: "#fbe193"
  ink: "#17181a"
  ink-soft: "#5b5d5f"
  ink-faint: "#8b8d8e"
  line: "#dfdbd1"
  accent: "#16213e"
  accent-deep: "#0e1626"
  garnet: "#76290b"
  garnet-bright: "#a8452a"
  on-navy: "#eae6dc"
  white: "#ffffff"
typography:
  display:
    fontFamily: "Spectral, Georgia, serif"
    fontSize: "clamp(48px, 7vw, 86px)"
    fontWeight: 500
    lineHeight: 1.02
    letterSpacing: "-.015em"
  headline:
    fontFamily: "Spectral, Georgia, serif"
    fontSize: "clamp(30px, 4vw, 42px)"
    fontWeight: 500
    lineHeight: 1.15
    letterSpacing: "-.01em"
  title:
    fontFamily: "Spectral, Georgia, serif"
    fontSize: "17px to 26px"
    fontWeight: 500
    lineHeight: 1.25
  pullquote:
    fontFamily: "Spectral, Georgia, serif"
    fontSize: "clamp(20px, 2.4vw, 26px)"
    fontWeight: 400
    fontStyle: "italic"
  body:
    fontFamily: "Public Sans, -apple-system, sans-serif"
    fontSize: "14.5px to 18px"
    fontWeight: 400
    lineHeight: 1.65
  label:
    fontFamily: "Public Sans, -apple-system, sans-serif"
    fontSize: "11.5px to 13.5px"
    fontWeight: 400
    letterSpacing: ".03em to .06em"
  intro-heading:
    fontFamily: "DM Serif Display, Georgia, serif"
    fontSize: "24px"
    fontWeight: 400
    note: "Scoped exception for #intro's h2 only, user-confirmed. Not part of the system-wide Spectral/Public Sans pairing."
  intro-body:
    fontFamily: "Work Sans, -apple-system, sans-serif"
    fontSize: "14.5px"
    fontWeight: 400
    note: "Scoped exception for #intro's body copy only, user-confirmed. Not part of the system-wide Spectral/Public Sans pairing."
rounded:
  none: "0px"
  full: "50%"
spacing:
  xs: "10px"
  sm: "18px"
  md: "40px"
  lg: "64px"
  section: "120px"
components:
  button-primary:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.white}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "14px 28px"
  button-primary-hover:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.white}"
  button-text:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "0"
---

# Design System: Ali Ikram — AI Specialist & Founder

## Overview

**Creative North Star: "The Editorial Brief"**

The site reads like a well-set executive dossier, not an app or an instrument panel: warm off-white paper, near-black ink, and a single deep-navy accent held in reserve for the one thing the visitor is asked to do. A large serif name and role open the page; one editorial paragraph follows; then a filled navy button and a quiet underlined text link, side by side, with nothing else competing for attention. This is a deliberate double refusal — of the generic dark-navy gradient "AI portfolio" template, and of this project's own prior identity, a phosphor-green radar/ATC instrument scope (near-black ground, bracket-cornered panels, IBM Plex Mono labels everywhere). Neither survives in the built page; the current index.html carries no radar vocabulary, no glow, no bracket corners, no mono-labeled data plane.

Spectral (serif) carries every display, heading, and pull-quote moment — the hero name, section titles, card titles, the italic role line under the name. Public Sans, the U.S. federal government's typeface, carries every structural and body string — paragraphs, navigation, labels, buttons, facts — for its plain, institutional trust register rather than for warmth or personality. Hierarchy is built from type scale, hairline rules, and whitespace, never from color or shadow: hairline `1px solid` lines (`#dfdbd1`) stand in for every border, card, and divider the system would otherwise need, and generous section padding (120px between sections) does the work a panel or a card background would do elsewhere.

**Key Characteristics:**
- A warm cream-to-gold gradient wash across sections (`#f5f0e0` → `#f9eecd` → `#ffeebd` → `#f8e6b4` → `#fbe6a7` → `#f9e29f` → `#fbe193`, one flat hex per section, no CSS gradients), near-black ink, deep-navy for trust (`#16213e`/`#0e1626`), deep garnet for luxury (`#76290b`/`#a8452a`) — a two-accent system atop a warming neutral ramp, not a single flat paper tone.
- Spectral for display/heading/pull-quote text, Public Sans for everything structural — never mixed within a single string.
- Hairline rules instead of borders, cards, or shadows; whitespace and rule-lines carry hierarchy.
- Zero border-radius except true circular list-bullet dots; zero box-shadow anywhere in the system (garnet hover rings are crisp 1px outlines, not blurred glows).
- Embedded YouTube demo thumbnails are held desaturated at rest and restored to color only on hover/focus, so they never compete with the palette.
- The page closes on a deep-navy full-bleed band (Contact + footer) — the system's one "committed" color field, breaking the paper ground for a deliberate, richer closing moment.

## Colors

A near-monochrome paper palette carrying two reserved accents, each with one job: deep navy for trust (the primary action, the closing band), deep garnet for luxury (small repeated marks — rule lines, hover states, proof figures — never a fill except on the navy band).

### Primary
- **Deep Navy** (`#16213e`, deeper `#0e1626` for the closing band): trust color. Fills the primary button on the paper ground (`.btn` — "Get in touch") and the full-bleed Contact/footer band. Never used for body text or decoration on the paper ground.
- **Garnet** (`#76290b`, brighter `#a8452a` for use on navy): luxury color. Never a large fill on the paper ground — only small, repeated marks: the `.kicker-rule` before every section title, the hero location line, hover states on nav links/text-links/underlined links, and highlighted proof figures (`.stat`) inside Experience bullets. On the navy band it inverts to a small fill: the "Email me" button (`.btn.on-navy`).

### Neutral
- **Gradient wash**: each section carries its own flat background hex, warming as the page scrolls down toward the closing navy band: Hero/Nav `#f5f0e0`, Ventures `#f9eecd`, Introduction `#ffeebd`, About `#f8e6b4`, Experience `#fbe6a7`, Projects `#f9e29f`, Skills `#fbe193`. Project cards (`.file-card`) stay at the lightest tone (`#f5f0e0`, via `var(--bg)`) so they read as distinct objects against their section's deeper gold. This is a deliberate directional wash the user set section-by-section, not a CSS `linear-gradient` — each section is one flat, explicit color.
- **Ink** (`#17181a`): headings, the logo, hero name, card titles, primary readout values (fact-list right-hand values).
- **Ink Soft** (`#5b5d5f`): default body text color — paragraphs, ventures/about/log/skills copy, secondary button text.
- **Ink Faint** (`#8b8d8e`): section notes, timestamps, uppercase field labels — the system's "quiet metadata" tone on the paper ground.
- **Line** (`#dfdbd1`): every hairline rule, border, and divider on the paper ground — section-top rules, nav bottom border, card seams, fact-list rows, video-frame borders, skill-category underlines.
- **On Navy** (`#eae6dc`): body text and secondary link color on the navy closing band — a warm off-white, not pure white, so the band reads as one considered surface rather than an inverted paper page.
- **White** (`#ffffff`): text on the navy primary button (paper-ground context only).

### Named Rules
**The Two-Accent Rule.** Navy signals trust and carries the primary action; garnet signals luxury and never appears as a large fill except on the navy band itself. The two never substitute for each other — a hover state, a rule mark, or a highlighted figure is always garnet; a primary action is always navy (or garnet-on-navy, its one inversion).

**The Hairline-Not-Border Rule.** Structure is drawn with `1px solid var(--line)` rules, not with card backgrounds, box-shadow, or heavier borders. A section opens with a rule-top; a card seam is a shared 1px line, not an owned border; a divider is a line, not a background change.

**The Crisp-Not-Blurred Rule.** Where garnet marks a hover or focus state, it is a solid `box-shadow: 0 0 0 1px` ring or a solid underline/color change — never a blurred glow. Luxury reads through precision (a jeweler's edge), not through an ambient halo.

## Typography

**Display Font:** Spectral (with Georgia, serif fallback)
**Body Font:** Public Sans (with system-sans fallback)

**Character:** Spectral is editorial and slightly literary — it carries the hero name, section titles, card and log titles, and the italic pull-quote role line under the hero name. Public Sans is plain and institutional by design choice (it is the U.S. federal government's typeface) — it carries navigation, body paragraphs, buttons, timestamps, and every uppercase label. The split is strict: a heading or title never renders in Public Sans, and body/structural text never renders in Spectral.

**One deliberate exception:** the Introduction section (`#intro`) overrides both families locally — DM Serif Display for its `h2` ("Introduction"), Work Sans for its body copy — a section-scoped variant the user chose directly, not a system-wide pairing change. It does not extend past that section.

### Hierarchy
- **Display** (500, `clamp(48px, 7vw, 86px)`, line-height 1.02, letter-spacing `-.015em`): the hero `<h1>` only — "Ali Ikram."
- **Headline** (500, `clamp(30px, 4vw, 42px)`, letter-spacing `-.01em`): `.section-title` — Ventures, About, Experience, Featured Projects, Technical Skills.
- **Pull-quote** (400 italic, `clamp(20px, 2.4vw, 26px)`): the hero `.role` line ("AI Specialist and Founder") — the system's one italic moment.
- **Title** (500, 17px–26px): venture-column h3 (26px), log/file-card h3 (21px), contact h2 (36px), transmission h2 (24px), skill-category h3 (17px), the nav logo (20px).
- **Body** (400, 14.5px–18px, line-height 1.65): hero lede (18px, capped 56ch), about copy (17px, capped 62ch), venture/log/contact copy (15–16px), section-note and card copy (14.5px).
- **Label** (400, 11.5px–13.5px, letter-spacing .03em–.06em, uppercase where used): nav links, hero location line, log timestamps and company names, fact-list field names, footer.

### Named Rules
**The Serif-Is-Voice Rule.** If a string is a name, a section title, a card title, or the hero's role line, it renders in Spectral. If it is a paragraph, a label, a timestamp, or a navigation string, it renders in Public Sans. The two families never appear within the same text node.

## Layout

The page is a single-column stack of full-bleed `<section>` blocks (`padding: 120px 0`, `80px 0` under 768px), each opening with a hairline `border-top` as its only vertical divider — there is no background-color section break anywhere. Content is capped by a shared `.container` (`max-width: 1100px`, `32px` side padding).

The hero breaks the section-padding rule: `min-height: 92vh`, content flex-aligned to the bottom, capped at `max-width: 720px` — a large block of type sitting low in an otherwise empty viewport, with no competing graphic device. Ventures uses a three-column grid (`1fr 1px 1fr`) where the center column is a literal 1px vertical divider line, collapsing to a single stacked column (divider hidden) under 760px. The intro-video and About sections use asymmetric two-column grids (copy + video/facts), collapsing to one column at 800px. The experience log uses a fixed `160px 1fr` timestamp-then-content grid, collapsing to one column at 700px. Projects and Skills use `repeat(auto-fit, minmax(Npx, 1fr))` grids (360px / 220px minimums) that reflow without an explicit breakpoint; the Projects grid has no card border of its own — cards butt directly against a shared `1px` gap filled with `var(--line)`, so the grid itself draws every card seam.

Nav switches from a horizontal Public Sans link row to a hamburger-toggled full-width dropdown at 768px (`.nav-toggle` becomes visible, `nav ul` becomes an absolutely-positioned panel toggled by a JS `.open` class). This logic is carried over unchanged from the site's prior world; only color and type were restyled for this pass. **It is coded but not visually confirmed in a narrow viewport this session** — browser automation could not resize the window on this machine — so treat the 760px/768px/800px/700px collapse rules as a known, unverified gap rather than confirmed system behavior.

Spacing clusters around a small reused set rather than a strict 8pt grid: `10px`–`18px` (label gaps, row padding), `40px`–`48px` (grid gaps, venture-column padding), `64px` (about-grid gap), `120px` (section rhythm).

## Elevation & Depth

Flat with no exceptions: there is no `box-shadow` anywhere in the system. Sections carry their own flat background hex (the gradient wash, see Colors), but within any given section every surface still sits directly on that section's ground with no secondary panel lift — project cards are the one deliberate exception, sitting at the lightest wash tone against their section's deeper gold so they read as distinct objects. Hierarchy and separation are otherwise conveyed entirely by hairline rules (`var(--line)`) and whitespace.

### Named Rules
**The Flat Paper Rule.** Nothing in this system lifts off the page. There is no card background distinct from the page background, no shadow, and no blur except the nav bar's `backdrop-filter: blur(8px)` behind its translucent scroll bar, which exists for legibility under scrolled content, not for depth.

## Shapes

Sharp rectangles by default (`border-radius` is never applied to any card, button, panel, or frame). The one exception is true circles: the small 5px bullet dot before each experience-log list item (`border-radius: 50%`) is the system's only rounded mark, reserved for that single decorative use.

The recurring hairline rule — a 40px × 1px ink-colored line preceding every section title (`.kicker-rule`) — is the system's signature graphic device. It is a pure rule mark with no text and no label riding on it; it is not a category tag, status badge, or eyebrow, and should not be confused with one.

## Components

### Buttons
- **Shape:** sharp rectangle, no radius.
- **Primary** (`.btn`): filled navy background and matching 1px navy border, white text, `padding: 14px 28px`, 14px Public Sans. Used on the paper ground for "Get in touch."
- **Primary, on-navy** (`.btn.on-navy`): the primary button's one inversion — filled garnet background, deep-navy text, used only inside the Contact closing band ("Email me").
- **Text** (`.btn-text`): no fill, ink-colored text with a 1px ink underline (border-bottom), 14px, garnet on hover. Used for every secondary action on the paper ground — "View my work," and every `.venture-link`/`.file-link`.
- **Text, on-navy** (`.btn-text.on-navy`): warm off-white text with a faint translucent underline, brightening to `--garnet-bright` on hover — used only inside the Contact band (LinkedIn, Upwork).
- **Hover:** primary button gains a crisp `0 0 0 1px` garnet ring (paper ground) or off-white ring (navy band) and lifts `translateY(-1px)`; text links change color/underline to garnet, never opacity. Nothing changes shape or gains a shadow.

### Cards / Containers
- **Corner Style:** sharp (0 radius) throughout.
- **Background:** project cards hold the lightest wash tone (`#f5f0e0`, via `var(--bg)`) regardless of their section's deeper gold ground — the one place in the system a card intentionally differs from its section background.
- **Border:** project cards carry no border of their own; the `.files-grid` background is line-colored with a 1px gap, so the grid draws a shared hairline seam between cards instead of each card owning a border.
- **Internal Padding:** 40px (file-card), 48px (venture-column).
- **Video frame:** `padding-bottom: 56.25%` (16:9), 1px line-colored border, embedded YouTube iframe held at `filter: grayscale(1) contrast(1.05) brightness(1.02)` at rest, reverting to `filter: none` on hover/focus-within — the loud stock thumbnails stay quiet inside the single-navy palette until a visitor actually engages.

### Navigation
- **Style:** fixed top bar, translucent cream background (`rgba(245,240,224,.92)`, `backdrop-filter: blur(8px)`), 1px line-colored bottom border.
- **Typography:** Public Sans, 13px, uppercase, `.06em` tracking.
- **States:** default ink-soft, hover ink with an ink underline.
- **Mobile:** below 768px, links collapse behind a hamburger into a full-width dropdown panel with per-item top rules; carried-over logic, unverified in a real narrow viewport this session (see Layout).

### Fact List (signature component)
The About section's right-hand column: a top-ruled, row-divided list (`1px solid var(--line)` top and per-row bottom) pairing a small uppercase Public Sans label (11.5px, ink-faint, left) with its value (13.5px, ink, right, right-aligned). This label/value row pattern is the system's one recurring "data pair" device and appears only here — it is not replicated as a card-header convention elsewhere in the system.

### Proof Figures (`.stat`)
Inside Experience bullet points, the specific achievement figure (a percentage, multiplier, latency, range, or frame rate — e.g. "30%," "3x," "100ms") is wrapped in `<span class="stat">` and rendered in garnet, 600 weight, against the surrounding ink-soft sentence. This is the system's device for making proof scannable without a card, badge, or icon: the eye catches the number, the sentence supplies the claim it backs. Only the figure itself is garnet — never the surrounding sentence, and never applied to a figure that isn't a real, sourced result.

### Closing Band (Contact + Footer)
The only place the page leaves the paper ground: `#contact` and `footer` both sit on `var(--accent-deep)` (`#0e1626`), running as one continuous dark band to the bottom of the page. Inside it: a garnet `.kicker-rule`, white `<h2>`, `--on-navy` body copy, the garnet-filled `.btn.on-navy` primary action, `.btn-text.on-navy` secondary links, and `--on-navy` at reduced opacity for the meta lines (location, phone) and footer copyright. The footer's top border is a faint garnet line (`rgba(118,41,11,.3)`) rather than the paper-ground `--line` gray, so the band reads as one considered dark surface, not a light-system border pasted onto a dark background.

## Do's and Don'ts

### Do:
- **Do** keep navy for trust (primary actions, the closing band) and garnet for luxury (rule marks, hover states, proof figures) — never swap which job each accent does.
- **Do** draw structure with 1px hairline rules (`var(--line)` on paper, faint garnet on the navy band) instead of borders, card backgrounds, or shadows — per the Hairline-Not-Border and Flat Paper Rules.
- **Do** hold embedded video thumbnails at `grayscale(1) contrast(1.05) brightness(1.02)` and restore full color only on hover/focus-within, so stock demo footage never fights the palette.
- **Do** keep corners sharp (0 radius) everywhere except the true circular log-entry bullet dot.
- **Do** use an en dash for date ranges ("2023 – 2024"), not a comma or an em dash; this is standard range typography already in use throughout Experience.
- **Do** keep visible copy free of em dashes and of AI-writing tells — buzzwords, hedge phrases, formulaic constructions — as a standing content constraint for any future copy edits on this site, confirmed clean at the last review.
- **Do** keep garnet hover/accent marks crisp and solid (a 1px ring, a color change, an underline) per the Crisp-Not-Blurred Rule — never a blurred glow.

### Don't:
- **Don't** add drop shadows, CSS `gradient()` functions, glassmorphism, or a secondary panel background — the system is flat by design. The section-to-section color wash is a sequence of flat hexes, not a rendered gradient; don't blend it into one with a CSS gradient.
- **Don't** extend the Introduction section's DM Serif Display / Work Sans pairing to any other section — it is a scoped, one-section exception, not a system-wide pairing change.
- **Don't** let garnet become a large fill on the paper ground, and don't let navy appear as body text or decoration there either — each accent's one job (trust-action / luxury-accent) is what keeps two colors from reading as clutter. Garnet only fills on the navy band (`.btn.on-navy`).
- **Don't** use rounded corners on cards, buttons, panels, or frames — radius is reserved for the one circular list-bullet mark.
- **Don't** reintroduce eyebrow, kicker-label, or category-tag text (e.g. a "venture-tag" or "file-tag" line above a title) — nine such tags were built, flagged as a banned kicker-label pattern in review, and removed entirely rather than relabeled; project and venture titles carry their own meaning without a tag riding above them. This is a defect the build carried and corrected, not a component to reintroduce.
- **Don't** apply `.stat` garnet styling to a figure that isn't a real, sourced achievement — it's a proof device, not decoration.
</content>
