# TEMPLATE 7.1: SEO TECHNICAL OPTIMIZATION CHECKLIST

## 📋 PURPOSE
This template provides a comprehensive technical SEO checklist to ensure your multi-language SaaS website is fully optimized for search engines, including on-page SEO, technical infrastructure, and content optimization.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Implement SEO Technical Optimization based on the following specification:

## PROJECT SEO OVERVIEW

Primary Target Market: _______________
Languages Supported: _______________
Primary Keywords: _______________
Secondary Keywords: _______________
Long-tail Keywords: _______________

Competitor URLs for Analysis:
1. _______________
2. _______________
3. _______________

---

## ON-PAGE SEO CONFIGURATION

### Meta Tags Setup

#### Homepage Meta Tags
Title Tag: _______________
- Length: _______________ characters (50-60 optimal)
- Format: [Brand] - [Value Proposition] | [Category]
- Include Primary Keyword: [Yes/No]

Meta Description: _______________
- Length: _______________ characters (150-160 optimal)
- Include CTA: [Yes/No]
- Include Keywords: _______________

Meta Keywords: _______________ (optional, low priority)

Open Graph Tags:
- og:type: website
- og:title: _______________
- og:description: _______________
- og:image: _______________ (URL, 1200x630px)
- og:url: _______________
- og:site_name: _______________
- og:locale: _______________ (e.g., en_US)
- og:locale:alternate: _______________ (other languages)

Twitter Card Tags:
- twitter:card: summary_large_image
- twitter:site: _______________ (@username)
- twitter:creator: _______________ (@username)
- twitter:title: _______________
- twitter:description: _______________
- twitter:image: _______________ (URL)

Additional Meta Tags:
- [ ] theme-color: _______________
- [ ] apple-mobile-web-app-capable: yes
- [ ] apple-mobile-web-app-status-bar-style: _______________
- [ ] viewport: width=device-width, initial-scale=1

#### Page-Specific Meta Tags Template

For Each Page:
Page URL: _______________

Title Tag: _______________
Meta Description: _______________
Canonical URL: _______________
Alternate Language URLs:
- en: _______________
- [other lang]: _______________
- [other lang]: _______________

Focus Keyword: _______________
Secondary Keywords: _______________

Open Graph Tags: [Same structure as homepage]
Twitter Card Tags: [Same structure as homepage]

### Heading Structure Optimization

H1 Tag Rules:
- One H1 per page: [Enforced]
- H1 contains primary keyword: [Yes]
- H1 Length: _______________ characters (30-70 optimal)

Heading Hierarchy Rules:
- Proper nesting: H1 > H2 > H3 > H4 > H5 > H6
- No skipping levels: [Enforced]
- Descriptive headings: [Yes]
- Keyword inclusion: [Natural, not forced]

Page-by-Page Heading Structure:

Homepage:
- H1: _______________
- H2 Sections:
  1. _______________
  2. _______________
  3. _______________
  [Continue...]

Features Page:
- H1: _______________
- H2 Sections:
  1. _______________
  2. _______________
  [Continue...]

Pricing Page:
- H1: _______________
- H2 Sections:
  [Continue...]

[Continue for all major pages...]

### Content Optimization

Content Length Guidelines:
- Homepage: _______________ words minimum
- Feature Pages: _______________ words minimum
- Blog Posts: _______________ words minimum
- Use Case Pages: _______________ words minimum

Keyword Optimization:
- Primary keyword density: 1-2%
- LSI keywords usage: [Yes]
- Keyword stuffing: [Avoid]
- Natural language: [Priority]

Content Quality Checklist:
- [ ] Original content (no duplicate)
- [ ] Value-driven (answers user questions)
- [ ] Scannable (headings, bullets, short paragraphs)
- [ ] Updated regularly
- [ ] Grammar/spelling checked
- [ ] Mobile-friendly formatting
- [ ] Internal links included
- [ ] External authoritative links

Semantic HTML:
- [ ] Proper use of <header>, <nav>, <main>, <article>, <section>, <aside>, <footer>
- [ ] Lists use <ul>, <ol>, <li>
- [ ] Important text uses <strong>, not just bold
- [ ] Emphasized text uses <em>, not just italic
- [ ] Quotes use <blockquote>
- [ ] Code uses <code>, <pre>

