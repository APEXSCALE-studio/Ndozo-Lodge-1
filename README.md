# Ndozo Lodge — Official demo Website

> Lusaka, Zambia · Hospitality · Single-file HTML/CSS/JS

A fully responsive, dark-luxury hospitality website for **Ndozo Lodge**, built as a single deployable HTML file with zero dependencies, zero frameworks, and zero build steps.

---

## Preview

| Hero | Booking Form | Rooms |
|------|-------------|-------|
| Auto-sliding pool photography | WhatsApp & Email tabs | Hover cards with availability CTA |

---

## Features

### UI & Design
- **Dark earth-tone aesthetic** — deep browns, warm golds, and charcoal throughout
- **Cormorant Garamond** display font paired with **Jost** for body text
- Auto-playing **hero slideshow** with real lodge photography and dot navigation
- Scroll-triggered **fade-in animations** via IntersectionObserver
- **Gallery lightbox** — click any photo to expand, `Esc` to close
- Fully responsive across desktop, tablet, and mobile (360px and up)

### Booking System
- **Dual-channel booking form** — WhatsApp and Email tabs
- Room card **"Check Availability"** buttons pre-select the room in both form tabs and auto-scroll to the booking section
- Pre-formatted WhatsApp message built from form data, opens in new tab via `wa.me`
- Pre-formatted `mailto:` email with subject line and full booking details
- **Inline validation** — no `alert()`, errors shown as red banners inside the form
- Date inputs enforce today as minimum; check-out enforces ≥ check-in
- Channel-specific success screen after submission

### Sections
| Section | Description |
|---------|-------------|
| **Hero** | 4-slide auto-rotating slideshow with CTA buttons |
| **Facts Bar** | Rooms count, pools, 24/7 service, guest rating |
| **About** | Overlapping image layout with years-of-service badge |
| **Rooms** | 4-card grid — Executive Suite, Deluxe, Classic, Comfort |
| **Amenities** | Icon list with mosaic image layout |
| **Dining** | Dark section with menu highlights and pricing |
| **Gallery** | 3-column masonry with lightbox |
| **Booking** | WhatsApp + Email form with room pre-selection |
| **Location** | Google Maps embed + contact cards |
| **Footer** | 4-column with links, socials, and hours |

---

## Tech Stack

| Layer | Choice | Reason |
|-------|--------|--------|
| Markup | HTML5 | Semantic structure |
| Styling | Vanilla CSS (custom properties) | No build step, full control |
| Scripting | Vanilla JS (ES6+) | Zero dependencies |
| Fonts | Google Fonts CDN | Cormorant Garamond + Jost |
| Maps | Google Maps Embed API | No API key required |
| Booking | `wa.me` + `mailto:` | Works without a backend |

No npm. No bundler. No framework. One file.

---

## Project Structure

```
ndozo-lodge/
├── index.html        # Entire site — HTML, CSS, and JS in one file
└── images/
    ├── aerial-view.jpg
    ├── pool-sunloungers.jpg
    ├── pool-cabana.jpg
    ├── pool-close.jpg
    ├── room-blue.jpg
    ├── room-floral.jpg
    ├── room-colorful.jpg
    ├── room-striped.jpg
    ├── room-orange-accent.jpg
    ├── room-white.jpg
    ├── room-red.jpg
    ├── outdoor-terrace.jpg
    ├── gardens.jpg
    ├── food-fish-nshima.jpg
    └── drinks-colorful.jpg
```

---

## Getting Started

### Local preview

No server required. Just open the file:

```bash
# Clone the repo
git clone https://github.com/your-username/ndozo-lodge.git
cd ndozo-lodge

# Open directly in browser
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

Or use a local dev server if you prefer:

```bash
npx serve .
# → http://localhost:3000
```

### Deploy

The site is a static file — deploy anywhere:

| Platform | Steps |
|----------|-------|
| **GitHub Pages** | Push to `main` → Settings → Pages → Deploy from branch |
| **Netlify** | Drag-and-drop the `ndozo-lodge/` folder onto netlify.com/drop |
| **Vercel** | `vercel --prod` from the project folder |
| **cPanel / shared hosting** | Upload via FTP to `public_html/` |

---

## Configuration

Before going live, replace the placeholder values in `index.html`:

```
Search for → Replace with
─────────────────────────────────────────────────────
260977000000     →  Real lodge WhatsApp number
info@ndozolodge.com  →  Real lodge email address
```

Both appear in the booking form, the contact cards, the dining section CTA, and the footer. A single find-and-replace in any editor covers all of them.

### Update the map

The map embeds using a Google search query. For a precise pin, replace the iframe `src` with a Google Maps Embed URL using the lodge's exact coordinates:

```
https://www.google.com/maps/embed?pb=<YOUR_EMBED_CODE>
```

Get the embed code: Google Maps → share the location → Embed a map → copy the `src` value.

---

## Booking Flow

```
User clicks "Check Availability" on a room card
        │
        ▼
Room pre-selected in form + page scrolls to #booking
        │
        ▼
User fills: Name · Phone/Email · Dates · Guests · Requests
        │
        ├─── WhatsApp tab ──→ wa.me link opens with pre-filled message
        │                     User taps Send in WhatsApp
        │
        └─── Email tab ─────→ mailto: opens mail client with pre-filled email
                              User taps Send in mail app
        │
        ▼
Success screen shown — "Almost Done! Tap Send to complete."
```

No server-side code. No database. The lodge owner receives the booking directly in WhatsApp or email and confirms manually.

---

## Browser Support

| Browser | Support |
|---------|---------|
| Chrome / Edge 90+ | ✅ Full |
| Safari 15+ | ✅ Full |
| Firefox 90+ | ✅ Full |
| Samsung Internet | ✅ Full |
| IE 11 | ❌ Not supported |

---

## Roadmap

- [ ] Firebase admin dashboard for managing bookings
- [ ] EmailJS integration for server-side email (removes need for mail client)
- [ ] Room availability calendar
- [ ] Multi-language support (English / Bemba / Nyanja)
- [ ] Google Analytics integration

---

## License

This project is proprietary. All photography and branding belong to **Ndozo Lodge, Lusaka, Zambia**.

The codebase was built by **Tommy** — freelance web developer, Lusaka 🇿🇲.

---

*Built with HTML, CSS, and a lot of patience.*
