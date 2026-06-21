# etta biz — Next.js E-Commerce Store

A deploy-ready Next.js 15 + TypeScript + Tailwind CSS storefront for **etta biz**, an affordable women’s clothing business serving shoppers in Spain.

## What is included

- Premium dark/glass e-commerce homepage
- Product catalog and category pages
- Product detail pages with schema markup
- Local cart using Zustand persistence
- Demo checkout and confirmation flow
- Contact page with React Hook Form + Zod validation
- Netlify Forms-ready contact form
- Returns, privacy, terms, cookie policy, accessibility pages
- Branded 404 and error states
- Cookie consent banner with granular categories
- Sitemap and robots generation
- Security headers in `next.config.ts` and `netlify.toml`
- Simple `/admin` starter content editor with JSON import/export

## Important production note

This package is intentionally built as a complete deployable storefront MVP. The admin editor is a **starter local editor**, not a real secure multi-user CMS. It lets the owner edit/export content without touching code, but live publishing for all visitors should be connected to Sanity, Supabase, or another database-backed CMS before serious production use.

The checkout is a safe demo flow. Connect Stripe before taking real payments.

## Local setup

```bash
npm install
npm run dev
```

Open:

```text
http://localhost:3000
```

## Build locally

```bash
npm run build
npm run start
```

## Deploy to Netlify

1. Upload this project to GitHub, or drag the folder/zip into Netlify.
2. Netlify should detect the `netlify.toml` file.
3. Build command: `npm run build`
4. Publish directory: `.next`
5. Node version: `20`
6. Add environment variables in Netlify:

```text
NEXT_PUBLIC_SITE_URL=https://your-site-name.netlify.app
NEXT_PUBLIC_ADMIN_PASSCODE=replace-with-your-own-passcode
NEXT_PUBLIC_GA_ID=optional
```

## Admin access

Go to:

```text
/admin
```

Default local passcode:

```text
change-this-before-deploy
```

Change it in Netlify environment variables before deployment.

## Recommended next production upgrades

- Connect Sanity for real CMS publishing.
- Connect Stripe for live checkout.
- Connect Resend/Postmark for transactional emails.
- Replace placeholder SVG product visuals with real product photography.
- Add exact business address, delivery rates, and lawyer-reviewed legal copy.
- Add GA4 and Search Console verification.

## Acceptance checklist

- [x] Homepage answers what the business sells, who it serves, and why it matters.
- [x] Primary e-commerce CTA is `Shop Now / Add to Cart`.
- [x] Product discovery, trust proof, and checkout path are implemented.
- [x] Cart and checkout are functional as a demo journey.
- [x] Legal/support pages are present.
- [x] Deploy files for Netlify are included.
