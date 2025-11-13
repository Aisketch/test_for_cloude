# Auth Pages Template - Technical Specification

**Page Type:** Authentication Pages (Sign In / Sign Up)
**URL Pattern:** `/signin`, `/signup`
**Priority:** Critical
**Approach:** Mobile First
**Last Updated:** November 12, 2025

---

## Page Overview

**Purpose:** Secure user authentication (login/registration) with optimal UX and conversion rate.

**Key Goals:**
- Simple, friction-free sign up/sign in
- Clear value proposition
- Social login options
- Strong security
- Mobile-optimized

---

## Sign Up Page Structure (`/signup`)

### Layout Structure

#### Mobile & Desktop (Centered Form)
```
┌─────────────────────────────────────┐
│                                     │
│  [Logo] ← Back to Home              │
│                                     │
│  ┌───────────────────────────────┐  │
│  │                               │  │
│  │  [Sign Up Form Container]     │  │
│  │                               │  │
│  └───────────────────────────────┘  │
│                                     │
└─────────────────────────────────────┘
```

**Alternative Layout (Split Screen - Desktop Only):**
```
┌────────────────────────────────────────────┐
│                    │                       │
│  [Left Panel]      │  [Right Panel]        │
│                    │                       │
│  Brand message     │  Sign Up Form         │
│  Value props       │                       │
│  Testimonial       │                       │
│                    │                       │
└────────────────────────────────────────────┘
```

---

### Block 01: Header
```
┌─────────────────────────────────────┐
│  [Logo]               [Need help?]  │
└─────────────────────────────────────┘
```

**Logo:**
- Size: 120px × 32px
- Link: `/` (homepage)
- Position: Top left

**Help Link:**
- Text: "Need help?"
- Link: `/contact` or support
- Font size: 14px
- Color: Secondary text

**Minimal:** No main navigation (keep focus on auth)

---

### Block 02: Sign Up Form Container
```
┌──────────────────────────────────────┐
│                                      │
│  [H1: Create Your Account]           │
│                                      │
│  [Subtitle: Start your free trial]   │
│                                      │
│  ┌────────────────────────────────┐  │
│  │ [Continue with Google]         │  │
│  └────────────────────────────────┘  │
│  ┌────────────────────────────────┐  │
│  │ [Continue with GitHub]         │  │
│  └────────────────────────────────┘  │
│                                      │
│  ────── OR ──────                    │
│                                      │
│  ┌────────────────────────────────┐  │
│  │ Full Name *                    │  │
│  └────────────────────────────────┘  │
│                                      │
│  ┌────────────────────────────────┐  │
│  │ Email Address *                │  │
│  └────────────────────────────────┘  │
│                                      │
│  ┌────────────────────────────────┐  │
│  │ Password *                     │  │
│  │                           [👁] │  │
│  └────────────────────────────────┘  │
│                                      │
│  Password strength: [Weak ████▒▒▒▒] │
│                                      │
│  ☐ I agree to Terms and Privacy      │
│                                      │
│  [Create Account Button]             │
│                                      │
│  Already have an account? [Sign in]  │
│                                      │
└──────────────────────────────────────┘
```

---

### Form Elements

**H1:**
- Text: "Create Your Account"
- Font size Mobile: 28px / 34px
- Font size Desktop: 32px / 40px
- Font weight: 700
- Text align: Center

**Subtitle:**
- Text: "Start your free trial. No credit card required."
- Font size: 16px / 24px
- Color: Secondary text
- Text align: Center
- Margin-bottom: 32px

---

**Social Login Buttons:**

**Google Button:**
- Text: "Continue with Google"
- Icon: Google logo (left)
- Background: White
- Border: 1px solid #D1D5DB
- Height: 48px
- Font size: 15px
- Font weight: 500
- Border-radius: 8px
- Hover: Background #F9FAFB

**GitHub Button:** (Optional)
- Text: "Continue with GitHub"
- Icon: GitHub logo
- Same styling as Google

**Spacing:** 12px between buttons, 24px below

---

**Divider:**
- Text: "OR"
- Position: Centered
- Lines: Horizontal, #E5E7EB
- Font size: 13px
- Color: #9CA3AF
- Margin: 24px 0

---

**Form Inputs:**

**Full Name:**
- Placeholder: "John Doe"
- Type: text
- Required: Yes
- Autocomplete: name

**Email:**
- Placeholder: "you@example.com"
- Type: email
- Required: Yes
- Autocomplete: email
- Validation: Real-time on blur

**Password:**
- Placeholder: "Create a strong password"
- Type: password (toggle to text)
- Required: Yes
- Min length: 8 characters
- Autocomplete: new-password
- Show/Hide icon: 👁️ (right side)

