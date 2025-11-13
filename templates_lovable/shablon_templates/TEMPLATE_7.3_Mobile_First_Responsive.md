# TEMPLATE 7.3: MOBILE-FIRST RESPONSIVE GUIDELINES

## 📋 PURPOSE
This template provides comprehensive mobile-first responsive design guidelines to ensure your website works flawlessly across all devices, screen sizes, and orientations.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Implement Mobile-First Responsive Design based on the following specification:

## RESPONSIVE DESIGN PHILOSOPHY

Design Approach: Mobile-First
- Start with mobile (320px)
- Progressively enhance for larger screens
- Content parity across devices
- Performance-first on mobile

Target Devices:

Mobile Phones:
- Small: 320px - 374px (iPhone SE, small Android)
- Medium: 375px - 413px (iPhone 12/13/14, most Android)
- Large: 414px+ (iPhone Plus/Max, large Android)
- Orientation: Portrait primary, landscape secondary

Tablets:
- Small: 768px - 834px (iPad Mini, small tablets)
- Large: 1024px - 1366px (iPad, iPad Pro, large tablets)
- Orientation: Both portrait and landscape

Desktop:
- Small: 1280px - 1439px (small laptops)
- Medium: 1440px - 1919px (standard desktop)
- Large: 1920px+ (large desktop, external monitors)

---

## BREAKPOINT SYSTEM

### Tailwind Default Breakpoints

Use Tailwind's default breakpoints:

```
sm:  640px  (Mobile landscape, small tablets)
md:  768px  (Tablets)
lg:  1024px (Desktop)
xl:  1280px (Large desktop)
2xl: 1536px (Extra large screens)
```

### Breakpoint Strategy

Base Styles (Mobile): 0px - 639px
- No prefix needed
- Default styles apply to mobile
- Example: `text-sm p-4`

Small (sm:): 640px+
- Mobile landscape, phablets
- Minor adjustments
- Example: `sm:text-base sm:p-6`

Medium (md:): 768px+
- Tablets, small desktops
- Significant layout changes
- Two-column layouts emerge
- Example: `md:grid-cols-2 md:text-lg`

Large (lg:): 1024px+
- Standard desktop
- Multi-column layouts
- Sidebar navigation possible
- Example: `lg:grid-cols-3 lg:text-xl`

Extra Large (xl:): 1280px+
- Large desktop
- Maximum content width
- Example: `xl:grid-cols-4`

2X Large (2xl:): 1536px+
- Very large screens
- Container constraints important
- Example: `2xl:max-w-7xl`

Custom Breakpoints (if needed):
```javascript
// tailwind.config.js
theme: {
  screens: {
    'xs': '475px',
    // ... other custom breakpoints
  }
}
```

Custom breakpoints needed: [Yes/No]
If Yes:
- xs: _______________ px
- Other: _______________ px

---

## LAYOUT PATTERNS

### Container System

Container Configuration:

Max Width Strategy:
- Mobile (base): 100% (no max-width)
- sm: 640px
- md: 768px
- lg: 1024px
- xl: 1280px
- 2xl: 1536px

Tailwind Container:
```jsx
<div className="container mx-auto px-4 sm:px-6 lg:px-8">
  {/* Content */}
</div>
```

Padding Strategy:
- Mobile: px-4 (16px)
- Tablet: px-6 (24px)
- Desktop: px-8 (32px)

Content Max Width:
- Text content: max-w-prose (65ch)
- Regular content: max-w-7xl (1280px)
- Wide content: max-w-screen-2xl

### Grid Systems

Mobile-First Grid Example:

Basic Grid:
```jsx
<div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 md:gap-6 lg:gap-8">
  {/* Items */}
</div>
```

Grid Patterns by Section:

Hero Section:
- Mobile: 1 column (text + image stacked)
- Tablet: 1 column OR 2 columns
- Desktop: 2 columns (text left, image right)

