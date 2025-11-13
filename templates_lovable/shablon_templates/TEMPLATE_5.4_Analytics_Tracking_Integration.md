# TEMPLATE 5.4: ANALYTICS & TRACKING INTEGRATION

## 📋 PURPOSE
This template defines the complete analytics and tracking system including event tracking, user behavior analysis, conversion tracking, and integration with analytics platforms.

---

## 🎯 LOVABLE PROMPT TEMPLATE

```
Implement Analytics & Tracking System based on the following specification:

## ANALYTICS PLATFORMS

### Primary Analytics Platform

Platform: [Google Analytics 4 / Mixpanel / Amplitude / Plausible / Fathom / Custom]
Account ID: _______________ (from environment variable)
Measurement ID: _______________ (GA4) or API Key

Setup Method: [Script tag / NPM package / GTM / Custom]

Configuration:
- Anonymous IP: [Yes/No]
- Cookie Consent Required: [Yes/No]
- Session Timeout: _______________ minutes
- Custom Dimensions: _______________
- Custom Metrics: _______________

### Secondary Analytics Platforms

Platform 2: [Yes/No]
If Yes:
- Platform: _______________
- Purpose: _______________ (e.g., Product analytics, Heatmaps)
- Integration Method: _______________
- Configuration: _______________

Platform 3: [Yes/No]
[Repeat structure...]

### Event Tracking Platforms

Additional Tracking:

Segment/CDP:
- Enable: [Yes/No]
- Write Key: _______________ (from env)
- Destinations: _______________

Customer Data Platform:
- Platform: [Segment / mParticle / RudderStack / Custom]
- Purpose: Unified customer data
- Integration: _______________

---

## TRACKING STRATEGY

### Event Taxonomy

Event Naming Convention: [snake_case / camelCase / PascalCase / Custom]
Pattern: [verb_noun / feature_action / custom]

Examples:
- button_clicked
- form_submitted
- page_viewed
- user_signed_up
- product_purchased

Event Structure:
```javascript
{
  event: "event_name",
  properties: {
    category: "...",
    label: "...",
    value: "...",
    // custom properties
  },
  user_id: "...",
  timestamp: "..."
}
```

### Event Categories

Total Event Categories: _______________

Category 1: Page Views
- Purpose: Track page navigation
- Events:
  * page_view
  * screen_view (mobile)
  * [Other page events...]

Category 2: User Actions
- Purpose: Track user interactions
- Events:
  * button_click
  * link_click
  * scroll_depth
  * video_play
  * [Other user actions...]

Category 3: Forms
- Purpose: Track form interactions
- Events:
  * form_start
  * form_submit
  * form_error
  * form_success
  * form_abandon
  * [Other form events...]

Category 4: Authentication
- Purpose: Track auth flows
- Events:
  * signup_start
  * signup_complete
  * login_success
  * login_failure
  * logout
  * password_reset
  * [Other auth events...]

Category 5: E-commerce (if applicable)
- Purpose: Track purchases
- Events:
  * view_item
  * add_to_cart
  * begin_checkout
  * purchase
  * refund
  * [Other ecommerce events...]

Category 6: Engagement
- Purpose: Track user engagement
- Events:
  * feature_used
  * content_viewed
  * search_performed
  * filter_applied
  * [Other engagement events...]

[Continue for all categories...]

---

## CORE EVENTS CONFIGURATION

### Page View Tracking

Page View Event:
- Event Name: page_view
- Trigger: [Every page / SPA route change / Manual]
- Automatic: [Yes/No]

Page View Properties:
- [ ] Page URL
- [ ] Page Title
- [ ] Page Path
- [ ] Referrer
- [ ] UTM Parameters
- [ ] Language
- [ ] User ID (if authenticated)
- [ ] Session ID
- [ ] Device Type
- [ ] Browser
- [ ] Screen Resolution
- [ ] Timestamp
- [ ] Other: _______________

Virtual Page Views (SPA):
- Track Route Changes: [Yes/No]
- Method: [React Router listener / Manual / History API]
- Exclude Routes: _______________

### Button Click Tracking

Click Event:
- Event Name: button_click
- Track All Buttons: [Yes/No]
- Specific Buttons Only: [Yes/No]

If Specific:
Button 1:
- Button ID/Class: _______________
- Button Text: _______________
- Event Name: _______________ (specific event)
- Properties:
  * button_text: _______________
  * button_location: _______________
  * button_type: _______________
  * destination_url: _______________

Button 2:
[Repeat structure...]

[Continue for important buttons...]

CTA Buttons to Track:
- [ ] Signup button
- [ ] Login button
- [ ] Start trial button
- [ ] Request demo button
- [ ] Download button
- [ ] Contact us button
- [ ] Buy now button
- [ ] All primary CTAs
- [ ] Navigation links
- [ ] Social sharing buttons

### Link Click Tracking

Outbound Links:
- Track: [Yes/No]
- Event Name: outbound_link_click
- Properties:
  * destination_url
  * link_text
  * link_location

Internal Links:
- Track: [Yes/No]
- Event Name: internal_link_click

Download Links:
- Track: [Yes/No]
- Event Name: download_link_click
- Properties:
  * file_name
  * file_type
  * file_size

### Form Tracking

Form Events:

Form Start:
- Event Name: form_start
- Trigger: [First field focus]
- Properties:
  * form_id
  * form_name
  * form_location

Field Interaction:
- Event Name: field_focus / field_blur
- Track Individual Fields: [Yes/No]
- Properties:
  * form_id
  * field_name
  * field_type

Form Submit:
- Event Name: form_submit
- Trigger: [Submit button click]
- Properties:
  * form_id
  * form_name
  * submission_time
  * field_count

Form Success:
- Event Name: form_success
- Properties:
  * form_id
  * response_time

Form Error:
- Event Name: form_error
- Properties:
  * form_id
  * error_type
  * error_field

Form Abandon:
- Event Name: form_abandon
- Trigger: [Leave page / Close tab]
- Properties:
  * form_id
  * fields_completed
  * abandonment_point

### Scroll Tracking

Scroll Depth:
- Track: [Yes/No]
- Event Name: scroll_depth
- Intervals: [25%, 50%, 75%, 100%]
- Fire Once Per Session: [Yes/No]
- Properties:
  * page_url
  * scroll_depth

Scroll to Element:
- Track Specific Elements: [Yes/No]
- Elements:
  * Element 1: _______________
  * Element 2: _______________
  * [Continue...]

### Video Tracking

Video Events:
- Platform: [YouTube / Vimeo / Native HTML5]

Events to Track:
- [ ] video_start
- [ ] video_play
- [ ] video_pause
- [ ] video_complete
- [ ] video_progress (25%, 50%, 75%)
- [ ] video_seek

Properties:
- video_id
- video_title
- video_duration
- current_time
- percent_watched

### Search Tracking

Site Search:
- Track: [Yes/No]
- Event Name: search_performed
- Properties:
  * search_query
  * search_location
  * results_count
  * result_clicked (if applicable)

Search Refinement:
- Track Filters: [Yes/No]
- Event Name: filter_applied
- Properties:
  * filter_type
  * filter_value

### Error Tracking

JavaScript Errors:
- Track: [Yes/No]
- Event Name: javascript_error
- Properties:
  * error_message
  * error_stack
  * page_url
  * user_agent

404 Errors:
- Track: [Yes/No]
- Event Name: page_not_found
- Properties:
  * requested_url
  * referrer

API Errors:
- Track: [Yes/No]
- Event Name: api_error
- Properties:
  * endpoint
  * status_code
  * error_message

### User Engagement

Session Duration:
- Track: [Automatic in GA4]
- Custom Logic: [Yes/No]

Time on Page:
- Track: [Yes/No]
- Method: [Visibility API / Heartbeat / Exit]

Active/Idle Time:
- Distinguish: [Yes/No]
- Idle Threshold: _______________ seconds

Feature Usage:
Feature 1:
- Feature Name: _______________
- Event Name: feature_used
- Properties:
  * feature_name
  * usage_count
  * context

[Repeat for key features...]

---

## CONVERSION TRACKING

### Conversion Goals

Total Conversion Goals: _______________

Goal 1: _______________
- Goal Name: _______________
- Goal Type: [Sign up / Purchase / Download / Form submission / Custom]
- Event Name: _______________
- Value: $_______________ (if monetary)
- Properties:
  * conversion_type
  * conversion_value
  * [Additional properties...]

Goal 2: _______________
[Repeat structure...]

Goal 3: _______________
[Repeat structure...]

[Continue for all goals...]

### Funnel Tracking

Conversion Funnels:

Funnel 1: Signup Funnel
- Funnel Name: _______________
- Steps:
  1. Landing page view
  2. Signup page view
  3. Form start
  4. Form submit
  5. Email verification
  6. Onboarding complete
- Drop-off Tracking: [Yes/No]

Funnel 2: Purchase Funnel (if e-commerce)
- Steps:
  1. Product view
  2. Add to cart
  3. Checkout initiated
  4. Payment info entered
  5. Purchase complete
- Drop-off Tracking: [Yes/No]

Funnel 3: Custom Funnel
[Define steps...]

### E-commerce Tracking (if applicable)

E-commerce Events:

Enable Enhanced Ecommerce: [Yes/No]

Standard Events:
- [ ] view_item
- [ ] view_item_list
- [ ] add_to_cart
- [ ] remove_from_cart
- [ ] begin_checkout
- [ ] add_payment_info
- [ ] purchase
- [ ] refund

Product Properties:
- item_id
- item_name
- item_brand
- item_category
- price
- quantity
- currency
- discount
- [Other properties...]

Transaction Properties:
- transaction_id
- value
- currency
- tax
- shipping
- affiliation
- coupon
- [Other properties...]

---

## USER IDENTIFICATION

### User ID Tracking

User Identification:
- Enable: [Yes/No]
- User ID Type: [Database ID / UUID / Email hash / Custom]
- Set User ID On: [Login / Signup / Both]

User ID Properties:
```javascript
{
  user_id: "...",
  user_properties: {
    account_type: "...",
    signup_date: "...",
    plan: "...",
    language: "...",
    [other properties...]
  }
}
```

Anonymous Users:
- Track: [Yes/No]
- Anonymous ID: [Auto-generated / Cookie-based]

### User Properties

Standard User Properties:
- [ ] user_id
- [ ] email (hashed)
- [ ] signup_date
- [ ] account_type
- [ ] subscription_plan
- [ ] user_role
- [ ] language_preference
- [ ] country
- [ ] company_size
- [ ] industry
- [ ] lifetime_value
- [ ] last_login_date
- [ ] login_count

Custom User Properties:
Property 1: _______________
Property 2: _______________
Property 3: _______________
[Continue...]

Update Frequency:
- On Every Event: [Yes/No]
- On User Property Change: [Yes/No]
- Once Per Session: [Yes/No]

---

## SESSION TRACKING

Session Configuration:

Session Timeout: _______________ minutes
Session ID: [Auto-generated / Custom]

Session Properties:
- [ ] session_id
- [ ] session_start_time
- [ ] session_duration
- [ ] pages_viewed_per_session
- [ ] events_per_session
- [ ] referrer
- [ ] utm_source
- [ ] utm_medium
- [ ] utm_campaign
- [ ] device_type
- [ ] browser
- [ ] operating_system

Cross-Domain Tracking:
- Enable: [Yes/No]
- Domains: _______________

---

## UTM PARAMETER TRACKING

UTM Parameters:

Track UTM Parameters: [Yes/No]

Standard Parameters:
- [ ] utm_source
- [ ] utm_medium
- [ ] utm_campaign
- [ ] utm_term
- [ ] utm_content

Custom Parameters:
- [ ] Other: _______________

Storage:
- Store in: [Cookie / Local storage / Session storage]
- Duration: _______________ days
- Attribution: [First touch / Last touch / Multi-touch]

Attribution Window:
- Direct: _______________ days
- Organic: _______________ days
- Paid: _______________ days

---

## CUSTOM EVENTS

### Product-Specific Events

Total Custom Events: _______________

Custom Event 1: _______________
- Event Name: _______________
- Description: _______________
- Trigger: _______________
- Properties:
  * property_1: _______________
  * property_2: _______________
  * [Continue...]

Custom Event 2: _______________
[Repeat structure...]

Custom Event 3: _______________
[Repeat structure...]

[Continue for all custom events...]

---

## ANALYTICS IMPLEMENTATION

### Implementation Method

Implementation: [Google Tag Manager / Direct Script / React SDK / Custom]

If GTM:
- Container ID: _______________ (from env)
- Data Layer: [Standard / Custom]
- Triggers: _______________
- Tags: _______________

If Direct Script:
- Script Location: [<head> / <body> / Async]
- Loading Strategy: [Async / Defer / Blocking]

If React SDK:
- Package: _______________
- Initialization: [App.js / _app.js / Custom]
- Provider: [Context / Redux / Custom]

### Event Tracking Code Structure

Event Helper Function:
```javascript
const trackEvent = (eventName, properties = {}) => {
  // GA4
  if (window.gtag) {
    gtag('event', eventName, properties);
  }
  
  // Mixpanel
  if (window.mixpanel) {
    mixpanel.track(eventName, properties);
  }
  
  // Segment
  if (window.analytics) {
    analytics.track(eventName, properties);
  }
  
  // Custom
  // ...
};
```

React Hook Example:
```javascript
const useAnalytics = () => {
  const trackEvent = (eventName, properties) => {
    // implementation
  };
  
  const trackPageView = (url) => {
    // implementation
  };
  
  return { trackEvent, trackPageView };
};
```

---

## PRIVACY & COMPLIANCE

### Cookie Consent

Cookie Consent Required: [Yes/No]

If Yes:
- Consent Management Platform: [OneTrust / Cookiebot / Custom]
- Consent Types:
  * Strictly Necessary: [Always allowed]
  * Analytics: [User choice]
  * Marketing: [User choice]
  * Personalization: [User choice]

Consent Banner:
- Position: [Bottom / Top / Modal]
- Options: [Accept all / Reject all / Customize]
- Granular Control: [Yes/No]

Tracking Before Consent:
- Allow: [No - wait for consent]
- Anonymous Tracking: [Yes/No]

### GDPR Compliance

GDPR Features:
- [ ] Cookie consent banner
- [ ] Opt-out mechanism
- [ ] IP anonymization
- [ ] Data retention limits
- [ ] Right to be forgotten
- [ ] Data export
- [ ] Consent logging

IP Anonymization:
- Enable: [Yes/No]
- Method: [Last octet / Server-side]

### Data Retention

Data Retention Policies:

Analytics Data:
- Retention Period: _______________ months
- Auto-delete: [Yes/No]

User Data:
- Active Users: _______________ retention
- Inactive Users: Delete after _______________ months

Event Data:
- Raw Events: _______________ months
- Aggregated Reports: _______________ years

---

## DEBUGGING & QA

### Debug Mode

Debug Mode: [Yes/No]

Enable Debug:
- Environment: [Development only / Query parameter / Admin users]
- Console Logging: [Yes/No]
- Event Validation: [Yes/No]

Debug Output:
- Log All Events: [Yes/No]
- Log Event Properties: [Yes/No]
- Log User Properties: [Yes/No]
- Highlight Errors: [Yes/No]

### Testing

Testing Strategy:

- [ ] Test in development environment
- [ ] Use debug mode
- [ ] Verify events in Real-Time reports
- [ ] Check event properties
- [ ] Test conversion tracking
- [ ] Test cross-domain tracking
- [ ] Test on multiple devices
- [ ] Test with ad blockers
- [ ] Test consent management

GA4 Debug View:
- Enable: [Yes/No]
- Access: _______________

---

## PERFORMANCE OPTIMIZATION

Performance Considerations:

Script Loading:
- Async Loading: [Yes/No]
- Defer Loading: [Yes/No]
- Load Priority: [High / Low]

Event Batching:
- Batch Events: [Yes/No]
- Batch Size: _______________ events
- Flush Interval: _______________ ms

Sampling:
- Enable Sampling: [Yes/No]
- Sample Rate: _______________% (e.g., 100% = all users)

Impact on Performance:
- Page Load Impact: < 100ms
- Bundle Size: < 50KB
- No Blocking: [Async only]

---

## ANALYTICS DASHBOARDS & REPORTS

### Standard Reports

Reports to Monitor:

- [ ] Real-time users
- [ ] Daily active users
- [ ] Traffic sources
- [ ] Top pages
- [ ] Conversion funnel
- [ ] User demographics
- [ ] Device breakdown
- [ ] Browser breakdown
- [ ] Geographic distribution
- [ ] User retention
- [ ] Custom events

### Custom Reports

Custom Report 1:
- Report Name: _______________
- Metrics: _______________
- Dimensions: _______________
- Filters: _______________
- Frequency: _______________

Custom Report 2:
[Repeat structure...]

### Alerts

Alert 1:
- Alert Name: _______________
- Condition: _______________
- Threshold: _______________
- Notification: [Email / Slack / Other]
- Recipients: _______________

Alert 2:
[Repeat structure...]

---

## INTEGRATION WITH OTHER TOOLS

### Marketing Automation

Platform: [HubSpot / Marketo / ActiveCampaign / Other]
Integration: [API / Native]
Data Synced:
- [ ] User properties
- [ ] Events
- [ ] Conversions
- [ ] Page views

### CRM Integration

Platform: [Salesforce / HubSpot / Pipedrive / Other]
Integration: _______________
Data Synced:
- [ ] Lead source
- [ ] User behavior
- [ ] Conversion events
- [ ] Engagement scores

### Heatmap & Session Recording

Platform: [Hotjar / FullStory / LogRocket / Clarity / Other]
Enable: [Yes/No]
Sampling Rate: _______________%
Privacy: [Mask sensitive data]

### A/B Testing

Platform: [Google Optimize / Optimizely / VWO / Custom]
Enable: [Yes/No]
Integration with Analytics: [Yes/No]
Track Variants: [Yes/No]

---

## ANALYTICS TEAM & ACCESS

Team Access:

Admin Access:
- Users: _______________
- Permissions: Full access

Analyst Access:
- Users: _______________
- Permissions: View reports

Developer Access:
- Users: _______________
- Permissions: Implementation, debug

---

## DOCUMENTATION

Analytics Documentation:

- [ ] Event tracking sheet (all events documented)
- [ ] Implementation guide
- [ ] Naming conventions
- [ ] Testing procedures
- [ ] Dashboard access
- [ ] Report definitions
- [ ] Privacy policies
- [ ] Changelog

Event Tracking Sheet:
- Format: [Google Sheets / Notion / Confluence]
- Location: _______________
- Maintained By: _______________

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
Implement Analytics & Tracking System based on the completed specification.

CONTEXT: I have defined a comprehensive analytics system with event tracking, user identification, conversion goals, and privacy compliance.

TASK:
1. Set up Google Analytics 4 (or chosen platform)
2. Implement page view tracking (SPA route changes)
3. Create event tracking helper functions
4. Track button clicks on all CTAs
5. Implement form tracking (start, submit, error, success)
6. Set up conversion goal tracking
7. Add user identification for logged-in users
8. Implement UTM parameter tracking
9. Add cookie consent management
10. Create debug mode for testing

GUIDELINES:
- Async script loading (don't block page load)
- Privacy-compliant (GDPR, CCPA)
- Cookie consent before tracking
- IP anonymization enabled
- Debug mode for development
- Track meaningful events only (avoid noise)
- Consistent event naming convention
- Document all tracked events

CONSTRAINTS:
- Script must load asynchronously
- No tracking before cookie consent (GDPR)
- Performance impact < 100ms
- Bundle size < 50KB
- Work with ad blockers (graceful degradation)
- No PII in event properties
- GDPR data retention limits

[Paste your filled analytics template here]

EXPECTED DELIVERABLES:
1. Working Google Analytics 4 integration
2. Page view tracking (SPA)
3. Event tracking helper functions
4. CTA button click tracking
5. Form interaction tracking
6. Conversion goal setup
7. User identification system
8. Cookie consent banner
9. Debug mode
10. Analytics documentation
```

