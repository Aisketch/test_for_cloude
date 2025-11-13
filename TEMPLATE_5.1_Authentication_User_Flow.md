# TEMPLATE 5.1: AUTHENTICATION & USER FLOW INTEGRATION

## 📋 PURPOSE
This template defines the complete authentication system, user flows, and account management functionality for your SaaS application.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Implement Authentication & User Flow System based on the following specification:

## AUTHENTICATION PROVIDER CONFIGURATION

Primary Auth Provider: [Supabase / Custom / Firebase / Auth0 / Other]
Backend: _______________

Database Tables Needed:
- [ ] users (profiles)
- [ ] sessions
- [ ] user_preferences
- [ ] user_roles
- [ ] api_keys (if applicable)
- [ ] oauth_connections
- [ ] audit_logs
- [ ] Other: _______________

## AUTHENTICATION METHODS

### Email/Password Authentication

Enable Email/Password: [Yes/No]

If Yes:

Email Requirements:
- Format Validation: [Yes/No]
- Domain Restrictions: [None / Whitelist / Blacklist]
- Allowed Domains: _______________
- Blocked Domains: _______________

Password Requirements:
- Minimum Length: _______________ characters
- Require Uppercase: [Yes/No]
- Require Lowercase: [Yes/No]
- Require Numbers: [Yes/No]
- Require Special Characters: [Yes/No]
- Disallow Common Passwords: [Yes/No]
- Password Strength Indicator: [Yes/No]

Password Security:
- Hashing Algorithm: [bcrypt / argon2 / scrypt]
- Salt Rounds: _______________
- Breach Database Check: [Yes/No] (e.g., Have I Been Pwned API)

### Social Login (OAuth)

Enable Social Login: [Yes/No]

If Yes:

Social Providers:

Provider 1: [Google]
- Enable: [Yes/No]
- Client ID: _______________ (from env variable)
- Scopes: [email, profile, other]
- Button Text: _______________
- Button Style: [Brand colors / Custom]
- Account Linking: [Automatic / Manual / Ask user]

Provider 2: [GitHub]
- Enable: [Yes/No]
- Client ID: _______________
- Scopes: [user:email, read:user, other]
- Button Text: _______________
- Button Style: _______________
- Account Linking: _______________

Provider 3: [Microsoft]
- Enable: [Yes/No]
- Client ID: _______________
- Scopes: _______________
- Button Text: _______________
- Button Style: _______________
- Account Linking: _______________

Provider 4: [LinkedIn]
- Enable: [Yes/No]
- Configuration: _______________

Provider 5: [Facebook]
- Enable: [Yes/No]
- Configuration: _______________

Provider 6: [Twitter/X]
- Enable: [Yes/No]
- Configuration: _______________

Other Providers: _______________

Social Login Flow:
- Create Account Automatically: [Yes/No]
- Require Additional Info: [Yes/No]
- Default User Role: _______________
- Email Verification Required: [Yes/No]

### Magic Link Authentication

Enable Magic Link: [Yes/No]

If Yes:

Magic Link Configuration:
- Token Expiry: _______________ minutes
- Single Use Only: [Yes/No]
- Rate Limiting: _______________ requests per hour
- Custom Email Template: [Yes/No]
- Redirect URL After Login: _______________

Email Template:
- Subject: _______________
- Preview Text: _______________
- Body Content: _______________
- CTA Button Text: _______________
- Sender Name: _______________
- Sender Email: _______________

### SSO / SAML (Enterprise)

Enable SSO: [Yes/No]

If Yes:

SSO Configuration:
- Provider: [Okta / Azure AD / Google Workspace / OneLogin / Custom]
- SAML Version: [2.0]
- Metadata URL: _______________
- Entity ID: _______________
- ACS URL: _______________
- Available For Plans: [Enterprise only / Custom]

Just-in-Time (JIT) Provisioning:
- Enable: [Yes/No]
- Auto-create Users: [Yes/No]
- Default Role: _______________
- Attribute Mapping: _______________

### Multi-Factor Authentication (MFA)

Enable MFA: [Yes/No]

If Yes:

MFA Configuration:
- Requirement: [Optional / Required / Required for admins / Required for certain actions]
- Enforcement Timeline: _______________

MFA Methods:

