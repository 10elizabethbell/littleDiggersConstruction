---
name: Little Diggers Construction
description: A marked-out New England lawn before the dig, for an Auburn, MA excavation and granite crew.
colors:
  soil: "#46311f"
  soil-deep: "#3b2918"
  loam: "#5a3f27"
  granite: "#dad9d3"
  granite-shade: "#c4c3bc"
  ink: "#2a1f16"
  ink-soft: "#57473a"
  bone: "#f2efe7"
  bone-soft: "#dcd1c1"
  machine-yellow: "#f5c518"
  machine-yellow-hot: "#ffd84a"
  survey-pink: "#ff5c9e"
  lawn: "#4a7a29"
  paint-water: "#2f7bea"
  paint-gas: "#ffd21a"
  paint-sewer: "#3fbf4a"
  paint-electric: "#ff3b2f"
  paint-white: "#f7f5ef"
  facebook-blue: "#1665d8"
typography:
  display:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(2.6rem, 12.4vw, 6rem)"
    fontWeight: 900
    lineHeight: 0.9
    letterSpacing: "-0.03em"
  headline:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(2.1rem, 9.4vw, 3.8rem)"
    fontWeight: 900
    lineHeight: 0.95
    letterSpacing: "-0.025em"
  title:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(20px, 5.6vw, 28px)"
    fontWeight: 900
    lineHeight: 1.1
    letterSpacing: "-0.01em"
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 800
    lineHeight: 1.2
  small:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.55
rounded:
  photo: "4px"
  field: "10px"
  button: "12px"
  slab: "14px"
  pill: "24px"
  round: "50%"
spacing:
  gutter: "16px"
  gutter-wide: "40px"
  max: "1180px"
  section-y: "76px"
  section-y-wide: "110px"
  stack: "22px"
  gap: "10px"
components:
  button-primary:
    backgroundColor: "{colors.machine-yellow}"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.button}"
    padding: "0 14px"
    height: "56px"
  button-primary-hover:
    backgroundColor: "{colors.machine-yellow-hot}"
    textColor: "{colors.ink}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.bone}"
    typography: "{typography.label}"
    rounded: "{rounded.button}"
    padding: "0 14px"
    height: "56px"
  button-send:
    backgroundColor: "{colors.machine-yellow}"
    textColor: "{colors.ink}"
    typography: "{typography.label}"
    rounded: "{rounded.button}"
    height: "60px"
    width: "100%"
  input-text:
    backgroundColor: "{colors.bone}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.field}"
    padding: "13px 14px"
    height: "52px"
  chip-service:
    backgroundColor: "transparent"
    textColor: "{colors.bone}"
    rounded: "{rounded.pill}"
    padding: "0 16px"
    height: "48px"
  chip-service-selected:
    backgroundColor: "{colors.machine-yellow}"
    textColor: "{colors.ink}"
  service-row:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    typography: "{typography.title}"
    height: "72px"
  facebook-slab:
    backgroundColor: "{colors.facebook-blue}"
    textColor: "#ffffff"
    rounded: "{rounded.slab}"
    padding: "12px 16px"
    height: "64px"
---

# Design System: Little Diggers Construction

## Overview

**Creative North Star: "Marked Out Before the Dig"**

The site is a residential lawn the morning a crew arrives: Dig Safe locate paint sprayed across New England grass, wet loam where the ground is open, granite curb sections laid in between. The page alternates two grounds, dark loam and speckled granite, and every accent is a material a crew actually uses: machine yellow for anything you press, survey-flag pink for the form field you are filling in, and the four utility locate colors (water blue, gas yellow, sewer green, electric red) as sprayed marks under headings and as the pipes buried in the hero lawn. Photos get white-lining, the dashed paint perimeter crews spray around a dig area.

Lettering is heavy, uppercase, tightly tracked system type, set large. The density is low and the targets are big because the visitor is a homeowner on a phone, usually inside Facebook's in-app browser. The signature is physical: the hero lawn is a canvas you dig into with a finger to uncover the colored pipes beneath each mark, and grass fringes sway along every top edge where a soil ground meets the section above it. Both react to the pointer and rest when off-screen.

The build rejects the stock contractor page: no stock excavator photography, no hazard stripes, no row of three icon cards.

**Key Characteristics:**
- Two alternating grounds: loam brown (dark) and granite gray with real mica-and-quartz speckle (light).
- Accent colors are site materials with fixed jobs, never decoration.
- Heavy uppercase system lettering, tight negative tracking, display sizes driven by viewport width.
- Spray-paint texture (an SVG turbulence filter) on every painted element: heading marks, step numerals, white-lining.
- Living ground: dig-to-reveal lawn canvas plus grass fringes, both tuned through `CFG` constants at the top of their JS modules, both honoring reduced motion.

## Colors

An earth-and-stone neutral pair carries the page; a strict set of jobsite signal colors does all the talking.

