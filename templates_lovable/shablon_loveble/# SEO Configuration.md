# SEO Configuration - SmartBook Platform

**Last Updated:** 2025-11-10  
**Status:** Template (to be filled)  
**Owner:** [TEAM MEMBER]

---

## 📋 Table of Contents

1. [Global SEO Settings](#global-seo-settings)
2. [Per-Page SEO](#per-page-seo)
3. [Structured Data Templates](#structured-data-templates)
4. [Technical SEO](#technical-seo)
5. [International SEO](#international-seo)
6. [Image SEO](#image-seo)
7. [Testing & Validation](#testing--validation)

---

## 1. Global SEO Settings

### 1.1 Brand Keywords

**Primary Keywords** (Target across site):
- [KEYWORD 1 - e.g., "AI booking platform"]
- [KEYWORD 2 - e.g., "expert consultation scheduling"]
- [KEYWORD 3 - e.g., "automated appointment booking"]

**Secondary Keywords**:
- [KEYWORD 4]
- [KEYWORD 5]
- [KEYWORD 6]

**Long-Tail Keywords** (for blog/docs):
- [LONG-TAIL 1 - e.g., "how to schedule consultations with AI"]
- [LONG-TAIL 2]
- [LONG-TAIL 3]

### 1.2 Brand Entities

**Primary Entity**: [BRAND NAME]  
**Entity Type**: SaaS Platform, Booking Software  
**Entity Location**: [CITY, COUNTRY]  
**Founded**: [YEAR]  
**Founder**: [NAME]  

**Social Profiles** (for sameAs in Organization schema):
- LinkedIn: [URL]
- Twitter: [URL]
- Facebook: [URL]
- GitHub: [URL]

### 1.3 Global Meta Tags (index.html)

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="author" content="[BRAND NAME]" />
    <meta name="theme-color" content="#[PRIMARY_COLOR_HEX]" />
    
    <!-- Favicon -->
    <link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png" />
    <link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png" />
    <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png" />
    <link rel="manifest" href="/site.webmanifest" />
    
    <!-- Primary Meta Tags -->
    <title>[BRAND] - [TAGLINE]</title>
    <meta name="title" content="[BRAND] - [TAGLINE]" />
    <meta name="description" content="[GLOBAL DESCRIPTION - 150-160 chars]" />
    <meta name="keywords" content="[KEYWORD1], [KEYWORD2], [KEYWORD3]" />
    
    <!-- Open Graph / Facebook -->
    <meta property="og:type" content="website" />
    <meta property="og:url" content="https://[DOMAIN]/" />
    <meta property="og:title" content="[BRAND] - [TAGLINE]" />
    <meta property="og:description" content="[OG DESCRIPTION]" />
    <meta property="og:image" content="https://[DOMAIN]/og-image.jpg" />
    <meta property="og:locale" content="en_US" />
    <meta property="og:locale:alternate" content="uk_UA" />
    
    <!-- Twitter -->
    <meta name="twitter:card" content="summary_large_image" />
    <meta name="twitter:url" content="https://[DOMAIN]/" />
    <meta name="twitter:title" content="[BRAND] - [TAGLINE]" />
    <meta name="twitter:description" content="[TWITTER DESCRIPTION]" />
    <meta name="twitter:image" content="https://[DOMAIN]/twitter-card.jpg" />
    <meta name="twitter:site" content="@[HANDLE]" />
    
    <!-- Canonical -->
    <link rel="canonical" href="https://[DOMAIN]/" />
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.tsx"></script>
  </body>
</html>
```

---

## 2. Per-Page SEO

### 2.1 Homepage (`/`)

**Meta Title EN**: `[BRAND] - [TAGLINE] | AI-Powered Booking Platform`  
**Meta Title UA**: `[BRAND] - [TAGLINE_UA] | Платформа для бронювання з AI`

**Meta Description EN** (150-160 chars):  
`[DESCRIPTION - e.g., "Book expert consultations instantly with AI-powered scheduling. Real-time availability, seamless payments, 24/7 support. Start free today."]`

**Meta Description UA**:  
`[DESCRIPTION_UA]`

**Primary Keywords**: [KEYWORD1], [KEYWORD2]  
**H1 EN**: `[HEADLINE - e.g., "Smart Booking That Adapts to You"]`  
**H1 UA**: `[HEADLINE_UA]`

**Canonical URL**: `https://[DOMAIN]/`  
**hreflang**:
- `en`: `https://[DOMAIN]/`
- `uk`: `https://[DOMAIN]/ua/`

**Open Graph Image**: `/images/og/homepage-en.jpg` (1200x630px)

---

### 2.2 Login Page (`/login`)

**Meta Title EN**: `Login | [BRAND]`  
**Meta Title UA**: `Вхід | [BRAND]`

**Meta Description EN**:  
`Log in to your [BRAND] account to manage bookings, view schedules, and access expert consultations.`

**Meta Description UA**:  
`[DESCRIPTION_UA]`

**robots**: `noindex, nofollow` (auth pages should NOT be indexed)

---

### 2.3 Booking Page (`/booking`)

**Meta Title EN**: `Book a Consultation | [BRAND]`  
**Meta Title UA**: `Забронювати консультацію | [BRAND]`

**Meta Description EN**:  
`Schedule your expert consultation in minutes. Choose from [X] verified professionals across [Y] industries. Instant confirmation.`

**Meta Description UA**:  
`[DESCRIPTION_UA]`

**Primary Keywords**: book consultation, schedule appointment, [BRAND] booking  
**H1 EN**: `Book Your Expert Consultation`  
**H1 UA**: `[H1_UA]`

**Canonical URL**: `https://[DOMAIN]/booking`  
**Open Graph Image**: `/images/og/booking-en.jpg`

---

### 2.4 Industries Page Template (`/industries/:slug`)

**Dynamic Meta Title EN**: `[INDUSTRY_NAME] Consultations | [BRAND]`  
**Example**: `Coaching Consultations | [BRAND]`

**Meta Description EN** (Template):  
`Book expert [INDUSTRY_NAME] consultations. Connect with top professionals in [INDUSTRY]. [X] verified experts, instant booking.`

**Primary Keywords**: [INDUSTRY] consultation, [INDUSTRY] expert, book [INDUSTRY]  
**H1 EN** (Dynamic): `[INDUSTRY_NAME] Consultations Made Simple`

**Canonical URL**: `https://[DOMAIN]/industries/[SLUG]`  
**Open Graph Image**: `/images/og/industries-[SLUG]-en.jpg`

---

### 2.5 Blog List (`/blog`)

**Meta Title EN**: `Blog - Insights & Updates | [BRAND]`  
**Meta Description EN**:  
`Expert insights on scheduling, productivity, and professional consultations. Tips, case studies, and industry trends.`

**Primary Keywords**: [BRAND] blog, scheduling tips, consultation insights  
**H1 EN**: `Insights & Updates`

**Canonical URL**: `https://[DOMAIN]/blog`

---

### 2.6 Blog Post Template (`/blog/:slug`)

**Dynamic Meta Title EN**: `[POST_TITLE] | [BRAND] Blog`  
**Meta Description EN** (from post excerpt, max 160 chars)

**Primary Keywords**: (from post content/tags)  
**H1 EN**: `[POST_TITLE]`

**Structured Data**: Article schema (see section 3.3)

**Canonical URL**: `https://[DOMAIN]/blog/[SLUG]`  
**Open Graph Image**: `[POST_FEATURED_IMAGE]` (1200x630px)

---

### 2.7 About Page (`/about`)

**Meta Title EN**: `About Us | [BRAND]`  
**Meta Description EN**:  
`Learn about [BRAND]'s mission to revolutionize professional consultations with AI-powered scheduling. Our story, team, and values.`

**H1 EN**: `About [BRAND]`

---

### 2.8 Documentation (`/docs`)

**Meta Title EN**: `Documentation - Getting Started | [BRAND]`  
**Meta Description EN**:  
`Complete guide to [BRAND]. Learn how to book consultations, manage schedules, integrate calendars, and more.`

**H1 EN**: `Documentation`

**Structured Data**: HowTo schema for tutorials (see section 3.4)

---

### 2.9 Team Page (`/team`)

**Meta Title EN**: `Our Team | [BRAND]`  
**Meta Description EN**:  
`Meet the [BRAND] team. [X] professionals dedicated to transforming professional consultations with technology.`

**Structured Data**: Person schema for each team member (see section 3.5)

---

### 2.10 Legal Pages

**Terms of Use** (`/terms`):
- Meta Title: `Terms of Use | [BRAND]`
- robots: `noindex, follow` (legal pages typically noindex)

**Privacy Policy** (`/privacy`):
- Meta Title: `Privacy Policy | [BRAND]`
- robots: `noindex, follow`

---

## 3. Structured Data Templates

### 3.1 Organization Schema (Global - for all pages)

**Location**: `index.html` or global layout component  
**Type**: `https://schema.org/Organization`

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "[BRAND_NAME]",
  "legalName": "[LEGAL_NAME]",
  "url": "https://[DOMAIN]",
  "logo": "https://[DOMAIN]/logo.png",
  "foundingDate": "[YYYY-MM-DD]",
  "founders": [
    {
      "@type": "Person",
      "name": "[FOUNDER_NAME]"
    }
  ],
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[STREET]",
    "addressLocality": "[CITY]",
    "addressRegion": "[REGION]",
    "postalCode": "[ZIP]",
    "addressCountry": "[COUNTRY_CODE]"
  },
  "contactPoint": {
    "@type": "ContactPoint",
    "contactType": "Customer Support",
    "telephone": "+[PHONE]",
    "email": "support@[DOMAIN]",
    "availableLanguage": ["English", "Ukrainian"]
  },
  "sameAs": [
    "https://twitter.com/[HANDLE]",
    "https://linkedin.com/company/[HANDLE]",
    "https://facebook.com/[HANDLE]",
    "https://github.com/[HANDLE]"
  ],
  "description": "[BRAND_DESCRIPTION_1_SENTENCE]"
}
```

---

### 3.2 Service Schema (Homepage, Industries)

```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "serviceType": "Professional Consultation Booking",
  "provider": {
    "@type": "Organization",
    "name": "[BRAND_NAME]"
  },
  "areaServed": {
    "@type": "Country",
    "name": "[COUNTRIES_SERVED]"
  },
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Consultation Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "[SERVICE_NAME_1 - e.g., Business Coaching]"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "[SERVICE_NAME_2]"
        }
      }
    ]
  },
  "availableChannel": {
    "@type": "ServiceChannel",
    "serviceUrl": "https://[DOMAIN]/booking",
    "serviceType": "Online Booking"
  }
}
```

---

### 3.3 Article Schema (Blog Posts)

```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "[POST_TITLE]",
  "description": "[POST_EXCERPT]",
  "image": "https://[DOMAIN]/images/blog/[POST_IMAGE].jpg",
  "datePublished": "[YYYY-MM-DDTHH:MM:SSZ]",
  "dateModified": "[YYYY-MM-DDTHH:MM:SSZ]",
  "author": {
    "@type": "Person",
    "name": "[AUTHOR_NAME]",
    "url": "https://[DOMAIN]/team/[AUTHOR_SLUG]"
  },
  "publisher": {
    "@type": "Organization",
    "name": "[BRAND_NAME]",
    "logo": {
      "@type": "ImageObject",
      "url": "https://[DOMAIN]/logo.png"
    }
  },
  "mainEntityOfPage": {
    "@type": "WebPage",
    "@id": "https://[DOMAIN]/blog/[POST_SLUG]"
  },
  "articleSection": "[CATEGORY]",
  "keywords": "[KEYWORD1], [KEYWORD2], [KEYWORD3]",
  "wordCount": [WORD_COUNT],
  "inLanguage": "en-US"
}
```

---

### 3.4 HowTo Schema (Documentation)

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "[TUTORIAL_TITLE - e.g., How to Book Your First Consultation]",
  "description": "[TUTORIAL_DESCRIPTION]",
  "image": "https://[DOMAIN]/images/docs/[IMAGE].jpg",
  "totalTime": "PT[X]M",
  "step": [
    {
      "@type": "HowToStep",
      "position": 1,
      "name": "[STEP_1_TITLE]",
      "text": "[STEP_1_DESCRIPTION]",
      "image": "https://[DOMAIN]/images/docs/step1.jpg"
    },
    {
      "@type": "HowToStep",
      "position": 2,
      "name": "[STEP_2_TITLE]",
      "text": "[STEP_2_DESCRIPTION]"
    },
    {
      "@type": "HowToStep",
      "position": 3,
      "name": "[STEP_3_TITLE]",
      "text": "[STEP_3_DESCRIPTION]"
    }
  ]
}
```