Method 1: [TOTP / Authenticator App]
- Enable: [Yes/No]
- Supported Apps: [Google Authenticator, Authy, 1Password, Microsoft Authenticator]
- Backup Codes: [Yes/No]
- Number of Backup Codes: _______________

Method 2: [SMS]
- Enable: [Yes/No]
- SMS Provider: [Twilio / Other]
- Supported Countries: _______________
- Rate Limiting: _______________

Method 3: [Email]
- Enable: [Yes/No]
- Code Expiry: _______________ minutes
- Rate Limiting: _______________

Method 4: [Hardware Keys (WebAuthn)]
- Enable: [Yes/No]
- Supported: [YubiKey, Security Key, Biometric]

MFA Setup Flow:
- Require During Signup: [Yes/No]
- Prompt After Login: [Yes/No]
- Grace Period: _______________ days
- Recovery Options: _______________

### Biometric Authentication (Mobile/Desktop)

Enable Biometric: [Yes/No]

If Yes:
- Face ID: [Yes/No]
- Touch ID: [Yes/No]
- Windows Hello: [Yes/No]
- Fallback: [PIN / Password]

---

## SIGNUP FLOW

### Signup Page Configuration

Signup Page URL: /signup (or /[lang]/signup)
Page Title: _______________
Page Description: _______________

Signup Form Layout: [Centered / Split / Sidebar]
Background: _______________

Signup Form Fields:

Field 1:
- Label: _______________
- Type: [Text / Email / Password]
- Required: [Yes/No]
- Validation: _______________
- Placeholder: _______________
- Auto-focus: [Yes/No]

Field 2: 
[Repeat structure...]

Field 3:
[Repeat structure...]

[Continue for all fields...]

Common Fields:
- [ ] Full Name / First & Last Name
- [ ] Email
- [ ] Password
- [ ] Company Name (optional for B2B)
- [ ] Phone Number (optional)
- [ ] How did you hear about us?
- [ ] Job Title/Role
- [ ] Team Size
- [ ] Use Case

Terms & Privacy:
- [ ] Checkbox: "I agree to Terms of Service and Privacy Policy"
- Required: [Yes/No]
- Links: [Inline / Modal / New tab]

Marketing Consent:
- [ ] Checkbox: "Send me product updates and marketing emails"
- Required: [No]
- Default: [Unchecked / Checked]

Social Signup Buttons:
Position: [Above form / Below form / Both]
Separator Text: _______________ (e.g., "or continue with email")

Submit Button:
- Text: _______________
- Loading State: _______________
- Disabled Until Valid: [Yes/No]

Alternative Actions:
- Login Link: "Already have an account? [Log in]"
- Position: [Below form / Top right]

### Signup Process Flow

Step 1: Form Submission
- Client-side Validation: [Yes/No]
- Server-side Validation: [Yes/No]
- Error Handling: _______________

Step 2: Account Creation
- Create User Record: [Yes/No]
- Generate User ID: [UUID / Auto-increment]
- Initial User Role: _______________
- Default Preferences: _______________

Step 3: Email Verification
- Required: [Yes/No]
- Send Verification Email: [Immediately / After trial period]
- Verification Link Expiry: _______________ hours
- Resend Limit: _______________ times per hour

Email Verification Email:
- Subject: _______________
- Preview Text: _______________
- Body Content: _______________
- CTA Button: _______________
- Sender: _______________

Verified Action:
- Redirect To: _______________
- Show Message: _______________
- Enable Full Access: [Yes/No]

Step 4: Welcome Email (Optional)
- Send Welcome Email: [Yes/No]
- Timing: [Immediate / After verification / Delayed]
- Content: _______________

Step 5: Onboarding
- Start Onboarding: [Immediately / After verification]
- Onboarding Type: [Modal / Separate page / Product tour]
- Skippable: [Yes/No]

Step 6: Redirect After Signup
- Destination: [Dashboard / Onboarding / Profile setup / Product]
- URL: _______________

### Signup Validations & Security

Rate Limiting:
- Max Attempts: _______________ per hour per IP
- Cooldown Period: _______________ minutes
- Error Message: _______________

Email Validation:
- Real-time Check: [Yes/No]
- Disposable Email Block: [Yes/No]
- MX Record Check: [Yes/No]

CAPTCHA:
- Enable: [Yes/No]
- Provider: [Google reCAPTCHA v3 / hCaptcha / Cloudflare Turnstile]
- Threshold Score: _______________
- Show When: [Always / After failed attempts / Suspicious behavior]

