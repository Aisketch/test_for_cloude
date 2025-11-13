# MIDOS Homepage - Technical Specification

**Page Type:** Landing Page
**URL:** `/en/` (homepage)  
**Priority:** Critical
**Approach:** Mobile First
**Language:** English (EN)
**Last Updated:** November 13, 2025

---

## Page Overview

**Purpose:** Primary landing page to introduce MIDOS Digital Twins platform, showcase product value, and drive users to book a personal demo.

**Key Goals:**
- Communicate core value proposition within 3 seconds
- Drive user to book a demo call
- Build trust through company story and team
- Educate about key platform capabilities

**Target Devices:**
- Mobile: 320px - 767px (Primary)
- Tablet: 768px - 1023px
- Desktop: 1024px+

---

## Page Structure (Top to Bottom)

### Block 01: Header Navigation
**Type:** Sticky Header  
**Mobile Height:** 64px
**Desktop Height:** 80px

#### Mobile Layout (320px - 767px)
```
┌─────────────────────────────────────┐
│ [Logo]              [☰ Menu]        │
└─────────────────────────────────────┘
```

**Components:**
- **Logo** (Left aligned)
  - Size: 120px × 32px
  - Link: `/en/`
  - Alt text: "MIDOS - AI Digital Twins Platform"
  
- **Hamburger Menu** (Right aligned)
  - Icon: 24px × 24px
  - Color: Primary text
  - Opens mobile navigation drawer

**Mobile Navigation Drawer:**
```
┌─────────────────────────────────────┐
│ [× Close]                           │
│                                     │
│ About                               │
│ Blog                                │
│ Documentation                       │
│ Contact                             │
│ ─────────────────                   │
│ [Book a Demo - CTA]                 │
└─────────────────────────────────────┘
```

#### Desktop Layout (1024px+)
```
┌────────────────────────────────────────────────────────────┐
│ [Logo]    About  Blog  Documentation  Contact  [Book a Demo] │
└────────────────────────────────────────────────────────────┘
```

**Navigation Items:**
- About → `/en/about`
- Blog → `/en/blog`
- Documentation → `https://docs.midos.io/en/`
- Contact → `/en/contact`
- Book a Demo → `/en/demo` (Primary CTA button)

**Behavior:**
- Sticky on scroll
- Background: White with shadow on scroll
- Z-index: 1000

---

### Block 02: Hero Section
**Mobile Height:** Auto (min 600px)
**Desktop Height:** Auto (min 700px)

#### Mobile Layout
```
┌─────────────────────────────────────┐
│                                     │
│         [H1 Headline]               │
│                                     │
│      [Subheadline]                  │
│                                     │
│   [Primary CTA Button]              │
│   [Secondary CTA Button]            │
│                                     │
│     [Hero Image/Video]              │
│                                     │
└─────────────────────────────────────┘
```

**Content:**

