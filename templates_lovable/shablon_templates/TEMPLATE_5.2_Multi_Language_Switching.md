# TEMPLATE 5.2: MULTI-LANGUAGE SWITCHING LOGIC

## 📋 PURPOSE
This template defines the complete internationalization (i18n) system, language detection, switching logic, and content translation management for your multi-language SaaS application.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Implement Multi-language System based on the following specification:

## INTERNATIONALIZATION CONFIGURATION

i18n Library: [react-i18next / next-i18next / Format.js / Custom]
Translation Format: [JSON / YAML / PO / Custom]

Supported Languages:

Total Languages: _______________

Language 1:
- Language Code: _______________ (e.g., en, uk, es)
- Language Name (Native): _______________ (e.g., English, Українська)
- Language Name (English): _______________
- Default Language: [Yes/No]
- RTL Support: [Yes/No]
- Locale Code: _______________ (e.g., en-US, uk-UA)
- Fallback Language: _______________

Language 2:
- Language Code: _______________
- Language Name (Native): _______________
- Language Name (English): _______________
- Default Language: [No]
- RTL Support: [Yes/No]
- Locale Code: _______________
- Fallback Language: _______________

Language 3:
[Repeat structure...]

[Continue for all languages...]

Default/Fallback Language: _______________
Translation Fallback Strategy: [Fallback to default / Show key / Show placeholder]

## LANGUAGE DETECTION STRATEGY

Detection Priority Order:

Priority 1: [User selection / URL parameter / Cookie / Browser / Geo IP]
Priority 2: _______________
Priority 3: _______________
Priority 4: _______________
Priority 5: _______________

### User Selection

User Language Preference:
- Stored In: [User profile / Cookie / Local storage / Session storage]
- Cookie Name: _______________
- Cookie Duration: _______________ days
- Override All Other Detection: [Yes/No]

Authenticated Users:
- Store in Database: [Yes/No]
- Database Field: _______________
- Sync Across Devices: [Yes/No]

### URL-Based Language Detection

URL Structure: [Subdomain / Path prefix / Query parameter / Cookie only]

If Subdomain:
- Pattern: [lang].domain.com
- Examples:
  * en.domain.com
  * uk.domain.com
  * es.domain.com
- Default Subdomain: _______________ (e.g., www or no subdomain)

If Path Prefix:
- Pattern: domain.com/[lang]/[page]
- Examples:
  * domain.com/en/features
  * domain.com/uk/features
  * domain.com/es/features
- Root URL Behavior: [Redirect to default / Show language selector]
- Canonical URL: [Include language / Language-neutral]

If Query Parameter:
- Parameter Name: _______________ (e.g., ?lang=uk)
- Override Cookie: [Yes/No]

URL Management:
- Include Language in All URLs: [Yes/No]
- Default Language in URL: [Yes / No - omit]
- 301 Redirect Wrong Language: [Yes/No]

### Browser Language Detection

Use Browser Accept-Language: [Yes/No]

Browser Detection Settings:
- Match Exactly: [Yes/No]
- Match Language Only (ignore region): [Yes/No]
- Priority: [First match / Best match / Weighted]
- Remember Choice: [Yes/No]

Examples:
- Browser sends "uk-UA, en-US" → Show: _______________
- Browser sends "pl-PL" (not supported) → Show: _______________

### Geo-IP Based Detection

Use Geo-IP: [Yes/No]

If Yes:
- Geo-IP Provider: [Cloudflare / MaxMind / ipapi / Custom]
- Fallback if Detection Fails: _______________

Country-to-Language Mapping:
- Ukraine → Ukrainian (uk)
- USA → English (en)
- Poland → Polish (pl)
- UK → English (en)
- Spain → Spanish (es)
- [Add all relevant mappings...]

Override User Choice: [Never / First visit only / Always suggest]

## LANGUAGE SWITCHER UI

### Switcher Component Configuration

