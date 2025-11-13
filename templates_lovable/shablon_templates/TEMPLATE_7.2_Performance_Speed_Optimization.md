# TEMPLATE 7.2: PERFORMANCE & SPEED OPTIMIZATION

## 📋 PURPOSE
This template provides a comprehensive performance optimization checklist to ensure your website loads fast, meets Core Web Vitals standards, and provides excellent user experience across all devices and network conditions.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Implement Performance & Speed Optimization based on the following specification:

## PERFORMANCE TARGETS

### Core Web Vitals Goals

Largest Contentful Paint (LCP):
- Target: < 2.5 seconds
- Current: _______________ seconds
- Priority: [Critical]

First Input Delay (FID) / Interaction to Next Paint (INP):
- Target: < 100ms (FID) / < 200ms (INP)
- Current: _______________ ms
- Priority: [Critical]

Cumulative Layout Shift (CLS):
- Target: < 0.1
- Current: _______________
- Priority: [Critical]

### Additional Performance Metrics

First Contentful Paint (FCP):
- Target: < 1.8 seconds
- Current: _______________ seconds

Time to Interactive (TTI):
- Target: < 3.8 seconds
- Current: _______________ seconds

Total Blocking Time (TBT):
- Target: < 200ms
- Current: _______________ ms

Speed Index:
- Target: < 3.4 seconds
- Current: _______________ seconds

### Page Weight Targets

Total Page Size:
- Target: < 2 MB
- Current: _______________ MB

JavaScript Bundle:
- Target: < 300 KB (compressed)
- Current: _______________ KB

CSS Bundle:
- Target: < 50 KB (compressed)
- Current: _______________ KB

Images:
- Target: < 1 MB total above fold
- Current: _______________ MB

Web Fonts:
- Target: < 100 KB total
- Current: _______________ KB

---

## RESOURCE OPTIMIZATION

### Image Optimization Strategy

#### Image Format Selection

Format Priority:
1. WebP (modern browsers)
2. AVIF (next-gen, optional)
3. JPEG/PNG (fallback)
4. SVG (icons, logos)

Format Guidelines:
- Photos: WebP (90% quality) with JPEG fallback
- Illustrations: WebP or SVG
- Icons: Inline SVG (< 2KB) or SVG sprite
- Logos: SVG
- Screenshots: WebP with PNG fallback

#### Image Compression

Compression Targets:

Hero Images:
- Original size: _______________ MB
- Compressed size: < 200 KB
- Quality: 80-85%

Feature Images:
- Compressed size: < 100 KB
- Quality: 75-80%

Thumbnails:
- Compressed size: < 30 KB
- Quality: 70-75%

Background Images:
- Compressed size: < 150 KB
- Quality: 75-80%

Icons:
- Size: < 5 KB each
- Format: Inline SVG preferred

Compression Tools:
- [ ] ImageOptim (Mac)
- [ ] Squoosh (Web)
- [ ] TinyPNG (Lossy)
- [ ] Sharp (Node.js)
- [ ] Cloudinary/Imgix (CDN)
- [ ] Other: _______________

#### Responsive Images

Srcset Configuration:

Example Implementation:
```html
<img
  src="image-800w.webp"
  srcset="
    image-400w.webp 400w,
    image-800w.webp 800w,
    image-1200w.webp 1200w,
    image-1600w.webp 1600w
  "
  sizes="
    (max-width: 640px) 100vw,
    (max-width: 1024px) 50vw,
    33vw
  "
  alt="_______________"
  loading="lazy"
  decoding="async"
/>
```

Breakpoints for Images:
- Mobile: 400px, 640px
- Tablet: 768px, 1024px
- Desktop: 1280px, 1600px
- Retina: 2x versions (optional)

#### Image Lazy Loading

Lazy Loading Strategy:
- Above fold images: loading="eager"
- Below fold images: loading="lazy"
- Intersection Observer: [Yes, for custom implementation]
- Placeholder: [BlurHash / Dominant color / Skeleton]

