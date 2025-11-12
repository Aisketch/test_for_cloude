# Pricing Page Template - Technical Specification

**Page Type:** Product/Pricing Page
**URL Pattern:** `/pricing`
**Priority:** High
**Approach:** Mobile First
**Last Updated:** November 12, 2025

---

## Page Overview

**Purpose:** Display pricing plans, compare features, and drive conversion to paid plans.

**Key Goals:**
- Clearly present pricing tiers
- Highlight value propositions
- Compare plan features
- Drive sign-ups (especially paid plans)
- Answer common pricing questions

---

## Page Structure

### Block 01: Header Navigation
*(Same as Homepage - Sticky header with "Pricing" highlighted)*

---

### Block 02: Page Hero
```
┌─────────────────────────────────────┐
│                                     │
│  [H1: Simple, Transparent Pricing]  │
│                                     │
│  [Subtitle: Start free, scale...]   │
│                                     │
│  ○ Monthly    ● Annual (Save 20%)   │
│                                     │
└─────────────────────────────────────┘
```

**H1:** "Simple, Transparent Pricing"
- Mobile: 32px / 38px, Desktop: 48px / 56px
- Weight: 700, Center aligned

**Subtitle:** "Start free. Scale as you grow. No hidden fees."
- Font size: 16px / 24px (mobile), 18px / 28px (desktop)
- Color: Secondary text

**Billing Toggle:**
- Options: Monthly / Annual
- Show savings badge on Annual: "Save 20%"
- Toggle switch or pill buttons
- Default: Monthly
- Mobile: Full width pills, Desktop: Centered inline

**Spacing:** Padding 40px 20px (mobile), 60px 40px (desktop)

---

### Block 03: Pricing Cards Grid

#### Mobile Layout (Stacked)
```
┌─────────────────────────────────────┐
│  ┌───────────────────────────────┐  │
│  │ Free                          │  │
│  │ $0/mo                         │  │
│  │ [Features list]               │  │
│  │ [Get Started Button]          │  │
│  └───────────────────────────────┘  │
│  [Gap]                              │
│  ┌───────────────────────────────┐  │
│  │ Builder (POPULAR)             │  │
│  │ $99/mo                        │  │
│  │ [Features]                    │  │
│  │ [Start Free Trial]            │  │
│  └───────────────────────────────┘  │
│  ...                                │
└─────────────────────────────────────┘
```

#### Desktop Layout
```
┌───────────┬───────────┬───────────┬───────────┐
│   Free    │  Builder  │  Scaler   │ Immortal  │
│           │ (POPULAR) │           │           │
└───────────┴───────────┴───────────┴───────────┘
```

---

### Pricing Card Structure

```
┌──────────────────────────┐
│  [Badge: POPULAR]        │  ← Optional
│                          │
│  [Plan Name]             │
│                          │
│  [Price]                 │
│  /month or /year         │
│                          │
│  [One-line description]  │
│                          │
│  ─────────────           │
│                          │
│  ✓ Feature 1             │
│  ✓ Feature 2             │
│  ✓ Feature 3             │
│  ✓ Feature 4             │
│  ✓ Feature 5             │
│                          │
│  [CTA Button]            │
│                          │
└──────────────────────────┘
```

---

### Plan 1: Free
**Name:** "Free"
**Price:** "$0"
**Period:** "/month"
**Description:** "Perfect for trying Delphi"
**CTA:** "Get Started"
**CTA URL:** `/signup`
**Highlight:** No

**Features:**
- ✓ 1 Digital Mind
- ✓ 100,000 training words
- ✓ 100 conversations/month
- ✓ Text interactions only
- ✓ Basic analytics
- ✓ Community support

---

### Plan 2: Builder (RECOMMENDED)
**Name:** "Builder"
**Badge:** "POPULAR" or "MOST POPULAR"
**Price:** "$99" (monthly), "$79" (annual - billed $948/year)
**Description:** "For creators scaling their expertise"
**CTA:** "Start Free Trial"
**CTA URL:** `/signup?plan=builder`
**Highlight:** YES (border, shadow, or background accent)

**Features:**
- ✓ Everything in Free, plus:
- ✓ 3 million training words
- ✓ 1,000 conversations/month
- ✓ Voice cloning
- ✓ Custom branding
- ✓ Advanced analytics
- ✓ Priority support
- ✓ Website embed
- ✓ Email support

---

### Plan 3: Scaler
**Name:** "Scaler"
**Price:** "$399" (monthly), "$319" (annual - billed $3,828/year)
**Description:** "For businesses scaling at volume"
**CTA:** "Start Free Trial"
**CTA URL:** `/signup?plan=scaler`

