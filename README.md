# Travel with Pandu

A responsive tourism website for travellers planning a trip to Sri Lanka. It is a static site built with plain HTML, CSS and JavaScript, with no frameworks and no build step.

## Features

- **Journey video:** a short film section with a silent preview that plays while on screen, and a button to watch it with sound.
- **Header slideshow:** full-screen photos that crossfade, plus a scrolling strip of landmarks. Both respect the `prefers-reduced-motion` setting.
- **Photo gallery page:** a separate view (`#gallery`) with a full-size viewer, keyboard arrow navigation and captions.
- **Itineraries:** tour cards with a day-by-day pop-up. Choosing a tour fills the trip enquiry form, so the owner receives the chosen itinerary in the WhatsApp or Gmail message.
- **Review cards:** each card opens the full review in a pop-up, with an optional photo.
- **Trip enquiry and review forms:** build a ready-to-send message and open WhatsApp or Gmail. On phones the Gmail app is opened where possible (iPhone: `googlegmail://`, Android: `mailto:`); on a computer, Gmail opens in a new tab.
- **Mobile-first layout** with a hash-based router (`#gallery`, `#top`) and no page reloads.

## Project structure

```
index.html      all markup, styles and scripts
images/
  logo.jpg
  about-photo.jpg
  hero/         header slideshow photos
  strip/        scrolling photo strip
  gallery/      gallery page photos
  reviews/      photos attached to reviews
videos/
  journey.mp4, journey-poster.jpg   the journey film and its poster image
```

## Run it locally

Open `index.html` in a browser. There is nothing to install or build.

## Editing content

All editable content is near the bottom of `index.html`:

| What | Where |
|---|---|
| WhatsApp number and email | `var WHATSAPP` and `var EMAIL` |
| Itineraries | the `ITINERARIES` array (title, days, subtitle, highlights and the day-by-day text) |
| Reviews | the `REVIEWS` array (name `n`, country `c`, stars `r`, optional photo `p`, optional date `d`, text `t`) |
| Gallery photos | the `GALLERY_PHOTOS` array (caption `t`, image path `s`) |

## Deploy

Any static host works. To use GitHub Pages: **Settings, then Pages**, choose the `main` branch and the `/ (root)` folder, and save.

## Tech

HTML5, CSS3 (custom properties, grid, flexbox), vanilla JavaScript.
