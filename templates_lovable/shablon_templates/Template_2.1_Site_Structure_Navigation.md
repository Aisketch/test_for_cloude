# TEMPLATE 2.1: SITE STRUCTURE & NAVIGATION SCHEMA

## 📋 PURPOSE
This template defines the complete sitemap, navigation structure, and page relationships for your multi-language SaaS website.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Implement Site Structure and Navigation based on the following specification:

## SITE HIERARCHY

### Primary Pages (Level 1)
Total Primary Pages: _______________

1. Homepage
   - URL: / (or /[lang]/ for multi-language)
   - Purpose: _______________
   - Key Message: _______________
   - Primary CTA: _______________
   - Secondary CTA: _______________

2. [Primary Page Name]: _______________
   - URL: _______________
   - Purpose: _______________
   - Key Message: _______________
   - Primary CTA: _______________
   - Secondary CTA: _______________

3. [Primary Page Name]: _______________
   - URL: _______________
   - Purpose: _______________
   - Key Message: _______________
   - Primary CTA: _______________
   - Secondary CTA: _______________

4. [Primary Page Name]: _______________
   - URL: _______________
   - Purpose: _______________
   - Key Message: _______________
   - Primary CTA: _______________
   - Secondary CTA: _______________

5. [Primary Page Name]: _______________
   - URL: _______________
   - Purpose: _______________
   - Key Message: _______________
   - Primary CTA: _______________
   - Secondary CTA: _______________

[Continue for all primary pages...]

### Secondary Pages (Level 2)
Parent-Child Relationships:

Parent: _______________
├── Child Page: _______________
│   URL: _______________
│   Purpose: _______________
├── Child Page: _______________
│   URL: _______________
│   Purpose: _______________
└── Child Page: _______________
    URL: _______________
    Purpose: _______________

Parent: _______________
├── Child Page: _______________
│   URL: _______________
│   Purpose: _______________
├── Child Page: _______________
│   URL: _______________
│   Purpose: _______________
└── Child Page: _______________
    URL: _______________
    Purpose: _______________

[Continue for all secondary pages...]

### Tertiary Pages (Level 3+)
Deep navigation structures (if applicable):

_______________________________________________
_______________________________________________

### Utility Pages
Required Pages:
- [ ] 404 Error Page
      URL: /404
      Messaging: _______________
      Helpful Links: _______________

- [ ] 500 Error Page
      URL: /500
      Messaging: _______________
      Support Contact: _______________

- [ ] Privacy Policy
      URL: /privacy
      Last Updated: _______________
      Compliance: [GDPR/CCPA/Other]

- [ ] Terms of Service
      URL: /terms
      Last Updated: _______________
      Key Sections: _______________

- [ ] Cookie Policy
      URL: /cookies
      Last Updated: _______________

- [ ] Sitemap Page (HTML)
      URL: /sitemap
      Purpose: User-facing sitemap

- [ ] Contact Page
      URL: /contact
      Form Fields: _______________
      Response Time: _______________

Optional Pages:
- [ ] About Us: /about
- [ ] Team: /team
- [ ] Careers: /careers
- [ ] Press/Media: /press
- [ ] Blog/Resources: /blog
- [ ] Help Center: /help
- [ ] Security: /security
- [ ] Accessibility Statement: /accessibility
- [ ] Status Page: /status

### Authentication Pages
User Account Pages:

- [ ] Sign Up
      URL: /signup
      Fields: _______________
      Social Login: [Yes/No]
      Providers: _______________

- [ ] Sign In
      URL: /login
      Fields: _______________
      Social Login: [Yes/No]
      Remember Me: [Yes/No]
      Password Reset Link: [Yes/No]

- [ ] Password Reset
      URL: /reset-password
      Flow: _______________

- [ ] Email Verification
      URL: /verify-email
      Success Redirect: _______________

- [ ] User Dashboard (if applicable)
      URL: /dashboard
      Default View: _______________

- [ ] User Settings (if applicable)
      URL: /settings
      Sections: _______________

