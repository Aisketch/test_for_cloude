# Homepage Template - Technical Specification

**Page Type:** Landing Page
**URL Pattern:** `/` (homepage)
**Priority:** Critical
**Approach:** Mobile First
**Last Updated:** November 12, 2025

---

## Page Overview

**Purpose:** Primary landing page to introduce Delphi.AI platform, showcase value proposition, and drive conversions (sign-ups).

**Key Goals:**
- Communicate core value proposition within 3 seconds
- Drive user to sign up or explore Digital Minds
- Build trust through social proof and testimonials
- Educate users about key features

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
  - Link: `/`
  - Alt text: "Delphi - AI Digital Clone Platform"

- **Hamburger Menu** (Right aligned)
  - Icon: 24px × 24px
  - Color: Primary text color
  - Opens mobile navigation drawer

**Mobile Navigation Drawer:**
```
┌─────────────────────────────────────┐
│ [× Close]                           │
│                                     │
│ Explore                             │
│ Pricing                             │
│ About                               │
│ Docs                                │
│ ─────────────────                   │
│ Sign In                             │
│ [Get Started - CTA Button]          │
└─────────────────────────────────────┘
```

#### Desktop Layout (1024px+)
```
┌─────────────────────────────────────────────────────────────┐
│ [Logo]    Explore  Pricing  About  Docs    Sign In  [Get Started] │
└─────────────────────────────────────────────────────────────┘
```

**Navigation Items:**
- Explore → `/explore`
- Pricing → `/pricing`
- About → `/about`
- Docs → `https://docs.delphi.ai/`
- Sign In → `/signin` (Text link)
- Get Started → `/signup` (Primary CTA button)

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
│      [Subheadline text]             │
│                                     │
│   [Primary CTA Button]              │
│   [Secondary CTA Button]            │
│                                     │
│     [Hero Image/Video]              │
│                                     │
│  "Trusted by 10,000+ experts"       │
│   [Logo] [Logo] [Logo] [Logo]       │
│                                     │
└─────────────────────────────────────┘
```

**Content:**

**H1 Headline:**
- Text: "Scale Your Insight. Stay Focused on What Matters."
- Font size Mobile: 32px / 36px line-height
- Font size Desktop: 56px / 64px line-height
- Font weight: 700
- Color: Primary text (#0A0A0A or similar)
- Max-width: 600px mobile, 800px desktop
- Text align: Center

**Subheadline:**
- Text: "Create your AI digital clone. Scale your expertise 24/7 with personalized AI minds that think, speak, and engage like you."
- Font size Mobile: 16px / 24px line-height
- Font size Desktop: 20px / 30px line-height
- Font weight: 400
- Color: Secondary text (#666666)
- Max-width: 500px mobile, 640px desktop
- Margin-top: 16px mobile, 24px desktop

**Primary CTA:**
- Text: "Get Started Free"
- URL: `/signup`
- Size Mobile: Full width (with 20px margin), Height 56px
- Size Desktop: Auto width (padding 24px 48px), Height 56px
- Font size: 16px
- Font weight: 600
- Background: Primary color (e.g., #6366F1)
- Color: White
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
- Color: Primary color
- Border: 2px solid primary color
- Border-radius: 8px
- Margin-top: 12px

**Hero Visual:**
- Type: Image or Looping video
- Mobile: Full width, 300px height
- Desktop: 600px width, 450px height
- Alt text: "Delphi AI digital clone interface demonstration"
- Margin-top: 40px
- Border-radius: 12px
- Optional: Subtle shadow

**Social Proof:**
- Text: "Trusted by 10,000+ experts"
- Font size: 14px
- Color: Secondary text
- Margin-top: 32px

**Logo Strip:**
- Display: Horizontal scroll on mobile, centered on desktop
- Logos: Greyscale, 80px × 40px each
- Gap: 24px mobile, 40px desktop
- Opacity: 0.6, hover 1.0 (desktop)

#### Desktop Layout
```
┌───────────────────────────────────────────────────────────┐
│                                                           │
│   ┌─────────────────────┐     ┌──────────────────────┐  │
│   │                     │     │                      │  │
│   │   [H1 Headline]     │     │    [Hero Visual]     │  │
│   │                     │     │                      │  │
│   │ [Subheadline text]  │     │    Image/Video       │  │
│   │                     │     │                      │  │
│   │ [CTA Buttons Row]   │     │                      │  │
│   │                     │     │                      │  │
│   │ [Social Proof]      │     └──────────────────────┘  │
│   └─────────────────────┘                               │
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

### Block 03: Features Overview
**Mobile:** Stack vertically
**Desktop:** 3 column grid

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
- Eyebrow: "Why Delphi"
- Font size: 14px, uppercase, letter-spacing: 1.5px
- Color: Primary brand color
- Font weight: 600

- H2: "Your AI Clone. Your Way."
- Font size Mobile: 28px / 34px line-height
- Font size Desktop: 40px / 48px line-height
- Font weight: 700

- Description: "Build a personalized AI digital mind that captures your knowledge, personality, and communication style."
- Font size: 16px / 24px line-height
- Color: Secondary text
- Max-width: 640px
- Margin: 0 auto

**Spacing:**
- Padding Mobile: 60px 20px
- Padding Desktop: 100px 40px

