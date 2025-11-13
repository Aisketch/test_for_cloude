# TEMPLATE 4.2: HERO SECTIONS & CTAs COMPONENTS

## 📋 PURPOSE
This template defines reusable hero section and call-to-action (CTA) components that drive conversions across your website, from homepage heroes to inline CTAs.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Create Hero Sections & CTA Components based on the following specification:

## COMPONENT LIBRARY OVERVIEW

Component Set: Hero Sections & CTAs
Design System: [Reference to Template 1.2]
Framework: React + TypeScript
Styling: Tailwind CSS with semantic tokens

Components to Create:
1. Full-Screen Hero
2. Above-the-Fold Hero
3. Split Hero (Text + Visual)
4. Minimal Hero
5. Video Hero
6. Primary CTA Button
7. Secondary CTA Button
8. CTA Section
9. Inline CTA
10. Sticky CTA Bar

---

## COMPONENT 4.2.1: FULL-SCREEN HERO

### Component Props

```typescript
interface FullScreenHeroProps {
  headline: string;
  subheadline?: string;
  description?: string;
  primaryCta: CTAConfig;
  secondaryCta?: CTAConfig;
  visual?: {
    type: 'image' | 'video' | 'illustration';
    src: string;
    alt?: string;
  };
  background?: BackgroundConfig;
  socialProof?: SocialProofConfig;
  scrollIndicator?: boolean;
}

interface CTAConfig {
  text: string;
  href?: string;
  onClick?: () => void;
  icon?: string;
  variant: 'primary' | 'secondary' | 'outline' | 'ghost';
  size?: 'sm' | 'md' | 'lg' | 'xl';
}
```

### Visual Design

Height: [100vh / 90vh / 80vh / 100dvh]
Min Height: _______________ (e.g., 600px on mobile)

Layout: [Centered / Split / Asymmetric]
Alignment: [Center / Left / Right]

Content Container:
- Max Width: _______________ (e.g., max-w-5xl)
- Padding: _______________
- Alignment: [Center / Left]

### Headline Configuration

Typography:
- Font Family: _______________ (use design system)
- Font Size:
  * Mobile: _______________ (e.g., text-4xl)
  * Tablet: _______________ (e.g., text-5xl)
  * Desktop: _______________ (e.g., text-6xl, text-7xl)
- Font Weight: _______________ (e.g., font-bold, font-extrabold)
- Line Height: _______________ (e.g., leading-tight)
- Letter Spacing: _______________ (optional)

Color: _______________ (semantic token)
Max Width: _______________ (e.g., max-w-4xl for readability)

Gradient Text: [Yes/No]
If Yes:
- Gradient: _______________ (e.g., from-primary to-accent)

Animation:
- Type: [Fade in / Slide up / Type effect / None]
- Delay: _______________
- Duration: _______________

### Subheadline/Description

Show Subheadline: [Yes/No]

Typography:
- Font Size:
  * Mobile: _______________
  * Tablet: _______________
  * Desktop: _______________
- Font Weight: _______________
- Line Height: _______________

Color: _______________ (typically muted)
Max Width: _______________ (e.g., max-w-2xl)
Margin Top: _______________

### CTA Buttons Configuration

Layout: [Horizontal / Vertical / Stack on mobile]
Spacing: _______________ (gap between buttons)
Alignment: [Center / Left / Right]

Primary CTA:
- Default Text: _______________
- Size: _______________ (e.g., lg, xl)
- Icon: [Yes/No] _______________
- Icon Position: [Left/Right]
- Full Width on Mobile: [Yes/No]

Secondary CTA:
- Default Text: _______________
- Variant: [Secondary / Outline / Ghost / Link]
- Size: _______________
- Icon: [Yes/No] _______________

Mobile Adjustments:
- Layout: [Stacked / Horizontal]
- Button Width: [Full width / Auto]
- Order: [Primary first / Secondary first]

### Visual Element

Show Visual: [Yes/No]

