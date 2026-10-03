# Her House

*One house, nineteen rooms. Every room is a different side of Suhani.*

**Live:** https://suhxnitiwari.github.io/suhani-house/

## What it is

A line-drawn house at night, four floors deep. Tap a room and its light turns on, a card tells you what lives there, and a "Walk in" link takes you to that section of my full personality portrait, [Soft heart. Strong spirit.](https://suhxnitiwari.github.io/suhani-personality/)

The floor plan follows the metaphor: the attic is my head, the basement is what I built, and every room in between is another side of me. The Greenhouse is my soft heart, the Gift Closet is my love language, the Boiler Room holds the twenty jobs I'd quit on day one, and the Workshop is the final personality test: I built this.

## How it's built

- **One self-contained file.** HTML, CSS and vanilla JavaScript, no build step and no images. Every piece of furniture is hand-written SVG path data.
- **Data-driven rooms.** All 19 rooms live in one array: id, name, what it holds, a line of copy, its box on the floor plan and its line art in local coordinates. The script turns each entry into an SVG group with a glow layer, a hit area, translated artwork, a room number and a label, then draws the house's walls on top.
- **Synthesized sound.** Each room plays a soft triangle-wave note from a C-major pentatonic scale through the Web Audio API, with rooms past the fourteenth jumping an octave. Light up all nineteen and a little four-note arpeggio plays.
- **Progress you can see.** A counter tracks how many rooms you've lit, and "Turn every light on" cascades through the house one room every 110 ms.
- **Accessible by default.** Every room is a focusable `role="button"` with a descriptive `aria-label` and Enter/Space support, the card is an `aria-live` region, decorative drawing is `aria-hidden`, and the steam, stars and swinging punching bag all stop for `prefers-reduced-motion`.

## Design choices

- Rooms are dark until you visit them, so exploring feels like walking through a house at night and switching lights on.
- Tiny animated details reward a closer look: steam from the chimney and the coffee cup, twinkling stars, a punching bag that sways in the Training Room.
- Wine, rose and petal pinks with Playfair Display and DM Sans, matching the palette of the personality site it opens into.

## Tech stack

HTML, CSS, vanilla JavaScript, inline SVG, Web Audio API.

## Run it locally

```bash
python3 -m http.server
```

Then open http://localhost:8000.

---

© 2026 Suhani Tiwari. All rights reserved. See [LICENSE](LICENSE).

Built by [Suhani Tiwari](https://suhanitiwari.com).
