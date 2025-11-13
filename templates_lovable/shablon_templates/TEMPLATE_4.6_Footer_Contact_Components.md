# TEMPLATE 4.6: FOOTER & CONTACT COMPONENTS

## 📋 PURPOSE
This template defines reusable footer and contact components that provide navigation, information, and ways to get in touch, appearing consistently across all pages.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Create Footer & Contact Components based on the following specification:

## COMPONENT LIBRARY OVERVIEW

Component Set: Footer & Contact
Design System: [Reference to Template 1.2]
Framework: React + TypeScript
Styling: Tailwind CSS with semantic tokens

Components to Create:
1. Main Footer
2. Footer Navigation Columns
3. Social Media Links
4. Newsletter Signup (Footer)
5. Footer Bottom Bar
6. Contact Information Block
7. Office Locations
8. Live Chat Widget
9. Contact CTA Section
10. Back to Top Button

---

## COMPONENT 4.6.1: MAIN FOOTER

### Component Props

```typescript
interface MainFooterProps {
  logo?: LogoConfig;
  columns: FooterColumn[];
  social: SocialLink[];
  newsletter?: NewsletterConfig;
  bottom: FooterBottomConfig;
  background?: BackgroundConfig;
}

interface FooterColumn {
  title: string;
  links: FooterLink[];
}

interface FooterLink {
  label: string;
  href: string;
  external?: boolean;
  badge?: string;
}
```

### Visual Design

Container:
- Background: _______________ (typically darker than body)
- Color: _______________ (light text on dark bg or vice versa)
- Padding:
  * Top: _______________
  * Bottom: _______________
  * Horizontal: _______________
- Border Top: _______________ (optional separator)

Max Width:
- Container: _______________ (e.g., container, max-w-7xl)
- Centered: [Yes/No]

### Layout Structure

Layout Type: [Multi-column / Single column on mobile]

Desktop Layout:
- Columns: [4 / 5 / 6]
- Grid: [Equal width / Custom widths]
- Gap: _______________

Mobile Layout:
- Stack: [Vertical]
- Accordion: [Yes/No] (collapsible sections)
- Spacing: _______________

Sections Order:
1. Logo & Description (optional)
2. Navigation Columns
3. Newsletter Signup (optional)
4. Social Links
5. Bottom Bar

---

## COMPONENT 4.6.2: FOOTER NAVIGATION COLUMNS

### Component Props

```typescript
interface FooterColumnsProps {
  columns: FooterColumn[];
  variant?: 'default' | 'minimal';
}
```

### Visual Design

Column Configuration:

Number of Columns: _______________

Column 1:
- Title: _______________
- Links Count: _______________
- Links:
  * Link 1: _______________
  * Link 2: _______________
  * Link 3: _______________
  [Continue...]

Column 2:
- Title: _______________
- Links Count: _______________
- Links:
  * Link 1: _______________
  * Link 2: _______________
  [Continue...]

Column 3:
- Title: _______________
- Links Count: _______________
- Links:
  [Continue...]

Column 4:
- Title: _______________
- Links Count: _______________
- Links:
  [Continue...]

[Continue for all columns...]

### Column Styling

Column Title:
- Font Size: _______________
- Font Weight: _______________ (e.g., font-semibold, font-bold)
- Color: _______________
- Margin Bottom: _______________
- Text Transform: [Uppercase / Normal]
- Letter Spacing: _______________ (if uppercase)

Link List:
- Spacing: _______________ (gap between links)
- List Style: [None]

Link Item:
- Font Size: _______________
- Font Weight: _______________
- Color: _______________ (muted or default)
- Hover Color: _______________ (brighter or primary)
- Transition: _______________
- Text Decoration: [None / Underline on hover]

Link Icon:
- Show: [Optional]
- Icon: [ExternalLink for external / None for internal]
- Size: _______________
- Position: [After text]
- Color: _______________ (muted)

Badge/Tag:
- Show: [Optional per link]
- Text: _______________ (e.g., "New", "Popular")
- Background: _______________
- Font Size: _______________
- Padding: _______________
- Border Radius: _______________
- Position: [After label]

### Mobile Accordion (if enabled)

Accordion Behavior:
- Enabled: [Yes/No]
- Default State: [All closed / First open]

Trigger:
- Icon: [ChevronDown]
- Icon Position: [Right]
- Icon Rotation: [When open]
- Padding: _______________
- Border: _______________ (bottom border)

Content:
- Animation: [Slide down / Fade in]
- Padding: _______________

---

## COMPONENT 4.6.3: SOCIAL MEDIA LINKS

### Component Props

