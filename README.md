# Yemane Tekeste — Website Package

Refined coaching. Elite performance. A single-file luxury website for Yemane Tekeste, Toronto.

## Files
| File | What it is |
|---|---|
| `index.html` | The entire website. One file — HTML, CSS, JS, fonts. No build step. |
| `logo-primary.svg` | Horizontal logo (header, signage) |
| `logo-secondary.svg` | Stacked logo (social, square) |
| `logo-icon.svg` | Crest icon (favicon, hats, app) |
| `logo-monogram.svg` | Interlocked PW (apparel, watermark) |
| `brand-guidelines.html` | Colour, type, logo, voice reference |

---

## ⚙️ STEP 1 — One required edit (2 minutes)

Open `index.html`, find this line near the bottom (in the `<script>`), and replace the placeholder with your real WhatsApp number — **digits only, international format, no `+`**:

```js
const WHATSAPP_NUMBER = "14165551234";   // ⚠️ REPLACE
```

Example: the number `+1 (416) 555-1234` becomes `"14165551234"`.

Every Book/WhatsApp button and the assessment hand-off use this one value. **Nothing else needs changing to go live.**

## Optional edits (recommended)
- **Hero footage** — in the hero `<div class="hero-bg">` there's a commented `<video>` block. Drop in your `hero.mp4` and uncomment it. Until then the cinematic gradient looks great on its own.
- **Coach portrait** — in the About section, replace the placeholder block with `<img src="coach-yemane.jpg" alt="Coach Yemane Tekeste">`.
- **Testimonials** — replace the three sample quotes (clearly marked) with real client reviews.
- **Instagram** — see note below.

---

## STEP 2 — Put it online (free, ~2 minutes)

You already have a live preview from me. To get your own public URL:

**Easiest — Netlify Drop**
1. Go to https://app.netlify.com/drop
2. Drag the whole `protennis` folder onto the page.
3. You instantly get a public URL like `random-name.netlify.app`. Done.

**Or Vercel**
1. Create a free account at https://vercel.com
2. "Add New → Project", drag the folder (or connect a GitHub repo).
3. Deploy → public URL.

**Or GitHub Pages** — push the folder to a repo, enable Pages on the `main` branch.

---

## STEP 3 — Connect your existing domain

Once deployed, point your domain at the host:

**On Netlify:** Site → *Domain management* → *Add custom domain* → enter your domain → follow the DNS records shown. Typically you set at your domain registrar:
- An `A` record → Netlify's load-balancer IP (Netlify gives it to you), **or**
- A `CNAME` record on `www` → your `*.netlify.app` address.

**On Vercel:** Project → *Settings → Domains* → add your domain → Vercel shows the exact `A` / `CNAME` records to enter at your registrar.

SSL (the padlock) is issued automatically and free on both, usually within minutes of the DNS resolving.

> Send me your host and registrar and I'll give you the exact records to paste.

---

## Notes on the two "live data" features

**AI assistant — the Court Concierge.** It's a fast, self-contained assistant built into the page (no API key, no monthly cost, works anywhere you host it). It answers pricing, programs, availability, location, assessments, payment and the coaching process, and routes people to WhatsApp. To add/adjust answers, edit the `reply()` function in the script — each topic is a clearly-labelled rule.

**Instagram feed.** Instagram doesn't allow truly automatic pulling of a feed without an approved app + access token. The section is built and links to `@protenniswyemane`. To show real posts, the clean options are: (a) a free/low-cost widget like **Elfsight**, **Behold.so**, or **SnapWidget** — paste their embed code into the Instagram section; or (b) embed specific posts via Instagram's own *Embed* code. Send me your preference and I'll wire it in.

## SEO — already done
Title, meta description, keywords (Tennis Lessons Toronto, Private Tennis Coach Toronto, Elite Tennis Coaching Toronto, Junior Tennis Toronto, Tennis Assessment Toronto), Open Graph tags, and LocalBusiness structured data are all in the `<head>`.
