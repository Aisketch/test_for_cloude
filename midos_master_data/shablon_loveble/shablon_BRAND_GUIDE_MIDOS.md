BRAND_GUIDE_MIDOS.md

```markdown
# BRAND GUIDE
> Заповніть всі секції детально. Використовуйте конкретні значення замість плейсхолдерів.

---

## 1. BRAND IDENTITY (Ідентичність бренду)

### 1.1 Brand Core
- **Brand Name**: [Назва бренду]
- **Tagline/Slogan**: [Слоган]
- **Mission Statement**: [Місія - навіщо ви існуєте]
- **Vision Statement**: [Бачення - куди прямуєте]
- **Core Values**: [3-5 ключових цінностей]

### 1.2 Brand Personality
- **Archetype**: [Hero/Creator/Sage/etc.]
- **Personality Traits**: [5 прикметників що описують бренд]
- **Brand Promise**: [Що гарантуєте клієнтам]

### 1.3 Target Audience
- **Primary Audience**: [Хто, демографія, психографія]
- **Secondary Audience**: [Додаткові сегменти]
- **Pain Points**: [Які проблеми вирішуєте]

---

## 2. VISUAL IDENTITY (Візуальна система)

### 2.1 Logo System
```
Primary Logo:
- File format: [SVG/PNG]
- Minimum size: [Xpx]
- Clear space: [X% від висоти логотипу]
- Positioning: [left/center/right]

Logo Variations:
- [ ] Full color logo
- [ ] Monochrome logo
- [ ] Inverted logo (for dark backgrounds)
- [ ] Icon/symbol only
- [ ] Text only

Logo Usage:
✓ DO: [Список дозволених використань]
✗ DON'T: [Список заборонених використань]
```

### 2.2 Brand Mark/Icon
- **Symbol Description**: [Опис символу/іконки]
- **Meaning**: [Символізм]
- **Usage Context**: [Коли використовувати]

---

## 3. COLOR SYSTEM (Кольорова палітра)

### 3.1 Primary Colors
```css
/* Main Brand Color */
--primary: [HSL/HEX value]
--primary-foreground: [HSL/HEX value]

/* Usage: CTAs, links, key elements */
/* Percentage: 60% of design */
```

### 3.2 Secondary Colors
```css
/* Accent Color 1 */
--secondary: [HSL/HEX value]
--secondary-foreground: [HSL/HEX value]

/* Accent Color 2 (якщо є) */
--accent: [HSL/HEX value]
--accent-foreground: [HSL/HEX value]

/* Usage: highlights, badges, secondary CTAs */
/* Percentage: 30% of design */
```

### 3.3 Neutral Colors
```css
/* Backgrounds */
--background: [HSL/HEX value]
--foreground: [HSL/HEX value]

/* Cards & Containers */
--card: [HSL/HEX value]
--card-foreground: [HSL/HEX value]

/* Borders & Dividers */
--border: [HSL/HEX value]
--input: [HSL/HEX value]

/* Muted Elements */
--muted: [HSL/HEX value]
--muted-foreground: [HSL/HEX value]

/* Usage: structure, text, subtle elements */
/* Percentage: 10% of design */
```

### 3.4 Semantic Colors
```css
/* Success */
--success: [HSL/HEX value]

/* Error/Destructive */
--destructive: [HSL/HEX value]
--destructive-foreground: [HSL/HEX value]

/* Warning */
--warning: [HSL/HEX value]

/* Info */
--info: [HSL/HEX value]
```

### 3.5 Color Psychology
- **Primary Color Meaning**: [Що викликає у аудиторії]
- **Color Associations**: [З чим асоціюється]
- **Competitor Differentiation**: [Чим відрізняється від конкурентів]

---

## 4. TYPOGRAPHY (Типографіка)

### 4.1 Font Families
```css
/* Primary Font (Headings) */
--font-primary: "[Font Name]", sans-serif;
/* Weights: [100/200/300/400/500/600/700/800/900] */
/* Source: [Google Fonts/Custom/System] */
/* Link: [URL якщо Google Fonts] */