Critical Images (No Lazy Load):
- [ ] Logo
- [ ] Hero image
- [ ] First visible image
- [ ] Critical icons

Lazy Load Everything Else:
- [ ] Feature screenshots
- [ ] Testimonial photos
- [ ] Team photos
- [ ] Background images (via CSS)
- [ ] Icon libraries (load on demand)

#### Image CDN Configuration

CDN Provider: _______________ (Cloudinary / Imgix / Cloudflare / AWS CloudFront)

CDN Features:
- [ ] Auto-format detection (serve WebP/AVIF to supporting browsers)
- [ ] Auto-quality optimization
- [ ] Responsive image generation
- [ ] Image transformations (resize, crop, optimize)
- [ ] Caching headers
- [ ] Global edge locations

CDN URL Pattern: _______________

### Font Optimization

#### Font Loading Strategy

Font Loading Method: [font-display: swap / optional / fallback / block]
Recommended: swap

Font Loading Sequence:
1. System font displays immediately (FOUT prevention)
2. Custom font loads asynchronously
3. Custom font swaps in when ready

#### Font File Optimization

Font Format Priority:
1. WOFF2 (modern browsers) - 30% smaller than WOFF
2. WOFF (fallback)
3. TTF/OTF (no longer needed for web)

Font Subsetting:
- Include only used characters: [Yes]
- Latin subset: [Yes]
- Latin-extended: [If needed]
- Cyrillic: [If needed] _______________
- Remove unused glyphs: [Yes]

Font Weights to Include:
- [ ] 300 (Light)
- [ ] 400 (Regular) - ESSENTIAL
- [ ] 500 (Medium)
- [ ] 600 (Semi-bold)
- [ ] 700 (Bold)
- [ ] Other: _______________

Minimize font weights: Load only what's actually used

#### Font Preloading

Preload Critical Fonts:
```html
<link
  rel="preload"
  href="/fonts/primary-font-400.woff2"
  as="font"
  type="font/woff2"
  crossorigin
/>
```

Fonts to Preload:
- Primary font (regular weight): [Yes]
- Primary font (bold): [Yes/No]
- Other critical fonts: _______________

Maximum fonts to preload: 2-3 (avoid overloading)

#### System Font Fallback

Font Stack:
```css
font-family: 'CustomFont', -apple-system, BlinkMacSystemFont, 'Segoe UI', 
  'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', 'Helvetica Neue', sans-serif;
```

Fallback Font Metrics:
Match size/spacing of custom font to minimize layout shift

CSS font-display:
```css
@font-face {
  font-family: 'CustomFont';
  src: url('/fonts/custom-font.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}
```

### JavaScript Optimization

#### Bundle Size Reduction

Code Splitting Strategy:
- [ ] Route-based splitting (per page)
- [ ] Component-based splitting (lazy load components)
- [ ] Vendor splitting (separate vendor bundle)
- [ ] Common chunks extraction

Bundle Analysis:
Tool: webpack-bundle-analyzer / rollup-plugin-visualizer
Target: Identify and eliminate large dependencies

Tree Shaking:
- Dead code elimination: [Enabled]
- Side effects marked: [Yes, in package.json]
- ES modules: [Used for tree-shaking]

Dependency Optimization:
- Replace large libraries with lightweight alternatives
- Example: Moment.js → date-fns or Day.js
- Example: Lodash → Lodash-es (tree-shakeable)
- Remove unused dependencies: [Yes]

#### JavaScript Loading Strategy

Critical JavaScript:
Inline in <head>: _______________ (minimal, < 14KB)
Purpose: Critical functionality only

Async Loading:
```html
<script src="script.js" async></script>
```
Use for: Independent scripts (analytics, ads)

Defer Loading:
```html
<script src="script.js" defer></script>
```
Use for: All non-critical scripts
Execution: After HTML parsing

Module/Nomodule Pattern:
```html
<script type="module" src="modern.js"></script>
<script nomodule src="legacy.js"></script>
```
Use: Serve modern ES6+ to modern browsers, fallback to transpiled

