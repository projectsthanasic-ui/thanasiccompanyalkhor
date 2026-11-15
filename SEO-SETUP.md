# SEO, Search Console, and Analytics setup

## Lead form

The contact form on the English landing page validates the required fields and opens a prefilled WhatsApp message to `+974 6624 6353`. The visitor must review and press Send in WhatsApp. This static site does not store or transmit submitted form data to a database. For direct email/CRM delivery, connect a form provider or backend and add its endpoint before launch.

## Google Search Console

Search Console ownership must be verified by the site owner; this repository cannot verify the Google account or domain. Recommended approach:

1. Open Google Search Console and add a **Domain** property for the domain you control.
2. Copy the DNS TXT verification value Google provides.
3. Add that TXT record at the domain's DNS provider, then click Verify in Search Console.
4. Submit `https://thanasiccompany.vercel.app/` or the domain sitemap after it is configured. If you connect a custom domain, use that domain consistently for canonical URLs and verification.
5. If you prefer HTML-tag verification instead, add Google's exact `<meta name="google-site-verification" content="...">` tag to both pages' `<head>` after obtaining the token. Do not publish a guessed token.

## Google Analytics 4

A GA4 property and Measurement ID are required. No fabricated ID is included and analytics will not send data until a real ID is configured.

1. Create a GA4 property and web data stream for the production domain.
2. Copy its Measurement ID (`G-XXXXXXXXXX`).
3. Add the official Google tag for that ID to the `<head>` of `index.html` and `ar/index.html`, or configure your consent-management/tag-manager setup.
4. Test with GA4 Realtime/DebugView and ensure your privacy notice and consent requirements are met for the regions you serve.

## Before launch

- Confirm the production domain and update canonical, hreflang, Open Graph, and JSON-LD URLs on both pages if it differs from `thanasiccompany.vercel.app`.
- Confirm business details, service areas, opening hours, pricing, and claims are accurate.
- Add a privacy notice explaining contact-data handling before collecting leads.
- Replace stock photos with company-owned images where available and ensure image licenses/consent are in order.
