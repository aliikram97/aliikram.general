---
name: Ali Ikram — AI Specialist & Founder
description: A radar/air-traffic-control instrument scope that tracks Ali Ikram, IRF Technologies, and Decom Robotics as live contacts, not a marketing page.
colors:
  scope-ground: "#05080a"
  panel-surface: "#0a1215"
  phosphor: "#4ce096"
  phosphor-bright: "#a8ffce"
  amber: "#ffb020"
  cyan: "#6fd6ff"
  ink: "#93a8a0"
  ink-dim: "#5c6e68"
  ink-bright: "#eafaf1"
  grid-line: "rgba(76, 224, 150, .13)"
  grid-line-strong: "rgba(76, 224, 150, .3)"
  border: "rgba(76, 224, 150, .16)"
typography:
  display:
    fontFamily: "Titillium Web, sans-serif"
    fontSize: "clamp(30px, 3vw, 38px)"
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: "-.01em"
  headline:
    fontFamily: "Titillium Web, sans-serif"
    fontSize: "clamp(28px, 4vw, 42px)"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "-.01em"
  title:
    fontFamily: "Titillium Web, sans-serif"
    fontSize: "16px to 22px"
    fontWeight: 600
    lineHeight: 1.3
  body:
    fontFamily: "Titillium Web, sans-serif"
    fontSize: "14px to 16.5px"
    fontWeight: 400
    lineHeight: 1.65
  label:
    fontFamily: "IBM Plex Mono, monospace"
    fontSize: "10.5px to 13px"
    fontWeight: 400
    letterSpacing: ".08em to .12em"
rounded:
  none: "0px"
  full: "50%"
spacing:
  xs: "6px"
  sm: "12px"
  md: "24px"
  lg: "48px"
  section: "110px"
components:
  button-primary:
    backgroundColor: "transparent"
    textColor: "{colors.phosphor-bright}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "13px 20px"
  button-primary-hover:
    backgroundColor: "rgba(76,224,150,.1)"
    textColor: "{colors.phosphor-bright}"
  button-amber:
    backgroundColor: "transparent"
    textColor: "{colors.amber}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "13px 20px"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "13px 20px"
  card:
    backgroundColor: "{colors.panel-surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "22px to 28px"
---

# Design System: Ali Ikram — AI Specialist & Founder

## Overview

**Creative North Star: "The Radar Scope"**

The site is an air-traffic-control instrument, not a résumé page. Ali, IRF Technologies, and Decom Robotics are contacts held on a live scope; his track record is logged telemetry, not prose bragging. The world is a near-black instrument ground lit by a single restrained phosphor-green (grid lines, sweep, lock-on pulses), with amber reserved for the one primary action (email) and a thin cyan used only for secondary classification tags. Every panel is bracket-framed like a HUD readout: corner ticks, hairline borders, monospaced field labels in small caps-by-convention uppercase. This deliberately refuses the dark-navy-plus-neon-gradient "AI portfolio" default — there are no glows-for-glow's-sake, no gradient blobs, no card shadows; depth comes from grid density and border-brightness, not elevation.

The pairing of Titillium Web (display/body) and IBM Plex Mono (every label, field, timestamp, and status tag) does the genre work: Titillium Web reads as confident, geometric, human; Plex Mono reads as instrument telemetry. The system never mixes them within one text role — mono is reserved for data-plane text, Titillium Web for narrative-plane text.

**Key Characteristics:**
- Near-black scope ground with a single phosphor-green system accent; amber and cyan are the only other hues, each with one job.
- Bracket-cornered, hairline-bordered instrument panels everywhere — no shadows, no rounded corners except true circles (the scope, its blips, status dots).
- Mono type carries every label/field/status; display type carries only names, headings, and body prose.
- A live rotating radar sweep and pulsing lock-on blips are the site's one motion signature; everything else uses a plain scroll-reveal fade/rise.

## Colors

A near-monochrome instrument palette: one dominant phosphor-green system accent, two single-purpose secondary hues, and a narrow ink range for text — never bright, saturated, or gradient-heavy.

### Primary
- **Phosphor** (`#4ce096`): the system's one signature hue — grid lines, borders, sweep, bracket corners, status dots, li markers, active-state text. Used at full saturation only for small marks (dots, corners, `›` bullets); used as translucent tints (13%/16%/30% alpha) for grid lines and borders.
- **Phosphor Bright** (`#a8ffce`): the "locked" state of phosphor — primary CTA text/border, the hero's self-blip, link-hover color. Reserved for things that are actively focused or being interacted with.

### Secondary
- **Amber** (`#ffb020`): the single action color, used only for the one primary conversion action (Email me). Never used decoratively; its rarity is what marks it as "the ask."
- **Cyan** (`#6fd6ff`): secondary-track classification color — venture "Class:" labels, experience-log company names, contact-blip dot fill. Marks "identifying metadata about a tracked entity," distinct from phosphor's "system state."