#### JavaScript Execution Optimization

Long Tasks Reduction:
- Break up long tasks (> 50ms)
- Use requestIdleCallback for non-critical work
- Debounce/throttle expensive operations
- Code splitting to reduce parse time

Main Thread Work:
- Target: < 2 seconds
- Offload to Web Workers: [Yes/No] _______________
- Use for: Heavy computations, data processing

Third-Party Scripts:
- Load priority: [Low]
- Load timing: [After page load / On user interaction]
- Self-host when possible: [Yes]

Third-Party Script List:
1. Google Analytics: [Defer / Async]
2. _______________: _______________
3. _______________: _______________

### CSS Optimization

#### CSS Loading Strategy

Critical CSS:
- Extract above-fold CSS: [Yes]
- Inline in <head>: [Yes, < 14KB]
- Tool: Critical / Critters
- Per-page critical CSS: [Yes/No]

Non-Critical CSS:
- Load asynchronously: [Yes]
- Use media="print" trick: [Yes]
```html
<link rel="stylesheet" href="styles.css" media="print" onload="this.media='all'">
```

CSS File Organization:
- Critical.css (inlined): _______________ KB
- Main.css (deferred): _______________ KB
- Page-specific.css: _______________ KB each

#### CSS Size Reduction

Minification: [Yes]
Tool: cssnano / clean-css

Unused CSS Removal:
Tool: PurgeCSS / UnCSS
Target: Remove unused Tailwind classes, component styles

CSS Optimization:
- [ ] Remove duplicate rules
- [ ] Combine similar selectors
- [ ] Shorten property values
- [ ] Remove comments
- [ ] Minimize specificity

CSS Bundle Size:
- Before optimization: _______________ KB
- After optimization: _______________ KB
- Target: < 50 KB

#### CSS Performance Best Practices

Avoid:
- [ ] @import (blocks rendering)
- [ ] Large number of CSS files
- [ ] Inline styles everywhere (except critical)
- [ ] Overly specific selectors
- [ ] Deep nesting (> 3 levels)

Optimize:
- [ ] Use CSS custom properties (variables)
- [ ] Minimize reflows/repaints
- [ ] Use transform/opacity for animations
- [ ] Avoid expensive properties (box-shadow, filter)

---

## LOADING & RENDERING OPTIMIZATION

### Resource Prioritization

#### Resource Hints

