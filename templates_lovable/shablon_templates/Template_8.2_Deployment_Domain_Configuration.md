# TEMPLATE 8.2: DEPLOYMENT & DOMAIN CONFIGURATION

## 📋 PURPOSE
This template guides the deployment process from Lovable.dev to production with custom domain configuration.

---

## 🎯 DEPLOYMENT SPECIFICATION

```
Execute Deployment Process based on the following configuration:

## PRE-DEPLOYMENT CHECKLIST

### Environment Preparation
- [ ] Production environment URL: _______________
- [ ] Staging environment URL (if applicable): _______________
- [ ] Development environment URL: _______________

- [ ] Environment variables configured:
      Variable: _______________
      Value: [Set/Not Set]
      Variable: _______________
      Value: [Set/Not Set]
      [List all environment variables]

- [ ] API keys secured:
      Service: _______________
      Key configured: [Yes/No]
      [List all API keys]

- [ ] Database ready:
      Type: Supabase PostgreSQL
      URL: _______________
      Connection tested: [Yes/No]

- [ ] CDN configured (if applicable):
      Provider: _______________
      Status: [Active/Inactive]

### Code Preparation
- [ ] All changes committed to GitHub
      Branch: _______________
      Last commit: _______________
      Status: [Clean/Uncommitted changes]

- [ ] GitHub integration connected
      Repository: _______________
      Connected: [Yes/No]

- [ ] Production branch ready:
      Branch name: _______________ (typically 'main' or 'production')
      Merged from: _______________
      Status: [Ready/Not Ready]

- [ ] Version tagged:
      Version: _______________
      Tag format: [v1.0.0/1.0.0/Other]

- [ ] Build settings verified:
      Build command: _______________
      Output directory: _______________
      Node version: _______________

### Content Finalization
- [ ] All content proofread:
      Proofread by: _______________
      Date: _______________

- [ ] All images optimized:
      Tool used: _______________
      Average savings: ___%

- [ ] All translations complete:
      Languages: _______________
      Completion: 100%

- [ ] No placeholder content:
      Verified: [Yes/No]

- [ ] Legal pages updated:
      Privacy Policy: [Updated/Not Updated]
      Terms of Service: [Updated/Not Updated]
      Cookie Policy: [Updated/Not Updated]

## DOMAIN CONFIGURATION

### Domain Information
Primary Domain: _______________
WWW Version: www._______________
Preferred Version: [Non-WWW/WWW/Both]

Additional Domains (if any):
- Secondary Domain: _______________
- Regional Domains: _______________

Language-Specific Domains (if applicable):
- Language: _______________ → Domain: _______________
- Language: _______________ → Domain: _______________

### Domain Registrar
Registrar: _______________
Account Email: _______________
Account Owner: _______________
Renewal Date: _______________
Auto-Renewal: [Yes/No]

### DNS Configuration
DNS Provider: _______________
Access: [Have access/Need access]
Account Email: _______________

TTL Settings: _______________ seconds (Recommended: 300 for deployment, 3600 after)

### SSL Certificate
Provider: [Let's Encrypt/Custom/Other]
Type: [Free/Paid/Wildcard]
Coverage: [Single domain/Multi-domain/Wildcard]
Auto-renewal: [Yes/No]
Expiry Date: _______________

## LOVABLE.DEV DEPLOYMENT

### Initial Deployment
- [ ] Lovable project ready:
      Project name: _______________
      Project URL: _______________

- [ ] Deploy to Lovable subdomain first:
      URL: https://_______________. lovable.app
      Status: [Deployed/Not deployed]

- [ ] Test on Lovable subdomain:
      All functionality working: [Yes/No]
      All pages accessible: [Yes/No]
      Forms submitting: [Yes/No]
      Images loading: [Yes/No]

### Deployment Method
Choose deployment platform: [Select One]
- [ ] Netlify (Recommended for Lovable)
- [ ] Vercel
- [ ] GitHub Pages (Static only)
- [ ] Custom hosting

## NETLIFY DEPLOYMENT (RECOMMENDED)

### Netlify Account Setup
- [ ] Netlify account created:
      Email: _______________
      Team: _______________

- [ ] Connect to GitHub:
      Repository linked: [Yes/No]
      Branch: _______________

### Netlify Build Configuration
Build Command: _______________
(Default Lovable: `npm run build` or `vite build`)

Publish Directory: _______________
(Default Lovable: `dist`)

Environment Variables:
Variable: VITE_SUPABASE_URL
Value: _______________

Variable: VITE_SUPABASE_ANON_KEY
Value: _______________

[Add all other environment variables]

### Netlify Domain Configuration
- [ ] Add custom domain in Netlify:
      Dashboard → Domain Settings → Add Custom Domain
      Domain: _______________
      Status: [Pending/Active]

- [ ] Netlify provides DNS instructions:
      A Record: _______________
      AAAA Record: _______________
      OR CNAME: _______________

- [ ] SSL certificate provisioning:
      Status: [Provisioning/Active/Failed]
      HTTPS enabled: [Yes/No]
      Force HTTPS: [Yes/No]

### Netlify DNS Configuration (Option 1: Use Netlify DNS)
- [ ] Transfer DNS to Netlify:
      Nameservers provided: _______________
      Updated at registrar: [Yes/No]
      Propagation status: [Pending/Complete]

### External DNS Configuration (Option 2: Keep existing DNS)
Configure at your DNS provider: _______________

For Root Domain (example.com):
- [ ] A Record:
      Type: A
      Name: @ (or blank)
      Value: 75.2.60.5 (Netlify's load balancer)
      TTL: 300

- [ ] AAAA Record (IPv6):
      Type: AAAA
      Name: @ (or blank)
      Value: 2600:1f18:2148:bc00:9d31:0d30:bce9:2bd4
      TTL: 300

For WWW Subdomain (www.example.com):
- [ ] CNAME Record:
      Type: CNAME
      Name: www
      Value: [your-site].netlify.app
      TTL: 300

### DNS Record Verification
Tool: [dig/nslookup/DNS checker]
- [ ] A record resolves: _______________
      Command: `dig example.com +short`
      Result: _______________

- [ ] AAAA record resolves: _______________
      Command: `dig example.com AAAA +short`
      Result: _______________

- [ ] CNAME record resolves: _______________
      Command: `dig www.example.com +short`
      Result: _______________

### DNS Propagation
- [ ] Check propagation status:
      Tool: whatsmydns.net
      Status: [Propagating/Complete]
      Time elapsed: _______________ hours

- [ ] Test from multiple locations:
      Location 1: _______________
      Location 2: _______________
      Location 3: _______________

Propagation Time: Usually 0-48 hours
Expedite by setting low TTL before changes (300 seconds)

## VERCEL DEPLOYMENT (ALTERNATIVE)

### Vercel Setup
- [ ] Vercel account created:
      Email: _______________

- [ ] Import project from GitHub:
      Repository: _______________
      Branch: _______________

- [ ] Configure build:
      Framework Preset: Vite
      Build Command: `npm run build`
      Output Directory: `dist`

- [ ] Add environment variables:
      [Same as Netlify section]

### Vercel Domain Configuration
- [ ] Add domain in Vercel:
      Dashboard → Domains → Add
      Domain: _______________

- [ ] Configure DNS:
      Provided by Vercel: _______________

For Root Domain:
- [ ] A Record: 76.76.21.21

For WWW:
- [ ] CNAME: cname.vercel-dns.com

## MULTI-LANGUAGE DOMAIN ROUTING

### Subdirectory Routing (/en/, /uk/, /es/)
- [ ] URL rewrite rules configured:
      Default language redirects: _______________
      Language detection: _______________

- [ ] Test all language URLs:
      /en/ → [Working/Not Working]
      /uk/ → [Working/Not Working]
      /es/ → [Working/Not Working]

### Subdomain Routing (en.domain.com)
- [ ] DNS records for subdomains:
      Subdomain: en._______________
      CNAME: _______________
      
      Subdomain: uk._______________
      CNAME: _______________

- [ ] SSL certificates for subdomains:
      Wildcard certificate: [Yes/No]
      Individual certificates: [Yes/No]

- [ ] Test subdomain access:
      en.domain.com → [Working/Not Working]
      uk.domain.com → [Working/Not Working]

## REDIRECT CONFIGURATION

### WWW to Non-WWW (or vice versa)
Preference: [WWW/Non-WWW]

Netlify Configuration (_redirects file or netlify.toml):
```
https://www.example.com/* https://example.com/:splat 301!
```

- [ ] Redirect configured: [Yes/No]
- [ ] Redirect tested: [Yes/No]

### HTTP to HTTPS
- [ ] Force HTTPS enabled:
      Netlify: Automatic
      Vercel: Automatic
      Custom: [Configuration needed]

- [ ] Test HTTP redirect:
      http://domain.com → https://domain.com
      Status: [Working/Not Working]

### Old URLs to New URLs (if applicable)
- [ ] Redirect map created:
      Old URL: _______________ → New URL: _______________
      [List all redirects]

- [ ] 301 redirects implemented:
      File: _redirects (Netlify) or vercel.json (Vercel)
      Tested: [Yes/No]

## SUPABASE CONFIGURATION FOR PRODUCTION

### Production Database
- [ ] Supabase project for production:
      Project name: _______________
      Region: _______________
      URL: _______________

- [ ] Database migrated:
      Schema applied: [Yes/No]
      Data imported: [Yes/No]

- [ ] Connection strings updated:
      VITE_SUPABASE_URL: _______________
      VITE_SUPABASE_ANON_KEY: _______________

### Supabase Authentication
- [ ] Email settings configured:
      SMTP provider: _______________
      From address: _______________
      Templates customized: [Yes/No]

- [ ] OAuth providers configured:
      Google: [Yes/No]
      GitHub: [Yes/No]
      Facebook: [Yes/No]
      Other: _______________

- [ ] Redirect URLs updated:
      Production URLs added: [Yes/No]
      Localhost removed: [Yes/No]

### Supabase Security
- [ ] Row Level Security (RLS) enabled:
      All tables: [Yes/No]
      Policies tested: [Yes/No]

- [ ] API keys secured:
      Service role key: [Secure storage]
      Public anon key: [In env variables]

- [ ] Database backups enabled:
      Frequency: _______________
      Retention: _______________

## ENVIRONMENT VARIABLES

### Production Environment Variables
Location: [Netlify/Vercel Dashboard → Settings → Environment Variables]

Required Variables:
- [ ] VITE_SUPABASE_URL=_______________
- [ ] VITE_SUPABASE_ANON_KEY=_______________
- [ ] VITE_ANALYTICS_ID=_______________
- [ ] VITE_STRIPE_PUBLIC_KEY=_______________ (if applicable)
- [ ] [Other custom variables]: _______________

Verification:
- [ ] All variables set: [Yes/No]
- [ ] Rebuild after variable changes: [Yes/No]

## EMAIL CONFIGURATION

### Transactional Email Service
Provider: [Supabase/SendGrid/AWS SES/Other]
- [ ] Account setup: [Yes/No]
- [ ] API key configured: [Yes/No]
- [ ] From address verified: [Yes/No]
- [ ] Templates uploaded: [Yes/No]

### Email Templates
- [ ] Welcome email: [Configured/Not Configured]
- [ ] Password reset: [Configured/Not Configured]
- [ ] Email verification: [Configured/Not Configured]
- [ ] Notification emails: [Configured/Not Configured]

### Email Deliverability
- [ ] SPF record set:
      DNS record: _______________

- [ ] DKIM configured:
      DNS record: _______________

- [ ] DMARC policy:
      DNS record: _______________

- [ ] Test email delivery:
      Inbox: [Yes/No]
      Spam folder: [Yes/No]

## ANALYTICS & MONITORING

### Google Analytics 4
- [ ] GA4 property created:
      Property ID: _______________
      Data stream: _______________

- [ ] Tracking code installed:
      Method: [gtag.js/Environment variable]
      Verified: [Yes/No]

- [ ] Goals configured:
      Goal 1: _______________
      Goal 2: _______________
      Goal 3: _______________

- [ ] Test tracking:
      Real-time report: [Events showing/Not showing]

### Google Search Console
- [ ] Property added:
      Property URL: _______________
      Verification method: [DNS/HTML file/Meta tag]
      Status: [Verified/Not Verified]

- [ ] Sitemap submitted:
      URL: https://domain.com/sitemap.xml
      Status: [Submitted/Not Submitted]

- [ ] Ownership verified for all domains:
      domain.com: [Verified/Not Verified]
      www.domain.com: [Verified/Not Verified]

### Uptime Monitoring
Service: [UptimeRobot/Pingdom/StatusCake/Other]
- [ ] Account created: [Yes/No]
- [ ] Monitors configured:
      URL: _______________
      Interval: _______________
      Alert contacts: _______________

### Error Tracking
Service: [Sentry/Rollbar/Bugsnag/Other]
- [ ] Project created: [Yes/No]
- [ ] SDK installed: [Yes/No]
- [ ] Source maps uploaded: [Yes/No]
- [ ] Test error sent: [Yes/No]

### Performance Monitoring
Service: [New Relic/Datadog/Other]
- [ ] Integration active: [Yes/No]

## DEPLOYMENT EXECUTION

### Final Pre-Deploy Steps
- [ ] Backup staging/current site: [Yes/No]
- [ ] Team notified of deployment: [Yes/No]
- [ ] Maintenance mode ready (if needed): [Yes/No]
- [ ] Rollback plan documented: [Yes/No]

### Deploy Process
1. [ ] Trigger deployment:
      Method: [Git push/Manual trigger/CI/CD]
      Branch: _______________
      Commit: _______________

2. [ ] Monitor build:
      Build status: [Success/Failed]
      Build time: _______________ minutes
      Build logs reviewed: [Yes/No]

3. [ ] Build artifacts:
      Size: _______________ MB
      Optimization: [Pass/Fail]

4. [ ] Deployment completion:
      Time: _______________
      Status: [Success/Failed]
      Live URL: _______________

### Post-Deploy Verification
- [ ] Homepage loads: [Yes/No]
- [ ] All pages accessible: [Yes/No]
- [ ] Navigation works: [Yes/No]
- [ ] Forms submit: [Yes/No]
- [ ] Authentication works: [Yes/No]
- [ ] Database connections: [Yes/No]
- [ ] Images load: [Yes/No]
- [ ] Analytics firing: [Yes/No]
- [ ] SSL certificate active: [Yes/No]
- [ ] No console errors: [Yes/No]

### Multi-Language Verification
- [ ] All language versions accessible:
      /en/ → [Yes/No]
      /uk/ → [Yes/No]
      /es/ → [Yes/No]

- [ ] Language switcher works: [Yes/No]
- [ ] Content displays correctly: [Yes/No]
- [ ] URLs follow pattern: [Yes/No]

## ROLLBACK PLAN

### If Deployment Fails
Immediate Actions:
1. [ ] Note error messages: _______________
2. [ ] Check build logs: _______________
3. [ ] Verify environment variables: [Yes/No]
4. [ ] Test API connections: [Yes/No]

Rollback Steps:
1. [ ] Revert to previous deployment:
      Method: [Git revert/Platform rollback]
      Previous version: _______________

2. [ ] Verify rollback successful:
      Site accessible: [Yes/No]
      Functionality restored: [Yes/No]

3. [ ] Investigate issue:
      Root cause: _______________
      Fix applied: _______________

4. [ ] Re-attempt deployment:
      New attempt: _______________

## POST-DEPLOYMENT TASKS

### Immediate (Within 1 hour)
- [ ] Test critical user flows:
      Homepage → Signup: [Working/Not Working]
      Homepage → Pricing → Trial: [Working/Not Working]

- [ ] Monitor error rates:
      Error tracking dashboard: _______________
      Errors detected: _______________

- [ ] Check performance:
      Load times acceptable: [Yes/No]
      Core Web Vitals: [Pass/Fail]

- [ ] Verify analytics:
      Events logging: [Yes/No]

### Within 24 Hours
- [ ] Monitor uptime:
      Downtime incidents: _______________

- [ ] Review user feedback:
      Support tickets: _______________
      User reports: _______________

- [ ] Check email delivery:
      Emails sending: [Yes/No]
      Delivery rate: ___%

- [ ] SEO verification:
      Google indexing: [Started/Not started]
      Search Console errors: _______________

### Within 1 Week
- [ ] Full regression testing:
      All features working: [Yes/No]

- [ ] Performance monitoring:
      Average load time: _______________
      Optimization needed: [Yes/No]

- [ ] SEO monitoring:
      Pages indexed: _______________
      Rankings check: _______________

- [ ] User analytics review:
      Traffic volume: _______________
      Bounce rate: ___%
      Conversion rate: ___%

## DOCUMENTATION

### Deployment Documentation
- [ ] Document deployment process: [Yes/No]
- [ ] Save configuration settings: [Yes/No]
- [ ] Update team wiki: [Yes/No]
- [ ] Create runbook: [Yes/No]

### Access & Credentials
- [ ] Document stored securely:
      Netlify/Vercel: _______________
      Domain registrar: _______________
      DNS provider: _______________
      Supabase: _______________
      Analytics: _______________
      Monitoring: _______________

### Handoff (if applicable)
- [ ] Client/team trained: [Yes/No]
- [ ] Access transferred: [Yes/No]
- [ ] Documentation provided: [Yes/No]
- [ ] Support plan in place: [Yes/No]

## SIGN-OFF

Deployment Completed By: _______________
Date: _______________
Time: _______________

Deployment Status: [Success/Failed/Partial]

Issues Encountered:
_______________________________________________

Resolution:
_______________________________________________

Live Site URL: _______________

Stakeholder Approval: _______________
Date: _______________
```

---

## ✅ USAGE INSTRUCTIONS

1. **Complete pre-deployment checklist** thoroughly
2. **Test on Lovable subdomain** before custom domain
3. **Set low TTL** before DNS changes (300s)
4. **Deploy during low-traffic hours** if possible
5. **Have rollback plan ready** before deployment
6. **Monitor actively** for first 24 hours post-launch

---

## ⚠️ CRITICAL REMINDERS

- DNS propagation takes 0-48 hours globally
- Always test on staging before production
- Keep old site accessible during propagation
- Document all credentials securely
- Monitor error rates closely post-deployment
- Have emergency rollback plan ready
- Budget time for DNS propagation
- Test from multiple locations/devices after deployment
