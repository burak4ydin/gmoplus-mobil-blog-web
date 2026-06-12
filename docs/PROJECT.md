# gmoplus-mobil-blog-web

## What It Does
Read-only Next.js blog frontend for the GMOPlus Mobil vertical. Renders articles from gmoplus-blog-api. Structurally identical to all other vertical blog frontends; vertical identity set via `vertical-config.ts` using the `mobil` key.

## Who Uses It
- Public visitors reading app reviews, mobile tech content, and platform news for the Mobil vertical
- SEO and content marketing for mobil.gmoplus.com

## Key Features
- Article list, detail, category, tag, author, search pages
- next-intl internationalised routing (`[locale]/`)
- Vertical branding: orange (#F97316), nav links for Apps and Reviews
- Reading progress bar, related posts, share buttons, sidebar search
- HTML content sanitisation via isomorphic-dompurify
- Newsletter CTA (no backend wired)

## Business Flow
1. Visitor arrives via organic search or links from mobil.gmoplus.com
2. Fetches articles from `NEXT_PUBLIC_BLOG_API_URL`
3. Content rendered from sanitised HTML

## Success Criteria
- Articles render correctly with author attribution
- Category and tag pages filter to relevant articles
- Domain correctly set to `blog.mobil.gmoplus.com`