Preconnect:
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://cdn.example.com">
```
Use for: Critical third-party origins

DNS-Prefetch:
```html
<link rel="dns-prefetch" href="https://analytics.example.com">
```
Use for: Lower-priority third-party domains

Preload:
```html
<link rel="preload" href="/hero-image.webp" as="image">
<link rel="preload" href="/critical-font.woff2" as="font" type="font/woff2" crossorigin>
<link rel="preload" href="/critical.css" as="style">
```
Use for: Critical resources that will be used soon

Resources to Preload:
1. Hero image: [Yes]
2. Critical font: [Yes]
3. Critical CSS: [No, inline instead]
4. Above-fold images: [Yes/No]

Prefetch:
```html
<link rel="prefetch" href="/next-page.html">
```
Use for: Resources for next navigation

Prerender (use sparingly):
```html
<link rel="prerender" href="/next-page.html">
```

#### Critical Rendering Path Optimization

Render-Blocking Resources:
Goal: Minimize or eliminate

CSS:
- Inline critical CSS: [Yes]
- Defer non-critical CSS: [Yes]
- Remove unused CSS: [Yes]

JavaScript:
- Defer all non-critical JS: [Yes]
- Async for independent scripts: [Yes]
- No render-blocking JS: [Goal]

Fonts:
- Use font-display: swap: [Yes]
- Preload critical fonts: [Yes]
- Limit font weights: [Yes]

### Layout Shift Prevention

#### CLS Optimization Strategies

Image Dimensions:
Always specify width and height:
```html
<img src="image.jpg" width="800" height="600" alt="..." />
```

CSS aspect-ratio:
```css
.image-container {
  aspect-ratio: 16 / 9;
}
```

Video Embeds:
Reserve space with aspect-ratio:
```css
.video-embed {
  aspect-ratio: 16 / 9;
}
```

Ads/Embeds:
- Reserve fixed space: [Yes]
- Min-height placeholder: [Yes]
- Avoid inserting content above existing: [Yes]

Font Loading:
- Use font-display: swap: [Yes]
- Match fallback font metrics: [Yes]
- Prevent FOIT (Flash of Invisible Text): [Yes]

Dynamic Content:
- Reserve space for loading content: [Yes]
- Use skeleton screens: [Yes]
- Avoid layout shift from injected content: [Yes]

#### Common CLS Issues to Fix

- [ ] Images without dimensions
- [ ] Web fonts causing text shift
- [ ] Ads/embeds without space reservation
- [ ] Dynamically injected content
- [ ] Animations that affect layout
- [ ] Cookie banners pushing content
- [ ] Late-loading CSS

Target CLS: < 0.1
Current CLS: _______________

### Interaction Optimization

#### First Input Delay / Interaction to Next Paint

Reduce JavaScript Execution:
- Code split: [Yes]
- Defer non-critical JS: [Yes]
- Minimize main thread work: [Yes]

Optimize Event Handlers:
- Debounce scroll/resize: [Yes]
- Use passive event listeners: [Yes]
- Minimize work in handlers: [Yes]

Break Up Long Tasks:
- Tasks > 50ms: [Split or defer]
- Use setTimeout/requestIdleCallback: [Yes]
- Yield to main thread: [Yes]

Target FID: < 100ms
Target INP: < 200ms
Current: _______________ ms

#### Loading State Optimization

Skeleton Screens:
Use for: [Content that loads dynamically]
Style: [Shimmer / Static gray / Branded]

Lazy Loading Strategy:
- Images: [Yes, below fold]
- Components: [Yes, route-based]
- Third-party widgets: [Yes, on interaction]

Progressive Enhancement:
- Site works without JS: [Basic functionality]
- Enhanced with JS: [Full features]

---

## CACHING STRATEGY

### Browser Caching

Cache-Control Headers:

Static Assets (immutable):
- Images: max-age=31536000, immutable
- CSS/JS (with hash): max-age=31536000, immutable
- Fonts: max-age=31536000, immutable

HTML:
- Pages: max-age=0, must-revalidate OR no-cache
- Dynamic: no-cache, no-store

Cache Configuration:
```
# Static assets
/assets/*: Cache-Control: public, max-age=31536000, immutable

# HTML
/*.html: Cache-Control: public, max-age=0, must-revalidate

# Fonts
/fonts/*: Cache-Control: public, max-age=31536000, immutable

# Images
/images/*: Cache-Control: public, max-age=31536000
```

### Service Worker / PWA Caching

Service Worker: [Yes/No]

If Yes:
Caching Strategy:
- Cache First: Static assets (CSS, JS, images)
- Network First: HTML pages
- Stale While Revalidate: API responses

Offline Fallback:
- Offline page: [Yes/No]
- Cached pages available: [Yes/No]

PWA Configuration:
- manifest.json: [Yes/No]
- Installable: [Yes/No]
- Offline capability: [Basic/Full/None]

### CDN Caching

CDN Provider: _______________
(Cloudflare / CloudFront / Fastly / Other)

CDN Configuration:
- Edge caching: [Enabled]
- Cache duration: _______________
- Purge on deploy: [Yes]
- Geographic distribution: _______________

Static Assets via CDN:
- [ ] Images
- [ ] CSS/JS
- [ ] Fonts
- [ ] Videos
- [ ] PDFs

---

## COMPRESSION & MINIFICATION

### Text Compression

Gzip Compression:
- Enabled: [Yes]
- Level: 6-9
- Files compressed: HTML, CSS, JS, JSON, XML, SVG

Brotli Compression:
- Enabled: [Yes]
- Level: 11 (max)
- Fallback to Gzip: [Yes]
- Reduction vs Gzip: ~20% smaller

Compression Configuration:
Server: _______________
Configuration:
```
# Enable Brotli + Gzip
Accept-Encoding: br, gzip, deflate
```

Assets to Compress:
- [ ] HTML
- [ ] CSS
- [ ] JavaScript
- [ ] JSON
- [ ] XML
- [ ] SVG
- [ ] Web fonts (if not already compressed)

### File Minification

HTML Minification:
- Tool: html-minifier
- Options: Remove comments, collapse whitespace
- Preserve: SEO-critical content

CSS Minification:
- Tool: cssnano
- Options: Optimize calc(), merge rules, shorten values

JavaScript Minification:
- Tool: Terser / esbuild
- Options: Mangle, compress, remove console.logs

SVG Optimization:
- Tool: SVGO
- Options: Remove metadata, simplify paths, round values

Build Process:
- Minify in production: [Yes]
- Source maps: [Yes, for debugging]
- Skip minification in dev: [Yes]

---

## THIRD-PARTY OPTIMIZATION

### Third-Party Scripts Audit

Third-Party Scripts:

Script 1:
- Name: Google Analytics
- Purpose: Analytics
- Loading: [Async/Defer] Defer
- Load timing: [Page load / User interaction]
- Impact: _______________ ms
- Necessary: [Yes/No]
- Alternative: [None / Lighter option]

Script 2:
- Name: _______________
- Purpose: _______________
- Loading: _______________
- Impact: _______________ ms
- Necessary: [Yes/No]
- Alternative: _______________

Script 3:
[Continue...]

### Third-Party Optimization Strategies

Defer Loading:
- Load after page load: [Yes]
- Load on user interaction: [Yes, for non-critical]
- Use Intersection Observer: [Yes, for widgets]

Facades:
Replace heavy embeds with lightweight facades:
- YouTube: Use lite-youtube-embed
- Maps: Use static image → load interactive on click
- Social feeds: Use placeholder → load on view

Self-Hosting:
Self-host when possible:
- [ ] Google Fonts
- [ ] Analytics script
- [ ] Icon fonts
- [ ] Other: _______________

Tag Manager Optimization:
If using GTM:
- Load only necessary tags: [Yes]
- Use custom HTML for lighter scripts: [Yes]
- Avoid tag bloat: [Yes]

### Monitoring Third-Party Impact

Measure Impact:
Tool: WebPageTest, Lighthouse

Third-Party Blocking Time: _______________ ms
Target: < 200ms total

Remove or Replace:
Scripts adding > 100ms: _______________
Plan: _______________

---

## PERFORMANCE MONITORING

### Performance Budgets

Set Budgets:

Total Page Weight: < 2 MB
JavaScript Bundle: < 300 KB
CSS: < 50 KB
Images: < 1 MB (above fold)

LCP: < 2.5s
FID/INP: < 100ms / < 200ms
CLS: < 0.1

Tool: Lighthouse CI / SpeedCurve / WebPageTest

Budget Enforcement:
- CI/CD integration: [Yes/No]
- Fail build if exceeded: [Yes/No]
- Alert on regression: [Yes/No]

### Real User Monitoring (RUM)

RUM Tool: _______________ 
(Google Analytics / Cloudflare / SpeedCurve / Other)

Metrics to Track:
- [ ] Core Web Vitals (LCP, FID/INP, CLS)
- [ ] Page load time
- [ ] Time to interactive
- [ ] First contentful paint
- [ ] By device type (mobile/desktop)
- [ ] By network (3G/4G/WiFi)
- [ ] By geography

Percentiles to Monitor:
- 50th percentile (median)
- 75th percentile
- 95th percentile (worst experiences)

### Synthetic Monitoring

Tools:
- [ ] Lighthouse (automated)
- [ ] WebPageTest
- [ ] GTmetrix
- [ ] PageSpeed Insights

Testing Schedule:
- Frequency: [Per deploy / Daily / Weekly]
- Pages to test: _______________
- Devices: [Mobile / Desktop / Both]
- Network: [3G / 4G / Cable]

Alerts:
- LCP > 3s: [Alert]
- FID > 200ms: [Alert]
- CLS > 0.15: [Alert]

---

## NETWORK OPTIMIZATION

### HTTP/2 & HTTP/3

HTTP Version: [HTTP/2 / HTTP/3]

HTTP/2 Features:
- [ ] Multiplexing (multiple requests over single connection)
- [ ] Server push (optional)
- [ ] Header compression

HTTP/3 (QUIC):
- [ ] Enabled (if supported by host)
- [ ] Benefits: Faster connection, better on poor networks

### Connection Optimization

Keep-Alive:
- Enabled: [Yes]
- Timeout: _______________ seconds

Connection Pooling:
- Limit connections per domain: _______________
- Use CDN for parallel downloads: [Yes]

Domain Sharding:
- Use: [No - unnecessary with HTTP/2]

### Request Reduction

Asset Consolidation:
- CSS files: [Combine into 1-2 files]
- JS files: [Bundle appropriately]
- Avoid excessive HTTP requests: [Yes]

Target Total Requests:
- Initial page load: < 50 requests
- Current: _______________ requests

Inline Small Assets:
- Small SVG icons: [Inline]
- Critical CSS: [Inline]
- Small scripts: [Consider inlining if < 2KB]

---

## MOBILE PERFORMANCE

### Mobile-Specific Optimizations

Network Conditions:
Test on:
- [ ] 3G (Slow 3G)
- [ ] 4G
- [ ] WiFi

Target Load Time (3G): < 5 seconds

Mobile Optimizations:
- [ ] Smaller images for mobile
- [ ] Reduced JavaScript bundle
- [ ] Simplified animations
- [ ] Touch-optimized interactions
- [ ] Reduced third-party scripts

Adaptive Loading:
Based on navigator.connection:
- Serve lower quality images on slow connections
- Defer non-critical features on slow connections
- Show loading states appropriately

### Mobile Testing

Test Devices:
- [ ] iPhone (Safari)
- [ ] Android (Chrome)
- [ ] Low-end Android device
- [ ] Tablet

Mobile Performance Checklist:
- [ ] Tap targets 44x44px minimum
- [ ] No horizontal scrolling
- [ ] Fast scroll performance
- [ ] Smooth animations (60fps)
- [ ] Optimized for touchscreen
- [ ] Works on slow networks

---

## PERFORMANCE TESTING

### Pre-Launch Performance Checklist

- [ ] Lighthouse score > 90 (all categories)
- [ ] LCP < 2.5s
- [ ] FID/INP < 100ms / 200ms
- [ ] CLS < 0.1
- [ ] Page size < 2MB
- [ ] All images optimized
- [ ] WebP with fallback
- [ ] Lazy loading implemented
- [ ] Critical CSS inlined
- [ ] JS deferred/async
- [ ] Fonts optimized
- [ ] Compression enabled (Brotli + Gzip)
- [ ] Caching configured
- [ ] Third-party scripts optimized
- [ ] Mobile performance tested
- [ ] Slow network tested (3G)

### Performance Testing Tools

Automated Testing:
- [ ] Lighthouse CI (in CI/CD)
- [ ] WebPageTest (periodic)
- [ ] GTmetrix (monitoring)
- [ ] PageSpeed Insights (quick checks)

Manual Testing:
- [ ] Chrome DevTools (throttling)
- [ ] Firefox Developer Tools
- [ ] Safari Web Inspector
- [ ] Real device testing

### Performance Regression Prevention

CI/CD Integration:
- Run Lighthouse on each PR: [Yes/No]
- Fail build if budget exceeded: [Yes/No]
- Comment performance scores on PR: [Yes/No]

Performance Monitoring:
- Dashboard: _______________
- Alert on regression: [Yes/No]
- Weekly/monthly reports: [Yes/No]

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
Implement Performance & Speed Optimization based on the completed specification.

CONTEXT: I have defined comprehensive performance optimization strategies targeting Core Web Vitals, fast load times, and excellent user experience across all devices and network conditions.

TASK:
1. Optimize all images (WebP format, compression, lazy loading, responsive srcset)
2. Implement font optimization (WOFF2, preload, font-display: swap)
3. Code split JavaScript and defer/async loading
4. Extract and inline critical CSS, defer non-critical
5. Configure resource hints (preconnect, preload)
6. Implement lazy loading for below-fold content
7. Set proper caching headers for all assets
8. Enable compression (Brotli + Gzip)
9. Optimize third-party scripts (defer, facades)
10. Set up performance monitoring (Lighthouse CI, RUM)

GUIDELINES:
- Target LCP < 2.5s, FID < 100ms, CLS < 0.1
- Total page size < 2MB
- JavaScript bundle < 300KB compressed
- All images in WebP format with fallback
- Critical CSS inlined (< 14KB)
- Fonts preloaded and optimized
- Mobile performance tested on 3G
- Performance budgets enforced

CONSTRAINTS:
- Hero image must load < 1s
- No render-blocking resources
- Layout shift prevented (specify dimensions)
- Third-party scripts defer until after load
- CDN for static assets
- Service worker for offline (optional)

[Paste your filled performance optimization template here]

EXPECTED DELIVERABLES:
1. All images optimized with WebP + fallback
2. Responsive images with srcset
3. Lazy loading implemented
4. Fonts optimized and preloaded
5. Critical CSS inlined
6. JS deferred/async appropriately
7. Resource hints configured
8. Compression enabled
9. Caching headers set
10. Performance monitoring active
```

---

## 📝 USAGE INSTRUCTIONS

1. **Measure first** - baseline metrics before optimization
2. **Prioritize impact** - focus on issues affecting Core Web Vitals
3. **Test on real devices** - especially low-end mobile
4. **Test slow networks** - throttle to 3G in DevTools
5. **Monitor continuously** - performance can regress
6. **Budget enforcement** - prevent regressions in CI/CD
7. **User-centric metrics** - optimize for real user experience
8. **Incremental improvement** - tackle one issue at a time

---

## 💡 BEST PRACTICES

- Images are typically the biggest opportunity for optimization
- WebP provides 25-35% better compression than JPEG
- Lazy loading saves bandwidth for images users never see
- Critical CSS should be < 14KB to fit in first network packet
- Font preloading prevents flash of unstyled text
- Code splitting reduces initial JavaScript bundle size
- Third-party scripts are often the biggest performance killers
- Compression (Brotli/Gzip) is free performance win
- Caching means repeat visitors load instantly
- Mobile performance matters more than desktop (mobile-first indexing)
- Core Web Vitals directly impact SEO rankings
- Layout shift ruins user experience - prevent with dimensions
- Defer everything that's not critical to first paint
- Test on real devices, not just DevTools emulation

---

## ⚠️ CRITICAL REMINDERS

- Core Web Vitals are Google ranking factors - must optimize
- LCP is about perceived speed - optimize hero image loading
- CLS ruins UX - always specify image/video dimensions
- FID/INP measures responsiveness - minimize JavaScript execution
- Images without dimensions cause layout shift
- Web fonts cause invisible text flash - use font-display: swap
- Third-party scripts can destroy performance - audit ruthlessly
- Render-blocking resources delay first paint - eliminate them
- Mobile performance is critical - test on real devices and slow networks
- Lighthouse score is helpful but test real user metrics (RUM)
- Performance is not one-time - monitor continuously
- Regressions happen - enforce budgets in CI/CD
- Page weight matters - every KB counts on mobile
- Lazy loading is essential but don't lazy load above-fold content
- Compression should be enabled on all text assets
- HTTP/2 changes optimization strategies (no more domain sharding)
- Preload critical resources, prefetch next-page resources
- Slow networks are common - test on 3G minimum
- Performance affects conversion rates directly
- Core Web Vitals monitoring available in Google Search Console
