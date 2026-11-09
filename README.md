# Tethr

Tethr was a web app for booking a caregiver the way you book a ride. A family enters an address, picks a date, time and visit length, and sends a request to a caregiver nearby. The caregiver accepts or declines.

I was cofounder and CEO. I wrote the spec, designed the UI, and built the web app with Claude Code in 13 days, from Aug 26 to Sep 7, 2026 (204 commits). We ran it as a private, invite only pilot with families from our waitlist.

![Start screen: search for care near an address](screenshots/start.png)

![Booking screen: address, building type, who the visit is for, date, time and visit length, next to a live map](screenshots/book-a-visit.png)

## Why we built it

On cold calls, agencies told me same day care is not how their industry works. We wanted a family to be able to book a caregiver in minutes.

## How it works

- Next.js app on Cloudflare Workers, served at jointethr.app/app
- Supabase for sign in and the database
- Family side: address search with a live map, booking details and request status
- Caregiver side: set availability, then accept or decline each request
- Operator console with live visitor counts and charts
- Security pass before launch covering authorization, CSRF, credentials and rate limits

## Code

The source is private because the app stored family addresses.

## Status

I left Tethr in November 2026. I'm now building [Nascoron](https://nascoron.com).