### Neutral
- **Scope Ground** (`#05080a`): page background — the instrument's near-black chassis.
- **Panel Surface** (`#0a1215`): background for raised instrument panels (venture cards, file cards, skill categories, profile card).
- **Ink Bright** (`#eafaf1`): headings, h1/h2/h3, primary readout values.
- **Ink** (`#93a8a0`): body copy, default text color.
- **Ink Dim** (`#5c6e68`): secondary/mono labels, field names (`dt`), timestamps, section indices.
- **Grid Line** (`rgba(76,224,150,.13)`) / **Grid Line Strong** (`rgba(76,224,150,.3)`): the two standard border/rule opacities, used consistently instead of ad hoc alphas.
- **Border** (`rgba(76,224,150,.16)`): the default hairline border for cards, dividers, and section rules.

### Named Rules
**The One Signal Rule.** Phosphor-green is the only color allowed to represent system/active state (status dots, "Active" tags, lock-on pulses). Amber and cyan never substitute for it — amber means "act now," cyan means "this is what kind of thing you're looking at."

**The No-Glow-Without-Cause Rule.** Color glow (`box-shadow` with color, `filter` bloom) only appears on elements that are literally instrument lights: the scope dots, the lock-pulse animation. Text, panels, and buttons never get a decorative glow.

## Typography

**Display Font:** Titillium Web (with sans-serif fallback)
**Label/Mono Font:** IBM Plex Mono (with monospace fallback) — no separate body font; body prose also renders in Titillium Web.

**Character:** Titillium Web carries every narrative and human-facing string (names, headings, prose); IBM Plex Mono carries every piece of structured/tabular data (labels, coordinates, statuses, timestamps, classifications). The split is strict and semantic, not decorative — it is what makes the "telemetry" read work.

### Hierarchy
- **Headline** (600, `clamp(28px, 4vw, 42px)`, tight tracking `-.01em`): section titles (`.section-title`) — "Ventures," "Experience," "Featured Projects."
- **Display/Title** (600, `clamp(30px, 3vw, 38px)` down to 19–22px): hero H1, contact-panel H2, card H3 titles (venture, file, skill-category, log-entry).
- **Body** (400, 14px–16.5px, line-height 1.65): paragraph copy in About, venture cards, project descriptions; About-copy caps at 68ch, hero lede at 46ch, transmission copy at 42ch.
- **Label** (400, 10.5px–13px, letter-spacing .04em–.12em, uppercase where used): every mono field — nav links, `.role`, `.readout-fields`, venture-head status, file-class, skill-head, footer status, section-index subheads.

### Named Rules
**The Mono-Is-Data Rule.** If a string is a value, status, timestamp, coordinate, or classification tag, it renders in IBM Plex Mono, uppercase, with letter-spacing. If it's a name, sentence, or heading, it renders in Titillium Web. Never mix the two within a single string.

## Layout

The page is a single-column stack of full-bleed `<section>` blocks (`padding: 110px 0`, `70px 0` under 768px), each opening with a hairline `border-top` that acts as the only vertical section divider — there are no background-color section breaks. Content is capped by a shared `.container` (`max-width: 1240px`, `24px` side padding).

The hero breaks the single-column rule: `.hero-instrument` is a two-up grid (`minmax(0,1fr) minmax(280px,360px)`) — circular scope on the left, mono readout panel on the right — collapsing to one column under 860px (readout panel moves below the scope, blip positions re-tuned for the narrower scope). Ventures, files, and skills sections use `repeat(auto-fit, minmax(Npx, 1fr))` card grids (320px/360px/250px minimums) that reflow to single-column at narrow widths without an explicit breakpoint. About and the intro-transmission section use asymmetric two-column grids (copy + panel/video) that collapse to one column at 860px/800px respectively. The experience log uses a fixed `150px 1fr` timestamp-then-content grid, collapsing to one column at 700px.

Nav switches from a horizontal mono link row to a hamburger-toggled full-width dropdown at 768px (`.nav-toggle` becomes visible, `nav ul` becomes an absolutely-positioned panel with `.open` class toggled by JS). **This mobile breakpoint behavior is coded but not visually verified** — browser automation in this build session could not resize the viewport to confirm the collapsed layout renders correctly; treat the 860px/768px/700px rules as unverified until checked in a real narrow viewport.

Spacing is not on a strict 8pt grid but clusters around a small set of reused values: `12px`/`14px` (mono field gaps, small internal padding), `22px`–`28px` (card internal padding, grid gaps), `48px`+ (panel padding, hero scope padding), `110px` (section rhythm).

## Elevation & Depth

Flat by design — there is no `box-shadow` anywhere in the system except the two literal instrument-light effects (blip glow, lock-pulse ring). Depth and hierarchy are conveyed entirely through border brightness (`--border` → `--grid-line` → `--grid-line-strong`) and background-layer contrast (`--bg` vs `--bg-panel`), never through shadow or blur elevation.