Position: [Right / Center / Background / Floating]
Size: _______________ (e.g., w-full, w-3/4)

If Image:
- Border Radius: _______________
- Shadow: _______________
- Animation: [Float / Parallax / None]

If Video:
- Autoplay: [Yes/No]
- Loop: [Yes/No]
- Muted: [Yes/No]
- Controls: [Show/Hide]
- Poster Image: _______________

Mockup Frame: [Browser / Phone / Laptop / Dashboard / None]
Mockup Style: _______________

### Background Configuration

Background Type: [Solid / Gradient / Pattern / Mesh / Animated]

If Solid:
- Color: _______________ (semantic token)

If Gradient:
- Direction: _______________ (e.g., to-br)
- From: _______________
- Via: _______________ (optional)
- To: _______________

If Pattern:
- Type: [Grid / Dots / Blobs / Custom SVG]
- Opacity: _______________

Decorative Elements:
- [ ] Gradient orbs
- [ ] Geometric shapes
- [ ] Grid lines
- [ ] Blob shapes
- [ ] Custom SVG elements

Animation: [Static / Subtle movement / Parallax / Interactive]

### Social Proof in Hero

Show Social Proof: [Yes/No]

Type: [Logos / Metrics / Rating / Testimonial quote]

Position: [Below CTAs / Above CTAs / Bottom of hero]

If Logos:
- Number: _______________
- Layout: [Row / Grid / Marquee]
- Text: _______________ (e.g., "Trusted by 1000+ companies")
- Logo Style: [Color / Grayscale / Monochrome]

If Metrics:
- Metric 1: _______________
- Metric 2: _______________
- Metric 3: _______________
- Layout: [Horizontal pills / Grid / Inline]

If Rating:
- Stars: _______________
- Platform: _______________
- Review Count: _______________

### Scroll Indicator

Show Indicator: [Yes/No]

If Yes:
- Type: [Animated arrow / Mouse icon / Text / Custom]
- Position: [Bottom center]
- Animation: [Bounce / Pulse / None]
- Text: _______________ (optional, e.g., "Scroll to explore")

---

## COMPONENT 4.2.2: ABOVE-THE-FOLD HERO

### Component Props

```typescript
interface AboveFoldHeroProps {
  headline: string;
  subheadline?: string;
  primaryCta: CTAConfig;
  secondaryCta?: CTAConfig;
  visual?: VisualConfig;
  features?: string[];
  socialProof?: SocialProofConfig;
  compact?: boolean;
}
```

### Visual Design

Height: [Auto / 70vh / 600px]
Padding:
- Top: _______________ (e.g., pt-24, pt-32)
- Bottom: _______________ (e.g., pb-16, pb-24)

Layout: [Same options as Full-Screen Hero]
Optimized For: [Fast load / Quick conversion]

Key Differences from Full-Screen:
- Shorter height (leaves room for content below fold)
- More compact spacing
- Often includes feature list or benefits
- Less decorative elements

### Feature List (Optional)

Show Features: [Yes/No]

Number of Features: _______________

Layout: [Checkmarks in row / Icon list / Pills]

Feature 1: _______________
Feature 2: _______________
Feature 3: _______________
[Continue...]

Styling:
- Icon: _______________ (e.g., Check, Star)
- Icon Color: _______________
- Font Size: _______________
- Spacing: _______________

---

## COMPONENT 4.2.3: SPLIT HERO

### Component Props

```typescript
interface SplitHeroProps {
  headline: string;
  subheadline?: string;
  description?: string;
  features?: string[];
  primaryCta: CTAConfig;
  secondaryCta?: CTAConfig;
  visual: VisualConfig;
  visualPosition?: 'left' | 'right';
  ratio?: '50-50' | '60-40' | '40-60';
}
```

### Layout Configuration

Split Ratio: [50-50 / 60-40 / 40-60]
Visual Position: [Left / Right]

Grid Layout:
- Desktop: _______________ (e.g., grid-cols-2)
- Tablet: _______________ (e.g., grid-cols-1 or grid-cols-2)
- Mobile: [Stacked / Visual first / Content first]

