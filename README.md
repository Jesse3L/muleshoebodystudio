# Muleshoe Body Studio

Live at https://muleshoebodystudio.com — landing page for Muleshoe Body Studio — invisa-RED™ red light laser treatments for weight loss, body contouring, cellulite and skin tightening in Muleshoe, TX.

Stack: Astro 7 · Tailwind CSS 4 · static output, ready for Vercel.

## Run it

```bash
npm install
npm run dev      # http://localhost:4321
npm run build    # outputs to dist/
```

## Setup checklist

1. **Business details**: phone, address, hours and service-area towns all live in `src/site.ts`. Change them there and they update everywhere, schema markup included.
2. **Booking webhook**: the form POSTs JSON to `PUBLIC_BOOKING_WEBHOOK`. Create a Make (or Zapier/n8n) custom webhook, then add the URL in Vercel → Settings → Environment Variables and redeploy. Payload fields: `booking_type`, `name`, `phone`, `email`, `preferred_day`, `preferred_time`, `goal`, `message`, `source`, `submitted_at`. Bot submissions (honeypot `company` filled) are dropped client-side. If the webhook is missing or fails, the visitor is asked to call instead.
3. **Domain**: after you buy it, add it in Vercel. If it isn't `muleshoebodystudio.com`, update `site` in `astro.config.mjs`, `url` in `src/site.ts`, and `public/robots.txt`.
4. **Google Business Profile**: create one for "Muleshoe Body Studio" using the same name, address and phone as `src/site.ts`. For a town this size, local rankings depend on it more than on anything else.

## Keyword targeting

Ubersuggest, US data, Nov 2026. Vol = monthly searches, SD = SEO difficulty (0–100).

| Keyword | Vol | SD | Where it's used |
|---|---|---|---|
| body sculpting near me | 12,100 | 14 | Intro, benefits, schema |
| red light therapy weight loss | 6,600 | 26 | Title, H2s, FAQ, schema |
| non invasive fat reduction | 6,600 | 18 | Meta description, hero, intro |
| laser lipo near me | 4,400 | 9 | FAQ "Is invisa-RED the same as laser lipo?" |
| non invasive fat reduction treatment | 4,400 | 46 | Hero, benefits |
| invisa red | 720 | 8 | Hero, results, FAQ (brand searches) |
| red light therapy weight loss before and after | 590 | 15 | Results section (add real client photos later) |
| laser body contouring | 170 | 37 | Title, how-it-works |
| red light therapy weight loss near me | 90 | 9 | Local copy + LocalBusiness schema |
| laser body contouring near me | 30 | 23 | Local copy |

Local modifiers worked into the copy: Muleshoe, Bailey County, Lubbock, Clovis, Littlefield, Friona, Farwell, Sudan, Earth, Morton, Dimmitt, Portales, Bovina. "City + body contouring" searches are tiny (for example, "body contouring lubbock" gets about 10/mo), so the plan is to rank on the "near me" and service terms through Google Business Profile proximity. That's why matching NAP and reviews matter.

**Next pages to add, ranked by opportunity:**
- `/red-light-therapy-weight-loss` — long-form guide (targets the 6.6k term + "does it work", "results")
- `/laser-lipo-vs-red-light` — comparison page (captures "laser lipo" 18k/27k searchers looking for non-surgical options)
- `/cellulite-treatment-muleshoe` and `/skin-tightening` — service pages
- `/results` — real client before/after photos (with consent), targeting the "before and after" terms

## Claims and compliance

The invisa-RED ELITE is FDA 510(k) cleared (K192275) for the **temporary reduction of waist, hip and thigh circumference**. Weight and fat-loss numbers on the page come from the manufacturer's report of trial NCT03811093 and are labeled that way, with a "results vary" disclaimer. Don't use the manufacturer's patient before/after photos as if they were studio results. Use your own clients' photos, with their written consent.

Images are from the manufacturer's site (invisaredtech.com), for use as an invisa-RED provider.
