# TEMPLATE 7.4: ACCESSIBILITY (WCAG 2.1 AA) IMPLEMENTATION

## 📋 PURPOSE
This template provides a comprehensive accessibility checklist to ensure your website meets WCAG 2.1 Level AA standards, making it usable for people with disabilities including visual, auditory, motor, and cognitive impairments.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Implement Accessibility (WCAG 2.1 AA) based on the following specification:

## ACCESSIBILITY STANDARDS

Target Compliance Level: WCAG 2.1 Level AA
Testing Standard: [WCAG 2.1 / Section 508 / ADA / EN 301 549]
Audit Schedule: _______________

WCAG 2.1 Principles:
1. Perceivable - Information must be presentable to users
2. Operable - Interface must be operable by all users
3. Understandable - Information and operation must be understandable
4. Robust - Content must be robust enough for assistive technologies

---

## PERCEIVABLE (Information & UI Components)

### 1.1 Text Alternatives

Alt Text for Images:

Informative Images:
- Include alt text describing the image
- Format: Describe what the image shows
- Example: `alt="Team collaborating on project in modern office"`

Decorative Images:
- Empty alt text: `alt=""`
- Purpose: Screen readers skip decorative images

Functional Images (links, buttons):
- Describe function, not appearance
- Example: `alt="Search"` not `alt="Magnifying glass icon"`

Complex Images (charts, diagrams):
- Provide detailed description in nearby text OR
- Use aria-describedby to link to detailed description
- Example: `aria-describedby="chart-description"`

Logo Images:
- Include company name in alt text
- Example: `alt="Acme Corporation logo"`

Icons with Text:
- If icon + text label: `aria-hidden="true"` on icon
- If icon only: Provide descriptive label

SVG Icons:
```jsx
<svg aria-label="Settings" role="img">
  <title>Settings</title>
  {/* SVG content */}
</svg>
```

Alt Text Checklist:
- [ ] All images have alt attribute (even if empty)
- [ ] Alt text is descriptive and concise
- [ ] Decorative images have empty alt
- [ ] Icons have labels or are hidden if redundant
- [ ] Complex images have detailed descriptions

### 1.2 Time-Based Media

Video Content:
- Captions: [Yes/No]
- Audio descriptions: [Yes/No]
- Transcript: [Yes/No]

Audio Content:
- Transcript: [Yes/No]

Implementation:
- Video player: [HTML5 with track element / Third-party accessible player]
- Caption format: [WebVTT / SRT]
- Languages: _______________

### 1.3 Adaptable Content

#### Semantic HTML

Proper Semantic Elements:

Document Structure:
```jsx
<header>Navigation, logo</header>
<nav>Navigation menu</nav>
<main>Main content</main>
<article>Article content</article>
<section>Section of content</section>
<aside>Sidebar content</aside>
<footer>Footer content</footer>
```

Headings Hierarchy:
- One H1 per page: [Enforced]
- Proper nesting: H1 → H2 → H3 (no skipping)
- Descriptive headings: [Yes]

Lists:
- Ordered lists: `<ol>` for sequences
- Unordered lists: `<ul>` for non-sequential items
- Definition lists: `<dl>` for term-definition pairs

Emphasis:
- Strong importance: `<strong>` (not just `<b>`)
- Emphasis: `<em>` (not just `<i>`)
- Quotes: `<blockquote>` with `<cite>`

Forms:
- Labels: `<label>` for each form input
- Fieldsets: `<fieldset>` for related inputs
- Legends: `<legend>` for fieldset description

Tables:
- Header cells: `<th>` with scope attribute
- Caption: `<caption>` for table title
- Complex tables: Use headers attribute

#### Landmark Regions

ARIA Landmarks:
```jsx
<header role="banner">
<nav role="navigation" aria-label="Main navigation">
<main role="main">
<aside role="complementary">
<footer role="contentinfo">
<form role="search">
```

