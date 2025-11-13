# TEMPLATE 5.3: FORMS & DATA COLLECTION SETUP

## 📋 PURPOSE
This template defines the complete form system including validation, submission handling, data collection, storage, and integration with CRM/database systems.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Implement Forms & Data Collection System based on the following specification:

## FORM LIBRARY CONFIGURATION

Form Library: [React Hook Form / Formik / Final Form / Custom]
Validation Library: [Zod / Yup / Joi / Custom]

Form Management Approach:
- Controlled Components: [Yes/No]
- Uncontrolled Components: [Yes/No]
- Form State Management: [React Hook Form / Redux / Context / Local state]

## FORM INVENTORY

Total Number of Forms: _______________

### Form 1: _______________

Form Name: _______________
Form Purpose: _______________
Form Location: _______________ (page/URL)
Form Type: [Contact / Lead capture / Signup / Booking / Survey / Feedback / Other]

Form Priority: [Critical / High / Medium / Low]
Conversion Goal: _______________

---

### Form 2: _______________

[Repeat structure for each form...]

---

### Form 3: _______________

[Repeat structure...]

---

[Continue for all forms...]

---

## CONTACT FORM CONFIGURATION (Example: Main Contact Form)

### Form Identification

Form ID: _______________
Form Name: Contact Form
Form URL: /contact
Form Purpose: Customer inquiries and lead capture

### Form Layout

Layout Style: [Single column / Two columns / Grid / Floating labels]
Responsive Behavior:
- Desktop: [Two columns / Single column]
- Mobile: [Single column]

Form Width: [Full width / Centered / Sidebar]
Max Width: _______________ px

Form Container:
- Background: _______________
- Border: _______________
- Border Radius: _______________
- Shadow: _______________
- Padding: _______________

### Form Fields

Total Fields: _______________

Field 1: Name
- Label: _______________
- Field Type: [Text / Email / Tel / Number / Select / Textarea / Checkbox / Radio / File]
- Input Type: text
- Required: [Yes/No]
- Placeholder: _______________
- Default Value: _______________
- Auto-focus: [Yes/No]
- Auto-complete: [Yes/No]
- Auto-complete Value: "name"
- Validation Rules:
  * Min Length: _______________
  * Max Length: _______________
  * Pattern: _______________
  * Custom Validation: _______________
- Error Messages:
  * Required: "Please enter your name"
  * Min Length: "Name must be at least X characters"
  * Max Length: "Name cannot exceed X characters"
  * Pattern: "Please enter a valid name"
- Help Text: _______________ (optional)
- Tooltip: _______________ (optional)
- Field Width: [Full width / Half / Third / Custom]
- Character Counter: [Yes/No]
- Disabled: [Yes/No]
- Read-only: [Yes/No]

Field 2: Email
- Label: _______________
- Field Type: Email
- Input Type: email
- Required: [Yes/No]
- Placeholder: _______________
- Default Value: _______________
- Auto-complete: "email"
- Validation Rules:
  * Email Format: [Yes/No]
  * Domain Validation: [Yes/No]
  * Disposable Email Check: [Yes/No]
  * MX Record Check: [Yes/No]
- Error Messages:
  * Required: "Email is required"
  * Invalid Format: "Please enter a valid email address"
  * Disposable: "Disposable email addresses are not allowed"
- Help Text: _______________
- Field Width: _______________

Field 3: Phone
- Label: _______________
- Field Type: Tel
- Required: [Yes/No]
- Placeholder: _______________
- Format: [International / Country-specific]
- Phone Library: [react-phone-number-input / libphonenumber-js / Custom]
- Country Selector: [Yes/No]
- Default Country: _______________
- Validation Rules:
  * Valid Phone Format: [Yes/No]
  * Allowed Countries: _______________
- Error Messages:
  * Required: _______________
  * Invalid Format: _______________
- Field Width: _______________

Field 4: Company
- Label: _______________
- Field Type: Text
- Required: [Yes/No]
- Placeholder: _______________
- Validation: _______________
- Error Messages: _______________
- Field Width: _______________

Field 5: Job Title/Role
- Label: _______________
- Field Type: [Text / Select]
- Required: [Yes/No]
- If Select, Options:
  * Option 1: _______________
  * Option 2: _______________
  * Option 3: _______________
  * [Continue...]
  * Other: [Allow custom text]
- Placeholder: _______________
- Field Width: _______________

Field 6: Subject/Inquiry Type
- Label: _______________
- Field Type: Select
- Required: [Yes/No]
- Options:
  * Sales Inquiry
  * Technical Support
  * Partnership
  * Feedback
  * Other