Duplicate Prevention:
- Check Existing Email: [Yes/No]
- Error Message: _______________
- Suggest Login: [Yes/No]

---

## LOGIN FLOW

### Login Page Configuration

Login Page URL: /login (or /[lang]/login)
Page Title: _______________
Page Description: _______________

Login Form Layout: [Centered / Split / Sidebar]
Background: _______________

Login Form Fields:

Field 1: Email
- Label: _______________
- Validation: [Email format]
- Remember Email: [Yes/No]
- Auto-complete: [Yes/No]

Field 2: Password
- Label: _______________
- Show/Hide Toggle: [Yes/No]
- Auto-complete: [Yes/No]

Remember Me:
- [ ] Checkbox: "Keep me logged in"
- Default: [Unchecked / Checked]
- Duration: _______________ days

Submit Button:
- Text: _______________
- Loading State: _______________

Forgot Password Link:
- Text: _______________
- Position: [Below password field / Below form]

Social Login Buttons:
Position: [Above form / Below form]
Separator Text: _______________

Alternative Actions:
- Signup Link: "Don't have an account? [Sign up]"
- Position: [Below form / Top right]

### Login Process Flow

Step 1: Credential Validation
- Check Email Exists: [Yes/No]
- Verify Password: [Yes/No]
- Rate Limiting: _______________ attempts per hour

Step 2: Account Status Check
- Check Email Verified: [Yes/No]
- Check Account Active: [Yes/No]
- Check Account Suspended: [Yes/No]

Step 3: MFA Challenge (if enabled)
- Show MFA Prompt: [Yes/No]
- MFA Methods Available: _______________
- Backup Codes Accepted: [Yes/No]

Step 4: Session Creation
- Session Duration: _______________ hours/days
- Session Storage: [Cookie / Local Storage / Both]
- Refresh Token: [Yes/No]
- Refresh Token Duration: _______________ days

Step 5: Redirect After Login
- Default Destination: _______________
- Remember Intended Destination: [Yes/No]
- Different Destinations by Role: [Yes/No]

### Login Error Handling

Failed Login Attempts:
- Max Attempts: _______________ before lockout
- Lockout Duration: _______________ minutes
- Show Remaining Attempts: [Yes/No]
- Error Messages:
  * Invalid Credentials: _______________
  * Account Locked: _______________
  * Email Not Verified: _______________
  * Account Suspended: _______________

Account Lockout:
- Enable Lockout: [Yes/No]
- Unlock Method: [Time-based / Email link / Admin action]
- Notification Email: [Yes/No]

### Login Security

Suspicious Activity Detection:
- New Device Detection: [Yes/No]
- New Location Detection: [Yes/No]
- Notification: [Email / In-app / Both]

Session Management:
- Concurrent Sessions: [Allow / Limit to _____ / Single session only]
- Session Timeout: _______________ minutes of inactivity
- Show Active Sessions: [Yes/No]
- Remote Logout: [Yes/No]

---

## PASSWORD RESET FLOW

### Password Reset Request

Reset Page URL: /reset-password
Page Title: _______________

Request Form:
- Field: Email address
- Button Text: _______________
- Success Message: _______________

Reset Email:
- Subject: _______________
- Preview Text: _______________
- Body Content: _______________
- CTA Button: _______________
- Link Expiry: _______________ hours
- Single Use: [Yes/No]

Rate Limiting:
- Max Requests: _______________ per hour per email
- Error Message: _______________

### Password Reset Completion

Reset Token Validation:
- Check Token Valid: [Yes/No]
- Check Token Expired: [Yes/No]
- Error Page: _______________

New Password Form:
- New Password Field: [Yes/No]
- Confirm Password Field: [Yes/No]
- Password Requirements: [Same as signup]
- Submit Button Text: _______________

Success:
- Message: _______________
- Redirect To: [Login page / Dashboard if logged in]
- Notification: [Yes/No]
- Invalidate All Sessions: [Yes/No]

---

## EMAIL VERIFICATION FLOW

### Verification Email

Trigger: [After signup / Manual request]
Subject: _______________
Content: _______________
Link Expiry: _______________ hours

Verification Page:
- URL: /verify-email?token=...
- Success Message: _______________
- Error Messages: _______________
- Redirect After: _______________

