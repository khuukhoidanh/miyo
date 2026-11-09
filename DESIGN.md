---
name: MIYO Memories
description: A monochrome, scroll-led visual system for remembering the Hà Nội exchange trip.
colors:
  paper: "#f7f7f5"
  ink: "#0a0a0a"
  ash: "#a5a5a2"
  soft-paper: "#e9e9e7"
  muted-ink: "#4e4e4e"
  white: "#ffffff"
typography:
  display:
    fontFamily: "Space Grotesk, Arial, sans-serif"
    fontSize: "clamp(3.2rem, 8vw, 6rem)"
    fontWeight: 500
    lineHeight: 0.9
    letterSpacing: "-0.04em"
  body:
    fontFamily: "DM Sans, Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.65
  label:
    fontFamily: "DM Mono, monospace"
    fontSize: "11px"
    fontWeight: 500
    lineHeight: 1.5
rounded:
  circle: "50%"
spacing:
  gutter: "clamp(22px, 6.2vw, 96px)"
  components:
    wordmark:
    textColor: "{colors.paper}"
    typography: "700 30px/.9 Space Grotesk"
  journey-marker:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.circle}"
    size: "10px"
---

# Design System: MIYO Memories

## Overview

**Creative North Star: “The Monochrome Film Strip”**

The `/memories/` surface treats the exchange trip as a sequence of cinematic pauses: a single image or typographic scene earns the space, while the interface stays quiet. The visual language is editorial and tactile rather than decorative, using paper-like off-white, near-black fields, grayscale photography, fine rules, and a subtle grain texture.

Scroll is the narrative mechanism. Chapters progress through restrained reveals, image parallax, and a pinned desktop title; mobile keeps the same story but avoids pinning. This system documents the implemented memories surface and should not be assumed to describe unrelated site routes.

**Key Characteristics:**
- Monochrome scenes with a deliberately limited set of illustrative photographs.
- Oversized, tightly composed display type balanced by readable Vietnamese body copy.
- Flat surfaces, hairline rules, and motion that follows the trip narrative.

## Colors

The palette is neutral by design: black and paper establish scene changes, while gray carries secondary information and image captions.

### Primary
- **Ink** ({colors.ink}): Near-black for chapter fields, footer, primary text, and high-contrast controls.
- **Paper** ({colors.paper}): Warm off-white for the page canvas and light timeline chapters.

### Neutral
- **Ash** ({colors.ash}): Secondary display emphasis and quiet brand punctuation.
- **Soft Paper** ({colors.soft-paper}): Alternate chapter and personal-memory background.
- **Muted Ink** ({colors.muted-ink}): Supporting prose and labels on light surfaces.
- **White** ({colors.white}): Captions and text over darkened photography.

**The Grayscale Rule.** Keep photography monochrome and do not introduce a decorative accent hue; use tonal contrast to distinguish chapters.

## Typography

**Display Font:** Space Grotesk (Arial, sans-serif fallback)  
**Body Font:** DM Sans (Arial, sans-serif fallback)  
**Label/Mono Font:** DM Mono (monospace fallback)

**Character:** Space Grotesk gives chapter titles a direct, contemporary editorial voice. DM Sans keeps longer Vietnamese passages comfortable, while DM Mono makes dates, section indices, and image credits feel like quiet archival metadata.

### Hierarchy
- **Display** (500, responsive 3.2–6rem, 0.9 line-height): Hero and chapter headlines; use large scale as the primary visual event.
- **Title** (500, responsive 3.5–6rem, 0.9 line-height): Timeline and section titles, reduced on small screens.
- **Body** (400, 16px, 1.65 line-height): Main reading copy; supporting paragraphs use a compact measure near 38ch.
- **Label** (500, 11px, 1.5 line-height, lightly tracked): Dates, route labels, chapter indices, and credits. Labels are metadata, not substitutes for body content.

**The Headline Rule.** Favor short, deliberate line breaks and modest negative tracking; allow Vietnamese words to wrap without clipping at narrow widths.

## Layout

The page alternates full-bleed scenes with generous, asymmetric editorial layouts. The main content gutter scales from 22px on small screens to a 6.2vw fluid inset, capped at 96px. Text/image chapters use a two-column grid on wider screens and stack into one column on mobile. Photo plates are broad and uncropped by card frames; their captions sit directly over the lower edge.

At widths up to 760px, the hero and chapter layouts become single-column, navigation tightens, and image heights are bounded relative to viewport width. At widths up to 430px, the home navigation link is hidden while the wordmark and journey link remain. The school chapter title pins only on desktop; mobile reveals it in normal document flow. Horizontal overflow is clipped and verified absent at a 390px viewport.

## Elevation & Depth

The system is flat: it uses no box shadows. Depth comes from alternating dark and light fields, grayscale photography, layered black gradients over full-bleed images, subtle film grain, and scroll-driven movement. Keep these layers restrained so text stays legible and the photograph remains a scene rather than a card.

## Shapes

Most geometry is square-edged and rectangular. Fine one-pixel rules define navigation and the timeline; the timeline's small circular marker is the only recurring rounded shape. Image crops are clipped to their scene bounds, not rounded into cards.

## Components

### Navigation
- **Wordmark:** Compact “MIYO.” signature in Space Grotesk, with a muted terminal dot. The top navigation overlays the opening hero and keeps direct journey and home destinations.
- **States:** Links remain text-first; hover underlines use a small offset. Keyboard focus uses a visible two-pixel outline with five-pixel offset.
- **Mobile:** Keep journey access beside the wordmark; hide the secondary home link at the narrowest breakpoint.

### Signature Components
- **Hero scene:** Full-viewport grayscale image, dark gradient, lower-left headline and a direct journey link. The route line is an SVG detail and animates independently of the copy.
- **Journey chapter:** Alternating light/dark full-width scene with a date/index, oversized title, and one selected photo. Timeline chapters reveal with GSAP; imagery may move with subtle parallax.
- **Personal memory:** The QR-selected profile section stays hidden until a matching profile is resolved. Preserve the supplied name, message, and photo rather than replacing this behavior with a generic profile card.
- **Scroll progress:** A two-pixel fixed line at the top edge tracks document progress without intercepting input.

## Do's and Don'ts

### Do:
- **Do** preserve the monochrome photo treatment, broad scene crops, and strong light/dark chapter changes.
- **Do** keep Vietnamese body text readable at 14px or larger and retain the 11px metadata treatment for genuinely secondary labels.
- **Do** keep desktop pinning and parallax conditional on motion preference; use normal-flow chapter reveals on mobile.
- **Do** keep profile content conditional on the QR/profile data and maintain the direct navigation links.

### Don't:
- **Don't** rebuild the page as a dense photo collage or a grid of rounded cards.
- **Don't** add color accents, heavy shadows, or decorative UI that competes with the trip scenes.
- **Don't** make meaning depend on motion; reduced-motion users must retain the complete story without pinning or scroll animation.
