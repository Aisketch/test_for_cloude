# TEMPLATE 4.4: FORMS & LEAD CAPTURE COMPONENTS

## 📋 PURPOSE
This template defines reusable form components for lead generation, contact forms, newsletter signups, and user input collection that maximize conversions while maintaining excellent UX.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Create Forms & Lead Capture Components based on the following specification:

## COMPONENT LIBRARY OVERVIEW

Component Set: Forms & Lead Capture
Design System: [Reference to Template 1.2]
Framework: React + TypeScript + React Hook Form
Styling: Tailwind CSS with semantic tokens
Validation: Zod or Yup schemas

Components to Create:
1. Text Input
2. Email Input
3. Select/Dropdown
4. Textarea
5. Checkbox/Radio
6. Newsletter Signup
7. Contact Form
8. Multi-Step Form
9. Lead Capture Modal
10. Inline Signup Form

---

## COMPONENT 4.4.1: TEXT INPUT

### Component Props

```typescript
interface TextInputProps {
  name: string;
  label?: string;
  placeholder?: string;
  required?: boolean;
  error?: string;
  helpText?: string;
  icon?: string;
  iconPosition?: 'left' | 'right';
  disabled?: boolean;
  maxLength?: number;
  showCharCount?: boolean;
}
```

### Visual Design

Container:
- Width: [Full width / Custom]
- Margin Bottom: _______________

Label:
- Font Size: _______________
- Font Weight: _______________
- Color: _______________
- Margin Bottom: _______________
- Required Indicator: [Asterisk / Badge / None]

Input Field:
- Height: _______________
- Padding: _______________
- Border: _______________ (use input semantic token)
- Border Radius: _______________ (use design system)
- Background: _______________
- Font Size: _______________
- Color: _______________

Placeholder:
- Color: _______________ (muted-foreground)
- Font Style: [Normal / Italic]

Icon:
- Position: [Left / Right]
- Size: _______________
- Color: _______________
- Padding: _______________

### States

Default:
- Border: [input token]
- Background: _______________

Focus:
- Border: [primary or ring token]
- Ring: [Yes/No]
- Ring Color: _______________
- Ring Width: _______________
- Ring Offset: _______________
- Outline: [None - use ring instead]

Error:
- Border: [destructive token]
- Background: _______________ (subtle destructive tint)
- Ring: [destructive]

Disabled:
- Background: [muted]
- Color: [muted-foreground]
- Cursor: [not-allowed]
- Opacity: _______________

### Help Text & Error Messages

Help Text:
- Position: [Below input]
- Font Size: _______________
- Color: [muted-foreground]
- Margin Top: _______________

Error Message:
- Position: [Below input]
- Font Size: _______________
- Color: [destructive]
- Icon: [AlertCircle / X]
- Animation: [Shake / Fade in]

Character Count (if enabled):
- Position: [Bottom right]
- Font Size: _______________
- Color: _______________
- Warning Color: _______________ (when near limit)

---

## COMPONENT 4.4.2: EMAIL INPUT

### Component Props

```typescript
interface EmailInputProps extends TextInputProps {
  validateOnBlur?: boolean;
  suggestions?: boolean;
  autocomplete?: string;
}
```

### Visual Design

[Inherits from Text Input]

Specific Features:
- Type: email
- Autocomplete: email
- Input Mode: email (mobile)
- Pattern Validation: Email regex

Email Suggestions:
- Show: [Yes/No]
- Suggestions: [Common domains: @gmail.com, @yahoo.com, etc.]
- Dropdown Style: _______________

Validation:
- Validate on: [Blur / Submit / Change]
- Show Success: [Checkmark icon / Green border / None]

---

## COMPONENT 4.4.3: SELECT / DROPDOWN

### Component Props

```typescript
interface SelectProps {
  name: string;
  label?: string;
  placeholder?: string;
  options: SelectOption[];
  required?: boolean;
  error?: string;
  disabled?: boolean;
  searchable?: boolean;
  multiple?: boolean;
}

interface SelectOption {
  value: string;
  label: string;
  icon?: string;
  disabled?: boolean;
}
```

