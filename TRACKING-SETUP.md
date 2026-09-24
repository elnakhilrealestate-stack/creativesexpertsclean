# Creative Experts – Website Tracking Fixes

Updated 2026-09-24.

## Changes
- Kept the existing Google Tag Manager container: `GTM-P2WNZHLC`.
- Added GTM to all service pages (they previously lacked it).
- Added a site-wide dataLayer event listener for:
  - `phone_click` – clicks on `tel:` links.
  - `whatsapp_click` – clicks on `wa.me` / `api.whatsapp.com` links.
- Added `lead_form_submit` to the homepage quote form before opening WhatsApp.
- Fixed the malformed FAQPage JSON-LD on the homepage.
- Fixed broken relative service links inside service-page footers (`services/...` -> `../services/...`).
- Cleaned the sitemap so it contains canonical page URLs without `#fragment` entries.

## Google Tag Manager next step
Create Custom Event triggers for `phone_click`, `whatsapp_click`, and `lead_form_submit`, then send each event to GA4. After confirming the events in GA4, import/create the corresponding Google Ads conversions.