**H1 Headline:**
- Text: "One-on-one with everyone, all at the same time."
- Font size Mobile: 32px / 36px line-height
- Font size Desktop: 56px / 64px line-height
- Font weight: 700
- Color: Primary text (#0A0A0A)
- Max-width: 600px mobile, 800px desktop
- Text align: Center

**Subheadline:**
- Text: "Your style. Your wisdom. Your exclusive approach. Now available to everyone who needs you. Around the clock. One-on-one."
- Font size Mobile: 16px / 24px line-height
- Font size Desktop: 20px / 30px line-height
- Font weight: 400
- Color: Secondary text (#666666)
- Max-width: 500px mobile, 640px desktop
- Margin-top: 16px mobile, 24px desktop

**Primary CTA:**
- Text: "Book a Demo Call 1:1"
- URL: `/en/demo`
- Size Mobile: Full width (with 20px margin), Height 56px
- Size Desktop: Auto width (padding 24px 48px), Height 56px
- Font size: 16px
- Font weight: 600
- Background: Primary color (#0066FF)
- Text color: White
- Border-radius: 8px
- Margin-top: 32px

**Secondary CTA:**
- Text: "Watch Demo"
- URL: `#demo-video` or modal trigger
- Size Mobile: Full width (with 20px margin), Height 56px
- Size Desktop: Auto width (padding 24px 48px), Height 56px
- Font size: 16px
- Font weight: 600
- Background: Transparent
- Text color: Primary color (#0066FF)
- Border: 2px solid primary color
- Border-radius: 8px
- Margin-top: 12px

**Hero Visual:**
- Type: Image or Looping video
- Mobile: Full width, 300px height
- Desktop: 600px width, 450px height
- Alt text: "MIDOS Digital Twins - platform interface"
- Margin-top: 40px
- Border-radius: 12px
- Optional: Subtle shadow

**Image:**
```markdown
![MIDOS Platform Interface](./assets/images/[SCREENSHOT_HERO_PLATFORM].png)
<!-- IMAGE_REQUIRED: Hero screenshot showing MIDOS platform interface with digital twin conversation -->
```

#### Desktop Layout
```
┌───────────────────────────────────────────────────────────┐
│                                                           │
│   ┌─────────────────────┐     ┌──────────────────────┐  │
│   │                     │     │                      │  │
│   │   [H1 Headline]     │     │    [Hero Visual]     │  │
│   │                     │     │                      │  │
│   │ [Subheadline]       │     │    Image/Video       │  │
│   │                     │     │                      │  │
│   │ [CTA Buttons Row]   │     │                      │  │
│   │                     │     │                      │  │
│   └─────────────────────┘     └──────────────────────┘  │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

**Desktop Specific:**
- Two column layout: 50/50 split
- Text column: Left aligned
- Visual column: Right aligned
- Max-width container: 1200px
- Padding: 80px 40px

---

### Block 03: Features Overview - 3 Key Capabilities
**Mobile:** Vertical stack
**Desktop:** 3-column grid

#### Section Header
```
┌─────────────────────────────────────┐
│                                     │
│         [Eyebrow text]              │
│      [H2 Section Title]             │
│     [Section Description]           │
│                                     │
└─────────────────────────────────────┘
```

**Content:**
- Eyebrow: "Why MIDOS"
- Font size: 14px, uppercase, letter-spacing: 1.5px
- Color: Primary brand color (#0066FF)
- Font weight: 600

- H2: "Your AI Twin. Your Way."
- Font size Mobile: 28px / 34px line-height
- Font size Desktop: 40px / 48px line-height
- Font weight: 700

- Description: "Build a personalized digital twin that captures your knowledge, personality, and communication style."
- Font size: 16px / 24px line-height
- Color: Secondary text
- Max-width: 640px
- Margin: 0 auto

**Spacing:**
- Padding Mobile: 60px 20px
- Padding Desktop: 100px 40px

#### Feature Cards

**Mobile Layout (Stack):**
```
┌─────────────────────────────────────┐
│         [Icon 64×64]                │
│                                     │
│      [Feature Title]                │
│                                     │
│   [Feature description text]        │
│                                     │
└─────────────────────────────────────┘
[Gap: 32px]
┌─────────────────────────────────────┐
│         [Icon 64×64]                │
│      [Feature Title]                │
│   [Feature description]             │
└─────────────────────────────────────┘
```

**Desktop Layout:**
```
┌──────────┬──────────┬──────────┐
│ [Icon]   │ [Icon]   │ [Icon]   │
│ [Title]  │ [Title]  │ [Title]  │
│ [Desc]   │ [Desc]   │ [Desc]   │
└──────────┴──────────┴──────────┘
```

**Feature 1: AI Twin with Your Knowledge**
- Icon: AI/Brain icon
- Title: "Your AI twin knows everything you know"
- Description: "Answers 100+ questions daily. In your voice. With your expertise. While you do what you love."

**Feature 2: Unlimited Conversations**
- Icon: Network/Scale icon
- Title: "Unlimited personal conversations simultaneously"
- Description: "Every client gets personal attention and an individual approach. Whether there's 10 or 10,000 of them."

**Feature 3: Works 24/7**
- Icon: Clock/24-7 icon
- Title: "Works 24/7 while you live your life"
- Description: "Your digital twin doesn't sleep, eat, or take days off. Always available. You get back 20+ hours every week. For creativity. For family. For yourself."

**Card Styling:**
- Background: White or light grey (#F9FAFB)
- Padding Mobile: 24px
- Padding Desktop: 32px
- Border-radius: 12px
- Border: 1px solid #E5E7EB (optional)
- Hover effect: Subtle lift + shadow (desktop)

**Icon:**
- Size: 48px × 48px mobile, 64px × 64px desktop
- Style: Outlined or filled
- Color: Primary brand color (#0066FF)

**Title:**
- Font size: 20px / 24px line-height
- Font weight: 600
- Margin-top: 16px

**Description:**
- Font size: 15px / 22px line-height
- Color: Secondary text
- Margin-top: 8px

**Grid:**
- Mobile: 1 column, gap 32px
- Tablet: 2 columns, gap 24px
- Desktop: 3 columns, gap 32px

---


### Block 04: How It Works
**Purpose:** Show simple 3-step process

#### Section Header
```
┌─────────────────────────────────────┐
│                                     │
│      [H2: "How It Works"]           │
│   [Subheadline]                     │
│                                     │
└─────────────────────────────────────┘
```

**H2 Content:** "How It Works"
**Subheadline:** "Three simple steps to your digital twin"

**Mobile Layout (Vertical Timeline):**
```
┌─────────────────────────────────────┐
│  ①  [Step Number Badge]             │
│                                     │
│  [Step Title]                       │
│  [Step Description]                 │
│                                     │
│  [Illustration/Screenshot]          │
│                                     │
│         ↓                           │
│                                     │
│  ②  [Step 2...]                     │
│                                     │
│         ↓                           │
│                                     │
│  ③  [Step 3...]                     │
│                                     │
└─────────────────────────────────────┘
```

**Steps:**

**Step 1: Build Your Twin**
- Badge: "01"
- Title: "Build Your Twin"
- Description: "Upload your content or take the MIDOS Interview. Our AI learns your knowledge, tone, and personality in minutes."
- Image: `[SCREENSHOT_STEP_1_BUILD]`
<!-- IMAGE_REQUIRED: Screenshot of content upload interface -->

**Step 2: Customize It**
- Badge: "02"
- Title: "Customize It"
- Description: "Fine-tune response style, personality traits, and communication manner. Make it truly yours with advanced settings."
- Image: `[SCREENSHOT_STEP_2_CUSTOMIZE]`
<!-- IMAGE_REQUIRED: Screenshot of customization dashboard -->

**Step 3: Launch and Scale**
- Badge: "03"  
- Title: "Launch and Scale"
- Description: "Deploy your AI twin across all platforms. Engage with your audience 24/7 while you focus on high-value work."
- Image: `[SCREENSHOT_STEP_3_LAUNCH]`
<!-- IMAGE_REQUIRED: Screenshot of deployment options -->

**Step Badge:**
- Size: 48px × 48px
- Background: Primary color with 10% opacity
- Border: 2px solid primary color
- Font size: 20px
- Font weight: 700
- Border-radius: 50%
- Color: Primary color (#0066FF)

**Desktop Layout:**
- Alternating left-right layout
- Step 1: Content left, image right
- Step 2: Image left, content right  
- Step 3: Content left, image right
- Max-width: 1100px

**Spacing:**
- Section padding Mobile: 60px 20px
- Section padding Desktop: 100px 40px
- Gap between steps: 48px mobile, 80px desktop

---

### Block 05: Company Story (instead of Featured Digital Minds)

**Purpose:** Share MIDOS founding story and build emotional connection

#### Section Header
```
┌─────────────────────────────────────┐
│                                     │
│  [H2: "How It All Started"]         │
│  [Subheadline]                      │
│                                     │
└─────────────────────────────────────┘
```

**Content:**
- H2: "How It All Started"
- Subheadline: "The story of one sleepless night that changed everything"

**Story Content:**

**The Breakthrough Moment**
```
┌─────────────────────────────────────┐
│                                     │
│  📅 June 1, 2025, 2:47 AM           │
│                                     │
│  Yuriy Boh sat at his kitchen table,│
│  responding to repetitive client    │
│  emails about marketing positioning.│
│                                     │
│  Instead of sleeping, he compiled   │
│  a decade of professional knowledge │
│  — hundreds of notes and thousands  │
│  of words — into a single document  │
│  and uploaded it to AI.             │
│                                     │
│  When he asked: "How do you build   │
│  a marketing strategy for a         │
│  psychologist?" — the AI responded  │
│  with remarkable clarity: "his      │
│  words. His thinking structure. His │
│  examples."                         │
│                                     │
│  This revelation sparked a pivotal  │
│  question: What if every expert     │
│  could transfer their knowledge     │
│  into a digital version capable of  │
│  serving thousands simultaneously?  │
│                                     │
└─────────────────────────────────────┘
```

**Our Mission**
- Heading: "Our Mission"
- Text: "Free from repetition. Scale impact. Return life."
- Extended description: "We don't sell technology. We return to experts the right to their own lives. More successful experts means more imprisonment in their own success. More clients = less time for each. More questions = more repetition. More impact = more burnout. MIDOS breaks this cycle."

**Our Vision**
- Heading: "Our Vision"  
- Text: "Your AI twin works in the digital world, while you live in reality."
- Extended description: "A world where digital and real are naturally divided. Your AI twin works 24/7 — answering emails at 3 AM, conducting cross-timezone consultations, handling hundreds of simultaneous inquiries. And you live your real life — family without phones, strategic creative work, genuine presence."

**Styling:**
- Background: Light grey (#F9FAFB) or gradient
- Padding Mobile: 60px 20px
- Padding Desktop: 100px 40px
- Max-width text: 700px centered

---

### Block 06: Testimonials  
**Status:** SKIPPED - no real testimonials (MVP stage)

```markdown
<!-- BLOCK_SKIPPED: Testimonials -->
<!-- REASON: MVP stage - no real customer testimonials yet -->
<!-- TODO: Add testimonials after first 10 customers -->
```

---

### Block 07: Team
**Purpose:** Show founding team

#### Section Header
```
┌─────────────────────────────────────┐
│                                     │
│  [H2: "The Team Behind It"]         │
│  [Subheadline]                      │
│                                     │
└─────────────────────────────────────┘
```

**Content:**
- H2: "The Team Behind It"
- Subheadline: "Three co-founders with expertise in marketing, operations, and technology"

**Team Grid (3 columns Desktop, stack Mobile):**

**Team Member 1:**
```
┌──────────────────────┐
│                      │
│   [Photo 3:4]        │
│                      │
│   Yuriy Boh          │
│   CEO & Co-Founder   │
│                      │
│   Head of            │
│   Marketing          │
│                      │
└──────────────────────┘
```
- Name: Yuriy Boh
- Position: CEO & Co-Founder
- Role: Head of Marketing
- Photo: `[TEAM_PHOTO_YURIY_BOH]`
<!-- IMAGE_REQUIRED: Professional photo of Yuriy Boh, format 3:4 -->

**Team Member 2:**
- Name: Yana Barko
- Position: COO & Co-Founder
- Role: Head of Operations
- Photo: `[TEAM_PHOTO_YANA_BARKO]`
<!-- IMAGE_REQUIRED: Professional photo of Yana Barko, format 3:4 -->

**Team Member 3:**
- Name: Dmytro Zahorulko
- Position: CTO & Co-Founder
- Role: Head of Technology
- Photo: `[TEAM_PHOTO_DMYTRO_ZAHORULKO]`
<!-- IMAGE_REQUIRED: Professional photo of Dmytro Zahorulko, format 3:4 -->

**Card Styling:**
- Photo size: Full card width, 3:4 aspect ratio
- Border-radius: 12px
- Padding: 24px
- Background: White
- Border: 1px solid #E5E7EB

**Name:**
- Font size: 20px
- Font weight: 600
- Margin-top: 16px

**Title:**
- Font size: 14px
- Color: Primary brand color (#0066FF)
- Margin-top: 4px

**Role:**
- Font size: 15px / 22px line-height
- Color: Secondary text
- Margin-top: 12px

---

### Block 08: Demo Booking (instead of Pricing Teaser)
**Purpose:** Drive users to book personal demo

```
┌─────────────────────────────────────┐
│                                     │
│  [H2: "Ready to See MIDOS            │
│        in Action?"]                 │
│  [Subheadline]                      │
│                                     │
│  ┌──────────────────────────────┐  │
│  │                              │  │
│  │   [Demo Booking Card]        │  │
│  │                              │  │
│  │   • Personal 1:1 demo        │  │
│  │   • 30 minutes with expert   │  │
│  │   • All questions answered   │  │
│  │   • Custom pricing           │  │
│  │                              │  │
│  │   [Book a Demo]              │  │
│  │                              │  │
│  └──────────────────────────────┘  │
│                                     │
└─────────────────────────────────────┘
```

**Content:**
- H2: "Ready to See MIDOS in Action?"
- Subheadline: "Book a personal demo with our team. We'll show you how MIDOS can transform your business."

**Demo Card:**
- Heading: "Personal Demo Call"
- Benefits list:
  - ✓ 1:1 platform walkthrough
  - ✓ 30 minutes with expert
  - ✓ All your questions answered
  - ✓ Custom pricing discussion
  - ✓ No commitment required

**CTA Button:**
- Text: "Book a Demo Call 1:1"
- URL: `/en/demo`
- Style: Primary button (full width on mobile)
- Size: Height 56px
- Background: Primary color (#0066FF)

**Alternative Link:**
- Text: "Or email us → hello@midos.io"
- Font size: 14px
- Color: Secondary text
- Margin-top: 16px

---

### Block 09: Final CTA Section
**Purpose:** Last conversion opportunity

**Background:** Gradient (Primary to Secondary brand color)

```
┌─────────────────────────────────────┐
│                                     │
│     [H2: Strong CTA headline]       │
│                                     │
│     [Supporting text]               │
│                                     │
│     [Primary CTA Button]            │
│     [Secondary text link]           │
│                                     │
└─────────────────────────────────────┘
```

**Content:**
- H2: "Ready to Return to Your Life?"
- Font size Mobile: 28px / 34px line-height
- Font size Desktop: 40px / 48px line-height
- Color: White (dark background)
- Text align: Center

- Subtext: "Join experts using MIDOS to scale their impact. Start with a personal demo."
- Font size: 18px / 26px line-height
- Color: White with 90% opacity
- Margin-top: 16px

- Primary CTA: "Book a Demo Call 1:1"
- URL: `/en/demo`
- Size Mobile: Full width (max 400px)
- Size Desktop: Auto width (padding 24px 64px)
- Height: 56px
- Background: White
- Text color: Primary brand color (#0066FF)
- Font size: 16px
- Font weight: 600
- Margin-top: 32px

- Secondary link: "Watch Video Demo"
- Font size: 16px
- Color: White
- Text decoration: Underline
- Margin-top: 16px

**Section Styling:**
- Background: Linear gradient (#0066FF to #7928CA)
- Padding Mobile: 60px 20px
- Padding Desktop: 100px 40px
- Text align: Center

---


### Block 10: Footer
**Type:** Multi-column footer

#### Mobile Layout (Stacked Sections)
```
┌─────────────────────────────────────┐
│  [Logo]                             │
│  [Tagline]                          │
│                                     │
│  Product                            │
│  - Documentation                    │
│  - Blog                             │
│                                     │
│  Company                            │
│  - About                            │
│  - Team                             │
│  - Contact                          │
│                                     │
│  [Social Icons]                     │
│  [LinkedIn] [Instagram] [X]         │
│  [Facebook] [YouTube] [TikTok]      │
│  [Telegram]                         │
│                                     │
│  ─────────────────────              │
│                                     │
│  © 2025 MIDOS.IO.                   │
│  All rights reserved.               │
│                                     │
│  Ukraine, Kyiv, Shevchenko 23       │
│                                     │
└─────────────────────────────────────┘
```

#### Desktop Layout (Multi-column)
```
┌───────────────────────────────────────────────────────────┐
│                                                           │
│  [Logo]           Product      Company                   │
│  [Tagline]        - Documentation - About                │
│                   - Blog        - Team                   │
│  [Social Icons]                 - Contact                │
│                                                           │
│  ─────────────────────────────────────────────────────   │
│                                                           │
│  © 2025 MIDOS.IO. All rights reserved.  [Social Icons]   │
│  Ukraine, Kyiv, Shevchenko 23                            │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

**Logo Section:**
- Logo: 140px × 36px
- Tagline: "One-on-one with everyone, all at the same time."
- Font size: 14px
- Color: Secondary text (#6B7280)
- Max-width: 280px
- Margin-top: 12px

**Footer Columns:**

**Column 1: Product**
- Documentation → `https://docs.midos.io/en/`
- Blog → `/en/blog`

**Column 2: Company**
- About → `/en/about`
- Team → `/en/about#team`
- Contact → `/en/contact`

**Column Heading:**
- Font size: 14px
- Font weight: 600
- Color: Primary text
- Margin-bottom: 12px
- Text transform: Uppercase
- Letter spacing: 0.5px

**Footer Links:**
- Font size: 14px
- Color: Secondary text (#6B7280)
- Line-height: 32px
- Hover: Primary color (#0066FF)

**Social Icons:**
- Size: 24px × 24px
- Color: Secondary text
- Hover: Primary color
- Gap: 16px
- Display: Flex row

**Social Links:**
- LinkedIn → `https://www.linkedin.com/company/midos_io`
- Instagram → `https://www.instagram.com/midos_io`
- X (Twitter) → `https://x.com/midos_io`
- Facebook → `https://www.facebook.com/people/Midos/61581132000448/`
- YouTube → `https://www.youtube.com/@midos_io`
- TikTok → `https://www.tiktok.com/@midos_io`
- Telegram → `https://t.me/midos_io`

**Copyright Bar:**
- Text: "© 2025 MIDOS.IO. All rights reserved."
- Address: "Ukraine, Kyiv, Shevchenko Street 23"
- Email: "hello@midos.io"
- Font size: 14px
- Color: Secondary text (#6B7280)
- Padding-top: 24px
- Border-top: 1px solid #E5E7EB

**Footer Styling:**
- Background: #F9FAFB or White
- Padding Mobile: 48px 20px 24px
- Padding Desktop: 60px 40px 32px
- Border-top: 1px solid #E5E7EB (optional)

**Grid:**
- Mobile: 1 column, stack all sections
- Tablet: 2 columns (Logo + Product, Company)
- Desktop: 3 columns (Logo takes 2x width, others 1x)
- Gap: 40px mobile, 60px desktop

---

## Interactive Elements

### 1. Sticky Header
- **Trigger:** On scroll > 100px
- **Behavior:**
  - Add background color (white)
  - Add shadow: `0 2px 4px rgba(0,0,0,0.08)`
  - Reduce height by 10% (optional)
- **Animation:** Smooth transition 0.3s

### 2. Mobile Navigation
- **Open:** Slide from right, 300ms ease-out
- **Overlay:** Dark background, 40% opacity
- **Close:** Click overlay or close button
- **Lock scroll:** When menu open

### 3. Scroll Animations
- **Fade in:** Elements fade in as they enter viewport
- **Slide up:** Elements slide up 20px as they appear
- **Stagger:** Sequential animation for groups (50ms delay)
- **Trigger:** IntersectionObserver, threshold 0.2

### 4. Button States
- **Default:** Primary color background
- **Hover:** Darken 10%, lift 2px (desktop)
- **Active:** Scale 0.98
- **Focus:** Outline 2px primary color
- **Disabled:** 50% opacity, cursor not-allowed

### 5. Card Hover Effects (Desktop)
- **Default:** Shadow: `0 1px 3px rgba(0,0,0,0.1)`
- **Hover:**
  - Lift: `translateY(-4px)`
  - Shadow: `0 8px 16px rgba(0,0,0,0.15)`
  - Transition: 0.3s ease

---

## Performance Optimization

### Images
- **Format:** WebP with JPG fallback
- **Lazy loading:** All images below fold
- **Responsive:** srcset for different screen sizes
- **Compression:** 80% quality
- **Dimensions:** Serve appropriate sizes per breakpoint

### Hero Video (if applicable)
- **Format:** MP4 (H.264)
- **Size:** Max 5MB
- **Dimensions:** 1920×1080 max
- **Autoplay:** Muted, loop, no controls
- **Fallback:** Static image for mobile

### Fonts
- **Loading:** font-display: swap
- **Subset:** Latin characters
- **Formats:** WOFF2 primary, WOFF fallback
- **Preload:** Critical fonts only

### JavaScript
- **Loading:** Defer non-critical scripts
- **Bundling:** Code splitting by route
- **Minification:** Production builds
- **Caching:** Aggressive cache headers

### CSS
- **Critical CSS:** Inline above-fold styles
- **Loading:** Defer non-critical stylesheets
- **Minification:** Remove whitespace, comments
- **Purge:** Remove unused styles

---

## Accessibility Requirements

### Semantic HTML
- Use appropriate heading hierarchy (H1 → H2 → H3)
- Use `<nav>`, `<main>`, `<section>`, `<article>` landmarks
- Use `<button>` for interactive elements, not `<div>`

### ARIA Labels
- Navigation: `aria-label="Main navigation"`
- Hamburger: `aria-label="Toggle menu"` + `aria-expanded`
- Buttons: Descriptive `aria-label` when text isn't clear

### Keyboard Navigation
- All interactive elements must be focusable
- Tab order must be logical
- Focus indicators must be visible (outline)
- Escape key closes modals/menus

### Screen Readers
- Images: Descriptive alt texts
- Icons: `aria-label` or `aria-hidden="true"` if decorative
- Links: Clear purpose, avoid "click here"
- Form inputs: Associated labels

### Color Contrast
- Text on backgrounds: WCAG AA minimum (4.5:1)
- Large text (18px+): 3:1 minimum
- Interactive elements: 3:1 against background

---

## Responsive Breakpoints

```css
/* Mobile First Approach */

/* Mobile Small: 320px - 374px */
@media (min-width: 320px) { }

/* Mobile Medium: 375px - 424px */
@media (min-width: 375px) { }

/* Mobile Large: 425px - 767px */
@media (min-width: 425px) { }

/* Tablet: 768px - 1023px */
@media (min-width: 768px) { }

/* Desktop: 1024px - 1439px */
@media (min-width: 1024px) { }

/* Desktop Large: 1440px+ */
@media (min-width: 1440px) { }
```

**Container Max-widths:**
- Mobile: 100% (with 20px padding)
- Tablet: 720px
- Desktop: 1100px
- Desktop Large: 1200px

---

## Design Tokens

### Colors
```
Primary Brand: #0066FF (Vibrant Blue)
Primary Hover: #0052CC
Secondary Brand: #7928CA (Transformational Purple)
Tertiary Brand: #3D25D3 (Deep Indigo)

Primary Text: #0A0A0A (Near Black)
Secondary Text: #6B7280 (Grey)
Tertiary Text: #9CA3AF (Light Grey)

Background Primary: #FFFFFF (White)
Background Secondary: #F9FAFB (Light Grey)
Background Accent: #EEF2FF (Light Blue)

Border Default: #E5E7EB (Light Grey)
Border Focus: #0066FF (Primary)

Success: #10B981 (Green)
Warning: #F59E0B (Orange)
Error: #EF4444 (Red)
Info: #3B82F6 (Blue)
```

### Typography
```
Font Family:
  - Primary: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif
  - Headings: 'Alegreya Sans', sans-serif
  - Mono: 'Roboto Mono', 'Courier New', monospace

Font Sizes (Mobile / Desktop):
  - H1: 32px / 56px
  - H2: 28px / 40px
  - H3: 24px / 32px
  - H4: 20px / 24px
  - Body: 16px / 16px
  - Small: 14px / 14px
  - Tiny: 12px / 12px

Font Weights:
  - Regular: 400
  - Medium: 500
  - Semibold: 600
  - Bold: 700

Line Heights:
  - Tight: 1.2
  - Normal: 1.5
  - Relaxed: 1.75
```

### Spacing Scale
```
xs: 4px
sm: 8px
md: 16px
lg: 24px
xl: 32px
2xl: 40px
3xl: 48px
4xl: 64px
5xl: 80px
6xl: 100px
```

### Border Radius
```
sm: 4px
md: 8px
lg: 12px
xl: 16px
2xl: 24px
full: 9999px (circles)
```

### Shadows
```
sm: 0 1px 2px rgba(0,0,0,0.05)
md: 0 4px 6px rgba(0,0,0,0.1)
lg: 0 10px 15px rgba(0,0,0,0.1)
xl: 0 20px 25px rgba(0,0,0,0.15)
```

---

## Animation Timing
```
Fast: 150ms
Normal: 300ms
Slow: 500ms

Easing:
  - ease-out: cubic-bezier(0, 0, 0.2, 1)
  - ease-in: cubic-bezier(0.4, 0, 1, 1)
  - ease-in-out: cubic-bezier(0.4, 0, 0.2, 1)
```

---

## SEO Metadata

### Meta Tags (HTML Head)

#### English Version
```html
<!-- Primary Meta Tags -->
<title>MIDOS - One-on-one with everyone, all at the same time. | AI Digital Twins</title>
<meta name="title" content="MIDOS - One-on-one with everyone, all at the same time." />
<meta name="description" content="Create your AI twin that works 24/7. Scale your expertise without burnout. Get back 20+ hours every week." />
<meta name="keywords" content="AI twin, digital twin, artificial intelligence, automation, business scaling" />
<meta name="theme-color" content="#0066FF" />
<meta name="robots" content="index, follow" />
<link rel="canonical" href="https://midos.io/en/" />

<!-- Open Graph / Facebook -->
<meta property="og:type" content="website" />
<meta property="og:url" content="https://midos.io/en/" />
<meta property="og:title" content="MIDOS - One-on-one with everyone, all at the same time." />
<meta property="og:description" content="Create your AI twin that works 24/7. Scale your expertise without burnout." />
<meta property="og:image" content="https://midos.io/images/og-image-en.png" />
<meta property="og:locale" content="en_US" />
<meta property="og:locale:alternate" content="uk_UA" />

<!-- Twitter -->
<meta property="twitter:card" content="summary_large_image" />
<meta property="twitter:url" content="https://midos.io/en/" />
<meta property="twitter:title" content="MIDOS - One-on-one with everyone, all at the same time." />
<meta property="twitter:description" content="Create your AI twin that works 24/7." />
<meta property="twitter:image" content="https://midos.io/images/twitter-image-en.png" />

<!-- Hreflang -->
<link rel="alternate" hreflang="en" href="https://midos.io/en/" />
<link rel="alternate" hreflang="uk" href="https://midos.io/" />
<link rel="alternate" hreflang="x-default" href="https://midos.io/en/" />

<!-- Favicon -->
<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png" />
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png" />
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png" />
```

### Structured Data (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "MIDOS",
  "legalName": "MIDOS.IO",
  "url": "https://midos.io",
  "logo": "https://midos.io/logo.png",
  "foundingDate": "2025-09-07",
  "founders": [
    {
      "@type": "Person",
      "name": "Yuriy Boh"
    },
    {
      "@type": "Person",
      "name": "Yana Barko"
    },
    {
      "@type": "Person",
      "name": "Dmytro Zahorulko"
    }
  ],
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Shevchenko Street 23",
    "addressLocality": "Kyiv",
    "addressCountry": "UA"
  },
  "contactPoint": {
    "@type": "ContactPoint",
    "telephone": "",
    "contactType": "Customer Service",
    "email": "hello@midos.io",
    "availableLanguage": ["Ukrainian", "English"]
  },
  "sameAs": [
    "https://www.linkedin.com/company/midos_io",
    "https://www.instagram.com/midos_io",
    "https://x.com/midos_io",
    "https://www.facebook.com/people/Midos/61581132000448/",
    "https://www.youtube.com/@midos_io",
    "https://www.tiktok.com/@midos_io",
    "https://t.me/midos_io"
  ]
}
```

---

## Testing Checklist

### Functional Testing
- [ ] All links navigate to correct URLs
- [ ] All buttons trigger correct actions
- [ ] Navigation menu opens/closes correctly
- [ ] CTA buttons are clickable and lead to correct pages

### Responsive Testing
- [ ] Test on iPhone SE (320px)
- [ ] Test on iPhone 12/13 (390px)
- [ ] Test on iPad (768px)
- [ ] Test on Desktop (1280px, 1920px)
- [ ] Test landscape orientation on mobile/tablet
- [ ] Check text doesn't overflow containers
- [ ] Images scale properly without distortion

### Browser Testing
- [ ] Chrome (latest)
- [ ] Firefox (latest)
- [ ] Safari (latest)
- [ ] Edge (latest)
- [ ] Mobile Safari (iOS)
- [ ] Chrome Mobile (Android)

### Performance Testing
- [ ] Lighthouse score > 90
- [ ] First Contentful Paint < 1.5s
- [ ] Largest Contentful Paint < 2.5s
- [ ] Total page weight < 2MB
- [ ] Images optimized (WebP)
- [ ] Fonts loaded efficiently

### Accessibility Testing
- [ ] Keyboard navigation works
- [ ] Screen reader tested (NVDA/VoiceOver)
- [ ] Color contrast passes WCAG AA
- [ ] Focus indicators visible
- [ ] ARIA labels present where needed
- [ ] Semantic HTML used
- [ ] Alt text on all images

---

## Developer Notes

### Tech Stack Recommendations
- **Framework:** React, Next.js, or Nuxt
- **Styling:** Tailwind CSS or CSS Modules
- **Animations:** Framer Motion or GSAP
- **Forms:** React Hook Form + Zod validation

### Page Load Priorities
1. **Critical:** Header, Hero section, fonts
2. **High:** Features, How It Works
3. **Medium:** Company Story, Team
4. **Low:** Footer

---

## Version History

**v1.0** - November 13, 2025
- Initial MIDOS homepage specification (English version)
- Mobile-first approach
- Complete block breakdown from header to footer
- Adapted for MVP stage (no testimonials, demo booking instead of pricing)

---

**End of MIDOS Homepage Specification (EN)**

