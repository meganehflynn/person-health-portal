# Agent 09: Conversion Optimization
## Person Health - CRO Strategy & Lead Generation

---

### Conversion Goals

| Priority | Goal | Metric |
|----------|------|--------|
| Primary | Partnership discussion requests | Form submissions |
| Secondary | Investor material requests | Gated content downloads |
| Tertiary | White paper downloads | Lead capture |

---

### Conversion Architecture

The site has ONE primary objective: **drive qualified conversation requests** from three distinct audience segments (Investors, Research Hospitals, Vendors).

#### CTA Strategy (by placement)

| Location | CTA Text | Style | Target |
|----------|----------|-------|--------|
| Navbar (persistent) | Request a Discussion | Filled primary button | /contact |
| Hero section | Request Partnership Discussion | Large white button | /contact |
| Investor section | Contact Us for Investor Materials | Outlined button | /contact?type=investor |
| Hospital section | Request Clinical Partnership Discussion | Outlined button | /contact?type=hospital |
| Vendor section | Submit Vendor Inquiry | Outlined button | /contact?type=vendor |
| Page bottom (sticky on mobile) | Let's Talk | Filled primary button | /contact |
| About page bottom | Start a Conversation | Filled primary button | /contact |

#### CTA Placement Rules
- **Every scroll section** should have a CTA within viewport or within one scroll
- **Mobile**: Sticky bottom bar with CTA appears after scrolling past hero
- **Desktop**: Navbar CTA is always visible (sticky header)
- **No dead ends**: Every page ends with a CTA leading to /contact

---

### Form Optimization

#### Reduce Friction
- **Pre-select audience type** when arriving from a segment-specific CTA (use URL params)
- **Minimal required fields**: Name, Email, Organization (3 fields)
- **Optional fields**: Phone, Role, Message
- **No CAPTCHA** unless spam becomes an issue (use honeypot field instead)
- **Auto-focus** first field on page load

#### Build Trust at Point of Conversion
- Display near form: "We respond within 1 business day"
- Show clinical partner logos (Mayo, Cleveland Clinic, Baylor)
- Include: "Your information is kept confidential and is never shared"

#### Post-Submission
- Success message: "Thank you. A member of our team will reach out within one business day."
- Redirect to a "Thank You" page (enables GA4 conversion tracking)
- Trigger email confirmation to submitter

---

### Social Proof & Trust Signals

| Element | Placement | Content |
|---------|-----------|---------|
| Clinical partner logos | Below hero, near forms | Mayo Clinic, Cleveland Clinic, MD Anderson, Baylor |
| Patent count | Key Advantages row | "43+ patents" |
| Certification badges | Key Advantages row | "CLIA-certified, CAP-accredited" |
| Boston Scientific lineage | About page | Origin story |
| Capitol Hill meetings | News/Resources | Government engagement signals |

---

### Audience-Specific Conversion Paths

#### Investor Path
```
Homepage Hero → Scroll to "For Investors" → CTA → Contact (pre-selected "Investor")
                                                    → Thank You page → Email follow-up
```
**Key motivator:** Market opportunity ($40-75B TAM), competitive moat, clinical validation partners

#### Hospital Path
```
Homepage Hero → Key Advantages (validation, CLIA/CAP) → "For Hospitals" → CTA → Contact
                                                                                → Thank You
```
**Key motivator:** Early Access Program (3-5 pilot sites, 90 days), co-publication, new billable service lines

#### Vendor Path
```
Homepage Hero → Platform Overview → "For Vendors" → CTA → Contact → Thank You
```
**Key motivator:** Early entry into global market, long-term supply agreements, co-development with IP protection

---

### A/B Testing Roadmap (Post-Launch)

| Test | Hypothesis | Metric |
|------|-----------|--------|
| Hero CTA text: "Request a Discussion" vs "Learn More" | Direct CTA will outperform vague CTA | Click-through rate |
| Form length: 3 fields vs 6 fields | Fewer fields = higher completion | Form completion rate |
| Audience section: Tabs vs scroll sections | Scroll sections get more visibility | Section engagement |
| Trust logos placement: Above fold vs below | Above fold increases conversions | Form submissions |
