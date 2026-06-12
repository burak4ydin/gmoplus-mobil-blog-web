# Architecture — gmoplus-mobil-blog-web

## Folder Structure
```
src/
  app/[locale]/
    [slug]/           Article detail
    author/[slug]/    Author page
    category/[slug]/  Category filtered articles
    tag/[slug]/       Tag filtered articles
    kategoriler/      All categories
    search/           Search results
    page.tsx          Homepage (featured + recent posts)
  components/
    blog/             PostCard, FeaturedPost, PostHeader, PostContent,
                      RelatedPosts, TagList, ShareButtons, ReadingProgress,
                      SidebarSearch, NewsletterCTA, CategoryBadge
    layout/           BlogHeader, BlogFooter, BlogSidebar, LanguageSwitcher
  lib/
    api.ts            Fetch wrapper for blog-api
    seo.ts            generateMetadata helpers
    vertical-config.ts All vertical branding (this repo uses `mobil` key)
  i18n/               next-intl request.ts, routing.ts
  middleware.ts       Locale detection
```

## Data Flow
```
Server component -> lib/api.ts fetch()
-> blog-api (NEXT_PUBLIC_BLOG_API_URL/blog/posts) -> JSON
-> PostContent (DOMPurify sanitised HTML) -> rendered page
```

## Service Communication
- Single upstream: `NEXT_PUBLIC_BLOG_API_URL` pointing to gmoplus-blog-api
- No authentication; fully public

## Auth Model
- None. Fully public read-only frontend.

## Note
This repo is a template clone of the other vertical blog frontends. The only meaningful differences per vertical are: `vertical-config.ts` active key, `NEXT_PUBLIC_APP_URL` env value, and `NEXT_PUBLIC_VERTICAL` env value. All three must be set correctly in Coolify for this vertical.