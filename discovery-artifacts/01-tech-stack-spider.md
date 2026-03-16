# Agent 01: Tech Stack Spider
## Person Health Microsite - Technology Recommendation

---

### Recommended Stack

| Layer | Technology | Rationale |
|-------|-----------|-----------|
| Framework | Next.js 14 (App Router) | SSR for SEO, fast loads, React ecosystem |
| Language | TypeScript | Type safety for medical/regulated content |
| Styling | Tailwind CSS + CSS Variables | Rapid prototyping, design token support |
| CMS | Sanity.io (Headless) | Structured content, HIPAA-aware, real-time preview |
| Forms | React Hook Form + Zod | Validation for segmented contact forms |
| Email/CRM | HubSpot or Salesforce Health Cloud API | Per appendix: Salesforce Health Cloud planned |
| Hosting | Vercel | Edge deployment, instant rollbacks, analytics |
| Analytics | Google Analytics 4 + Hotjar | Traffic + heatmaps for conversion tracking |
| Animations | Framer Motion | Smooth scroll, icon row transitions |
| Icons | Lucide React | Clean medical/tech icon library |

### Performance Targets

- Lighthouse Score: 95+ across all categories
- First Contentful Paint: < 1.2s
- Largest Contentful Paint: < 2.5s
- Cumulative Layout Shift: < 0.1
- Time to Interactive: < 3.5s

### Security & Compliance Considerations

- HTTPS enforced (Vercel default)
- CSP headers configured
- No PHI collected via contact forms (name, email, org only)
- GDPR cookie consent banner (international audience noted in deck)
- Form submissions encrypted in transit
- No client-side storage of sensitive data

### Third-Party Integrations

1. **Salesforce Health Cloud** - CRM for lead routing (investor vs. hospital vs. vendor)
2. **Calendly or HubSpot Meetings** - For "Request Partnership Discussion" CTA
3. **Google Tag Manager** - Event tracking without code deploys
4. **Cloudinary** - Image optimization for logo assets and hero imagery

### Domain & DNS

- Primary domain: `personhealth.com` (or `.health` TLD for brand alignment)
- SSL: Auto-provisioned via Vercel
- CDN: Vercel Edge Network (global)

### Development Environment

- Node.js 20 LTS
- pnpm for package management
- ESLint + Prettier for code quality
- Husky pre-commit hooks