/* Secondary Font (Body) */
--font-secondary: "[Font Name]", sans-serif;
/* Weights: [300/400/500/600] */
/* Source: [Google Fonts/Custom/System] */
/* Link: [URL якщо Google Fonts] */

/* Monospace Font (Code) */
--font-mono: "[Font Name]", monospace;
/* Usage: code blocks, technical content */
```

### 4.2 Type Scale (Desktop)
```css
/* Display (Hero titles) */
--text-display: [Xrem / Xpx] | line-height: [X] | weight: [X] | tracking: [Xem]

/* H1 */
--text-h1: [Xrem / Xpx] | line-height: [X] | weight: [X] | tracking: [Xem]

/* H2 */
--text-h2: [Xrem / Xpx] | line-height: [X] | weight: [X] | tracking: [Xem]

/* H3 */
--text-h3: [Xrem / Xpx] | line-height: [X] | weight: [X] | tracking: [Xem]

/* H4 */
--text-h4: [Xrem / Xpx] | line-height: [X] | weight: [X] | tracking: [Xem]

/* Body Large */
--text-body-lg: [Xrem / Xpx] | line-height: [X] | weight: [X]

/* Body Regular */
--text-body: [Xrem / Xpx] | line-height: [X] | weight: [X]

/* Body Small */
--text-body-sm: [Xrem / Xpx] | line-height: [X] | weight: [X]

/* Caption */
--text-caption: [Xrem / Xpx] | line-height: [X] | weight: [X]
```

### 4.3 Type Scale (Mobile)
```css
/* Adjustments for mobile (<768px) */
--text-display-mobile: [Xrem / Xpx]
--text-h1-mobile: [Xrem / Xpx]
--text-h2-mobile: [Xrem / Xpx]
/* ... інші розміри ... */
```

### 4.4 Typography Rules
- **Letter Spacing (Tracking)**: [tight: -0.02em / normal: 0 / wide: 0.05em]
- **Line Height**: [tight: 1.2 / normal: 1.5 / relaxed: 1.8]
- **Paragraph Spacing**: [Xrem between paragraphs]
- **Max Line Length**: [60-80 characters for readability]
- **Hierarchy**: [How to establish visual hierarchy]

---

## 5. SPACING & LAYOUT (Відступи та сітка)

### 5.1 Spacing Scale
```css
/* Base unit: [4px / 8px] */
--space-xs: [Xpx]    /* [4px] */
--space-sm: [Xpx]    /* [8px] */
--space-md: [Xpx]    /* [16px] */
--space-lg: [Xpx]    /* [24px] */
--space-xl: [Xpx]    /* [32px] */
--space-2xl: [Xpx]   /* [48px] */
--space-3xl: [Xpx]   /* [64px] */
--space-4xl: [Xpx]   /* [96px] */
```

### 5.2 Grid System
- **Columns**: [12-column / 16-column]
- **Gutter Width**: [Xpx]
- **Max Container Width**: [1280px / 1440px / full]
- **Breakpoints**:
  ```css
  --breakpoint-sm: 640px   /* Mobile */
  --breakpoint-md: 768px   /* Tablet */
  --breakpoint-lg: 1024px  /* Desktop */
  --breakpoint-xl: 1280px  /* Large Desktop */
  --breakpoint-2xl: 1536px /* Extra Large */
  ```

### 5.3 Layout Principles
- **Mobile First**: [true/false]
- **Content Width**: [Optimal reading width: 60-80ch]
- **Section Padding**: [Vertical: Xpx, Horizontal: Xpx]
- **Whitespace Philosophy**: [generous/minimal/balanced]

---

## 6. COMPONENTS & UI PATTERNS (Компоненти)

### 6.1 Buttons
```css
/* Primary Button */
Style: [filled/outlined/ghost]
Padding: [Y: Xpx, X: Xpx]
Border Radius: [Xpx]
Font: [size, weight]
States:
- Default: [bg, text, border]
- Hover: [transformations]
- Active: [style]
- Disabled: [opacity, cursor]