#### Feature Cards

**Mobile Layout (Stacked):**
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

**Feature 1:**
- Icon: Upload/Content icon
- Title: "Upload Your Knowledge"
- Description: "Add writing, videos, podcasts, or link live feeds. Delphi indexes everything and mirrors your tone, style, and expertise."

**Feature 2:**
- Icon: Voice/Audio icon
- Title: "Your Voice, Cloned"
- Description: "Professional voice cloning with emotional intelligence. Your AI sounds exactly like you across text, voice, and video."

**Feature 3:**
- Icon: Scale/Network icon
- Title: "Scale Your Reach"
- Description: "Deploy on your website, via SMS, or any chat platform. Engage with thousands while you focus on what matters."

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
- Color: Primary brand color

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
│   [Subheadline description]         │
│                                     │
└─────────────────────────────────────┘
```

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

**Step 1: Build Your Mind**
- Badge: "01"
- Title: "Build Your Mind"
- Description: "Upload your content or take the Delphi Interview. Our AI learns your knowledge, tone, and personality in minutes."
- Image: Screenshot of content upload interface
- Image size Mobile: Full width, aspect ratio 16:9
- Image size Desktop: 500px width

**Step 2: Customize Your Clone**
- Badge: "02"
- Title: "Customize Your Clone"
- Description: "Fine-tune voice settings, personality traits, and response style. Make it truly yours with advanced mind settings."
- Image: Screenshot of customization dashboard

**Step 3: Launch and Scale**
- Badge: "03"
- Title: "Launch and Scale"
- Description: "Deploy your AI across platforms. Engage with your audience 24/7 while you focus on high-value work."
- Image: Screenshot of deployment options

**Step Badge:**
- Size: 48px × 48px
- Background: Primary color with 10% opacity
- Border: 2px solid primary color
- Font size: 20px
- Font weight: 700
- Border-radius: 50%
- Color: Primary color

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

### Block 05: Featured Digital Minds Carousel
**Purpose:** Showcase popular AI clones

#### Section Header
```
┌─────────────────────────────────────┐
│                                     │
│  [H2: "Explore Digital Minds"]      │
│  [Subheadline]                      │
│                                     │
└─────────────────────────────────────┘
```

**Content:**
- H2: "Explore Digital Minds"
- Subheadline: "Get personalized advice from world-class experts in business, health, marketing, and more."

**Carousel Layout:**

**Mobile:**
```
┌─────────────────────────────────────┐
│  ← [Card Card Card] →               │
│                                     │
│      ● ○ ○ ○ (dots)                 │
└─────────────────────────────────────┘
```

**Card Structure:**
```
┌──────────────────────┐
│                      │
│   [Profile Image]    │
│                      │
│   [Name]             │
│   [Title/Expertise]  │
│                      │
│   [Short Bio]        │
│                      │
│   [Try Demo →]       │
│                      │
└──────────────────────┘
```

**Featured Profiles:**
1. **Lenny Rachitsky**
   - Title: "Product & Growth Expert"
   - Bio: "Building and growing products"
   - Image: Professional headshot
   - Link: `/lenny` (example)

2. **Dr. Mark Hyman**
   - Title: "Functional Medicine Pioneer"
   - Bio: "Your health, unlocked"

3. **Arnold Schwarzenegger**
   - Title: "Fitness & Motivation Icon"
   - Bio: "Get pumped"

4. **Ramit Sethi**
   - Title: "Personal Finance Expert"
   - Bio: "Own your financial freedom"

5. **Vanessa Van Edwards**
   - Title: "Communication Expert"
   - Bio: "Communicate with confidence"

**Card Styling:**
- Size Mobile: 280px width
- Size Desktop: 320px width
- Background: White
- Border: 1px solid #E5E7EB
- Border-radius: 16px
- Padding: 24px
- Shadow: 0 4px 6px rgba(0,0,0,0.1)
- Hover: Lift effect + increased shadow (desktop)

**Profile Image:**
- Size: 120px × 120px
- Border-radius: 50%
- Border: 3px solid #F3F4F6
- Margin: 0 auto 16px

**Name:**
- Font size: 20px
- Font weight: 600
- Text align: Center

**Title:**
- Font size: 14px
- Color: Primary brand color
- Text align: Center
- Margin-top: 4px

**Bio:**
- Font size: 15px / 22px line-height
- Color: Secondary text
- Text align: Center
- Margin-top: 12px
- Min-height: 66px (3 lines)

**CTA Link:**
- Text: "Try Demo →"
- Font size: 14px
- Font weight: 600
- Color: Primary color
- Margin-top: 16px
- Text align: Center
- Hover: Underline

**Carousel Behavior:**
- Mobile: Horizontal scroll, snap to card
- Tablet: Show 2 cards
- Desktop: Show 3-4 cards, arrows on sides
- Gap: 20px between cards

**Navigation:**
- Mobile: Swipe + pagination dots
- Desktop: Prev/Next arrows + dots
- Arrow size: 40px × 40px
- Arrow position: Outside container on sides

**CTA Below Carousel:**
```
┌─────────────────────────────────────┐
│   [View All Digital Minds Button]   │
└─────────────────────────────────────┘
```
- Text: "View All Digital Minds"
- Style: Secondary button (outlined)
- Link: `/explore`
- Margin-top: 40px

---

### Block 06: Social Proof / Testimonials
**Purpose:** Build trust with user testimonials

#### Section Header
```
┌─────────────────────────────────────┐
│                                     │
│  [H2: "Loved by Experts"]           │
│  [Subheadline]                      │
│                                     │
└─────────────────────────────────────┘
```

**Content:**
- H2: "Loved by Experts Worldwide"
- Subheadline: "See how creators, coaches, and business leaders use Delphi to scale their impact."

**Testimonial Grid:**

**Mobile: Stack 1 column**
**Desktop: 2-3 columns**

```
┌──────────────────────────────┐
│  ★★★★★                       │
│                              │
│  [Testimonial quote text]    │
│                              │
│  [Avatar]  [Name]            │
│            [Title/Company]   │
│                              │
└──────────────────────────────┘
```

**Testimonial 1:**
- Quote: "Delphi helped me answer 600+ client questions without picking up my phone. I reclaimed 35+ hours every month."
- Name: "Jaden Bales"
- Title: "Marketing Consultant"
- Avatar: 48px × 48px

**Testimonial 2:**
- Quote: "The voice cloning is incredible. It actually sounds like me and captures my personality. My audience can't tell the difference."
- Name: "George B. Thomas"
- Title: "Content Creator"

**Testimonial 3:**
- Quote: "From upload to launch took less than an hour. Now my AI handles repetitive questions while I focus on strategy."
- Name: "Sarah Chen"
- Title: "Business Coach"

**Testimonial 4:**
- Quote: "Delphi has been a game-changer for scaling my consulting practice. It's like having 10 of me working simultaneously."
- Name: "Michael Rodriguez"
- Title: "Startup Advisor"

**Card Styling:**
- Background: White
- Padding: 32px 24px
- Border: 1px solid #E5E7EB
- Border-radius: 12px
- Shadow: Subtle on hover (desktop)

**Rating Stars:**
- Size: 16px each
- Color: #FBBF24 (yellow/gold)
- Margin-bottom: 16px

**Quote:**
- Font size: 16px / 24px line-height
- Color: Primary text
- Font style: Normal (not italic)
- Margin-bottom: 20px

**Author Section:**
- Display: Flex, align center
- Gap: 12px

**Avatar:**
- Size: 48px × 48px
- Border-radius: 50%

**Name:**
- Font size: 15px
- Font weight: 600

**Title:**
- Font size: 14px
- Color: Secondary text
- Margin-top: 2px

**Grid:**
- Mobile: 1 column, gap 24px
- Tablet: 2 columns, gap 24px
- Desktop: 3 columns (or 2 columns with larger cards), gap 32px

---

### Block 07: Use Cases Section
**Purpose:** Show different user types and benefits

```
┌─────────────────────────────────────┐
│  [H2: "Built for Every Expert"]     │
└─────────────────────────────────────┘
```

**Tab Navigation (Mobile: Dropdown, Desktop: Tabs):**

**Mobile:**
```
┌─────────────────────────────────────┐
│  [Coaches & Consultants  ▼]         │
└─────────────────────────────────────┘
```

**Desktop:**
```
┌───────────────────────────────────────────────┐
│ [Coaches] [Creators] [Business] [Thought Leaders] │
└───────────────────────────────────────────────┘
```

**Categories:**
1. Coaches & Consultants
2. Creators & Influencers
3. Business Owners
4. Thought Leaders
5. Newsletter Writers

**Use Case Card:**
```
┌───────────────────────────────────────┐
│                                       │
│  ┌──────────┐   [Title]              │
│  │  Icon    │   [Description]         │
│  └──────────┘                         │
│                                       │
│  ✓ Benefit 1                          │
│  ✓ Benefit 2                          │
│  ✓ Benefit 3                          │
│                                       │
│  [Get Started Button]                 │
│                                       │
└───────────────────────────────────────┘
```

**Example: Coaches & Consultants**
- Icon: Person with chat bubbles
- Title: "Scale Your Coaching Practice"
- Description: "Provide 24/7 personalized guidance to your clients without burning out. Let your AI clone handle routine questions while you focus on high-value sessions."
- Benefits:
  - "Answer client questions instantly, 24/7"
  - "Maintain consistent communication style"
  - "Free up 30+ hours per month"
- CTA: "Start Free Trial"

**Styling:**
- Background: Gradient or image background
- Padding Mobile: 40px 20px
- Padding Desktop: 60px 40px
- Border-radius: 16px
- Content max-width: 500px

---

### Block 08: Pricing Teaser
**Purpose:** Show pricing preview and drive to pricing page

```
┌─────────────────────────────────────┐
│                                     │
│  [H2: "Simple, Transparent Pricing"] │
│  [Subheadline]                      │
│                                     │
│  ┌─────────┬─────────┬─────────┐   │
│  │  Free   │ Builder │ Scaler  │   │
│  │         │         │         │   │
│  │  $0/mo  │ $99/mo  │ $399/mo │   │
│  │         │         │         │   │
│  │ [Start] │ [Start] │ [Start] │   │
│  └─────────┴─────────┴─────────┘   │
│                                     │
│  [View Full Pricing Details →]      │
│                                     │
└─────────────────────────────────────┘
```

**Mobile:** Stack cards vertically
**Desktop:** 3 column grid

**Card Structure:**
- Plan name
- Price
- 3-4 key features
- CTA button

**Featured Plan:** Builder (highlighted with border/shadow)

**Link to full pricing:**
- Text: "View Full Pricing Details →"
- Link: `/pricing`
- Font size: 16px
- Font weight: 600
- Color: Primary color
- Margin-top: 32px
- Text align: Center

---

### Block 08.7: FAQ Section
**Purpose:** Address objections, improve SEO, reduce support load
**Mobile Height:** Auto
**Desktop Height:** Auto

#### Section Header
```
┌─────────────────────────────────────┐
│                                     │
│  [H2: "Frequently Asked Questions"] │
│                                     │
│  [Search: "Search 45+ answers..."]  │
│                                     │
│  [All] [Pricing] [Features]         │
│  [Security] [Getting Started]       │
│                                     │
└─────────────────────────────────────┘
```

**Content:**
- H2: "Frequently Asked Questions"
- Font size Mobile: 28px / 34px line-height
- Font size Desktop: 40px / 48px line-height
- Font weight: 700
- Text align: Center
- Margin-bottom: 32px

**Search Box:**
- Placeholder: "Search 45+ answers..."
- Width Mobile: Full width (with 20px margin)
- Width Desktop: 500px centered
- Height: 48px
- Border: 1px solid #E5E7EB
- Border-radius: 24px (pill shape)
- Icon: Search icon (20px) on left
- Padding: 0 20px 0 48px
- Margin-bottom: 24px

**Category Tabs:**
```
┌─────────────────────────────────────┐
│  [All] [Pricing] [Features]         │
│  [Security] [Getting Started]       │
└─────────────────────────────────────┘
```

**Tab Styling:**
- Mobile: Horizontal scroll
- Desktop: Centered flex row
- Each tab: Padding 10px 20px
- Active tab: Primary color background, white text
- Inactive tab: White background, grey text
- Border-radius: 20px
- Font size: 14px
- Font weight: 600
- Margin-bottom: 40px

#### FAQ Accordion Items

**Mobile Layout (Stacked):**
```
┌─────────────────────────────────────┐
│  ❓ Question title                  │
│  [+ Expand]                         │
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│  💰 Question title                  │
│  [- Collapse]                       │
│                                     │
│  Answer text appears here when      │
│  expanded. 2-3 sentences providing  │
│  clear, helpful information.        │
│                                     │
│  Was this helpful?                  │
│  [👍 Yes] [👎 No]                   │
│                                     │
│  [Contact Support]                  │
└─────────────────────────────────────┘
```

**8 Priority Questions:**

**Question 1:**
- Icon: ❓
- Question: "What is Delphi and how does it work?"
- Answer: "Delphi is an AI platform that creates your digital clone - a personalized AI mind trained on your knowledge, voice, and communication style. Upload your content, train the AI, and deploy it across any platform to engage with your audience 24/7 while you focus on high-value work."
- Category: Getting Started

**Question 2:**
- Icon: 💰
- Question: "How much does Delphi cost?"
- Answer: "Delphi offers flexible pricing starting from a free trial with no credit card required. Paid plans begin at $99/month for the Builder plan with advanced features. View our full pricing page for details on all plans and features."
- Link: → View Pricing (`/pricing`)
- Category: Pricing

**Question 3:**
- Icon: 🆓
- Question: "Is there a free trial?"
- Answer: "Yes! We offer a 14-day free trial with full access to all features. No credit card required to start. You can explore all capabilities and see if Delphi is right for you before committing to a paid plan."
- Category: Pricing

**Question 4:**
- Icon: 🔐
- Question: "Is my data secure?"
- Answer: "Absolutely. Delphi is SOC 2 Type II certified and fully GDPR compliant. We use enterprise-grade 256-bit encryption for all data in transit and at rest. Your content is never used to train other models, and you maintain full ownership and control of your data."
- Category: Security

**Question 5:**
- Icon: ⏱️
- Question: "How long does setup take?"
- Answer: "Most users complete their first AI clone setup in 5-10 minutes. The Delphi Interview guides you through the process step-by-step. You can start with basic settings and refine your AI over time as you add more content and preferences."
- Category: Getting Started

**Question 6:**
- Icon: 🌍
- Question: "What languages do you support?"
- Answer: "Delphi supports 95+ languages for both input content and AI responses. Your digital clone can understand and respond in multiple languages, making it easy to serve a global audience without language barriers."
- Category: Features

**Question 7:**
- Icon: 🔄
- Question: "Can I cancel anytime?"
- Answer: "Yes, you can cancel your subscription at any time with no penalties or cancellation fees. Your data remains accessible for 30 days after cancellation, giving you time to export everything if needed."
- Category: Pricing

**Question 8:**
- Icon: 📞
- Question: "Do you offer customer support?"
- Answer: "We provide 24/7 customer support via live chat and email. Our response time averages under 2 hours, and we offer priority support for Builder and Scaler plan members. We also have comprehensive documentation and video tutorials."
- Category: Features

**Accordion Item Styling:**
- Background: White
- Border: 1px solid #E5E7EB
- Border-radius: 12px
- Padding Collapsed: 20px
- Padding Expanded: 20px 20px 24px 20px
- Margin-bottom: 12px
- Shadow on hover: 0 4px 6px rgba(0,0,0,0.05)

**Question Title:**
- Font size: 18px / 24px line-height
- Font weight: 600
- Color: Primary text
- Display: Flex
- Icon size: 20px, margin-right: 12px

**Expand/Collapse Icon:**
- Size: 24px × 24px
- Position: Absolute right
- Color: Primary brand color
- Rotation: + 0deg (collapsed), × 45deg (expanded)
- Transition: 0.3s ease

**Answer Text:**
- Font size: 16px / 24px line-height
- Color: Secondary text (#6B7280)
- Margin-top: 16px
- Max-width: 700px

**Feedback Section:**
- Text: "Was this helpful?"
- Font size: 14px
- Margin-top: 20px
- Buttons: 32px × 32px, rounded
- Border: 1px solid #E5E7EB
- Hover: Primary color background

**Contact Support Button:**
- Text: "Contact Support"
- Style: Text link with arrow →
- Font size: 14px
- Font weight: 600
- Color: Primary color
- Margin-top: 12px

**Section Spacing:**
- Padding Mobile: 60px 20px
- Padding Desktop: 100px 40px
- Background: #F9FAFB (light grey)

**Expected Impact:**
- +10-15% conversion via objection removal
- +20% SEO traffic via featured snippets
- -30% support tickets for common questions

---

### Block 09: Final CTA Section
**Purpose:** Last conversion opportunity

**Background:** Gradient or brand color background

```
┌─────────────────────────────────────┐
│                                     │
│     [H2: Strong CTA headline]       │
│                                     │
│     [Supporting subtext]            │
│                                     │
│     [Primary CTA Button]            │
│     [Secondary text link]           │
│                                     │
└─────────────────────────────────────┘
```

**Content:**
- H2: "Ready to Scale Your Expertise?"
- Font size Mobile: 28px / 34px line-height
- Font size Desktop: 40px / 48px line-height
- Color: White (if dark background)
- Text align: Center

- Subtext: "Join 10,000+ experts using Delphi to scale their impact. Start free, no credit card required."
- Font size: 18px / 26px line-height
- Color: White with 90% opacity
- Margin-top: 16px

- Primary CTA: "Get Started Free"
- Link: `/signup`
- Size Mobile: Full width (max 400px)
- Size Desktop: Auto width (padding 24px 64px)
- Height: 56px
- Background: White
- Color: Primary brand color
- Font size: 16px
- Font weight: 600
- Margin-top: 32px

- Secondary link: "Schedule a Demo"
- Font size: 16px
- Color: White
- Text decoration: Underline
- Margin-top: 16px

**Section Styling:**
- Background: Linear gradient (primary to secondary brand color)
- Padding Mobile: 60px 20px
- Padding Desktop: 100px 40px
- Text align: Center

---

### Block 09.5: Exit-Intent Modal
**Purpose:** Recover 5-10% of abandoning visitors
**Type:** Overlay Modal
**Trigger:** Mouse exit or back button

**Trigger Conditions:**
- **Desktop:** Mouse cursor leaves viewport (top edge)
- **Mobile:** Back button press or rapid scroll to top
- **Delay:** 500ms after trigger event
- **Frequency:** Once per session (localStorage tracking)
- **Key:** `exit_intent_shown_session_[timestamp]`

#### Variant A: Lead Magnet Offer

**Modal Layout:**
```
Semi-transparent overlay (rgba(0,0,0,0.5))

