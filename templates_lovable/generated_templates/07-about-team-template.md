# About/Team Page Template - Technical Specification

**Page Type:** Company/About Page
**URL Pattern:** `/about`, `/team`, `/careers`
**Priority:** Medium
**Approach:** Mobile First
**Last Updated:** November 12, 2025

---

## Page Overview

**Purpose:** Communicate company mission, showcase team, and build trust with potential customers and candidates.

---

## About Page Structure (`/about`)

### Block 01: Header Navigation
*(Same as Homepage)*

---

### Block 02: Hero Section
```
┌─────────────────────────────────────┐
│                                     │
│  [H1: Our Mission]                  │
│                                     │
│  [Mission statement - 2-3 sentences]│
│                                     │
└─────────────────────────────────────┘
```

**H1:** "Our Mission" or "About Delphi"
- Mobile: 32px / 38px, Desktop: 48px / 56px
- Weight: 700, Center aligned

**Mission Statement:**
- Font size: 18px / 28px (mobile), 22px / 34px (desktop)
- Color: Secondary text
- Max-width: 800px
- Center aligned

**Spacing:** 60px 20px (mobile), 100px 40px (desktop)

---

### Block 03: Story Section
```
┌─────────────────────────────────────┐
│  ┌────────────┐  [H2: Our Story]    │
│  │            │                     │
│  │  Image or  │  [Paragraph text    │
│  │  Video     │   describing the    │
│  │            │   company journey]  │
│  └────────────┘                     │
└─────────────────────────────────────┘
```

**Mobile:** Stack (image top, text below)
**Desktop:** Side-by-side (50/50 or 40/60)

**Image/Video:**
- Border-radius: 12px
- Aspect ratio: 4:3 or 16:9
- Alt text descriptive

**Text:**
- Font size: 16px / 26px
- Color: Primary text
- Max-width: 600px

**Container:**
- Max-width: 1100px
- Padding: 60px 20px (mobile), 80px 40px (desktop)

---

### Block 04: Values Section
```
┌─────────────────────────────────────┐
│  [H2: Our Values]                   │
│                                     │
│  ┌──────────┬──────────┬──────────┐ │
│  │ [Icon]   │ [Icon]   │ [Icon]   │ │
│  │ [Title]  │ [Title]  │ [Title]  │ │
│  │ [Text]   │ [Text]   │ [Text]   │ │
│  └──────────┴──────────┴──────────┘ │
└─────────────────────────────────────┘
```

**Values (Example):**
1. **User-First**
   - Icon: User icon
   - Text: "We build for experts who want to scale..."

2. **Innovation**
   - Icon: Lightbulb
   - Text: "We push boundaries of AI technology..."

3. **Integrity**
   - Icon: Shield
   - Text: "We handle your data with utmost care..."

**Grid:**
- Mobile: 1 column
- Tablet: 2 columns
- Desktop: 3 columns
- Gap: 32px

**Card Styling:**
- Text align: Center
- Padding: 24px
- Icon: 64px, color primary
- Title: 20px, weight 600
- Text: 15px / 22px, color secondary

---

### Block 05: Investors/Backers Section
```
┌─────────────────────────────────────┐
│  [H2: Backed By The Best]           │
│                                     │
│  [Logo] [Logo] [Logo] [Logo]        │
│                                     │
│  [Quote from investor]              │
│  - [Investor Name, Firm]            │
│                                     │
└─────────────────────────────────────┘
```

**Investor Logos:**
- Greyscale
- Size: 120px × 60px
- Opacity: 0.7, hover 1.0
- Gap: 40px
- Center aligned

**Quote:**
- Font size: 20px / 30px
- Font style: Italic
- Max-width: 700px
- Center aligned
- Color: Secondary text

**Spacing:** 80px 20px (mobile), 100px 40px (desktop)

---

### Block 06: Press/Featured In
```
┌─────────────────────────────────────┐
│  [H3: As Featured In]               │
│                                     │
│  [Logo] [Logo] [Logo] [Logo] [Logo] │
│                                     │
└─────────────────────────────────────┘
```

**Publication Logos:**
- Greyscale
- Size: 100px × 40px
- Gap: 32px
- Horizontal scroll mobile, centered desktop

---

### Block 07: CTA Section
```
┌─────────────────────────────────────┐
│  [H3: Join Our Mission]             │
│  [Subtitle text]                    │
│  [View Open Roles Button]           │
└─────────────────────────────────────┘
```

**Background:** Gradient or accent color
**Padding:** 60px 20px
**Link:** `/careers`

---

## Team Page Structure (`/team`)

### Block 01: Header
*(Same)*

---

### Block 02: Hero
```
┌─────────────────────────────────────┐
│  [H1: Meet The Team]                │
│  [Subtitle text]                    │
└─────────────────────────────────────┘
```

---

### Block 03: Team Members Grid
```
┌─────────────────────────────────────┐
│  [H2: Leadership]                   │
│                                     │
│  ┌────────┬────────┬────────┐       │
│  │ [Card] │ [Card] │ [Card] │       │
│  └────────┴────────┴────────┘       │
│                                     │
│  [H2: Team]                         │
│                                     │
│  ┌────────┬────────┬────────┬────┐  │
│  │ [Card] │ [Card] │ [Card] │... │  │
│  └────────┴────────┴────────┴────┘  │
└─────────────────────────────────────┘
```

