# TEMPLATE 4.3: FEATURE CARDS & PRODUCT SHOWCASES

## 📋 PURPOSE
This template defines reusable components for displaying features, benefits, and product capabilities in visually appealing and scannable formats.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Create Feature Cards & Product Showcase Components based on the following specification:

## COMPONENT LIBRARY OVERVIEW

Component Set: Feature Cards & Product Showcases
Design System: [Reference to Template 1.2]
Framework: React + TypeScript
Styling: Tailwind CSS with semantic tokens

Components to Create:
1. Feature Card (Grid Item)
2. Feature List (Vertical)
3. Feature Comparison Card
4. Product Showcase Section
5. Before/After Comparison
6. Interactive Feature Demo
7. Bento Grid Layout
8. Icon Feature Block
9. Stats Display
10. Integration Showcase

---

## COMPONENT 4.3.1: FEATURE CARD (Grid Item)

### Component Props

```typescript
interface FeatureCardProps {
  icon: string | ReactNode;
  title: string;
  description: string;
  link?: {
    text: string;
    href: string;
  };
  badge?: string;
  variant?: 'default' | 'bordered' | 'elevated' | 'minimal';
  clickable?: boolean;
  featured?: boolean;
}
```

### Visual Design

Card Layout:
- Padding: _______________
- Border Radius: _______________ (use design system)
- Aspect Ratio: [Auto / Square / 4:3]
- Min Height: _______________ (for consistent grid)

Variant Styles:

Default:
- Background: _______________ (e.g., background semantic token)
- Border: [None / Subtle]
- Shadow: [None / Subtle]

Bordered:
- Background: _______________
- Border: [1px / 2px] [border semantic token]
- Shadow: [None]

Elevated:
- Background: _______________
- Border: [None]
- Shadow: _______________ (e.g., shadow-lg)

Minimal:
- Background: [Transparent]
- Border: [None]
- Shadow: [None]
- Hover: [Subtle background]

Featured (Highlighted):
- Background: [Accent gradient / Primary color]
- Border: [Thicker / Gradient]
- Shadow: [Stronger]
- Badge: [Optional "Popular" or "New"]

### Icon Configuration

Icon Type: [Lucide React icon / Custom SVG / Image / Emoji]

Styling:
- Size: _______________ (e.g., h-12 w-12, h-10 w-10)
- Color: _______________ (semantic token, e.g., primary)
- Background: [Circle / Square / None]

If Background:
- Background Color: _______________ (e.g., primary with opacity)
- Padding: _______________
- Border Radius: _______________

Gradient Icon: [Yes/No]
If Yes:
- Gradient: _______________ (e.g., from-primary to-accent)

Icon Position: [Top / Left / Center]
Margin: _______________ (spacing from text)

### Text Content

Title:
- Font Size: _______________
- Font Weight: _______________ (e.g., font-semibold, font-bold)
- Color: _______________ (foreground semantic token)
- Margin Top: _______________
- Margin Bottom: _______________

Description:
- Font Size: _______________
- Font Weight: _______________
- Color: _______________ (muted-foreground semantic token)
- Line Height: _______________
- Max Characters: _______________ (for consistency)

Link/CTA:
- Show: [Optional]
- Text: _______________ (e.g., "Learn more", "Explore")
- Style: [Text link / Button / Icon arrow]
- Icon: [Arrow / ChevronRight / External link]
- Color: _______________ (primary)
- Position: [Bottom / Below description]

Badge:
- Position: [Top right / Top left / Above title]
- Text: _______________
- Background: _______________
- Color: _______________
- Size: [Small / XS]
- Border Radius: _______________

### Hover & Interactive States

Clickable: [Yes/No]

If Clickable:
Hover Effects:
- Transform: _______________ (e.g., translateY(-4px), scale-105)
- Shadow: _______________ (increase shadow)
- Border: _______________ (change color if bordered)
- Background: _______________ (subtle change)
- Transition: _______________ (e.g., all 200ms ease)