Resend Verification:
- Allow Resend: [Yes/No]
- Resend Limit: _______________ per hour
- Button Location: [Login page / Profile page / Email]

Unverified Account Restrictions:
- Allow Login: [Yes/No]
- Feature Restrictions: _______________
- Show Banner: [Yes/No]
- Reminder Emails: [Yes/No]
- Reminder Schedule: _______________

---

## USER SESSION MANAGEMENT

### Session Configuration

Session Type: [JWT / Session cookies / Database sessions]
Storage: [HTTP-only cookies / Local storage / Session storage]

JWT Configuration (if applicable):
- Secret Key: _______________ (env variable)
- Algorithm: [HS256 / RS256]
- Expiry: _______________ hours
- Refresh Token: [Yes/No]
- Refresh Token Expiry: _______________ days

Cookie Configuration:
- Cookie Name: _______________
- HTTP Only: [Yes/No]
- Secure: [Yes - HTTPS only]
- SameSite: [Strict / Lax / None]
- Domain: _______________
- Path: /

Session Data Stored:
- [ ] User ID
- [ ] Email
- [ ] Name
- [ ] Role
- [ ] Permissions
- [ ] Preferences
- [ ] Last Activity
- [ ] Other: _______________

### Session Lifecycle

Session Creation:
- Create On: [Login / Signup]
- Initial Expiry: _______________

Session Refresh:
- Auto-refresh: [Yes/No]
- Refresh Trigger: [Any activity / Specific actions]
- Sliding Window: [Yes/No]

Session Termination:
- Manual Logout: [Yes/No]
- Automatic Timeout: _______________ minutes inactivity
- Token Expiry: [Yes/No]
- Account Deletion: [Yes/No]

### Session Security

CSRF Protection:
- Enable: [Yes/No]
- Token Type: [Double-submit cookie / Synchronizer token]

Session Hijacking Prevention:
- IP Binding: [Yes/No]
- User Agent Binding: [Yes/No]
- Token Rotation: [Yes/No]

Active Session Management:
- Show Active Sessions: [Yes/No]
- Session Details: [Device, Location, Last Activity]
- Terminate Individual Session: [Yes/No]
- Terminate All Sessions: [Yes/No]

---

## USER PROFILE & ACCOUNT SETTINGS

### Profile Page

Profile Page URL: /profile or /account or /settings
Page Title: _______________

Profile Sections:

Section 1: Personal Information
Fields:
- [ ] Profile Photo
- [ ] Name
- [ ] Email (read-only or editable)
- [ ] Phone
- [ ] Job Title
- [ ] Company
- [ ] Bio
- [ ] Location
- [ ] Timezone
- [ ] Language Preference

Section 2: Account Security
Options:
- [ ] Change Password
- [ ] Enable/Disable MFA
- [ ] View Active Sessions
- [ ] Connected OAuth Accounts
- [ ] API Keys (if applicable)
- [ ] Security Questions

Section 3: Preferences
Options:
- [ ] Language
- [ ] Timezone
- [ ] Date Format
- [ ] Time Format
- [ ] Currency
- [ ] Theme (Light/Dark)
- [ ] Notifications

Section 4: Email Notifications
Categories:
- [ ] Product Updates
- [ ] Marketing Emails
- [ ] Security Alerts
- [ ] Weekly Digest
- [ ] Other: _______________

Section 5: Privacy & Data
Options:
- [ ] Download My Data
- [ ] Delete My Account
- [ ] Data Sharing Preferences
- [ ] Cookie Preferences

Section 6: Billing (if applicable)
Options:
- [ ] Payment Methods
- [ ] Billing History
- [ ] Invoices
- [ ] Subscription Management
- [ ] Usage/Limits

### Profile Updates

Update Process:
- Real-time Save: [Yes/No]
- Save Button Required: [Yes/No]
- Validation: [Client-side / Server-side / Both]
- Success Notification: _______________

Email Change:
- Require Verification: [Yes/No]
- Verify New Email: [Yes/No]
- Verify Old Email: [Yes/No]
- Both Required: [Yes/No]

Photo Upload:
- Allow Upload: [Yes/No]
- Max File Size: _______________ MB
- Allowed Formats: [JPG, PNG, WebP]
- Image Cropping: [Yes/No]
- Storage: [Supabase Storage / S3 / Cloudinary]

---

## ACCOUNT DELETION FLOW

### Account Deletion Process

