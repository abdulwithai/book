# AI Implementation Partner — Landing Page

A lean, trustworthy landing page to convert SME owners, roofing companies, and home service businesses into booked discovery calls and $297 system audits.

## What This Page Does

- **Frames the problem** — Combines pain points with concrete solutions, tailored to roofing, home services, and growing SMEs
- **Offers two entry points** — A free 30-minute discovery call or a $297 System Audit + Roadmap
- **Drives to booking** — Every call-to-action button routes to your scheduler (or email fallback)
- **Builds trust** — Navy and white palette signals "dependable business software," with orange accents on CTAs only

## Page Structure

1. **Hero** — Headline + two CTAs + note about what to expect
2. **Problem → Fix** — 4 pain/solution pairs showing you understand their workflow
3. **Packages** — Two clear options to engage
4. **Steps** — Simple 3-step process (Book → Map → Get plan)
5. **Final CTA** — Reminder of both options
6. **Footer** — Contact links

## Configuration

### Set Your Booking Links

Near the bottom of `index.html` (around line 407), you'll see:

```javascript
var FREE_CALL_URL = ""; // e.g. "https://calendly.com/your-name/discovery-call"
var AUDIT_URL = "";     // e.g. "https://calendly.com/your-name/system-audit"
```

- **`FREE_CALL_URL`** — Set this to your Calendly (or Cal.com / Stripe checkout / etc.) link for the free discovery call
- **`AUDIT_URL`** — Set this to your Calendly event for the $297 audit, or a Stripe checkout if you want to collect payment upfront

Leave them blank to fall back to email (`mailto:` links with pre-filled subjects).

### Customize the $297 Audit Price

If you want a different price, search for `$297` in the HTML and change all three instances (pricing card, final CTA band, and mini-steps text).

### Color Palette

The page uses CSS custom properties in `:root`. To change colors, edit these lines at the top of `<style>`:

- `--bg` — Main background (currently white)
- `--ink` — Headline/text color (currently navy)
- `--accent` — CTA buttons and key highlights (currently terracotta)

## What You're Offering

### Discovery Call (Free)
- 30-minute conversation, no pitch
- You walk through your current workflow
- Abdul flags 1–2 automation wins on the spot
- No obligation

### System Audit + Roadmap ($297)
- Full audit of your tools and process
- Written report ranking where you're losing time most
- Prioritized automation roadmap with effort estimates
- 45-minute walkthrough call
- Yours to keep and act on, with or without Abdul's help to build

## Customizing Copy

All text is inline in `index.html`. Key sections to edit:

- **Hero headline & lead** — Lines ~240–242
- **Problem/Fix cards** — Lines ~303–310
- **Pricing package descriptions** — Lines ~354–361 and ~368–375
- **Footer contact info** — Lines ~397–400

The current copy targets roofing, home services, and SMEs. Adjust the verticals or example pain points to match your actual market.

## Tracking & Analytics

This is a static HTML page—add your own analytics by inserting a Google Analytics or Fathom snippet into the `<head>` section.

---

**Ready to go live?** Update the booking URLs, double-check the copy and price, and share the link wherever your customers are.