┌─────────────────────────────────────┐
│  [× Close]                   (top right)
│                                     │
│  📘 "Before You Go..."              │
│                                     │
│  "Get Our Free Guide:               │
│   10 Ways to Automate Your          │
│   Workflow with AI                  │
│   (No Experience Required)"         │
│                                     │
│  ┌──────────────────────────────┐  │
│  │ Email input field            │  │
│  └──────────────────────────────┘  │
│                                     │
│  [Download Free Guide]              │
│                                     │
│  ✓ 8,543 downloads this month       │
│  ✓ No spam, unsubscribe anytime     │
│                                     │
│  [No thanks, I'll miss out →]       │
│                                     │
└─────────────────────────────────────┘
```

**Content:**
- Icon: 📘 (32px)
- Headline: "Before You Go..."
- Font size: 24px
- Font weight: 700
- Color: Primary text
- Margin-bottom: 12px

- Subheadline: "Get Our Free Guide: 10 Ways to Automate Your Workflow with AI (No Experience Required)"
- Font size: 18px / 26px line-height
- Font weight: 600
- Color: Primary text
- Margin-bottom: 24px

**Email Input:**
- Placeholder: "Enter your email address"
- Width: 100%
- Height: 48px
- Border: 2px solid #E5E7EB
- Border-radius: 8px
- Font size: 16px
- Padding: 0 16px
- Focus border: Primary color

**Primary CTA:**
- Text: "Download Free Guide"
- Width: 100%
- Height: 48px
- Background: Primary color
- Color: White
- Border-radius: 8px
- Font size: 16px
- Font weight: 600
- Margin-top: 16px

**Social Proof:**
- Text: "✓ 8,543 downloads this month"
- Text: "✓ No spam, unsubscribe anytime"
- Font size: 14px
- Color: Secondary text
- Margin-top: 16px
- Line-height: 24px

**Secondary Link:**
- Text: "No thanks, I'll miss out →"
- Font size: 14px
- Color: Secondary text (#6B7280)
- Text decoration: Underline
- Margin-top: 16px
- Text align: Center
- Hover: Primary color

#### Variant B: Discount Offer

**Modal Layout:**
```
┌─────────────────────────────────────┐
│  [× Close]                   (top right)
│                                     │
│  🎁 "Wait! Special Offer"           │
│                                     │
│  "Get 20% Off Your First Month"     │
│                                     │
│  Promo Code: WELCOME20              │
│  ⏰ Expires in: [14:32]             │
│                                     │
│  [Claim My 20% Discount]            │
│                                     │
│  [No thanks, I'll pay full price]   │
│                                     │
└─────────────────────────────────────┘
```

**Content:**
- Icon: 🎁 (32px)
- Headline: "Wait! Special Offer"
- Font size: 24px
- Font weight: 700
- Margin-bottom: 12px

- Offer text: "Get 20% Off Your First Month"
- Font size: 20px
- Font weight: 600
- Margin-bottom: 24px

**Promo Code Display:**
- Background: #F9FAFB
- Border: 2px dashed primary color
- Padding: 12px 20px
- Border-radius: 8px
- Font family: Monospace
- Font size: 18px
- Font weight: 700
- Letter-spacing: 2px
- Text align: Center
- Margin-bottom: 16px

**Countdown Timer:**
- Text: "⏰ Expires in: "
- Timer format: [MM:SS]
- Font size: 16px
- Font weight: 600
- Color: Warning color (#F59E0B)
- Margin-bottom: 24px
- Text align: Center

**Primary CTA:**
- Text: "Claim My 20% Discount"
- Width: 100%
- Height: 48px
- Background: Primary color
- Color: White
- Border-radius: 8px
- Font size: 16px
- Font weight: 600

**Secondary Link:**
- Text: "No thanks, I'll pay full price"
- Font size: 14px
- Color: Secondary text
- Text decoration: Underline
- Margin-top: 16px
- Text align: Center

**Modal Styling:**
- Width Mobile: 90% (max 380px)
- Width Desktop: 480px
- Background: White
- Border-radius: 16px
- Padding: 40px 32px
- Box shadow: 0 20px 25px rgba(0,0,0,0.25)
- Position: Fixed, centered
- Z-index: 10000

**Close Button (X):**
- Size: 32px × 32px
- Position: Absolute top 16px, right 16px
- Color: Secondary text
- Hover: Primary text
- Font size: 24px
- Cursor: pointer

**Overlay:**
- Background: rgba(0,0,0,0.5)
- Backdrop-filter: blur(4px) (optional)
- Position: Fixed, full viewport
- Z-index: 9999

**Close Behavior:**
- Click X button
- Click overlay background
- Press Escape key
- Don't show again this session

**Form Behavior:**
- POST to `/api/exit-intent-signup` (Variant A)
- Redirect to `/signup?promo=WELCOME20` (Variant B)
- On success: Show "Check your email!" message (Variant A)
- Analytics: `gtag('event', 'exit_intent_conversion', {variant: 'lead_magnet'})`

**Technical Specs:**
- JavaScript: Monitor mouse position for exit detection
- localStorage tracking: `exit_intent_shown = timestamp`
- Session check: Only show once per session
- A/B testing: Track conversion rate per variant
- Mobile: Detect back button with popstate event

**Expected Impact:**
- +5-10% email capture rate
- +3-7% conversion recovery
- Variant A best for: Top of funnel, awareness stage
- Variant B best for: Mid-funnel, consideration stage

---

### Block 09.7: Sticky Mobile CTA Bar
**Purpose:** Persistent conversion path on mobile
**Type:** Fixed Bottom Bar
**Scope:** Mobile devices only (<768px)

**Layout:**
```
Fixed Bottom Bar (Mobile Only):

┌─────────────────────────────────────┐
│  Free Trial • $99/mo after         │
│  ┌──────────────────────────────┐  │
│  │  [Start Free Trial]          │  │
│  └──────────────────────────────┘  │
└─────────────────────────────────────┘
```

**Specifications:**

**Bar Dimensions:**
- Height: 68px (total)
- Width: 100% viewport
- Background: White (#FFFFFF)
- Border-top: 1px solid #E5E7EB
- Box shadow: 0 -4px 6px rgba(0,0,0,0.1)
- Z-index: 999
- Position: Fixed bottom 0

**Pricing Text:**
- Text: "Free Trial • $99/mo after"
- Font size: 12px
- Font weight: 500
- Color: Secondary text (#6B7280)
- Text align: Center
- Margin-bottom: 8px
- Padding-top: 8px

**CTA Button:**
- Text: "Start Free Trial" (default)
- Height: 48px
- Width: calc(100% - 32px) (16px margin each side)
- Background: Primary color (#6366F1)
- Color: White
- Font size: 16px
- Font weight: 600
- Border-radius: 8px
- Border: None
- Margin: 0 16px 8px 16px

**Activation Behavior:**
- **Show:** After user scrolls 50% down page
- **Animation:** Slide up from bottom (300ms ease-out)
- **Hide:** When footer becomes visible (IntersectionObserver)
- **Persist:** Stays visible during scroll
- **Transform:** translateY(100%) → translateY(0)

**Dynamic CTA Text by Section:**
```javascript
Section Detection (via scroll position):
- Hero area (0-20%): "Start Free Trial"
- Features area (20-40%): "See How It Works"
- Pricing area (40-60%): "Choose Your Plan"
- Testimonials (60-80%): "Join 10,000+ Experts"
- Bottom of page (80-100%): "Get Started Now"
```

**JavaScript Example:**
```javascript
let stickyBar = document.getElementById('sticky-mobile-cta');
let footer = document.getElementById('footer');

// Show after 50% scroll
window.addEventListener('scroll', () => {
  let scrollPercent = (window.scrollY / (document.body.scrollHeight - window.innerHeight)) * 100;

  if (scrollPercent > 50) {
    stickyBar.classList.add('visible');
  } else {
    stickyBar.classList.remove('visible');
  }

  // Update CTA text based on scroll position
  if (scrollPercent < 20) {
    stickyBar.querySelector('button').textContent = 'Start Free Trial';
  } else if (scrollPercent < 40) {
    stickyBar.querySelector('button').textContent = 'See How It Works';
  } else if (scrollPercent < 60) {
    stickyBar.querySelector('button').textContent = 'Choose Your Plan';
  } else if (scrollPercent < 80) {
    stickyBar.querySelector('button').textContent = 'Join 10,000+ Experts';
  } else {
    stickyBar.querySelector('button').textContent = 'Get Started Now';
  }
});

// Hide when footer is visible
let footerObserver = new IntersectionObserver((entries) => {
  if (entries[0].isIntersecting) {
    stickyBar.classList.add('hidden');
  } else {
    stickyBar.classList.remove('hidden');
  }
}, { threshold: 0.1 });

footerObserver.observe(footer);
```

**CSS Classes:**
```css
.sticky-mobile-cta {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  transform: translateY(100%);
  transition: transform 0.3s ease-out;
}

.sticky-mobile-cta.visible {
  transform: translateY(0);
}

.sticky-mobile-cta.hidden {
  transform: translateY(100%);
}

@media (min-width: 768px) {
  .sticky-mobile-cta {
    display: none; /* Hide on tablet and desktop */
  }
}
```

**Analytics Tracking:**
- Event: `gtag('event', 'sticky_cta_click', {cta_text: 'Start Free Trial', scroll_position: '65%'})`
- Track: Click-through rate, conversion rate, scroll depth when clicked

**Expected Impact:**
- +15-25% mobile conversion rate improvement
- Reduced drop-off on long-scroll pages
- Better CTA visibility on small screens

---

### Block 10: Footer
**Type:** Multi-column footer

#### Mobile Layout (Stacked Sections)
```
┌─────────────────────────────────────┐
│  [Logo]                             │
│  [Tagline text]                     │
│                                     │
│  Product                            │
│  - Pricing                          │
│  - FAQ                              │
│                                     │
│  Resources                          │
│  - Documentation                    │
│  - Status                           │
│  - Privacy Policy                   │
│  - Terms of Use                     │
│                                     │
│  Company                            │
│  - About                            │
│  - Team                             │
│  - Careers                          │
│  - Blog                             │
│                                     │
│  [Social Icons]                     │
│  [LinkedIn] [Instagram] [X] [TikTok] [YouTube] │
│                                     │
│  ─────────────────────              │
│                                     │
│  © 2025 Delphi. All rights reserved.│
│                                     │
└─────────────────────────────────────┘
```

#### Desktop Layout (Multi-column)
```
┌───────────────────────────────────────────────────────────┐
│                                                           │
│  [Logo]           Product      Resources    Company      │
│  [Tagline]        - Pricing    - Docs       - About      │
│                   - FAQ        - Status     - Team       │
│  [Social Icons]                - Privacy    - Careers    │
│                                - Terms      - Blog       │
│                                                           │
│  ─────────────────────────────────────────────────────   │
│                                                           │
│  © 2025 Delphi. All rights reserved.    [Social Icons]   │
│                                                           │
└───────────────────────────────────────────────────────────┘
```

**Logo Section:**
- Logo: 140px × 36px
- Tagline: "Scale Your Insight. Stay Focused on What Matters."
- Font size: 14px
- Color: Secondary text (#6B7280)
- Max-width: 280px
- Margin-top: 12px

**Footer Columns:**

**Column 1: Product**
- Pricing → `/pricing`
- FAQ → `/faq`

**Column 2: Resources**
- Documentation → `https://docs.delphi.ai/`
- Status → `/status`
- Privacy Policy → `/privacy-policy`
- Terms of Use → `/terms-of-use`

**Column 3: Company**
- About → `/about`
- Team → `/team`
- Careers → `/careers`
- Blog → `/blog`

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
- Hover: Primary color

**Social Icons:**
- Size: 24px × 24px
- Color: Secondary text
- Hover: Primary color
- Gap: 16px
- Display: Flex row

**Social Links:**
- LinkedIn → `https://www.linkedin.com/company/delphi-ai`
- Instagram → `https://www.instagram.com/delphi.ai`
- X (Twitter) → `https://twitter.com/delphi_ai`
- TikTok → `https://www.tiktok.com/@delphi.ai`
- YouTube → `https://www.youtube.com/@delphi-ai`

**Copyright Bar:**
- Text: "© 2025 Delphi. All rights reserved."
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
- Tablet: 2 columns (Logo + Product, Resources + Company)
- Desktop: 4 columns (Logo takes 2x width, others 1x)
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

### 3. Carousel Controls
- **Touch:** Swipe left/right
- **Mouse:** Click and drag (desktop)
- **Arrows:** Previous/Next navigation
- **Auto-play:** Optional, 5s interval, pause on hover
- **Dots:** Indicate current slide, clickable

### 4. Scroll Animations
- **Fade in:** Elements fade in as they enter viewport
- **Slide up:** Elements slide up 20px as they appear
- **Stagger:** Sequential animation for groups (50ms delay)
- **Trigger:** IntersectionObserver, threshold 0.2

### 5. Button States
- **Default:** Primary color background
- **Hover:** Darken 10%, lift 2px (desktop)
- **Active:** Scale 0.98
- **Focus:** Outline 2px primary color
- **Disabled:** 50% opacity, cursor not-allowed

### 6. Card Hover Effects (Desktop)
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
- **Subset:** Latin characters only
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
- Carousel: `aria-label="Featured Digital Minds"` + `aria-live="polite"`
- Buttons: Descriptive `aria-label` when text isn't clear

### Keyboard Navigation
- All interactive elements must be focusable
- Tab order must be logical
- Focus indicators must be visible (outline)
- Escape key closes modals/menus
- Arrow keys navigate carousel

### Screen Readers
- Images: Descriptive alt text
- Icons: `aria-label` or `aria-hidden="true"` if decorative
- Links: Clear purpose, avoid "click here"
- Form inputs: Associated labels

### Color Contrast
- Text on backgrounds: WCAG AA minimum (4.5:1)
- Large text (18px+): 3:1 minimum
- Interactive elements: 3:1 against background
- Test with contrast checker tools

### Focus Management
- Skip to main content link (hidden, visible on focus)
- Modal open: Focus first interactive element
- Modal close: Return focus to trigger element

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
Primary Brand: #6366F1 (Indigo)
Primary Hover: #4F46E5
Primary Text: #0A0A0A (Near Black)
Secondary Text: #6B7280 (Grey)
Tertiary Text: #9CA3AF (Light Grey)

Background Primary: #FFFFFF (White)
Background Secondary: #F9FAFB (Light Grey)
Background Accent: #EEF2FF (Light Indigo)

Border Default: #E5E7EB (Light Grey)
Border Focus: #6366F1 (Primary)

Success: #10B981 (Green)
Warning: #F59E0B (Orange)
Error: #EF4444 (Red)
Info: #3B82F6 (Blue)
```

### Typography
```
Font Family:
  - Primary: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif
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

## Testing Checklist

### Functional Testing
- [ ] All links navigate to correct URLs
- [ ] All buttons trigger correct actions
- [ ] Forms validate properly (if applicable)
- [ ] Navigation menu opens/closes correctly
- [ ] Carousel navigation works (swipe, arrows, dots)
- [ ] CTAs are clickable and lead to correct pages

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

### Cross-Device Testing
- [ ] Touch interactions work (mobile/tablet)
- [ ] Hover states work (desktop)
- [ ] Gestures work (swipe, pinch, etc.)
- [ ] Viewport meta tag present
- [ ] No horizontal scrolling

---

## Developer Notes

### Tech Stack Recommendations
- **Framework:** React, Next.js, or Framer (current)
- **Styling:** Tailwind CSS or CSS Modules
- **Animations:** Framer Motion or GSAP
- **Carousel:** Swiper.js or Embla Carousel
- **Forms:** React Hook Form + Zod validation
- **Analytics:** Google Tag Manager (already implemented)

### Third-Party Scripts
- **GTM:** GTM-MSZHW3T7 (already set up)
- **Font Loading:** Google Fonts or self-hosted
- **Video Player:** Native HTML5 or Plyr

### SEO Requirements
- **Title:** "Delphi | Scale Your Insight. Stay Focused on What Matters."
- **Meta Description:** "Create your AI digital clone. Delphi enables experts, creators, and businesses to build personalized AI minds that scale their expertise 24/7."
- **Open Graph:** Image 1200×630px, title, description
- **Twitter Card:** Summary large image
- **Canonical URL:** https://www.delphi.ai/
- **Structured Data:** Organization, WebSite schemas
- **Hreflang:** If multi-language support

### Page Load Priorities
1. **Critical:** Header, Hero section, fonts
2. **High:** Features, How It Works
3. **Medium:** Carousel, Testimonials
4. **Low:** Footer, Analytics scripts

---

## Version History

**v1.0** - November 12, 2025
- Initial homepage template specification
- Mobile-first approach
- Complete block breakdown from header to footer

---

## Questions for Stakeholders

1. Video in hero section: What duration? Auto-play?
2. Carousel auto-advance: Enabled or manual only?
3. Featured Digital Minds: Which profiles to showcase?
4. Testimonials: Real names or anonymized?
5. Pricing teaser: Show all 4 plans or just 3?
6. Final CTA: Same as hero or different messaging?
7. Analytics: Additional tracking beyond GTM?
8. A/B testing: Variants planned for any sections?

---

**End of Homepage Template Specification**