Multiple Landmarks:
Use aria-label to differentiate:
```jsx
<nav aria-label="Main navigation">
<nav aria-label="Footer navigation">
```

#### Reading Order

Logical Reading Order:
- Visual order matches DOM order: [Yes]
- CSS positioning doesn't disrupt order: [Yes]
- Tab order is logical: [Yes]

Test:
- Disable CSS and check order: [Logical]
- Use screen reader: [Logical]

### 1.4 Distinguishable

#### Color Contrast

Contrast Ratios (WCAG AA):

Normal Text (< 18px or < 14px bold):
- Minimum contrast: 4.5:1
- Examples to test:
  - Body text on background: _______________
  - Link text on background: _______________
  - Button text on button color: _______________

Large Text (≥ 18px or ≥ 14px bold):
- Minimum contrast: 3:1
- Examples to test:
  - Headings on background: _______________
  - Large CTA text: _______________

UI Components:
- Interactive elements: 3:1 minimum
- Examples:
  - Button borders: _______________
  - Form input borders: _______________
  - Icon colors: _______________

Testing Tool: WebAIM Contrast Checker
URL: https://webaim.org/resources/contrastchecker/

Contrast Audit:

Primary Text: 
- Color: _______________ on _______________
- Ratio: _______________
- Pass/Fail: _______________

Secondary Text:
- Color: _______________ on _______________
- Ratio: _______________
- Pass/Fail: _______________

Link Text:
- Color: _______________ on _______________
- Ratio: _______________
- Pass/Fail: _______________

Button (Primary):
- Text color: _______________ on _______________
- Ratio: _______________
- Pass/Fail: _______________

Form Inputs:
- Border color: _______________ on _______________
- Ratio: _______________
- Pass/Fail: _______________

[Continue for all color combinations...]

#### Color Independence

Don't Rely on Color Alone:

Links:
- Underline links: [Yes] OR
- Provide additional visual cue (icon, bold)
- Example: Underline on hover if not always underlined

Form Validation:
- Don't use color only for error/success
- Include icons: ✓ (success) ✗ (error)
- Include text labels: "Error: Email required"

Charts/Graphs:
- Use patterns in addition to colors
- Label directly on chart
- Provide data table alternative

Status Indicators:
- Don't use color only (red/green status)
- Include text labels or icons
- Example: "Active" (green) vs "Inactive" (gray) - use text too

#### Text Sizing & Spacing

Text Resize:
- Allow zoom up to 200%: [Yes]
- Layout doesn't break when zoomed: [Yes]
- No loss of content/functionality: [Yes]

Minimum Text Size:
- Body text: 16px minimum
- Small text: 14px minimum (use sparingly)
- Never below: 12px

Line Height:
- Paragraphs: 1.5 minimum (leading-relaxed)
- Headings: 1.25 minimum (leading-tight)

Letter Spacing:
- Normal spacing: Default
- Increased for readability: [Optional]

Word Spacing:
- Normal spacing: Default

Paragraph Spacing:
- Between paragraphs: 2x font size minimum

Text Block Width:
- Maximum width: 80 characters
- Tailwind: max-w-prose (65ch)

#### Non-Text Contrast

Interactive Elements:
- Minimum contrast: 3:1 against background
- Examples:
  - Button borders
  - Form input borders
  - Focus indicators
  - Icons

States:
- Normal state: 3:1
- Hover state: 3:1
- Focus state: 3:1
- Active state: 3:1

---

## OPERABLE (User Interface & Navigation)

### 2.1 Keyboard Accessible

#### Keyboard Navigation

All Functionality Available via Keyboard:
- Links: Accessible via Tab
- Buttons: Accessible via Tab
- Forms: Navigate with Tab, Arrow keys
- Dropdowns: Arrow keys to navigate
- Modals: Tab traps inside modal
- Carousels: Keyboard controls provided

Keyboard Shortcuts:

Skip Links:
```jsx
<a href="#main-content" className="sr-only focus:not-sr-only">
  Skip to main content
</a>
```

