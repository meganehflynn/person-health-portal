# Agent 07: UI Design System
## Person Health - Component Library & Design Tokens

---

### Design Tokens

#### Spacing Scale
```
--space-1: 4px
--space-2: 8px
--space-3: 12px
--space-4: 16px
--space-5: 24px
--space-6: 32px
--space-7: 48px
--space-8: 64px
--space-9: 96px
--space-10: 128px
```

#### Typography Scale
```
--text-xs:   12px / 1.5
--text-sm:   14px / 1.5
--text-base: 16px / 1.6
--text-lg:   18px / 1.6
--text-xl:   20px / 1.5
--text-2xl:  24px / 1.3
--text-3xl:  30px / 1.3
--text-4xl:  36px / 1.2
--text-5xl:  48px / 1.1
--text-hero: 56px / 1.05
```

#### Border Radius
```
--radius-sm: 4px
--radius-md: 8px
--radius-lg: 12px
--radius-xl: 16px
--radius-full: 9999px
```

#### Shadows
```
--shadow-sm: 0 1px 2px rgba(0,0,0,0.05)
--shadow-md: 0 4px 6px rgba(0,0,0,0.07)
--shadow-lg: 0 10px 15px rgba(0,0,0,0.1)
--shadow-xl: 0 20px 25px rgba(0,0,0,0.1)
```

---

### Component Specifications

#### 1. Navigation Bar (Sticky)
- Height: 72px
- Background: White with subtle bottom border
- Logo: Left-aligned, max-height 40px
- Links: Center or right-aligned, 16px medium weight
- CTA Button: Pill shape, primary color, right-aligned
- Mobile: Hamburger menu at 768px breakpoint

#### 2. Hero Section
- Full viewport width, 80-90vh height
- Background: Abstract/nature image with gradient overlay
- Headline: text-hero, bold, white
- Subhead: text-xl, regular, white/80% opacity
- CTA Button: Large (56px height), white background, primary text
- Optional: Subtle animated particles or gradient shift

#### 3. Key Advantages (Icon Row)
- 5 items in a horizontal row (desktop)
- Each: 64px icon + label text below
- Grid: 5-column on desktop, 2+3 on tablet, 1-column on mobile
- Icons: Outlined style, primary brand color
- Labels: text-sm, center-aligned, 2 lines max

#### 4. Platform Card (Three Companies)
- 3-column layout (desktop)
- Each card: Logo/name + description + key stat
- Card style: White background, subtle shadow, rounded corners
- Hover: Slight elevation change

#### 5. Audience Section
- Tab or scroll-based (Investors | Hospitals | Vendors)
- Each section: Headline + 3-4 bullet points + CTA button
- Visual separator between sections
- CTA buttons: Outlined style, audience-specific color accent

#### 6. Contact Form (Segmented)
- 3 audience buttons at top (toggle/tab style)
- Form fields: Full-width, 48px height, rounded borders
- Labels: Above field, text-sm, medium weight
- Submit button: Full-width, primary color, 56px height
- Validation: Inline error messages, red accent

#### 7. Footer
- Dark background (brand dark color)
- 3-column layout: Logo+tagline | Navigation | Legal
- Text: White/70% opacity
- Bottom bar: Copyright

---

### Breakpoints

| Name | Width | Layout |
|------|-------|--------|
| Mobile | < 640px | Single column |
| Tablet | 640px - 1024px | 2-column grid |
| Desktop | 1024px - 1280px | Full layout |
| Wide | > 1280px | Max-width container (1200px) |

---

### Grid System

- Container max-width: 1200px
- Gutter: 24px (mobile 16px)
- Columns: 12-column grid
- Section padding: 96px vertical (mobile 64px)

---

### Iconography (Key Advantages Row)

| Concept | Icon Suggestion (Lucide) |
|---------|-------------------------|
| Multi-Modal | `grid-3x3` or `network` |
| Validation | `badge-check` or `shield-check` |
| IP Protection | `shield` or `lock` |
| Lab Infrastructure | `building-2` or `flask-conical` |
| Early Detection | `radar` or `activity` |