Deletion Trigger: [User request / Admin action / Automated]

Deletion Requirements:
- Password Confirmation: [Yes/No]
- Email Confirmation: [Yes/No]
- Reason Selection: [Yes/No]
- Feedback Form: [Optional / Required]

Reasons for Deletion:
- [ ] Not using the product
- [ ] Too expensive
- [ ] Missing features
- [ ] Found alternative
- [ ] Privacy concerns
- [ ] Other: _______________

Deletion Confirmation:
- Confirmation Method: [Type "DELETE" / Checkbox / Email link]
- Warning Message: _______________
- Grace Period: _______________ days

Data Retention:
- Immediate Deletion: [Yes/No]
- Soft Delete: [Yes/No]
- Retention Period: _______________ days
- Data to Retain: _______________ (legal requirements)
- Data to Delete: _______________

Post-Deletion:
- Confirmation Email: [Yes/No]
- Reactivation Option: [Yes/No] within _______________ days
- Redirect To: _______________

---

## ROLE-BASED ACCESS CONTROL (RBAC)

### User Roles

Number of Roles: _______________

Role 1: _______________
- Permissions: _______________
- Access Level: _______________
- Default Role: [Yes/No]

Role 2: _______________
[Repeat structure...]

Role 3: _______________
[Repeat structure...]

[Continue for all roles...]

Common Roles:
- [ ] Admin
- [ ] Owner
- [ ] Member
- [ ] Guest/Viewer
- [ ] Custom: _______________

### Permissions System

Permission Types:
- [ ] Read
- [ ] Write
- [ ] Delete
- [ ] Share
- [ ] Admin
- [ ] Custom: _______________

Permission Scope:
- [ ] Global
- [ ] Workspace/Team
- [ ] Project
- [ ] Resource-specific

Role Assignment:
- Assigned By: [Admin / Owner / Self-selection]
- Change Role: [Admin only / Self-service]
- Multiple Roles: [Yes/No]

---

## TEAM/WORKSPACE MANAGEMENT (if applicable)

### Team Structure

Enable Teams: [Yes/No]

Team Features:
- [ ] Create teams/workspaces
- [ ] Invite members
- [ ] Role assignment
- [ ] Team settings
- [ ] Shared resources
- [ ] Team billing

Team Invitation:
- Invitation Method: [Email / Link / Both]
- Require Approval: [Yes/No]
- Auto-join Domain: [Yes/No]
- Allowed Domains: _______________

Member Limits:
- Free Plan: _______________ members
- Paid Plans: _______________

---

## AUTHENTICATION UI COMPONENTS

### Shared Components

Loading States:
- Spinner/Skeleton: [Yes/No]
- Loading Text: _______________

Error Display:
- Position: [Top of form / Inline / Toast]
- Style: [Alert / Inline / Modal]
- Dismissible: [Yes/No]

Success Messages:
- Position: [Top of form / Toast / Redirect]
- Duration: _______________ seconds

Input Styling:
- Use Design System: [Yes/No]
- Error State: [Red border / Icon / Message]
- Focus State: [Ring / Border / Shadow]

Buttons:
- Primary Style: _______________
- Loading State: [Spinner / Text change / Disabled]

---

## SECURITY BEST PRACTICES

Security Measures:

- [ ] HTTPS Only
- [ ] Secure cookies
- [ ] CSRF protection
- [ ] XSS prevention
- [ ] SQL injection prevention
- [ ] Rate limiting
- [ ] Password hashing (bcrypt/argon2)
- [ ] MFA support
- [ ] Session timeout
- [ ] Account lockout
- [ ] Audit logging
- [ ] Security headers

Audit Logging:
- Log Events:
  * Login success/failure
  * Password reset
  * Email change
  * MFA enable/disable
  * Role changes
  * Account deletion
  * Other: _______________

---

## REDIRECT RULES

Protected Routes:
- Redirect Unauthenticated To: /login
- Redirect Authenticated From Login To: _______________
- Remember Intended Destination: [Yes/No]

Role-Based Redirects:
- Admin → _______________
- User → _______________
- Guest → _______________

---

## INTERNATIONALIZATION

Multi-language Support: [Yes/No]

Authentication Text Translation:
- Error Messages: [Yes/No]
- Form Labels: [Yes/No]
- Email Templates: [Yes/No]

Languages Supported: _______________

---

## ANALYTICS & TRACKING

