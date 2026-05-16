# VOUCHT — Project Reference Document

> This document is the single source of truth for the Voucht project. Use it to understand the business, brand, codebase, and make updates. Read this fully before making any changes.

---

## 1. What Voucht Is

Voucht is a managed digital presence service for independent local businesses (cafés, restaurants, barbers, nail salons, small retail). We help them climb Google rankings in their local area.

### The Product

- **Branded NFC/QR scan pads** installed on tables and counters at local businesses
- **Custom hub page** for each business — a one-page portal linking their Google reviews, Instagram, Facebook, TikTok, website, menu, and events
- **Competitive intelligence** — monthly scorecards showing the business how they rank against every competitor in their area on Google reviews
- **Managed updates** — businesses WhatsApp us changes, we update their hub page

### What We're NOT

- We are NOT a review-generation tool (we don't filter, gate, or incentivise reviews)
- We are NOT a website builder (we build hub pages, not full websites)
- We are NOT a marketing agency (we provide tools and intelligence, not campaigns)
- We are NOT a software platform (no self-serve dashboard in v1 — we manage everything)

### Core Positioning

**"We help local businesses dominate their area on Google."**

The pads are the delivery mechanism. The hub page is the product. The competitive scorecard is the retention engine. The subscription is the business model.

---

## 2. The Team

- **Jelani** — Sales & Onboarding. 4+ years specialty coffee experience across London (Genuine Dining Co./Spotify, Daisy Green, Colicci, Freds in Crofton Park). Handles B2B sales, demos, installations, and relationship management.
- **Raphique** — Operations & Tech. Manages super-admin system, hub page builds, asset processing, analytics, pad ordering, Stripe billing, and support.

---

## 3. Pricing Model

### No setup fees. Pads included in subscription. Cancel anytime with 30 days' notice. First month paid at signup before installation. Pads remain Voucht property.

| | Counter | Table | House |
|---|---|---|---|
| Monthly price | £29 | £49 | £79 |
| Pads included | 3 | 6 | 10 |
| Hub page | ✓ | ✓ | ✓ |
| Socials, menu, reviews, events | ✓ | ✓ | ✓ |
| "What's On" section | ✓ | ✓ | ✓ |
| Update turnaround | 48 hours | Same day | 2-hour priority |
| Scan analytics | — | ✓ | ✓ |
| Monthly competitive scorecard | — | ✓ | ✓ |
| Competitor review tracking | — | ✓ | ✓ |
| Monthly proactive hub refresh | — | ✓ | ✓ |
| QR stickers for packaging | — | ✓ | ✓ |
| Review milestone alerts | — | ✓ | ✓ |
| White-label (no Voucht footer) | — | ✓ | ✓ |
| Seasonal hub refresh (4x/year) | — | — | ✓ |
| Multi-location admin | — | — | ✓ |
| Additional location discount | — | — | 20% off |
| Quarterly in-person strategy session | — | — | ✓ |

Additional pads: £6 each across all tiers.

### Stripe Products

- **Voucht Counter** — £29/month recurring
- **Voucht Table** — £49/month recurring
- **Voucht House** — £79/month recurring

Statement descriptor: VOUCHT

---

## 4. Brand Identity

### Name

**Voucht** (rhymes with "vouched")

- Domain: voucht.co.uk
- Email: hello@voucht.co.uk
- Instagram: @voucht

### Logo

The logo is a stylised letter "V" made from two shapes:
- Left stroke: a tall rounded rectangle tilted to the left (representing a scan/tap motion)
- Right stroke: a square/rectangle tilted to the right with a QR code positioning marker in the corner

The V shape is formed by the two strokes meeting at the bottom. The QR marker communicates "scan this" without words.

Primary version: green (#00CC6F) mark on dark (#1A1A1A or #0A0A0A) background.

Logo was created in Affinity Designer. Master vector file is maintained by Jelani.

### Colour Palette

| Name | Hex | Usage |
|---|---|---|
| Primary Green | `#00CC6F` | Logo, CTAs, accents, highlights, scorecard "you" bar |
| Green Hover | `#00E87D` | Button hover states |
| Green Dim | `rgba(0,204,111,0.12)` | Subtle backgrounds, icon containers, badges |
| Green Glow | `rgba(0,204,111,0.25)` | Box shadows on hover |
| Background | `#0A0A0A` | Page background |
| Background Elevated | `#111111` | Slightly raised surfaces |
| Card Background | `#151515` | Cards, feature blocks |
| Card Hover | `#1A1A1A` | Card hover state |
| Text Primary | `#F0EDE6` | Headings, body text |
| Text Dim | `#999990` | Secondary text, descriptions |
| Text Faint | `#5A5A52` | Tertiary text, labels, footnotes |
| Border | `rgba(255,255,255,0.06)` | Default borders |
| Border Hover | `rgba(255,255,255,0.12)` | Hover state borders |

### Typography

| Role | Font | Weight | Source |
|---|---|---|---|
| Display / Headings | Instrument Serif | 400 (regular + italic) | Google Fonts |
| Body / UI | Satoshi | 400, 500, 600, 700 | Google Fonts (fallback: DM Sans) |

- Headings use `font-family: 'Instrument Serif', Georgia, serif`
- Body uses `font-family: 'Satoshi', 'DM Sans', system-ui, sans-serif`
- The green italic treatment on key words in headings (e.g., "Dominate your area on *Google*") uses `<em>` tags styled with `color: var(--green)`

### Design Principles

- Dark theme throughout — never use light/white backgrounds for the main site
- Grain texture overlay on the body (subtle, pointer-events: none)
- Green is used sparingly — accents, CTAs, highlights, and the scorecard. Never as a background colour for large areas
- Cards have subtle border, dark fill, and lift on hover (translateY + border-color change)
- Generous whitespace — sections are 7rem padding
- Rounded corners: 14px for cards, 20px for large cards, 100px for buttons/pills
- Animations: fadeUp on hero elements (staggered), hover lifts on cards, accordion on FAQ

---

## 5. Website Structure

The site is a single HTML file (`index.html`) hosted on Netlify, connected to voucht.co.uk via DNS.

### Sections (top to bottom)

1. **Nav** — fixed, blurred background, logo + section links + green CTA
2. **Hero** — headline, subtext, two CTAs, "no setup fees" note, grid background, green glow
3. **How It Works** — 3 step cards (build hub page, install pads, climb rankings)
4. **What You Get** — 6 feature cards in 2-column grid
5. **Competitive Scorecard Preview** — split layout: text left, mock scorecard right showing bar chart of competitors
6. **Pricing** — 3-tier grid, Table highlighted as "Most popular"
7. **Stats** — 4 stat cards (93%, 4.5x, 15s, <£2/day)
8. **FAQ** — 7 accordion questions
9. **Final CTA** — "Your competitors are already ahead"
10. **Footer** — copyright, email, Instagram

### CTAs

All "Get started" buttons currently link to `mailto:hello@voucht.co.uk`. When Stripe payment links are ready, replace with direct Stripe checkout URLs.

### File Structure

```
voucht-site/
├── index.html          ← the entire site
├── logo.png            ← Voucht logo (green on dark)
├── favicon.png         ← 32x32 or 16x16 favicon
└── VOUCHT_REFERENCE.md ← this file
```

---

## 6. Tech Stack

### Website

- Pure HTML/CSS/JS — no framework, no build step, no dependencies beyond Google Fonts
- Hosted on Netlify (free tier)
- Domain: voucht.co.uk (registered via Squarespace, DNS pointed to Netlify)
- Auto-deploys from GitHub repo on push to main

### Business Operations

| Tool | Purpose |
|---|---|
| Airtable | Client database, scan logs, sales pipeline CRM |
| Stripe | Subscription billing (Counter/Table/House) and invoicing |
| Carrd (or Vercel) | Hub page hosting for individual client pages |
| Canva | Pad card design, marketing materials |
| NFC Tools app | Programming NFC tags |
| Google Looker Studio | Analytics dashboards for Table/House customers |
| Zapier | Monthly email automation for competitive scorecards |
| WhatsApp Business | Client communications and update requests |

### Hardware

- NTAG215 NFC sticker tags (sourced from Amazon UK)
- Acrylic table stands (A7 or business card size)
- Printed cards with business logo + QR code (local print shop or Instantprint)

---

## 7. Key Pages / URLs

| URL | What it is |
|---|---|
| voucht.co.uk | Main website (this codebase) |
| voucht.co.uk/[business-slug] | Client hub pages (future — not yet built) |
| hello@voucht.co.uk | Primary contact email |
| instagram.com/voucht | Instagram profile |

---

## 8. Competitive Landscape

### Direct Competitors

| Company | What they sell | Price |
|---|---|---|
| Reviews Card (UK) | NFC review stands/cards | £10–50 one-time |
| Amazon/Etsy sellers | Generic NFC review cards | £5–25 one-time |
| Tapt (AU) | NFC cards and accessories | £15–40 one-time |

### How Voucht is Different

- Competitors sell a physical product and walk away. Voucht provides an ongoing managed service.
- Competitors link to ONE platform (just Google). Voucht links to everything (reviews, socials, menu, events).
- No competitor offers competitive review tracking or monthly scorecards.
- No competitor does in-person installation, managed updates, or quarterly check-ins.
- Voucht sells an outcome (climbing Google rankings) not a product (NFC cards).

---

## 9. Google Review Policy Compliance

**THIS IS CRITICAL. READ BEFORE MAKING ANY CHANGES TO HUB PAGES.**

- The review button on hub pages links DIRECTLY to the Google review URL. No middle step. No filtering.
- We do NOT ask customers to rate their experience before sending them to Google.
- We do NOT gate reviews (sending happy customers to Google and unhappy customers elsewhere).
- We do NOT offer incentives for reviews (no "scan and get 10% off if you leave a review").
- The business can verbally encourage reviews — that's fine and normal.
- If a business asks us to build a review filter, we decline and explain the risk to their Google listing.

Violating Google's review policy can get a client's entire review profile flagged or removed, which would destroy trust in Voucht and end the business.

---

## 10. Common Update Tasks

### Updating pricing

1. Edit the pricing section in `index.html` — search for `pricing-section`
2. Update the amounts, features, and tier names
3. Update the Stripe products to match
4. Update this reference document

### Adding testimonials

Add a new section between the stats and the final CTA. Use the card style from the features section. Include: quote, business name, owner name, and number of reviews gained.

### Updating the scorecard mockup

The scorecard in the website is a static HTML mockup (not real data). To update the business names or numbers, search for `scorecard-mock` in the HTML and edit the bar widths (as percentages) and review counts.

### Changing CTA destinations

Search for `mailto:hello@voucht.co.uk` in the HTML file. Replace with Stripe payment links when ready. The nav CTA, hero CTA, and each pricing card CTA all need updating.

### Adding the logo to the nav

In the nav section, replace:
```html
<span>Voucht</span>
```
With:
```html
<img src="logo.png" alt="Voucht"><span>Voucht</span>
```
Make sure `logo.png` is in the same folder as `index.html`.

### Deploying changes

If using GitHub + Netlify:
```bash
git add .
git commit -m "description of changes"
git push origin main
```
Netlify auto-deploys within 30 seconds of push.

---

## 11. Future Development Roadmap

### V1 (Current — Pre-revenue)
- [x] Business model locked
- [x] Pricing finalised (Counter/Table/House)
- [x] Brand identity (logo, colours, typography)
- [x] Website built and deployed
- [x] Stripe account set up
- [ ] Airtable base configured
- [ ] 3 pilot businesses installed
- [ ] First paid customers

### V2 (10–30 customers)
- [ ] Hub page template system (scalable, not one-off builds)
- [ ] Scan tracking backend (log scans per pad, per table, per business)
- [ ] Pro analytics dashboard (Google Looker Studio)
- [ ] Monthly email automation (Zapier)
- [ ] Testimonial section added to website

### V3 (30–100 customers)
- [ ] Self-serve admin panel for businesses to update their own hub pages
- [ ] Automated competitive scorecard generation
- [ ] Referral programme
- [ ] Territory expansion beyond SE London

### V4 (100+ customers)
- [ ] Consider Ltd company registration
- [ ] Hire part-time install/sales help
- [ ] Franchise or territory licensing model exploration

---

## 12. Important Contacts & Accounts

| Service | Account Owner | Notes |
|---|---|---|
| Squarespace (domain) | Jelani | voucht.co.uk registration |
| Netlify (hosting) | [TBD] | Free tier, auto-deploy from GitHub |
| GitHub | [TBD] | Repository: voucht-site |
| Stripe | Jelani | Payments, subscriptions, invoicing |
| Airtable | [TBD] | Client database |
| WhatsApp Business | [TBD] | Client communications |
| Instagram | [TBD] | @voucht |
| Google (Place ID Finder) | N/A | Free tool for finding review URLs |

---

## 13. Brand Voice & Copy Guidelines

### Tone
- Direct, confident, no fluff
- Hospitality-native — speak the language of café and restaurant owners
- Never say "NFC technology" or "QR code solution" — say "scan pads" or "tap with your phone"
- Never say "we're a startup" — say "we work with [business names]"
- Never say "it's only £49" — say "it's £49 a month and we handle everything"

### Key Phrases to Use
- "Dominate your area on Google"
- "Climb Google rankings"
- "Your competitors are already ahead"
- "We handle everything"
- "One scan, everything about your business"
- "No setup fees. Cancel anytime."

### Key Phrases to NEVER Use
- "It's basically a QR code"
- "Like Linktree but better"
- "Our NFC technology"
- "Review generation tool"
- "Trust me"

### Tagline
**"Your business, one scan away."**
Alternative: **"Dominate your area. One scan at a time."**

---

*Last updated: May 2026*
*This document should be updated whenever pricing, features, brand identity, or business model changes.*
