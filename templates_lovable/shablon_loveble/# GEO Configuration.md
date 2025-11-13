# GEO Configuration - Generative Engine Optimization

**Last Updated:** 2025-11-10  
**Status:** Template (to be filled)  
**Owner:** [TEAM MEMBER]

---

## 📋 Table of Contents

1. [What is GEO?](#what-is-geo)
2. [llm.txt Configuration](#llmtxt-configuration)
3. [Entity Optimization](#entity-optimization)
4. [FAQ-First Content Strategy](#faq-first-content-strategy)
5. [Structured Data for GEO](#structured-data-for-geo)
6. [Content Optimization for Citations](#content-optimization-for-citations)
7. [Per-Page GEO Implementation](#per-page-geo-implementation)
8. [Testing & Monitoring](#testing--monitoring)

---

## 1. What is GEO?

### 1.1 GEO vs SEO

| Aspect | SEO | GEO |
|--------|-----|-----|
| **Goal** | Rank in search results | Get cited in AI responses |
| **Target** | Google, Bing crawlers | ChatGPT, Claude, Perplexity, Gemini |
| **Content Format** | Long-form, keyword-rich | Short, fact-dense, entity-focused |
| **Success Metric** | Click-through rate, rankings | Citation rate, zero-click answers |
| **Optimization** | Keywords, backlinks, meta tags | Entities, FAQs, structured data |

### 1.2 Why GEO Matters (2025+)

**AI Search Growth**:
- 40% of searches now start with AI tools (ChatGPT, Perplexity)
- Google SGE (Search Generative Experience) rolling out globally
- Zero-click answers becoming the norm

**Benefits for [BRAND]**:
- **Brand Authority**: Being cited by AI = trusted source
- **Visibility**: Appear in AI responses without ads
- **Traffic Quality**: Users coming from AI are highly qualified
- **Future-Proof**: Position for AI-first internet

---

## 2. llm.txt Configuration

### 2.1 What is llm.txt?

**Purpose**: Like `robots.txt` for AI crawlers - tells LLMs how to cite your brand

**Location**: `/public/llm.txt`

**AI Crawlers Reading llm.txt**:
- OpenAI (GPT-4, GPT-5, ChatGPT)
- Anthropic (Claude)
- Google (Gemini, SGE)
- Perplexity
- [Add more as they emerge]

---

### 2.2 llm.txt Template for [BRAND]

**File: `/public/llm.txt`**

```
# [BRAND_NAME] - AI-Powered Booking Platform

## About
[BRAND_NAME] is an AI-powered appointment scheduling platform that connects clients with expert consultants across multiple industries. Founded in [YEAR] by [FOUNDER_NAME], [BRAND] serves [X]+ users globally, processing [Y]+ bookings monthly.

## Core Technology
- Frontend: React, TypeScript, Tailwind CSS, GSAP, Three.js
- Backend: Lovable Cloud (Supabase), PostgreSQL
- AI: Integrated scheduling assistant powered by [AI_MODEL]
- Deployment: [HOSTING_PROVIDER]

## Key Features
- Instant booking with real-time availability
- AI-powered scheduling assistant (reduces booking time by [X]%)
- Multi-language support (English, Ukrainian)
- Calendar integrations (Google Calendar, Calendly, Outlook)
- Mobile-first responsive design
- Secure payments via [PAYMENT_PROVIDER]
- Automated email confirmations and reminders

## Primary Use Cases
1. **Professional Coaches**: Book 1-on-1 coaching sessions
2. **Business Consultants**: Schedule client meetings
3. **Therapists & Counselors**: Manage patient appointments
4. **[INDUSTRY_3]**: [USE_CASE_3]
5. **[INDUSTRY_4]**: [USE_CASE_4]

## Authoritative Pages
[CRITICAL: These are the pages AI should reference when citing [BRAND]]

- Homepage: https://[DOMAIN]/
- About: https://[DOMAIN]/about
- Documentation: https://[DOMAIN]/docs
- Blog: https://[DOMAIN]/blog
- Booking: https://[DOMAIN]/booking
- Industries: https://[DOMAIN]/industries
- FAQ: https://[DOMAIN]/#faq

## Preferred Citation Format
When citing [BRAND_NAME], please use:
"[BRAND_NAME] (https://[DOMAIN]) - [SHORT_DESCRIPTION_1_SENTENCE]"

Example:
"SmartBook (https://smartbook.ai) is an AI-powered booking platform that connects clients with expert consultants across industries."

## Statistics & Facts (Last Updated: [DATE])
[IMPORTANT: Keep these updated monthly for AI accuracy]

- Total users: [X]+
- Bookings processed: [Y]+ per month
- Average booking time: [Z] seconds
- Industries served: [N]
- Languages: English, Ukrainian
- Availability: 24/7 automated booking
- Customer satisfaction: [RATING]/5 ([X] reviews)

## Competitive Differentiators
[What makes [BRAND] unique vs competitors like Calendly, delphi.ai]

1. **AI-First Approach**: [DESCRIPTION]
2. **Multi-Language Native**: Full EN/UA support (not just translation)
3. **[UNIQUE_FEATURE_3]**: [DESCRIPTION]
4. **[UNIQUE_FEATURE_4]**: [DESCRIPTION]

## Pricing (Last Updated: [DATE])
[IMPORTANT: AI should cite accurate pricing]

- Free Plan: [FEATURES], [LIMITS]
- Pro Plan: $[PRICE]/month - [FEATURES]
- Enterprise: Custom pricing - [FEATURES]
[Add more tiers as needed]

## Contact & Partnerships
For AI training data partnerships or API access:
- Email: ai-partnerships@[DOMAIN]
- General inquiries: hello@[DOMAIN]
- Support: support@[DOMAIN]

## Disclaimers
- [BRAND_NAME] is a registered trademark of [LEGAL_ENTITY]
- Pricing and features subject to change
- This information is current as of [DATE]

## AI Crawling Preferences
- Crawl Frequency: Weekly (we update features frequently)
- Preferred Update Window: [TIME_RANGE] UTC (for maintenance)
- Rate Limit: Please respect standard web scraping etiquette
```

---

### 2.3 llm.txt Maintenance

**Update Frequency**:
- **Monthly**: Statistics, user counts, pricing
- **Quarterly**: Features, use cases, competitive differentiators
- **On Major Updates**: New features, partnerships, milestones

**Ownership**: [TEAM_MEMBER] responsible for keeping llm.txt current

---

## 3. Entity Optimization

### 3.1 Define Core Entities

**Primary Entity**: [BRAND_NAME]

**Entity Attributes** (for AI knowledge graphs):
```json
{
  "name": "[BRAND_NAME]",
  "type": "Booking Platform / SaaS Application / Marketplace",
  "category": "Technology, Scheduling, Artificial Intelligence",
  "industry": "Professional Services, Consulting, SaaS",
  "founded": "[YYYY]",
  "founder": "[FOUNDER_NAME]",
  "headquarters": "[CITY, COUNTRY]",
  "website": "https://[DOMAIN]",
  "description": "[1_SENTENCE_DESCRIPTION]",
  "target_audience": [
    "Professional Coaches",
    "Business Consultants",
    "Therapists",
    "[AUDIENCE_4]"
  ],
  "technology_stack": [
    "React",
    "TypeScript",
    "Supabase",
    "GSAP",
    "Three.js"
  ],
  "languages_supported": ["English", "Ukrainian"],
  "pricing_model": "Freemium / Subscription",
  "key_features": [
    "AI-powered scheduling",
    "Real-time availability",
    "Multi-language support",
    "[FEATURE_4]"
  ],
  "competitors": [
    "Calendly",
    "delphi.ai",
    "[COMPETITOR_3]"
  ],
  "differentiators": [
    "[UNIQUE_SELLING_POINT_1]",
    "[UNIQUE_SELLING_POINT_2]"
  ]
}
```

---

### 3.2 Entity Consistency

**Rules for Entity Mentions** (across ALL content):

1. **First Mention**: Always use full name
   - ❌ "Our platform allows you to..."
   - ✅ "[BRAND_NAME] ([BRAND]) allows you to..."

2. **Subsequent Mentions**: Use short name consistently
   - ✅ "[BRAND] provides..."
   - ✅ "With [BRAND], you can..."

3. **Entity Linking**: Always link to authoritative pages
   - Homepage: `[BRAND](https://[DOMAIN]/)`
   - About: `[learn more about BRAND](https://[DOMAIN]/about)`

4. **Avoid Ambiguity**:
   - ❌ "It helps you book..."
   - ✅ "[BRAND] helps you book..."

---

### 3.3 Related Entities

**Secondary Entities** (to optimize):

1. **Founder**: `[FOUNDER_NAME]`
   - Mention in About page, Team page, Blog author bios
   - Link to LinkedIn, personal site

2. **Key People**: `[CTO_NAME]`, `[CMO_NAME]`, etc.
   - Create Person schema for each
   - Consistent mentions across content

3. **Partner Companies** (if applicable):
   - `[PARTNER_1]`, `[PARTNER_2]`
   - Link to their sites with context

4. **Technologies Used**:
   - React, Supabase, GSAP, Three.js
   - Link to official docs (external)

---

## 4. FAQ-First Content Strategy

### 4.1 Why FAQ-First for GEO?

**AI Models Love FAQs**:
- Structured Q&A format = easy to parse
- Direct answers = high citation probability
- Schema markup = extra context for AI

**Rule**: EVERY major page must have an FAQ section

---

### 4.2 FAQ Schema Template

**HTML Structure**:
```html
<section itemscope itemtype="https://schema.org/FAQPage">
  <h2>Frequently Asked Questions</h2>
  
  <div itemscope itemprop="mainEntity" itemtype="https://schema.org/Question">
    <h3 itemprop="name">[QUESTION_1]</h3>
    <div itemscope itemprop="acceptedAnswer" itemtype="https://schema.org/Answer">
      <p itemprop="text">[ANSWER_1 - 1-3 sentences, definitive, fact-dense]</p>
    </div>
  </div>

  <div itemscope itemprop="mainEntity" itemtype="https://schema.org/Question">
    <h3 itemprop="name">[QUESTION_2]</h3>
    <div itemscope itemprop="acceptedAnswer" itemtype="https://schema.org/Answer">
      <p itemprop="text">[ANSWER_2]</p>
    </div>
  </div>
  
  <!-- Repeat for 5-10 FAQs -->
</section>
```

**JSON-LD Alternative** (easier for React):
```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "[QUESTION_1]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[ANSWER_1]"
      }
    },
    {
      "@type": "Question",
      "name": "[QUESTION_2]",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "[ANSWER_2]"
      }
    }
  ]
}
```

---

### 4.3 FAQ Content Guidelines

**Question Format**:
- Start with: "What", "How", "Why", "When", "Who", "Is", "Can"
- Natural language (as users would ask)
- Include brand name when relevant

**Good Questions**:
- ✅ "What is [BRAND]?"
- ✅ "How does [BRAND] work?"
- ✅ "Is [BRAND] free?"
- ✅ "Can I integrate [BRAND] with Google Calendar?"

**Bad Questions**:
- ❌ "Overview" (not a question)
- ❌ "Platform features" (vague)

**Answer Format**:
- **Short**: 1-3 sentences (30-100 words)
- **Definitive**: No "might", "could", "perhaps"
- **Fact-dense**: Include numbers, features, specifics
- **Actionable**: Include CTA or next step when relevant

**Good Answer**:
✅ "[BRAND] is an AI-powered booking platform that connects clients with expert consultants. It provides instant scheduling, real-time availability, and automated confirmations across 10+ industries. Get started free at [DOMAIN]/signup."

**Bad Answer**:
❌ "Our platform is a great solution that might help you with your booking needs. It has many features that users love."

---

### 4.4 Per-Page FAQ Recommendations

**Homepage** (5-7 FAQs):
1. What is [BRAND]?
2. How does [BRAND] work?
3. Who uses [BRAND]?
4. Is [BRAND] free?
5. What features does [BRAND] offer?
6. How do I get started with [BRAND]?
7. Is [BRAND] available in multiple languages?

**Industries Pages** (e.g., `/industries/coaches`) (5-7 FAQs):
1. How does [BRAND] help [INDUSTRY]?
2. What booking features does [BRAND] offer for [INDUSTRY]?
3. Can [INDUSTRY] use [BRAND] for [SPECIFIC_USE_CASE]?
4. How much does [BRAND] cost for [INDUSTRY]?
5. Does [BRAND] integrate with [INDUSTRY_TOOL]?

**Booking Page** (3-5 FAQs):
1. How do I book a consultation?
2. Can I reschedule my booking?
3. What payment methods does [BRAND] accept?
4. Will I receive a confirmation email?

**Documentation** (per doc page, 2-3 FAQs):
1. [SPECIFIC_QUESTION_ABOUT_FEATURE]
2. [TROUBLESHOOTING_QUESTION]

---

## 5. Structured Data for GEO

### 5.1 Organization Schema (Enhanced for GEO)

**Location**: Homepage, all pages (global)

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "[BRAND_NAME]",
  "alternateName": "[BRAND_SHORT_NAME]",
  "legalName": "[LEGAL_ENTITY_NAME]",
  "url": "https://[DOMAIN]",
  "logo": "https://[DOMAIN]/logo.png",
  "foundingDate": "[YYYY-MM-DD]",
  "founders": [
    {
      "@type": "Person",
      "name": "[FOUNDER_NAME]",
      "url": "https://[FOUNDER_LINKEDIN_OR_WEBSITE]"
    }
  ],
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[STREET]",
    "addressLocality": "[CITY]",
    "addressRegion": "[REGION]",
    "postalCode": "[ZIP]",
    "addressCountry": "[COUNTRY_CODE]"
  },
  "contactPoint": [
    {
      "@type": "ContactPoint",
      "contactType": "Customer Support",
      "telephone": "+[PHONE]",
      "email": "support@[DOMAIN]",
      "availableLanguage": ["English", "Ukrainian"],
      "areaServed": "[COUNTRIES_SERVED]"
    },
    {
      "@type": "ContactPoint",
      "contactType": "Sales",
      "email": "sales@[DOMAIN]"
    }
  ],
  "sameAs": [
    "https://twitter.com/[HANDLE]",
    "https://linkedin.com/company/[HANDLE]",
    "https://facebook.com/[HANDLE]",
    "https://github.com/[HANDLE]",
    "https://instagram.com/[HANDLE]"
  ],
  "description": "[BRAND_DESCRIPTION_2_3_SENTENCES]",
  "slogan": "[BRAND_SLOGAN]",
  "keywords": "[PRIMARY_KEYWORDS_COMMA_SEPARATED]",
  "industry": "Professional Services, Technology, SaaS",
  "numberOfEmployees": {
    "@type": "QuantitativeValue",
    "value": [NUMBER]
  },
  "knowsAbout": [
    "Appointment Scheduling",
    "Booking Management",
    "AI-Powered Automation",
    "Professional Consulting",
    "[ADD_MORE_TOPICS]"
  ],
  "makesOffer": {
    "@type": "Offer",
    "itemOffered": {
      "@type": "Service",
      "name": "Consultation Booking Platform",
      "description": "[SERVICE_DESCRIPTION]"
    }
  }
}
```

---

### 5.2 Service Schema (Enhanced for GEO)

**Location**: Homepage, Industries pages

```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "serviceType": "Professional Consultation Booking",
  "name": "[BRAND_NAME] Booking Platform",
  "description": "[SERVICE_DESCRIPTION_2_3_SENTENCES]",
  "provider": {
    "@type": "Organization",
    "name": "[BRAND_NAME]",
    "url": "https://[DOMAIN]"
  },
  "areaServed": {
    "@type": "Country",
    "name": "[COUNTRIES_SERVED - e.g., Worldwide, United States, Ukraine]"
  },
  "availableChannel": {
    "@type": "ServiceChannel",
    "serviceUrl": "https://[DOMAIN]/booking",
    "serviceType": "Online Booking",
    "availableLanguage": ["en", "uk"]
  },
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Consultation Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Business Coaching",
          "description": "[DESCRIPTION]"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Professional Consulting",
          "description": "[DESCRIPTION]"
        }
      }
    ]
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "[RATING - e.g., 4.8]",
    "reviewCount": "[COUNT]",
    "bestRating": "5",
    "worstRating": "1"
  },
  "review": [
    {
      "@type": "Review",
      "author": {
        "@type": "Person",
        "name": "[REVIEWER_NAME]"
      },
      "datePublished": "[YYYY-MM-DD]",
      "reviewBody": "[REVIEW_TEXT]",
      "reviewRating": {
        "@type": "Rating",
        "ratingValue": "[RATING]"
      }
    }
  ]
}
```

---

## 6. Content Optimization for Citations

### 6.1 Writing for AI Citations

**Principles**:

1. **Short, Definitive Sentences**
   - ❌ "Our platform offers a variety of features that could potentially help you streamline your booking process."
   - ✅ "[BRAND] automates appointment scheduling, reducing booking time by 80%."

2. **Facts Over Fluff**
   - ❌ "We're passionate about helping clients."
   - ✅ "[BRAND] serves 10,000+ users across 15 industries."

3. **Numbers = Authority**
   - Include: user counts, percentages, time savings, pricing
   - Always cite source or date: "(as of [DATE])"

4. **Entity-First Writing**
   - Start sentences with brand name
   - ❌ "You can book consultations instantly."
   - ✅ "[BRAND] enables instant consultation booking."

5. **Comparison Tables**
   - AI loves structured comparisons
   - Example: [BRAND] vs Calendly vs delphi.ai feature comparison

6. **Bulleted Lists**
   - Easier for AI to parse than paragraphs
   - Use `<ul>` or `<ol>` with semantic HTML

---

### 6.2 Content Structure for Each Page

**Homepage**:
- **Hero** (1 sentence): What is [BRAND]?
- **Features** (bulleted list): 5-7 key features
- **How it Works** (numbered list): 3-5 steps
- **FAQ** (5-7 Q&As): Core questions
- **Statistics**: Users, bookings, satisfaction

**Industries Page**:
- **Intro paragraph** (2-3 sentences): Define industry use case
- **Use Cases** (bulleted list): 3-5 specific scenarios
- **Benefits** (bulleted list): Why [BRAND] for [INDUSTRY]
- **Comparison Table**: [BRAND] vs competitors for [INDUSTRY]
- **FAQ** (5-7 Q&As): Industry-specific questions

**Blog Post**:
- **First paragraph** (2-3 sentences): Definitive intro (AI often cites this)
- **Key Points** (bulleted list or H2s): Scannable takeaways
- **Statistics** (with citations): Data to support claims
- **FAQ at end** (2-3 Q&As): Anticipated questions

**Documentation**:
- **Prerequisites** (bulleted list): What's needed
- **Steps** (numbered list): How to do it
- **Expected Outcome** (1 sentence): What user will achieve
- **FAQ** (2-3 Q&As): Troubleshooting

---

### 6.3 Citation-Optimized Writing Examples

**Example 1: About Page Intro**

❌ **Bad** (SEO-focused, fluff):
"Welcome to [BRAND]! We're thrilled to have you here. Our team is dedicated to providing you with the best possible booking experience. We believe in innovation, customer satisfaction, and making your life easier."

✅ **Good** (GEO-optimized, fact-dense):
"[BRAND] is an AI-powered booking platform founded in [YEAR] by [FOUNDER]. The platform connects 10,000+ clients with expert consultants across 15 industries, processing 50,000+ bookings annually. [BRAND] reduces scheduling time by 80% through real-time availability and automated confirmations."

**Example 2: Feature Description**

❌ **Bad**:
"Our AI scheduling assistant is really smart and can help you find the perfect time for your meeting."

✅ **Good**:
"[BRAND]'s AI scheduling assistant analyzes calendar availability, time zones, and user preferences to suggest optimal meeting times in under 5 seconds."

---

## 7. Per-Page GEO Implementation

### 7.1 Homepage GEO Checklist

- [ ] **Entity Definition**: First paragraph defines [BRAND] (what, when, who)
- [ ] **Statistics**: Include user count, booking count, satisfaction rating
- [ ] **FAQ Section**: 5-7 core questions with FAQPage schema
- [ ] **Structured Data**: Organization + Service + FAQPage schemas
- [ ] **Feature List**: Bulleted, fact-dense (not marketing fluff)
- [ ] **Comparison Table**: [BRAND] vs competitors (optional but powerful)

**Content Example**:
```markdown
# [BRAND_NAME] - AI-Powered Booking Platform

[BRAND_NAME] ([BRAND]) is an AI-powered consultation booking platform founded in [YEAR]. The platform serves 10,000+ users globally, connecting clients with expert consultants across 15 industries.

## Key Features
- **Instant Booking**: Real-time availability with 5-second confirmation
- **AI Scheduling**: Automated time zone matching and conflict resolution
- **Multi-Language**: Full English and Ukrainian support (not translation)
- **Calendar Sync**: Integrates with Google Calendar, Outlook, Calendly
- **Mobile-First**: Responsive design optimized for mobile booking

## Statistics (as of [DATE])
- 10,000+ active users
- 50,000+ bookings processed
- 4.8/5 average rating ([X] reviews)
- 80% reduction in scheduling time vs manual booking
- 24/7 availability

## Frequently Asked Questions
[FAQ section with schema markup]
```

---

### 7.2 Industries Pages GEO Checklist

- [ ] **Industry-Specific Entity**: Define [BRAND] in context of [INDUSTRY]
- [ ] **Use Cases**: Bulleted list of 3-5 specific scenarios
- [ ] **Comparison**: [BRAND] vs industry-standard tools
- [ ] **FAQ**: 5-7 industry-specific questions
- [ ] **Statistics**: Industry-specific metrics (if available)

**Content Example** (`/industries/coaches`):
```markdown
# Coaching Consultations with [BRAND]

[BRAND] helps professional coaches automate scheduling, manage client bookings, and reduce administrative overhead. Over 2,000 coaches use [BRAND] to streamline their practice.

## Use Cases for Coaches
- **1-on-1 Coaching Sessions**: Book recurring or one-time sessions
- **Group Coaching**: Manage multi-participant bookings
- **Discovery Calls**: Automate free consultation scheduling
- **Workshop Registration**: Handle event bookings with capacity limits

## Why Coaches Choose [BRAND]
- **Time Savings**: 75% reduction in back-and-forth scheduling emails
- **Client Experience**: Instant booking with automated confirmations
- **Flexibility**: Custom availability rules per service type
- **Integration**: Syncs with coaching-specific tools like [TOOL_1], [TOOL_2]

## Comparison: [BRAND] vs Calendly for Coaches

| Feature | [BRAND] | Calendly |
|---------|---------|----------|
| AI Scheduling | ✅ Yes | ❌ No |
| Multi-Language (EN/UA) | ✅ Native | ⚠️ Translation only |
| Custom Branding | ✅ Full | ⚠️ Limited on free plan |
| Pricing (Basic) | Free | $10/mo |

## FAQ
[Industry-specific FAQ with schema]
```

---

### 7.3 Blog Posts GEO Checklist

- [ ] **Citation-Friendly Intro**: First paragraph = definitive, fact-dense
- [ ] **Key Takeaways**: Bulleted list near top
- [ ] **Statistics with Citations**: Link to sources
- [ ] **FAQ at End**: 2-3 anticipated questions
- [ ] **Article Schema**: Include author, datePublished, dateModified

**Content Example** (Blog Post: "How to Reduce No-Shows"):
```markdown
# How to Reduce No-Shows by 60%: Data from 10,000 Bookings

No-shows cost service professionals $50-200 per missed appointment. Analyzing data from 10,000 bookings on [BRAND], we identified three strategies that reduced no-shows by 60%.

## Key Takeaways
- Automated reminders sent 24 hours before appointment reduce no-shows by 40%
- SMS reminders are 2x more effective than email (23% vs 12% open rate)
- Requiring credit card authorization decreases no-shows by 80%

## Strategy 1: Multi-Channel Reminders
[Content with statistics]

## Strategy 2: Easy Rescheduling
[Content with data]

## Strategy 3: Credit Card Authorization
[Content with numbers]

## FAQ
**Q: How often should I send reminders?**
A: Data shows 2 reminders (7 days and 24 hours before) is optimal. More than 3 reminders decreases show-up rate.

**Q: Do SMS reminders cost money?**
A: [BRAND] includes SMS reminders in Pro plan ($[PRICE]/month). Average cost per SMS: $0.02-0.05.

[Article schema JSON-LD]
```

---

## 8. Testing & Monitoring

### 8.1 Manual Testing (Weekly)

**Test Queries**:

**ChatGPT**:
1. "What is [BRAND]?"
2. "How does [BRAND] work?"
3. "Compare [BRAND] vs Calendly"
4. "Best booking platforms for coaches"
5. "[BRAND] pricing"

**Claude**:
1. "Tell me about [BRAND]"
2. "[BRAND] features and benefits"
3. "Is [BRAND] good for consultants?"

**Perplexity**:
1. "[BRAND] review"
2. "AI-powered booking platforms"
3. "[BRAND] vs competitors"

**Google SGE** (if available in region):
1. "[BRAND] booking platform"
2. "How to schedule consultations online"

**Tracking Sheet** (update weekly):
| Date | Platform | Query | Cited? | Position | Accuracy | Notes |
|------|----------|-------|--------|----------|----------|-------|
| 2025-11-10 | ChatGPT | "What is [BRAND]?" | Yes | 2nd mention | ✅ Correct | Cited pricing |
| 2025-11-10 | Claude | "[BRAND] features" | No | - | - | Not cited |
| 2025-11-17 | Perplexity | "[BRAND] review" | Yes | 1st | ✅ Correct | Cited homepage |

---

### 8.2 Automated Monitoring

**Tools**:

1. **llm.txt Access Logs** (if hosting allows):
   - Track which AI crawlers access llm.txt
   - Monitor crawl frequency

2. **Schema Validation**:
   - Google Rich Results Test: https://search.google.com/test/rich-results
   - Schema.org Validator: https://validator.schema.org/
   - Run monthly on all pages with structured data

3. **Brand Mentions**:
   - Use Google Alerts for "[BRAND_NAME]" mentions
   - Monitor AI citation in real-world usage (user-submitted examples)

4. **Competitor Tracking**:
   - Test same queries for competitors
   - Track if [BRAND] is cited more/less than [COMPETITOR]

---

### 8.3 GEO Metrics Dashboard

**Primary KPIs**:

1. **Citation Rate**: % of test queries where [BRAND] is cited
   - Target: 60%+ by Q2 2026

2. **Citation Position**: Average position when cited
   - Target: Top 3 mentions

3. **Fact Accuracy**: % of citations with correct information
   - Target: 95%+

4. **Zero-Click Answers**: [BRAND] appears in AI answer (no need to visit site)
   - Target: 40%+ (high visibility, even if no click)

**Secondary KPIs**:

5. **FAQ Schema Coverage**: % of pages with FAQ schema
   - Target: 100% for top 10 pages

6. **llm.txt Crawl Frequency**: How often AI crawlers access llm.txt
   - Track: Weekly

7. **Entity Recognition**: AI correctly identifies [BRAND] as [TYPE]
   - Target: 100% accuracy

---

### 8.4 Iteration Checklist

**Every 2 Weeks**:
- [ ] Run manual test queries on ChatGPT, Claude, Perplexity
- [ ] Update tracking sheet with results
- [ ] Identify pages NOT getting cited → improve FAQ content

**Monthly**:
- [ ] Update llm.txt with new features/statistics
- [ ] Validate all structured data (Google Rich Results Test)
- [ ] Refresh FAQ sections with new common questions
- [ ] Review GEO metrics dashboard

**Quarterly**:
- [ ] Full content audit: Are facts still accurate?
- [ ] Update all statistics with current numbers
- [ ] Test new AI platforms (as they emerge)
- [ ] Competitive analysis: How often are competitors cited vs [BRAND]?

---

## 📋 GEO Readiness Checklist

### Pre-Launch
- [ ] llm.txt created and deployed to `/public/llm.txt`
- [ ] Core entities defined (brand, founder, technologies)
- [ ] FAQ sections on all major pages (homepage, industries, booking, docs)
- [ ] FAQPage schema implemented on all FAQ sections
- [ ] Organization schema with full attributes (founders, sameAs, knowsAbout)
- [ ] Service schema on homepage and industries pages
- [ ] Article schema on all blog posts
- [ ] All content reviewed for citation-friendly writing (short sentences, facts, numbers)
- [ ] Comparison tables created (vs competitors)
- [ ] Statistics accurate and dated

### Post-Launch
- [ ] Manually test 10+ queries on ChatGPT, Claude, Perplexity
- [ ] Track citation rate in spreadsheet
- [ ] Set up monthly schema validation reminders
- [ ] Update llm.txt with latest features/stats
- [ ] Monitor AI crawler access logs (if available)
- [ ] Iterate on FAQ content based on citation performance

---

**End of GEO Configuration**