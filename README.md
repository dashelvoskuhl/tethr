# Tethr

Tethr was a web app for booking a caregiver the way you book a ride. A family enters an address, picks a date, time and visit length, and sends a request to a caregiver nearby. The caregiver accepts or declines.

I was cofounder and CEO. I wrote the spec, designed the UI, and built the web app with Claude Code in 13 days, from Aug 26 to Sep 7, 2026 (204 commits). We ran it as a private, invite only pilot with families from our waitlist.

![Start screen: search for care near an address](screenshots/start.png)

![Booking screen: address, building type, who the visit is for, date, time and visit length, next to a live map](screenshots/book-a-visit.png)

## Why we built it

On cold calls, agencies told me same day care is not how their industry works. We wanted a family to be able to book a caregiver in minutes.

## How it works

- Next.js app on Cloudflare Workers (through OpenNext), served at jointethr.app/app
- Supabase for sign in and the Postgres database, with the household tables locked down
- Family side: address search with autocomplete and a live map, booking details, and request status
- Caregiver side: set availability, then accept or decline each request
- Operator console with live visitor counts and charts that refresh every ten seconds
- A security pass before launch covering authorization, CSRF protection, credentials and rate limits

## Designed around California law

Without a state license, Tethr could not assign caregivers or set their pay. So the family picks the caregiver, the caregiver accepts or declines, and the app never assigns anyone.

## Team

- Dash Voskuhl, cofounder and CEO: product, design and the web app
- Yousif, cofounder and CTO
- Harvey, cofounder and COO

## Code

The source stays private because the app stored family addresses and visit details. I'm happy to walk through it on a call.

## Status

I left Tethr in November 2026. I'm now building [Nascoron](https://nascoron.com).
