# Homepage Template - Technical Specification

**Page Type:** Landing Page
**URL Pattern:** `/` (homepage)
**Priority:** Critical
**Approach:** Mobile First
**Last Updated:** November 12, 2025

---

## 🌐 i18n Configuration

### Languages
- **Default Language:** UA (Українська)
- **Available Languages:** EN (English), UA (Українська)
- **Language Selector:** Yes (Header, top-right corner)
- **RTL Support:** No

### URL Structure
- **UA (Default):** `https://[DOMAIN]/`
- **EN:** `https://[DOMAIN]/en/`
- **Pattern:** `/{locale?}/` where locale is optional (defaults to UA)

### Content Keys Structure (JSON)
```json
{
  "ua": {
    "navigation": {
      "explore": "[NAVIGATION_EXPLORE_UA]",
      "pricing": "[NAVIGATION_PRICING_UA]",
      "about": "[NAVIGATION_ABOUT_UA]",
      "docs": "[NAVIGATION_DOCS_UA]",
      "signIn": "[NAVIGATION_SIGNIN_UA]",
      "getStarted": "[NAVIGATION_GETSTARTED_UA]"
    },
    "hero": {
      "badge": "[HERO_BADGE_UA]",
      "title": "[HERO_TITLE_UA]",
      "description": "[HERO_DESCRIPTION_UA]",
      "cta": {
        "primary": "[HERO_CTA_PRIMARY_UA]",
        "secondary": "[HERO_CTA_SECONDARY_UA]"
      },
      "socialProof": "[HERO_SOCIAL_PROOF_UA]",
      "microDetails": [
        "[MICRO_DETAIL_1_UA]",
        "[MICRO_DETAIL_2_UA]",
        "[MICRO_DETAIL_3_UA]"
      ]
    },
    "features": {
      "eyebrow": "[FEATURES_EYEBROW_UA]",
      "heading": "[FEATURES_HEADING_UA]",
      "description": "[FEATURES_DESCRIPTION_UA]",
      "cards": [
        {
          "title": "[FEATURE_1_TITLE_UA]",
          "description": "[FEATURE_1_DESC_UA]"
        },
        {
          "title": "[FEATURE_2_TITLE_UA]",
          "description": "[FEATURE_2_DESC_UA]"
        },
        {
          "title": "[FEATURE_3_TITLE_UA]",
          "description": "[FEATURE_3_DESC_UA]"
        }
      ]
    },
    "howItWorks": {
      "heading": "[HOW_IT_WORKS_HEADING_UA]",
      "steps": [
        {
          "title": "[STEP_1_TITLE_UA]",
          "description": "[STEP_1_DESC_UA]"
        },
        {
          "title": "[STEP_2_TITLE_UA]",
          "description": "[STEP_2_DESC_UA]"
        },
        {
          "title": "[STEP_3_TITLE_UA]",
          "description": "[STEP_3_DESC_UA]"
        }
      ]
    },
    "testimonials": {
      "heading": "[TESTIMONIALS_HEADING_UA]",
      "subheading": "[TESTIMONIALS_SUBHEADING_UA]"
    },
    "cta": {
      "heading": "[FINAL_CTA_HEADING_UA]",
      "description": "[FINAL_CTA_DESCRIPTION_UA]",
      "button": "[FINAL_CTA_BUTTON_UA]",
      "link": "[FINAL_CTA_LINK_UA]"
    },
    "footer": {
      "tagline": "[FOOTER_TAGLINE_UA]",
      "copyright": "[FOOTER_COPYRIGHT_UA]"
    }
  },
  "en": {
    "navigation": {
      "explore": "[NAVIGATION_EXPLORE_EN]",
      "pricing": "[NAVIGATION_PRICING_EN]",
      "about": "[NAVIGATION_ABOUT_EN]",
      "docs": "[NAVIGATION_DOCS_EN]",
      "signIn": "[NAVIGATION_SIGNIN_EN]",
      "getStarted": "[NAVIGATION_GETSTARTED_EN]"
    },
    "hero": {
      "badge": "[HERO_BADGE_EN]",
      "title": "[HERO_TITLE_EN]",
      "description": "[HERO_DESCRIPTION_EN]",
      "cta": {
        "primary": "[HERO_CTA_PRIMARY_EN]",
        "secondary": "[HERO_CTA_SECONDARY_EN]"
      },
      "socialProof": "[HERO_SOCIAL_PROOF_EN]",
      "microDetails": [
        "[MICRO_DETAIL_1_EN]",
        "[MICRO_DETAIL_2_EN]",
        "[MICRO_DETAIL_3_EN]"
      ]
    },
    "features": {
      "eyebrow": "[FEATURES_EYEBROW_EN]",
      "heading": "[FEATURES_HEADING_EN]",
      "description": "[FEATURES_DESCRIPTION_EN]",
      "cards": [
        {
          "title": "[FEATURE_1_TITLE_EN]",
          "description": "[FEATURE_1_DESC_EN]"
        },
        {
          "title": "[FEATURE_2_TITLE_EN]",
          "description": "[FEATURE_2_DESC_EN]"
        },
        {
          "title": "[FEATURE_3_TITLE_EN]",
          "description": "[FEATURE_3_DESC_EN]"
        }
      ]
    },
    "howItWorks": {
      "heading": "[HOW_IT_WORKS_HEADING_EN]",
      "steps": [
        {
          "title": "[STEP_1_TITLE_EN]",
          "description": "[STEP_1_DESC_EN]"
        },
        {
          "title": "[STEP_2_TITLE_EN]",
          "description": "[STEP_2_DESC_EN]"
        },
        {
          "title": "[STEP_3_TITLE_EN]",
          "description": "[STEP_3_DESC_EN]"
        }
      ]
    },
    "testimonials": {
      "heading": "[TESTIMONIALS_HEADING_EN]",
      "subheading": "[TESTIMONIALS_SUBHEADING_EN]"
    },
    "cta": {
      "heading": "[FINAL_CTA_HEADING_EN]",
      "description": "[FINAL_CTA_DESCRIPTION_EN]",
      "button": "[FINAL_CTA_BUTTON_EN]",
      "link": "[FINAL_CTA_LINK_EN]"
    },
    "footer": {
      "tagline": "[FOOTER_TAGLINE_EN]",
      "copyright": "[FOOTER_COPYRIGHT_EN]"
    }
  }
}
```