```typescript
interface SocialLinksProps {
  links: SocialLink[];
  variant?: 'icons' | 'buttons';
  size?: 'sm' | 'md' | 'lg';
}

interface SocialLink {
  platform: string;
  url: string;
  icon: string;
  label?: string;
}
```

### Visual Design

Platforms:
- [ ] Twitter/X
- [ ] Facebook
- [ ] LinkedIn
- [ ] Instagram
- [ ] YouTube
- [ ] GitHub
- [ ] Discord
- [ ] TikTok
- [ ] Other: _______________

Social Link 1:
- Platform: _______________
- URL: _______________
- Icon: _______________ (lucide-react icon name)

Social Link 2:
[Repeat for all platforms...]

### Variant Styles

Icons Only:
- Icon Size: _______________
- Icon Color: _______________ (muted or white)
- Hover Color: _______________ (platform brand color / primary)
- Background: [None / Circle / Square]
- Spacing: _______________

If Background:
- Background Color: _______________
- Background Size: _______________
- Border Radius: _______________
- Hover Background: _______________ (brand color)

Buttons:
- Background: _______________
- Border: _______________
- Border Radius: _______________
- Padding: _______________
- Icon + Label: [Both visible]
- Hover Style: _______________ (brand color bg)

### Layout

Position: [Dedicated section / In column / Bottom bar / All]
Alignment: [Left / Center / Right]
Layout: [Horizontal row / Grid / Vertical]
Spacing: _______________

ARIA Labels:
- Include platform name for accessibility
- Example: "Follow us on Twitter"

---

## COMPONENT 4.6.4: NEWSLETTER SIGNUP (Footer)

### Component Props

```typescript
interface FooterNewsletterProps {
  headline?: string;
  description?: string;
  placeholder?: string;
  buttonText?: string;
  compact?: boolean;
}
```

### Visual Design

Position: [Dedicated column / Full width section / Sidebar]

Container:
- Background: _______________ (may differ from footer bg)
- Border: _______________
- Border Radius: _______________
- Padding: _______________
- Max Width: _______________ (if in column)

Headline:
- Text: _______________ (e.g., "Stay Updated", "Newsletter")
- Font Size: _______________
- Font Weight: _______________
- Color: _______________
- Margin Bottom: _______________

Description:
- Text: _______________ (e.g., "Get the latest updates...")
- Font Size: _______________
- Color: _______________ (muted)
- Max Width: _______________
- Margin Bottom: _______________

Form Layout: [Horizontal / Vertical]

Email Input:
- Placeholder: _______________
- Background: _______________
- Border: _______________
- Color: _______________
- Padding: _______________

Submit Button:
- Text: _______________
- Style: [Primary / Accent]
- Size: _______________
- Icon: [Mail / ArrowRight / None]
- Width: [Auto / Full width on mobile]

Privacy Notice:
- Show: [Yes/No]
- Text: "We respect your privacy"
- Font Size: _______________
- Color: _______________ (muted)
- Margin Top: _______________

Success/Error States:
[Same as Newsletter Signup component from 4.4.6]

---

## COMPONENT 4.6.5: FOOTER BOTTOM BAR

### Component Props

```typescript
interface FooterBottomProps {
  copyright: string;
  legalLinks: FooterLink[];
  paymentMethods?: PaymentMethod[];
  languageSwitch?: boolean;
}
```

### Visual Design

Container:
- Background: _______________ (may be darker than main footer)
- Border Top: _______________ (separator)
- Padding:
  * Vertical: _______________
  * Horizontal: _______________

Layout: [Space between / Centered / Stacked on mobile]

### Copyright Section

Text: _______________
Format: © 2025 [Company Name]. All rights reserved.
Font Size: _______________
Color: _______________ (muted)

Dynamic Year: [Yes - use JavaScript to insert current year]

### Legal Links

Links:
- [ ] Privacy Policy
- [ ] Terms of Service
- [ ] Cookie Policy
- [ ] Accessibility
- [ ] Other: _______________

Layout: [Horizontal list / Pipe-separated]
Separator: [Dot / Pipe / None]
Spacing: _______________

Link Styling:
- Font Size: _______________
- Color: _______________ (muted)
- Hover Color: _______________
- Text Decoration: [Underline on hover / None]

### Payment Methods (Optional)

Show: [Yes/No]

Icons:
- [ ] Visa
- [ ] Mastercard
- [ ] American Express
- [ ] PayPal
- [ ] Apple Pay
- [ ] Google Pay
- [ ] Other: _______________

Layout: [Horizontal row]
Icon Size: _______________
Filter: [Grayscale / None]
Opacity: _______________

