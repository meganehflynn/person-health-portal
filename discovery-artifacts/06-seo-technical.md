# Agent 06: SEO & Technical Marketing
## Person Health - SEO Strategy & Technical Implementation

---

### Target Keyword Strategy

#### Primary Keywords (Homepage)

| Keyword | Intent | Search Volume Est. | Difficulty |
|---------|--------|-------------------|------------|
| multi-modal diagnostics platform | Informational | Low-Med | Low |
| early disease detection AI | Informational | Medium | Medium |
| breath diagnostics cancer | Research | Medium | Low |
| liquid biopsy early detection | Research | Medium | Medium |
| health intelligence platform | Commercial | Low | Low |

#### Secondary Keywords (Subpages)

| Page | Target Keywords |
|------|----------------|
| About | multi-modal health OS, breath blood AI diagnostics, Person Health |
| Resources | early detection white paper, multi-cancer screening research |
| Contact | Person Health partnership, diagnostic platform investment |

---

### On-Page SEO Specifications

#### Homepage
- **Title Tag:** Person Health | Multi-Modal AI Platform for Early Disease Detection
- **Meta Description:** Person Health integrates breath diagnostics, blood molecular testing, and AI-driven intelligence to detect disease before symptoms appear. Request a partnership discussion.
- **H1:** Detect Disease Before Symptoms. Understand Health for Life.
- **H2s:** Three Companies One Health OS | For Investors | For Research Hospitals | For Vendors

#### About Page
- **Title Tag:** About Person Health | Building Infrastructure for Early Understanding
- **Meta Description:** Born from the integration of three companies - VocxiHealth, Oncodea, and Molecular Testing Labs - Person Health is building the infrastructure for lifelong health stewardship.

#### Resources Page
- **Title Tag:** Resources & News | Person Health Publications and Research
- **Meta Description:** Explore Person Health's clinical publications, white papers on multi-modal diagnostics, and the latest company news and partnership announcements.

#### Contact Page
- **Title Tag:** Contact Person Health | Partnership & Investment Inquiries
- **Meta Description:** Connect with Person Health for investor materials, clinical partnership discussions, or vendor integration opportunities.

---

### Technical SEO Checklist

- [ ] XML Sitemap auto-generated (Next.js)
- [ ] robots.txt configured (allow all public pages)
- [ ] Canonical URLs on all pages
- [ ] Open Graph tags (title, description, image) per page
- [ ] Twitter Card meta tags
- [ ] JSON-LD structured data:
  - Organization schema (name, logo, founders, description)
  - MedicalOrganization schema
  - ContactPage schema
  - BreadcrumbList schema
- [ ] 301 redirects configured if migrating from existing domain
- [ ] Image alt text on all images
- [ ] Lazy loading for below-fold images
- [ ] Preconnect to third-party origins (fonts, analytics)
- [ ] Core Web Vitals optimized (LCP < 2.5s, CLS < 0.1, INP < 200ms)

---

### Link Building Strategy (Post-Launch)

1. **Clinical partner co-mentions** - Mayo Clinic, Baylor press releases
2. **Conference coverage** - AACR, ASH, ASCO abstract mentions
3. **Healthcare industry directories** - MedTech Innovator, BioSpace
4. **Thought leadership** - LinkedIn articles from leadership team
5. **Capitol Hill meeting PR** - Press around March 2026 Washington DC meetings

---

### Analytics & Tracking Plan

| Event | Trigger | Goal |
|-------|---------|------|
| `cta_click_investor` | Click "I'm an Investor" | Lead generation |
| `cta_click_hospital` | Click "I'm a Health System" | Lead generation |
| `cta_click_vendor` | Click "I'm a Vendor/Partner" | Lead generation |
| `form_submit` | Contact form submitted | Conversion |
| `hero_cta_click` | "Request Partnership Discussion" click | Engagement |
| `whitepaper_click` | White paper download/view | Content engagement |
| `scroll_depth` | 25%, 50%, 75%, 100% | Page engagement |
| `time_on_page` | 30s, 60s, 120s | Content quality signal |