---

## 🔍 SEO Configuration

### Meta Tags (HTML Head)

#### Ukrainian Version (Default)
```html
<!-- Primary Meta Tags -->
<title>[BRAND_NAME] - [BRAND_TAGLINE_UA] | [INDUSTRY_UA]</title>
<meta name="title" content="[BRAND_NAME] - [BRAND_TAGLINE_UA] | [INDUSTRY_UA]" />
<meta name="description" content="[META_DESCRIPTION_UA]" />
<meta name="keywords" content="[PRIMARY_KEYWORD_UA], [SECONDARY_KEYWORD_UA], [LONG_TAIL_KEYWORD_UA]" />
<meta name="theme-color" content="[THEME_COLOR_HEX]" />
<meta name="robots" content="index, follow" />
<link rel="canonical" href="https://[DOMAIN]/" />

<!-- Favicon & Icons -->
<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png" />
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png" />
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png" />
<link rel="manifest" href="/site.webmanifest" />
```

#### English Version
```html
<!-- Primary Meta Tags -->
<title>[BRAND_NAME] - [BRAND_TAGLINE_EN] | [INDUSTRY_EN]</title>
<meta name="title" content="[BRAND_NAME] - [BRAND_TAGLINE_EN] | [INDUSTRY_EN]" />
<meta name="description" content="[META_DESCRIPTION_EN]" />
<meta name="keywords" content="[PRIMARY_KEYWORD_EN], [SECONDARY_KEYWORD_EN], [LONG_TAIL_KEYWORD_EN]" />
<meta name="theme-color" content="[THEME_COLOR_HEX]" />
<meta name="robots" content="index, follow" />
<link rel="canonical" href="https://[DOMAIN]/en/" />
```