Gap: _______________ (e.g., gap-12, gap-16)
Alignment: [Center / Top / Custom]

### Content Side

Max Width: _______________ (may constrain for readability)
Padding: _______________

Vertical Alignment: [Center / Top / Bottom]

Content Order:
1. Headline
2. Subheadline
3. Description/Features
4. CTAs
5. Social Proof (optional)

### Visual Side

Visual Type: [Product screenshot / Illustration / Video / Multiple images]

Styling:
- Aspect Ratio: _______________ (e.g., aspect-video, aspect-square)
- Border Radius: _______________
- Shadow: _______________
- Animation: [Float / Fade in / None]

Multiple Images: [Yes/No]
If Yes:
- Layout: [Overlapping / Grid / Stacked]
- Animation: [Parallax / Stagger / None]

---

## COMPONENT 4.2.4: MINIMAL HERO

### Component Props

```typescript
interface MinimalHeroProps {
  headline: string;
  description?: string;
  breadcrumbs?: BreadcrumbItem[];
  background?: 'default' | 'muted' | 'accent';
}
```

### Visual Design

Use Case: [Internal pages / Blog / Documentation]

Height: [Auto / 200px / 300px]
Padding: _______________

Layout: [Centered / Left-aligned]

Content:
- Headline only: [Most common]
- Optional: Short description
- Optional: Breadcrumbs above headline

Styling:
- Background: _______________ (typically muted)
- Border: [Bottom border / None]

---

## COMPONENT 4.2.5: VIDEO HERO

### Component Props

```typescript
interface VideoHeroProps {
  headline: string;
  subheadline?: string;
  videoSrc: string;
  videoPoster?: string;
  videoType?: 'background' | 'featured';
  primaryCta: CTAConfig;
  secondaryCta?: CTAConfig;
  overlay?: boolean;
  overlayColor?: string;
  overlayOpacity?: number;
}
```

### Video Configuration

Video Type: [Background video / Featured video player]

If Background Video:
- Source: _______________
- Format: [MP4 / WebM / Multiple]
- Autoplay: [Yes - muted]
- Loop: [Yes]
- Playback Rate: _______________ (optional slow-mo effect)
- Mobile Behavior: [Play / Fallback to image / Hide]

Overlay:
- Show: [Yes/No]
- Color: _______________
- Opacity: _______________ (e.g., 0.5, 0.7)
- Gradient: [Yes/No]

If Featured Video:
- Position: [Center / Side]
- Size: _______________
- Controls: [Yes/No]
- Thumbnail: _______________
- Play Button Style: _______________

### Content Positioning

Z-Index: [Above video]
Text Shadow: [Yes/No] _______________ (for readability)
Text Color: [Light / Dark based on video]

---

## COMPONENT 4.2.6: PRIMARY CTA BUTTON

### Component Props

```typescript
interface PrimaryCTAProps {
  text: string;
  href?: string;
  onClick?: () => void;
  icon?: LucideIcon;
  iconPosition?: 'left' | 'right';
  size?: 'sm' | 'md' | 'lg' | 'xl';
  fullWidth?: boolean;
  loading?: boolean;
  disabled?: boolean;
  ariaLabel?: string;
}
```

### Visual Design

Sizes:

Small (sm):
- Padding: _______________
- Font Size: _______________
- Height: _______________

Medium (md) - Default:
- Padding: _______________
- Font Size: _______________
- Height: _______________

Large (lg):
- Padding: _______________
- Font Size: _______________
- Height: _______________

Extra Large (xl):
- Padding: _______________
- Font Size: _______________
- Height: _______________

Styling:
- Background: [primary semantic token]
- Text Color: [primary-foreground semantic token]
- Border: _______________
- Border Radius: _______________ (use design system)
- Font Weight: _______________ (e.g., font-semibold, font-bold)
- Shadow: _______________ (optional)

### States

