# Molepo Logistics Holdings — Website

The public website for **Molepo Logistics Holdings**, a Johannesburg-based South African company focused on passenger transportation, fleet services and practical logistics solutions.

It is a single, mobile-first page with sections for services, about (mission and vision), how we work, and contact. The contact section includes an enquiry form whose submissions are collected by Netlify Forms.

## Technology

- Plain HTML, CSS and a small amount of vanilla JavaScript. There is no build step and nothing to install.
- **Netlify Forms** for the enquiry form (`enquiry`), with honeypot spam protection and an inline confirmation message. `/thank-you` is the fallback page if JavaScript is unavailable.
- Google Fonts: Inter (body and headings) and Instrument Serif (italic accents).

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The full website (styles and script are inline) |
| `thank-you.html` | Confirmation page shown after a form submission when JavaScript is off |
| `404.html` | Branded "page not found" page |
| `favicon.svg` | "ML" brand-mark icon |
| `netlify.toml` | Publishes the project root and adds security headers |

## Running locally

Open `index.html` in a browser. To test the enquiry form locally, run `netlify dev` from the project root.

## Managing enquiries

Submissions appear in the Netlify dashboard under **Forms → enquiry**. To get an email for every new enquiry, add an email notification under **Forms → Form notifications**.

## Before sharing widely

- Confirm the wording, email address and phone numbers are correct.
- The site intentionally makes no claims about fleet size, licences, clients, years of experience, certifications or service areas. Add these only once confirmed.
- A custom domain (for example `molepologistics.co.za`) can be registered and connected in Netlify's domain settings when the company is ready.
