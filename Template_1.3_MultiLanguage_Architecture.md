# TEMPLATE 1.3: MULTI-LANGUAGE ARCHITECTURE SETUP

## 📋 PURPOSE
This template defines the internationalization (i18n) strategy for your multi-language SaaS website, optimized for Lovable.dev implementation.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Implement Multi-Language Architecture with the following specifications:

## LANGUAGE CONFIGURATION

### Supported Languages
Default Language: _______________
Language Code: _______________ (e.g., en, uk, es)
Language Direction: [LTR/RTL]

Additional Languages:
1. Language: _______________
   Code: _______________
   Direction: [LTR/RTL]
   Priority: [High/Medium/Low]

2. Language: _______________
   Code: _______________
   Direction: [LTR/RTL]
   Priority: [High/Medium/Low]

3. Language: _______________
   Code: _______________
   Direction: [LTR/RTL]
   Priority: [High/Medium/Low]

4. Language: _______________
   Code: _______________
   Direction: [LTR/RTL]
   Priority: [High/Medium/Low]

5. Language: _______________
   Code: _______________
   Direction: [LTR/RTL]
   Priority: [High/Medium/Low]

Total Languages: _______________

## TECHNICAL APPROACH

### Implementation Strategy
Preferred Method: [Select One]
- [ ] Client-side routing (React Router with language prefix)
- [ ] Path-based routing (/en/, /uk/, /es/)
- [ ] Subdomain routing (en.domain.com, uk.domain.com)
- [ ] Cookie-based language detection
- [ ] Browser language auto-detection with manual override

Rationale for choice: _______________

### URL Structure
Language in URL: [Yes/No]
URL Pattern: [domain.com/en/page OR en.domain.com/page OR domain.com/page?lang=en]

Examples:
- Default language URL: _______________
- Secondary language URL: _______________

Hide default language from URL: [Yes/No]

### Language Detection Logic
Priority Order:
1. _______________
2. _______________
3. _______________
4. _______________

Example: [User selection > URL parameter > Cookie > Browser setting > Default]

Auto-redirect on first visit: [Yes/No]
Remember user language choice: [Yes/No/Session only]
Storage method: [localStorage/Cookie/URL parameter]

## TRANSLATION MANAGEMENT

### Translation File Structure
File Organization: [Select One]
- [ ] Single file per language (e.g., /src/i18n/en.json, /src/i18n/uk.json)
- [ ] Nested by feature (e.g., /src/i18n/en/homepage.json, /src/i18n/en/pricing.json)
- [ ] Component-colocated translations

File Format: [JSON/TypeScript/YAML]

### Translation Keys Structure
Naming Convention: [Select One]
- [ ] Flat structure (e.g., "homepage_hero_title")
- [ ] Nested structure (e.g., "homepage.hero.title")
- [ ] Feature-based (e.g., "features.ai_chat.description")

Translation Key Examples:
- Page titles: _______________
- Navigation items: _______________
- Button labels: _______________
- Form fields: _______________
- Error messages: _______________

### Content Categories to Translate

Static Content:
- [ ] Navigation menu items
- [ ] Page titles and headings
- [ ] Body content and descriptions
- [ ] Button labels and CTAs
- [ ] Form labels and placeholders
- [ ] Error messages and validation
- [ ] Toast notifications
- [ ] Footer content

Dynamic Content:
- [ ] Blog posts/articles
- [ ] User-generated content
- [ ] Product descriptions
- [ ] FAQ items
- [ ] Testimonials
- [ ] Case studies

Meta Content (SEO):
- [ ] Meta titles
- [ ] Meta descriptions
- [ ] OG tags (Open Graph)
- [ ] Schema markup
- [ ] Alt text for images
- [ ] hreflang tags

## LANGUAGE SWITCHER COMPONENT

### Visual Design
Location: _______________
Display Type: [Dropdown/Flags/Text/Combined]
Icon/Flag Display: [Yes/No]
Current Language Indicator: _______________

Desktop Layout:
- Position: _______________
- Style: _______________

Mobile Layout:
- Position: _______________
- Style: _______________

### Switcher Behavior
On Language Change:
- [ ] Reload page with new language
- [ ] Update content without reload (SPA)
- [ ] Redirect to equivalent page in new language
- [ ] Stay on current page if translation unavailable
- [ ] Redirect to homepage if page not translated