### Language Switcher

Show: [Yes/No]
Type: [Dropdown / Flags / Text]
Position: [Right / Center / Left]
[See Language Switcher from 4.1.7]

---

## COMPONENT 4.6.6: CONTACT INFORMATION BLOCK

### Component Props

```typescript
interface ContactInfoProps {
  email?: string;
  phone?: string;
  address?: AddressConfig;
  hours?: string;
  variant?: 'compact' | 'detailed';
}
```

### Visual Design

Container:
- Background: _______________
- Border: _______________
- Border Radius: _______________
- Padding: _______________

Layout: [Vertical list / Grid / Cards]

### Contact Items

Email:
- Show: [Yes/No]
- Icon: [Mail]
- Icon Size: _______________
- Icon Color: _______________
- Format: _______________ (e.g., hello@company.com)
- Clickable: [Yes - mailto link]
- Font Size: _______________

Phone:
- Show: [Yes/No]
- Icon: [Phone]
- Icon Size: _______________
- Icon Color: _______________
- Format: _______________ (e.g., +1 (555) 123-4567)
- Clickable: [Yes - tel link]
- Font Size: _______________

Address:
- Show: [Yes/No]
- Icon: [MapPin]
- Icon Size: _______________
- Icon Color: _______________
- Format: [Multi-line]
  * Street: _______________
  * City, State ZIP: _______________
  * Country: _______________
- Link: [Yes - Google Maps / None]
- Font Size: _______________

Business Hours:
- Show: [Yes/No]
- Icon: [Clock]
- Icon Size: _______________
- Icon Color: _______________
- Format: "Mon-Fri: 9am-5pm EST"
- Font Size: _______________

### Item Styling

Layout: [Icon on left, text on right]
Spacing: _______________ (gap between icon and text)
Item Margin: _______________ (vertical spacing between items)

Label:
- Show: [Optional]
- Text: "Email:", "Phone:", "Address:"
- Font Weight: _______________ (semibold)
- Color: _______________

Value:
- Font Weight: [Normal]
- Color: _______________ (muted or default)

Link Hover:
- Color: _______________ (primary)
- Text Decoration: [Underline]

---

## COMPONENT 4.6.7: OFFICE LOCATIONS

### Component Props

```typescript
interface OfficeLocationsProps {
  offices: Office[];
  variant?: 'list' | 'cards' | 'map';
}

interface Office {
  name: string;
  address: string;
  phone?: string;
  email?: string;
  mapUrl?: string;
}
```

### Visual Design

Headline:
- Text: _______________ (e.g., "Our Offices", "Visit Us")
- Font Size: _______________
- Font Weight: _______________
- Margin Bottom: _______________

Variant Styles:

List:
- Layout: [Vertical list]
- Dividers: [Yes/No]

Cards:
- Layout: [Grid]
- Columns: [2 / 3]
- Gap: _______________
- Card Background: _______________
- Card Border: _______________
- Card Padding: _______________

Map:
- Interactive Map: [Yes/No]
- Map Service: [Google Maps / OpenStreetMap]
- Markers: [All offices]

### Office Item

Office Name:
- Font Size: _______________
- Font Weight: _______________
- Color: _______________
- Margin Bottom: _______________

Address:
- Font Size: _______________
- Color: _______________ (muted)
- Line Height: _______________

Phone:
- Show: [Yes/No]
- Icon: [Phone]
- Font Size: _______________
- Link: [tel:]

Email:
- Show: [Yes/No]
- Icon: [Mail]
- Font Size: _______________
- Link: [mailto:]

Map Link:
- Show: [Yes/No]
- Text: "Get directions"
- Icon: [MapPin / ExternalLink]
- Link: [Google Maps URL]

---

## COMPONENT 4.6.8: LIVE CHAT WIDGET

### Component Props

```typescript
interface LiveChatProps {
  provider?: 'intercom' | 'drift' | 'custom';
  position?: 'bottom-right' | 'bottom-left';
  color?: string;
  greeting?: string;
  availability?: boolean;
}
```

### Visual Design

Position: [Bottom right / Bottom left]
Offset:
- Bottom: _______________
- Right/Left: _______________

Z-Index: 5000 (above most elements)

### Chat Bubble (Closed State)

Size: _______________
Shape: [Circle / Rounded square]
Background: _______________ (primary or brand color)
Icon: [MessageCircle / MessageSquare]
Icon Color: [White]
Shadow: _______________

Badge (Unread):
- Show: [When messages]
- Position: [Top right of bubble]
- Background: [Destructive/red]
- Count: [Number of messages]
- Size: _______________