Hover:
- Background: _______________ (e.g., opacity-90)
- Transform: _______________ (e.g., scale-105, translateY(-2px))
- Shadow: _______________ (increase shadow)
- Transition: _______________ (e.g., all 200ms ease)

Active:
- Transform: _______________ (e.g., scale-95)
- Background: _______________

Focus:
- Outline: [Ring / Border / Custom]
- Ring Color: _______________ (semantic token)
- Ring Width: _______________
- Ring Offset: _______________

Disabled:
- Opacity: _______________
- Cursor: not-allowed
- Pointer Events: none

Loading:
- Show Spinner: [Yes/No]
- Spinner Position: [Replace text / Left of text]
- Text: [Hide / Show / Change to "Loading..."]

### Icon Configuration

Show Icon: [Optional]
Icon Size: _______________
Icon Spacing: _______________ (gap from text)

Icon Animations:
- Hover: [Move / Scale / Rotate / None]
- Example: [Arrow moves right on hover]

---

## COMPONENT 4.2.7: SECONDARY CTA BUTTON

### Component Props

[Same as PrimaryCTA but with different styling]

### Visual Design

Variant Options:

Secondary:
- Background: [secondary semantic token]
- Text Color: [secondary-foreground]
- Border: _______________

Outline:
- Background: [Transparent]
- Text Color: [foreground or primary]
- Border: [2px solid primary or border]
- Hover Background: [muted]

Ghost:
- Background: [Transparent]
- Text Color: [foreground or primary]
- Border: [None]
- Hover Background: [muted]
- Padding: [Less than primary]

Link Style:
- Background: [None]
- Text Color: [primary]
- Underline: [On hover / Always / Never]
- Padding: [Minimal]

[Other specifications same as Primary CTA]

---

## COMPONENT 4.2.8: CTA SECTION

### Component Props

```typescript
interface CTASectionProps {
  headline: string;
  description?: string;
  primaryCta: CTAConfig;
  secondaryCta?: CTAConfig;
  background?: BackgroundConfig;
  centered?: boolean;
  features?: string[];
  visual?: VisualConfig;
  size?: 'compact' | 'standard' | 'large';
}
```

### Visual Design

Use Case: [Bottom of page / Between sections / Standalone section]

Layout: [Centered / Split / Card overlay]

Padding:
- Vertical: _______________
- Horizontal: _______________

Background Options:
- Solid Color: _______________
- Gradient: _______________
- Pattern: _______________
- Accent Color: [Yes/No]

Container:
- Max Width: _______________
- Border Radius: _______________ (if card style)
- Shadow: _______________ (if card style)
- Border: _______________

### Content Layout

Alignment: [Center / Left]

Headline:
- Font Size: _______________
- Font Weight: _______________
- Color: _______________
- Max Width: _______________

Description:
- Font Size: _______________
- Color: _______________ (typically muted)
- Max Width: _______________
- Margin: _______________

CTAs:
- Layout: [Horizontal / Vertical]
- Spacing: _______________
- Alignment: [Center / Left]

Additional Elements:
- [ ] Feature list
- [ ] Social proof metrics
- [ ] Trust badges
- [ ] Visual element
- [ ] Timer/urgency element

---

## COMPONENT 4.2.9: INLINE CTA

### Component Props

```typescript
interface InlineCTAProps {
  text: string;
  ctaText: string;
  href?: string;
  onClick?: () => void;
  variant?: 'banner' | 'card' | 'text';
  dismissible?: boolean;
  icon?: string;
}
```

### Visual Design

Use Case: [Within content / End of article / Side of content]

Variant Options:

Banner Style:
- Width: [Full width / Container width]
- Padding: _______________
- Background: [Accent / Muted / Gradient]
- Border: _______________
- Position: [Inline / Sticky top / Sticky bottom]

Card Style:
- Padding: _______________
- Background: _______________
- Border: _______________
- Border Radius: _______________
- Shadow: _______________

Text Style:
- Layout: [Inline with content]
- Icon: [Optional]
- Text Color: [Primary]
- Arrow: [Yes/No]

