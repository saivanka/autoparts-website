# Gem3 Auto Parts

A static marketing website for Gem3 Auto Parts, a budget-friendly supplier of used auto parts. It presents the business through an auto salvage network: visitors can browse services, search parts by vehicle brand, and submit a parts request through the "Book Now" form.

## What it does

- **Home page (`index.html`)** — hero section, service slider (engines, transmissions, all auto parts), a brand search box, and an FAQ accordion.
- **Service pages** — `engine.html`, `transmission.html` and `service-list.html` describe the parts categories on offer.
- **Booking (`booking.html`)** — a "Book Now" form asking for vehicle year, make, model and part, plus name, address, email, phone and a message; submissions are sent to a Supabase `entries` table, with a success/error toast shown to the visitor.
- **Info pages** — `faq.html`, `location.html`, a contact page and a custom `404-error.html`.
- **PWA setup** — `manifest.json` and `sw.js` register a service worker so the site can behave like an installable app.

## Tech stack

- Plain HTML, CSS and JavaScript — no build step and no framework
- Bootstrap and Bulma for layout and components, jQuery and Swiper for the sliders, SweetAlert2 for the form toasts
- Supabase (via the browser JS client) for storing booking-form submissions
- Assets under `assets/` (images, vendor CSS/JS, plugins) and part data in `parts.json`

## How to run

There is no build step. Serve the folder with any static server and open `index.html`, for example:

```bash
npx serve .
```

or simply open `index.html` directly in a browser. The booking form needs the Supabase project configured in `index.html` to actually store submissions.

## Project structure

```
index.html          # Home page: hero, services, brand search, FAQ, booking modal
booking.html        # Booking page
engine.html         # Used engines page
transmission.html   # Used transmissions page
service-list.html   # Services overview
faq.html            # FAQ page
location.html       # Locations page
contact copy.html   # Contact page
404-error.html      # Custom error page
assets/             # Images, CSS (vendor + plugins + site) and JS
parts.json          # Part data
manifest.json       # PWA manifest
sw.js               # Service worker
package.json        # Project metadata
```

## Status

A complete static site from 2022. Some FAQ answers are still placeholder text, and the booking form depends on its Supabase backend being live.
