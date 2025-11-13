# Blog Listing Page Template - Technical Specification

**Page Type:** Content Listing Page
**URL Pattern:** `/blog`
**Priority:** Medium
**Approach:** Mobile First
**Last Updated:** November 12, 2025

---

## Page Overview

**Purpose:** Display all blog articles, enable filtering/search, drive content discovery and engagement.

**Key Goals:**
- Showcase latest content
- Enable easy article discovery
- Drive article reads
- Build thought leadership
- Support SEO through content hub

---

## Page Structure

### Block 01: Header Navigation
*(Same as Homepage - "Blog" highlighted if in main nav, or add to Resources dropdown)*

---

### Block 02: Page Hero
```
┌─────────────────────────────────────┐
│                                     │
│  [H1: Delphi Blog]                  │
│                                     │
│  [Subtitle: Insights on AI...]      │
│                                     │
│  ┌───────────────────────────────┐  │
│  │ 🔍 Search articles...         │  │
│  └───────────────────────────────┘  │
│                                     │
└─────────────────────────────────────┘
```

**H1:** "Delphi Blog" or "Insights on AI, Digital Minds & Expert Growth"
- Mobile: 32px / 38px, Desktop: 48px / 56px
- Weight: 700, Center aligned

**Subtitle:** "Expert insights, case studies, and tips for scaling your impact with AI."
- Font size: 16px / 24px (mobile), 18px / 28px (desktop)
- Color: Secondary text

**Search Bar:**
- Placeholder: "Search articles..."
- Width: Full mobile, 600px max desktop
- Height: 52px
- Border-radius: 12px
- Icon: Magnifying glass (left)

**Spacing:** 40px 20px (mobile), 60px 40px (desktop)

---

### Block 03: Category Filter Tabs
```
┌─────────────────────────────────────┐
│ [All] [Leadership] [Product] [Case Studies] → │
└─────────────────────────────────────┘
```

**Categories:**
- All
- Leadership
- Product & Growth
- Case Studies
- AI & Technology
- Marketing
- How-To Guides

**Pills:** Same styling as Explore page filters
- Horizontal scroll mobile
- Centered desktop
- Active state highlighted

---

### Block 04: Featured Article (Hero Post)
```
┌─────────────────────────────────────┐
│                                     │
│  ┌─────────────────────────────┐   │
│  │                             │   │
│  │    [Featured Image]         │   │
│  │                             │   │
│  └─────────────────────────────┘   │
│                                     │
│  [Category Badge]                   │
│                                     │
│  [H2 Article Title]                 │
│                                     │
│  [Excerpt text - 2-3 lines]         │
│                                     │
│  [Author] · [Date] · [Read time]    │
│                                     │
│  [Read Article →]                   │
│                                     │
└─────────────────────────────────────┘
```

**Mobile:** Stack image, then content
**Desktop:** Two-column (image left 50%, content right 50%)

**Featured Image:**
- Size Mobile: Full width, 16:9 aspect
- Size Desktop: 600px × 400px
- Border-radius: 12px
- Object-fit: cover

**Category Badge:**
- Background: Primary color 10% opacity
- Color: Primary color
- Padding: 4px 12px
- Border-radius: 12px
- Font size: 12px
- Font weight: 600
- Text: uppercase

**Article Title (H2):**
- Font size Mobile: 24px / 30px
- Font size Desktop: 32px / 40px
- Font weight: 700
- Margin: 12px 0
- Color: Primary text
- Hover: Primary color (if clickable)

**Excerpt:**
- Font size: 16px / 24px
- Color: Secondary text
- Lines: 2-3
- Margin: 12px 0