### Content

Text: _______________
CTA Text: _______________
Layout: [Text + Button / All text with link]

Dismissible: [Yes/No]
If Yes:
- Close Button Position: [Top right]
- Remember Dismissal: [Session / Permanent]

---

## COMPONENT 4.2.10: STICKY CTA BAR

### Component Props

```typescript
interface StickyCTABarProps {
  text: string;
  ctaText: string;
  href?: string;
  onClick?: () => void;
  position?: 'top' | 'bottom';
  showAfterScroll?: number;
  hideAfterScroll?: number;
  dismissible?: boolean;
}
```

### Visual Design

Position: [Top / Bottom]
Show After Scroll: _______________ px
Hide After Scroll: _______________ px (optional, hides at page bottom)

Styling:
- Background: _______________
- Padding: _______________
- Shadow: _______________
- Border: _______________

Z-Index: 1050 (above navigation)

Layout:
- Container: [Full width / Container width]
- Content Layout: [Text left, CTA right / Centered / Custom]

Mobile Adjustments:
- Text: [Shorter / Hide on small screens]
- Layout: [Stacked / Horizontal]
- Button: [Full width / Auto]

Animation:
- Entrance: [Slide / Fade]
- Exit: [Slide / Fade]
- Duration: _______________

Dismissible: [Yes/No]
If Yes:
- Close Button: [X icon]
- Remember: [Session / Permanent]

---

## SHARED SPECIFICATIONS

### Accessibility Requirements

All Components Must Include:
- [ ] Semantic HTML (button, a tags)
- [ ] ARIA labels for icons-only buttons
- [ ] Keyboard accessible (Enter, Space)
- [ ] Focus indicators visible
- [ ] Color contrast WCAG AA (4.5:1 minimum)
- [ ] Screen reader friendly
- [ ] Touch targets 44x44px minimum
- [ ] Loading states announced
- [ ] Error states handled

### Animation Configuration

Respect Reduced Motion:
- Check: prefers-reduced-motion
- Alternative: [Instant transitions / Shorter duration]

Default Animations:
- Duration: [150ms-300ms]
- Easing: [ease-in-out / ease-out]

### Responsive Behavior

Mobile (<768px):
- Hero height: [Reduced / Auto]
- Button size: [Full width or Large]
- Text size: [Responsive scale]
- Spacing: [Reduced]
- Visual: [Smaller / Below text / Hidden]

Tablet (768-1024px):
- Split heroes: [May stack or maintain split]
- Button size: [Large]

Desktop (>1024px):
- Full specified design
- Max widths applied
- Optimal spacing

### Performance Optimization

- [ ] Lazy load below-fold content
- [ ] Optimize hero images (WebP, responsive)
- [ ] Defer video loading
- [ ] Minimize animation jank
- [ ] Preload critical assets
- [ ] Avoid layout shift

### Testing Requirements

Test Cases:
- [ ] CTAs clickable and lead to correct destination
- [ ] Animations smooth on all devices
- [ ] Text readable at all sizes
- [ ] Buttons accessible via keyboard
- [ ] Loading states display correctly
- [ ] Mobile layout doesn't break
- [ ] Video plays/pauses correctly
- [ ] Sticky CTA shows at right time
- [ ] Dismissible elements remember state

### Analytics Tracking

Track Events:
- Hero CTA clicks
- Secondary CTA clicks
- Video plays (if video hero)
- Scroll depth (for sticky CTAs)
- CTA section visibility
- Inline CTA clicks

---

## USAGE EXAMPLES

