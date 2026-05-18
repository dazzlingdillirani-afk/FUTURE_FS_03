# FUTURE_FS_03
# Brew & Bloom Coffee — Demo Website

https://brewandbloomcafe.lovable.app

A professional demo website for **Brew & Bloom Coffee**, a fictional neighborhood
coffee bar in Brooklyn. Built as a real-world client pitch project — designed to
show a local business owner what a modern, conversion-focused website can do for
them.

> Replace the brand name, copy, images, menu, and address with a real local
> business (café, restaurant, gym, salon, boutique, clinic, etc.) and you have
> a live client deliverable.

---

## Live Preview

Run locally (see below) or deploy to any static / edge host
(Cloudflare, Vercel, Netlify).

---

## Tech Stack

- **Framework:** TanStack Start v1 (React 19 + Vite 7, SSR-ready)
- **Routing:** File-based routing under `src/routes/`
- **Styling:** Tailwind CSS v4 with a custom design system in `src/styles.css`
  (warm cream / espresso palette, `oklch` color tokens)
- **Typography:** Cormorant Garamond (display) + Inter (body)
- **UI primitives:** shadcn/ui components
- **Icons:** lucide-react
- **Notifications:** sonner

---

## Pages

| Route       | Purpose                                                    |
|-------------|------------------------------------------------------------|
| `/`         | Hero, value props, story preview                           |
| `/menu`     | Categorized menu with pricing                              |
| `/about`    | Brand story, values, team                                  |
| `/visit`    | Address, hours, embedded OpenStreetMap                     |
| `/contact`  | Inquiry form with toast feedback                           |

SEO is wired in: per-route `head()` metadata, `sitemap.xml`, `robots.txt`,
semantic HTML, alt text on images, responsive viewport, OpenGraph tags.

---

## Project Structure

```
src/
├── assets/              # AI-generated hero & lifestyle images
├── components/
│   ├── SiteHeader.tsx   # Responsive top nav
│   ├── SiteFooter.tsx   # Location, hours, Instagram
│   └── ui/              # shadcn primitives
├── routes/
│   ├── __root.tsx       # Shell + global metadata
│   ├── index.tsx        # Home
│   ├── menu.tsx
│   ├── about.tsx
│   ├── visit.tsx
│   ├── contact.tsx
│   └── sitemap[.]xml.ts
└── styles.css           # Design tokens (colors, fonts, shadows)
public/
└── robots.txt
```

---

## Getting Started

```bash
# 1. Install deps
bun install      # or: npm install

# 2. Run dev server
bun run dev      # or: npm run dev

# 3. Build for production
bun run build    # or: npm run build
```

App runs at `http://localhost:5173`.

---

## How to Customize for a Real Client

1. **Brand:** Search/replace `Brew & Bloom` with the business name.
2. **Colors & fonts:** Edit tokens in `src/styles.css`.
3. **Images:** Drop new photos into `src/assets/` and update imports.
4. **Menu / services:** Edit the data arrays in `src/routes/menu.tsx`.
5. **Address & hours:** Update `src/components/SiteFooter.tsx` and
   `src/routes/visit.tsx` (also swap the OpenStreetMap embed coordinates).
6. **Social links:** Update the Instagram URL in `SiteFooter.tsx`.
7. **Contact form:** Wire `src/routes/contact.tsx` to an email service
   (e.g. Resend) via a server function.

---

## The Pitch (for a real business owner)

> "Right now, when someone Googles your café, they find a Yelp page someone
> else wrote. This site changes that. In 30 seconds a visitor knows what you
> serve, what makes you different, where to find you, and how to book a table
> — all on their phone. That's the difference between 'looks nice, maybe
> later' and 'let's go now.' It gives you one professional home that ties
> your Instagram, Google listing, and physical brand together."

**Value delivered:**
- Converts search traffic into walk-ins and bookings
- Mobile-first, fast-loading, SEO-optimized
- Owner controls the brand story (not Yelp, not Google)
- One source of truth for menu, hours, location, contact

---

## License

Demo / educational use. Replace assets and copy before commercial deployment.