Features Grid:
- Mobile: 1 column
- Tablet: 2 columns
- Desktop: 3 columns
- Large Desktop: 4 columns

Pricing Cards:
- Mobile: 1 column (cards stacked)
- Tablet: 2 columns
- Desktop: 3 columns (if 3 plans) OR 4 columns (if 4 plans)

Team Grid:
- Mobile: 1 column OR 2 columns
- Tablet: 3 columns
- Desktop: 4 columns

Blog/Article Grid:
- Mobile: 1 column
- Tablet: 2 columns
- Desktop: 3 columns

Testimonials:
- Mobile: 1 column (carousel)
- Tablet: 2 columns
- Desktop: 3 columns

### Flexbox Patterns

Navigation:
```jsx
<nav className="flex flex-col md:flex-row items-start md:items-center gap-4 md:gap-6">
  {/* Nav items */}
</nav>
```

Card Layout:
```jsx
<div className="flex flex-col md:flex-row gap-6">
  <div className="flex-1">{/* Content */}</div>
  <div className="flex-1">{/* Content */}</div>
</div>
```

Split Sections:
```jsx
<section className="flex flex-col lg:flex-row items-center gap-8 lg:gap-12">
  <div className="flex-1">{/* Text */}</div>
  <div className="flex-1">{/* Image */}</div>
</section>
```

---

## TYPOGRAPHY RESPONSIVE SCALE

### Heading Sizes

H1 (Page Title):
```jsx
className="text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-bold"
```
- Mobile: 30px (text-3xl)
- Small: 36px (text-4xl)
- Tablet: 48px (text-5xl)
- Desktop: 60px (text-6xl)

H2 (Section Title):
```jsx
className="text-2xl sm:text-3xl md:text-4xl lg:text-5xl font-bold"
```
- Mobile: 24px (text-2xl)
- Small: 30px (text-3xl)
- Tablet: 36px (text-4xl)
- Desktop: 48px (text-5xl)

H3 (Subsection):
```jsx
className="text-xl sm:text-2xl md:text-3xl font-semibold"
```
- Mobile: 20px (text-xl)
- Small: 24px (text-2xl)
- Tablet: 30px (text-3xl)
- Desktop: 30px (text-3xl)

H4 (Card Title):
```jsx
className="text-lg sm:text-xl md:text-2xl font-semibold"
```
- Mobile: 18px (text-lg)
- Small: 20px (text-xl)
- Tablet: 24px (text-2xl)

Body Text:
```jsx
className="text-base md:text-lg"
```
- Mobile: 16px (text-base)
- Tablet+: 18px (text-lg)

Small Text:
```jsx
className="text-sm md:text-base"
```
- Mobile: 14px (text-sm)
- Tablet+: 16px (text-base)

Line Height:
- Headings: leading-tight (1.25)
- Body: leading-relaxed (1.625)
- Small text: leading-normal (1.5)

### Text Alignment

Text Alignment Strategy:
```jsx
className="text-left md:text-center lg:text-left"
```

Patterns:
- Mobile: text-left (easier to read)
- Tablet: May center for hero/CTAs
- Desktop: Depends on layout

Hero Section:
```jsx
className="text-center lg:text-left"
```

Features:
```jsx
className="text-center md:text-left"
```

Body Content:
```jsx
className="text-left"
```
(Always left-aligned for readability)

---

## SPACING SYSTEM

### Section Spacing

Vertical Section Padding:
```jsx
className="py-12 md:py-16 lg:py-24"
```
- Mobile: 48px (py-12)
- Tablet: 64px (py-16)
- Desktop: 96px (py-24)

Section Gap (Between Sections):
```jsx
className="space-y-12 md:space-y-16 lg:space-y-24"
```

### Element Spacing

Between Elements:
```jsx
className="space-y-4 md:space-y-6 lg:space-y-8"
```
- Mobile: 16px
- Tablet: 24px
- Desktop: 32px

