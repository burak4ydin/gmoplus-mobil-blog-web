# Task Backlog — gmoplus-mobil-blog-web

## P0 — Critical / Blocking
- [ ] None currently blocking deployment

## P1 — High Priority
- [ ] Wrong domain in .env.example: `NEXT_PUBLIC_APP_URL=https://blog.auto.gmoplus.com` — must be `https://blog.mobil.gmoplus.com` in Coolify env
- [ ] `NEXT_PUBLIC_VERTICAL=mobil` not set in .env.example — vertical-config defaults to `online`; set explicitly in Coolify

## P2 — Medium Priority
- [ ] Newsletter CTA has no backend endpoint wired
- [ ] No sitemap.ts or robots.ts — search engine crawl directives absent
- [ ] No canonical URL meta tag on article pages — risk of duplicate content penalty

## P3 — Low Priority
- [ ] LanguageSwitcher locale list hardcoded — should read from next-intl routing config
- [ ] ReadingProgress scroll handler not throttled
- [ ] No 404 illustration/image on not-found page