/* Secondary Button */
[Аналогічно]

/* Tertiary/Ghost Button */
[Аналогічно]
```

### 6.2 Cards
```css
Background: [color]
Border: [width, color, radius]
Shadow: [elevation level]
Padding: [Xpx]
Hover State: [lift/scale/glow/none]
```

### 6.3 Forms
```css
/* Input Fields */
Height: [Xpx]
Border: [width, color, radius]
Focus State: [ring, border color]
Error State: [border, message color]
Label Style: [position, size, weight]

/* Checkboxes/Radio */
Size: [Xpx]
Style: [rounded/square]
Checked State: [color, icon]
```

### 6.4 Navigation
```css
/* Header */
Height: [Xpx]
Position: [fixed/sticky/static]
Background: [color, blur effect]
Shadow: [on scroll]

/* Links */
Default: [color, decoration]
Hover: [underline/color change/scale]
Active: [style]
```

### 6.5 Iconography
- **Icon Library**: [Lucide/Heroicons/Custom]
- **Icon Size Scale**: [16px, 20px, 24px, 32px, 48px]
- **Icon Style**: [outline/solid/duotone]
- **Icon Usage**: [When to use, where to place]

---

## 7. IMAGERY & MEDIA (Зображення)

### 7.1 Photography Style
- **Mood**: [light/dark/vibrant/muted]
- **Subject Matter**: [people/products/abstract/nature]
- **Composition**: [rule of thirds/centered/asymmetric]
- **Color Treatment**: [saturated/desaturated/monochrome]
- **Usage Context**: [hero sections/blog/team photos]

### 7.2 Illustrations
- **Style**: [flat/3D/isometric/hand-drawn/minimalist]
- **Color Palette**: [brand colors/custom palette]
- **Line Weight**: [thin/medium/bold]
- **Usage**: [empty states/onboarding/decorative]

### 7.3 Image Specifications
```
Hero Images:
- Dimensions: [Wpx × Hpx]
- Aspect Ratio: [16:9 / 21:9 / 4:3]
- Format: [WebP, fallback PNG/JPG]
- Max File Size: [XMB]

Thumbnails:
- Dimensions: [Wpx × Hpx]
- Aspect Ratio: [1:1 / 4:3 / 16:9]

Profile Photos:
- Dimensions: [Wpx × Hpx]
- Shape: [circle/rounded square]
```

### 7.4 Video Guidelines
- **Aspect Ratio**: [16:9 / 9:16 for mobile]
- **Max Duration**: [Xs for hero videos]
- **Autoplay**: [yes/no, muted/unmuted]
- **Controls**: [visible/hidden]

---

## 8. MOTION & ANIMATION (Анімація)

### 8.1 Animation Principles
- **Philosophy**: [subtle/energetic/minimal/playful]
- **Purpose**: [delight/feedback/guide attention/explain]
- **Performance**: [60fps, GPU-accelerated]

### 8.2 Timing Functions
```css
/* Easing */
--ease-in: cubic-bezier(0.4, 0, 1, 1)
--ease-out: cubic-bezier(0, 0, 0.2, 1)
--ease-in-out: cubic-bezier(0.4, 0, 0.2, 1)
--ease-custom: cubic-bezier([X, X, X, X])

/* Duration */
--duration-fast: [150ms]    /* micro-interactions */
--duration-normal: [300ms]  /* standard transitions */
--duration-slow: [500ms]    /* page transitions */
```

### 8.3 Animation Types
```
Page Load:
- Hero fade-in: [duration, delay, easing]
- Stagger children: [delay between elements]

Hover Interactions:
- Buttons: [scale/lift/glow - duration]
- Links: [underline slide/color - duration]
- Cards: [shadow/scale - duration]

Scroll Animations:
- Parallax: [speed multiplier]
- Fade in on scroll: [threshold, duration]
- Number counters: [duration, easing]