**Meta Info:**
- Font size: 14px
- Color: Tertiary text (#9CA3AF)
- Display: Flex, gap 8px
- Items separated by "·"

**Author:**
- Optional avatar (24px × 24px)
- Name text

**Read Time:** "5 min read"

**CTA Link:**
- Text: "Read Article →"
- Font size: 16px
- Font weight: 600
- Color: Primary
- Hover: Underline

**Container:**
- Border: 1px solid #E5E7EB
- Border-radius: 16px
- Padding: 24px (mobile), 32px (desktop)
- Margin: 24px 20px (mobile), 40px auto (desktop)
- Max-width: 1100px
- Background: White
- Hover: Subtle shadow (desktop)

---

### Block 05: Articles Grid
```
┌─────────────────────────────────────┐
│  ┌──────────────┐  ┌──────────────┐ │
│  │   Article    │  │   Article    │ │
│  │     Card     │  │     Card     │ │
│  └──────────────┘  └──────────────┘ │
│  ┌──────────────┐  ┌──────────────┐ │
│  │   Article    │  │   Article    │ │
│  └──────────────┘  └──────────────┘ │
└─────────────────────────────────────┘
```

**Grid:**
- Mobile: 1 column
- Tablet: 2 columns
- Desktop: 3 columns
- Gap: 24px

---

### Article Card Structure
```
┌──────────────────────┐
│                      │
│  [Featured Image]    │
│                      │
│  [Category Badge]    │
│                      │
│  [Title]             │
│                      │
│  [Excerpt]           │
│                      │
│  [Meta: Author, Date]│
│                      │
└──────────────────────┘
```

**Image:**
- Full width card
- Aspect ratio: 16:9
- Border-radius: 12px 12px 0 0
- Object-fit: cover
- Alt text: Article title

**Category Badge:**
- Position: Over image or below
- Same styling as featured article

**Title (H3):**
- Font size: 18px / 24px
- Font weight: 600
- Color: Primary text
- Lines: 2 max (clamp)
- Margin: 12px 0

**Excerpt:**
- Font size: 14px / 20px
- Color: Secondary text
- Lines: 2-3 max
- Margin: 8px 0

**Meta:**
- Font size: 13px
- Color: Tertiary text
- Display: Flex, wrap
- Gap: 8px
- Items: Author · Date · Read time

**Card Styling:**
- Background: White
- Border: 1px solid #E5E7EB
- Border-radius: 12px
- Overflow: hidden
- Hover (Desktop):
  - Transform: translateY(-4px)
  - Shadow: 0 8px 16px rgba(0,0,0,0.12)
  - Transition: 0.3s ease

**Entire card clickable:** Wrap in <a> tag

---

### Block 06: Load More / Pagination
```
┌─────────────────────────────────────┐
│     [Load More Articles]            │
│  or                                 │
│     [← 1 2 3 4 5 →]                 │
└─────────────────────────────────────┘
```

**Option A: Load More Button**
- Text: "Load More Articles"
- Style: Secondary button
- Load 9 more articles per click

**Option B: Pagination**
- Show 5 page numbers
- Previous/Next arrows
- Current page highlighted
- URL: `/blog?page=2`

**Container:**
- Padding: 40px 20px
- Text align: Center

---

### Block 07: Newsletter Signup CTA
```
┌─────────────────────────────────────┐
│                                     │
│  📧 [Icon]                          │
│                                     │
│  [H3: Stay Updated]                 │
│                                     │
│  [Subtitle text]                    │
│                                     │
│  ┌────────────────┐  ┌──────────┐  │
│  │ Enter email... │  │ Subscribe│  │
│  └────────────────┘  └──────────┘  │
│                                     │
└─────────────────────────────────────┘
```

**H3:** "Stay Updated"
**Subtitle:** "Get the latest insights delivered to your inbox weekly."

**Email Input:**
- Placeholder: "Enter your email"
- Width Mobile: Full, Desktop: 320px
- Height: 48px
- Border: 1px solid #D1D5DB
- Border-radius: 8px

**Submit Button:**
- Text: "Subscribe"
- Height: 48px
- Background: Primary color
- Color: White
- Padding: 0 24px
- Mobile: Full width (below input)
- Desktop: Inline (right of input)

**Container:**
- Background: #F9FAFB
- Border: 1px solid #E5E7EB
- Border-radius: 16px
- Padding: 40px 24px
- Margin: 60px 20px
- Max-width: 700px
- Text align: Center

---

### Block 08: Footer
*(Same as Homepage)*

---

## Interactive Elements

### 1. Search Functionality
- Real-time search (debounce 300ms)
- Search: Title, excerpt, author
- Highlight matches
- No results message

### 2. Category Filters
- Click to filter
- Update URL: `/blog?category=leadership`
- Fade out/in animation
- Preserve search query

### 3. Card Hover (Desktop)
- Lift animation
- Shadow increase
- Image subtle zoom (scale 1.05)

### 4. Infinite Scroll (Optional)
- Auto-load at 80% scroll
- Show loading skeleton
- Update URL

---

## Performance

- Lazy load images (below fold)
- Pagination/Infinite scroll to limit initial load
- WebP images with fallback
- Preload featured article image

---

## SEO

**Title:** "Blog | Delphi - AI, Digital Minds & Expert Growth Insights"
**Description:** "Expert insights, case studies, and practical tips for scaling your impact with AI digital clones and thought leadership."
**Canonical:** `https://www.delphi.ai/blog`

**Structured Data:**
```json
{
  "@type": "Blog",
  "blogPost": [...]
}
```

**Each Card:**
```json
{
  "@type": "BlogPosting",
  "headline": "Article Title",
  "image": "...",
  "datePublished": "2025-11-07",
  "author": {...}
}
```

---

**End of Blog Listing Page Template**
