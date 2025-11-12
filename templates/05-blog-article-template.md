# Blog Article Page Template - Technical Specification

**Page Type:** Content Article Page
**URL Pattern:** `/blog/{slug}`
**Priority:** Medium
**Approach:** Mobile First
**Last Updated:** November 12, 2025

---

## Page Overview

**Purpose:** Display individual blog article with optimal readability, encourage engagement, and drive conversions.

---

## Page Structure

### Block 01: Header Navigation
*(Same as Homepage)*

---

### Block 02: Article Header
```
┌─────────────────────────────────────┐
│                                     │
│  [Category Badge]                   │
│                                     │
│  [H1: Article Title]                │
│                                     │
│  [Author Avatar] [Author Name]      │
│  [Date] · [Read Time]               │
│                                     │
│  [Share Icons: Twitter, LinkedIn, Copy] │
│                                     │
└─────────────────────────────────────┘
```

**H1 Title:**
- Font size Mobile: 28px / 34px
- Font size Desktop: 40px / 48px
- Font weight: 700
- Max-width: 800px
- Margin: 16px 0 24px

**Author Info:**
- Display: Flex, align center
- Avatar: 48px × 48px, border-radius 50%
- Name: 15px, weight 600
- Date: 14px, color secondary
- Read time: 14px, color secondary

**Share Buttons:**
- Size: 36px × 36px
- Border: 1px solid #E5E7EB
- Border-radius: 50%
- Color: Secondary text
- Hover: Primary color
- Gap: 8px

**Container:**
- Max-width: 800px
- Margin: 0 auto
- Padding: 40px 20px (mobile), 60px 40px (desktop)

---

### Block 03: Featured Image
```
┌─────────────────────────────────────┐
│                                     │
│     [Large Featured Image]          │
│                                     │
└─────────────────────────────────────┘
```

**Image:**
- Width: Full width (up to 1200px)
- Aspect ratio: 16:9 or 2:1
- Border-radius: 12px
- Alt text: Article title
- Margin: 0 0 40px

---

### Block 04: Article Content
```
┌─────────────────────────────────────┐
│                                     │
│  [Paragraph text...]                │
│                                     │
│  ## Subheading                      │
│                                     │
│  [More paragraphs...]               │
│                                     │
│  > Blockquote text...               │
│                                     │
│  - List item 1                      │
│  - List item 2                      │
│                                     │
│  [Image with caption]               │
│                                     │
│  ```code block```                   │
│                                     │
└─────────────────────────────────────┘
```

**Typography:**
- **Body Text:** 18px / 28px line-height
- **Paragraph Margin:** 0 0 24px
- **Max Width:** 680px (optimal readability)
- **Font:** Georgia, serif or Inter, sans-serif
- **Color:** #1F2937 (darker for readability)

**Headings:**
- **H2:** 28px / 36px, weight 700, margin 40px 0 16px
- **H3:** 22px / 30px, weight 600, margin 32px 0 12px
- **H4:** 18px / 26px, weight 600, margin 24px 0 8px