Transitions:
- Page transitions: [slide/fade/scale - duration]
- Modal open/close: [animation type, duration]
```

### 8.4 GSAP Integration
- **Library Version**: [GSAP 3.x]
- **Plugins Used**: [ScrollTrigger/SplitText/MorphSVG]
- **Signature Animation**: [Опис унікальної анімації бренду]

---

## 9. TONE & VOICE (Тон і голос)

### 9.1 Brand Voice Attributes
- **Attribute 1**: [e.g., Professional] - [Опис як це проявляється]
- **Attribute 2**: [e.g., Friendly] - [Опис]
- **Attribute 3**: [e.g., Innovative] - [Опис]
- **Attribute 4**: [e.g., Clear] - [Опис]

### 9.2 Writing Style
```
Sentence Structure:
- Length: [short/medium/varied]
- Complexity: [simple/technical/mixed]
- Active vs Passive: [prefer active voice]

Word Choice:
- Technical Terms: [when to use jargon]
- Contractions: [yes/no - "we're" vs "we are"]
- Personal Pronouns: [we/you/I - when to use]

Formatting:
- Lists: [bullets vs numbers]
- Emphasis: [bold/italic/color]
- Call-to-Actions: [command/question/statement]
```

### 9.3 Tone by Context

#### Marketing/Landing Pages
- **Tone**: [Enthusiastic, persuasive]
- **Example**: "[Приклад тексту]"

#### Product/Documentation
- **Tone**: [Clear, instructional]
- **Example**: "[Приклад тексту]"

#### Error Messages
- **Tone**: [Helpful, apologetic]
- **Example**: "[Приклад тексту]"

#### Success Messages
- **Tone**: [Celebratory, affirming]
- **Example**: "[Приклад тексту]"

### 9.4 Localization (EN/UA)

#### English Version
- **Formality**: [casual/neutral/formal]
- **Idioms**: [use/avoid]
- **Cultural References**: [local/global]

#### Ukrainian Version
- **Ви/Ти**: [which form to use]
- **Terminology**: [literal translation/adaptation]
- **Cultural Adaptation**: [how to adjust messaging]

---

## 10. ACCESSIBILITY (Доступність)

### 10.1 Color Contrast
- **WCAG Level**: [AA / AAA]
- **Text Contrast Ratio**: [minimum 4.5:1 for normal text]
- **Large Text**: [minimum 3:1]
- **Interactive Elements**: [minimum 3:1]

### 10.2 Typography Accessibility
- **Minimum Font Size**: [16px for body text]
- **Line Height**: [1.5 for body, 1.2 for headings]
- **Paragraph Width**: [max 80ch for readability]

### 10.3 Interaction
- **Keyboard Navigation**: [all interactive elements accessible]
- **Focus Indicators**: [visible, high contrast]
- **Touch Targets**: [minimum 44×44px]
- **Motion**: [respect prefers-reduced-motion]

### 10.4 Content
- **Alt Text**: [descriptive for all images]
- **Heading Hierarchy**: [proper H1-H6 structure]
- **Link Text**: [descriptive, not "click here"]
- **Form Labels**: [visible, associated with inputs]

---

## 11. BRAND APPLICATIONS (Застосування)

### 11.1 Digital Touchpoints
- **Website**: [Primary brand expression]
- **Web App**: [Simplified, functional focus]
- **Mobile App**: [Adapted for touch, smaller screens]
- **Email**: [HTML templates, plain text fallback]
- **Social Media**: [Profile images, cover photos, post templates]

### 11.2 Marketing Materials
- **One-Pagers**: [Layout, key messages]
- **Presentations**: [Slide master, templates]
- **Infographics**: [Style, data visualization approach]
- **Video Thumbnails**: [Design template]

### 11.3 Print (if applicable)
- **Business Cards**: [Dimensions, layout]
- **Letterhead**: [Layout, margins]
- **Brochures**: [Fold type, layout grid]

---

## 12. DO'S & DON'TS (Правила)

### 12.1 Logo
✓ DO:
- [Список дозволених використань]
- Use approved color variations only
- Maintain clear space around logo
- Use vector files when possible

✗ DON'T:
- [Список заборонених використань]
- Distort or rotate logo
- Use unapproved colors
- Place logo on busy backgrounds without backdrop

### 12.2 Colors
✓ DO:
- Use color palette consistently
- Ensure sufficient contrast
- Test colors in different contexts

✗ DON'T:
- Introduce new colors without approval
- Use colors that fail accessibility tests
- Overuse accent colors

### 12.3 Typography
✓ DO:
- Follow type scale
- Use approved font weights
- Maintain hierarchy

✗ DON'T:
- Stretch or condense fonts
- Use more than 3 font sizes on one screen
- Use decorative fonts for body text

### 12.4 Imagery
✓ DO:
- Use high-quality, on-brand images
- Optimize for web performance
- Provide alt text

✗ DON'T:
- Use generic stock photos
- Over-filter or heavily edit brand photos
- Use images with inconsistent style

---

## 13. BRAND EVOLUTION (Еволюція)

### 13.1 Version History
```
Version 1.0 - [Date]
- Initial brand guidelines established
- [Key decisions made]

