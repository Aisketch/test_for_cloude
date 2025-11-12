# Explore/Catalog Page Template - Technical Specification

**Page Type:** Directory/Catalog Page
**URL Pattern:** `/explore`
**Priority:** High
**Approach:** Mobile First
**Last Updated:** November 12, 2025

---

## Page Overview

**Purpose:** Showcase all available Digital Minds, enable filtering by category, and drive users to try or engage with AI clones.

**Key Goals:**
- Display comprehensive catalog of Digital Minds
- Enable easy filtering and discovery
- Showcase diversity of expertise areas
- Drive clicks to individual Digital Mind profiles
- Encourage sign-ups to create own Digital Mind

**Target Devices:**
- Mobile: 320px - 767px (Primary)
- Tablet: 768px - 1023px
- Desktop: 1024px+

---

## Page Structure (Top to Bottom)

### Block 01: Header Navigation
**Type:** Sticky Header (Same as Homepage)

**Mobile:**
```
┌─────────────────────────────────────┐
│ [Logo]              [☰ Menu]        │
└─────────────────────────────────────┘
```

**Desktop:**
```
┌─────────────────────────────────────────────────────────────┐
│ [Logo]    Explore  Pricing  About  Docs    Sign In  [Get Started] │
└─────────────────────────────────────────────────────────────┘
```

**Active State:** "Explore" link is highlighted/bold

---

### Block 02: Page Hero/Header
**Mobile Height:** Auto (min 200px)
**Desktop Height:** Auto (min 250px)

#### Layout
```
┌─────────────────────────────────────┐
│                                     │
│      [H1: Explore Digital Minds]    │
│                                     │
│      [Subtitle description]         │
│                                     │
│   ┌──────────────────────────────┐  │
│   │ 🔍 [Search input]           │  │
│   └──────────────────────────────┘  │
│                                     │
└─────────────────────────────────────┘
```

**Content:**

**H1:**
- Text: "Explore Digital Minds"
- Font size Mobile: 32px / 38px line-height
- Font size Desktop: 48px / 56px line-height
- Font weight: 700
- Color: Primary text
- Text align: Center

**Subtitle:**
- Text: "Get personalized advice from world-class experts in business, health, marketing, technology, and more."
- Font size Mobile: 16px / 24px line-height
- Font size Desktop: 18px / 28px line-height
- Color: Secondary text
- Max-width: 640px
- Margin: 0 auto
- Text align: Center
- Margin-top: 12px

**Search Input:**
- Placeholder: "Search by name, expertise, or topic..."
- Width Mobile: Full width (20px padding)
- Width Desktop: 600px max
- Height: 52px
- Border: 1px solid #D1D5DB
- Border-radius: 12px
- Padding: 0 16px 0 48px (space for icon)
- Font size: 16px
- Margin-top: 32px

**Search Icon:**
- Position: Absolute, left 16px
- Size: 20px × 20px
- Color: #9CA3AF

**Styling:**
- Background: White or light gradient
- Padding Mobile: 40px 20px
- Padding Desktop: 60px 40px 40px
- Border-bottom: 1px solid #E5E7EB (optional)

---

### Block 03: Filter Section
**Type:** Horizontal scrollable pills (mobile), Tabs (desktop)

#### Mobile Layout
```
┌─────────────────────────────────────┐
│ [All] [Spotlight] [Business] [Tech] → │
└─────────────────────────────────────┘
```

#### Desktop Layout
```
┌──────────────────────────────────────────────────────────┐
│ [All] [Spotlight] [Marketing] [Tech] [Health] [Business] [Life] │
└──────────────────────────────────────────────────────────┘
```

**Filter Categories:**
1. **All** - Show all Digital Minds
2. **Spotlight** - Featured/Recommended
3. **Marketing** - Marketing experts
4. **Tech** - Technology and product experts
5. **Health** - Health and wellness experts
6. **Business** - Business and finance experts
7. **Life** - Life coaching and personal development

