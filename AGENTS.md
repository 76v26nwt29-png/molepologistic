# AGENTS.md

## Architecture
This is a static Cloudflare Pages site built with plain HTML, CSS and vanilla JavaScript. There is no package manager, framework or build step. Cloudflare Pages publishes the repository root.

## Main pages
- `index.html`: corporate homepage, service overview and client-side WhatsApp quotation request form.
- `services/*.html`: dedicated service information pages.
- `company-profile.html`: print-ready company profile.
- `privacy.html`: POPIA-oriented privacy notice.
- `404.html`: not-found page.
- `assets/`: brand marks and social preview artwork.

## Enquiry form
The form validates required fields and prepares a WhatsApp message addressed to +27 84 240 9561. It opens WhatsApp; the visitor must review and press Send. The website does not store or independently submit form details. Do not describe this as a server-side form or automated bot.

## Content safeguards
- Do not invent fleet size, clients, licences, insurance status, certifications, fixed prices, service capacity or completed projects.
- Quote-based pricing only; no fixed price list.
- Do not publish a physical street address unless the company confirms it should be public.
- Confirm legal entity name and registration number against current CIPC documentation before production.
- Confirm that info@molepologistic.co.za is active and monitored before production.
- Use genuine company/vehicle photographs only when supplied or approved.
- Do not change the production branch without explicit approval.
- The new palette is graphite navy, mineral white and restrained cobalt blue; do not restore the previous green/cream/gold palette.