### Open Graph Tags

#### Ukrainian Version
```html
<!-- Open Graph / Facebook -->
<meta property="og:type" content="website" />
<meta property="og:url" content="https://[DOMAIN]/" />
<meta property="og:title" content="[BRAND_NAME] - [BRAND_TAGLINE_UA]" />
<meta property="og:description" content="[OG_DESCRIPTION_UA]" />
<meta property="og:image" content="https://[DOMAIN]/images/og/homepage-og-ua.png" />
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />
<meta property="og:locale" content="uk_UA" />
<meta property="og:locale:alternate" content="en_US" />
<meta property="og:site_name" content="[BRAND_NAME]" />
```

#### English Version
```html
<!-- Open Graph / Facebook -->
<meta property="og:type" content="website" />
<meta property="og:url" content="https://[DOMAIN]/en/" />
<meta property="og:title" content="[BRAND_NAME] - [BRAND_TAGLINE_EN]" />
<meta property="og:description" content="[OG_DESCRIPTION_EN]" />
<meta property="og:image" content="https://[DOMAIN]/images/og/homepage-og-en.png" />
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />
<meta property="og:locale" content="en_US" />
<meta property="og:locale:alternate" content="uk_UA" />
<meta property="og:site_name" content="[BRAND_NAME]" />
```

### Twitter Card Tags

#### Ukrainian Version
```html
<!-- Twitter -->
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:url" content="https://[DOMAIN]/" />
<meta name="twitter:title" content="[BRAND_NAME] - [BRAND_TAGLINE_UA]" />
<meta name="twitter:description" content="[TWITTER_DESCRIPTION_UA]" />
<meta name="twitter:image" content="https://[DOMAIN]/images/twitter/homepage-twitter-ua.png" />
<meta name="twitter:creator" content="[TWITTER_HANDLE]" />
<meta name="twitter:site" content="[TWITTER_HANDLE]" />
```

#### English Version
```html
<!-- Twitter -->
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:url" content="https://[DOMAIN]/en/" />
<meta name="twitter:title" content="[BRAND_NAME] - [BRAND_TAGLINE_EN]" />
<meta name="twitter:description" content="[TWITTER_DESCRIPTION_EN]" />
<meta name="twitter:image" content="https://[DOMAIN]/images/twitter/homepage-twitter-en.png" />
<meta name="twitter:creator" content="[TWITTER_HANDLE]" />
<meta name="twitter:site" content="[TWITTER_HANDLE]" />
```

### Hreflang Tags
```html
<!-- Language Alternates -->
<link rel="alternate" hreflang="uk" href="https://[DOMAIN]/" />
<link rel="alternate" hreflang="en" href="https://[DOMAIN]/en/" />
<link rel="alternate" hreflang="x-default" href="https://[DOMAIN]/" />
```

### Additional SEO Elements
```html
<!-- Preconnect for Performance -->
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />

<!-- DNS Prefetch -->
<link rel="dns-prefetch" href="https://www.google-analytics.com" />
```

---

## 🤖 GEO Configuration (Generative Engine Optimization)

### Primary Entity Definition

**Entity Name:** [BRAND_NAME]
**Entity Type:** [ENTITY_TYPE] (e.g., SaaS Platform, Service Provider, Technology Company)
**Category:** [INDUSTRY_CATEGORY]
**Founded:** [FOUNDING_DATE]
**Founders:** [FOUNDER_NAME_1], [FOUNDER_NAME_2]
**Headquarters:** [CITY], [COUNTRY]
**Website:** https://[DOMAIN]
**Description:** [ENTITY_DESCRIPTION_100_WORDS]

### Secondary Entities

**Key Personnel:**
- [PERSON_1_NAME] - [PERSON_1_ROLE]
- [PERSON_2_NAME] - [PERSON_2_ROLE]
- [PERSON_3_NAME] - [PERSON_3_ROLE]