Active State:
- Transform: _______________ (e.g., scale-98)

Focus State:
- Ring: _______________ (semantic ring token)
- Ring Offset: _______________

---

## COMPONENT 4.3.2: FEATURE LIST (Vertical)

### Component Props

```typescript
interface FeatureListProps {
  features: FeatureItem[];
  variant?: 'default' | 'icons' | 'numbers' | 'checkmarks';
  columns?: 1 | 2 | 3;
  spacing?: 'compact' | 'normal' | 'relaxed';
}

interface FeatureItem {
  title: string;
  description?: string;
  icon?: string;
  badge?: string;
}
```

### Visual Design

Layout: [Single column / Two columns / Three columns]
Spacing Between Items: _______________

Variant Styles:

Default (No indicator):
- Title only
- Optional description
- Clean, minimal

Icons:
- Icon on left
- Icon size: _______________
- Icon color: _______________
- Text alignment: [Left / Center]

Numbers:
- Numbered list (1, 2, 3...)
- Number styling: _______________
- Number background: [Circle / Square / None]
- Number color: _______________

Checkmarks:
- Checkmark icon on left
- Icon: [Check / CheckCircle / BadgeCheck]
- Icon color: _______________ (typically success color)
- Icon size: _______________

### Item Styling

Title:
- Font Size: _______________
- Font Weight: _______________
- Color: _______________
- Margin Bottom: _______________

Description (if shown):
- Font Size: _______________
- Color: _______________ (muted)
- Line Height: _______________
- Max Width: _______________

Spacing Options:

Compact:
- Gap between items: _______________

Normal:
- Gap between items: _______________

Relaxed:
- Gap between items: _______________

---

## COMPONENT 4.3.3: FEATURE COMPARISON CARD

### Component Props

```typescript
interface FeatureComparisonProps {
  title: string;
  plans: PlanComparison[];
  features: ComparisonFeature[];
  highlighted?: string; // plan to highlight
}

interface PlanComparison {
  name: string;
  icon?: string;
  color?: string;
}

interface ComparisonFeature {
  name: string;
  tooltip?: string;
  values: (boolean | string | number)[];
}
```

### Visual Design

Card Styling:
- Background: _______________
- Border: _______________
- Border Radius: _______________
- Padding: _______________
- Shadow: _______________

Header Row:
- Background: _______________
- Padding: _______________
- Border Bottom: _______________

Plan Name Styling:
- Font Size: _______________
- Font Weight: _______________
- Color: _______________
- Icon Size: _______________ (if showing icons)

Feature Rows:
- Background: [Alternating / All same]
- Padding: _______________
- Border Bottom: _______________
- Hover Background: _______________

Feature Name:
- Font Size: _______________
- Font Weight: _______________
- Width: _______________ (e.g., 40% of row)
- Tooltip Icon: [Info / HelpCircle]

Feature Values:
- Layout: [Evenly distributed]
- Alignment: [Center]
- Checkmark: [For Yes/true values]
- Cross: [For No/false values]
- Text: [For string/number values]

Highlighted Column:
- Background: _______________ (subtle accent)
- Border: _______________ (thicker or colored)
- Font Weight: [Bolder]

---

## COMPONENT 4.3.4: PRODUCT SHOWCASE SECTION

### Component Props

```typescript
interface ProductShowcaseProps {
  headline: string;
  description?: string;
  visual: {
    type: 'image' | 'video' | 'interactive';
    src: string;
    alt?: string;
  };
  features: string[];
  cta?: CTAConfig;
  visualPosition?: 'left' | 'right' | 'center';
  background?: BackgroundConfig;
}
```

### Layout Options

Layout Type: [Split / Centered / Asymmetric / Stacked]

Split Layout:
- Ratio: [50-50 / 60-40 / 40-60]
- Visual Position: [Left / Right]
- Vertical Alignment: [Center / Top / Bottom]
- Gap: _______________

Centered Layout:
- Visual: [Above text / Below text]
- Max Width: _______________
- Alignment: [Center]