Essential Shortcuts:
- Tab: Next focusable element
- Shift+Tab: Previous element
- Enter/Space: Activate button
- Escape: Close modal/dropdown
- Arrow keys: Navigate menus/tabs/carousels

Custom Shortcuts:
- Document if implemented: _______________
- Avoid conflicts with browser/AT: [Yes]
- Provide shortcut reference: [Yes/No]

Focus Management:

Focus Order:
- Logical tab order: [Yes]
- Matches visual order: [Yes]
- No focus traps (except modals): [Yes]

Focus Never Lost:
- Always visible focus indicator: [Yes]
- Focus returns after modal close: [Yes]
- Dynamic content receives focus appropriately: [Yes]

Tab Index:
- Default (0): For interactive elements
- -1: For programmatic focus only
- Avoid positive values: [Yes]

```jsx
// Good
<div tabIndex="0" role="button">

// Good - programmatic focus
<div tabIndex="-1" ref={focusRef}>

// Avoid
<div tabIndex="1">
```

### 2.2 Enough Time

#### Timing

Auto-Refresh/Update:
- Used: [Yes/No]
- User can pause: [Yes/No]
- User can adjust timing: [Yes/No]

Session Timeout:
- Timeout duration: _______________ minutes
- Warning before timeout: [Yes/No]
- Time to warning: _______________ seconds
- Extend session option: [Yes/No]

Auto-Advancing Content:
- Carousels: User can pause/stop
- Auto-play videos: Pause button provided
- Animations: Can be paused

Moving/Scrolling Content:
- User control: [Yes]
- Auto-scrolling: [Disabled / User-controlled]

### 2.3 Seizures & Physical Reactions

#### Flashing Content

Flashing Threshold:
- No more than 3 flashes per second: [Enforced]
- Large flashing areas avoided: [Yes]

Content Check:
- Animations checked for flashing: [Yes]
- Videos checked: [Yes]
- Auto-playing GIFs: [Limited/None]

### 2.4 Navigable

#### Navigation Mechanisms

Multiple Ways to Find Content:
- [ ] Main navigation menu
- [ ] Search function
- [ ] Site map
- [ ] Breadcrumbs
- [ ] Footer links
- [ ] Related content links

Minimum Required: 2 ways

#### Page Titles

Page Title Format:
```
[Page Name] | [Section] | [Site Name]
```

Examples:
- Homepage: `_______________`
- Features: `_______________`
- Pricing: `_______________`
- Blog Post: `_______________`

Requirements:
- Unique per page: [Yes]
- Descriptive: [Yes]
- Concise: [Yes]
- Most important info first: [Yes]

#### Focus Visible

Focus Indicator:

Default Focus Style:
```css
/* Ensure visible focus indicator */
:focus {
  outline: 2px solid blue;
  outline-offset: 2px;
}
```

Custom Focus Style:
```jsx
className="focus:ring-2 focus:ring-blue-500 focus:outline-none"
```

Requirements:
- Visible on all interactive elements: [Yes]
- Sufficient contrast (3:1): [Yes]
- Not removed without replacement: [Yes]
- Visible on keyboard focus: [Yes]

Focus Indicator Examples:

Buttons:
```jsx
className="focus:ring-2 focus:ring-blue-500 focus:ring-offset-2"
```

Links:
```jsx
className="focus:underline focus:ring-2 focus:ring-blue-500"
```

Form Inputs:
```jsx
className="focus:border-blue-500 focus:ring-2 focus:ring-blue-500"
```

Custom Interactive Elements:
```jsx
<div 
  tabIndex="0"
  role="button"
  className="focus:ring-2 focus:ring-blue-500"
>
```

#### Link Purpose

Link Text:
- Descriptive of destination: [Yes]
- Avoid "click here": [Yes]
- Avoid "read more" alone: [Yes]

Good Examples:
- "Read our privacy policy"
- "View pricing plans"
- "Download user guide (PDF, 2MB)"

