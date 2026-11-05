# AGENTS.md

## Architecture
A static, single-page marketing site for Molepo Logistics Holdings. There is no framework, package.json or build step. Netlify publishes the repository root (`netlify.toml` → `publish = "."`).

- `index.html` holds everything: CSS in `<style>`, an inline SVG icon sprite (`<symbol id="i-*">`, used with `<use href="#i-…">`), the page sections, and one IIFE `<script>` at the end.
- `thank-you.html` / `404.html` are self-contained pages that share the same palette.
- `.netlify/features/netlify-forms` is a marker that tells the deploy pipeline to enable form detection. Do not delete it.

## Page sections (in order)
`#home` hero → `#services` → `#about` → `#approach` (dark) → `#contact` (enquiry form + contact panel) → footer. A fixed `.quickbar` (Call / Enquire) appears only at ≤720px.

## Conventions
- Design tokens are CSS custom properties in `:root` (forest green `--green`, cream `--cream`, sand/gold accents). Reuse them; don't hard-code new colours.
- Headings use Inter 800; `<em>` inside `h1`/`h2` is set in Instrument Serif italic as the accent style.
- Breakpoints: 960px, 880px (single-column layouts), 720px (mobile menu, quickbar, hidden top bar).
- Elements with `.reveal` fade in on scroll only when JS adds the `js` class to `<html>`, so content stays visible without JS. `prefers-reduced-motion` disables all animation.
- Keep it build-free. Don't add a bundler or framework unless the product owner asks for one.

## Enquiry form (Netlify Forms)
- Form name `enquiry`. Fields: `name`, `organisation`, `email`, `phone`, `service`, `preferred-date`, `location`, `message`, plus hidden `form-name`, `subject` and the honeypot `bot-field`.
- JS submits URL-encoded data to `/` and shows the inline `#formSuccess` state. Without JS, the form posts to `/thank-you`.
- Service cards carry `data-service="…"`, which pre-selects the matching `<option>`. Keep those values identical to the option text.
- If you rename or remove fields, older submissions keep their data but the UI shows only the current fields.

## Content rules
Don't invent facts (fleet size, licences, clients, years in operation, certifications, service areas, prices). The contact details must stay consistent across the top bar, hero, contact panel, footer, quickbar, thank-you page and JSON-LD block.