### Visual Element

Visual Type: [Screenshot / Video / Interactive demo / Multiple images]

Styling:
- Border Radius: _______________
- Shadow: _______________
- Border: _______________
- Max Width: _______________

Mockup Frame: [Browser / Phone / Laptop / Tablet / Dashboard / None]
Frame Style: _______________

Animation:
- Type: [Float / Parallax / Fade in / None]
- Duration: _______________
- Trigger: [On scroll / On load / On hover]

### Content Side

Headline:
- Font Size: _______________
- Font Weight: _______________
- Color: _______________
- Max Width: _______________

Description:
- Font Size: _______________
- Color: _______________
- Max Width: _______________
- Margin: _______________

Feature List:
- Layout: [Checkmarks / Icons / Pills / None]
- Spacing: _______________
- Icon: _______________
- Icon Color: _______________

CTA (Optional):
- Show: [Yes/No]
- Position: [Below features / Inline]
- Button Config: _______________

---

## COMPONENT 4.3.5: BEFORE/AFTER COMPARISON

### Component Props

```typescript
interface BeforeAfterProps {
  headline: string;
  before: {
    label: string;
    description: string;
    visual?: string;
    points: string[];
  };
  after: {
    label: string;
    description: string;
    visual?: string;
    points: string[];
  };
  variant?: 'side-by-side' | 'slider';
}
```

### Visual Design

Variant Options:

Side-by-Side:
- Layout: [Two columns]
- Divider: [Line / Arrow / VS badge]
- Card Styling: _______________

Slider (Interactive):
- Type: [Image slider with handle]
- Handle Style: _______________
- Labels: [On hover / Always visible]

### Before Section

Label:
- Text: _______________ (e.g., "Before", "Without [Product]")
- Position: [Top / Inside card]
- Styling: _______________
- Background: _______________ (often muted or red-tint)

Visual:
- Show: [Optional]
- Styling: [Desaturated / Red tint / Normal]

Description:
- Font Size: _______________
- Color: _______________

Pain Points List:
- Icon: [X / AlertCircle / Frown]
- Icon Color: _______________ (destructive or warning)
- Styling: _______________

### After Section

Label:
- Text: _______________ (e.g., "After", "With [Product]")
- Position: [Top / Inside card]
- Styling: _______________
- Background: _______________ (often success color)

Visual:
- Show: [Optional]
- Styling: [Vibrant / Green tint / Normal]

Description:
- Font Size: _______________
- Color: _______________

Benefits List:
- Icon: [Check / CheckCircle / Smile]
- Icon Color: _______________ (success green)
- Styling: _______________

### Transition Element

Divider/Arrow:
- Type: [Arrow / Badge / Line / Icon]
- Position: [Center between cards]
- Text: [VS / → / Transform]
- Styling: _______________
- Animation: [Pulse / Bounce / None]

---

## COMPONENT 4.3.6: INTERACTIVE FEATURE DEMO

### Component Props

```typescript
interface InteractiveDemoProps {
  tabs?: TabConfig[];
  features?: FeatureConfig[];
  defaultActive?: string | number;
  autoplay?: boolean;
  autoplayInterval?: number;
}

interface TabConfig {
  id: string;
  label: string;
  icon?: string;
  content: {
    headline: string;
    description: string;
    visual: string;
    features?: string[];
  };
}
```

### Visual Design

Layout Type: [Tabs / Accordion / Slideshow / Carousel]

If Tabs:
Tab Position: [Top / Side / Bottom]

Tab Styling:
- Background (Inactive): _______________
- Background (Active): _______________
- Border (Active): _______________
- Color (Inactive): _______________
- Color (Active): _______________
- Padding: _______________
- Border Radius: _______________

Tab Layout:
- Direction: [Horizontal / Vertical]
- Spacing: _______________
- Indicator: [Underline / Background / Border]

Content Area:
- Background: _______________
- Padding: _______________
- Border: _______________
- Border Radius: _______________
- Min Height: _______________ (prevent layout shift)