Bad Examples:
- "Click here"
- "Read more"
- "Learn more"

Link with Context:
If link text is generic, provide context:
```jsx
<a href="/pricing" aria-label="View pricing for Pro plan">
  Learn more
</a>
```

#### Breadcrumbs

Breadcrumb Navigation:
```jsx
<nav aria-label="Breadcrumb">
  <ol className="flex gap-2">
    <li><a href="/">Home</a></li>
    <li aria-hidden="true">›</li>
    <li><a href="/products">Products</a></li>
    <li aria-hidden="true">›</li>
    <li aria-current="page">Current Page</li>
  </ol>
</nav>
```

Requirements:
- aria-label="Breadcrumb"
- Use `<ol>` list
- aria-current="page" on current page
- Separators hidden from screen readers

#### Headings & Labels

Heading Structure:
- Descriptive headings: [Yes]
- Logical hierarchy: [Yes]
- No skipped levels: [Yes]

Label Association:
- Every input has label: [Yes]
- Explicit association: [Yes]

```jsx
// Explicit label
<label htmlFor="email">Email:</label>
<input id="email" type="email" />

// Implicit label
<label>
  Email:
  <input type="email" />
</label>
```

### 2.5 Input Modalities

#### Pointer Gestures

Touch Gestures:
- Single-pointer gestures: [Yes]
- Path-based gestures: [Alternative provided]
- Multi-point gestures: [Alternative provided]

Examples:
- Drag-and-drop: Keyboard alternative provided
- Pinch-to-zoom: Zoom controls provided
- Swipe: Arrow buttons provided

#### Pointer Cancellation

Click/Tap Activation:
- Down-event: Avoid using for activation
- Up-event: Use for activation (standard)
- Cancel: Allow users to cancel (slide off button)

#### Label in Name

Visible Label Matches Accessible Name:
- Button text = aria-label (if aria-label used)
- Visible label included in accessible name
- Don't contradict visible label

Example:
```jsx
// Good
<button>Submit Form</button>

// Good
<button aria-label="Submit registration form">Submit Form</button>

// Bad
<button aria-label="Send">Submit Form</button>
```

#### Motion Actuation

Device Motion:
- Shake to undo: [Alternative provided]
- Tilt to scroll: [Alternative provided]
- Motion-based features: [Can be disabled]

---

## UNDERSTANDABLE (Information & User Interface)

### 3.1 Readable

#### Language of Page

HTML Lang Attribute:
```html
<html lang="en">
```

Primary Language: _______________
Additional Languages: _______________

Language Changes:
```jsx
<p>The French phrase <span lang="fr">Bonjour</span> means hello.</p>
```

Multi-Language Support:
- Language switcher: [Yes/No]
- hreflang tags: [Yes/No]
- Each language page has correct lang attribute: [Yes]

### 3.2 Predictable

#### Consistent Navigation

Navigation Location:
- Same position across pages: [Yes]
- Same order across pages: [Yes]
- Consistent labeling: [Yes]

Repeated Components:
- Header: Consistent across pages
- Footer: Consistent across pages
- Sidebar: Consistent position

#### Consistent Identification

Components with Same Function:
- Same labels: [Yes]
- Same icons: [Yes]
- Same styling: [Yes]

Examples:
- Search icon always means search
- Shopping cart icon always goes to cart
- "Contact Us" link always goes to contact page

#### Focus Changes

Change of Context:
- On focus: [Avoid]
- Only on user action: [Yes]

Don't Change Context On:
- Focus on form input: No auto-submit
- Focus on select: No navigation
- Focus on checkbox: No form submission

Acceptable Changes:
- User clicks button: Context can change
- User presses Enter: Context can change
- User explicitly requests: Context can change

#### Input Changes

Change of Context:
- On input: [Avoid unless user informed]
- Provide submit button: [Yes]

Examples:
- Don't auto-submit form when last field filled
- Don't navigate when selecting from dropdown
- Do provide explicit "Submit" button

