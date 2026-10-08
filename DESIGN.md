---
name: Deadweight Removal
description: One-page phone-first pitch site for a South Jersey junk removal crew, built out of their own logo.
colors:
  navy: "#0f1b30"
  navy-2: "#162745"
  navy-3: "#21365c"
  navy-glow: "#1b3157"
  steel: "#dfe6ef"
  steel-2: "#c5d1df"
  steel-ink: "#46566d"
  chrome: "#eef3f9"
  mist: "#a8b8cd"
  blue: "#2694f1"
  blue-deep: "#1462c4"
  blue-hover: "#1a70d8"
  blue-ink: "#0f4fa3"
  spark: "#8cc6ff"
  white: "#ffffff"
typography:
  display:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(2.55rem, 11.2vw, 5.6rem)"
    fontWeight: 900
    lineHeight: 0.98
    letterSpacing: "-0.01em"
  headline:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(2.1rem, 9vw, 4rem)"
    fontWeight: 900
    lineHeight: 0.98
    letterSpacing: "-0.01em"
  claim:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(1.65rem, 7.6vw, 3.4rem)"
    fontWeight: 900
    lineHeight: 1.08
    letterSpacing: "-0.01em"
  title:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(1.25rem, 5.6vw, 1.6rem)"
    fontWeight: 900
    lineHeight: 1.05
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.55
  lead:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(17px, 4.7vw, 20px)"
    fontWeight: 400
    lineHeight: 1.45
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "13.5px"
    fontWeight: 800
    letterSpacing: "0.06em"
rounded:
  focus: "6px"
  control: "14px"
  card: "28px"
  round: "50%"
spacing:
  gutter-phone: "20px"
  gutter-desk: "32px"
  gap: "12px"
  section-top: "34px"
  section-bottom: "56px"
  container: "1180px"
components:
  button-primary:
    backgroundColor: "{colors.blue-deep}"
    textColor: "{colors.white}"
    rounded: "{rounded.control}"
    padding: "0 22px"
    height: "58px"
  button-primary-hover:
    backgroundColor: "{colors.blue-hover}"
  button-secondary:
    backgroundColor: "rgba(15,27,48,.55)"
    textColor: "{colors.chrome}"
    rounded: "{rounded.control}"
    padding: "0 22px"
    height: "58px"
  button-secondary-hover:
    backgroundColor: "{colors.navy-2}"
  service-row:
    textColor: "{colors.navy}"
    typography: "{typography.title}"
    padding: "18px 2px"
    height: "76px"
  service-go:
    backgroundColor: "{colors.blue-deep}"
    textColor: "{colors.white}"
    rounded: "{rounded.round}"
    size: "44px"
  text-preview-card:
    backgroundColor: "{colors.white}"
    rounded: "{rounded.card}"
    padding: "22px 22px 26px"
---

# Design System: Deadweight Removal

Everything lives in one file: `index.html`. Colors and the radius are CSS custom properties in the `:root` block at the top of `<style>`; motion and physics are in the `DW` object at the top of `<script>`. Edit those two places before touching anything else.

## Overview

**Creative North Star: "The Chains Come Off"**

The page is built from the client's own logo: a chrome strongman snapping steel chains over a pile of concrete chunks, electric blue light, navy night. The logo's materials are the page's materials. Rubble piles (canvas) sit at the top and bottom of the page with the cut-out logo standing in them. Sagging steel chains (canvas) join every section. Between them, the copy is flyer-loud: heavy uppercase headings, plain sentence-case body, the phone number everywhere.

It is phone-first and built to be acted on. Every primary action is a full-width 58px button. Every service row opens a pre-filled text message. A sticky Text/Call dock covers the space between the hero and closing buttons on phones. Motion is physical. Pointer and touch shove the pile and the chains, and a tap flicks a chunk away. All of it stops under reduced-motion.

**Key Characteristics:**
- Navy night ground, one steel-light section, one electric-blue band. That three-tone sequence is the page rhythm.
- Heavy uppercase system sans for display, sentence case for body.
- Two canvas signatures: the rubble heap with the logo and chain seams whose fill follows the chain.
- One button component, two variants, used everywhere.
- Real facts only. The phone number is the only call to action.

## Colors

Navy dominates, steel lightens, electric blue does the work. All values come from the logo (navy vignette, "REMOVAL" blue, brushed chrome).

### Primary
- **Removal Blue** (`blue`): taken from the logo's "REMOVAL" lettering. Used for the accent words in headings ("dead weight.", "Removal"), step numerals, icons on navy, focus rings, button borders and the wordmark's REMOVAL line.
- **Deep Blue** (`blue-deep`): fill for primary buttons, the service arrow discs and the whole promise band. Use it where white text has to sit on blue. `blue-hover` is its hover state only.
- **Blue Ink** (`blue-ink`): blue for icons on the steel section, where Removal Blue is too light.
- **Spark** (`spark`): pale blue for the chain-link icons in the promise band and the rising dust motes in the heaps.