---

### 3.5 Person Schema (Team Members)

```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "[PERSON_NAME]",
  "jobTitle": "[JOB_TITLE]",
  "worksFor": {
    "@type": "Organization",
    "name": "[BRAND_NAME]"
  },
  "url": "https://[DOMAIN]/team/[PERSON_SLUG]",
  "image": "https://[DOMAIN]/images/team/[PERSON_IMAGE].jpg",
  "sameAs": [
    "https://linkedin.com/in/[PERSON_LINKEDIN]",
    "https://twitter.com/[PERSON_TWITTER]"
  ],
  "description": "[BIO_1_SENTENCE]"
}
```

---

### 3.6 FAQPage Schema (Homepage, Docs, Industries)

**CRITICAL for GEO** - include on every major page

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "[QUESTION_1 - e.g., What is [BRAND]?]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[ANSWER_1 - 1-3 sentences, definitive]"
      }
    },
    {
      "@type": "Question",
      "name": "[QUESTION_2 - e.g., How does [BRAND] work?]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[ANSWER_2]"
      }
    },
    {
      "@type": "Question",
      "name": "[QUESTION_3 - e.g., Is [BRAND] free?]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[ANSWER_3]"
      }
    }
  ]
}
```

---

## 4. Technical SEO

### 4.1 robots.txt

**Location**: `/public/robots.txt`

```
User-agent: *
Allow: /