Gap in Grids:
```jsx
className="gap-4 md:gap-6 lg:gap-8"
```
- Mobile: 16px
- Tablet: 24px
- Desktop: 32px

Card Padding:
```jsx
className="p-4 md:p-6 lg:p-8"
```
- Mobile: 16px
- Tablet: 24px
- Desktop: 32px

Button Padding:
```jsx
className="px-4 py-2 md:px-6 md:py-3"
```
- Mobile: 16px x 8px
- Tablet+: 24px x 12px

### Margin & Padding Patterns

Container Padding:
```jsx
className="px-4 sm:px-6 lg:px-8"
```

Content Max Width with Padding:
```jsx
className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8"
```

Vertical Spacing:
```jsx
className="mt-8 md:mt-12 lg:mt-16"
```

---

## COMPONENT RESPONSIVE PATTERNS

### Navigation

Mobile Navigation:
```jsx
// Mobile: Hamburger menu
<div className="lg:hidden">
  <button>☰</button>
  {/* Mobile menu */}
</div>

// Desktop: Horizontal menu
<nav className="hidden lg:flex gap-6">
  {/* Nav items */}
</nav>
```

Navigation Items Visibility:
```jsx
className="flex flex-col lg:flex-row gap-4 lg:gap-6"
```

### Hero Section

Hero Layout:
```jsx
<section className="flex flex-col lg:flex-row items-center gap-8 lg:gap-12">
  {/* Text content */}
  <div className="flex-1 text-center lg:text-left">
    <h1 className="text-4xl md:text-5xl lg:text-6xl font-bold">
      {/* Title */}
    </h1>
    {/* CTAs */}
    <div className="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
      {/* Buttons */}
    </div>
  </div>
  
  {/* Visual */}
  <div className="flex-1">
    {/* Image/Video */}
  </div>
</section>
```

Hero Image:
```jsx
className="w-full lg:w-auto"
```

CTA Buttons:
```jsx
className="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start"
```

### Cards

Card Grid:
```jsx
<div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
  <div className="bg-white p-6 rounded-lg shadow">
    {/* Card content */}
  </div>
</div>
```

Card Content:
```jsx
<div className="flex flex-col space-y-4">
  <img className="w-full h-48 object-cover rounded" />
  <h3 className="text-xl md:text-2xl font-semibold">Title</h3>
  <p className="text-base md:text-lg">Description</p>
</div>
```

### Forms

Form Layout:
```jsx
<form className="space-y-4 md:space-y-6 max-w-lg mx-auto">
  {/* Mobile: Full width, stacked */}
  {/* Desktop: May use multi-column for related fields */}
</form>
```

Input Fields:
```jsx
<input 
  className="w-full px-4 py-2 md:py-3 text-base md:text-lg rounded-lg border"
/>
```

Form Buttons:
```jsx
<button className="w-full sm:w-auto px-6 py-3 text-base md:text-lg">
  Submit
</button>
```

Multi-Column Form (Desktop):
```jsx
<div className="grid grid-cols-1 md:grid-cols-2 gap-4">
  <input /> {/* First name */}
  <input /> {/* Last name */}
</div>
```

### Images

Responsive Images:
```jsx
<img 
  className="w-full h-auto md:w-1/2 lg:w-1/3"
  srcSet="image-400w.webp 400w, image-800w.webp 800w, image-1200w.webp 1200w"
  sizes="(max-width: 640px) 100vw, (max-width: 1024px) 50vw, 33vw"
/>
```

Image Aspect Ratio:
```jsx
<div className="aspect-w-16 aspect-h-9">
  <img className="object-cover" />
</div>
```

### Tables

Mobile-Friendly Tables:

Option 1: Horizontal Scroll
```jsx
<div className="overflow-x-auto">
  <table className="min-w-full">
    {/* Table content */}
  </table>
</div>
```

Option 2: Card Layout on Mobile
```jsx
// Mobile: Stack as cards
// Desktop: Table layout
<div className="block md:table w-full">
  {/* Transforms table to cards on mobile */}
</div>
```