- Default Option: [None / First option]
- Placeholder: "Select a topic"
- Field Width: _______________

Field 7: Message
- Label: _______________
- Field Type: Textarea
- Required: [Yes/No]
- Placeholder: _______________
- Rows: _______________ (initial height)
- Max Length: _______________ characters
- Character Counter: [Yes/No]
- Auto-expand: [Yes/No]
- Validation Rules:
  * Min Length: _______________ characters
  * Max Length: _______________ characters
- Error Messages: _______________
- Field Width: Full width

Field 8: How did you hear about us?
- Label: _______________
- Field Type: Select
- Required: [No]
- Options:
  * Search Engine (Google, Bing)
  * Social Media
  * Referral
  * Advertisement
  * Blog/Content
  * Other
- Field Width: _______________

Field 9: Newsletter Opt-in
- Label: "Send me product updates and marketing emails"
- Field Type: Checkbox
- Required: [No]
- Default: [Unchecked]
- Position: [Before submit / After submit]

Field 10: Terms & Conditions
- Label: "I agree to the [Terms of Service] and [Privacy Policy]"
- Field Type: Checkbox
- Required: [Yes/No]
- Links Open In: [New tab / Modal]
- Error Message: "You must agree to the terms to continue"

[Continue for all fields...]

### Field Styling

Input Style:
- Background: _______________
- Border: _______________
- Border Radius: _______________
- Padding: _______________
- Font Size: _______________
- Height: _______________

Focus State:
- Border Color: _______________
- Ring: [Yes/No]
- Ring Color: _______________
- Background: _______________

Error State:
- Border Color: _______________
- Background: _______________
- Icon: [Yes/No]
- Icon Position: [Left / Right]

Success State (optional):
- Show Success Indicator: [Yes/No]
- Border Color: _______________
- Icon: [Checkmark]

Disabled State:
- Background: _______________
- Cursor: not-allowed
- Opacity: _______________

### Form Validation

Validation Strategy: [On blur / On change / On submit / Combination]

Real-time Validation:
- Enable: [Yes/No]
- Validate On: [Blur / Change / Blur then change]
- Debounce Delay: _______________ ms

Error Display:
- Position: [Below field / Inline / Tooltip / Summary at top]
- Style: [Text / Icon + text / Highlighted]
- Color: _______________
- Icon: [Yes/No]

Error Message Timing:
- Show On: [Validation fail / Focus loss / Submit attempt]
- Hide On: [Field correction / Focus / Manual dismiss]

Required Field Indicator:
- Show Asterisk: [Yes/No]
- Position: [After label / Before label]
- Color: _______________
- "Required" Text: [Yes/No]

### Submit Button

Button Configuration:
- Text: _______________
- Position: [Left / Center / Right / Full width]
- Size: [Small / Medium / Large / Full width]
- Style: [Primary / Secondary / Custom]
- Icon: [Yes/No]
- Icon Position: [Left / Right]

Loading State:
- Show Spinner: [Yes/No]
- Button Text During Loading: _______________
- Disable Button: [Yes/No]
- Disable All Fields: [Yes/No]

Disabled State:
- Disable Until Valid: [Yes/No]
- Opacity: _______________
- Cursor: not-allowed
- Tooltip: _______________ (reason disabled)

Success State:
- Change Button After Success: [Yes/No]
- Success Text: _______________
- Success Icon: [Checkmark]
- Duration: _______________ seconds

### Form Submission

Submission Process:

Step 1: Client-side Validation
- Validate All Fields: [Yes/No]
- Stop If Errors: [Yes/No]
- Scroll to First Error: [Yes/No]
- Focus First Error Field: [Yes/No]

Step 2: Data Preparation
- Sanitize Inputs: [Yes/No]
- Trim Whitespace: [Yes/No]
- Format Phone Numbers: [Yes/No]
- Lowercase Email: [Yes/No]

Step 3: Submission
- Submit Method: [POST / GET]
- Submit Endpoint: _______________
- Headers: _______________
- Timeout: _______________ seconds

Step 4: Loading State
- Show Loading Indicator: [Yes/No]
- Disable Form: [Yes/No]
- Loading Message: _______________

Step 5: Response Handling
- Success HTTP Codes: [200, 201]
- Error HTTP Codes: [400, 500]

Success Response:
- Show Success Message: [Yes/No]
- Success Message: _______________
- Success Position: [Inline / Modal / Toast / New page]
- Redirect: [Yes/No]
- Redirect URL: _______________
- Redirect Delay: _______________ seconds
- Reset Form: [Yes/No]
- Keep Form Data: [Yes/No]