**Links:**
- Color: Primary (#6366F1)
- Text decoration: underline
- Hover: Darken 10%

**Blockquote:**
- Border-left: 4px solid #6366F1
- Padding-left: 20px
- Font-style: italic
- Color: #4B5563
- Margin: 32px 0
- Font size: 20px / 30px

**Lists:**
- Padding-left: 24px
- Margin: 24px 0
- List item margin: 8px 0

**Code Blocks:**
- Background: #F3F4F6
- Border-radius: 8px
- Padding: 16px
- Font: Roboto Mono, monospace
- Font size: 14px
- Overflow-x: auto

**Inline Code:**
- Background: #F3F4F6
- Padding: 2px 6px
- Border-radius: 4px
- Font: Roboto Mono

**Images in Content:**
- Max-width: 100%
- Height: auto
- Border-radius: 8px
- Margin: 32px 0
- Box-shadow: 0 4px 6px rgba(0,0,0,0.1)

**Image Captions:**
- Font size: 14px
- Color: #6B7280
- Text align: center
- Margin-top: 8px
- Font style: italic

**Container:**
- Max-width: 680px
- Margin: 0 auto
- Padding: 0 20px (mobile), 0 40px (desktop)

---

### Block 05: Article Footer
```
┌─────────────────────────────────────┐
│  [Tags: #AI #DigitalClone #Scaling] │
│                                     │
│  ──────────────────────             │
│                                     │
│  Share this article:                │
│  [Twitter] [LinkedIn] [Facebook] [Copy] │
│                                     │
└─────────────────────────────────────┘
```

**Tags:**
- Display: Flex, flex-wrap
- Gap: 8px
- Background: #F3F4F6
- Padding: 6px 12px
- Border-radius: 16px
- Font size: 13px
- Color: #4B5563
- Hover: Background #E5E7EB

**Share Section:**
- Margin-top: 32px
- Padding-top: 32px
- Border-top: 1px solid #E5E7EB

---

### Block 06: Author Bio Card
```
┌─────────────────────────────────────┐
│  ┌────────┐                         │
│  │        │  [Author Name]          │
│  │ Avatar │  [Job Title]            │
│  │        │                         │
│  └────────┘  [Short bio 2-3 lines]  │
│                                     │
│              [Twitter] [LinkedIn]   │
│                                     │
└─────────────────────────────────────┘
```

**Avatar:** 80px × 80px, border-radius 50%
**Name:** 18px, weight 600
**Title:** 14px, color primary
**Bio:** 15px / 22px, color secondary

**Container:**
- Background: #F9FAFB
- Border: 1px solid #E5E7EB
- Border-radius: 12px
- Padding: 24px
- Margin: 40px 0
- Max-width: 680px

---

### Block 07: Related Articles
```
┌─────────────────────────────────────┐
│  [H3: Related Articles]             │
│                                     │
│  [Card] [Card] [Card]               │
│                                     │
└─────────────────────────────────────┘
```

**Display:** 3 article cards (2 on tablet, 1 on mobile)
**Cards:** Same design as blog listing page cards
**Margin:** 60px 0

---

### Block 08: CTA Banner
```
┌─────────────────────────────────────┐
│  [H3: Ready to Create Your Clone?]  │
│  [Subtitle]                         │
│  [Get Started Free Button]          │
└─────────────────────────────────────┘
```

**Background:** Gradient or accent
**Padding:** 60px 20px
**Margin:** 60px 0

---

### Block 09: Footer
*(Same as Homepage)*

---

## Reading Experience Features

### 1. Reading Progress Bar
- Fixed top of viewport
- Width: % of article read
- Height: 3px
- Color: Primary
- Z-index: 1000

### 2. Table of Contents (Optional, for long articles)
- **Desktop:** Sticky sidebar (left or right)
- **Mobile:** Collapsible at top
- Auto-highlight current section

### 3. Floating Share Buttons (Desktop)
- **Position:** Fixed left side, vertically centered
- **Icons:** Twitter, LinkedIn, Facebook, Copy
- **Size:** 40px × 40px each
- **Stack vertically**
- **Sticky:** Follow scroll, hide at top/bottom

---

## Interactive Elements

### 1. Social Share
- Twitter: Pre-filled text with title + URL
- LinkedIn: Share URL
- Facebook: Share URL
- Copy link: Copy to clipboard, show "Copied!" tooltip

### 2. Image Lightbox
- Click content images to enlarge
- Dark overlay
- Close with X or click outside
- Keyboard: ESC to close, arrows for multiple images

### 3. Anchor Links
- Headings are anchor links (#heading-slug)
- Hover: Show link icon
- Click: Scroll to section, update URL

---

## SEO

**Title:** "{Article Title} | Delphi Blog"
**Description:** First 155 characters of article or custom excerpt
**Canonical:** `https://www.delphi.ai/blog/{slug}`
**OG Image:** Featured image (1200×630)

**Structured Data:**
```json
{
  "@type": "BlogPosting",
  "headline": "Article Title",
  "image": "featured-image.jpg",
  "datePublished": "2025-11-07",
  "dateModified": "2025-11-08",
  "author": {
    "@type": "Person",
    "name": "Author Name"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Delphi"
  },
  "description": "Article excerpt"
}
```

**Schema:** Article, BreadcrumbList

---

## Accessibility

- Proper heading hierarchy (H1 → H2 → H3)
- Alt text on all images
- Sufficient color contrast (WCAG AA)
- Skip to content link
- Keyboard navigation for all interactive elements
- ARIA labels on share buttons

---

**End of Blog Article Page Template**
