# Contact Page Template - Technical Specification

**Page Type:** Contact/Support Page
**URL Pattern:** `/contact`
**Priority:** Medium
**Approach:** Mobile First
**Last Updated:** November 12, 2025

---

## 🌐 i18n Configuration

### Languages
- **Default Language:** UA (Українська)
- **Available Languages:** EN (English), UA (Українська)
- **Language Selector:** Yes
- **RTL Support:** No

### URL Structure  
- **UA (Default):** `https://[DOMAIN][PAGE_PATH]`
- **EN:** `https://[DOMAIN]/en[PAGE_PATH]`

### Content Keys (JSON)
```json
{
  "ua": { "page_specific_keys": "[PLACEHOLDER_UA]" },
  "en": { "page_specific_keys": "[PLACEHOLDER_EN]" }
}
```

---

## 🔍 SEO Configuration

### Meta Tags

**Ukrainian Version:**
```html
<title>[PAGE_TITLE_UA] | [BRAND_NAME]</title>
<meta name="description" content="[META_DESCRIPTION_UA]" />
<meta name="keywords" content="[PRIMARY_KEYWORD_UA], [SECONDARY_KEYWORD_UA]" />
<meta name="robots" content="[ROBOTS_DIRECTIVE]" />
<link rel="canonical" href="https://[DOMAIN][PAGE_PATH]" />
```

**English Version:**
```html
<title>[PAGE_TITLE_EN] | [BRAND_NAME]</title>
<meta name="description" content="[META_DESCRIPTION_EN]" />
<meta name="keywords" content="[PRIMARY_KEYWORD_EN], [SECONDARY_KEYWORD_EN]" />
<link rel="canonical" href="https://[DOMAIN]/en[PAGE_PATH]" />
```

### Open Graph (Ukrainian)
```html
<meta property="og:type" content="[OG_TYPE]" />
<meta property="og:url" content="https://[DOMAIN][PAGE_PATH]" />
<meta property="og:title" content="[OG_TITLE_UA]" />
<meta property="og:description" content="[OG_DESCRIPTION_UA]" />
<meta property="og:image" content="https://[DOMAIN]/images/og/[PAGE_SLUG]-og-ua.png" />
<meta property="og:locale" content="uk_UA" />
<meta property="og:locale:alternate" content="en_US" />
```

### Hreflang
```html
<link rel="alternate" hreflang="uk" href="https://[DOMAIN][PAGE_PATH]" />
<link rel="alternate" hreflang="en" href="https://[DOMAIN]/en[PAGE_PATH]" />
<link rel="alternate" hreflang="x-default" href="https://[DOMAIN][PAGE_PATH]" />
```

---

## 🤖 GEO Configuration

### FAQ Schema - [PAGE_NAME]

**Questions (Ukrainian):**
1. [FAQ_Q1_UA] → Answer: [FAQ_A1_UA]
2. [FAQ_Q2_UA] → Answer: [FAQ_A2_UA]
3. [FAQ_Q3_UA] → Answer: [FAQ_A3_UA]

**Questions (English):**
1. [FAQ_Q1_EN] → Answer: [FAQ_A1_EN]
2. [FAQ_Q2_EN] → Answer: [FAQ_A2_EN]
3. [FAQ_Q3_EN] → Answer: [FAQ_A3_EN]

---

## 📊 Structured Data

```json
{
  "@context": "https://schema.org",
  "@type": "[SCHEMA_TYPE]",
  "[SCHEMA_PROPERTIES]": "[SCHEMA_VALUES]"
}
```

---
---

## Page Overview

**Purpose:** Provide multiple ways for users to contact the company (form, email, social, chat).

---

## Page Structure

### Block 01: Header Navigation
*(Same as Homepage)*

---

### Block 02: Hero Section
```
┌─────────────────────────────────────┐
│                                     │
│  [H1: Get in Touch]                 │
│                                     │
│  [Subtitle: We're here to help...] │
│                                     │
└─────────────────────────────────────┘
```

**H1:** "Get in Touch" or "Contact Us"
- Mobile: 32px / 38px, Desktop: 48px / 56px
- Weight: 700, Center aligned

**Subtitle:** "We're here to help. Choose the best way to reach us."
- Font size: 16px / 24px (mobile), 18px / 28px (desktop)
- Color: Secondary text

**Spacing:** 40px 20px (mobile), 60px 40px (desktop)

---

### Block 03: Contact Methods Grid
```
┌─────────────────────────────────────┐
│  ┌──────────┬──────────┬──────────┐ │
│  │ [Icon]   │ [Icon]   │ [Icon]   │ │
│  │ Sales    │ Support  │ Partners │ │
│  │ [Email]  │ [Email]  │ [Form]   │ │
│  └──────────┴──────────┴──────────┘ │
└─────────────────────────────────────┘
```