Visual Display:
- Size: _______________
- Border Radius: _______________
- Shadow: _______________
- Animation: [Fade / Slide / Scale when switching]

Autoplay:
- Enabled: [Yes/No]
- Interval: _______________ ms
- Pause on Hover: [Yes/No]
- Progress Indicator: [Bar / Dots / None]

---

## COMPONENT 4.3.7: BENTO GRID LAYOUT

### Component Props

```typescript
interface BentoGridProps {
  items: BentoItem[];
  columns?: 2 | 3 | 4;
  gap?: number;
}

interface BentoItem {
  title: string;
  description?: string;
  visual?: string;
  icon?: string;
  size?: 'small' | 'medium' | 'large' | 'wide' | 'tall';
  featured?: boolean;
}
```

### Visual Design

Grid Configuration:
- Desktop Columns: _______________ (e.g., 3, 4)
- Tablet Columns: _______________
- Mobile Columns: [1 / 2]
- Gap: _______________

Item Size Classes:

Small:
- Grid Span: [1 column x 1 row]
- Min Height: _______________

Medium:
- Grid Span: [1 column x 2 rows] or [2 columns x 1 row]
- Min Height: _______________

Large:
- Grid Span: [2 columns x 2 rows]
- Min Height: _______________

Wide:
- Grid Span: [2-3 columns x 1 row]
- Min Height: _______________

Tall:
- Grid Span: [1 column x 2-3 rows]
- Min Height: _______________

### Item Styling

Card Base:
- Background: _______________
- Border: _______________
- Border Radius: _______________
- Padding: _______________
- Shadow: _______________

Content Layout:
- Vertical Alignment: [Top / Center / Bottom / Space between]
- Horizontal Alignment: [Left / Center]

Icon/Visual:
- Size: _______________ (scales with item size)
- Position: [Top / Floating / Background]
- Opacity: _______________ (if background)

Text:
- Title Size: _______________ (scales with item size)
- Title Weight: _______________
- Description Size: _______________
- Description Color: _______________

Featured Items:
- Background: [Gradient / Accent color]
- Border: [Thicker / Gradient]
- Shadow: [Stronger]
- Text Color: [Adjusted for contrast]

Hover Effect:
- Transform: _______________
- Shadow: _______________
- Border: _______________

---

## COMPONENT 4.3.8: ICON FEATURE BLOCK

### Component Props

```typescript
interface IconFeatureBlockProps {
  icon: string;
  title: string;
  description: string;
  layout?: 'vertical' | 'horizontal' | 'centered';
  iconStyle?: 'simple' | 'circle' | 'square' | 'gradient';
  size?: 'sm' | 'md' | 'lg';
}
```

### Visual Design

Layout Options:

Vertical:
- Icon: [Top]
- Text: [Below icon]
- Alignment: [Left / Center]

Horizontal:
- Icon: [Left]
- Text: [Right of icon]
- Alignment: [Top / Center]

Centered:
- Icon: [Center top]
- Text: [Centered below]
- Alignment: [Center]

### Icon Styling

Size Options:

Small:
- Icon Size: _______________
- Background Size: _______________

Medium:
- Icon Size: _______________
- Background Size: _______________

Large:
- Icon Size: _______________
- Background Size: _______________

Style Options:

Simple:
- Icon only
- Color: _______________

Circle:
- Background Shape: [Circle]
- Background Color: _______________
- Icon Color: _______________
- Padding: _______________

Square:
- Background Shape: [Rounded square]
- Background Color: _______________
- Icon Color: _______________
- Border Radius: _______________
- Padding: _______________

Gradient:
- Background: [Gradient]
- Gradient Colors: _______________
- Icon Color: [White / Contrast color]
- Padding: _______________

### Text Styling

Title:
- Font Size: _______________
- Font Weight: _______________
- Color: _______________
- Margin Top: _______________

Description:
- Font Size: _______________
- Color: _______________
- Line Height: _______________
- Max Width: _______________