### Primary
- **Machine Yellow** (machine-yellow): Every action. Primary button fill, ghost button border, selected chips, service-row arrow on hover, the yellow phone and Facebook icons, the second line of the footer wordmark, and text selection. Brightens to **Hot Yellow** (machine-yellow-hot) on hover.

### Secondary
- **Survey Pink** (survey-pink): Focus, plus hover inside the quote form. The global `:focus-visible` outline (3px, 3px offset), the outline on text fields, chips and form buttons on hover and on focus (a house rule from the site's designer: every form control is outlined on hover and focus in one accent that isn't the button fill), and the text caret. It appears nowhere else.

### Tertiary
- **Locate Paints** (paint-water, paint-gas, paint-sewer, paint-electric, paint-white): The utility marking code. Used as sprayed underlines beneath every section headline (one color per section), as the dashed marks and buried pipes in the hero lawn, and (paint-white) as the white-lining around photos. On granite, the gas yellow and sewer green numerals are darkened for legibility (to #a87c00 and #2a9b36); electric red holds as-is.
- **Lawn Green** (lawn): The base under the hero canvas; blades are drawn from a five-step green family (#355c1c to #6c9d3c) shared by the lawn and the fringes.

### Neutral
- **Wet Loam** (soil): The page ground; hero, Work and Quote sections. Also the browser theme color.
- **Deep Loam** (soil-deep): Footer ground and scrollbar track.
- **Loam** (loam): Photo placeholder fill and scrollbar thumb.
- **Granite** (granite) with **Granite Shade** (granite-shade): The light section ground, always under the speckle texture.
- **Ink** (ink) and **Ink Soft** (ink-soft): Text on granite; ink-soft for step body copy and the service-row arrow ring.
- **Bone** (bone) and **Bone Soft** (bone-soft): Text on loam; bone-soft for supporting copy, the wordmark sub-line and optional labels. Bone is also the text-field fill.
- **Facebook Blue** (facebook-blue): Third-party brand color, used only on the single "see more of our work" link to Facebook.

### Named Rules
**The Jobsite Signal Rule.** Yellow means press, pink means you are here or about to be (form hover and focus), locate paint means a mark on the ground. A color never borrows another color's job.

**The One Paint Per Section Rule.** Each section headline gets exactly one sprayed mark in one locate color; sections do not repeat their neighbor's color.

## Typography

**Display Font:** System UI stack (-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif)
**Body Font:** Same stack

**Character:** One family, pushed to weight 900 and uppercase for everything that names a thing, left at 400 for anything that explains. The system stack is a deliberate house rule from the site owner's designer, chosen for speed in in-app browsers; it is not a fallback awaiting a webfont.

### Hierarchy
- **Display** (900, clamp(2.6rem, 12.4vw, 6rem); 3.4rem to 6rem at 960px+, line-height 0.9, uppercase): The hero headline only, one short line per span.
- **Headline** (900, clamp(2.1rem, 9.4vw, 3.8rem), 0.95, uppercase): Section headlines, always followed by a sprayed mark. The footer wordmark runs at a near-display size (clamp(2rem, 10vw, 4.6rem)).
- **Title** (900, 20–28px, 1.1, uppercase): Service rows and step headings (24px).
- **Body** (400, 17px, 1.55): All running copy, capped near 34em. The hero promise steps up to 17–20px in bone-soft.
- **Label** (800, 17px): Buttons, form labels, phone and footer links.
- **Small** (400–700, 16px): Helper text, chips, form messages.

### Named Rules
**The Heavy-or-Plain Rule.** Text is either 900 uppercase with negative tracking, or sentence-case 400–800 body. Nothing in between, no light weights, no italics.

**The 16px Floor Rule.** Interactive and reading text never goes below 16px (17px body); the only smaller text is the 12px wordmark sub-line and 14px legal line.

## Layout

Single column on phones with a 16px gutter; a 1180px content column with a 40px gutter from 960px. Sections are full-bleed grounds with generous vertical rhythm (76px top / 64px bottom, 110px / 96px at 960px+). At 600px the work photos and steps go to two and three columns; at 960px the hero splits into copy left and lawn right (1.1fr / 1fr, capped at 1600px wide), services become a two-column list, and the quote section splits heading / form (0.8fr / 1.2fr). On phones the hero lawn is a fixed band (260–340px, 40svh) so part of the first screen still scrolls, since the lawn captures every drag. Hero actions sit in a two-up grid up to 460px wide.

## Elevation & Depth

Flat grounds; depth comes from material and texture (granite speckle, grass blades, dug soil inside the canvas). Shadows exist only where an object physically sits on the ground: the work photos and the Facebook slab. Both are soft, low, and tinted with soil rather than black.

### Shadow Vocabulary
- **Photo lift** (`box-shadow: 0 18px 36px -10px rgba(20,12,6,.6)`): Work photographs.
- **Slab lift** (`box-shadow: 0 12px 26px -10px rgba(20,12,6,.6)`): The Facebook link slab.

### Named Rules
**The Things-On-The-Ground Rule.** Only physical objects (photos, the slab) cast shadows. Buttons, fields, chips and sections stay flat.

## Shapes

Softly rounded, never sharp and never blobby: 10px on fields, 12px on buttons, 14px on the larger Facebook slab, 4px on photos, full pills (24px) on chips, and true circles on the 44px service-row arrows. Section boundaries are straight cuts, softened only by the grass fringe that grows up over each soil edge. Painted geometry is hand-made: sprayed marks are gentle bezier strokes (9px, round caps) under the spray filter, and white-lining is a 5px dashed (22 / 13) round-capped rectangle inset around each photo.

## Components

### Buttons
Big, blunt, and yellow; built for a thumb.
- **Shape:** Gently rounded (12px), 2px machine-yellow border, minimum 56px tall (60px for the form's send button, full width).
- **Primary:** Machine-yellow fill, ink label at 800 / 17px.
- **Ghost:** Transparent with the yellow border and bone label; hover tints the fill with 12% yellow.
- **Hover / Focus / Active:** Primary brightens to hot yellow; focus is the pink outline; active nudges down 1px. Transitions are 0.15–0.2s on color only.
- **Copy (tertiary):** 48px, 10px radius, transparent with a translucent bone border, bone label.

### Chips
- **Style:** Service checkboxes as 48px pills, 2px translucent bone border (45%), bone text 700 / 16px.
- **State:** Checked fills machine yellow with ink text. Tapping a service row up the page preselects its chip with a short scale pulse.

### Inputs / Fields
- **Style:** Bone fill, ink text, 2px bone border, 10px radius, 52px minimum height (120px textarea), 17px text.
- **Hover and focus:** Border and a 2px outline (2px offset) turn survey pink (house rule: form controls outline on hover and focus alike).
- **Error:** A plain 16px / 700 line above the send button in a pale pink tint; the field gets `aria-invalid`.

### Service Rows
A list, not cards: each service is a 72px title-weight row with a 2px faint ink rule beneath and a 44px circled arrow at the end. Hover or focus fills the arrow with machine yellow; focus also draws the pink ring on the arrow.

### Navigation
No menu. The header is the wordmark (900 uppercase name over a 12px wide-tracked "CONSTRUCTION" sub-line) on the left and the phone number with a yellow phone glyph on the right, 44px tall target. The footer repeats the wordmark at headline scale with the second word in yellow, plus phone and Facebook links.

### Dig-to-Reveal Lawn (signature)
A canvas filling the hero's lawn band: dense grass blades parted by the pointer, crossed by sprayed locate marks with their utility letter. Dragging digs a soil hole along a depth grid, throwing clods, until the colored pipe under the mark shows; holes regrow after a delay. Untouched, it digs itself along the marks for two passes, then resumes after 6s idle. Its edge against the hero copy is an irregular sine-driven grass line. Every behavior is tuned in the `CFG` block at the top of its module (cell size, dig radius, touch radius, dig and regrow rates, autoplay passes, blade density caps per device, parting radius). Reduced motion stops the autoplay and sway; digging by hand still works.

### Grass Fringe (signature)
A 44px canvas strip of swaying blades that overlaps the top of every soil ground (Work, Quote, footer) by 40px, so loam always meets the section above through grass. Blades lean away from the pointer. Tuned via its own `CFG` (spacing, min / max height, parting radius and push). Runs only while visible.

### Sprayed Marks and White-Lining
Section headline underlines (240px max, 62% on phones) are sprayed bezier strokes that draw in once on scroll (1.1s, cubic-bezier(.16,1,.3,1)); step numerals are 58px sprayed glyphs in locate colors. Photos sit inside a dashed paint-white perimeter, also sprayed.

## Do's and Don'ts

### Do:
- **Do** alternate loam and granite grounds section by section, and put a grass fringe on top of every loam ground.
- **Do** give every section headline one sprayed locate-paint mark, a different color from its neighbors.
- **Do** keep machine yellow (#f5c518) on actions only and survey pink (#ff5c9e) on focus and on form-control hover only.
- **Do** run every painted element through the spray filter so paint reads as paint.
- **Do** keep touch targets at 44px minimum (buttons 56px, fields 52px, chips 48px).
- **Do** expose new living behavior through a `CFG` block at the top of its module and stop it when off-screen or under reduced motion.
- **Do** use the system font stack at 900 uppercase for names and 400 for explanation.

### Don't:
- **Don't** use stock excavator photography, hazard stripes, or rows of three icon cards.
- **Don't** add a webfont; the system stack is a house rule.
- **Don't** put shadows on buttons, fields, chips or sections; only photos and the Facebook slab sit on the ground.
- **Don't** use locate-paint colors for buttons, links or UI state; they mark the ground.
- **Don't** set body or control text below 16px.