Option 3: Hide Columns on Mobile
```jsx
<th className="hidden md:table-cell">Column</th>
```

### Modals/Dialogs

Modal Sizing:
```jsx
<div className="w-full max-w-sm sm:max-w-md md:max-w-lg lg:max-w-xl">
  {/* Modal content */}
</div>
```

Modal Position:
- Mobile: Full screen OR bottom sheet
- Desktop: Centered overlay

---

## TOUCH & INTERACTION

### Touch Targets

Minimum Touch Target Size:
- Buttons: 44x44px minimum
- Links: 44x44px minimum (add padding if needed)
- Icons: 44x44px minimum
- Form inputs: 44px height minimum

Implementation:
```jsx
className="min-h-[44px] min-w-[44px] flex items-center justify-center"
```

Button Sizing:
```jsx
// Small
className="px-4 py-2 text-sm"
// Medium (default)
className="px-6 py-3 text-base"
// Large
className="px-8 py-4 text-lg"
```

Touch Target Spacing:
Minimum 8px between touch targets:
```jsx
className="space-x-2"  // 8px between
className="gap-4"      // 16px between (better)
```

### Hover States

Mobile (No Hover):
```jsx
className="active:scale-95 transition-transform"
```
Use active states instead of hover

Desktop (With Hover):
```jsx
className="hover:bg-blue-600 transition-colors"
```

Combined (Mobile + Desktop):
```jsx
className="active:scale-95 lg:hover:bg-blue-600 transition-all"
```

### Gestures

Swipe Support:
For carousels, image galleries:
- Touch-enabled swiping: [Yes]
- Arrow buttons for desktop: [Yes]
- Indicator dots: [Yes]

Pinch-to-Zoom:
- On images: [Allow for detail views]
- On main content: [Disabled]

Scroll Behavior:
- Smooth scroll: [Yes]
- Overscroll behavior: [Controlled]

---

## NAVIGATION PATTERNS

### Mobile Navigation

Hamburger Menu:
```jsx
<button className="lg:hidden p-2 text-2xl">
  ☰
</button>

// Mobile menu overlay
<div className="fixed inset-0 bg-white z-50 lg:hidden">
  {/* Mobile menu content */}
</div>
```

Mobile Menu Animation:
- Slide from right/left: [Yes]
- Fade in: [Yes]
- Smooth transition: [Yes]

Mobile Menu Layout:
```jsx
<nav className="flex flex-col space-y-4 p-6">
  {/* Stacked navigation items */}
</nav>
```

### Desktop Navigation

Horizontal Navigation:
```jsx
<nav className="hidden lg:flex items-center gap-6">
  {/* Navigation items */}
</nav>
```

Sticky Navigation:
```jsx
className="sticky top-0 z-50 bg-white shadow"
```

### Bottom Navigation (Mobile)

Mobile Bottom Nav:
```jsx
<nav className="fixed bottom-0 left-0 right-0 bg-white border-t lg:hidden">
  <div className="flex justify-around p-2">
    {/* Bottom nav items (4-5 max) */}
  </div>
</nav>
```

Use for: Mobile apps, content-heavy sites
Items: 3-5 maximum

---

## CONTENT ADAPTATION

### Text Content

Truncation:
```jsx
className="line-clamp-2 md:line-clamp-3"
```

Read More:
- Mobile: Shorter preview (2-3 lines)
- Desktop: Longer preview (4-5 lines)

### Media

Video Embeds:
```jsx
<div className="aspect-w-16 aspect-h-9">
  <iframe className="w-full h-full" />
</div>
```

Image Galleries:
- Mobile: Single image with swipe
- Desktop: Grid with hover preview

### Lists

List Display:
- Mobile: Vertical list (easier thumb scrolling)
- Desktop: Grid or multi-column

### Charts/Data Visualization

Responsive Charts:
- Mobile: Simplified version OR horizontal scroll
- Desktop: Full detailed version