## NAVIGATION SYSTEMS

### Primary Navigation (Main Menu)

Location: _______________
Style: [Horizontal/Vertical/Mega Menu/Dropdown]
Sticky: [Yes/No]
Transparent on Hero: [Yes/No]

Desktop Navigation Items (Left to Right):
1. _______________
   - Link: _______________
   - Dropdown: [Yes/No]
   - Mega Menu: [Yes/No]

2. _______________
   - Link: _______________
   - Dropdown: [Yes/No]
   - Submenu Items: _______________

3. _______________
   - Link: _______________
   - Dropdown: [Yes/No]
   - Submenu Items: _______________

4. _______________
   - Link: _______________
   - Dropdown: [Yes/No]
   - Submenu Items: _______________

5. _______________
   - Link: _______________
   - Dropdown: [Yes/No]
   - Submenu Items: _______________

Right-Side Items:
- [ ] Language Switcher
      Position: _______________
- [ ] Login Button
      Style: _______________
- [ ] Sign Up Button (CTA)
      Style: _______________
- [ ] User Avatar (if logged in)
- [ ] Search Icon
- [ ] Dark Mode Toggle

Mobile Navigation:
Type: [Hamburger Menu/Slide-out/Full Screen]
Animation: _______________
Menu Button Position: _______________
Close Button Position: _______________

Mobile Menu Items (Top to Bottom):
[Same as desktop or simplified version]
_______________________________________________

### Secondary Navigation

Location: [Top bar/Below header/None]
Purpose: _______________

Items:
1. _______________
2. _______________
3. _______________

### Footer Navigation

Footer Layout: [Single Column/Multi-Column/Mega Footer]
Number of Columns: _______________

Column 1: [Column Title]
- _______________
- _______________
- _______________
- _______________

Column 2: [Column Title]
- _______________
- _______________
- _______________
- _______________

Column 3: [Column Title]
- _______________
- _______________
- _______________
- _______________

Column 4: [Column Title]
- _______________
- _______________
- _______________
- _______________

Footer Bottom Section:
- [ ] Copyright Notice
- [ ] Legal Links (Privacy, Terms, etc.)
- [ ] Social Media Icons
- [ ] Language Switcher
- [ ] Contact Information
- [ ] Trust Badges/Certifications

### Breadcrumb Navigation

Implement Breadcrumbs: [Yes/No]
Pages with Breadcrumbs: _______________
Format: Home > Category > Current Page
Schema Markup: [Yes/No]

### Contextual Navigation

In-Page Navigation:
- [ ] Table of Contents (for long pages)
- [ ] "Back to Top" Button
- [ ] Previous/Next Page Links
- [ ] Related Pages Suggestions

Sidebar Navigation (if applicable):
Pages with Sidebar: _______________
Sidebar Content: _______________

## URL STRUCTURE & ROUTING

### URL Naming Convention
Pattern: [kebab-case/snake_case/camelCase]
Example: _______________

Language Prefix: [Yes/No]
If Yes: /[lang]/[page] (e.g., /en/features, /uk/features)

Trailing Slash: [Yes/No]
Clean URLs: [Yes/No] (remove .html extensions)

### URL Hierarchy Rules
Parent-Child Pattern: /[parent]/[child]
Example: _______________

Deep Nesting Limit: _______________ levels
Canonical URL Rules: _______________

### Special URL Patterns
Blog/Articles: _______________
Product Pages: _______________
Category Pages: _______________
User Profiles: _______________

### URL Parameters
Query Parameters Allowed: [Yes/No]
Common Parameters:
- utm_source (marketing tracking)
- ref (referral tracking)
- lang (language override)
- Other: _______________

### Redirects Strategy
Old URLs to Redirect: _______________
Redirect Type: [301 Permanent/302 Temporary]
Redirect Rules: _______________

## MEGA MENU STRUCTURE (if applicable)

Mega Menu for: _______________

Layout: [2 Columns/3 Columns/4 Columns/Featured + Lists]