### Neutral
- **Navy Night** (`navy`): page ground, hero, How, close and footer. Also `theme-color` and `--ink` (the text color on steel).
- **Raised Navy** (`navy-2`, `navy-3`): secondary-button hover and the scrollbar thumb.
- **Navy Glow** (`navy-glow`): center of the radial gradient behind the hero and close heaps (the glow comes from the bottom).
- **Steel** (`steel`): ground of the services section. **Steel Rule** (`steel-2`): the 2px dividers between service rows. **Steel Ink** (`steel-ink`): secondary text on steel.
- **Chrome** (`chrome`): primary text on navy. **Mist** (`mist`): secondary text on navy.

### Named Rules
**The Never-Black Rule.** The darkest ground is Navy Night (`#0f1b30`). Never use `#000`. Shadows are tinted navy (`rgba(3,8,20,…)`).

**The Three-Ground Rule.** Sections use only navy, steel or deep blue as their ground. A new section picks one of these and gets a chain seam above and below it.

## Typography

**Display Font:** system sans stack (`--font`: -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial)
**Body Font:** same stack

**Character:** this is the owner's chosen house style, and loading no webfont is deliberate. San Francisco/Roboto at weight 900 in uppercase sounds like the flyer, and the body reads like a text message.

### Hierarchy
- **Display** (900, uppercase, `clamp(2.55rem, 11.2vw, 5.6rem)`, line-height 0.98, -0.01em): hero h1 only. On desktop ≥1000px it is clamped to `clamp(4rem, 5.5vw, 5.4rem)`.
- **Headline** (900, uppercase, `clamp(2.1rem, 9vw, 4rem)`): section h2s.
- **Claim** (900, uppercase, `clamp(1.65rem, 7.6vw, 3.4rem)`): promise-band lines.
- **Title** (900, uppercase, `clamp(1.25rem, 5.6vw, 1.6rem)`): service names. Step titles are 22px.
- **Step numeral** (900, Removal Blue, 58px phone / 84px desktop, tabular).
- **Lead** (400, `clamp(17px, 4.7vw, 20px)`, Mist, max 34–36ch): the hero pitch and close area line. Key phrases are set in `<strong>` (700, Chrome).
- **Body** (400, 17px/1.55): sentence case, max ~44ch. Service blurbs and notes are 16px.
- **Label** (800, 13.5px, uppercase, 0.06em): the three proof chips under the hero buttons.

### Named Rules
**The Loud/Plain Rule.** Headings are uppercase weight 900. Body text is always sentence case. Never set a paragraph in caps, and never set a heading in mixed case.

**The Tabular Number Rule.** The phone number always uses `font-variant-numeric: tabular-nums`.

## Layout

- **Container:** max 1180px, with 20px gutters on phones and 32px from 760px up.
- **Breakpoints:** `<760px` is phone (the dock shows, buttons stack full width, the services preview is hidden). `≥760px`: buttons sit side by side (min 250px) and show the number, services become a 1.15fr/0.85fr grid with the sticky text preview, steps go to three columns, seams grow to 92px. The promise claims stay a single stacked column at every width, like the flyer (a two-column grid clipped at 1440px and was removed). `≥1000px`: the hero fills `min(100vh, 900px)`, and the heaps go absolute at the section bottom with the logo pinned right.
- **Section rhythm:** 34px top padding everywhere, 52–60px bottom. Button groups and grids use 12px gaps.
- **Phone first viewport:** wordmark + tap-to-call, h1, pitch, Text/Call, proof chips, then the top of the heap. Keep all of it on one screen.
- **Footer** reserves `100px + safe-area` at the bottom so the dock never covers it.

## Elevation & Depth

Depth comes from light, not from cards. Navy grounds glow from the bottom (radial `navy-glow`), and a blue radial glow (`rgba(38,148,241,.32)`) sits behind each logo. Real shadows exist in only three places, all soft and navy-tinted: the primary button (`0 10px 22px -10px rgba(3,8,20,.7)`, deeper on hover), the dock (`0 -10px 30px -12px rgba(0,0,0,.5)` with a 10px backdrop blur) and the desktop text-preview card. Rubble chunks and chain links bake their own drop shadows into their canvas sprites.

**The Glow-Not-Lift Rule.** To add emphasis on navy, add blue light behind the element. Don't stack shadowed cards.

## Shapes

