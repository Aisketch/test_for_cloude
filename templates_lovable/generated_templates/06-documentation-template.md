# Documentation Page Template - Technical Specification

**Page Type:** Documentation/Help Center Page
**URL Pattern:** `docs.delphi.ai/*`
**Priority:** High
**Approach:** Mobile First
**Last Updated:** November 12, 2025

---

## Page Overview

**Purpose:** Provide comprehensive documentation, guides, and help content with easy navigation and search.

---

## Page Structure

### Block 01: Header
```
┌─────────────────────────────────────┐
│ [Delphi Docs Logo] [Search] [Sign In] │
└─────────────────────────────────────┘
```

**Logo:** "Delphi Docs" or "Delphi Help Center"
**Search:** Prominent search bar (300px desktop)
**Sign In:** Link to main app

**Sticky:** Yes, height 64px

---

### Block 02: Layout Structure

#### Mobile (Drawer Navigation)
```
┌─────────────────────────────────────┐
│ [☰ Menu] [Page Title]    [Search 🔍]│
├─────────────────────────────────────┤
│                                     │
│  [Article Content]                  │
│                                     │
│  [Table of Contents]                │
│                                     │
└─────────────────────────────────────┘
```

**Hamburger:** Opens full-screen navigation drawer
**Content:** Full width
**TOC:** Below content (collapsible)

#### Desktop (3-Column Layout)
```
┌───────────────────────────────────────────────┐
│ [Header]                                      │
├──────────┬─────────────────────┬──────────────┤
│          │                     │              │
│ [Sidebar]│  [Main Content]     │ [TOC Sidebar]│
│          │                     │              │
│  Nav     │   Article           │  On This     │
│  Tree    │   Content           │  Page        │
│          │                     │              │
│          │                     │              │
└──────────┴─────────────────────┴──────────────┘
```

**Left Sidebar:** 280px, navigation tree
**Main Content:** Flexible width (max 800px)
**Right Sidebar:** 240px, table of contents
**Both sidebars sticky**

---

### Block 03: Left Sidebar Navigation

```
┌──────────────────────────┐
│  [Search Docs Input]     │
│                          │
│  ▼ Getting Started       │
│    • Quickstart          │
│    • Studio Navigation   │
│    • FAQs                │
│                          │
│  ▼ Build Your Delphi     │
│    • Mind Settings       │
│    • Content             │
│    • Voice               │
│                          │
│  ▼ Launch                │
│    • Access Groups       │
│    • Integrations        │
│                          │
│  ▼ Operate               │
│    • Broadcasts          │
│    • Actions             │
│    • Products            │
│                          │
│  ▼ Settings              │
│    • Billing             │
│    • Privacy & Security  │
│                          │
└──────────────────────────┘
```

**Search Input:**
- Placeholder: "Search docs..."
- Height: 40px
- Border-radius: 8px
- Margin-bottom: 16px

**Section Headers:**
- Font size: 13px
- Font weight: 700
- Text transform: Uppercase
- Color: #4B5563
- Margin: 16px 0 8px
- Collapsible with chevron icon

**Nav Links:**
- Font size: 14px
- Color: #6B7280
- Padding: 8px 12px
- Border-radius: 6px
- Hover: Background #F3F4F6
- Active: Background #EEF2FF (light primary), Color #6366F1, Font weight 600

**Nested Items:**
- Indent: 16px per level
- Max depth: 3 levels

**Scrollable:**
- Overflow-y: auto
- Max-height: calc(100vh - 120px)
- Custom scrollbar styling

---

### Block 04: Main Content Area

```
┌─────────────────────────────────────┐
│  [Breadcrumbs]                      │
│  Home > Getting Started > Quickstart│
│                                     │
│  [H1: Page Title]                   │
│                                     │
│  [Last updated: Nov 12, 2025]       │
│                                     │
│  ───────────────────                │
│                                     │
│  [Article Content]                  │
│                                     │
│  ## Section 1                       │
│  Paragraph text...                  │
│                                     │
│  ## Section 2                       │
│  Paragraph text...                  │
│                                     │
│  ───────────────────                │
│                                     │
│  Was this helpful? 👍 👎            │
│                                     │
│  [Previous Page] [Next Page]        │
│                                     │
└─────────────────────────────────────┘
```

**Breadcrumbs:**
- Font size: 14px
- Color: #6B7280
- Separator: " > " or chevron
- Links: Underline on hover
- Margin-bottom: 16px

**H1 Title:**
- Font size Mobile: 28px / 34px
- Font size Desktop: 36px / 44px
- Font weight: 700
- Margin-bottom: 8px

**Last Updated:**
- Font size: 13px
- Color: #9CA3AF
- Margin-bottom: 24px

**Content Styling:**
- **Body Text:** 16px / 26px
- **Paragraphs:** Margin 0 0 20px
- **H2:** 24px / 32px, weight 700, margin 32px 0 12px
- **H3:** 20px / 28px, weight 600, margin 24px 0 10px
- **H4:** 18px / 26px, weight 600, margin 20px 0 8px

**Code Blocks:**
- Background: #1F2937 (dark)
- Color: #F9FAFB (light text)
- Border-radius: 8px
- Padding: 16px
- Font: Roboto Mono, 14px
- Overflow-x: auto
- Copy button: Top right corner

**Inline Code:**
- Background: #F3F4F6
- Color: #DC2626 (red accent)
- Padding: 2px 6px
- Border-radius: 4px
- Font: Roboto Mono, 14px

**Callout Boxes:**
```
┌─────────────────────────────────────┐
│ ℹ️ INFO                              │
│ This is an informational callout.   │
└─────────────────────────────────────┘
```