**Features:**
- ✓ Everything in Builder, plus:
- ✓ 12 million training words
- ✓ 10,000 contacts
- ✓ 3 team members
- ✓ CRM sync
- ✓ WhatsApp, Slack, Zoom integrations
- ✓ Professional voice with emotional intelligence
- ✓ Advanced mind architecture
- ✓ Dedicated account manager

---

### Plan 4: Immortal
**Name:** "Immortal"
**Badge:** "ENTERPRISE"
**Price:** "Custom"
**Description:** "Unlimited scale for enterprises"
**CTA:** "Contact Sales"
**CTA URL:** `/contact?inquiry=enterprise` or modal

**Features:**
- ✓ Everything in Scaler, plus:
- ✓ Unlimited training words
- ✓ Unlimited contacts
- ✓ Unlimited team members
- ✓ Custom integrations
- ✓ SLA & uptime guarantee
- ✓ Advanced security controls
- ✓ Dedicated infrastructure
- ✓ White-glove onboarding

---

### Card Styling

**Default Card:**
- Background: White
- Border: 1px solid #E5E7EB
- Border-radius: 16px
- Padding: 32px 24px
- Shadow: 0 1px 3px rgba(0,0,0,0.1)

**Popular Card (Builder):**
- Border: 2px solid #6366F1 (Primary)
- Shadow: 0 8px 16px rgba(99,102,241,0.15)
- Scale: 1.05 on desktop (slightly larger)
- Optional: Background accent (#EEF2FF - light primary)

**Badge:**
- Position: Top right or above plan name
- Background: #6366F1 (Primary)
- Color: White
- Padding: 4px 12px
- Border-radius: 12px
- Font size: 11px
- Font weight: 700
- Text: uppercase

**Plan Name:**
- Font size: 24px
- Font weight: 700
- Margin-bottom: 8px

**Price:**
- Font size: 48px / 56px
- Font weight: 700
- Color: Primary text
- Display: inline

**Period:**
- Font size: 16px
- Color: Secondary text
- Display: inline

**Description:**
- Font size: 15px
- Color: Secondary text
- Margin: 12px 0 24px

**Features List:**
- Font size: 15px / 22px line-height
- Color: Primary text
- List style: None
- Padding: 0
- Margin: 24px 0

**Feature Item:**
- Margin-bottom: 12px
- Display: flex, align-items: start
- Gap: 8px

**Checkmark:**
- Color: #10B981 (Green) or Primary color
- Size: 20px

**CTA Button:**
- Width: 100%
- Height: 48px
- Font size: 16px
- Font weight: 600
- Border-radius: 8px
- Margin-top: 24px

**Primary CTA (Popular plan):**
- Background: #6366F1
- Color: White
- Hover: Darken 10%

**Secondary CTA (Other plans):**
- Background: White
- Color: Primary
- Border: 2px solid Primary
- Hover: Background Primary, Color White

**Grid:**
- Mobile: 1 column, gap 24px
- Tablet: 2 columns, gap 24px
- Desktop: 4 columns, gap 24px
- Max-width: 1300px
- Padding: 40px 20px

---

### Block 04: Feature Comparison Table
**Purpose:** Detailed feature comparison

```
┌─────────────────────────────────────┐
│  [H2: Compare Plans]                │
│                                     │
│  [Table Header]                     │
│  Feature  | Free | Builder | ...   │
│  ─────────────────────────────────  │
│  Row 1    |  ✓   |    ✓    | ...   │
│  Row 2    |  ✗   |    ✓    | ...   │
│  ...                                │
└─────────────────────────────────────┘
```

**Mobile:** Accordion or collapsible sections per category
**Desktop:** Full comparison table

**Feature Categories:**
1. **Content & Training**
   - Training words capacity
   - Content types supported
   - Upload methods
   - Content refresh rate

2. **Interactions**
   - Monthly conversations
   - Text interactions
   - Voice interactions
   - Video interactions
   - Response time

3. **Customization**
   - Voice cloning
   - Personality tuning
   - Custom branding
   - Mind architecture

4. **Distribution**
   - Website embed
   - WhatsApp
   - Slack
   - Zoom
   - SMS
   - API access

5. **Management**
   - Contacts limit
   - Team members
   - Access groups
   - CRM sync
   - Analytics
   - Broadcasts

6. **Support**
   - Community support
   - Email support
   - Priority support
   - Dedicated account manager
   - SLA

**Table Styling:**
- Header: Sticky on scroll
- Cell padding: 16px
- Border: 1px solid #E5E7EB
- Alternate row background: #F9FAFB
- Icons: ✓ (green) / ✗ (grey) / – (not applicable)

---

### Block 05: FAQ Section
```
┌─────────────────────────────────────┐
│  [H2: Frequently Asked Questions]   │
│                                     │
│  [Accordion Item 1] ▼               │
│  [Accordion Item 2] ▼               │
│  ...                                │
└─────────────────────────────────────┘
```

**Questions:**
1. **Can I try Delphi for free?**
   - Yes! Our Free plan lets you create one Digital Mind...

2. **What happens after my free trial?**
   - Your 14-day free trial gives you full access to Builder...

3. **Can I upgrade or downgrade anytime?**
   - Absolutely. You can change plans at any time...

4. **What payment methods do you accept?**
   - We accept all major credit cards, PayPal, and wire transfer...

5. **Do you offer refunds?**
   - Yes, we offer a 30-day money-back guarantee...

6. **How is pricing calculated?**
   - Plans are billed monthly or annually...

7. **Is there a limit on conversations?**
   - Yes, each plan has a monthly conversation limit...

8. **Can I add more team members?**
   - Yes, additional team members can be added for $X/month each...

9. **Do you offer discounts for nonprofits or students?**
   - Yes! Contact us for special pricing...

10. **What's included in custom enterprise pricing?**
    - Immortal plans include unlimited everything...

**Accordion Styling:**
- Button height: 56px
- Background: White
- Border: 1px solid #E5E7EB
- Border-radius: 8px
- Margin-bottom: 12px
- Font size: 16px
- Font weight: 600
- Padding: 16px 20px
- Hover: Background #F9FAFB

**Answer:**
- Padding: 20px
- Background: #F9FAFB
- Font size: 15px / 22px
- Color: Secondary text

**Icon:**
- Chevron down/up
- Position: Right side
- Transition: rotate 180deg when open

---

### Block 06: Trust Signals
```
┌─────────────────────────────────────┐
│  Trusted by 10,000+ experts         │
│                                     │
│  [Company Logo] [Logo] [Logo]       │
│                                     │
│  🔒 Bank-level security             │
│  ✓ SOC 2 compliant                  │
│  ✓ GDPR compliant                   │
│  ✓ 99.9% uptime SLA                 │
└─────────────────────────────────────┘
```

---

### Block 07: Final CTA
```
┌─────────────────────────────────────┐
│  [H2: Ready to Get Started?]        │
│  [Subtitle]                         │
│  [Start Free Trial Button]          │
│  [Schedule Demo Link]               │
└─────────────────────────────────────┘
```

**Background:** Gradient or accent color
**Padding:** 60px 20px (mobile), 100px 40px (desktop)

---

### Block 08: Footer
*(Same as Homepage)*

---

## Interactive Elements

### 1. Billing Toggle (Monthly/Annual)
- Update all prices dynamically
- Show savings badge on annual
- Smooth transition (300ms)
- URL parameter: `?billing=annual`

### 2. Plan Card Hover (Desktop)
- Lift effect: translateY(-8px)
- Shadow increase
- Transition: 0.3s ease

### 3. FAQ Accordion
- Click to expand/collapse
- One or multiple open at once
- Smooth height animation
- Arrow rotation
- Optional: Deep link to specific question (#faq-question-1)

### 4. Comparison Table Scroll
- Horizontal scroll on mobile
- Shadow indicators for scrollable area
- Sticky header column (feature names)

---

## Conversion Optimization

### Psychological Triggers
- **Anchoring:** Show most expensive first or in middle
- **Social Proof:** "Most popular" badge
- **Scarcity:** "Limited time offer" (if applicable)
- **Urgency:** "14-day trial" creates deadline
- **Reciprocity:** Free plan builds trust

### CTA Hierarchy
1. **Primary:** Popular plan CTA (most prominent)
2. **Secondary:** Other plan CTAs
3. **Tertiary:** Contact sales, Learn more

### Clarity
- Clear feature differences between plans
- No hidden fees messaging
- Transparent pricing
- Easy upgrade path

---

## Accessibility

- All prices have proper currency semantics
- Comparison table has proper headers (th/td)
- Accordion buttons keyboard accessible (Enter/Space)
- Focus indicators on all interactive elements
- Screen reader announces expanded/collapsed state

---

## SEO

**Title:** "Pricing | Delphi - AI Digital Clone Platform"
**Description:** "Simple, transparent pricing for Delphi. Start free, scale as you grow. Plans from $0 to custom enterprise. No hidden fees."
**Canonical:** `https://www.delphi.ai/pricing`

**Structured Data:**
```json
{
  "@type": "Offer",
  "name": "Builder Plan",
  "price": "99",
  "priceCurrency": "USD"
}
```

---

**End of Pricing Page Template**