Implementation:
```jsx
// Show simple version on mobile
<div className="block md:hidden">{/* Simple chart */}</div>
// Show complex version on desktop
<div className="hidden md:block">{/* Detailed chart */}</div>
```

---

## PERFORMANCE ON MOBILE

### Image Loading

Mobile-Specific Images:
Serve smaller images to mobile:
```jsx
<img
  srcSet="
    image-400w.webp 400w,
    image-800w.webp 800w,
    image-1600w.webp 1600w
  "
  sizes="
    (max-width: 640px) 100vw,
    (max-width: 1024px) 50vw,
    800px
  "
/>
```

Lazy Loading:
```jsx
loading="lazy"
```
On all below-fold images

### JavaScript

Mobile Performance:
- Reduce JS bundle for mobile: [Consider]
- Defer non-critical scripts: [Yes]
- Use Intersection Observer: [Yes]

### CSS

Critical CSS:
Inline critical CSS for above-fold content

Unused CSS:
Remove with PurgeCSS/Tailwind purge

### Network

Slow Network Handling:
- Show loading states: [Yes]
- Graceful degradation: [Yes]
- Offline message: [Yes/No]

---

## TESTING REQUIREMENTS

### Device Testing

Real Device Testing:
- [ ] iPhone 12/13/14 (375px)
- [ ] iPhone SE (small, 320px)
- [ ] iPhone Pro Max (large)
- [ ] Android (Samsung, Pixel)
- [ ] iPad (768px)
- [ ] iPad Pro (1024px)
- [ ] Desktop (1920px)

Emulator Testing:
- [ ] Chrome DevTools device emulation
- [ ] Firefox Responsive Design Mode
- [ ] Safari Responsive Design Mode

### Orientation Testing

Test Both Orientations:
- [ ] Portrait (primary)
- [ ] Landscape (secondary)

Landscape Considerations:
- Navigation still accessible: [Yes]
- Content readable: [Yes]
- No horizontal scrolling: [Yes]

### Browser Testing

Mobile Browsers:
- [ ] Safari (iOS)
- [ ] Chrome (Android)
- [ ] Samsung Internet
- [ ] Firefox (Android)

Desktop Browsers:
- [ ] Chrome
- [ ] Firefox
- [ ] Safari
- [ ] Edge

### Responsive Checklist

- [ ] All breakpoints tested
- [ ] No horizontal scrolling
- [ ] Touch targets 44x44px minimum
- [ ] Text readable (16px minimum)
- [ ] Images responsive
- [ ] Forms usable on mobile
- [ ] Navigation accessible on all sizes
- [ ] Content parity across devices
- [ ] Performance acceptable on 3G
- [ ] Landscape orientation works
- [ ] Tables mobile-friendly
- [ ] Modals fit on small screens

---

## ACCESSIBILITY ON MOBILE

### Touch Accessibility

- Sufficient spacing between touch targets
- Large enough buttons/links
- Clear active/focus states
- No hover-only interactions

### Screen Reader

- Proper heading hierarchy
- Descriptive labels
- ARIA attributes where needed
- Focus management in modals

### Zoom

- Allow text zoom up to 200%
- Layout doesn't break when zoomed
- No fixed positioning that obscures content

### Motion

- Respect prefers-reduced-motion
- Provide pause controls for auto-play
- Avoid motion sickness triggers

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
Implement Mobile-First Responsive Design based on the completed specification.

CONTEXT: I have defined a comprehensive mobile-first responsive strategy ensuring the website works flawlessly on all devices from 320px mobile to 1920px+ desktop.

TASK:
1. Implement mobile-first styles using Tailwind breakpoints
2. Create responsive layouts with mobile (1 col) → tablet (2 col) → desktop (3-4 col)
3. Set responsive typography scale (text-3xl sm:text-4xl md:text-5xl lg:text-6xl)
4. Configure responsive spacing (py-12 md:py-16 lg:py-24)
5. Build hamburger menu for mobile, horizontal nav for desktop
6. Implement touch targets minimum 44x44px
7. Create responsive images with srcset and sizes
8. Design mobile-friendly forms (full width, proper input sizes)
9. Configure container max-widths and padding
10. Test on real devices across all breakpoints