# Disallow auth and admin pages
Disallow: /login
Disallow: /signup
Disallow: /admin/
Disallow: /api/

# Disallow dynamic user pages (if any)
Disallow: /dashboard/
Disallow: /profile/

# Allow CSS and JS for rendering
Allow: /*.css$
Allow: /*.js$

# Crawl-delay (optional, for aggressive crawlers)
# Crawl-delay: 10

# Sitemap
Sitemap: https://[DOMAIN]/sitemap.xml
```

---

### 4.2 sitemap.xml

**Generation**: Auto-generate with script or library (e.g., `sitemap` npm package)

**Include**:
- Homepage: `/`
- Static pages: `/about`, `/team`, `/careers`, `/booking`
- Industries: `/industries/[slug]` (all published)
- Blog: `/blog`, `/blog/[slug]` (all published posts)
- Docs: `/docs`, `/docs/[section]/[page]` (all doc pages)

**Exclude**:
- Auth pages: `/login`, `/signup`
- Admin pages: `/admin/*`
- User dashboards: `/dashboard/*`, `/profile/*`
- API routes: `/api/*`

**Example sitemap.xml structure**:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://[DOMAIN]/</loc>
    <lastmod>2025-11-10</lastmod>
    <changefreq>weekly</changefreq>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://[DOMAIN]/about</loc>
    <lastmod>2025-11-10</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
  <!-- Add more URLs -->
</urlset>
```

**Update frequency**:
- Static pages: monthly or on content change
- Blog: weekly (or on new post)
- Industries: monthly

---

### 4.3 Canonical URLs

**Implementation**: Use `<link rel="canonical" href="..." />` on ALL pages

**Rules**:
- Always point to the "main" version of a page
- Include protocol (https://)
- Include trailing slash (consistent)
- For paginated pages: point first page to `/blog`, subsequent pages to `/blog?page=2`

**Example (React Helmet or meta tags)**:
```tsx
<Helmet>
  <link rel="canonical" href={`https://[DOMAIN]${location.pathname}`} />
</Helmet>
```

---

### 4.4 Performance Optimization

**Image Optimization**:
1. **Format**: Use WebP (fallback to JPEG/PNG)
2. **Compression**: TinyPNG, ImageOptim, or Lovable's built-in optimization
3. **Lazy Loading**: Use `loading="lazy"` for below-the-fold images
4. **Responsive Images**: Use `srcset` and `sizes`
   ```html
   <img 
     src="/images/hero.webp" 
     srcset="/images/hero-640.webp 640w, /images/hero-1280.webp 1280w, /images/hero-1920.webp 1920w"
     sizes="(max-width: 640px) 640px, (max-width: 1280px) 1280px, 1920px"
     alt="[DESCRIPTIVE_ALT]"
     loading="lazy"
     width="1920"
     height="1080"
   />
   ```

**Font Loading**:
- Use `font-display: swap` (already in Tailwind)
- Preload critical fonts:
  ```html
  <link rel="preload" href="/fonts/Inter-Regular.woff2" as="font" type="font/woff2" crossorigin />
  ```

**Critical CSS**:
- Inline critical CSS for above-the-fold content (optional)
- Use Vite's built-in code splitting

**Core Web Vitals Targets**:
- **LCP** (Largest Contentful Paint): < 2.5s
  - Optimize hero images
  - Use CDN for assets
- **FID** (First Input Delay): < 100ms
  - Minimize JavaScript execution time
  - Use React.lazy() for code splitting
- **CLS** (Cumulative Layout Shift): < 0.1
  - Always specify width/height for images
  - Avoid dynamic content above-the-fold

---

## 5. International SEO (EN/UA)

### 5.1 hreflang Implementation

**Method 1: HTML `<link>` tags** (in `<head>`):
```html
<link rel="alternate" hreflang="en" href="https://[DOMAIN]/page" />
<link rel="alternate" hreflang="uk" href="https://[DOMAIN]/ua/page" />
<link rel="alternate" hreflang="x-default" href="https://[DOMAIN]/page" />
```

**Method 2: HTTP headers** (for non-HTML files):
```
Link: <https://[DOMAIN]/page>; rel="alternate"; hreflang="en",
      <https://[DOMAIN]/ua/page>; rel="alternate"; hreflang="uk",
      <https://[DOMAIN]/page>; rel="alternate"; hreflang="x-default"
```

**Method 3: Sitemap** (if many pages):
```xml
<url>
  <loc>https://[DOMAIN]/page</loc>
  <xhtml:link rel="alternate" hreflang="en" href="https://[DOMAIN]/page" />
  <xhtml:link rel="alternate" hreflang="uk" href="https://[DOMAIN]/ua/page" />
  <xhtml:link rel="alternate" hreflang="x-default" href="https://[DOMAIN]/page" />
</url>
```

**Recommended**: Method 1 (HTML tags) for simplicity with React

---

### 5.2 URL Structure

**Chosen Strategy**: Subdirectory (RECOMMENDED)

**English (default)**:
- Homepage: `https://[DOMAIN]/`
- About: `https://[DOMAIN]/about`
- Blog: `https://[DOMAIN]/blog/post-slug`

**Ukrainian**:
- Homepage: `https://[DOMAIN]/ua/`
- About: `https://[DOMAIN]/ua/about`
- Blog: `https://[DOMAIN]/ua/blog/post-slug`

**Implementation (React Router)**:
```tsx
<Routes>
  <Route path="/" element={<HomePage />} />
  <Route path="/ua/" element={<HomePage lang="ua" />} />
  <Route path="/about" element={<AboutPage />} />
  <Route path="/ua/about" element={<AboutPage lang="ua" />} />
  {/* ... */}