**Pill/Tab Styling:**
- **Default State:**
  - Background: Transparent
  - Border: 1px solid #E5E7EB
  - Color: Secondary text (#6B7280)
  - Padding: 10px 20px
  - Border-radius: 24px (full rounded)
  - Font size: 14px
  - Font weight: 500

- **Active State:**
  - Background: Primary color (#6366F1)
  - Border: 1px solid Primary color
  - Color: White
  - Font weight: 600

- **Hover (Desktop):**
  - Background: #F3F4F6
  - Border: 1px solid #D1D5DB

**Mobile Behavior:**
- Horizontal scroll
- No scrollbar visible (hide with CSS)
- Snap scroll optional
- White space: nowrap

**Desktop Behavior:**
- Centered horizontally
- Flex row with gap
- All visible, no scroll

**Container:**
- Padding Mobile: 16px 20px
- Padding Desktop: 24px 40px
- Background: White
- Border-bottom: 1px solid #E5E7EB
- Sticky: Optional (stick below header)
- Z-index: 100

**Gap between pills:** 8px mobile, 12px desktop

---

### Block 04: Results Count
**Purpose:** Show number of results

```
┌─────────────────────────────────────┐
│ Showing 48 Digital Minds            │
└─────────────────────────────────────┘
```

**Content:**
- Text: "Showing [X] Digital Minds" or "Showing [X] results in [Category]"
- Font size: 14px
- Color: Secondary text
- Padding: 16px 20px (mobile), 20px 40px (desktop)

---

### Block 05: Spotlight Section (When "Spotlight" or "All" active)
**Purpose:** Highlight featured Digital Minds

```
┌─────────────────────────────────────┐
│  ⭐ Spotlight                        │
│                                     │
│  [Large Featured Card]              │
│                                     │
│  [Card] [Card] [Card]               │
│                                     │
└─────────────────────────────────────┘
```

**Section Header:**
- Icon: ⭐ or "Featured" badge
- Text: "Spotlight"
- Font size: 20px
- Font weight: 600
- Margin-bottom: 20px

**Large Featured Card (First spotlight):**

**Mobile:**
```
┌────────────────────────────────────┐
│                                    │
│  ┌──────────────────────────────┐  │
│  │    [Large Profile Image]     │  │
│  └──────────────────────────────┘  │
│                                    │
│  [Name]                            │
│  [Title/Expertise]                 │
│                                    │
│  [Bio text - 2-3 lines]            │
│                                    │
│  [Topics Tags]                     │
│                                    │
│  [Try Now →]                       │
│                                    │
└────────────────────────────────────┘
```

**Content:**
- Profile Image: 200px × 200px (mobile), 280px × 280px (desktop)
- Border-radius: 16px
- Name: 24px / 28px, weight 700
- Title: 16px, primary color
- Bio: 15px / 22px, 2-3 lines max
- Tags: Pill style, small
- CTA: Primary button

**Desktop:**
```
┌───────────────────────────────────────────────────────┐
│                                                       │
│  ┌──────────┐                                        │
│  │          │  [Name]                                │
│  │  Image   │  [Title/Expertise]                     │
│  │          │                                        │
│  └──────────┘  [Bio text - 3-4 lines]                │
│                                                       │
│                [Topics Tags]                         │
│                                                       │
│                [Try Now →]                           │
│                                                       │
└───────────────────────────────────────────────────────┘
```

**Desktop Specific:**
- Horizontal layout
- Image left, content right
- Max-width: 800px
- Padding: 32px
- Background: Gradient or accent background

**Remaining Spotlight Cards:**
- Display as regular cards (see Block 06)
- Show 2-3 more spotlight Digital Minds

---

### Block 06: Digital Minds Grid
**Purpose:** Main catalog grid of all Digital Minds

#### Mobile Layout (1 Column)
```
┌─────────────────────────────────────┐
│ ┌─────────────────────────────────┐ │
│ │                                 │ │
│ │  [Profile Image]                │ │
│ │                                 │ │
│ │  [Name]                         │ │
│ │  [Title]                        │ │
│ │                                 │ │
│ │  [Short Bio]                    │ │
│ │                                 │ │
│ │  [Tags]                         │ │
│ │                                 │ │
│ │  [Try Demo →]                   │ │
│ │                                 │ │
│ └─────────────────────────────────┘ │
│ [Gap]                               │
│ ┌─────────────────────────────────┐ │
│ │  [Next Card]                    │ │
│ └─────────────────────────────────┘ │
└─────────────────────────────────────┘
```

#### Tablet Layout (2 Columns)
```
┌────────────────────┬────────────────────┐
│  [Card]            │  [Card]            │
└────────────────────┴────────────────────┘
```

#### Desktop Layout (3-4 Columns)
```
┌──────────┬──────────┬──────────┬──────────┐
│ [Card]   │ [Card]   │ [Card]   │ [Card]   │
└──────────┴──────────┴──────────┴──────────┘
```

**Card Structure:**

```
┌──────────────────────┐
│                      │
│  [Profile Image]     │
│  120×120             │
│                      │
│  [Name]              │
│  [Title/Expertise]   │
│                      │
│  [Bio - 2 lines]     │
│                      │
│  [Tag] [Tag] [Tag]   │
│                      │
│  [Try Demo →]        │
│                      │
└──────────────────────┘
```

**Profile Image:**
- Size: 120px × 120px
- Border-radius: 50% (circle)
- Border: 3px solid #F3F4F6
- Object-fit: cover
- Margin: 0 auto 16px
- Position: Centered

**Name:**
- Font size: 18px / 20px (mobile/desktop)
- Font weight: 600
- Color: Primary text
- Text align: Center
- Margin-bottom: 4px

**Title/Expertise:**
- Font size: 14px
- Color: Primary brand color (#6366F1)
- Font weight: 500
- Text align: Center
- Margin-bottom: 12px

**Bio:**
- Font size: 14px / 20px line-height
- Color: Secondary text
- Text align: Center
- Lines: 2 max (clamp)
- Min-height: 40px (maintain consistent card heights)
- Margin-bottom: 12px

**Topic Tags:**
- Display: Flex, flex-wrap
- Justify: Center
- Gap: 6px
- Margin-bottom: 16px

**Tag Styling:**
- Background: #F3F4F6
- Color: #6B7280
- Font size: 12px
- Padding: 4px 10px
- Border-radius: 12px
- Max tags visible: 3 (hide overflow)

**CTA Link:**
- Text: "Try Demo →"
- Font size: 14px
- Font weight: 600
- Color: Primary color
- Text align: Center
- Hover: Underline
- Display: Block

**Card Container:**
- Background: White
- Padding Mobile: 24px 16px
- Padding Desktop: 28px 20px
- Border: 1px solid #E5E7EB
- Border-radius: 12px
- Hover (Desktop):
  - Transform: translateY(-4px)
  - Shadow: 0 8px 16px rgba(0,0,0,0.12)
  - Border-color: Primary color (subtle)
  - Transition: all 0.3s ease

**Grid Properties:**
- Mobile: 1 column, gap 20px
- Tablet: 2 columns, gap 24px
- Desktop: 3 columns (1024px-1280px), 4 columns (1280px+), gap 28px

**Grid Container:**
- Padding Mobile: 20px
- Padding Desktop: 40px
- Max-width: 1400px
- Margin: 0 auto

**Grid Items:** Minimum 12 cards visible initially

---

### Block 07: Load More
**Purpose:** Pagination or infinite scroll

#### Option A: Load More Button
```
┌─────────────────────────────────────┐
│                                     │
│     [Load More Button]              │
│                                     │
│  Showing 12 of 48 Digital Minds     │
│                                     │
└─────────────────────────────────────┘
```

**Button:**
- Text: "Load More"
- Width Mobile: Full width (max 400px)
- Width Desktop: Auto (padding 24px 48px)
- Height: 48px
- Background: White
- Color: Primary color
- Border: 2px solid Primary color
- Border-radius: 8px
- Font size: 16px
- Font weight: 600
- Hover (Desktop):
  - Background: Primary color
  - Color: White

**Counter Text:**
- Font size: 14px
- Color: Secondary text
- Text align: Center
- Margin-top: 16px

**Behavior:**
- Click loads 12 more cards
- Smooth scroll to first new card
- Update counter text
- Hide button when all loaded

#### Option B: Infinite Scroll
- Trigger when user scrolls to 80% of page
- Show loading spinner
- Load next batch (12 cards)
- Update URL with ?page=X parameter

**Container:**
- Padding: 40px 20px
- Text align: Center

---

### Block 08: CTA Banner
**Purpose:** Encourage users to create their own Digital Mind

```
┌─────────────────────────────────────┐
│                                     │
│  [Icon or Illustration]             │
│                                     │
│  [H2: Create Your Own Digital Mind] │
│                                     │
│  [Subtitle text]                    │
│                                     │
│  [Get Started Free Button]          │
│                                     │
└─────────────────────────────────────┘
```

**Content:**

**Icon/Illustration:**
- Size: 80px × 80px
- Style: Line illustration or icon
- Color: Primary color
- Margin-bottom: 20px
- Centered

**H2:**
- Text: "Create Your Own Digital Mind"
- Font size Mobile: 24px / 30px line-height
- Font size Desktop: 32px / 40px line-height
- Font weight: 700
- Color: Primary text
- Text align: Center

**Subtitle:**
- Text: "Join 10,000+ experts who are scaling their impact with AI. Get started in minutes."
- Font size: 16px / 24px line-height
- Color: Secondary text
- Max-width: 500px
- Margin: 12px auto 0
- Text align: Center

**CTA Button:**
- Text: "Get Started Free"
- URL: `/signup`
- Width Mobile: Full width (max 360px)
- Width Desktop: Auto (padding 24px 48px)
- Height: 56px
- Background: Primary color
- Color: White
- Border-radius: 8px
- Font size: 16px
- Font weight: 600
- Margin-top: 24px

**Container:**
- Background: #F9FAFB or light gradient
- Border: 1px solid #E5E7EB
- Border-radius: 16px
- Padding Mobile: 40px 20px
- Padding Desktop: 60px 40px
- Margin: 60px 20px (mobile), 80px auto (desktop)
- Max-width: 800px
- Text align: Center

---

### Block 09: Footer
**Type:** Multi-column footer (Same as Homepage)

**Mobile (Stacked):**
```
┌─────────────────────────────────────┐
│  [Logo]                             │
│  [Tagline]                          │
│                                     │
│  Product                            │
│  Resources                          │
│  Company                            │
│                                     │
│  [Social Icons]                     │
│                                     │
│  © 2025 Delphi                      │
└─────────────────────────────────────┘
```

**Desktop:**
```
┌───────────────────────────────────────────────────────┐
│ [Logo]     Product    Resources    Company           │
│ [Tagline]                                             │
│ [Social]                                              │
│                                                       │
│ © 2025 Delphi. All rights reserved.  [Social Icons]  │
└───────────────────────────────────────────────────────┘
```

*(Full footer spec same as Homepage template)*

---

## Interactive Elements

### 1. Search Functionality
**Behavior:**
- **Real-time search:** Filter as user types (debounce 300ms)
- **Search scope:** Name, title, bio, tags
- **No results:** Show "No Digital Minds found. Try different keywords." message
- **Clear button:** X icon appears when text entered

**Implementation:**
- Use Fuse.js or similar for fuzzy search
- Highlight matching text (optional)
- Preserve filter selection during search

### 2. Category Filters
**Behavior:**
- **Click:** Filter cards by category
- **Active state:** Highlight selected filter
- **URL update:** Update URL with ?category=X parameter
- **Preserve search:** Keep search query active when filtering
- **Animation:** Fade out old cards, fade in new cards (300ms)

**Mobile:**
- Scroll selected filter into view
- Maintain scroll position of pill container

### 3. Card Hover (Desktop Only)
**Default:**
- Border: 1px solid #E5E7EB
- Shadow: 0 1px 3px rgba(0,0,0,0.1)
- Transform: none

**Hover:**
- Border: 1px solid #A5B4FC (light primary)
- Shadow: 0 8px 16px rgba(0,0,0,0.12)
- Transform: translateY(-4px)
- Transition: all 0.3s ease

**Click:**
- Navigate to Digital Mind profile page
- Or open modal/drawer with details

### 4. Load More / Infinite Scroll
**Load More Button:**
- Click: Load next batch
- Loading state: Show spinner in button, disable button
- Success: Append new cards, update counter
- Smooth scroll to first new card

**Infinite Scroll:**
- Trigger at 80% scroll position
- Show loading indicator at bottom
- Load next batch
- Update URL with page parameter

### 5. Empty States

**No Results (Search):**
```
┌─────────────────────────────────────┐
│                                     │
│     [🔍 Icon]                       │
│                                     │
│  No Digital Minds found             │
│                                     │
│  Try different keywords or filters  │
│                                     │
│  [Clear Search Button]              │
│                                     │
└─────────────────────────────────────┘
```

**No Results (Category):**
```
┌─────────────────────────────────────┐
│     [Icon]                          │
│                                     │
│  No Digital Minds in this category  │
│                                     │
│  Check back soon for new experts    │
│                                     │
└─────────────────────────────────────┘
```

**Loading State:**
```
┌─────────────────────────────────────┐
│  [Skeleton Card]                    │
│  [Skeleton Card]                    │
│  [Skeleton Card]                    │
└─────────────────────────────────────┘
```

- Show 6-12 skeleton cards
- Pulse animation
- Same layout as real cards

---

## Filtering Logic

### Client-Side Filtering (Preferred for <100 items)
```javascript
// Pseudo-code
const filteredMinds = allMinds.filter(mind => {
  const matchesCategory = selectedCategory === 'all' || mind.category === selectedCategory
  const matchesSearch = searchQuery === '' ||
    mind.name.toLowerCase().includes(searchQuery.toLowerCase()) ||
    mind.bio.toLowerCase().includes(searchQuery.toLowerCase()) ||
    mind.tags.some(tag => tag.toLowerCase().includes(searchQuery.toLowerCase()))

  return matchesCategory && matchesSearch
})
```

### Server-Side Filtering (For 100+ items)
- API endpoint: `/api/minds?category=X&search=Y&page=Z`
- Return paginated results
- Include total count
- Cache results where appropriate

---

## URL Structure & Deep Linking

**Base URL:** `/explore`

**With Category:** `/explore?category=marketing`

**With Search:** `/explore?search=finance`

**With Pagination:** `/explore?page=2`

**Combined:** `/explore?category=business&search=startup&page=2`

**Benefits:**
- Shareable links
- Browser back/forward navigation
- SEO-friendly
- Bookmark specific views

**Implementation:**
- Use URL SearchParams API
- Update URL without page reload (History API)
- Initialize filters from URL on page load

---

## Performance Optimization

### Lazy Loading
- Load cards in viewport first
- Lazy load images (Intersection Observer)
- Defer below-fold content

### Image Optimization
- WebP format with fallback
- Responsive images (srcset)
- Placeholder blur or solid color
- Compress to 80% quality
- Serve from CDN

### Data Loading
- Initial load: First 12 cards
- Subsequent loads: 12 cards per batch
- Cache API responses (consider SWR pattern)
- Prefetch next page on scroll proximity

### Animation Performance
- Use transform and opacity (GPU accelerated)
- Avoid animating width, height, margin
- RequestAnimationFrame for smooth animations
- Reduce motion for users with prefers-reduced-motion

---

## Accessibility Requirements

### Keyboard Navigation
- Tab through filters
- Arrow keys to navigate between filters (optional)
- Enter/Space to activate filter
- Tab to cards
- Enter to open card
- Focus indicators visible

### Screen Readers
- Announce filter changes: "Showing 12 Digital Minds in Marketing"
- Announce loading: "Loading more Digital Minds" (aria-live)
- Card structure: Heading (name), text (title, bio), link (Try Demo)
- Search input: Label "Search Digital Minds"

### ARIA Labels
- Filters: `role="tablist"` or `role="radiogroup"`
- Individual filter: `role="tab"` or `role="radio"`, `aria-selected`
- Grid: `role="list"` or semantic `<ul>`
- Cards: `role="listitem"` or semantic `<li>`
- Search: `aria-label="Search Digital Minds"`
- Load More: `aria-label="Load more Digital Minds"`

### Focus Management
- After filter change: Announce results, optionally move focus to results
- After load more: Move focus to first new card
- Skip link: "Skip to results"

### Color Contrast
- All text passes WCAG AA (4.5:1 minimum)
- Active filter clearly visible
- Links have 3:1 contrast against background

---

## SEO Optimization

### Meta Tags
- **Title:** "Explore Digital Minds | Delphi"
- **Description:** "Get personalized advice from world-class experts in business, health, marketing, technology, and more. Discover your perfect AI mentor."
- **Canonical:** `https://www.delphi.ai/explore`

### Structured Data (Schema.org)
```json
{
  "@context": "https://schema.org",
  "@type": "CollectionPage",
  "name": "Digital Minds Catalog",
  "description": "Explore AI digital minds from experts",
  "provider": {
    "@type": "Organization",
    "name": "Delphi"
  }
}
```

### Individual Card Schema
```json
{
  "@type": "Person",
  "name": "Expert Name",
  "jobTitle": "Expertise Area",
  "description": "Bio text",
  "url": "https://www.delphi.ai/expert-name"
}
```

### Indexing
- Allow indexing of main page
- Consider noindex for filtered/paginated views (or canonical to main)
- Sitemap: Include `/explore` and individual profile pages

---

## Responsive Breakpoints

```css
/* Mobile: 320px - 767px */
.grid {
  grid-template-columns: 1fr;
  gap: 20px;
}

/* Tablet: 768px - 1023px */
@media (min-width: 768px) {
  .grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 24px;
  }
}

/* Desktop Small: 1024px - 1279px */
@media (min-width: 1024px) {
  .grid {
    grid-template-columns: repeat(3, 1fr);
    gap: 28px;
  }
}

/* Desktop Large: 1280px+ */
@media (min-width: 1280px) {
  .grid {
    grid-template-columns: repeat(4, 1fr);
    gap: 32px;
  }
}
```

---

## Design Tokens

### Colors (Same as Homepage)
```
Primary Brand: #6366F1
Primary Hover: #4F46E5
Primary Text: #0A0A0A
Secondary Text: #6B7280
Background: #FFFFFF
Background Secondary: #F9FAFB
Border: #E5E7EB
```

### Spacing
```
Card Padding Mobile: 24px 16px
Card Padding Desktop: 28px 20px
Grid Gap Mobile: 20px
Grid Gap Desktop: 28px
Section Padding Mobile: 20px
Section Padding Desktop: 40px
```

---

## Testing Checklist

### Functional Testing
- [ ] Search filters results correctly
- [ ] Category filters work
- [ ] Filters can be combined (search + category)
- [ ] Load More loads correct cards
- [ ] URL updates with filters
- [ ] Back button restores previous state
- [ ] Empty states show correctly
- [ ] Card links navigate to correct profiles

### Responsive Testing
- [ ] Grid adapts to screen size (1/2/3/4 columns)
- [ ] Filter pills scroll horizontally on mobile
- [ ] Cards maintain aspect ratio on all sizes
- [ ] Images load without distortion
- [ ] Search input full width on mobile

### Performance Testing
- [ ] Initial page load < 2s
- [ ] Images lazy load
- [ ] Infinite scroll smooth without jank
- [ ] Filtering/search feels instant (< 100ms perceived)
- [ ] No layout shift during image load

### Accessibility Testing
- [ ] Keyboard navigation works
- [ ] Screen reader announces filter changes
- [ ] Focus indicators visible
- [ ] Color contrast passes
- [ ] ARIA labels present

---

## Developer Notes

### Recommended Libraries
- **Search:** Fuse.js (fuzzy search)
- **Infinite Scroll:** react-infinite-scroll-component
- **Lazy Loading:** react-lazy-load-image-component
- **URL State:** next/router or react-router

### Data Structure
```typescript
interface DigitalMind {
  id: string
  name: string
  slug: string
  title: string // e.g., "Marketing Expert"
  bio: string // 2-3 sentences
  category: 'marketing' | 'tech' | 'health' | 'business' | 'life'
  tags: string[] // e.g., ["SEO", "Content Marketing"]
  avatar: string // URL to image
  featured: boolean // Spotlight
  profileUrl: string // e.g., "/expert-name"
}
```

### API Endpoints
```
GET /api/minds
GET /api/minds?category=marketing
GET /api/minds?search=finance
GET /api/minds?page=2&limit=12
```

---

**End of Explore/Catalog Page Template Specification**