### 3.3 Input Assistance

#### Error Identification

Error Messages:

Format:
- Text description: [Yes]
- Not color only: [Yes]
- Icon + text: [Yes]
- Location: Near input or top of form

Example:
```jsx
{error && (
  <div role="alert" className="text-red-600 flex items-center gap-2">
    <span aria-hidden="true">✗</span>
    <span>{error.message}</span>
  </div>
)}
```

Required Fields:
- Marked before submission: [Yes]
- Indication method: [Asterisk * + "(required)" label]
- Explained at form start: [Yes]

Form Validation:
- Client-side: [Yes]
- Error messages clear: [Yes]
- Suggestion for fix: [Yes]

#### Labels or Instructions

Form Labels:
- Every input has label: [Yes]
- Label visible: [Yes]
- Label descriptive: [Yes]

Instructions:
- Format requirements stated: [Yes]
- Example provided: [Yes]

Examples:
```jsx
<label htmlFor="phone">
  Phone Number
  <span className="text-gray-600 text-sm">(Format: +1-555-555-5555)</span>
</label>
<input 
  id="phone" 
  type="tel"
  placeholder="+1-555-555-5555"
  aria-describedby="phone-hint"
/>
<div id="phone-hint" className="text-sm text-gray-600">
  Enter your phone number with country code
</div>
```

Required Fields:
```jsx
<label htmlFor="email">
  Email <span className="text-red-600">*</span>
</label>
<input 
  id="email" 
  type="email" 
  required 
  aria-required="true"
/>
```

#### Error Suggestion

Error Messages Provide Suggestions:

Format Error:
```jsx
"Email format is invalid. Please use format: name@example.com"
```

Required Field:
```jsx
"Email is required. Please enter your email address."
```

Value Out of Range:
```jsx
"Age must be between 18 and 100. You entered: 150"
```

#### Error Prevention (Legal, Financial, Data)

For Important Transactions:

Confirmation Step:
- Review before submit: [Yes]
- Explicit confirmation: [Yes]

Reversible:
- Can undo: [Yes/No]
- Time limit to undo: _______________

Validation:
- Check for errors: [Yes]
- Allow correction: [Yes]

Example Flow:
1. Fill form
2. Review page ("Are these details correct?")
3. Edit link provided
4. Confirm submission

---

## ROBUST (Content Compatible with Assistive Technologies)

### 4.1 Compatible

#### Valid HTML

HTML Validation:
- Tool: W3C HTML Validator
- Valid markup: [Yes]
- No duplicate IDs: [Yes]
- Properly nested elements: [Yes]
- Complete start/end tags: [Yes]

Common Issues to Avoid:
- [ ] Duplicate IDs
- [ ] Missing closing tags
- [ ] Incorrectly nested elements
- [ ] Invalid attributes

#### Name, Role, Value

ARIA Attributes:

Roles:
```jsx
// Button
<div role="button" tabIndex="0">Click me</div>

// Link
<span role="link" tabIndex="0">Go to page</span>

// Checkbox
<div role="checkbox" aria-checked="false">Option</div>

// Tab panel
<div role="tabpanel">Content</div>
```

States & Properties:
```jsx
// Expanded/collapsed
<button aria-expanded="true">Menu</button>

// Selected
<li role="option" aria-selected="true">Option 1</li>

// Disabled
<button disabled aria-disabled="true">Submit</button>

// Hidden
<div aria-hidden="true">Decorative content</div>

// Labeled by
<div role="dialog" aria-labelledby="dialog-title">
  <h2 id="dialog-title">Confirm Action</h2>
</div>

// Described by
<input aria-describedby="password-hint" />
<div id="password-hint">Must be at least 8 characters</div>
```

Values:
- Interactive elements have appropriate values
- States communicated to assistive tech
- Names are clear and descriptive

---

## ARIA IMPLEMENTATION

### ARIA Landmarks