</Routes>
```

---

### 5.3 Language Switcher

**UI**:
- Location: Top navigation (right corner)
- Design: Dropdown or toggle (EN | UA)
- Mobile: Accessible in mobile menu

**Behavior**:
1. User clicks language switcher
2. Switch to corresponding URL (e.g., `/about` → `/ua/about`)
3. Save preference to `localStorage`
4. Update `<html lang="...">` attribute
5. Update all i18n content

**Implementation (React)**:
```tsx
const LanguageSwitcher = () => {
  const { i18n } = useTranslation();
  const navigate = useNavigate();
  const location = useLocation();

  const switchLanguage = (lang: 'en' | 'ua') => {
    const newPath = lang === 'ua' 
      ? `/ua${location.pathname}`
      : location.pathname.replace(/^\/ua/, '');
    
    i18n.changeLanguage(lang);
    localStorage.setItem('preferred_language', lang);
    navigate(newPath);
  };

  return (
    <select value={i18n.language} onChange={(e) => switchLanguage(e.target.value)}>
      <option value="en">EN</option>
      <option value="ua">UA</option>
    </select>
  );
};
```

---

## 6. Image SEO

### 6.1 Filename Conventions

**Format**: `descriptive-keyword-rich-name.webp`

**Examples**:
- ❌ `IMG_1234.jpg`
- ❌ `screenshot.png`
- ✅ `ai-booking-platform-hero.webp`
- ✅ `expert-consultation-dashboard-screenshot.webp`
- ✅ `team-member-john-doe.jpg`

---

### 6.2 Alt Text Guidelines

**Format**: Descriptive + context + keyword (when relevant)

**Examples**:
- Hero image: `AI-powered booking platform interface showing real-time calendar`
- Team photo: `[PERSON_NAME], [ROLE] at [BRAND], smiling in office`
- Icon: `Calendar icon representing scheduling feature`
- Decorative: `alt=""` (empty, not missing)

**Bad Alt Text**:
- ❌ `image`
- ❌ `photo`
- ❌ `IMG_1234`

**Good Alt Text**:
- ✅ `Dashboard showing booking analytics and upcoming consultations`
- ✅ `Mobile app interface for booking expert consultations`

---

### 6.3 Image Optimization Checklist

- [ ] **Format**: WebP (with JPEG/PNG fallback for old browsers)
- [ ] **Size**: 
  - Hero images: < 300KB
  - Thumbnails: < 50KB
  - Icons: SVG (scalable, small)
- [ ] **Dimensions**: 
  - OG images: 1200x630px
  - Blog thumbnails: 800x450px (16:9)
  - Team photos: 400x400px (square)
- [ ] **Lazy loading**: `loading="lazy"` for below-the-fold images
- [ ] **Width/Height**: Always specify to prevent CLS
- [ ] **Srcset**: Use responsive images for different screen sizes
- [ ] **Alt text**: Descriptive + keyword-rich
- [ ] **Filename**: Descriptive + hyphens + keyword

---

## 7. Testing & Validation

### 7.1 SEO Testing Tools

**Pre-Launch Checklist**:
1. **Google Search Console**:
   - Verify domain ownership
   - Submit sitemap
   - Check mobile usability
   - Fix any indexing errors

2. **Google Rich Results Test**:
   - URL: https://search.google.com/test/rich-results
   - Validate ALL structured data (Organization, FAQPage, Article, etc.)
   - Fix any errors before launch

3. **Schema.org Validator**:
   - URL: https://validator.schema.org/
   - Paste JSON-LD code
   - Ensure no warnings/errors

4. **Lighthouse (Chrome DevTools)**:
   - Run on ALL major pages (homepage, blog, docs, booking)
   - Target: 90+ score on Performance, Accessibility, Best Practices, SEO
   - Fix any critical issues

5. **PageSpeed Insights**:
   - URL: https://pagespeed.web.dev/
   - Test on mobile AND desktop
   - Check Core Web Vitals
   - Target: "Good" for all metrics

6. **Mobile-Friendly Test**:
   - URL: https://search.google.com/test/mobile-friendly
   - Ensure all pages pass

7. **Broken Link Checker**:
   - Use tool like Screaming Frog or online checker
   - Fix all 404 errors

---

### 7.2 Ongoing Monitoring

**Weekly**:
- [ ] Check Google Search Console for new errors/warnings
- [ ] Monitor Core Web Vitals
- [ ] Review top search queries (GSC → Performance)

**Monthly**:
- [ ] Review organic traffic (Google Analytics)
- [ ] Update sitemap if new pages added
- [ ] Re-test top 5 pages with Lighthouse
- [ ] Check for new backlinks (Ahrefs, SEMrush, or Google Search Console)

**Quarterly**:
- [ ] Full site audit (Screaming Frog, Sitebulb)
- [ ] Refresh old blog content (update dates, add new info)
- [ ] Review and update meta titles/descriptions
- [ ] Competitor analysis (keywords, backlinks, content gaps)

---

### 7.3 Key Metrics to Track

**SEO KPIs**:
1. **Organic Traffic**: Google Analytics → Acquisition → All Traffic → Channels → Organic Search
2. **Keyword Rankings**: Track top 10 keywords (Google Search Console or SEMrush)
3. **Click-Through Rate (CTR)**: GSC → Performance → Average CTR
4. **Impressions**: GSC → Performance → Total Impressions
5. **Average Position**: GSC → Performance → Average Position (target: < 10)
6. **Core Web Vitals**: PageSpeed Insights or GSC → Experience
7. **Indexed Pages**: GSC → Coverage → Valid (should match sitemap)
8. **Crawl Errors**: GSC → Coverage → Errors (target: 0)

---

## 📋 SEO Readiness Checklist

### Pre-Launch
- [ ] All meta titles/descriptions written (EN + UA)
- [ ] All structured data implemented and validated
- [ ] robots.txt configured
- [ ] sitemap.xml generated
- [ ] Canonical URLs on all pages
- [ ] hreflang tags for EN/UA
- [ ] All images have alt text
- [ ] All images optimized (WebP, lazy loading)
- [ ] Lighthouse score 90+ on key pages
- [ ] Google Search Console verified
- [ ] Open Graph images created (1200x630px)
- [ ] Twitter Cards tested (Twitter Card Validator)
- [ ] Mobile responsive (Google Mobile-Friendly Test)

### Post-Launch
- [ ] Submit sitemap to Google Search Console
- [ ] Submit sitemap to Bing Webmaster Tools
- [ ] Set up Google Analytics
- [ ] Set up Google Tag Manager (optional)
- [ ] Request indexing for key pages (GSC → URL Inspection)
- [ ] Monitor crawl errors (GSC → Coverage)
- [ ] Set up weekly SEO report (automated)

---

**End of SEO Configuration**