Hover Effect:
- Transform: _______________ (scale)
- Shadow: _______________ (increase)

### Chat Window (Open State)

Size:
- Width: _______________
- Height: _______________
- Mobile: [Full screen / Large modal]

Container:
- Background: _______________
- Border Radius: _______________
- Shadow: _______________

Header:
- Background: _______________ (brand color)
- Color: [White]
- Padding: _______________
- Height: _______________
- Close Button: [Yes]

Title:
- Text: _______________ (e.g., "Chat with us")
- Font Size: _______________
- Font Weight: _______________

Status:
- Show: [Yes/No]
- Text: "We're online" / "Typically responds in X minutes"
- Color: [Success green / Muted]
- Icon: [Dot / Clock]

Body:
- Padding: _______________
- Background: _______________
- Max Height: _______________ (with scroll)

Input Area:
- Background: _______________
- Border: _______________
- Padding: _______________
- Input Height: _______________
- Send Button: [Icon / Text]

### Availability

Show When Online: [Yes/No]
Show When Offline: [Yes/No]
Offline Message: "We're currently offline. Leave a message!"
Auto-Response: [Yes/No]

---

## COMPONENT 4.6.9: CONTACT CTA SECTION

### Component Props

```typescript
interface ContactCTAProps {
  headline: string;
  description?: string;
  primaryCta: CTAConfig;
  secondaryCta?: CTAConfig;
  background?: BackgroundConfig;
  contactMethods?: ContactMethod[];
}
```

### Visual Design

Use Case: [Above footer / Separate section]

Container:
- Background: _______________ (accent / gradient)
- Padding: _______________
- Border Radius: _______________
- Max Width: _______________

Layout: [Centered / Split]

Headline:
- Font Size: _______________
- Font Weight: _______________
- Color: _______________
- Text Align: [Center / Left]
- Max Width: _______________

Description:
- Font Size: _______________
- Color: _______________ (muted)
- Text Align: [Center / Left]
- Max Width: _______________
- Margin: _______________

CTAs:
- Layout: [Horizontal / Vertical / Stacked on mobile]
- Spacing: _______________
- Alignment: [Center / Left]

Primary CTA:
- Text: _______________ (e.g., "Contact Sales", "Get in Touch")
- Style: [Primary button]
- Size: [Large]
- Icon: [Mail / Phone / None]

Secondary CTA:
- Text: _______________ (e.g., "Schedule a call")
- Style: [Secondary / Outline]
- Size: [Large]
- Icon: [Calendar]

Contact Methods:
- Show: [Yes/No]
- Layout: [Icons row below CTAs]
- Methods: [Email / Phone / Chat / Calendar]
- Icons: [With labels / Icons only]

---

## COMPONENT 4.6.10: BACK TO TOP BUTTON

### Component Props

```typescript
interface BackToTopProps {
  showAfterScroll?: number;
  position?: 'bottom-right' | 'bottom-left';
  smooth?: boolean;
  icon?: string;
}
```

### Visual Design

Button Shape: [Circle / Square / Rounded square]
Size: _______________

Position: [Bottom right / Bottom left]
Offset:
- Bottom: _______________
- Right/Left: _______________

Z-Index: 1000

Background: _______________
Color: _______________
Border: _______________
Shadow: _______________

Icon:
- Type: [ArrowUp / ChevronUp / ChevronsUp]
- Size: _______________
- Color: _______________

### Behavior

Show After Scroll: _______________ px
Hide When: [At top / Never auto-hide]

Animation:
- Entrance: [Fade in / Slide in / Scale in]
- Exit: [Fade out / Slide out / Scale out]
- Duration: _______________

Scroll Behavior:
- Type: [Smooth / Instant]
- Duration: _______________ ms (if smooth)
- Easing: _______________

Hover Effect:
- Transform: _______________ (scale / translateY)
- Shadow: _______________ (increase)
- Background: _______________ (darken)

Mobile:
- Show: [Yes/No]
- Size: _______________ (may be smaller)
- Position: _______________ (may adjust)

Accessibility:
- ARIA Label: "Back to top"
- Keyboard: [Tab to focus, Enter to activate]

---

## SHARED SPECIFICATIONS

### Footer Brand Section (Optional)

Logo:
- Show: [Yes/No]
- Size: _______________
- Position: [Top of footer / In column]
- Link: [Homepage]

Tagline/Description:
- Show: [Yes/No]
- Text: _______________
- Font Size: _______________
- Color: _______________ (muted)
- Max Width: _______________
- Margin: _______________

### Dark Mode Support

Light Mode:
- Background: _______________
- Text: _______________
- Links: _______________