Persist Selection: [Yes/No]
Method: [Cookie/localStorage/URL]

Animation: [Yes/No]
Transition Type: _______________

### Accessibility
ARIA Labels: [Yes/No]
Keyboard Navigation: [Yes/No]
Screen Reader Support: [Yes/No]
Language Names: [Display in native language/English/Both]

Example Display:
- English → English / English
- Українська → Українська / Ukrainian
- Español → Español / Spanish

## CONTENT FALLBACK STRATEGY

### Missing Translation Handling
When translation is missing:
- [ ] Show default language
- [ ] Show translation key
- [ ] Show placeholder text
- [ ] Log missing translations for review
- [ ] Hide element completely

Fallback Language: _______________

### Partial Translation Support
Allow partial translations: [Yes/No]
Mix of translated/untranslated content: [Yes/No]
Visual indicator for untranslated content: [Yes/No]

## RTL (Right-to-Left) SUPPORT

RTL Languages in Project: [Yes/No]

If Yes:
Languages with RTL: _______________

Layout Mirroring:
- [ ] Automatic layout flip
- [ ] Manual RTL stylesheets
- [ ] Tailwind RTL plugin

RTL-specific Design Considerations:
_______________________________________________

## SEO OPTIMIZATION FOR MULTI-LANGUAGE

### Hreflang Implementation
Implement hreflang tags: [Yes/No]
Method: [HTML tags/XML sitemap/Both]

Example hreflang structure:
```html
<link rel="alternate" hreflang="en" href="https://domain.com/en/page" />
<link rel="alternate" hreflang="uk" href="https://domain.com/uk/page" />
<link rel="alternate" hreflang="x-default" href="https://domain.com/en/page" />
```

### Language-Specific SEO
Separate meta tags per language: [Yes/No]
Separate sitemaps per language: [Yes/No]
Separate robots.txt: [Yes/No]

Canonical URL Strategy:
_______________________________________________

### Structured Data (Schema)
Translate schema markup: [Yes/No]
Implement InLanguage property: [Yes/No]

## DATE, TIME, AND NUMBER FORMATTING

### Localization Settings
Date Format per Language:
- Default: _______________
- Secondary: _______________

Time Format: [12-hour/24-hour/Based on locale]

Number Format:
- Decimal separator: _______________
- Thousands separator: _______________

Currency Display:
- Primary currency: _______________
- Show currency symbols: [Yes/No]
- Format: _______________

### Timezone Handling
Display timezone: [Yes/No]
Default timezone: _______________
User timezone detection: [Yes/No]

## TRANSLATION WORKFLOW

### Content Update Process
Who provides translations: _______________
Translation review process: _______________
Update frequency: _______________

Translation Tools: [Select if applicable]
- [ ] Manual translation files
- [ ] Translation management system (TMS)
- [ ] Integration with translation service
- [ ] AI-assisted translation with review

Quality Assurance:
- [ ] Native speaker review
- [ ] Context screenshots for translators
- [ ] Character limit guidelines
- [ ] Brand voice guidelines per language

### Version Control
How translations are versioned: _______________
Deployment strategy: _______________

## PERFORMANCE OPTIMIZATION

### Loading Strategy
Translation Files: [Select One]
- [ ] Load all translations on initial load
- [ ] Lazy load by language
- [ ] Code split by route and language
- [ ] Load on language switch

Optimize for: _______________

### Caching Strategy
Cache translations: [Yes/No]
Cache duration: _______________
Update mechanism: _______________

## COMPONENT LIBRARY INTEGRATION

shadcn/ui Components Translation:
- [ ] Translate built-in component labels
- [ ] Error messages
- [ ] Validation messages
- [ ] Aria labels

## USER PREFERENCES

### Language Selection Storage
Store in: [localStorage/Cookie/User account]
Cookie name: _______________
Cookie duration: _______________
GDPR compliance: [Yes/No]

### User Account Integration
Store language preference in database: [Yes/No]
Sync across devices: [Yes/No]
Override browser language: [Yes/No]

## TESTING REQUIREMENTS