**Password Toggle:**
- Icon: Eye (show) / Eye-slash (hide)
- Position: Absolute right 12px
- Size: 20px
- Color: #9CA3AF
- Cursor: pointer
- Click: Toggle password visibility

**Password Strength Indicator:**
- Visual: Progress bar
- Colors:
  - Weak: Red (#EF4444)
  - Fair: Orange (#F59E0B)
  - Good: Yellow (#FBBF24)
  - Strong: Green (#10B981)
- Criteria:
  - Length >= 8
  - Contains uppercase
  - Contains lowercase
  - Contains number
  - Contains special character
- Text: "Weak" / "Fair" / "Good" / "Strong"
- Font size: 13px
- Margin-top: 8px

**Input Styling:**
- Height: 48px
- Border: 1px solid #D1D5DB
- Border-radius: 8px
- Padding: 12px 16px
- Font size: 16px (prevent zoom on mobile)
- Background: White
- Focus:
  - Border: 2px solid #6366F1 (Primary)
  - Outline: None
  - Box-shadow: 0 0 0 3px rgba(99,102,241,0.1)

**Error State:**
- Border: 1px solid #EF4444 (Red)
- Error message below input
- Font size: 13px
- Color: #EF4444
- Margin-top: 4px

---

**Terms Checkbox:**
- Required: Yes
- Text: "I agree to the [Terms of Service](#) and [Privacy Policy](#)"
- Font size: 14px
- Links: Underline, primary color
- Error: Show red border and message if unchecked on submit

---

**Create Account Button:**
- Text: "Create Account"
- Width: 100%
- Height: 52px
- Background: Primary color (#6366F1)
- Color: White
- Font size: 16px
- Font weight: 600
- Border-radius: 8px
- Border: None
- Margin-top: 24px
- Cursor: pointer
- Disabled state:
  - Background: #D1D5DB
  - Cursor: not-allowed
- Loading state:
  - Text: "Creating account..."
  - Spinner icon
  - Disabled
- Hover (enabled):
  - Background: Darken 10%

---

**Sign In Link:**
- Text: "Already have an account? [Sign in](#)"
- Font size: 14px
- Color: Secondary text
- Link: Primary color, hover underline
- Text align: Center
- Margin-top: 20px

---

**Container Styling:**
- Max-width: 440px
- Background: White
- Padding: 40px 24px (mobile), 48px 40px (desktop)
- Border-radius: 16px (if not full-width)
- Box-shadow: 0 4px 6px rgba(0,0,0,0.1) (if floating)
- Margin: 40px auto

---

## Sign In Page Structure (`/signin`)

### Form Container
```
┌──────────────────────────────────────┐
│                                      │
│  [H1: Welcome Back]                  │
│                                      │
│  [Subtitle: Sign in to your account] │
│                                      │
│  ┌────────────────────────────────┐  │
│  │ [Continue with Google]         │  │
│  └────────────────────────────────┘  │
│  ┌────────────────────────────────┐  │
│  │ [Continue with GitHub]         │  │
│  └────────────────────────────────┘  │
│                                      │
│  ────── OR ──────                    │
│                                      │
│  ┌────────────────────────────────┐  │
│  │ Email Address *                │  │
│  └────────────────────────────────┘  │
│                                      │
│  ┌────────────────────────────────┐  │
│  │ Password *                [👁] │  │
│  └────────────────────────────────┘  │
│                                      │
│  [Forgot password?]                  │
│                                      │
│  ☐ Remember me                       │
│                                      │
│  [Sign In Button]                    │
│                                      │
│  Don't have an account? [Sign up]    │
│                                      │
└──────────────────────────────────────┘
```

**H1:** "Welcome Back"

**Inputs:**
- Email (autocomplete: email)
- Password (autocomplete: current-password)

**Forgot Password Link:**
- Text: "Forgot password?"
- Position: Right aligned
- Font size: 14px
- Color: Primary
- Link: `/forgot-password`

**Remember Me Checkbox:**
- Optional
- Font size: 14px
- Position: Left aligned

**Sign In Button:**
- Text: "Sign In"
- Same styling as Create Account

**Sign Up Link:**
- Text: "Don't have an account? [Sign up](#)"
- Link: `/signup`

---

## Forgot Password Page (`/forgot-password`)

```
┌──────────────────────────────────────┐
│                                      │
│  [H1: Reset Password]                │
│                                      │
│  [Subtitle: Enter your email...]     │
│                                      │
│  ┌────────────────────────────────┐  │
│  │ Email Address *                │  │
│  └────────────────────────────────┘  │
│                                      │
│  [Send Reset Link Button]            │
│                                      │
│  [← Back to Sign In]                 │
│                                      │
└──────────────────────────────────────┘
```

**Flow:**
1. User enters email
2. Click "Send Reset Link"
3. Show success: "Check your email for reset instructions"
4. Email contains link: `/reset-password?token=XXX`
5. User clicks link, enters new password
6. Success: Redirect to `/signin`

---

## Reset Password Page (`/reset-password?token=XXX`)

```
┌──────────────────────────────────────┐
│                                      │
│  [H1: Create New Password]           │
│                                      │
│  ┌────────────────────────────────┐  │
│  │ New Password *            [👁] │  │
│  └────────────────────────────────┘  │
│                                      │
│  [Password strength indicator]       │
│                                      │
│  ┌────────────────────────────────┐  │
│  │ Confirm Password *        [👁] │  │
│  └────────────────────────────────┘  │
│                                      │
│  [Reset Password Button]             │
│                                      │
└──────────────────────────────────────┘
```

**Validation:**
- Passwords match
- New password meets strength requirements
- Token valid and not expired

---

## Interactive Elements & States

### 1. Form Validation
- **Real-time:** Validate on blur
- **Submit:** Validate all fields
- **Errors:** Show below each field
- **Success:** Green checkmark icon (optional)

### 2. Social OAuth Flow
- Click button
- Redirect to provider (Google/GitHub)
- User authorizes
- Redirect back to app with token
- Create account or sign in
- Redirect to dashboard

### 3. Loading States
- **Button:** Show spinner, disable
- **Input:** Disable during submission
- **Overlay:** Optional full-page loader

### 4. Error States
- **Invalid credentials:** "Email or password is incorrect"
- **Email exists:** "This email is already registered. [Sign in](#)"
- **Network error:** "Connection error. Please try again."
- **Rate limit:** "Too many attempts. Try again in 15 minutes."

### 5. Success States
- **Sign Up:** Show success message, redirect to onboarding or dashboard
- **Sign In:** Redirect to dashboard or previous page
- **Password Reset:** "Password reset successful. [Sign in](#)"

---

## Security Features

### Password Requirements
- Min 8 characters
- At least 1 uppercase letter (recommended)
- At least 1 number (recommended)
- At least 1 special character (recommended)

### Protection
- **Rate Limiting:** Max 5 attempts per 15 min
- **CSRF Protection:** Tokens
- **XSS Protection:** Sanitize inputs
- **HTTPS Only:** Enforce SSL
- **Password Hashing:** bcrypt or Argon2
- **Session Management:** Secure cookies
- **2FA:** Optional (for later phase)

### Email Verification
- **On Sign Up:** Send verification email
- **Unverified:** Show banner, limit access
- **Verified:** Full access

---

## Redirects & Flow

### Sign Up Flow:
1. `/signup`
2. User fills form
3. Submit
4. Success → Redirect to `/onboarding` or `/dashboard`
5. Show welcome message

### Sign In Flow:
1. `/signin`
2. User enters credentials
3. Submit
4. Success → Redirect to `/dashboard` or `returnTo` URL
5. Error → Show message, stay on page

### Forgot Password Flow:
1. `/forgot-password`
2. Enter email
3. Success → "Check your email"
4. Email link → `/reset-password?token=XXX`
5. Enter new password
6. Success → `/signin` with success message

---

## Accessibility

- All inputs have labels (visible or aria-label)
- Error messages announced to screen readers
- Keyboard navigation (Tab, Enter)
- Focus indicators visible
- Password toggle accessible (button with aria-label)
- Form has proper role="form"

---

## SEO

**Sign Up:**
- Title: "Sign Up | Delphi - Create Your Account"
- Meta robots: noindex, nofollow (don't index auth pages)

**Sign In:**
- Title: "Sign In | Delphi - Welcome Back"
- Meta robots: noindex, nofollow

---

## Mobile Optimization

- Input font size: 16px (prevent auto-zoom iOS)
- Large touch targets: 48px min height
- Autofocus on email input (desktop only)
- Autocomplete attributes
- Show password toggle (since mobile keyboards harder)
- Full-width buttons for easy tapping
- Minimal scrolling: Keep form above fold if possible

---

## Analytics & Tracking

**Events to Track:**
- Page view: Sign Up / Sign In
- Button click: Social login (Google, GitHub)
- Form submit: Email sign up / sign in
- Error: Validation error, auth error
- Success: Account created, signed in
- Abandon: User leaves form incomplete

---

## A/B Testing Opportunities
- Social login position (top vs bottom)
- Number of form fields (2-step vs single form)
- Button copy ("Create Account" vs "Get Started Free")
- Value proposition text
- Social proof (testimonials, user count)

---

**End of Auth Pages Template**