---

## 📝 USAGE INSTRUCTIONS

1. **Start simple** - track page views and key conversions first
2. **Event naming** - consistent, descriptive convention
3. **Privacy first** - cookie consent, IP anonymization
4. **Test thoroughly** - use debug mode, verify in real-time
5. **Document everything** - event tracking sheet essential
6. **Monitor performance** - async loading, minimal impact
7. **Segment users** - authenticated vs anonymous
8. **Track funnels** - identify drop-off points

---

## 💡 BEST PRACTICES

- Load analytics scripts asynchronously to avoid blocking page load
- Use consistent event naming convention (snake_case or camelCase)
- Track user intent, not just clicks (why did they click?)
- Set up conversion funnels to identify drop-off points
- Use user properties to segment and personalize
- Implement server-side tracking for critical events
- Respect privacy - IP anonymization, cookie consent
- Track errors to improve user experience
- Use UTM parameters consistently in marketing campaigns
- Set up automated alerts for anomalies
- Review analytics weekly, not just monthly
- A/B test based on data, not assumptions
- Track both quantity and quality of engagement
- Use cohort analysis to understand retention
- Document all events in a tracking sheet

---

## ⚠️ CRITICAL REMINDERS

- Analytics must comply with GDPR/CCPA - cookie consent required
- Never track PII (personally identifiable information) in events
- IP anonymization required in many jurisdictions
- Script loading must not block page rendering
- Test with ad blockers enabled (many users block analytics)
- Cookie consent must be obtained BEFORE tracking (EU law)
- Data retention policies must be implemented (GDPR)
- Track meaningful events only - too many events = noise
- Event properties should be consistent and documented
- User ID tracking requires explicit consent
- Cross-domain tracking needs proper configuration
- UTM parameters are case-sensitive
- GA4 has different data model than Universal Analytics
- Debug mode essential for testing - don't skip
- Analytics documentation prevents confusion later
- Review analytics regularly to catch implementation errors
- Sampling may be needed for high-traffic sites
- Consider server-side tracking for better accuracy