Error Response:
- Show Error Message: [Yes/No]
- Error Message: _______________
- Error Position: [Top of form / Inline / Modal / Toast]
- Field-Specific Errors: [Yes/No]
- Retry Option: [Yes/No]
- Keep Form Data: [Yes/No]

### Form Security

Security Measures:

CSRF Protection:
- Enable: [Yes/No]
- Token Type: [Double-submit cookie / Synchronizer token]
- Token in: [Header / Hidden field / Both]

CAPTCHA:
- Enable: [Yes/No]
- Provider: [Google reCAPTCHA v3 / hCaptcha / Cloudflare Turnstile]
- Score Threshold: _______________ (for reCAPTCHA v3)
- Position: [Before submit / Invisible]
- Fallback for Low Score: [Visible CAPTCHA / Block / Manual review]

Rate Limiting:
- Enable: [Yes/No]
- Limit: _______________ submissions per hour per IP
- Limit: _______________ submissions per hour per email
- Error Message: _______________
- Lockout Duration: _______________ minutes

Honeypot Field:
- Enable: [Yes/No]
- Field Name: _______________
- Hidden with CSS: [Yes/No]
- Reject if Filled: [Yes/No]

Input Sanitization:
- HTML Entities: [Encode]
- Script Tags: [Strip / Encode]
- SQL Injection: [Prepared statements / ORM]
- XSS Protection: [Encode / Sanitize]

### Data Processing

Data Handling:

Submission Data Structure:
```json
{
  "name": "...",
  "email": "...",
  "phone": "...",
  "company": "...",
  "subject": "...",
  "message": "...",
  "source": "...",
  "consent": true/false,
  "timestamp": "...",
  "metadata": {
    "url": "...",
    "referrer": "...",
    "utm_source": "...",
    "utm_medium": "...",
    "utm_campaign": "..."
  }
}
```

Metadata Collection:
- [ ] Submission timestamp
- [ ] Page URL
- [ ] Referrer
- [ ] UTM parameters
- [ ] User Agent
- [ ] IP Address (if allowed)
- [ ] Device type
- [ ] Browser
- [ ] Other: _______________

Data Storage:

Primary Storage: [Database / CRM / Email / Multiple]

If Database:
- Table Name: _______________
- Fields Mapping: _______________
- Encryption: [Yes/No]
- Encrypted Fields: _______________

If CRM Integration:
- CRM: [HubSpot / Salesforce / Pipedrive / ActiveCampaign / Other]
- API Endpoint: _______________
- API Key Storage: [Environment variable]
- Field Mapping: _______________
- Lead Status: _______________
- Lead Source: _______________

If Email:
- Send To: _______________
- CC: _______________
- Subject: _______________
- Email Template: _______________
- Include All Fields: [Yes/No]
- Format: [Plain text / HTML / Both]

Backup Storage: [Yes/No]
If Yes: _______________

### Confirmation Email

Send Confirmation Email: [Yes/No]

If Yes:

Email Configuration:
- Send To: [User's email]
- From: _______________
- From Name: _______________
- Reply-To: _______________
- Subject: _______________
- Preview Text: _______________

Email Content:
- Template: [Plain text / HTML / Both]
- Content: _______________
- Include Submission Details: [Yes/No]
- CTA Button: _______________ (optional)

Email Timing:
- Send: [Immediately / After delay / Async]
- Delay: _______________ seconds

### Analytics & Tracking

Form Analytics:

Events to Track:
- [ ] Form viewed
- [ ] Form started (first field interaction)
- [ ] Field focused
- [ ] Field completed
- [ ] Field error
- [ ] Form submitted
- [ ] Form submission success
- [ ] Form submission error
- [ ] Form abandoned

Event Properties:
- Form ID/Name
- Field Name
- Error Type
- Submission Time
- Time to Complete
- Abandonment Point

Conversion Tracking:
- Track as Conversion: [Yes/No]
- Conversion Value: _______________
- Conversion Goal: _______________

Heatmap/Session Recording:
- Enable: [Yes/No]
- Tool: [Hotjar / FullStory / LogRocket / Other]

### Form Variants (A/B Testing)

A/B Testing: [Yes/No]

If Yes:

Test Elements:
- [ ] Form length (short vs long)
- [ ] Field order
- [ ] Button text
- [ ] Button color
- [ ] Field labels
- [ ] Placeholder text
- [ ] Required vs optional fields
- [ ] Privacy/consent messaging

Testing Tool: [Google Optimize / Optimizely / VWO / Custom]

### Accessibility

Accessibility Features:

Form Structure:
- [ ] Semantic HTML (fieldset, legend)
- [ ] Proper label association (for/id)
- [ ] ARIA labels where needed
- [ ] ARIA required attributes
- [ ] ARIA invalid on errors
- [ ] ARIA describedby for help text
- [ ] Role attributes

Keyboard Navigation:
- [ ] Logical tab order
- [ ] Enter to submit
- [ ] Escape to clear
- [ ] Arrow keys in selects
- [ ] Focus visible indicators

Screen Reader Support:
- [ ] Error announcements
- [ ] Success announcements
- [ ] Required field announcements
- [ ] Help text accessible
- [ ] Loading state announced

Visual:
- [ ] High contrast mode
- [ ] Color not sole indicator
- [ ] Focus indicators visible
- [ ] Error states clear
- [ ] Text resize support

### Mobile Optimization

Mobile-Specific:

Input Types:
- Email: type="email" (triggers email keyboard)
- Phone: type="tel" (triggers numeric keyboard)
- Number: type="number" (triggers numeric keyboard)
- URL: type="url" (triggers URL keyboard)

Mobile Layout:
- Single Column: [Yes/No]
- Field Spacing: _______________ (touch-friendly)
- Button Size: _______________ (min 44x44px)
- Font Size: _______________ (min 16px to prevent zoom)

Mobile-Specific Features:
- [ ] Auto-zoom prevention
- [ ] Sticky submit button
- [ ] Progress indicator
- [ ] Simplified validation messages
- [ ] Touch-optimized selects

### Multi-Step Forms

Is Multi-Step: [Yes/No]

If Yes:

Number of Steps: _______________

Step 1: _______________
- Fields: _______________
- Validation: [On next / On blur]
- Skippable: [Yes/No]

Step 2: _______________
[Repeat structure...]

Step 3: _______________
[Repeat structure...]

Progress Indicator:
- Show: [Yes/No]
- Style: [Stepper / Progress bar / Step count]
- Position: [Top / Bottom / Sidebar]

Navigation:
- Next Button: _______________
- Previous Button: _______________
- Save Draft: [Yes/No]
- Exit Warning: [Yes/No]

Data Persistence:
- Save Between Steps: [Local storage / Session / Database]
- Resume Later: [Yes/No]
- Expiry: _______________

### Conditional Logic

Conditional Fields: [Yes/No]

If Yes:

Condition 1:
- Trigger Field: _______________
- Trigger Value: _______________
- Show Fields: _______________
- Hide Fields: _______________
- Action: [Show/Hide / Enable/Disable / Required/Optional]

Condition 2:
[Repeat structure...]

### File Upload Fields (if applicable)

File Upload: [Yes/No]

If Yes:

Upload Configuration:
- Max File Size: _______________ MB
- Allowed File Types: _______________
- Multiple Files: [Yes/No]
- Max Files: _______________
- Upload Method: [Direct / Presigned URL]
- Storage: [Supabase Storage / S3 / Cloudinary]

UI Elements:
- Drag & Drop: [Yes/No]
- Preview: [Yes/No]
- Progress Bar: [Yes/No]
- File List: [Yes/No]
- Remove File: [Yes/No]

Validation:
- File Size Check: [Yes/No]
- File Type Check: [Yes/No]
- Virus Scan: [Yes/No]

---

## LEAD CAPTURE FORMS

### Newsletter Signup Form

Form Type: Newsletter/Email Capture
Form Locations: [Footer / Modal / Sidebar / Dedicated page]

Fields:
- Email: Required
- Name: [Optional / Required / Not included]
- Consent Checkbox: [Yes/No]

Submit Button Text: _______________

Success Message: _______________
Error Message: _______________

Integration:
- Email Service: [Mailchimp / ConvertKit / SendGrid / Supabase / Custom]
- List/Audience: _______________
- Double Opt-in: [Yes/No]
- Welcome Email: [Yes/No]

Form Triggers (for modals):
- Exit Intent: [Yes/No]
- Time Delay: _______________ seconds
- Scroll Depth: _______________% 
- Click Trigger: [Yes/No]

### Demo Request Form

Fields:
- Name
- Email
- Company
- Role/Title
- Company Size
- Phone (optional)
- Preferred Date/Time
- Message/Requirements

Integration:
- CRM: _______________
- Calendar: [Calendly / Google Calendar / Custom]
- Sales Team Notification: [Email / Slack / CRM]

---

## FEEDBACK & SURVEY FORMS

### Feedback Form

Form Purpose: Collect user feedback
Form Location: _______________

Fields:
- Rating: [Stars / Emoji / Number scale]
- Category: [Select from options]
- Message: [Textarea]
- Email (optional)

Submit: _______________
Storage: _______________

### NPS Survey

Question: "How likely are you to recommend [Product] to a friend?"
Scale: 0-10
Follow-up: "What's the primary reason for your score?"

Trigger: [After X days / After action / Manual]
Display: [Modal / Inline / Email]

---

## FORM PERFORMANCE

Performance Optimization:

- [ ] Lazy load form fields
- [ ] Debounce validation
- [ ] Optimize bundle size
- [ ] Code splitting
- [ ] Minimize re-renders
- [ ] Use uncontrolled inputs where appropriate

Performance Metrics:
- Time to Interactive: < 3 seconds
- First Input Delay: < 100ms
- Form Submission Time: < 2 seconds

---

## GDPR & PRIVACY COMPLIANCE

GDPR Compliance:

- [ ] Clear consent checkboxes
- [ ] Separate marketing consent
- [ ] Privacy policy linked
- [ ] Data retention policy stated
- [ ] Right to access data
- [ ] Right to delete data
- [ ] Data processing basis disclosed

Required Disclosures:
- Who collects data: _______________
- How data is used: _______________
- Who data is shared with: _______________
- How to withdraw consent: _______________
- Data retention period: _______________

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
Implement Forms & Data Collection System based on the completed specification.

CONTEXT: I have defined a comprehensive form system with validation, submission handling, security measures, and data collection workflows.

TASK:
1. Set up React Hook Form with Zod validation
2. Create contact form with all specified fields
3. Implement real-time validation with error messages
4. Build submit button with loading states
5. Set up form submission to backend/CRM
6. Implement CAPTCHA (reCAPTCHA v3)
7. Create confirmation email system
8. Add analytics tracking for form events
9. Implement CSRF protection
10. Build success/error message displays

GUIDELINES:
- Mobile-first responsive design
- Use design system tokens for styling
- Accessible forms (WCAG 2.1 AA)
- Clear, helpful error messages
- Loading states for all async operations
- Proper input types for mobile keyboards
- Touch-friendly targets (44x44px minimum)
- Smooth validation without blocking user

CONSTRAINTS:
- Form must be accessible via keyboard
- All fields must have proper labels
- Error messages must be clear and actionable
- CAPTCHA score threshold: 0.5 (reCAPTCHA v3)
- Form submission timeout: 10 seconds
- Must work without JavaScript for basic functionality
- GDPR compliant consent collection

[Paste your filled forms template here]

EXPECTED DELIVERABLES:
1. Working contact form with validation
2. Real-time field validation
3. Submit button with loading state
4. Success/error message displays
5. Form submission to backend/CRM
6. CAPTCHA integration
7. Confirmation email sending
8. Analytics event tracking
9. Mobile-optimized layout
10. Accessibility features implemented
```

---

## 📝 USAGE INSTRUCTIONS

1. **Keep forms short** - only ask for essential information
2. **Clear labels** - no placeholder-only fields
3. **Real-time validation** - on blur, not on every keystroke
4. **Helpful errors** - specific, actionable messages
5. **Mobile keyboards** - proper input types
6. **Progress indication** - especially for multi-step
7. **Save data** - don't lose user input on errors
8. **Thank users** - clear success messages

---

## 💡 BEST PRACTICES

- Use type="email" for email inputs (mobile keyboard optimization)
- Use type="tel" for phone inputs (numeric keyboard on mobile)
- Label every input (no placeholder-only labels)
- Show password requirements before user types
- Validate on blur, then on change after first error
- Don't clear form on submission error
- Disable submit button while processing
- Show clear success message after submission
- Send confirmation email for important forms
- Use autocomplete attributes for better UX
- Group related fields with fieldset/legend
- Make required fields obvious (asterisk or "required" text)
- Keep error messages close to fields
- Don't use CAPTCHA unless necessary (friction point)
- Test with real users, especially on mobile
- Track form abandonment to find UX issues

---

## ⚠️ CRITICAL REMINDERS

- Forms are conversion points - optimize ruthlessly
- Every field you add decreases completion rate
- Mobile users abandon forms faster than desktop
- Clear error messages prevent support requests
- CAPTCHA adds friction - use only when needed (spam)
- Confirmation emails build trust and reduce anxiety
- GDPR requires explicit consent - pre-checked boxes illegal
- Never validate as user types (too aggressive)
- Always sanitize input server-side (never trust client)
- Rate limiting prevents abuse and spam
- Honeypot fields catch simple bots
- Test forms on actual mobile devices
- Accessibility is legal requirement in many jurisdictions
- Form abandonment analytics reveal UX problems
- Multi-step forms work for complex data, fail for simple
- Long forms need save/resume functionality
- File uploads need clear size/type restrictions
- Loading states prevent duplicate submissions