**Types:**
- **Info:** Blue background, ℹ️ icon
- **Warning:** Yellow background, ⚠️ icon
- **Success:** Green background, ✅ icon
- **Danger:** Red background, ⛔ icon

**Styling:**
- Border-left: 4px solid [color]
- Background: [color] 10% opacity
- Padding: 16px
- Border-radius: 8px
- Margin: 24px 0

**Images:**
- Max-width: 100%
- Border: 1px solid #E5E7EB
- Border-radius: 8px
- Margin: 24px 0
- Box-shadow: Subtle

**Tables:**
- Border: 1px solid #E5E7EB
- Border-radius: 8px
- Overflow: auto (horizontal scroll mobile)
- Header: Background #F9FAFB, font weight 600
- Cells: Padding 12px 16px

**Feedback Section:**
- Margin-top: 48px
- Padding-top: 24px
- Border-top: 1px solid #E5E7EB
- Text: "Was this helpful?"
- Buttons: 👍 👎 (emoji or icons)
- Hover: Scale 1.2
- Click: Show "Thanks for your feedback!"

**Page Navigation:**
- Display: Flex, justify space-between
- Margin-top: 32px
- Previous: "← Previous: {Title}"
- Next: "Next: {Title} →"
- Buttons: Border, padding 12px 20px, border-radius 8px
- Hover: Background primary, color white

---

### Block 05: Right Sidebar (Table of Contents)

```
┌──────────────────────┐
│  On This Page        │
│                      │
│  • Section 1         │
│  • Section 2         │
│    • Subsection 2.1  │
│    • Subsection 2.2  │
│  • Section 3         │
│                      │
└──────────────────────┘
```

**Title:** "On This Page"
- Font size: 13px
- Font weight: 700
- Text transform: Uppercase
- Color: #4B5563
- Margin-bottom: 12px

**Links:**
- Font size: 13px
- Color: #6B7280
- Line-height: 28px
- Hover: Color primary
- Active: Color primary, font weight 600
- Smooth scroll to section

**Nested:**
- Indent: 12px per level
- Max depth: 2 levels (H2, H3)

**Sticky:**
- Position: sticky
- Top: 80px
- Max-height: calc(100vh - 100px)
- Overflow-y: auto

**Auto-Highlight:**
- As user scrolls, highlight current section
- Intersection Observer API

---

### Block 06: Footer (Docs)

```
┌─────────────────────────────────────┐
│  Need Help?                         │
│  [Join Community] [Contact Support] │
│                                     │
│  © 2025 Delphi · Privacy · Terms    │
│                                     │
└─────────────────────────────────────┘
```

**Minimal footer**
- Background: #F9FAFB
- Padding: 40px 20px
- Text align: Center

---

## Interactive Elements

### 1. Search Functionality
- **Trigger:** Click search or Cmd/Ctrl+K
- **Overlay:** Full-screen modal (mobile), dropdown (desktop)
- **Features:**
  - Instant search as you type
  - Fuzzy matching
  - Highlight matches
  - Keyboard navigation (arrows, enter)
  - Show breadcrumb path
  - Recent searches
  - Popular articles

**Search Result Item:**
```
┌─────────────────────────────────────┐
│  [Article Title]                    │
│  [Breadcrumb path]                  │
│  [Matching text snippet...]         │
└─────────────────────────────────────┘
```

### 2. Code Block Features
- **Copy Button:** Top right, click to copy
- **Line Numbers:** Optional
- **Syntax Highlighting:** Language-specific
- **Wrap Toggle:** Long lines

### 3. Expand/Collapse Navigation
- Click section header to expand/collapse
- Remember state (localStorage)
- Animate: Max-height transition

### 4. Dark Mode Toggle (Optional)
- Icon in header
- Toggle light/dark theme
- Save preference (localStorage)
- Smooth transition

---

## Mobile Considerations

### Navigation Drawer
- Full-screen overlay
- Slide from left
- Dark overlay background
- Close: X button, swipe left, click overlay
- Lock body scroll when open

### Table Overflow
- Horizontal scroll
- Shadow indicators on sides
- Touch-friendly scroll

### Code Blocks
- Horizontal scroll
- Pinch to zoom (optional)

---

## Search Implementation

**Search Index:**
- Index all page titles, headings, content
- Weight: Title > H2 > H3 > Body
- Use Algolia, Typesense, or custom solution

**Search API:**
```
GET /api/docs/search?q=query
Response:
{
  "results": [
    {
      "title": "Page Title",
      "url": "/path",
      "breadcrumb": ["Section", "Subsection"],
      "snippet": "...matching text..."
    }
  ]
}
```

---

## Accessibility

- **Skip Links:** Skip to content, skip to navigation
- **ARIA Landmarks:** `<nav>`, `<main>`, `<aside>`
- **Heading Hierarchy:** Proper H1-H6 structure
- **Keyboard Navigation:**
  - Tab through links
  - Enter to activate
  - Escape to close modals
- **Screen Reader:** Announce expanded/collapsed state
- **Focus Indicators:** Visible on all interactive elements

---

## SEO

**Title Pattern:** "{Page Title} | Delphi Documentation"
**Description:** First paragraph or custom excerpt
**Canonical:** `https://docs.delphi.ai/{path}`

**Structured Data:**
```json
{
  "@type": "TechArticle",
  "headline": "Page Title",
  "articleBody": "...",
  "datePublished": "...",
  "publisher": {...}
}
```

**Sitemap:** Include all doc pages
**Robots:** Allow indexing
**Breadcrumbs Schema:** BreadcrumbList

---

**End of Documentation Page Template**