### Visual Design

Select Trigger:
- Height: _______________
- Padding: _______________
- Border: _______________
- Border Radius: _______________
- Background: _______________
- Font Size: _______________

Chevron Icon:
- Position: [Right]
- Icon: [ChevronDown]
- Size: _______________
- Color: _______________
- Animation: [Rotate when open]

### Dropdown Menu

Styling:
- Background: _______________
- Border: _______________
- Border Radius: _______________
- Shadow: _______________
- Max Height: _______________ (with scroll)
- Padding: _______________
- Z-Index: _______________

Position: [Below trigger / Above if no space]
Animation: [Fade in / Slide down]

Option Item:
- Padding: _______________
- Font Size: _______________
- Color: _______________
- Hover Background: _______________
- Selected Background: _______________
- Selected Indicator: [Checkmark / Bold / Background]

Icon in Option:
- Size: _______________
- Position: [Left]
- Spacing: _______________

Disabled Option:
- Color: [muted-foreground]
- Cursor: [not-allowed]
- Opacity: _______________

Search Input (if searchable):
- Position: [Top of dropdown]
- Placeholder: "Search..."
- Styling: _______________
- Padding: _______________

Empty State:
- Message: "No options found"
- Styling: _______________

---

## COMPONENT 4.4.4: TEXTAREA

### Component Props

```typescript
interface TextareaProps {
  name: string;
  label?: string;
  placeholder?: string;
  required?: boolean;
  error?: string;
  helpText?: string;
  rows?: number;
  maxLength?: number;
  showCharCount?: boolean;
  autoResize?: boolean;
}
```

### Visual Design

Textarea Field:
- Min Height: _______________ (or rows)
- Padding: _______________
- Border: _______________
- Border Radius: _______________
- Background: _______________
- Font Size: _______________
- Line Height: _______________
- Resize: [Vertical / None / Both]

Auto-Resize: [Yes/No]
If Yes:
- Min Rows: _______________
- Max Rows: _______________
- Resize Behavior: [Smooth transition]

[Other styling same as Text Input]

---

## COMPONENT 4.4.5: CHECKBOX / RADIO

### Component Props

```typescript
interface CheckboxProps {
  name: string;
  label: string;
  required?: boolean;
  error?: string;
  disabled?: boolean;
  description?: string;
}

interface RadioGroupProps {
  name: string;
  label?: string;
  options: RadioOption[];
  required?: boolean;
  error?: string;
  direction?: 'vertical' | 'horizontal';
}
```

### Checkbox Visual Design

Layout: [Horizontal / Vertical]

Checkbox Box:
- Size: _______________
- Border: _______________
- Border Radius: _______________
- Background: _______________
- Checked Background: [primary]
- Checked Color: [primary-foreground]

Checkmark:
- Icon: [Check / CheckIcon]
- Size: _______________
- Animation: [Scale in / Fade in]

Label:
- Position: [Right of box]
- Font Size: _______________
- Color: _______________
- Margin Left: _______________
- Cursor: [pointer]

Description (optional):
- Font Size: _______________
- Color: [muted-foreground]
- Margin Top: _______________

States:
- Hover: [Border color change]
- Focus: [Ring around box]
- Disabled: [Muted colors, not-allowed cursor]

### Radio Visual Design

Radio Button:
- Size: _______________
- Border: _______________
- Border Radius: [Full - circle]
- Background: _______________
- Selected: [Inner circle fills]

Inner Circle (Selected):
- Size: _______________ (smaller than outer)
- Color: [primary]
- Animation: [Scale in]

Label & States: [Same as Checkbox]

Radio Group Layout:
- Direction: [Vertical / Horizontal]
- Spacing: _______________

---

## COMPONENT 4.4.6: NEWSLETTER SIGNUP