**Mobile:** 1 column, stack
**Desktop:** 3 columns

**Card Structure:**
```
┌──────────────────────┐
│                      │
│  [Icon 64×64]        │
│                      │
│  [Title]             │
│                      │
│  [Description]       │
│                      │
│  [CTA Button/Link]   │
│                      │
└──────────────────────┘
```

**Example Cards:**

**1. Sales Inquiries**
- Icon: 💼 Briefcase
- Title: "Sales"
- Description: "Interested in Delphi for your team? Let's talk."
- CTA: "sales@delphi.ai" (clickable mailto)

**2. Customer Support**
- Icon: 🛟 Life Preserver
- Title: "Support"
- Description: "Need help? Our support team is ready to assist."
- CTA: "Visit Help Center" → `docs.delphi.ai`

**3. Partnership Opportunities**
- Icon: 🤝 Handshake
- Title: "Partnerships"
- Description: "Let's explore collaboration opportunities."
- CTA: "Get in Touch" → Opens form

**4. Media & Press**
- Icon: 📰 Newspaper
- Title: "Press"
- Description: "Media inquiries and press kit."
- CTA: "press@delphi.ai"

**Card Styling:**
- Background: White
- Border: 1px solid #E5E7EB
- Border-radius: 12px
- Padding: 32px 24px
- Text align: Center
- Hover: Shadow, lift

**Grid:**
- Gap: 24px
- Max-width: 1100px
- Padding: 40px 20px

---

### Block 04: Contact Form
```
┌─────────────────────────────────────┐
│  [H2: Send Us a Message]            │
│                                     │
│  ┌───────────────────────────────┐  │
│  │ Full Name *                   │  │
│  └───────────────────────────────┘  │
│                                     │
│  ┌───────────────────────────────┐  │
│  │ Email Address *               │  │
│  └───────────────────────────────┘  │
│                                     │
│  ┌───────────────────────────────┐  │
│  │ Subject *                     │  │
│  └───────────────────────────────┘  │
│                                     │
│  ┌───────────────────────────────┐  │
│  │ Message *                     │  │
│  │                               │  │
│  │ (multiline textarea)          │  │
│  │                               │  │
│  └───────────────────────────────┘  │
│                                     │
│  ☐ I agree to the Privacy Policy    │
│                                     │
│  [Send Message Button]              │
│                                     │
└─────────────────────────────────────┘
```

**Form Inputs:**

**Full Name:**
- Type: text
- Placeholder: "John Doe"
- Required: Yes
- Validation: Min 2 characters

**Email:**
- Type: email
- Placeholder: "john@example.com"
- Required: Yes
- Validation: Valid email format

**Subject:**
- Type: select or text
- Options (if select):
  - General Inquiry
  - Sales Question
  - Technical Support
  - Partnership
  - Press Inquiry
  - Other
- Required: Yes

**Message:**
- Type: textarea
- Placeholder: "How can we help you?"
- Rows: 6 (mobile), 8 (desktop)
- Required: Yes
- Validation: Min 10 characters
- Max: 1000 characters (show counter)

**Privacy Checkbox:**
- Required: Yes
- Text: "I agree to the [Privacy Policy](#)" (link)
- Font size: 14px

**Submit Button:**
- Text: "Send Message"
- Width: Full (mobile), Auto (desktop)
- Height: 52px
- Background: Primary color
- Color: White
- Font size: 16px
- Font weight: 600
- Border-radius: 8px
- Disabled: If form invalid or submitting
- Loading state: Show spinner

**Input Styling:**
- Height: 48px (text inputs)
- Border: 1px solid #D1D5DB
- Border-radius: 8px
- Padding: 12px 16px
- Font size: 16px
- Focus: Border color primary, outline offset

**Error States:**
- Border: Red
- Show error message below input
- Font size: 13px
- Color: #EF4444 (Red)
- Icon: ⚠️

**Success State:**
```
┌─────────────────────────────────────┐
│  ✅                                  │
│  Message Sent Successfully!         │
│  We'll get back to you within 24h.  │
│  [Back to Home]                     │
└─────────────────────────────────────┘
```

**Container:**
- Max-width: 600px
- Margin: 0 auto
- Padding: 40px 20px (mobile), 60px 40px (desktop)
- Background: White
- Border: 1px solid #E5E7EB (optional)
- Border-radius: 16px (optional)

---

### Block 05: Alternative Contact Methods
```
┌─────────────────────────────────────┐
│  [H3: Other Ways to Reach Us]       │
│                                     │
│  [Social Icon] [Social Icon] [Icon] │
│  LinkedIn     Twitter       Discord │
│                                     │
└─────────────────────────────────────┘
```