**Technologies Used:**
- [TECHNOLOGY_1] - [TECHNOLOGY_1_PURPOSE]
- [TECHNOLOGY_2] - [TECHNOLOGY_2_PURPOSE]
- [TECHNOLOGY_3] - [TECHNOLOGY_3_PURPOSE]

**Partner Companies:**
- [PARTNER_1_NAME]
- [PARTNER_2_NAME]
- [PARTNER_3_NAME]

### Entity Mention Rules

**First Mention:** Use full brand name with descriptor
- Example UA: "[BRAND_NAME] — [DESCRIPTOR_UA]"
- Example EN: "[BRAND_NAME] — [DESCRIPTOR_EN]"

**Subsequent Mentions:** Use short form consistently
- Example: "[BRAND_NAME]" або "[SHORT_NAME]"

### FAQ Schema (FAQPage) - Homepage

**Questions for Homepage (Ukrainian):**

1. **Що таке [BRAND_NAME]?**
   - Answer (30-100 words): [FAQ_ANSWER_1_UA]

2. **Як працює [BRAND_NAME]?**
   - Answer: [FAQ_ANSWER_2_UA]

3. **Хто користується [BRAND_NAME]?**
   - Answer: [FAQ_ANSWER_3_UA]

4. **Які тарифні плани пропонує [BRAND_NAME]?**
   - Answer: [FAQ_ANSWER_4_UA]

5. **Які ключові функції [BRAND_NAME]?**
   - Answer: [FAQ_ANSWER_5_UA]

6. **Як почати роботу з [BRAND_NAME]?**
   - Answer: [FAQ_ANSWER_6_UA]

7. **Які мови підтримує [BRAND_NAME]?**
   - Answer: [FAQ_ANSWER_7_UA]

**Questions for Homepage (English):**

1. **What is [BRAND_NAME]?**
   - Answer: [FAQ_ANSWER_1_EN]

2. **How does [BRAND_NAME] work?**
   - Answer: [FAQ_ANSWER_2_EN]

3. **Who uses [BRAND_NAME]?**
   - Answer: [FAQ_ANSWER_3_EN]

4. **What pricing plans does [BRAND_NAME] offer?**
   - Answer: [FAQ_ANSWER_4_EN]

5. **What are the key features of [BRAND_NAME]?**
   - Answer: [FAQ_ANSWER_5_EN]

6. **How do I get started with [BRAND_NAME]?**
   - Answer: [FAQ_ANSWER_6_EN]

7. **What languages does [BRAND_NAME] support?**
   - Answer: [FAQ_ANSWER_7_EN]

### llm.txt Content (for AI Citations)

**Location:** `/public/llm.txt`

**Content Structure:**
```
# [BRAND_NAME] - AI Citation Guide

## Brand Overview
[BRAND_NAME] is [DESCRIPTION_1_SENTENCE].

Founded: [FOUNDING_DATE]
Founders: [FOUNDER_NAMES]
Headquarters: [LOCATION]
Industry: [INDUSTRY]

## Core Technology
- Platform: [TECH_STACK]
- Languages: [PROGRAMMING_LANGUAGES]
- Infrastructure: [INFRASTRUCTURE]

## Key Features
1. [FEATURE_1_NAME]: [FEATURE_1_DESCRIPTION]
2. [FEATURE_2_NAME]: [FEATURE_2_DESCRIPTION]
3. [FEATURE_3_NAME]: [FEATURE_3_DESCRIPTION]

## Use Cases
- [USE_CASE_1]
- [USE_CASE_2]
- [USE_CASE_3]

## Authoritative Pages
- Homepage: https://[DOMAIN]/
- Documentation: https://[DOMAIN]/docs
- Pricing: https://[DOMAIN]/pricing
- Blog: https://[DOMAIN]/blog

## Preferred Citation Format
"[BRAND_NAME] ([YEAR]) is [DESCRIPTION]. Available at: https://[DOMAIN]"

## Statistics (Updated: [UPDATE_DATE])
- Users: [USER_COUNT]
- Countries: [COUNTRY_COUNT]
- Uptime: [UPTIME_PERCENTAGE]%

## Competitive Differentiators
- [DIFFERENTIATOR_1]
- [DIFFERENTIATOR_2]
- [DIFFERENTIATOR_3]

## Pricing
- Free Tier: [FREE_TIER_DETAILS]
- Paid Plans: Starting at [STARTING_PRICE]/month
- Enterprise: Custom pricing

## Contact
- Email: [CONTACT_EMAIL]
- Partnerships: [PARTNERSHIPS_EMAIL]
- Support: [SUPPORT_URL]
```