Test Coverage:
- [ ] All languages render correctly
- [ ] Language switcher works on all pages
- [ ] URLs follow correct pattern
- [ ] RTL layouts display properly (if applicable)
- [ ] Date/time/numbers format correctly
- [ ] No untranslated strings visible
- [ ] SEO tags present for all languages
- [ ] Navigation between languages works
- [ ] Forms work in all languages

Translation Quality Checks:
- [ ] No truncated text
- [ ] Proper character encoding
- [ ] No broken layouts due to text length
- [ ] Culturally appropriate content
- [ ] Correct terminology for industry

## DEVELOPMENT GUIDELINES

Code Implementation:
1. Use i18n library compatible with React (e.g., react-i18next, react-intl)
2. Never hardcode user-facing strings in components
3. All text content must use translation keys
4. Provide context in translation keys for clarity
5. Use interpolation for dynamic content
6. Handle pluralization correctly per language
7. Extract translations early in development
8. Test with longer translations (e.g., German, Russian)

Component Pattern Example:
```tsx
import { useTranslation } from 'react-i18next';

const Component = () => {
  const { t } = useTranslation();
  return <h1>{t('homepage.hero.title')}</h1>;
};
```

## LAUNCH CHECKLIST

Pre-Launch Verification:
- [ ] All translations complete and reviewed
- [ ] Language switcher functional on all pages
- [ ] URLs follow specified pattern
- [ ] hreflang tags implemented correctly
- [ ] Separate sitemaps generated per language
- [ ] Meta tags translated for all pages
- [ ] No console errors related to i18n
- [ ] Performance tested with all languages
- [ ] Mobile responsive with all languages
- [ ] Analytics tracking language selection
- [ ] 404 pages translated
- [ ] Legal pages (Privacy, Terms) translated

## MAINTENANCE PLAN

Regular Tasks:
- Review missing translations: _______________
- Update translations for new features: _______________
- Quality check: _______________
- Performance monitoring: _______________

Expansion Plan:
Future languages to add: _______________
Timeline: _______________
Resources needed: _______________

## NOTES & SPECIAL REQUIREMENTS
_______________________________________________
_______________________________________________
_______________________________________________
```

---

## ✅ IMPLEMENTATION PROMPT FOR LOVABLE

After filling this template:

```
Implement Multi-Language Architecture based on the completed specification.

CONTEXT: I have defined a comprehensive multi-language strategy with [NUMBER] supported languages using [CHOSEN STRATEGY] approach.

TASK:
1. Install and configure i18n library (react-i18next recommended)
2. Create translation file structure in /src/i18n/
3. Implement language switcher component with specified design
4. Set up routing with language prefixes (if path-based)
5. Configure language detection and persistence logic
6. Create translation hook for components
7. Set up language-specific meta tags and SEO
8. Implement hreflang tags
9. Configure date/time/number formatting per locale
10. Handle RTL layouts (if applicable)

GUIDELINES:
- Never hardcode user-facing strings
- Use semantic translation keys with context
- Mobile-first responsive language switcher
- Ensure accessibility (ARIA labels, keyboard navigation)
- Test with longest possible translations
- Implement loading states during language switch
- Handle missing translations gracefully

CONSTRAINTS:
- Must work with existing design system
- Performance: lazy load translations per route
- SEO: proper hreflang and meta tag implementation
- Accessibility: WCAG 2.1 AA compliance

[Paste your filled multi-language template here]

EXPECTED DELIVERABLES:
1. Functional language switcher in navigation
2. All static content using translation keys
3. Language-specific routing working
4. SEO tags implemented for all languages
5. Date/time formatting per locale
6. Fallback mechanism for missing translations
7. Documentation of translation key structure
```

---

## 📝 USAGE INSTRUCTIONS

1. **Choose implementation strategy carefully** - path-based is recommended for SEO
2. **Plan translation keys structure** before development
3. **Coordinate with translation team** on workflow
4. **Test with actual translated content** not lorem ipsum
5. **Verify SEO implementation** with Google Search Console
6. **Document translation process** for team

---

## ⚠️ CRITICAL REMINDERS

- Path-based routing (/en/, /uk/) is best for SEO
- Never serve untranslated content in production
- Test layouts with languages that have longer text (German, Russian)
- Implement hreflang correctly to avoid SEO issues
- Consider regional variations (en-US vs en-GB)
- Budget time for translation QA and cultural adaptation
- Use professional translators for launch languages
- Keep translation keys organized and well-documented