Landmark Roles:
```jsx
<header role="banner">
<nav role="navigation" aria-label="Main">
<main role="main">
<aside role="complementary">
<footer role="contentinfo">
<form role="search">
```

### ARIA Labels

aria-label:
```jsx
<button aria-label="Close dialog">✕</button>
<nav aria-label="Main navigation">
```

aria-labelledby:
```jsx
<section aria-labelledby="section-title">
  <h2 id="section-title">Features</h2>
</section>
```

aria-describedby:
```jsx
<input 
  type="password" 
  aria-describedby="password-rules"
/>
<div id="password-rules">
  Password must be at least 8 characters
</div>
```

### ARIA Live Regions

Live Announcements:
```jsx
// Polite - wait for pause
<div role="status" aria-live="polite">
  Item added to cart
</div>

// Assertive - interrupt
<div role="alert" aria-live="assertive">
  Error: Form submission failed
</div>
```

### ARIA States

Common States:
```jsx
// Expanded
aria-expanded="true"

// Selected
aria-selected="true"

// Checked
aria-checked="true"

// Disabled
aria-disabled="true"

// Hidden
aria-hidden="true"

// Invalid
aria-invalid="true"

// Required
aria-required="true"

// Current
aria-current="page"
```

---

## FORMS ACCESSIBILITY

### Form Structure

Form Labels:
```jsx
<form>
  <div className="form-group">
    <label htmlFor="name">Full Name *</label>
    <input 
      id="name" 
      type="text" 
      required 
      aria-required="true"
    />
  </div>
</form>
```

Fieldsets:
```jsx
<fieldset>
  <legend>Contact Information</legend>
  {/* Related form fields */}
</fieldset>
```

### Form Validation

Accessible Validation:
```jsx
<div className="form-group">
  <label htmlFor="email">Email *</label>
  <input 
    id="email"
    type="email"
    required
    aria-required="true"
    aria-invalid={error ? "true" : "false"}
    aria-describedby={error ? "email-error" : undefined}
  />
  {error && (
    <div id="email-error" role="alert" className="error">
      {error.message}
    </div>
  )}
</div>
```

### Form Error Handling

Error Summary:
```jsx
{errors.length > 0 && (
  <div role="alert" className="error-summary">
    <h2>Please fix the following errors:</h2>
    <ul>
      {errors.map((error, i) => (
        <li key={i}>
          <a href={`#${error.fieldId}`}>{error.message}</a>
        </li>
      ))}
    </ul>
  </div>
)}
```

---

## MODALS/DIALOGS ACCESSIBILITY

### Modal Structure

Accessible Modal:
```jsx
<div
  role="dialog"
  aria-modal="true"
  aria-labelledby="modal-title"
  aria-describedby="modal-description"
>
  <h2 id="modal-title">Confirm Action</h2>
  <div id="modal-description">
    Are you sure you want to proceed?
  </div>
  <button>Confirm</button>
  <button>Cancel</button>