---

## 📊 Structured Data (Schema.org JSON-LD)

### Organization Schema

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "[BRAND_NAME]",
  "legalName": "[LEGAL_NAME]",
  "alternateName": "[ALTERNATE_NAME]",
  "url": "https://[DOMAIN]",
  "logo": "https://[DOMAIN]/images/logo.png",
  "foundingDate": "[FOUNDING_DATE]",
  "founders": [
    {
      "@type": "Person",
      "name": "[FOUNDER_1_NAME]"
    },
    {
      "@type": "Person",
      "name": "[FOUNDER_2_NAME]"
    }
  ],
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[STREET_ADDRESS]",
    "addressLocality": "[CITY]",
    "addressRegion": "[REGION]",
    "postalCode": "[POSTAL_CODE]",
    "addressCountry": "[COUNTRY_CODE]"
  },
  "contactPoint": [
    {
      "@type": "ContactPoint",
      "telephone": "[PHONE_NUMBER]",
      "contactType": "customer support",
      "availableLanguage": ["Ukrainian", "English"],
      "areaServed": "[AREA_SERVED]"
    },
    {
      "@type": "ContactPoint",
      "email": "[CONTACT_EMAIL]",
      "contactType": "sales",
      "availableLanguage": ["Ukrainian", "English"]
    }
  ],
  "sameAs": [
    "[LINKEDIN_URL]",
    "[TWITTER_URL]",
    "[FACEBOOK_URL]",
    "[INSTAGRAM_URL]"
  ],
  "description": "[ORGANIZATION_DESCRIPTION]",
  "slogan": "[BRAND_TAGLINE]",
  "numberOfEmployees": {
    "@type": "QuantitativeValue",
    "value": "[EMPLOYEE_COUNT]"
  },
  "serviceArea": {
    "@type": "GeoCircle",
    "geoMidpoint": {
      "@type": "GeoCoordinates",
      "latitude": "[LATITUDE]",
      "longitude": "[LONGITUDE]"
    }
  },
  "keywords": "[PRIMARY_KEYWORD], [SECONDARY_KEYWORD], [TERTIARY_KEYWORD]",
  "knowsLanguage": ["uk", "en"]
}
```

### Website Schema

```json
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "name": "[BRAND_NAME]",
  "url": "https://[DOMAIN]",
  "potentialAction": {
    "@type": "SearchAction",
    "target": {
      "@type": "EntryPoint",
      "urlTemplate": "https://[DOMAIN]/search?q={search_term_string}"
    },
    "query-input": "required name=search_term_string"
  },
  "inLanguage": ["uk", "en"]
}
```

### FAQPage Schema (Homepage)

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "[FAQ_QUESTION_1_UA]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[FAQ_ANSWER_1_UA]"
      }
    },
    {
      "@type": "Question",
      "name": "[FAQ_QUESTION_2_UA]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[FAQ_ANSWER_2_UA]"
      }
    },
    {
      "@type": "Question",
      "name": "[FAQ_QUESTION_3_UA]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[FAQ_ANSWER_3_UA]"
      }
    },
    {
      "@type": "Question",
      "name": "[FAQ_QUESTION_4_UA]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[FAQ_ANSWER_4_UA]"
      }
    },
    {
      "@type": "Question",
      "name": "[FAQ_QUESTION_5_UA]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[FAQ_ANSWER_5_UA]"
      }
    },
    {
      "@type": "Question",
      "name": "[FAQ_QUESTION_6_UA]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[FAQ_ANSWER_6_UA]"
      }
    },
    {
      "@type": "Question",
      "name": "[FAQ_QUESTION_7_UA]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[FAQ_ANSWER_7_UA]"
      }
    }
  ]
}
```

