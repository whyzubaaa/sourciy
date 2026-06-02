# Sourcify

> Find the source. Stop overpaying middlemen.

Sourcify finds the products you see on Russian marketplaces at their real 
wholesale price on Chinese platforms — where resellers actually buy.

---

## The problem

Thousands of people resell goods bought in China. But the entry barrier is high:
you need to know the platforms, search in Chinese, tell a trustworthy supplier
from a scam, and calculate logistics. Most either overpay agents or never start.

## The solution

Paste a marketplace product link (or upload a photo) → Sourcify finds the same
product at wholesale price, shows rated suppliers, and calculates the final
landed cost including delivery.

**Two search modes:**
- 🔗 **By link** — paste a product, get its wholesale equivalents
- 📷 **By photo** — upload an image, find visually similar products

**Each result shows:**
- Original price vs. wholesale price
- Savings in absolute value and %
- Direct link to supplier with rating
- Minimum order quantity (MOQ)
- Estimated delivery cost
- **Final landed cost** — what it really comes to

---

## Tech Stack

**Frontend**  
![Next.js](https://img.shields.io/badge/Next.js_14-000000?style=flat&logo=next.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React_18-61DAFB?style=flat&logo=react&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat&logo=tailwindcss&logoColor=white)

**Backend & Infrastructure**  
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat&logo=stripe&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)

---

## Architecture principle
The browser never talks to external providers directly. Everything goes through
our server. This keeps API keys server-side only, enforces rate limits and
plan tiers that can't be bypassed, and keeps business logic out of the client.

The data layer is decoupled through provider interfaces — adding a new source
platform means adding one adapter, not rewriting the app.

---

## Status

`In development` — core search and pricing engine in progress.

---

*Built solo. Full stack. Every decision made by one person.*