### Image SEO Optimization

Image Guidelines:

File Naming:
- Format: descriptive-keyword-name.webp
- Avoid: image1.jpg, IMG_1234.png
- Include keywords: [Yes]
- Use hyphens: [Yes]

Alt Text Best Practices:
- Descriptive: [Yes]
- Include keywords naturally: [Yes]
- Length: _______________ characters max
- Decorative images: alt=""
- Format: [Describe what image shows]

Example Alt Text Template:
"[Primary subject] [doing what] [in what context]"

Image Format Priority:
1. WebP (modern browsers)
2. AVIF (next-gen, optional)
3. JPG/PNG (fallback)

Image Sizes:
- Hero images: _______________ KB max
- Feature images: _______________ KB max
- Thumbnails: _______________ KB max
- Icons: _______________ KB max (or inline SVG)

Responsive Images:
- Use srcset: [Yes]
- Use sizes attribute: [Yes]
- Lazy loading: [Yes, below fold]
- Loading="eager": [Hero image only]

Image Optimization Tools:
- [ ] ImageOptim
- [ ] TinyPNG
- [ ] Squoosh
- [ ] Built-in optimization: _______________

### Internal Linking Strategy

Link Structure:
- Descriptive anchor text: [Yes]
- Avoid "click here": [Yes]
- Keyword-rich anchors: [Natural usage]
- Follow link equity flow: [Yes]

Internal Link Guidelines:

Homepage Links To:
- Features: _______________
- Pricing: _______________
- Use Cases: _______________
- About: _______________
- Blog: _______________

Each Page Should Have:
- Minimum Internal Links: 3-5
- Maximum Internal Links: _______________ (no specific limit, but natural)
- Links to Higher-Level Pages: [Yes]
- Links to Related Content: [Yes]

Link Placement:
- [ ] Navigation menu
- [ ] Contextual in-content links
- [ ] Related pages section
- [ ] Footer links
- [ ] Breadcrumbs
- [ ] Sidebar (if applicable)

Orphan Pages Check: [No pages without internal links]

### External Linking Strategy

External Link Policy:
- Link to authoritative sources: [Yes]
- Open in new tab: [Yes/No] _______________
- Rel="nofollow" for sponsored: [Yes]
- Rel="noopener noreferrer" for security: [Yes]

Link Attributes:
- Affiliate links: rel="nofollow sponsored"
- User-generated content: rel="nofollow ugc"
- Trusted editorial: rel="follow" (default)

---

## TECHNICAL SEO INFRASTRUCTURE

### URL Structure Optimization

URL Format Rules:
- Pattern: [kebab-case] (lowercase, hyphens)
- Include keywords: [Yes]
- Keep short: [Yes] _______________ characters max
- Avoid parameters: [Prefer clean URLs]
- Remove stop words: [Optional] (a, an, the, etc.)

URL Examples:
Homepage: _______________
Features: _______________
Pricing: _______________
Blog Post: _______________
Use Case: _______________

Multi-Language URL Structure:
Format: [Subdirectory / Subdomain / ccTLD]

If Subdirectory:
- English: example.com/en/
- Ukrainian: example.com/uk/
- Pattern: [domain]/[lang]/[page]

If Subdomain:
- English: en.example.com/
- Ukrainian: uk.example.com/

If ccTLD:
- English: example.com
- Ukrainian: example.ua

Canonical URL Rules:
- Every page has canonical: [Yes]
- Self-referencing canonical: [Yes]
- HTTPS in canonical: [Yes]
- Trailing slash consistency: [Yes/No] _______________

URL Redirects:
- 301 for permanent: [Yes]
- 302 for temporary: [Yes]
- Redirect chains: [Avoid - max 1 redirect]
- Old URLs to redirect: _______________

### Robots.txt Configuration

Robots.txt Location: /robots.txt

Content:

```
User-agent: *
Disallow: /admin/
Disallow: /api/
Disallow: /private/
Disallow: [other restricted paths]

Allow: /

Sitemap: https://example.com/sitemap.xml
Sitemap: https://example.com/sitemap-images.xml (if applicable)
```