### Service Schema

```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "serviceType": "[SERVICE_TYPE]",
  "provider": {
    "@type": "Organization",
    "name": "[BRAND_NAME]",
    "url": "https://[DOMAIN]"
  },
  "areaServed": {
    "@type": "Country",
    "name": "[COUNTRY_NAME]"
  },
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "[BRAND_NAME] Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "[SERVICE_1_NAME]",
          "description": "[SERVICE_1_DESCRIPTION]"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "[SERVICE_2_NAME]",
          "description": "[SERVICE_2_DESCRIPTION]"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "[SERVICE_3_NAME]",
          "description": "[SERVICE_3_DESCRIPTION]"
        }
      }
    ]
  },
  "availableChannel": {
    "@type": "ServiceChannel",
    "serviceUrl": "https://[DOMAIN]",
    "servicePhone": "[PHONE_NUMBER]",
    "availableLanguage": ["Ukrainian", "English"]
  }
}
```

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

## 🎨 Image Assets Requirements

### OG Images (Open Graph)

**Ukrainian Version:**
- **File:** `/public/images/og/homepage-og-ua.png`
- **Dimensions:** 1200px × 630px
- **Format:** PNG or JPG
- **File Size:** < 300KB
- **Content:** Brand name, tagline in Ukrainian, visual element
- **Alt Text (UA):** "[BRAND_NAME] - [TAGLINE_UA]"

**English Version:**
- **File:** `/public/images/og/homepage-og-en.png`
- **Dimensions:** 1200px × 630px
- **Format:** PNG or JPG
- **File Size:** < 300KB
- **Content:** Brand name, tagline in English, visual element
- **Alt Text (EN):** "[BRAND_NAME] - [TAGLINE_EN]"

### Twitter Card Images

**Ukrainian Version:**
- **File:** `/public/images/twitter/homepage-twitter-ua.png`
- **Dimensions:** 1200px × 630px
- **Format:** PNG or JPG
- **File Size:** < 300KB

**English Version:**
- **File:** `/public/images/twitter/homepage-twitter-en.png`
- **Dimensions:** 1200px × 630px
- **Format:** PNG or JPG
- **File Size:** < 300KB

### Favicon Set
- **32×32px:** `/public/favicon-32x32.png`
- **16×16px:** `/public/favicon-16x16.png`
- **180×180px (Apple Touch):** `/public/apple-touch-icon.png`
- **Manifest:** `/public/site.webmanifest`
- **Format:** PNG with transparency
- **Background:** Transparent or brand color

### Hero Section Images
- **Hero Image/Video:** `/public/images/hero/homepage-hero.jpg` or `.mp4`
- **Dimensions Image:** 1920px × 1080px (16:9 aspect ratio)
- **Dimensions Video:** 1920px × 1080px, max 5MB
- **Alt Text (UA):** "[HERO_IMAGE_ALT_UA]"
- **Alt Text (EN):** "[HERO_IMAGE_ALT_EN]"

### Logo Assets
- **Main Logo:** `/public/images/logo/logo.svg` (vector)
- **Logo PNG:** `/public/images/logo/logo.png` (transparent background)
- **Logo Dark:** `/public/images/logo/logo-dark.svg` (for light backgrounds)
- **Logo Light:** `/public/images/logo/logo-light.svg` (for dark backgrounds)
- **Dimensions:** Multiple sizes (120×32px for header, 140×36px for footer)