### Component Props

```typescript
interface NewsletterSignupProps {
  variant?: 'inline' | 'modal' | 'section';
  headline?: string;
  description?: string;
  buttonText?: string;
  placeholder?: string;
  showPrivacy?: boolean;
  compactMode?: boolean;
}
```

### Visual Design

Variant Options:

Inline (Horizontal):
- Layout: [Input + Button in row]
- Input: [Grows to fill space]
- Button: [Auto width / Fixed width]
- Border: [Shared / Separate]
- Gap: _______________

Section (Vertical):
- Layout: [Stacked]
- Input: [Full width]
- Button: [Full width / Centered]
- Spacing: _______________
- Container: [Card / No card]

Modal:
- Trigger: [Button / Link / Auto-popup]
- Content: [Headline + Description + Form]
- Width: _______________

### Content

Headline:
- Show: [Yes/No]
- Text: _______________
- Font Size: _______________
- Font Weight: _______________
- Margin Bottom: _______________

Description:
- Show: [Yes/No]
- Text: _______________
- Font Size: _______________
- Color: _______________
- Max Width: _______________

Email Input:
- Placeholder: _______________ (e.g., "Enter your email")
- Required: [Yes]
- Validation: [Email format]

Submit Button:
- Text: _______________ (e.g., "Subscribe", "Get updates")
- Size: _______________
- Style: [Primary]
- Icon: [None / Arrow / Mail]

Privacy Notice:
- Show: [Yes/No]
- Text: "We respect your privacy. Unsubscribe anytime."
- Font Size: _______________
- Color: [muted-foreground]
- Position: [Below button]

### Success State

Message: "Thanks for subscribing!"
Icon: [CheckCircle / Mail]
Color: [success]
Animation: [Fade in / Check animation]
Duration: [Show for 3s then reset / Permanent]

### Error State

Message: [Validation error or server error]
Color: [destructive]
Position: [Below input]

---

## COMPONENT 4.4.7: CONTACT FORM

### Component Props

```typescript
interface ContactFormProps {
  variant?: 'simple' | 'detailed';
  showSubject?: boolean;
  showPhone?: boolean;
  showCompany?: boolean;
  submitText?: string;
  onSubmit: (data: ContactFormData) => Promise<void>;
}

interface ContactFormData {
  name: string;
  email: string;
  subject?: string;
  phone?: string;
  company?: string;
  message: string;
}
```

### Form Structure

Simple Variant:
Fields:
1. Name (Text Input)
2. Email (Email Input)
3. Message (Textarea)
4. Submit Button

Detailed Variant:
Fields:
1. Name (Text Input)
2. Email (Email Input)
3. Phone (Text Input) - Optional
4. Company (Text Input) - Optional
5. Subject (Select or Text Input)
6. Message (Textarea)
7. Submit Button

### Visual Design

Form Layout:
- Width: [Full width / Max width container]
- Max Width: _______________
- Padding: _______________

Field Spacing:
- Vertical Gap: _______________
- Two Column Layout: [Yes/No on desktop]
- Mobile: [Always single column]

Name & Email Row (if two columns):
- Layout: [50-50 / 60-40]
- Gap: _______________

Subject Options (if select):
- Options:
  * General Inquiry
  * Sales
  * Support
  * Partnership
  * Other

Message Textarea:
- Rows: _______________ (e.g., 5-6)
- Max Length: _______________
- Placeholder: "Your message..."

Submit Button:
- Width: [Full width / Auto]
- Size: [Large]
- Text: _______________
- Loading State: [Spinner + "Sending..."]
- Success State: [Checkmark + "Sent!"]

Privacy/GDPR:
- Checkbox: [Optional consent checkbox]
- Text: "I agree to the privacy policy"
- Link: [To privacy policy]

Response Time Info:
- Text: "We'll respond within 24 hours"
- Position: [Above/below button]
- Icon: [Clock]

### Success State