**Social Links:**
- LinkedIn: `https://www.linkedin.com/company/delphi-ai`
- Twitter/X: `https://twitter.com/delphi_ai`
- Discord/Community: (if applicable)

**Icon Styling:**
- Size: 48px × 48px
- Border: 1px solid #E5E7EB
- Border-radius: 50%
- Color: Secondary text
- Hover: Color brand color, border brand color
- Gap: 16px

**Container:**
- Text align: Center
- Padding: 40px 20px
- Border-top: 1px solid #E5E7EB

---

### Block 06: FAQ Section (Optional)
```
┌─────────────────────────────────────┐
│  [H3: Frequently Asked Questions]   │
│                                     │
│  [Accordion Item 1] ▼               │
│  [Accordion Item 2] ▼               │
│  ...                                │
│                                     │
│  [View All FAQs →]                  │
│                                     │
└─────────────────────────────────────┘
```

**Questions:**
- How do I reset my password?
- What are your support hours?
- Do you offer refunds?
- How can I upgrade my plan?

**Link:** "View All FAQs" → `/faq` or `docs.delphi.ai/faq`

---

### Block 07: Live Chat Widget (Optional)
- **Position:** Bottom right corner
- **Icon:** Chat bubble, 56px × 56px
- **Color:** Primary
- **Shadow:** Prominent
- **Click:** Opens chat widget
- **Platforms:** Intercom, Drift, Crisp, etc.
- **Behavior:**
  - Show unread count badge
  - Pulse animation to draw attention
  - Hide on small screens (optional)

---

### Block 08: Footer
*(Same as Homepage)*

---

## Form Validation

### Client-Side Validation
- **Real-time:** Validate on blur
- **Final:** Validate on submit
- **Clear errors:** On focus/input

### Server-Side Validation
- Sanitize inputs
- Validate email format
- Check for spam (reCAPTCHA optional)
- Rate limiting: Max 3 submissions per hour per email

### Error Messages
- **Empty field:** "This field is required"
- **Invalid email:** "Please enter a valid email address"
- **Message too short:** "Message must be at least 10 characters"
- **Generic error:** "Something went wrong. Please try again."

---

## Form Submission

### Flow
1. User fills form
2. Click "Send Message"
3. Validate form
4. Show loading state (disable button, show spinner)
5. POST to `/api/contact` or email service
6. Show success message OR error message
7. Clear form (on success) OR keep data (on error)

### API Endpoint
```
POST /api/contact
Body:
{
  "name": "John Doe",
  "email": "john@example.com",
  "subject": "General Inquiry",
  "message": "...",
  "consent": true
}

Success Response:
{
  "success": true,
  "message": "Message sent successfully"
}

Error Response:
{
  "success": false,
  "error": "Invalid email address"
}
```

### Email Service
- Use SendGrid, Mailgun, or AWS SES
- Send to: support@delphi.ai or sales@delphi.ai
- Auto-reply: Thank user, set expectations (24h response)
- Notification: Alert team in Slack/Email

---

## Accessibility

- All form fields have labels (visible or aria-label)
- Error messages associated with inputs (aria-describedby)
- Required fields marked (aria-required)
- Focus indicators visible
- Keyboard navigation (Tab, Enter)
- Screen reader friendly error announcements

---

## SEO

**Title:** "Contact Us | Delphi - Get in Touch"
**Description:** "Have questions? Get in touch with Delphi. Contact sales, support, or partnerships. We're here to help."
**Canonical:** `https://www.delphi.ai/contact`
**Robots:** Index, follow

---

## Conversion Optimization

- **Multiple contact methods:** Email, form, chat, social
- **Fast response promise:** "We'll reply within 24 hours"
- **Trust signals:** "We respect your privacy"
- **Low friction:** Minimal required fields
- **Mobile optimized:** Large touch targets, easy to type

---

**End of Contact Page Template**

---

## 🎨 Image Assets

### OG Images
- **UA:** `/public/images/og/[PAGE_SLUG]-og-ua.png` (1200×630px)
- **EN:** `/public/images/og/[PAGE_SLUG]-og-en.png` (1200×630px)

### Twitter Cards
- **UA:** `/public/images/twitter/[PAGE_SLUG]-twitter-ua.png` (1200×630px)
- **EN:** `/public/images/twitter/[PAGE_SLUG]-twitter-en.png` (1200×630px)

---

## 📝 Content Maintenance

### Update Frequency
- **Monthly:** [MONTHLY_UPDATE_ITEMS]
- **Quarterly:** [QUARTERLY_UPDATE_ITEMS]
- **On-Demand:** [ON_DEMAND_TRIGGERS]

### Monitoring
- Track: [KPI_LIST]
- Tools: Google Search Console, Analytics, Lighthouse

---