### Feature Icons
- **Location:** `/public/images/icons/`
- **Format:** SVG (preferred) or PNG
- **Size:** 64px × 64px
- **Style:** Outlined or filled (consistent across all)
- **Color:** Primary brand color or customizable via CSS

### Screenshot Images (How It Works section)
- **Step 1 Screenshot:** `/public/images/screenshots/step-1.png`
- **Step 2 Screenshot:** `/public/images/screenshots/step-2.png`
- **Step 3 Screenshot:** `/public/images/screenshots/step-3.png`
- **Dimensions:** 1000px × 600px (16:10 aspect ratio)
- **Format:** PNG or JPG
- **Compression:** 80% quality

### Testimonial Avatars
- **Location:** `/public/images/avatars/`
- **Format:** JPG or PNG
- **Size:** 96px × 96px (will be displayed at 48px)
- **Shape:** Square (will be cropped to circle via CSS)
- **File naming:** `[person-name]-avatar.jpg`

### Logo Strip (Partner/Client Logos)
- **Location:** `/public/images/partners/`
- **Format:** SVG (preferred) or PNG with transparency
- **Size:** 160px × 80px (2:1 aspect ratio)
- **Style:** Greyscale
- **Opacity:** 60% default, 100% on hover

---

## 📝 Content Maintenance Schedule

### Monthly Updates (Every 1st of the month)

**Statistics in llm.txt:**
- [ ] User count update
- [ ] Countries served update
- [ ] Uptime percentage
- [ ] New features count

**Homepage Content:**
- [ ] Update "Trusted by X+ experts" number if changed
- [ ] Review and update testimonials if new ones available
- [ ] Check all links are working

**Meta Tags:**
- [ ] Verify OG images still accessible
- [ ] Check canonical URLs
- [ ] Ensure hreflang tags are correct

### Quarterly Updates (Every 3 months)

**llm.txt Content:**
- [ ] Competitive differentiators review
- [ ] Use cases update
- [ ] Feature list update
- [ ] Pricing structure review

**Structured Data:**
- [ ] Organization schema: Verify all information current
- [ ] FAQ schema: Update with new common questions
- [ ] Service schema: Add new services if applicable

**Content Review:**
- [ ] Hero section: Evaluate headline effectiveness
- [ ] Features: Add/remove/update based on product changes
- [ ] Testimonials: Rotate or add fresh testimonials
- [ ] Use cases: Update based on customer feedback

### On-Demand Updates (As needed)

**Trigger Events:**
- New product launch → Update features, llm.txt
- Pricing changes → Update pricing teaser, meta descriptions
- Rebranding → Update all brand mentions, logos, colors
- New partnership → Update partner logos, mentions
- Major milestone → Update statistics, hero section
- Language expansion → Add new hreflang tags, content versions
- SEO strategy change → Update keywords, meta descriptions

**Process:**
1. Identify what changed
2. Update content.json files (UA and EN)
3. Regenerate structured data if needed
4. Update llm.txt if applicable
5. Test all language versions
6. Verify meta tags and OG images
7. Submit updated sitemap to search engines

### Content Ownership

**Responsible Team/Person:** [CONTENT_OWNER_NAME]
**Backup Contact:** [BACKUP_CONTACT_NAME]
**Review Frequency:** Monthly for critical, Quarterly for standard

### Monitoring & Validation

**Tools to Use:**
- Google Search Console (indexation, errors)
- Google Analytics (traffic, conversions)
- Structured Data Testing Tool (schema validation)
- Lighthouse (performance, SEO, accessibility)
- Broken Link Checker (monthly)

**KPIs to Track:**
- Organic traffic (month over month)
- Conversion rate (homepage → signup)
- Bounce rate
- Time on page
- CTA click-through rate
- Language distribution (UA vs EN visitors)

---

## Version History

**v2.0** - November 12, 2025
- Added i18n configuration (UA/EN support)
- Added comprehensive SEO configuration
- Added GEO (Generative Engine Optimization)
- Added structured data schemas
- Added image assets requirements
- Added content maintenance schedule
- Mobile-first approach maintained

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