**Team Card:**
```
┌──────────────────────┐
│                      │
│  [Profile Photo]     │
│                      │
│  [Name]              │
│  [Job Title]         │
│                      │
│  [LinkedIn Icon]     │
│                      │
└──────────────────────┘
```

**Photo:**
- Size: 200px × 200px
- Border-radius: 50% (circle)
- Grayscale: Optional
- Hover: Color (if greyscale)

**Name:**
- Font size: 18px
- Font weight: 600
- Margin: 12px 0 4px

**Job Title:**
- Font size: 14px
- Color: Primary color
- Margin-bottom: 12px

**LinkedIn:**
- Icon: 24px
- Color: #0A66C2 (LinkedIn blue)
- Hover: Opacity 0.8

**Grid:**
- Mobile: 1 column
- Tablet: 2 columns
- Desktop: 3-4 columns
- Gap: 32px

**Card Styling:**
- Background: White
- Padding: 20px
- Border: 1px solid #E5E7EB
- Border-radius: 12px
- Text align: Center
- Hover: Shadow, lift

---

### Block 04: Join Team CTA
```
┌─────────────────────────────────────┐
│  We're Hiring!                      │
│  [View Open Positions Button]       │
└─────────────────────────────────────┘
```

---

## Careers Page Structure (`/careers`)

### Block 01: Header
*(Same)*

---

### Block 02: Hero
```
┌─────────────────────────────────────┐
│  [H1: Careers at Delphi]            │
│  [Subtitle: Join us in building...] │
└─────────────────────────────────────┘
```

---

### Block 03: Why Join Section
```
┌─────────────────────────────────────┐
│  [H2: Why Delphi?]                  │
│                                     │
│  [Benefit Card] [Benefit Card]      │
│  [Benefit Card] [Benefit Card]      │
└─────────────────────────────────────┘
```

**Benefits:**
- 💼 Competitive salary + equity
- 🏥 Health, dental, vision insurance
- 🌴 Unlimited PTO
- 🏠 Remote-first culture
- 📈 Growth opportunities
- 🧠 Learning stipend

**Grid:** 2 columns mobile, 3-4 desktop

---

### Block 04: Open Positions
```
┌─────────────────────────────────────┐
│  [H2: Open Positions]               │
│                                     │
│  ┌───────────────────────────────┐  │
│  │ Senior Backend Engineer       │  │
│  │ Engineering · Remote · Full-time│  │
│  │ [Apply →]                     │  │
│  └───────────────────────────────┘  │
│  [Gap]                              │
│  ┌───────────────────────────────┐  │
│  │ Product Designer              │  │
│  │ Design · SF/Remote · Full-time│  │
│  │ [Apply →]                     │  │
│  └───────────────────────────────┘  │
└─────────────────────────────────────┘
```

**Job Card:**
- Background: White
- Border: 1px solid #E5E7EB
- Border-radius: 12px
- Padding: 24px
- Hover: Shadow, border color primary

**Job Title:**
- Font size: 20px
- Font weight: 600

**Meta:**
- Font size: 14px
- Color: Secondary text
- Separated by " · "

**Apply Button:**
- Text: "Apply →"
- Color: Primary
- Font weight: 600
- Hover: Underline

**Link:** Opens Lever, Greenhouse, or application form

**Empty State (No positions):**
```
┌─────────────────────────────────────┐
│  No open positions at the moment.   │
│  Check back soon or send us your    │
│  resume at careers@delphi.ai        │
└─────────────────────────────────────┘
```

---

### Block 05: Talk to CEO's Digital Mind
```
┌─────────────────────────────────────┐
│  [H3: Want to Learn More?]          │
│  Talk to our CEO's Digital Mind     │
│  [Start Conversation Button]        │
└─────────────────────────────────────┘
```

**Unique Feature:** Showcase product by letting candidates talk to CEO's AI

**Background:** Accent color
**Padding:** 60px 20px

---

### Block 06: Footer
*(Same)*

---

## Interactive Elements

### 1. Team Card Hover (Desktop)
- Lift: translateY(-4px)
- Shadow increase
- Photo: Color if greyscale
- Smooth transition

### 2. Filter Jobs (If many positions)
- Department: Engineering, Design, Marketing, etc.
- Location: Remote, SF, NYC, etc.
- Type: Full-time, Part-time, Contract

### 3. Application Flow
- Click "Apply" → Modal or new page
- Form fields:
  - Full Name
  - Email
  - LinkedIn/Portfolio
  - Resume upload
  - Cover letter (optional)
  - Checkbox: "I accept privacy policy"
  - Submit button

---

## SEO

**About:**
- Title: "About Delphi | Our Mission to Scale Expertise with AI"
- Description: "Learn about Delphi's mission to help experts scale their impact..."

**Team:**
- Title: "Team | Delphi"
- Description: "Meet the team building the future of AI digital clones."

**Careers:**
- Title: "Careers at Delphi | Join Us in Building the Future"
- Description: "Explore open positions at Delphi. Remote-first culture, competitive compensation..."

---

**End of About/Team Page Template**