Show: [Replace form / Show message above form]
Message: "Thanks! We'll be in touch soon."
Icon: [CheckCircle / Mail]
Color: [success]
Reset: [After 5s / Manual / Don't reset]

### Error State

Show: [Above form / Inline]
Message: "Something went wrong. Please try again."
Color: [destructive]
Retry: [Automatic / Manual]

---

## COMPONENT 4.4.8: MULTI-STEP FORM

### Component Props

```typescript
interface MultiStepFormProps {
  steps: FormStep[];
  currentStep: number;
  showProgress?: boolean;
  showStepLabels?: boolean;
  onStepChange?: (step: number) => void;
  onComplete: (data: any) => void;
}

interface FormStep {
  title: string;
  description?: string;
  fields: FormField[];
  validation?: ValidationSchema;
}
```

### Progress Indicator

Type: [Steps / Progress bar / Numbers / Both]

Steps Indicator:
- Layout: [Horizontal / Vertical]
- Step Style: [Circles / Bars / Numbers / Icons]
- Spacing: _______________

Step States:
- Completed: 
  * Color: [success or primary]
  * Icon: [Checkmark]
  * Background: _______________
  
- Current:
  * Color: [primary]
  * Ring: [Yes/No]
  * Background: _______________
  
- Upcoming:
  * Color: [muted]
  * Background: _______________

Connector Line:
- Show: [Yes/No]
- Style: [Solid / Dashed]
- Color: [Completed = primary, Upcoming = muted]

Labels:
- Position: [Below step / Right of step]
- Font Size: _______________
- Show Always: [Yes/No]
- Current Step Larger: [Yes/No]

Progress Bar (if used):
- Height: _______________
- Background: [muted]
- Fill Color: [primary]
- Border Radius: _______________
- Show Percentage: [Yes/No]

### Step Content

Container:
- Padding: _______________
- Min Height: _______________ (prevent layout shift)

Step Header:
- Title Font Size: _______________
- Description Font Size: _______________
- Spacing: _______________

Field Layout:
- [Same as Contact Form]
- Responsive: [Single column mobile]

### Navigation

Button Layout:
- Position: [Below form / Fixed bottom]
- Layout: [Space between]
- Spacing: _______________

Back Button:
- Show: [Not on first step]
- Text: "Back" or "Previous"
- Style: [Secondary / Ghost]
- Icon: [ArrowLeft]

Next Button:
- Text: "Next" or "Continue"
- Style: [Primary]
- Icon: [ArrowRight]
- Position: [Right]

Submit Button:
- Text: "Submit" or "Complete"
- Show: [Only on last step]
- Style: [Primary]
- Full Width: [Yes/No]

### Behavior

Step Validation:
- Validate: [On next button click]
- Block Next: [If validation fails]
- Show Errors: [Inline / Summary]

Save Progress:
- Auto-save: [Yes/No]
- Local Storage: [Yes/No]
- Resume: [On page reload]

Keyboard Navigation:
- Enter: [Next step / Submit]
- Arrows: [Navigate steps (if allowed)]

---

## COMPONENT 4.4.9: LEAD CAPTURE MODAL

### Component Props

```typescript
interface LeadCaptureModalProps {
  trigger?: 'time' | 'scroll' | 'exit' | 'manual';
  delay?: number;
  scrollPercentage?: number;
  headline: string;
  description?: string;
  fields: FormField[];
  submitText?: string;
  closeButton?: boolean;
  dismissible?: boolean;
  showOnce?: boolean;
}
```

### Trigger Configuration

Trigger Types:

Time-based:
- Delay: _______________ seconds

Scroll-based:
- Trigger at: _______________% scroll depth

Exit Intent:
- Trigger: [When mouse leaves viewport top]
- Sensitivity: _______________

Manual:
- Triggered by: [Button click / Event / Function call]

Show Once:
- Cookie Duration: _______________ days
- Override: [Manual trigger always shows]

### Modal Design

Overlay:
- Background: _______________
- Opacity: _______________
- Blur: [Yes/No] _______________
- Click to Close: [Yes/No]

Modal Container:
- Width: _______________
- Max Width: _______________
- Background: _______________
- Border Radius: _______________
- Shadow: _______________
- Padding: _______________

Animation:
- Entrance: [Fade in / Scale in / Slide up]
- Exit: [Fade out / Scale out / Slide down]
- Duration: _______________

Close Button:
- Position: [Top right / Top left]
- Icon: [X / Close]
- Size: _______________
- Color: _______________

### Content

Header:
- Headline Font Size: _______________
- Headline Weight: _______________
- Description Font Size: _______________
- Description Color: _______________
- Spacing: _______________

Image/Visual (optional):
- Position: [Top / Left / Right]
- Size: _______________
- Style: _______________

Form Fields:
- Layout: [Vertical / Compact]
- Field Types: [Minimal for conversion]
- Typical: Name + Email
- Optional: Phone, Company

Submit Button:
- Width: [Full width]
- Size: [Large]
- Text: _______________

Privacy Notice:
- Text: _______________
- Font Size: _______________
- Link to Policy: [Yes/No]

### Mobile Behavior

Modal on Mobile:
- Width: [Full width / 90% / Slide up]
- Position: [Center / Bottom sheet]
- Safe Area: [Respect notches]

Close Method:
- Close Button: [Yes]
- Swipe Down: [Yes/No]
- Back Button: [Yes]

---

## COMPONENT 4.4.10: INLINE SIGNUP FORM

### Component Props

```typescript
interface InlineSignupProps {
  variant?: 'compact' | 'expanded';
  headline?: string;
  ctaText?: string;
  fields?: 'email' | 'email-name';
  inline?: boolean;
}
```

### Visual Design

Compact Variant:
- Layout: [Horizontal - input + button]
- Input Border: [Shared with button / Separate]
- Button: [Attached / Separate]

Expanded Variant:
- Layout: [Vertical]
- Multiple Fields: [Name + Email]
- Spacing: _______________

Inline Variant:
- Use Case: [Within content]
- Width: [Auto / Full]
- Alignment: [Left / Center]

Styling:
- Background: [Transparent / Card]
- Border: _______________
- Padding: _______________

---

## SHARED SPECIFICATIONS

### Validation

Validation Timing:
- On Blur: [Yes/No]
- On Change: [Yes/No - after first submit]
- On Submit: [Yes - always]

Validation Display:
- Error Position: [Below field / Inline]
- Error Icon: [Yes/No]
- Error Animation: [Shake / Fade in]

Required Field Indicator:
- Style: [Asterisk / "Required" badge / Both]
- Color: [destructive]

### Form States

Loading:
- Button: [Spinner + "Submitting..."]
- Disable Fields: [Yes]
- Overlay: [Optional dim]

Success:
- Message Position: [Replace form / Above form / Modal]
- Icon: [CheckCircle]
- Color: [success]
- Animation: [Success animation]
- Duration: [3s / Permanent / Until dismissed]

Error:
- Message Position: [Above form / Inline]
- Icon: [AlertCircle]
- Color: [destructive]
- Allow Retry: [Yes]

### Accessibility

All Forms Must Include:
- [ ] Label for every input
- [ ] Proper form structure
- [ ] ARIA labels and descriptions
- [ ] Error announcement for screen readers
- [ ] Keyboard navigation (Tab, Enter, Escape)
- [ ] Focus management
- [ ] Required field indicators
- [ ] Error focus (focus first error on submit)
- [ ] Success announcement
- [ ] Fieldset for grouped inputs

### Security

- [ ] CSRF protection
- [ ] Rate limiting
- [ ] Spam protection (honeypot / reCAPTCHA)
- [ ] Input sanitization
- [ ] SQL injection prevention
- [ ] XSS prevention

### Mobile Optimization

- [ ] Input types (email, tel, number)
- [ ] Autocomplete attributes
- [ ] Appropriate keyboard (email, numeric)
- [ ] Zoom disabled for inputs (font-size 16px min)
- [ ] Touch-friendly targets (44px min)
- [ ] Sticky form on scroll (if long)

### Performance

- [ ] Client-side validation (fast feedback)
- [ ] Debounced validation (don't validate every keystroke)
- [ ] Lazy load heavy components
- [ ] Optimize images in forms
- [ ] Minimize JavaScript bundle

### Analytics

Track:
- Form views
- Field interactions
- Field completion rate
- Abandonment points
- Submit attempts
- Submission success/failure
- Time to complete
- Error occurrences

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
Create Forms & Lead Capture Components based on the completed specification.

CONTEXT: I have defined a comprehensive form component library with inputs, validation, multi-step forms, and lead capture elements optimized for conversion.

TASK:
1. Create TextInput component with all states
2. Build EmailInput with validation
3. Implement Select dropdown with search
4. Create Textarea with auto-resize
5. Build Checkbox and Radio components
6. Implement NewsletterSignup variants
7. Create ContactForm (simple & detailed)
8. Build MultiStepForm with progress
9. Implement LeadCaptureModal with triggers
10. Create InlineSignupForm

GUIDELINES:
- Use React Hook Form + Zod validation
- Mobile-first responsive design
- Semantic tokens from design system
- Clear error states and messages
- Loading states for all submissions
- Success states with animations
- Accessibility: labels, ARIA, keyboard nav
- Spam protection (honeypot minimum)

CONSTRAINTS:
- All inputs must have labels
- Error messages must be clear
- Form submission optimistic/pessimistic UI
- Color contrast WCAG AA compliant
- Touch targets 44px minimum
- Works on all modern browsers
- Input font-size 16px min (prevent zoom)

[Paste your filled forms template here]

EXPECTED DELIVERABLES:
1. TextInput component with validation
2. EmailInput component
3. Select/Dropdown component
4. Textarea component
5. Checkbox/Radio components
6. NewsletterSignup component
7. ContactForm component
8. MultiStepForm component
9. LeadCaptureModal with triggers
10. InlineSignupForm component
```

---

## 📝 USAGE INSTRUCTIONS

1. **Minimize fields** - each field reduces conversion
2. **Clear labels** - users shouldn't guess
3. **Instant validation** - catch errors early
4. **Mobile keyboard** - use correct input types
5. **Success feedback** - confirm submission
6. **Error recovery** - make it easy to fix mistakes
7. **Progress indication** - for multi-step forms
8. **Smart defaults** - pre-fill when possible

---

## 💡 BEST PRACTICES

- Every extra form field reduces conversion by ~10%
- Inline validation increases completion by 20-30%
- Multi-step forms work better for complex forms (5+ fields)
- Modal forms grab attention but can feel interruptive
- Newsletter forms convert best when value is clear
- "Submit" is weak CTA - use action verbs
- Show password strength meter for password fields
- Auto-focus first field on page load (desktop only)
- Use placeholder examples: "e.g., john@company.com"
- Group related fields visually
- Mark optional fields not required (fewer asterisks)
- Success messages should be obvious and confirmatory
- Mobile: use tel type for phone, date picker for dates

---

## ⚠️ CRITICAL REMINDERS

- Forms are highest-friction conversion points
- Mobile users abandon forms 2x more than desktop
- Validation errors must be actionable
- Multi-step forms need clear progress
- Modal timing critical - too early/late reduces conversion
- Email validation must allow + and other valid characters
- Required fields should be minimized
- Error messages shouldn't blame user
- Success state must be unmissable
- Form abandonment tracking essential
- A/B test form fields - huge conversion impact
- GDPR compliance needed for EU users
- Spam protection required but invisible to users
- Accessibility non-negotiable for forms
- Test on real mobile devices - keyboards, autocomplete
- Never lose user data on errors