Section 1: [Title]
- Items: _______________
- Featured: _______________
- CTA: _______________

Section 2: [Title]
- Items: _______________
- Featured: _______________
- CTA: _______________

Section 3: [Title]
- Items: _______________
- Featured: _______________
- CTA: _______________

Visual Elements:
- [ ] Icons for menu items
- [ ] Featured product/page highlight
- [ ] Banner/Promo spot
- [ ] Image/Screenshot
- [ ] CTA Button

## MOBILE NAVIGATION SPECIFIC

Mobile Menu Behavior:
Open Animation: _______________
Close Animation: _______________
Overlay: [Yes/No]
Scroll Behavior: [Disable body scroll/Allow scroll]

Mobile Menu Structure:
- Simplified from desktop: [Yes/No]
- Accordion for submenus: [Yes/No]
- Search prominent: [Yes/No]
- CTA buttons visible: [Yes/No]

Mobile Bottom Navigation Bar: [Yes/No]
If Yes, Items:
1. _______________
2. _______________
3. _______________
4. _______________
5. _______________

## NAVIGATION ACCESSIBILITY

Keyboard Navigation:
- [ ] Tab order logical
- [ ] Skip to main content link
- [ ] Escape key closes menus
- [ ] Arrow keys navigate submenus

Screen Reader Support:
- [ ] ARIA labels on all nav elements
- [ ] aria-expanded for dropdowns
- [ ] aria-current for active page
- [ ] Landmark roles (nav, main, footer)

Focus Indicators:
Style: _______________
Color: _______________

## NAVIGATION BEHAVIOR

Active Page Indication:
Style: _______________
Color: _______________

Hover States:
Desktop: _______________
Tablet: _______________

Dropdown Behavior:
Trigger: [Hover/Click/Both]
Close Trigger: [Click outside/Hover out/Manual close]
Delay: _______________

Scroll Behavior:
Sticky Navigation: [Yes/No]
Hide on Scroll Down: [Yes/No]
Show on Scroll Up: [Yes/No]
Change Style After Scroll: [Yes/No]
Scroll Threshold: _______________ px

## SEARCH FUNCTIONALITY

Site Search: [Yes/No]

If Yes:
Location: _______________
Type: [Full page/Modal/Dropdown]
Search Scope: _______________
Results Display: _______________
Autocomplete: [Yes/No]
Recent Searches: [Yes/No]
Popular Searches: [Yes/No]

## PAGE RELATIONSHIPS

### Cross-Page Connections
Related Pages Feature: [Yes/No]
"You might also like" Section: [Yes/No]
Contextual Links: _______________

### Conversion Paths
Primary Conversion Path:
Homepage → _______________ → _______________ → Signup

Alternative Paths:
Path 1: _______________
Path 2: _______________
Path 3: _______________

### External Links
Open in New Tab: [Yes/No]
External Link Indicator: [Yes/No]
Nofollow on External: [Case by case/All/None]

## NAVIGATION ANALYTICS

Track Navigation Events:
- [ ] Menu item clicks
- [ ] Dropdown opens
- [ ] Mobile menu toggles
- [ ] Language switches
- [ ] Search queries
- [ ] 404 pages reached
- [ ] External link clicks

Event Naming Convention: _______________

## SITEMAP GENERATION

XML Sitemap: [Yes/No]
Location: /sitemap.xml
Update Frequency: [Daily/Weekly/On Deploy]
Priority Values: _______________
Language Alternate Links: [Yes/No]

HTML Sitemap: [Yes/No]
Location: /sitemap
Organize By: [Category/Alphabetical/Hierarchy]

## NAVIGATION PERFORMANCE

Optimize For:
- [ ] First Contentful Paint (FCP)
- [ ] Largest Contentful Paint (LCP)
- [ ] Minimize layout shift (CLS)
- [ ] Fast interaction (FID)

Lazy Load: [Images in mega menu/Heavy navigation assets]
Preload: [Critical navigation assets]

## INTERNATIONALIZATION