</div>
```

### Focus Management

Modal Focus Trap:
- Focus moves to modal on open
- Tab cycles through modal elements only
- Shift+Tab cycles backwards
- Escape closes modal
- Focus returns to trigger element on close

### Background Content

Inert Background:
- aria-hidden="true" on background
- No tabbing to background elements
- Background not scrollable

---

## TESTING & VALIDATION

### Automated Testing Tools

- [ ] WAVE (Web Accessibility Evaluation Tool)
- [ ] axe DevTools
- [ ] Lighthouse (Accessibility audit)
- [ ] Pa11y
- [ ] HTML Validator (W3C)
- [ ] Color Contrast Analyzer

### Manual Testing

Keyboard Testing:
- [ ] Navigate entire site with keyboard only
- [ ] All functionality accessible
- [ ] Focus visible at all times
- [ ] Logical tab order
- [ ] No keyboard traps

Screen Reader Testing:
- [ ] NVDA (Windows, free)
- [ ] JAWS (Windows, paid)
- [ ] VoiceOver (Mac/iOS, built-in)
- [ ] TalkBack (Android, built-in)

Zoom Testing:
- [ ] Zoom to 200%
- [ ] No horizontal scrolling
- [ ] Content still readable
- [ ] Functionality preserved

Color Blind Testing:
- [ ] Use color blind simulators
- [ ] Information not conveyed by color alone

### User Testing

Test with Actual Users:
- [ ] Screen reader users
- [ ] Keyboard-only users
- [ ] Users with motor impairments
- [ ] Users with cognitive disabilities
- [ ] Users with low vision

---

## ACCESSIBILITY CHECKLIST

### Critical (Must Have)

- [ ] All images have alt text
- [ ] All interactive elements keyboard accessible
- [ ] Focus indicators visible
- [ ] Color contrast meets 4.5:1 (normal text)
- [ ] Color contrast meets 3:1 (large text, UI components)
- [ ] Information not conveyed by color alone
- [ ] All form inputs have labels
- [ ] Heading hierarchy correct (no skipped levels)
- [ ] One H1 per page
- [ ] HTML is valid
- [ ] No keyboard traps
- [ ] Page title unique and descriptive
- [ ] Lang attribute on HTML
- [ ] Skip link provided
- [ ] Semantic HTML used
- [ ] ARIA used correctly (when needed)

### Important (Should Have)

- [ ] Error messages provide suggestions
- [ ] Link text descriptive
- [ ] Consistent navigation
- [ ] Breadcrumbs provided
- [ ] Multiple ways to find content
- [ ] Tables have headers
- [ ] Lists use proper markup
- [ ] Focus order logical
- [ ] Touch targets 44x44px
- [ ] Zoom up to 200% supported
- [ ] Modals manage focus correctly
- [ ] Live regions for dynamic content
- [ ] Videos have captions
- [ ] Auto-play can be paused

### Recommended (Nice to Have)

- [ ] Reduced motion support
- [ ] High contrast mode support
- [ ] Dark mode (for light sensitivity)
- [ ] Adjustable text size controls
- [ ] Keyboard shortcuts documented
- [ ] Accessibility statement page
- [ ] VPAT (Voluntary Product Accessibility Template)

---

## ACCESSIBILITY STATEMENT

Create Accessibility Statement Page:

Content to Include:
- Commitment to accessibility
- Standards followed (WCAG 2.1 AA)
- Known issues (if any)
- Contact for accessibility concerns
- Last updated date
- Feedback mechanism

Example:
```
Accessibility Statement

We are committed to ensuring digital accessibility for people with disabilities. We continually improve the user experience for everyone and apply relevant accessibility standards.

Standards:
We aim to conform to WCAG 2.1 Level AA standards.

Feedback:
We welcome your feedback on the accessibility of this site.
Email: accessibility@example.com
Phone: +1-555-555-5555

Last Updated: [Date]
```

---

## NOTES & SPECIAL REQUIREMENTS
_______________________________________________
_______________________________________________
_______________________________________________

---

## LEGAL CONSIDERATIONS

Compliance Laws:
- [ ] ADA (Americans with Disabilities Act) - USA
- [ ] Section 508 - USA Federal
- [ ] EN 301 549 - European Union
- [ ] Accessibility for Ontarians with Disabilities Act - Canada
- [ ] Other: _______________

Legal Review: [Yes/No]
Last Legal Review: _______________
```

---

## ✅ IMPLEMENTATION PROMPT FOR LOVABLE

After filling this template:

```
Implement Accessibility (WCAG 2.1 AA) based on the completed specification.

CONTEXT: I have defined comprehensive accessibility requirements ensuring the website is usable by people with disabilities, meeting WCAG 2.1 Level AA standards.

TASK:
1. Add alt text to all images (descriptive for informative, empty for decorative)
2. Implement proper semantic HTML (header, nav, main, article, section, footer)
3. Ensure all interactive elements are keyboard accessible
4. Add visible focus indicators (ring-2 ring-blue-500) to all interactive elements
5. Verify color contrast meets 4.5:1 (normal text) and 3:1 (large text/UI)
6. Associate labels with all form inputs
7. Implement proper heading hierarchy (one H1, no skipped levels)
8. Add ARIA attributes where needed (roles, labels, states)
9. Create skip link for keyboard users
10. Test with screen reader and keyboard-only navigation

GUIDELINES:
- Semantic HTML first, ARIA only when needed
- Every interactive element must be keyboard accessible
- Focus indicators must be visible (not outline: none)
- All images need alt attributes (even if empty)
- Form inputs must have associated labels
- Color contrast must meet WCAG AA (4.5:1 normal, 3:1 large)
- Don't rely on color alone to convey information
- Test with keyboard, screen reader, and zoom

CONSTRAINTS:
- Minimum contrast 4.5:1 for normal text
- Minimum contrast 3:1 for large text and UI components
- Touch targets minimum 44x44px
- Alt text required on all images
- Labels required on all form inputs
- One H1 per page, logical heading hierarchy
- Valid HTML (no duplicate IDs)
- All functionality available via keyboard

[Paste your filled accessibility template here]

EXPECTED DELIVERABLES:
1. All images with appropriate alt text
2. Semantic HTML structure throughout
3. Keyboard navigation working on all elements
4. Visible focus indicators
5. Color contrast meeting WCAG AA
6. Form labels properly associated
7. Proper heading hierarchy
8. ARIA attributes where needed
9. Skip link implemented
10. Passed automated accessibility tests
```

---

## 📝 USAGE INSTRUCTIONS

1. **Test early and often** - accessibility easier to build in than retrofit
2. **Use semantic HTML** - correct elements for meaning, not just styling
3. **Keyboard test everything** - unplug mouse, navigate entire site
4. **Check color contrast** - use WebAIM Contrast Checker
5. **Alt text matters** - describe images meaningfully
6. **Form labels required** - every input needs associated label
7. **ARIA carefully** - use only when semantic HTML insufficient
8. **Test with screen readers** - NVDA (free), VoiceOver (built-in Mac/iOS)

---

## 💡 BEST PRACTICES

- Accessibility benefits everyone, not just disabled users
- Semantic HTML provides accessibility for free
- ARIA is powerful but can make things worse if used incorrectly
- Keyboard accessibility is foundation - must work without mouse
- Focus indicators must be visible - never remove without replacement
- Alt text should describe what's in image, not repeat surrounding text
- Form validation errors must be announced to screen readers
- Color contrast is often forgotten but critical for readability
- Headings provide document structure for screen reader users
- Skip links save keyboard users time navigating repetitive content
- Test with real assistive technology, not just automated tools
- Automated tools catch ~30% of issues - manual testing essential
- Screen reader testing reveals many issues automated tools miss

---

## ⚠️ CRITICAL REMINDERS

- Accessibility is a legal requirement in many jurisdictions (ADA, Section 508)
- WCAG 2.1 Level AA is typically the minimum legal standard
- Missing alt text is one of most common accessibility violations
- Removing focus indicators (outline: none) breaks keyboard navigation
- Poor color contrast affects millions (color blindness, low vision)
- Form labels are required - placeholder is not a label
- Keyboard traps are severe accessibility failures
- ARIA can make accessibility worse if used incorrectly
- Semantic HTML > ARIA (use native elements when possible)
- Screen readers announce content differently than visual presentation
- Automated testing catches only ~30% of accessibility issues
- Real user testing with disabled users is invaluable
- One H1 per page is best practice for accessibility and SEO
- Headings must not skip levels (H1 → H3 is wrong)
- alt="" (empty) is correct for decorative images
- Keyboard accessibility benefits many, not just screen reader users
- Focus management in modals/dialogs is complex but critical
- Live regions announce dynamic content to screen readers
- Touch targets < 44x44px cause problems on mobile
- Text zoom to 200% is WCAG requirement - test it