### Named Rules
**The Flat-Instrument Rule.** Panels sit directly on the scope ground with a hairline border; hover states brighten the border and/or lift the element with `translateY(-2px to -4px)`, never add a shadow.

## Shapes

Sharp rectangles everywhere (`border-radius: 0` is the implicit default — no radius token is ever applied to cards, buttons, or panels). The one exception is true circles: the radar scope itself, contact blips, and status-indicator dots all use `border-radius: 50%`, reserved strictly for "things that are lit up on the instrument," never for cards or buttons.

Bracket-corner framing (`.bracket`, plus the hero's own corner pseudo-elements) is the system's signature device: two opposing L-shaped corner marks (1.5–2px phosphor border, partial opacity) laid over a hairline-bordered rectangle, used on cards, the hero instrument, and the contact panel to read as an "instrument panel" rather than a plain box.

## Components

### Buttons
- **Shape:** sharp rectangle, no radius, 1px solid border, mono label text, uppercase, letter-spacing `.08em`.
- **Primary** (`.btn`): transparent background, phosphor border, phosphor-bright text, `padding: 13px 20px`.
- **Amber** (`.btn.amber`): same shape, amber border/text — reserved for the single primary conversion CTA (Email me).
- **Ghost** (`.btn.ghost`): dim `--ink` text, `--border`-color border — used for secondary actions (View log).
- **Hover:** background tints to a 10% alpha of the button's own color; primary/amber also lift `translateY(-2px)`.

### Cards / Containers
- **Corner Style:** sharp (0 radius); bracket corner marks on most card types (venture, file, skill-category, profile-card, experience log-entry).
- **Background:** `--bg-panel` (#0a1215) on `--bg` (#05080a) — a one-step tonal lift, no shadow.
- **Border:** 1px `--border`, brightening to `--grid-line-strong` on hover; file-cards additionally carry a 2px phosphor top border as a signature accent.
- **Internal Padding:** 22px–28px.
- **Header convention:** every card type opens with a small mono "head" row (class/status/category label, right- or space-between-aligned, uppercase, `--ink-dim` or `--cyan`) before the title — this is the system's recurring "instrument readout header" pattern, not a one-off.

### Navigation
- **Style:** fixed top bar, translucent blurred scope-ground background (`rgba(5,8,10,.88)`, `backdrop-filter: blur(10px)`), hairline bottom border.
- **Typography:** mono, 12px, uppercase, `.12em` tracking.
- **States:** default `--ink`, hover `--phosphor-bright`.
- **Mobile:** below 768px, links collapse behind a hamburger (`.nav-toggle`) into a full-width dropdown panel; unverified in a real narrow viewport this session (see Layout).

### The Radar Scope (signature component)
The hero's circular instrument: four concentric ring guides, a crosshair, a 15°-stepped tick ring (masked to a thin annulus), and a continuously rotating conic-gradient sweep (`9s linear infinite`) as the sole primary-viewport motion. Three "contact blips" sit at fixed bearings — Ali at center (larger, phosphor-bright dot with a `lock-pulse` ring animation), IRF and Decom Robotics at fixed off-center coordinates (cyan dots, no pulse) — each with a mono tag label that fades/slides in on load. This is the one non-reusable, page-specific device in the system; it should not be miniaturized or reused as a generic decorative background.

## Do's and Don'ts

### Do:
- **Do** keep phosphor-green as the only color that signals system/active state; reserve amber for the single primary action and cyan for secondary classification tags only.
- **Do** render every label, timestamp, coordinate, and status in IBM Plex Mono, uppercase, with letter-spacing; keep names/headings/prose in Titillium Web.
- **Do** use hairline borders and border-brightness (not shadow) for elevation; hover states brighten borders and/or lift with `translateY`.
- **Do** frame instrument-style panels with bracket corner marks (`.bracket`) and lead each card with a small mono "head" row before the title, consistent with the existing card types.
- **Do** keep corners sharp (0 radius) everywhere except true circular "lit" elements (scope, blips, status dots).

### Don't:
- **Don't** add drop shadows, glassmorphism, or gradient blobs — depth comes from grid density and border alpha only, per the Flat-Instrument Rule.
- **Don't** introduce a second saturated accent color; the system deliberately runs on one dominant hue plus two single-purpose secondaries.
- **Don't** use rounded corners on cards, buttons, or panels — radius is reserved for circular instrument elements only.
- **Don't** reintroduce sequential sub-numbering (e.g. "SYS-01," "FILE-02") as a card-header convention — this pattern was flagged and removed twice during this build's review; card head labels are non-sequential category/status codes (e.g. `AI/ML`, `Class: Navigation`), never an invented ordinal sequence.
</content>