Track Authentication Events:

- [ ] Signup started
- [ ] Signup completed
- [ ] Signup method (email/social)
- [ ] Login success
- [ ] Login failure
- [ ] Logout
- [ ] Password reset requested
- [ ] Password reset completed
- [ ] Email verified
- [ ] MFA enabled
- [ ] Profile updated
- [ ] Account deleted

Analytics Properties:
- User ID
- Email (hashed)
- Signup method
- Login method
- Device type
- Location (country)
- Referral source

---

## TESTING REQUIREMENTS

Test Cases:

Authentication:
- [ ] Successful signup
- [ ] Duplicate email prevention
- [ ] Password validation
- [ ] Email verification
- [ ] Successful login
- [ ] Failed login (wrong password)
- [ ] Account lockout
- [ ] Password reset flow
- [ ] Social login
- [ ] MFA flow
- [ ] Session timeout
- [ ] Logout

Security:
- [ ] CSRF protection
- [ ] Rate limiting
- [ ] SQL injection prevention
- [ ] XSS prevention

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
Implement Authentication & User Flow System based on the completed specification.

CONTEXT: I have defined a comprehensive authentication system with multiple login methods, secure session management, user profiles, and role-based access control.

TASK:
1. Set up Supabase authentication (or chosen provider)
2. Create signup page with form validation
3. Create login page with email/password and social options
4. Implement password reset flow
5. Create email verification system
6. Set up protected routes and redirects
7. Build user profile/settings page
8. Implement MFA (if specified)
9. Create session management
10. Add authentication state management (React Context/Redux)

GUIDELINES:
- Secure by default (HTTPS only, secure cookies)
- Clear error messages without exposing security details
- Loading states for all async operations
- Mobile-responsive authentication pages
- Accessible forms (WCAG 2.1 AA)
- Rate limiting on authentication endpoints
- Audit logging for security events
- Use design system tokens consistently

CONSTRAINTS:
- No passwords stored in plain text
- CSRF protection required
- Rate limiting on all auth endpoints
- Session timeout after inactivity
- Email verification required (if specified)
- MFA required for sensitive operations (if specified)

[Paste your filled authentication template here]

EXPECTED DELIVERABLES:
1. Working signup flow with validation
2. Working login flow (email/password + social)
3. Password reset functionality
4. Email verification system
5. Protected routes with redirects
6. User profile page
7. Session management
8. MFA setup (if specified)
9. Logout functionality
10. Authentication state management
```

---

## 📝 USAGE INSTRUCTIONS

1. **Start with Supabase** - Lovable.dev integrates well with Supabase Auth
2. **Enable email verification** - reduces spam accounts
3. **Require strong passwords** - but not overly complex
4. **Add social login** - reduces friction, increases conversion
5. **Implement MFA** - at least for admins/sensitive actions
6. **Rate limit everything** - prevent brute force attacks
7. **Log security events** - audit trail for investigations
8. **Test thoroughly** - authentication bugs are critical

---

## 💡 BEST PRACTICES

- Never expose detailed error messages ("user not found" vs "invalid credentials")
- Use HTTP-only secure cookies for session management
- Implement proper CSRF protection
- Hash passwords with bcrypt or argon2 (never MD5/SHA1)
- Rate limit authentication attempts
- Use email verification to reduce spam
- Implement account lockout after failed attempts
- Send notifications for suspicious activity (new device/location)
- Provide clear password requirements during signup
- Allow users to see and manage active sessions
- Implement proper logout that invalidates sessions
- Use refresh tokens for long-lived sessions
- Test authentication flows thoroughly
- Have account recovery process for locked accounts

---

## ⚠️ CRITICAL REMINDERS

- Authentication is your first security layer - get it right
- Never store passwords in plain text or use weak hashing
- Rate limiting is essential to prevent brute force attacks
- Email verification reduces fake/spam accounts significantly
- MFA dramatically improves security for high-value accounts
- Session timeout prevents unauthorized access from forgotten logouts
- Audit logs help investigate security incidents
- Social login increases conversion but adds OAuth complexity
- Password reset is common attack vector - secure it properly
- Account lockout needs balance (security vs user frustration)
- GDPR requires ability to export and delete user data
- Test authentication on multiple devices and browsers
- Have clear account recovery process
- Consider legal requirements (age verification, consent)
- Authentication errors should not leak information