Blocked Paths:
- [ ] /admin/
- [ ] /api/
- [ ] /private/
- [ ] /_next/ (if Next.js)
- [ ] /node_modules/
- [ ] Other: _______________

Special Rules:
- Disallow certain bots: [Yes/No]
- Crawl-delay: [Yes/No] _______________ seconds

### XML Sitemap Configuration

Sitemap Location: /sitemap.xml

Sitemap Structure:
- [ ] Main sitemap (index)
- [ ] Pages sitemap
- [ ] Blog posts sitemap
- [ ] Images sitemap (optional)
- [ ] Videos sitemap (optional)
- [ ] Multi-language sitemaps

Pages to Include:
- [ ] Homepage
- [ ] All product/feature pages
- [ ] Pricing page
- [ ] About page
- [ ] Blog posts
- [ ] Use cases
- [ ] Legal pages: [Yes/No]

Pages to Exclude:
- [ ] Admin pages
- [ ] Thank you pages
- [ ] 404 error page
- [ ] Login/signup pages: [Yes/No]

Sitemap Properties:

For Each URL:
<url>
  <loc>_______________</loc>
  <lastmod>_______________ (YYYY-MM-DD)</lastmod>
  <changefreq>_______________ (always/hourly/daily/weekly/monthly/yearly/never)</changefreq>
  <priority>_______________ (0.0-1.0)</priority>
  <xhtml:link rel="alternate" hreflang="___" href="___" /> (multi-language)
</url>

Priority Guidelines:
- Homepage: 1.0
- Main pages (Features, Pricing): 0.8-0.9
- Secondary pages: 0.6-0.7
- Blog posts: 0.4-0.6
- Legal pages: 0.3-0.4

Change Frequency Guidelines:
- Homepage: weekly
- Product pages: monthly
- Blog: weekly/daily
- Legal pages: yearly

Auto-generation: [Yes/No]
Update Trigger: [On content change / Daily / Weekly]

Multi-Language Sitemap:
Include hreflang tags: [Yes]

### Structured Data (Schema.org)

Schema Implementation Format: [JSON-LD / Microdata]
Location: [<head> tag / End of <body>]

Required Schema Types:

1. Organization Schema (All pages)
```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "_______________",
  "url": "_______________",
  "logo": "_______________",
  "description": "_______________",
  "foundingDate": "_______________",
  "founders": [
    {
      "@type": "Person",
      "name": "_______________"
    }
  ],
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "_______________",
    "addressLocality": "_______________",
    "addressRegion": "_______________",
    "postalCode": "_______________",
    "addressCountry": "_______________"
  },
  "contactPoint": {
    "@type": "ContactPoint",
    "contactType": "customer support",
    "email": "_______________",
    "url": "_______________"
  },
  "sameAs": [
    "_______________ (LinkedIn)",
    "_______________ (Twitter)",
    "_______________ (Facebook)"
  ]
}
```

2. WebSite Schema (Homepage)
```json
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "name": "_______________",
  "url": "_______________",
  "potentialAction": {
    "@type": "SearchAction",
    "target": "_______________?q={search_term_string}",
    "query-input": "required name=search_term_string"
  }
}
```

3. SoftwareApplication Schema (Product pages)
```json
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "_______________",
  "operatingSystem": "_______________",
  "applicationCategory": "_______________",
  "offers": {
    "@type": "Offer",
    "price": "_______________",
    "priceCurrency": "_______________"
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "_______________",
    "ratingCount": "_______________"
  }
}
```

4. Offer Schema (Pricing page)
[Define for each pricing plan]

5. FAQPage Schema (FAQ sections)
```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "_______________",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "_______________"
      }
    }
  ]
}
```

6. BreadcrumbList Schema (All pages with breadcrumbs)

7. Article Schema (Blog posts)

8. HowTo Schema (Tutorial/Use case pages)

9. Review/Rating Schema (If testimonials)

10. JobPosting Schema (Careers page)

Schema Validation:
- Tool: Google Rich Results Test
- Validation URL: _______________
- Errors to fix: _______________

### Hreflang Tags (Multi-Language)

Implementation: [<head> tags / Sitemap / HTTP headers]