---

## COMPONENT 4.3.9: STATS DISPLAY

### Component Props

```typescript
interface StatsDisplayProps {
  stats: StatItem[];
  layout?: 'horizontal' | 'grid' | 'featured';
  animated?: boolean;
  background?: BackgroundConfig;
}

interface StatItem {
  value: string | number;
  label: string;
  suffix?: string;
  prefix?: string;
  icon?: string;
  description?: string;
  highlighted?: boolean;
}
```

### Visual Design

Layout Options:

Horizontal:
- Direction: [Row]
- Spacing: _______________
- Dividers: [Yes/No]

Grid:
- Columns: [2 / 3 / 4]
- Gap: _______________
- Cards: [Yes/No]

Featured:
- One large stat
- Supporting stats smaller
- Layout: _______________

### Stat Item Styling

Value:
- Font Size: _______________
- Font Weight: _______________ (e.g., font-bold, font-extrabold)
- Color: _______________ (often primary or accent)
- Line Height: _______________

Prefix/Suffix:
- Font Size: _______________ (slightly smaller)
- Font Weight: _______________
- Color: _______________

Label:
- Font Size: _______________
- Font Weight: _______________
- Color: _______________ (muted)
- Margin Top: _______________

Description (Optional):
- Font Size: _______________
- Color: _______________
- Max Width: _______________

Icon (Optional):
- Position: [Above value / Next to label]
- Size: _______________
- Color: _______________

### Animation

Counter Animation: [Yes/No]
If Yes:
- Type: [Count up from 0 / Fade in]
- Duration: _______________
- Trigger: [On scroll into view / On load]
- Easing: _______________

Background:
- Style: [Solid / Gradient / Accent]
- Padding: _______________
- Border Radius: _______________

---

## COMPONENT 4.3.10: INTEGRATION SHOWCASE

### Component Props

```typescript
interface IntegrationShowcaseProps {
  headline: string;
  description?: string;
  integrations: Integration[];
  layout?: 'grid' | 'marquee' | 'featured';
  filter?: boolean;
  categories?: string[];
}

interface Integration {
  name: string;
  logo: string;
  category?: string;
  link?: string;
  description?: string;
}
```

### Visual Design

Layout Options:

Grid:
- Columns: [4 / 5 / 6 / 8]
- Gap: _______________
- Logo Style: [Contained / Grayscale / Color]

Marquee (Scrolling):
- Direction: [Left to right / Right to left]
- Speed: _______________
- Pause on Hover: [Yes/No]
- Duplicate: [Yes - for seamless loop]

Featured:
- Featured Count: _______________
- Featured Size: [Larger]
- Grid for Others: [Smaller logos]

### Logo Styling

Logo Container:
- Background: _______________
- Border: _______________
- Border Radius: _______________
- Padding: _______________
- Aspect Ratio: [Square / 4:3 / 3:2]

Logo Image:
- Filter: [Grayscale / None]
- Opacity: _______________ (if grayscale)
- Max Width: _______________
- Max Height: _______________
- Object Fit: [Contain / Cover]

Hover State:
- Filter: [None - show color]
- Opacity: [Full]
- Transform: _______________ (scale, lift)
- Shadow: _______________

### Interactive Features

Clickable: [Yes/No]
If Yes:
- Link to: [Integration page / External site]
- Open in: [Same tab / New tab]

Tooltip: [Yes/No]
If Yes:
- Content: [Name / Name + description]
- Position: [Top / Bottom]

Filter/Categories:
- Show: [Yes/No]
- Categories: _______________
- Filter UI: [Tabs / Buttons / Dropdown]
- Animation: [Fade / Slide when filtering]

---

## SHARED SPECIFICATIONS

### Responsive Behavior

Mobile (<768px):
- Grid columns: [1-2]
- Card padding: [Reduced]
- Font sizes: [Scaled down]
- Icon sizes: [Smaller]
- Spacing: [Tighter]

Tablet (768-1024px):
- Grid columns: [2-3]
- Moderate sizing