Language Switcher in Navigation: [Yes/No]
Location: _______________
Display: [Flags/Text/Dropdown/Both]

Per-Language Navigation Differences:
_______________________________________________

RTL Navigation Adjustments (if applicable):
_______________________________________________

## SPECIAL NAVIGATION FEATURES

Notification Badge: [Yes/No]
Location: _______________

User Menu (Logged In):
Items:
- _______________
- _______________
- _______________
- _______________

Promotional Banner:
Display: [Yes/No]
Location: [Above navigation/Below navigation]
Dismissible: [Yes/No]
Content: _______________

## NAVIGATION TESTING REQUIREMENTS

Test Cases:
- [ ] All links work correctly
- [ ] Active states display properly
- [ ] Dropdowns open/close smoothly
- [ ] Mobile menu functions correctly
- [ ] Keyboard navigation works
- [ ] Screen reader announces correctly
- [ ] Language switcher works
- [ ] Breadcrumbs accurate
- [ ] Search returns results
- [ ] 404 page displays for broken links

Cross-Browser Testing:
- [ ] Chrome
- [ ] Firefox
- [ ] Safari
- [ ] Edge
- [ ] Mobile Safari
- [ ] Mobile Chrome

## NAVIGATION MAINTENANCE

Review Schedule: _______________
Update Process: _______________
Version Control: _______________
Stakeholder Approval: _______________

## NOTES & SPECIAL REQUIREMENTS
_______________________________________________
_______________________________________________
_______________________________________________
```

---

## ✅ IMPLEMENTATION PROMPT FOR LOVABLE

After filling this template:

```
Implement Site Navigation Structure based on the completed specification.

CONTEXT: I have defined a comprehensive site structure with [NUMBER] primary pages, multi-level navigation, and user flows for a multi-language SaaS website.

TASK:
1. Create React Router routing configuration with all specified pages
2. Build primary navigation component (desktop + mobile)
3. Implement footer navigation with specified columns
4. Set up breadcrumb navigation system
5. Configure URL structure with language prefixes
6. Create 404 and error pages
7. Implement sticky navigation behavior
8. Add active page indicators
9. Set up navigation analytics events
10. Generate sitemap.xml configuration

GUIDELINES:
- Mobile-first responsive navigation
- Smooth animations and transitions
- Keyboard accessible (skip links, focus management)
- ARIA labels for all navigation elements
- Active states clearly visible
- Test all navigation paths
- Ensure proper heading hierarchy
- Language switcher integrated in navigation

CONSTRAINTS:
- Must work with multi-language routing
- Performance: minimize navigation render time
- Accessibility: WCAG 2.1 AA compliance
- SEO: proper semantic HTML structure
- Mobile: touch-friendly targets (44x44px minimum)

[Paste your filled navigation template here]

EXPECTED DELIVERABLES:
1. Fully functional desktop navigation with dropdowns
2. Mobile hamburger menu with smooth animation
3. Footer with organized link columns
4. Breadcrumb component for deep pages
5. 404 error page with helpful navigation
6. Language switcher in specified location
7. Active page indication working
8. All routes configured correctly
9. Navigation accessible via keyboard
10. Analytics tracking on navigation events
```

---

## 📝 USAGE INSTRUCTIONS

1. **Map out full site structure** before filling template
2. **Keep navigation depth** to 3 levels maximum for usability
3. **Prioritize mobile navigation** - test on actual devices
4. **Use clear, action-oriented** navigation labels
5. **Test all paths** lead to correct destinations
6. **Review with stakeholders** before implementation
7. **Plan for scalability** - easy to add pages later

---

## ⚠️ CRITICAL REMINDERS

- Navigation is critical for SEO and UX
- Keep primary navigation items to 5-7 for clarity
- Mobile menu should load fast (no heavy assets)
- Test keyboard navigation thoroughly
- Ensure language switcher is prominent
- 404 pages should be helpful, not dead ends
- Sitemap XML crucial for SEO
- Monitor navigation analytics to optimize