Hreflang Structure:

For Each Page:
```html
<link rel="alternate" hreflang="en" href="https://example.com/en/page" />
<link rel="alternate" hreflang="uk" href="https://example.com/uk/page" />
<link rel="alternate" hreflang="x-default" href="https://example.com/en/page" />
```

Language Codes:
- English: en
- Ukrainian: uk
- [Other]: _______________

Default Language (x-default): _______________

Hreflang Rules:
- Bidirectional: [Yes - each page references all versions]
- Self-referential: [Yes - include self]
- Consistent across pages: [Yes]
- Return links: [Yes - reciprocal]

Common Errors to Avoid:
- [ ] Missing return links
- [ ] Incorrect language codes
- [ ] No x-default
- [ ] Broken URLs in hreflang
- [ ] Missing self-referential link

### Canonical Tags

Canonical Implementation:
Every page must have: [Yes]

Canonical URL Format:
- Protocol: HTTPS
- Domain: www or non-www (consistent)
- Trailing slash: [Yes/No] _______________
- Lowercase: [Yes]
- No parameters: [Preferred]

Self-Referencing Canonical:
```html
<link rel="canonical" href="https://example.com/page" />
```

Cross-Domain Canonical: [Yes/No]
If Yes: _______________

Pagination Canonical:
- Each page self-canonical: [Yes]
- OR all to page 1: [No - discouraged]

### Mobile Optimization Tags

Viewport Meta Tag:
```html
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=5">
```

Mobile-Specific Meta Tags:
```html
<meta name="mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="default">
<meta name="apple-mobile-web-app-title" content="_______________">
```

Touch Icons:
- apple-touch-icon: _______________ (180x180px)
- favicon-32x32: _______________
- favicon-16x16: _______________
- android-chrome icons: _______________

Mobile SEO Checklist:
- [ ] Responsive design
- [ ] Mobile-friendly test passed
- [ ] No intrusive interstitials
- [ ] Touch targets 44x44px minimum
- [ ] Readable font sizes (16px minimum)
- [ ] No horizontal scrolling
- [ ] Fast mobile page speed

---

## CONTENT SEO OPTIMIZATION

### Keyword Research Implementation

Primary Keywords: _______________
Secondary Keywords: _______________
Long-Tail Keywords: _______________

Keyword Mapping:

Homepage:
- Primary: _______________
- Secondary: _______________
- LSI: _______________

Features Page:
- Primary: _______________
- Secondary: _______________
- LSI: _______________

Pricing Page:
- Primary: _______________
- Secondary: _______________
- LSI: _______________

[Continue for all pages...]

Keyword Placement:
- [ ] Title tag
- [ ] Meta description
- [ ] H1 heading
- [ ] First paragraph
- [ ] Subheadings (H2, H3)
- [ ] Image alt text
- [ ] URL
- [ ] Internal anchor text

### Content Freshness Strategy

Update Schedule:
- Homepage: _______________
- Product pages: _______________
- Blog posts: _______________
- Legal pages: _______________

Update Triggers:
- [ ] Product changes
- [ ] Industry trends
- [ ] Competitor updates
- [ ] Seasonal content
- [ ] Outdated information

Last Modified Date:
Display on page: [Yes/No]
Format: _______________

### Duplicate Content Prevention

Duplicate Content Checks:
- [ ] Pagination handled correctly
- [ ] Parameter URLs canonicalized
- [ ] HTTP/HTTPS consistency
- [ ] WWW/non-WWW consistency
- [ ] Trailing slash consistency
- [ ] Multi-language versions use hreflang
- [ ] Copied content avoided

Syndicated Content:
If publishing elsewhere:
- Canonical to original: [Yes]
- Time delay: _______________ days
- Noindex on syndicated: [Consider]

---

## LOCAL SEO (If Applicable)

Google Business Profile:
- Created: [Yes/No]
- Verified: [Yes/No]
- Optimized: [Yes/No]

NAP Consistency:
Name: _______________
Address: _______________
Phone: _______________

Consistent across:
- [ ] Website footer
- [ ] Contact page
- [ ] Google Business Profile
- [ ] Social media profiles
- [ ] Local directories