Switcher Type: [Dropdown / Flags / Text links / Modal / Slide-out]

Desktop Switcher:
- Position: [Header right / Header left / Footer / Both]
- Display Format: [Language name / Flag + name / Flag only / Code]
- Current Language Indicator: [Bold / Checkmark / Highlight / None]

Mobile Switcher:
- Position: [Header / Footer / Mobile menu / Separate button]
- Display Format: [Same as desktop / Simplified]

Switcher Content:

Language Option 1: _______________
- Display Text: _______________ (e.g., "English", "EN", "🇬🇧 English")
- Flag Icon: [Yes/No] _______________
- Active State: _______________

Language Option 2: _______________
[Repeat structure...]

Language Option 3: _______________
[Repeat structure...]

[Continue for all languages...]

Switcher Behavior:
- Dropdown Opens On: [Hover / Click]
- Close On: [Click outside / Select language / Manual close]
- Search/Filter: [Yes/No] (for many languages)
- Group Languages: [By region / Alphabetically / By popularity]

Flag Icons:
- Use Flags: [Yes/No]
- Icon Library: [Emoji flags / SVG / Icon library]
- Accessibility: [Country name in alt text / ARIA labels]

### Switcher Styling

Appearance:
- Style: [Minimal / Bordered / Filled / Custom]
- Size: [Small / Medium / Large]
- Icon Size: _______________
- Font Size: _______________

Current Language Display:
- Show Flag: [Yes/No]
- Show Code: [Yes/No]
- Show Full Name: [Yes/No]
- Dropdown Icon: [Chevron down / Globe / Other]

Dropdown Menu:
- Max Height: _______________ (before scroll)
- Width: [Auto / Fixed width]
- Animation: [Fade / Slide / None]
- Shadow: _______________
- Border: _______________

Active Language:
- Highlight Color: _______________
- Checkmark: [Yes/No]
- Different Font Weight: [Yes/No]

## LANGUAGE SWITCHING BEHAVIOR

### Switching Action

On Language Selection:

Step 1: Update User Preference
- Update Cookie: [Yes/No]
- Update Local Storage: [Yes/No]
- Update Database (if logged in): [Yes/No]
- Update URL: [Yes/No]

Step 2: Page Behavior
- Reload Page: [Yes/No]
- Soft Reload (SPA): [Yes/No]
- Redirect to Equivalent Page: [Yes/No]
- Stay on Current Page: [Yes/No]

Step 3: URL Update
- Update URL Path: [Yes/No]
- Update URL Query: [Yes/No]
- History State: [Push new state / Replace state]

Step 4: Content Update
- Immediate Translation: [Yes/No]
- Show Loading State: [Yes/No]
- Smooth Transition: [Fade / None]

Preserve State:
- Form Data: [Yes/No]
- Scroll Position: [Yes/No]
- Modal/Dialog State: [Yes/No]
- Filters/Selections: [Yes/No]

### Page-Specific Behavior

Homepage:
- Redirect to Localized Version: [Yes/No]
- Show Language Selector First Visit: [Yes/No]

Product/Feature Pages:
- Redirect to Equivalent: [Yes/No]
- Fallback if Translation Missing: [Show default language / Show 404]

Blog Posts:
- Switch Language: [Only if translated / Show original / Redirect to blog home]