Controls have a firm 14px radius (`--r`). Circular forms are kept for the 44px service arrow discs and the avatar. The single card (the desktop text preview) is 28px, like a phone sheet, and its bubble uses iMessage corners (20/20/6/20). Dividers are 2px steel rules, not boxes. The chains are the main section dividers: never use a straight line or a CSS wave between sections.

## Components

### Buttons
One component everywhere (`.btn`), tactile and confident.
- **Shape:** 14px radius, 2px Removal Blue border, min-height 58px, 18px/800 label with a 22px stroke icon.
- **Primary (Text a photo):** Deep Blue fill, white text, soft navy shadow. Always an `sms:` link with the pre-filled body.
- **Secondary (Call now):** translucent navy fill, Chrome text, same border. Always a `tel:` link.
- **States:** press scales to 0.97. Hover (pointer devices only) lifts 2px, and primary goes to `blue-hover`. Easing is `cubic-bezier(.2,.8,.2,1)` at .25s.
- **Desktop:** the number (`.num`) appears inside the button.

### Service rows
Each row is a full-width `sms:` link (min 76px tall) with a title, a one-line blurb and a Deep Blue arrow disc. Rows have 2px Steel Rule dividers. On hover the text slides 10px and the disc 4px, with a faint blue wash (`rgba(20,98,196,.07)`). The pre-filled body follows one template: "Hi Deadweight Removal! I'd like a quote for {service}. / What needs to go: / Town: / When works: / (I'll attach a photo.)" A new service gets the same template.

### Text preview (desktop only)
A sticky white phone-sheet card beside the service list. Hover or focus on a row puts that row's decoded `sms` body into the blue bubble.

### Phone dock
Fixed bottom bar on phones (1.4fr Text / 1fr Call, 58px buttons, 92% navy with blur). It slides in (.35s) only while both the hero and close button groups are off screen, and it is hidden ≥760px.

### Rubble heap (signature)
The stack, back to front: blue glow, back canvas (`rubble-back`), cut-out logo (`--logo`, a data-URI PNG), front canvas (`rubble-front`). The logo stands *in* the pile because chunks draw on both sides of it. The chunks are faceted polygons in a steel/navy HSL palette with a few blue chunks (the `PALETTE` array in the script: `[hue, sat, light, weight]`). Band height is `--band` (300px hero phone, 290/260/240px close by breakpoint). `--ext` is how far the canvas reaches above the band.

### Chain seams (signature)
A `.seam` div between every pair of sections, with `--from` (the color above) and `--to` (the color below) set inline. The canvas paints `from`, then fills `to` below the live chain curve, so the color boundary is always exactly the chain. Links alternate ring and edge-on bar with a steel gradient (`#e6edf5 → #9fb0c5 → #4b5c74`). Seams after the hero and close use `--from: transparent` and a -44px overlap so they sit over the pile's foot. **Adding a section:** add a seam on each side whose `--from`/`--to` match the neighboring grounds.

### Tuning (`DW` object, top of `<script>`)
- **Pile:** `rubble.lanesPhone/lanesDesk` (rows of chunks), `sizePhone/sizeDesk` (chunk size), `surface` (pile top as a share of the band), `roll` (surface speed), `dustPhone/dustDesk` (motes).
- **Interaction:** `pushRadius/push/carry` (shove), `kick` (tap flick), `spring/damping` (spring-back and wobble), `flyTime` (how fast a flicked chunk vanishes).
- **Chains:** `chain.linkPhone/linkDesk` (link size in px), `sag/swell/ripple` (wave shape), `speed` (wave speed, currently 2.0 because Ellie likes it lively), `tension` and the push/spring values for touch response.
- **Sizes and colors:** logo and glow sizes are in the HERO and CLOSE CSS media blocks. Colors are in `:root`, and the seam colors are the inline `--from`/`--to` on each `.seam`. Those are hard-coded hex, so if a ground color changes, update the seams too.

## Do's and Don'ts

### Do:
- **Do** make every new call to action a `.btn-primary` (`sms:` with the quote template) or a `.btn-secondary` (`tel:`), at 58px.
- **Do** put a chain seam between any two sections and set its `--from`/`--to` to the exact grounds.
- **Do** keep the ground sequence to navy, steel and deep blue, and use Removal Blue for the one accent word in a heading.
- **Do** use stroke SVG icons (2px, round caps) at 17–22px, colored with `currentColor`.
- **Do** honor `prefers-reduced-motion`: the canvases render one still frame and all transitions are off.

### Don't:
- **Don't** use pure black, or grey-neutral shadows on navy.
- **Don't** load a webfont. The system stack is the owner's house style.
- **Don't** add invented facts (prices, reviews, years, towns) to fill a component.
- **Don't** separate sections with straight rules, CSS waves or plain color jumps. The chain is the divider.
- **Don't** set body copy in uppercase.