GUIDELINES:
- Start with mobile styles (no prefix)
- Progressively enhance with md:, lg:, xl: prefixes
- Touch targets minimum 44x44px
- No horizontal scrolling on any device
- Text minimum 16px for readability
- Content parity (same features on mobile and desktop)
- Performance-first on mobile
- Test on real devices, not just emulator

CONSTRAINTS:
- Mobile: 320px minimum width
- Touch targets: 44x44px minimum
- Button tap area: 44x44px minimum
- Text size: 16px minimum for body
- No hover-only interactions on mobile
- Forms must be usable with touch
- No horizontal scrolling
- Test on iPhone SE (small), iPhone 14, iPad, desktop

[Paste your filled mobile-first responsive template here]

EXPECTED DELIVERABLES:
1. Mobile-first responsive layouts
2. Proper Tailwind breakpoint usage
3. Responsive typography scale
4. Responsive spacing system
5. Mobile hamburger menu + desktop nav
6. Touch-friendly buttons (44x44px)
7. Responsive images with srcset
8. Mobile-friendly forms
9. Container system with proper padding
10. Tested on multiple devices
```

---

## 📝 USAGE INSTRUCTIONS

1. **Design mobile first** - start with smallest screen, enhance upward
2. **Use Tailwind breakpoints** - sm:, md:, lg:, xl:, 2xl:
3. **Test on real devices** - emulators don't catch everything
4. **Touch targets matter** - 44x44px minimum for usability
5. **Content parity** - same functionality on mobile and desktop
6. **Performance critical** - mobile users on slow networks
7. **Orientation testing** - both portrait and landscape
8. **Accessibility first** - mobile users use screen readers too

---

## 💡 BEST PRACTICES

- Mobile-first means starting with base styles, adding complexity
- Tailwind classes without prefix are mobile (0px+)
- Use container mx-auto px-4 sm:px-6 lg:px-8 for consistent spacing
- Hamburger menu on mobile, horizontal nav on desktop (lg:)
- Grid columns: 1 (mobile) → 2 (tablet) → 3-4 (desktop)
- Typography should scale up: text-3xl sm:text-4xl md:text-5xl
- Images need srcset and sizes for proper responsive loading
- Forms full-width on mobile, can be constrained on desktop
- Touch targets 44x44px minimum - add padding if needed
- Test with real fingers, not mouse cursor
- Landscape orientation often forgotten but important
- Tables need special handling on mobile (scroll or card layout)
- Modals should be full-screen or nearly full-screen on mobile
- Bottom navigation can be useful on mobile (4-5 items max)

---

## ⚠️ CRITICAL REMINDERS

- Mobile-first is not just CSS - it's a philosophy
- Most users are on mobile - optimize for mobile first
- Touch targets < 44x44px cause user frustration and errors
- Horizontal scrolling is always wrong (except intentional carousels)
- Text < 16px is hard to read on mobile
- Hover-only interactions don't work on touch devices
- Test on real devices - iOS and Android behave differently
- iPhone SE (320px) is smallest common device - test it
- Landscape orientation matters - test it
- Forms are harder on mobile - make inputs big enough
- Navigation is critical - hamburger menu must work flawlessly
- Content parity - mobile users expect same features as desktop
- Performance matters more on mobile (slow networks, slower devices)
- Google uses mobile-first indexing - mobile version affects SEO
- Tailwind breakpoints are min-width (mobile-first)
- Always test on actual devices before launch
- Responsive images save bandwidth on mobile - use srcset
- Grid/flexbox make responsive layouts easier than old techniques
- Container padding prevents content touching screen edges
- Breakpoints should be based on content, not specific devices