Local Schema Markup:
- LocalBusiness schema: [Yes/No]
- Location pages: [Yes/No]

---

## SEO MONITORING & ANALYTICS

### Search Console Setup

Google Search Console:
- Property verified: [Yes/No]
- Sitemap submitted: [Yes/No]
- All versions added: [HTTP/HTTPS, www/non-www]
- Mobile usability: [Checked]
- Core Web Vitals: [Monitored]

Bing Webmaster Tools:
- Property verified: [Yes/No]
- Sitemap submitted: [Yes/No]

### Analytics Configuration

Google Analytics 4:
- Property ID: _______________
- Stream ID: _______________
- Enhanced measurement: [Enabled]

SEO-Specific Events to Track:
- [ ] Organic search sessions
- [ ] Landing pages
- [ ] Search queries (Search Console integration)
- [ ] Exit pages
- [ ] Bounce rate by page
- [ ] Time on page
- [ ] Scroll depth
- [ ] Click-through from search

### Rank Tracking

Keywords to Track:
1. _______________
2. _______________
3. _______________
[Continue for priority keywords...]

Tracking Tool: _______________ (e.g., Ahrefs, SEMrush, Google Search Console)
Tracking Frequency: _______________
Target Locations: _______________

### Backlink Monitoring

Backlink Profile:
- Monitor tool: _______________
- Check frequency: _______________
- Disavow toxic links: [Yes/No]

Link Building Strategy:
- [ ] Guest posting
- [ ] Resource pages
- [ ] Industry directories
- [ ] Press mentions
- [ ] Partner links
- [ ] Content marketing

---

## TECHNICAL SEO TESTING

### Pre-Launch SEO Checklist

- [ ] All meta tags configured
- [ ] Sitemap generated and submitted
- [ ] Robots.txt configured
- [ ] Canonical tags on all pages
- [ ] Hreflang tags for multi-language
- [ ] Schema markup implemented
- [ ] Internal linking structure complete
- [ ] 404 page customized
- [ ] Redirects configured
- [ ] Mobile-friendly
- [ ] Page speed optimized
- [ ] HTTPS enabled
- [ ] No broken links
- [ ] Images optimized with alt text
- [ ] Heading hierarchy correct
- [ ] Content original and valuable

### SEO Testing Tools

Crawl Tools:
- [ ] Screaming Frog SEO Spider
- [ ] Sitebulb
- [ ] DeepCrawl
- [ ] OnCrawl

Testing Tools:
- [ ] Google Search Console
- [ ] Google Mobile-Friendly Test
- [ ] Google Rich Results Test
- [ ] PageSpeed Insights
- [ ] GTmetrix
- [ ] Lighthouse
- [ ] Ahrefs Site Audit
- [ ] SEMrush Site Audit

### Common SEO Issues to Fix

- [ ] Broken links (404 errors)
- [ ] Redirect chains
- [ ] Missing meta descriptions
- [ ] Duplicate title tags
- [ ] Thin content pages
- [ ] Orphan pages (no internal links)
- [ ] Slow page speed
- [ ] Mobile usability issues
- [ ] Missing alt text
- [ ] Incorrect heading hierarchy
- [ ] Broken hreflang implementation
- [ ] Schema markup errors
- [ ] Mixed content (HTTP on HTTPS)
- [ ] Uncompressed images
- [ ] No canonical tags

---

## ONGOING SEO MAINTENANCE

### Monthly SEO Tasks

- [ ] Review Search Console for issues
- [ ] Check keyword rankings
- [ ] Analyze organic traffic trends
- [ ] Update content freshness
- [ ] Add new content
- [ ] Check for broken links
- [ ] Monitor backlink profile
- [ ] Review Core Web Vitals
- [ ] Analyze competitor SEO

### Quarterly SEO Tasks

- [ ] Comprehensive site audit
- [ ] Keyword research refresh
- [ ] Content gap analysis
- [ ] Technical SEO review
- [ ] Schema markup validation
- [ ] Mobile experience review
- [ ] Conversion rate optimization
- [ ] Link building review

### Annual SEO Tasks