Dynamic Content:
- User-Generated Content: [Don't translate / Auto-translate / Show original]

## CONTENT TRANSLATION MANAGEMENT

### Translation File Structure

File Organization: [By page / By feature / By namespace / Flat]

If By Namespace:
- common.json (shared translations)
- auth.json (authentication pages)
- dashboard.json
- pricing.json
- features.json
- errors.json
- emails.json
- [Other namespaces...]

Translation File Format:

```json
{
  "key": "Translation",
  "nested": {
    "key": "Translation"
  },
  "interpolation": "Hello {{name}}",
  "plural": "{{count}} item_one",
  "plural_other": "{{count}} items"
}
```

File Locations:
- Translation Files Path: _______________ (e.g., /locales/[lang]/[namespace].json)
- Public Access: [Yes/No]

### Translation Keys

Key Naming Convention: [dot.notation / snake_case / camelCase]
Examples:
- common.header.login
- auth_signup_button_text
- dashboardWelcomeMessage

Key Structure Best Practices:
- Namespace First: [Yes/No]
- Group by Feature: [Yes/No]
- Descriptive Keys: [Yes/No]

Translation Variables:
- Variable Syntax: {{variable}} or {variable} or %{variable}
- Common Variables:
  * {{name}} - User name
  * {{count}} - Numbers for pluralization
  * {{date}} - Formatted dates
  * {{email}} - Email addresses
  * Other: _______________

### Pluralization

Pluralization Support: [Yes/No]

If Yes:
- Pluralization Rules: [By language / ICU format / Custom]
- Example Structure:
  ```json
  {
    "items": {
      "zero": "No items",
      "one": "{{count}} item",
      "other": "{{count}} items"
    }
  }
  ```

Languages with Complex Plurals:
- Ukrainian: [zero, one, few, many, other]
- Polish: [zero, one, few, many, other]
- [Add others if applicable...]

### Date, Time, and Number Formatting

Use Locale-Specific Formatting: [Yes/No]

Date Formatting:
- Library: [Intl.DateTimeFormat / date-fns / Moment.js / Day.js]
- Format Pattern: _______________ (e.g., DD/MM/YYYY vs MM/DD/YYYY)
- Locale Support: [Automatic / Manual per language]

Examples:
- English (US): 12/31/2024
- Ukrainian: 31.12.2024
- ISO Format: 2024-12-31

Time Formatting:
- Format: [12-hour / 24-hour / Based on locale]
- Examples:
  * English (US): 3:30 PM
  * Ukrainian: 15:30

Number Formatting:
- Thousands Separator: [Comma / Space / Period / Locale-based]
- Decimal Separator: [Period / Comma / Locale-based]
- Examples:
  * English: 1,234.56
  * Ukrainian: 1 234,56
  * German: 1.234,56

Currency Formatting:
- Format: [Symbol + amount / Amount + symbol / Locale-based]
- Examples:
  * USD: $1,234.56
  * EUR: €1.234,56
  * UAH: 1 234,56 ₴

### RTL (Right-to-Left) Support

RTL Languages Supported: [Yes/No]

If Yes:

RTL Languages:
- [ ] Arabic (ar)
- [ ] Hebrew (he)
- [ ] Persian (fa)
- [ ] Urdu (ur)
- [ ] Other: _______________

RTL Implementation:
- Automatic Direction: [Yes/No]
- CSS Direction: [dir="rtl" / CSS logical properties]
- Mirror Layout: [Yes/No]
- Flip Icons: [Yes/No]

RTL Exceptions:
- Numbers: [LTR / RTL]
- URLs: [LTR / RTL]
- Code Blocks: [LTR / RTL]
- Dates: [LTR / RTL]

### Translation Workflow

Translation Management: [Manual files / Translation management system]

If Translation Management System:
- Platform: [Lokalise / Crowdin / Phrase / POEditor / Custom]
- API Integration: [Yes/No]
- Auto-sync: [Yes/No]

Translation Sources:
- Professional Translation: [Yes/No]
- Machine Translation: [Yes/No]
- Community Translation: [Yes/No]

Translation Quality:
- Review Process: [Yes/No]
- Quality Check: [Automated / Manual]
- Proofreading: [Yes/No]

Missing Translation Handling:
- Show Translation Key: [Yes/No]
- Show Fallback Language: [Yes/No]
- Show Placeholder: [Yes/No]
- Log Missing Keys: [Yes/No]
- Alert Developer: [Yes/No]

## TRANSLATED CONTENT SCOPE

### Application UI

Translate:
- [ ] Navigation menu
- [ ] Buttons and CTAs
- [ ] Form labels and placeholders
- [ ] Error messages
- [ ] Success messages
- [ ] Tooltips
- [ ] Modal content
- [ ] Loading states
- [ ] Empty states
- [ ] Footer links

### Marketing Pages

Translate:
- [ ] Homepage
- [ ] Features pages
- [ ] Pricing page
- [ ] About us
- [ ] Use cases
- [ ] FAQ
- [ ] Blog posts
- [ ] Landing pages

### Product Content

Translate:
- [ ] Dashboard
- [ ] Settings pages
- [ ] Help documentation
- [ ] Onboarding flow
- [ ] Email templates
- [ ] Notifications
- [ ] Chat messages

### Legal Pages

Translate:
- [ ] Privacy Policy
- [ ] Terms of Service
- [ ] Cookie Policy
- [ ] GDPR/CCPA notices

Legal Translation Approach:
- Professional Translation Required: [Yes/No]
- Legal Review Per Language: [Yes/No]
- Version Tracking: [Yes/No]

### Email Templates

Email Translation:
- [ ] Welcome emails
- [ ] Verification emails
- [ ] Password reset
- [ ] Notifications
- [ ] Marketing emails
- [ ] Transactional emails

Email Language Selection:
- Use User Preference: [Yes/No]
- Fallback: _______________

### Dynamic Content

User-Generated Content:
- Translation: [Auto-translate / Show original / Don't translate]
- Auto-translation Provider: [Google Translate API / DeepL / Other]
- Show Original Option: [Yes/No]

### SEO Content

Translate SEO Elements:
- [ ] Page titles
- [ ] Meta descriptions
- [ ] Alt text
- [ ] Open Graph tags
- [ ] Structured data

SEO Configuration:
- Hreflang Tags: [Yes/No]
- Language-Specific Sitemaps: [Yes/No]
- Localized URLs: [Yes/No]

## LANGUAGE PREFERENCE PERSISTENCE

### Storage Methods

Storage Options Used:

Cookie:
- Cookie Name: _______________
- Duration: _______________ days
- Scope: [Domain / Subdomain]
- Secure: [Yes/No]
- SameSite: [Strict / Lax / None]

Local Storage:
- Key Name: _______________
- Sync Across Tabs: [Yes/No]

Session Storage:
- Key Name: _______________
- Lifetime: [Session only]

Database (Authenticated Users):
- User Table Field: _______________
- Default Value: _______________
- Sync on Login: [Yes/No]

### Cross-Device Sync

Logged In Users:
- Sync Language Preference: [Yes/No]
- Priority: [Database / Local]
- Update on Change: [Immediate / On session]

Anonymous Users:
- Cross-Device Sync: [No - not possible]
- Rely On: [Cookie / Local storage]

## SEO OPTIMIZATION

### Language-Specific SEO

Hreflang Implementation:
- Add Hreflang Tags: [Yes/No]
- Format: [HTML tag / Sitemap / Both]
- X-Default Tag: [Yes/No]
- X-Default Points To: _______________

Example:
```html
<link rel="alternate" hreflang="en" href="https://example.com/en/page" />
<link rel="alternate" hreflang="uk" href="https://example.com/uk/page" />
<link rel="alternate" hreflang="x-default" href="https://example.com/en/page" />
```

Sitemap:
- Separate Sitemaps Per Language: [Yes/No]
- Language in URLs: [Yes/No]
- Update Frequency: _______________

Canonical URLs:
- Self-Referencing Canonical: [Yes/No]
- Cross-Language Canonical: [No]

Content Duplication:
- Handling Strategy: [Hreflang tags / Separate domains / Language folders]

### Search Engine Indexing

Indexing Per Language:
- Allow All Languages: [Yes/No]
- Robots.txt Per Language: [No - shared]
- Meta Robots: [All pages indexed]

Google Search Console:
- Separate Property Per Language: [Optional]
- International Targeting: [Yes/No]

## LANGUAGE SWITCHER ANALYTICS

Track Language Interactions:

Events to Track:
- [ ] Language switcher opened
- [ ] Language selected
- [ ] Language changed
- [ ] Default language assigned
- [ ] Browser language detected
- [ ] Geo-IP language suggested

Event Properties:
- From Language: _______________
- To Language: _______________
- Detection Method: _______________
- Page URL: _______________
- User Authenticated: [Yes/No]

Conversion Tracking:
- Track Conversion by Language: [Yes/No]
- Segment Users by Language: [Yes/No]

## PERFORMANCE OPTIMIZATION

### Translation Loading

Loading Strategy:
- Load All Languages: [No - too heavy]
- Load Current Language Only: [Yes/No]
- Lazy Load Namespaces: [Yes/No]
- Preload Key Namespaces: [Yes/No]

Translation Bundle:
- Bundle Size Target: _______________ KB per language
- Code Splitting: [Yes/No]
- Caching Strategy: [Service Worker / CDN / Browser cache]
- Cache Duration: _______________

Loading States:
- Show Loading Skeleton: [Yes/No]
- Fallback to Default Language: [Yes/No]
- Partial Translation Rendering: [Yes/No]

### Caching Strategy

Translation Cache:
- Client-Side Cache: [Yes/No]
- Cache Duration: _______________
- Invalidation Strategy: [Version-based / Time-based]

CDN Delivery:
- Serve Translations from CDN: [Yes/No]
- CDN Provider: _______________

## TESTING & QUALITY ASSURANCE

### Translation Testing

Test Coverage:

- [ ] All UI elements translated
- [ ] No missing translation keys
- [ ] Pluralization works correctly
- [ ] Date/time formatting correct
- [ ] Number formatting correct
- [ ] Currency formatting correct
- [ ] RTL layout (if applicable)
- [ ] Text overflow handled
- [ ] Mobile responsive
- [ ] Email templates
- [ ] Error messages

Testing Tools:
- i18n Testing Library: [Yes/No]
- Visual Regression Testing: [Yes/No]
- Translation Coverage Reports: [Yes/No]

### Text Expansion Handling

Text Expansion Accommodation:
- UI Elements Support Expansion: [Yes/No]
- Expansion Factor: _______________ (e.g., 1.3x for German)
- Ellipsis for Overflow: [Yes/No]
- Multi-line Support: [Yes/No]

Languages with Expansion:
- German: +30-40%
- French: +15-20%
- Spanish: +15-25%
- Russian: +10-15%

### Language-Specific Testing

Test Per Language:
- Layout Integrity: [Yes/No]
- Button/Link Functionality: [Yes/No]
- Form Validation Messages: [Yes/No]
- Navigation: [Yes/No]

Browser Testing:
- Test in Multiple Browsers: [Yes/No]
- Test on Mobile Devices: [Yes/No]

## FALLBACK STRATEGIES

Missing Translation Handling:

Strategy: [Show key / Show default language / Show placeholder / Custom]

Examples:
- Missing Key: "nav.new_feature"
- Show: _______________ (e.g., "nav.new_feature" / "[Missing translation]" / English version)

Partial Translation:
- Page Partially Translated: [Show mixed / Show fully in default language]
- Missing Namespace: [Load default language namespace]

## LOCALIZATION BEYOND TRANSLATION

Additional Localization:

- [ ] Images (text in images localized)
- [ ] Videos (subtitles/dubbing)
- [ ] Phone number formats
- [ ] Address formats
- [ ] Name formats (First Last vs Last First)
- [ ] Cultural adaptations (colors, symbols)
- [ ] Local examples/testimonials
- [ ] Local payment methods
- [ ] Local holidays/working days
- [ ] Local regulations/compliance

Cultural Sensitivity:
- Review Content for Cultural Appropriateness: [Yes/No]
- Local Expert Review: [Yes/No]

## NOTES & SPECIAL REQUIREMENTS
_______________________________________________
_______________________________________________
_______________________________________________
```

---

## ✅ IMPLEMENTATION PROMPT FOR LOVABLE

After filling this template:

```
Implement Multi-language System based on the completed specification.

CONTEXT: I have defined a comprehensive internationalization system with language detection, switching UI, translation management, and SEO optimization.

TASK:
1. Install and configure react-i18next (or chosen library)
2. Create translation files for all languages
3. Implement language detection (URL, cookie, browser, geo-IP)
4. Build language switcher component (desktop + mobile)
5. Set up language persistence (cookie + database for logged-in users)
6. Implement URL routing with language prefix
7. Add date/time/number/currency formatting per locale
8. Implement RTL support (if applicable)
9. Add hreflang tags for SEO
10. Create translation loading strategy with code splitting

GUIDELINES:
- Use semantic tokens for all styling
- Mobile-first responsive design
- Smooth language switching without full page reload
- Fallback to default language for missing translations
- Performance: lazy load translation files
- SEO: proper hreflang and canonical tags
- Accessibility: ARIA labels on language switcher
- User preference persistence across sessions

CONSTRAINTS:
- Translation files must be under 50KB per language
- Language switch must complete in <500ms
- No flash of untranslated content (FOUC)
- Support concurrent language detection methods
- Handle missing translations gracefully
- Mobile-optimized language selector

[Paste your filled multi-language template here]

EXPECTED DELIVERABLES:
1. Working language detection system
2. Language switcher component in header/footer
3. Translation files for all languages
4. URL routing with language prefixes
5. Date/time/number formatting per locale
6. Language persistence (cookie + database)
7. RTL support (if specified)
8. Hreflang tags in <head>
9. Missing translation fallback
10. Analytics tracking for language changes
```

---

## 📝 USAGE INSTRUCTIONS

1. **Start with 2 languages** - expand later (complexity increases with each language)
2. **Professional translation** for marketing pages - machine translation for UI only
3. **URL structure matters** for SEO - choose early (subdomain vs path prefix)
4. **Test text expansion** - some languages need 30% more space
5. **RTL requires testing** - layout completely changes
6. **Date/number formats** - use proper locale formatting
7. **Persist preference** - remember user's language choice
8. **SEO hreflang tags** - critical for international SEO

---

## 💡 BEST PRACTICES

- Use language codes (ISO 639-1): en, uk, es, de, fr, etc.
- Store translations in separate files per language
- Use namespaces to organize translations by feature/page
- Implement proper pluralization for each language
- Use locale-specific date/time/number formatting
- Test with actual native speakers, not just translators
- Handle text expansion gracefully (German can be 40% longer)
- Don't use flags alone for language selection (accessibility issue)
- Implement proper RTL support, not just text direction
- Use hreflang tags for SEO
- Cache translation files aggressively
- Lazy load translations for better performance
- Provide fallback to default language for missing keys
- Track which translations are missing in production
- Update legal pages in all languages when changed

---

## ⚠️ CRITICAL REMINDERS

- Language detection priority matters - get it right early
- URL structure affects SEO - choose wisely (can't easily change)
- Professional translation for marketing - quality matters
- Legal pages require professional legal translation
- RTL support is complex - budget extra time
- Text expansion breaks layouts - test thoroughly
- Currency formatting is locale-specific - use proper libraries
- Date formats vary widely - don't assume MM/DD/YYYY
- Flags can be controversial - consider language names instead
- Missing translations break user experience - have fallbacks
- Some languages have complex plural rules (Ukrainian has 4 forms)
- Locale codes include region (en-US vs en-GB)
- Hreflang tags critical for international SEO
- Machine translation is NOT suitable for legal/marketing content
- Test with native speakers - not just Google Translate
- Consider character encoding (UTF-8) for all languages
- Browser language detection can be inaccurate
- Geo-IP can be wrong (VPNs, proxies)
