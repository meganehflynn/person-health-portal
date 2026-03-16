# Agent 08: Frontend Development Architecture
## Person Health - Project Structure & Implementation Plan

---

### Project Structure

```
person-health-site/
+-- src/
|   +-- app/
|   |   +-- layout.tsx          # Root layout (nav + footer)
|   |   +-- page.tsx            # Homepage
|   |   +-- about/
|   |   |   +-- page.tsx        # About Person Health
|   |   +-- resources/
|   |   |   +-- page.tsx        # Resources / Newsroom
|   |   +-- contact/
|   |       +-- page.tsx        # Segmented Contact Forms
|   |
|   +-- components/
|   |   +-- layout/
|   |   |   +-- Navbar.tsx
|   |   |   +-- Footer.tsx
|   |   |   +-- Container.tsx
|   |   |
|   |   +-- home/
|   |   |   +-- Hero.tsx
|   |   |   +-- KeyAdvantages.tsx
|   |   |   +-- PlatformOverview.tsx
|   |   |   +-- ModalitiesDiagram.tsx
|   |   |   +-- AudienceSection.tsx
|   |   |   +-- CTABar.tsx
|   |   |
|   |   +-- about/
|   |   |   +-- Mission.tsx
|   |   |   +-- Origins.tsx
|   |   |   +-- Team.tsx
|   |   |   +-- TrustedNetwork.tsx
|   |   |
|   |   +-- contact/
|   |   |   +-- AudienceSelector.tsx
|   |   |   +-- ContactForm.tsx
|   |   |
|   |   +-- ui/
|   |       +-- Button.tsx
|   |       +-- Card.tsx
|   |       +-- SectionHeading.tsx
|   |       +-- Icon.tsx
|   |       +-- Badge.tsx
|   |
|   +-- lib/
|   |   +-- constants.ts        # Brand copy, key phrases
|   |   +-- validation.ts       # Zod schemas for forms
|   |   +-- analytics.ts        # GA4 event helpers
|   |
|   +-- styles/
|       +-- globals.css         # Tailwind + CSS custom properties
|
+-- public/
|   +-- images/
|   |   +-- logo.svg
|   |   +-- hero-bg.jpg
|   |   +-- og-image.jpg
|   +-- fonts/
|
+-- tailwind.config.ts
+-- next.config.ts
+-- package.json
+-- tsconfig.json
```

---

### Key Implementation Notes

#### Server vs Client Components
- **Server Components (default):** All page layouts, static content sections, SEO metadata
- **Client Components:** Navbar mobile toggle, contact form, audience tab selector, scroll animations

#### Form Handling
```
Contact Form Flow:
1. User selects audience type (Investor / Hospital / Vendor)
2. Form renders with Zod-validated fields
3. On submit: POST to /api/contact
4. Server action validates + sends to Salesforce/email
5. Success state shown to user
6. GA4 event fired: form_submit with audience_type
```

#### Image Strategy
- Hero backgrounds: WebP format, srcset for responsive
- Logo: SVG (scalable, small file)
- Icons: Lucide React (tree-shaken, no extra downloads)
- OG Image: Pre-rendered 1200x630 branded card

#### Performance Budget
| Asset Type | Max Size |
|-----------|----------|
| JavaScript (total) | < 150KB gzipped |
| CSS (total) | < 30KB gzipped |
| Hero image | < 200KB (WebP) |
| Fonts | < 100KB (subset) |
| Total page weight | < 500KB first load |

---

### Tailwind Config (Key Customizations)

```typescript
// tailwind.config.ts (conceptual)
{
  theme: {
    extend: {
      colors: {
        brand: {
          primary: 'var(--color-primary)',    // Set by logo choice
          secondary: 'var(--color-secondary)',
          dark: 'var(--color-dark)',
          light: 'var(--color-light)',
          accent: '#05D16E',
        }
      },
      fontFamily: {
        sans: ['Inter', 'system-ui', 'sans-serif'],
        display: ['Plus Jakarta Sans', 'Inter', 'sans-serif'],
      },
      maxWidth: {
        site: '1200px',
      }
    }
  }
}
```

---

### API Routes

| Route | Method | Purpose |
|-------|--------|---------|
| `/api/contact` | POST | Form submission handler |

Form submissions will be validated server-side with Zod, then forwarded to the configured CRM (Salesforce Health Cloud) or sent via email as a fallback.
