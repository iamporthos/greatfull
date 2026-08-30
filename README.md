# Greatfull

Landing page for **Greatfull** — a takeout-only breakfast burrito operation in Markham, Ontario.

One size. Eighteen dollars, tax in. Ninety a week, Friday through Sunday. Then we're out.

> Eat great. Get full. Stay grateful.

---

## What this is

A single-page pre-launch site. It explains the product, presents the menu, tells the story behind the shop, and collects waitlist emails.

`index.html` is fully self-contained — no build step, no dependencies, no network required. Open it in a browser or drop it on any static host.

### GitHub Pages

Push to your repo, then **Settings → Pages → Source: Deploy from a branch**, pick your branch and `/ (root)`. The site is live at `https://<user>.github.io/<repo>/`.

---

## Sections

| | |
|---|---|
| **Hero** | *You are enough. So is one burrito.* |
| **The Deal** | $18, one size, and where the money goes |
| **Menu** | The omulet, then the three permanent flavours |
| **The Wildcard** | One extra flavour, new every month + Poblano Season |
| **Vegan** | Silken tofu omulet swap, any flavour, no upcharge |
| **How it's made** | 72-hour sourdough, four steps, flour to foil |
| **Story** | Why the shop exists |
| **People's Greatfull** | Pay-it-forward: 3–5 burritos given away daily |
| **Pickup** | Hours, location, how ordering works |
| **Waitlist** | Email capture |
| **FAQ** | Six questions |

---

## The menu

Every burrito is a hand-folded **omulet** — a thin egg omelet named for omurice, minus the rice — wrapped in a three-day cold-fermented sourdough tortilla. All flavours vegetarian.

**Papi Chorizo** *(hot)* · **Hasta el Fin** *(medium)* · **Mac n Cheez** *(mild)*

Plus one rotating wildcard each month. Full ingredient lists, the unscheduled rotation, and the vegan spec are in [`menu.md`](menu.md).

---

## Configuration

Five values drive the page's state. They live at the top of the logic class in the source file:

| Value | Default | Effect |
|---|---|---|
| `dropDate` | `"TBA"` | Shown in the hero and above the waitlist form |
| `waitlistOpen` | `false` | `false` = pre-launch copy; `true` = live-order copy. Changes the CTA label and two headings |
| `handle` | `"@GREATFULL"` | Instagram link text |
| `motion` | `"full"` | `"calm"` disables all animation |

---

## Before launch

- [ ] Real photography — there are 14 image slots, currently flat placeholders. This is the single biggest improvement available to the page.
- [ ] Wire the waitlist form to a real endpoint. It's client-side only right now: submitting swaps in a confirmation message but sends nothing.
- [ ] Set `dropDate` and flip `waitlistOpen` when ordering goes live.
- [ ] Point the Instagram link at the real profile.

---

## Notes

- No fixed widths or media queries — every layout track collapses fluidly, and all type scales with the viewport. Works from 320px up.
- Respects `prefers-reduced-motion`.
- Type is Archivo Black, Instrument Serif, Space Grotesk, and Space Mono, all bundled into the file.

---

© 2026 Greatfull · Markham, Ontario · Takeout only