Dark Mode:
- Background: _______________
- Text: _______________
- Links: _______________

Auto-Switch: [Based on theme / Independent]

### Accessibility

Footer Must Include:
- [ ] Semantic HTML (footer tag)
- [ ] Landmark role="contentinfo"
- [ ] Keyboard navigation
- [ ] ARIA labels for icons
- [ ] Focus indicators
- [ ] Screen reader friendly
- [ ] Skip to footer link (optional)
- [ ] Color contrast WCAG AA

### Responsive Behavior

Mobile (<768px):
- Columns: [Stack vertically]
- Accordion: [Optional for nav columns]
- Social: [Center aligned]
- Newsletter: [Full width]
- Bottom bar: [Stack elements]
- Contact: [Simplified / Hidden]

Tablet (768-1024px):
- Columns: [2-3]
- Some stacking

Desktop (>1024px):
- Full column layout
- Optimal spacing

### Performance

- [ ] Lazy load newsletter form
- [ ] Optimize logo image
- [ ] Minimal JavaScript
- [ ] Efficient social icons

### SEO Considerations

- [ ] Structured data (Organization)
- [ ] Important links for crawlers
- [ ] Contact information visible
- [ ] Sitemap link
- [ ] Social profiles

---

## NOTES & SPECIAL REQUIREMENTS
_______________________________________________
_______________________________________________
_______________________________________________
```

---

## ✅ IMPLEMENTATION PROMPT FOR LOVABLE

After filling this template:

```
Create Footer & Contact Components based on the completed specification.

CONTEXT: I have defined a comprehensive footer system with navigation columns, social links, newsletter signup, contact information, and supporting components.

TASK:
1. Create MainFooter component with layout structure
2. Build FooterNavigation columns
3. Implement SocialLinks component
4. Create footer NewsletterSignup
5. Build FooterBottomBar with legal links
6. Implement ContactInfo block
7. Create OfficeLocations component
8. Integrate LiveChatWidget
9. Build ContactCTA section
10. Create BackToTop button

GUIDELINES:
- Mobile-first responsive design
- Use semantic tokens from design system
- Clear information hierarchy
- Accessible navigation
- Collapsible sections on mobile (optional)
- Footer appears on every page
- Works with dark mode
- WCAG 2.1 AA compliance

CONSTRAINTS:
- Must include all legal pages
- Contact information accurate
- Social links work correctly
- Newsletter form validates
- Color contrast sufficient
- Touch targets 44px minimum
- Works on all modern browsers
- Fast load time

[Paste your filled footer template here]

EXPECTED DELIVERABLES:
1. MainFooter component structure
2. FooterNavigation columns
3. SocialLinks component
4. Footer NewsletterSignup
5. FooterBottomBar component
6. ContactInfo display
7. OfficeLocations component
8. LiveChatWidget integration
9. ContactCTA section
10. BackToTop button
```

---

## 📝 USAGE INSTRUCTIONS

1. **Essential links only** - footer shouldn't be overwhelming
2. **Legal compliance** - privacy, terms, cookie policy required
3. **Contact info** - make it easy to reach you
4. **Social proof** - social links show you're active
5. **Newsletter** - footer signup captures interested users
6. **Mobile friendly** - footer usable on mobile devices
7. **Consistent** - appears same on all pages
8. **Update regularly** - keep copyright year current

---

## 💡 BEST PRACTICES

- Keep footer navigation to 4-6 columns maximum
- Most important links in leftmost columns (F-pattern reading)
- Include contact information in footer
- Newsletter signup works well in footer (high intent)
- Social links with icons more recognizable than text
- Legal links always in bottom bar
- Office locations build local trust
- Live chat widget increases conversions 20-30%
- Back to top button improves UX on long pages
- Footer logo should link to homepage
- Copyright year should auto-update
- Test footer links regularly (they break easily)
- Mobile footer should collapse/accordion to save space
- Payment icons build trust for e-commerce

---

## ⚠️ CRITICAL REMINDERS

- Footer appears on every page - must be perfect
- Legal links are required (privacy, terms, cookies)
- Contact information must be current and accurate
- Social links must actually work (test regularly)
- Newsletter signup must comply with GDPR/CCPA
- Copyright year should be dynamic (not hardcoded)
- Footer is second-most important navigation (after header)
- Mobile footer UX often overlooked - test thoroughly
- Live chat can be annoying if poorly timed
- Back to top button essential for long pages
- Accessibility critical - footer contains important links
- Office locations help with local SEO
- Payment icons should match actual accepted methods
- Trust badges in footer build credibility
- Footer size impacts page performance
- Test all links quarterly - footer links break easily