- [ ] SEO strategy review
- [ ] Major content refresh
- [ ] Technical infrastructure review
- [ ] Competitor benchmarking
- [ ] Algorithm update assessment
- [ ] Tool/subscription review

---

## NOTES & SPECIAL REQUIREMENTS
_______________________________________________
_______________________________________________
_______________________________________________
```

---

## ✅ IMPLEMENTATION PROMPT FOR LOVABLE

After filling this template:

```
Implement Technical SEO Optimization based on the completed specification.

CONTEXT: I have defined a comprehensive SEO strategy covering on-page optimization, technical infrastructure, structured data, and monitoring for a multi-language SaaS website.

TASK:
1. Configure all meta tags (title, description, OG, Twitter Card) for each page
2. Implement proper heading hierarchy (H1-H6) across all pages
3. Set up canonical tags and hreflang tags for multi-language
4. Generate and configure XML sitemap with priorities
5. Implement structured data (Organization, WebSite, SoftwareApplication, FAQPage, etc.)
6. Optimize all images with proper alt text and file names
7. Create robots.txt with appropriate rules
8. Set up internal linking structure
9. Implement semantic HTML throughout
10. Configure Search Console and Analytics tracking

GUIDELINES:
- Every page must have unique title and meta description
- One H1 per page containing primary keyword
- All images must have descriptive alt text
- Canonical tags on every page
- Schema markup in JSON-LD format
- Clean, keyword-rich URLs
- Mobile-optimized meta tags
- Sitemap auto-generates on content changes

CONSTRAINTS:
- Title tags 50-60 characters
- Meta descriptions 150-160 characters
- Alt text descriptive but concise
- URLs lowercase with hyphens
- No duplicate content
- HTTPS canonical URLs
- Valid structured data (test with Google Rich Results)

[Paste your filled SEO optimization template here]

EXPECTED DELIVERABLES:
1. Meta tags configured for all pages
2. Proper heading hierarchy implemented
3. Sitemap.xml generated and accessible
4. Robots.txt configured
5. Canonical and hreflang tags working
6. Schema markup on relevant pages
7. Image optimization with alt text
8. Internal linking structure
9. Search Console configured
10. Analytics tracking SEO metrics
```

---

## 📝 USAGE INSTRUCTIONS

1. **Start with keyword research** - understand what users search for
2. **Map keywords to pages** - each page targets specific keywords
3. **Write for humans first** - natural content, then optimize
4. **Test everything** - use Google Search Console and testing tools
5. **Monitor regularly** - SEO is ongoing, not one-time
6. **Update content** - fresh content ranks better
7. **Build quality links** - focus on authoritative backlinks
8. **Track rankings** - measure progress on target keywords

---

## 💡 BEST PRACTICES

- Title tags should be compelling clickable headlines, not keyword stuffing
- Meta descriptions are ad copy - include CTAs and benefits
- Use primary keyword in H1, but make it natural and compelling
- Alt text should describe what's in the image for accessibility first
- Internal links use descriptive anchor text, not "click here"
- Schema markup must match actual page content - don't mislead
- Sitemap should update automatically when content changes
- Canonical tags prevent duplicate content issues
- Hreflang crucial for multi-language sites
- Mobile optimization is table stakes, not optional
- Page speed directly impacts rankings
- Content quality matters more than keyword density
- User experience signals (bounce rate, time on site) affect rankings

---

## ⚠️ CRITICAL REMINDERS

- SEO is long-term - results take 3-6 months minimum
- Title and meta description are first impression in search results
- Missing or duplicate meta tags hurt rankings
- Every page needs unique, optimized title and description
- Schema markup gives rich snippets in search results
- Broken links damage both UX and SEO
- Sitemap must be submitted to Search Console
- Mobile-first indexing means mobile version is what Google uses
- HTTPS is ranking factor - must use SSL
- Page speed is Core Web Vital - optimize aggressively
- Content freshness matters - update regularly
- Backlinks still crucial - quality over quantity
- Technical errors (404s, redirects chains) waste crawl budget
- Never copy content - Google penalizes duplicates
- Algorithm updates happen frequently - stay informed
- Local SEO matters even for SaaS (for founder/company searches)
- Hreflang errors cause wrong language versions to rank
- Search Console shows what Google sees - check regularly