```tsx
// Full Screen Hero
<FullScreenHero
  headline="Build better products faster"
  subheadline="The all-in-one platform for modern teams"
  primaryCta={{
    text: "Start free trial",
    href: "/signup",
    variant: "primary",
    size: "xl"
  }}
  secondaryCta={{
    text: "Watch demo",
    href: "/demo",
    variant: "outline",
    size: "xl",
    icon: "Play"
  }}
  visual={{
    type: "image",
    src: "/hero-screenshot.png",
    alt: "Product dashboard"
  }}
  socialProof={{
    type: "logos",
    text: "Trusted by 1000+ companies",
    logos: [...]
  }}
  scrollIndicator={true}
/>

// Inline CTA
<InlineCTA
  text="Ready to get started?"
  ctaText="Start your free trial"
  href="/signup"
  variant="card"
/>
```

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
Create Hero Sections & CTA Components based on the completed specification.

CONTEXT: I have defined a comprehensive set of hero and CTA components for different use cases - from full-screen homepage heroes to inline CTAs and sticky bars.

TASK:
1. Create FullScreenHero component with headline, CTAs, and visual
2. Build AboveFoldHero optimized for quick conversion
3. Implement SplitHero with 50-50 or custom ratios
4. Create MinimalHero for internal pages
5. Build VideoHero with background or featured video
6. Implement PrimaryCTA button component
7. Create SecondaryCTA with multiple variants
8. Build CTASection for standalone conversion sections
9. Implement InlineCTA for content integration
10. Create StickyCTABar with scroll triggers

GUIDELINES:
- Mobile-first responsive design
- Use semantic tokens from design system
- Smooth animations with reduced-motion support
- Strong visual hierarchy
- High-contrast CTAs that stand out
- Accessibility: keyboard navigation, ARIA labels
- Performance: optimize images and videos
- Touch-friendly button sizes (44px min)

CONSTRAINTS:
- Hero must load fast (LCP < 2.5s)
- Videos optimized for web
- No layout shift during load
- CTAs must be keyboard accessible
- Color contrast WCAG AA compliant
- Works on all modern browsers
- Responsive at all breakpoints

[Paste your filled hero/CTA template here]

EXPECTED DELIVERABLES:
1. FullScreenHero component
2. AboveFoldHero component
3. SplitHero component
4. MinimalHero component
5. VideoHero component
6. PrimaryCTA button
7. SecondaryCTA button with variants
8. CTASection component
9. InlineCTA component
10. StickyCTABar component
```

---

## 📝 USAGE INSTRUCTIONS

1. **Hero = first impression** - make it count
2. **One clear message** - don't overwhelm
3. **Strong CTA** - action-oriented text
4. **Social proof early** - builds immediate trust
5. **Mobile-first** - most traffic is mobile
6. **Fast load** - hero impacts LCP metric
7. **Test CTAs** - small changes = big conversion impact
8. **Visual quality** - low-res images hurt credibility

---

## 💡 BEST PRACTICES

- Hero headline should communicate value in 5 seconds
- Primary CTA should use action verbs ("Start", "Get", "Try")
- Contrasting CTA color increases clicks
- Video heroes need fallback image for mobile
- Split heroes: visual on right performs better (F-pattern)
- Social proof in hero increases conversion by 15-30%
- Sticky CTA bars effective but can annoy - use sparingly
- A/B test hero variations - huge impact on conversion
- Keep CTAs above the fold on mobile
- Use "Start free trial" not "Submit" or "Learn more"
- Secondary CTA should be less prominent but still visible
- Inline CTAs work great at natural decision points
- Full-screen heroes work for landing pages, not content pages

---

## ⚠️ CRITICAL REMINDERS

- Hero is single most important conversion element
- CTA button text dramatically impacts conversion
- Social proof in hero builds immediate trust
- Mobile hero height shouldn't fill entire screen (uncomfortable)
- Video backgrounds must be optimized (file size)
- Loading state must look good while hero loads
- Color contrast on CTAs non-negotiable
- Touch targets must be 44x44px minimum on mobile
- Test hero on real devices, not just browser
- Sticky CTAs can be annoying - use scroll triggers wisely
- Analytics essential - track all CTA clicks
- A/B test everything - hero has massive ROI
- Don't use too many CTAs - creates decision paralysis
- Primary CTA should always be more prominent
- Hero text must be readable on all backgrounds