Version 1.1 - [Date]
- [What changed and why]
```

### 13.2 Review Schedule
- **Frequency**: [Quarterly/Annually]
- **Stakeholders**: [Who reviews]
- **Update Process**: [How changes are approved]

### 13.3 Exception Process
```
When brand guidelines need to be bent:
1. Document the reason
2. Get approval from [role]
3. Create temporary exception guideline
4. Review in next brand audit
```

---

## 14. RESOURCES & ASSETS

### 14.1 Asset Library
- **Location**: [URL/Folder path]
- **Structure**: [How assets are organized]
- **Naming Convention**: [File naming pattern]

### 14.2 Font Files
- **Primary Font**: [Download link/CDN]
- **Secondary Font**: [Download link/CDN]
- **License**: [OFL/Commercial/etc.]

### 14.3 Design Tools
- **Figma**: [Link to design system]
- **Component Library**: [Storybook/other URL]
- **Icon Set**: [Link to icon library]

### 14.4 Reference Links
- **Brand Inspiration**: [Moodboard/Pinterest]
- **Competitor Analysis**: [Document link]
- **Color Palette Tool**: [Coolors/Adobe Color link]

---

## 15. COMPETITIVE DIFFERENTIATION (Відмінність від конкурентів)

### 15.1 Competitor Comparison
```
Competitor A (e.g., Delphi.ai):
- Visual Style: [Опис]
- Our Difference: [Як ви відрізняєтесь]

Competitor B:
- Visual Style: [Опис]
- Our Difference: [Як ви відрізняєтесь]
```

### 15.2 Unique Brand Elements
- **Signature Element 1**: [e.g., Neural network hero animation]
- **Signature Element 2**: [e.g., Specific color combination]
- **Signature Element 3**: [e.g., Custom illustration style]

### 15.3 Brand Positioning
- **Market Position**: [Premium/Accessible/Innovative/etc.]
- **Key Differentiator**: [What makes you unique]
- **Brand Promise**: [What customers can always expect]

---

## 16. IMPLEMENTATION CHECKLIST

### Phase 1: Foundation ✓
- [ ] Brand colors added to Tailwind config
- [ ] Fonts loaded (Google Fonts/local)
- [ ] Typography scale implemented
- [ ] Spacing scale configured
- [ ] Base components styled

### Phase 2: Components ✓
- [ ] Button variants created
- [ ] Card styles applied
- [ ] Form elements styled
- [ ] Navigation components
- [ ] All UI components match brand

### Phase 3: Content ✓
- [ ] All text follows tone & voice
- [ ] Images follow style guidelines
- [ ] Icons consistent throughout
- [ ] Animations implemented
- [ ] Accessibility checked

### Phase 4: Polish ✓
- [ ] Mobile responsiveness tested
- [ ] Cross-browser testing done
- [ ] Performance optimized
- [ ] Brand consistency audit
- [ ] Final approval received

---

**Last Updated**: [Date]
**Version**: [X.X]
**Maintained By**: [Name/Team]
```