Desktop (>1024px):
- Full specified design
- Optimal spacing

### Accessibility

- [ ] Semantic HTML
- [ ] ARIA labels for icons
- [ ] Keyboard navigation
- [ ] Focus indicators
- [ ] Color contrast WCAG AA
- [ ] Screen reader friendly
- [ ] Alt text for images/logos
- [ ] Tooltips accessible

### Performance

- [ ] Lazy load below-fold cards
- [ ] Optimize images/logos
- [ ] Avoid layout shift
- [ ] Efficient animations
- [ ] Virtual scrolling (large lists)

### Analytics

Track:
- Feature card clicks
- Tab switches
- Video plays
- Integration logo clicks
- Comparison interactions

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
Create Feature Cards & Product Showcase Components based on the completed specification.

CONTEXT: I have defined a comprehensive library of components for displaying features, comparisons, product showcases, and integrations in engaging visual formats.

TASK:
1. Create FeatureCard component with multiple variants
2. Build FeatureList component with different styles
3. Implement FeatureComparison card
4. Create ProductShowcase section
5. Build BeforeAfter comparison component
6. Implement InteractiveDemo with tabs
7. Create BentoGrid layout
8. Build IconFeatureBlock component
9. Implement StatsDisplay with counter animation
10. Create IntegrationShowcase with filtering

GUIDELINES:
- Mobile-first responsive grid systems
- Use semantic tokens from design system
- Smooth hover effects and transitions
- Scannable layouts with clear hierarchy
- Icon consistency across components
- Accessibility: keyboard navigation, ARIA labels
- Performance: optimize images, lazy loading
- Analytics tracking on interactions

CONSTRAINTS:
- Grid layouts must not break on mobile
- Images optimized (<200KB)
- Animations respect prefers-reduced-motion
- Color contrast WCAG AA compliant
- Touch targets 44px minimum
- Works on all modern browsers

[Paste your filled feature cards template here]

EXPECTED DELIVERABLES:
1. FeatureCard component with variants
2. FeatureList component
3. FeatureComparison card
4. ProductShowcase section
5. BeforeAfter comparison
6. InteractiveDemo tabs component
7. BentoGrid layout system
8. IconFeatureBlock component
9. StatsDisplay with animations
10. IntegrationShowcase component
```

---

## 📝 USAGE INSTRUCTIONS

1. **Consistency** - use same card style across sections
2. **Scannability** - icons and headlines draw eye
3. **White space** - don't overcrowd cards
4. **Limit text** - keep descriptions concise
5. **Visual balance** - mix text and visuals
6. **Mobile grids** - test on actual devices
7. **Interactive elements** - provide feedback on hover
8. **Performance** - lazy load below-fold cards

---

## 💡 BEST PRACTICES

- Feature cards should be scannable in 3 seconds
- Use icons consistently - same style across all cards
- Keep descriptions under 100 characters for readability
- Interactive demos increase engagement significantly
- Before/After comparisons very effective for pain points
- Bento grids create visual interest but need good content balance
- Stats should count up on scroll for engagement
- Integration logos better grayscale (shows more color options)
- Comparison tables should highlight differences, not just list features
- Product screenshots should show real interface, not empty states
- Hover effects provide feedback but shouldn't be essential
- Grid layouts should balance text/visual cards

---

## ⚠️ CRITICAL REMINDERS

- Feature cards are primary way users scan offerings
- Icons should be meaningful, not decorative
- Comparison cards must be fair and accurate
- Mobile grid layout critical - test thoroughly
- Stats must be accurate and up-to-date
- Integration logos need permission/trademark compliance
- Empty states look bad - use actual product screenshots
- Too many features overwhelming - prioritize most important
- Interactive elements must work on touch devices
- Animations should enhance, not distract
- Color contrast especially important for icons on backgrounds
- Card heights in grid should be consistent or intentionally varied
- Loading states important for dynamic content
- A/B test card layouts - huge impact on comprehension
