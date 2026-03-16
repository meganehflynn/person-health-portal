# Agent 10: Interaction & Widget Design
## Person Health - Interaction Specifications & Micro-Interactions

---

### Page-Level Interactions

#### 1. Hero Section

**Background Effect:**
- Subtle gradient animation: slow color shift between brand primary shades (8s cycle)
- Optional: particle/node network animation suggesting data connections
- Image parallax on scroll (subtle, 10-15% offset)

**Text Entry:**
- Headline fades in + slides up (400ms, ease-out, 0ms delay)
- Subhead fades in + slides up (400ms, ease-out, 200ms delay)
- CTA button fades in + scales from 95% to 100% (300ms, ease-out, 400ms delay)

**Scroll Indicator:**
- Small animated chevron or line at bottom of hero
- Pulses every 3 seconds
- Disappears after first scroll

---

#### 2. Key Advantages (Icon Row)

**Scroll-Triggered Reveal:**
- Icons appear one by one, left to right
- Each icon: fade in + slide up (300ms, stagger 100ms between items)
- On hover (desktop): icon scales to 110%, subtle shadow appears

**Icon Animation (optional enhancement):**
- Grid icon: nodes connect briefly on reveal
- Checkmark: draws itself (SVG path animation)
- Shield: subtle pulse glow
- Building: builds up from base
- Radar: concentric rings ripple outward

---

#### 3. Platform Overview - Three Companies

**Card Reveal:**
- Cards fade in as group or stagger (200ms apart)
- On hover: card lifts (translateY -4px), shadow deepens
- Transition: 200ms ease

**Modalities Diagram:**
- Central hub (Person Health) with 4 connected nodes
- On scroll-into-view: lines draw from center to each modality (SVG path animation, 600ms)
- Each modality label fades in after its line completes
- Optional: subtle continuous pulse on connection lines suggesting data flow

---

#### 4. Audience Sections (Investors / Hospitals / Vendors)

**Implementation Option A: Scroll Sections**
- Each section fades in on scroll (IntersectionObserver, threshold 0.2)
- Content slides in from left or right (alternating)
- CTA button has a subtle shimmer/pulse after section fully visible (draw attention)

**Implementation Option B: Tab Interface**
- 3 tabs at top of section, sticky within section
- Tab switch: crossfade content (200ms)
- Active tab: underline slides to active position (300ms, spring easing)
- Content height animates smoothly (no layout jump)

**Recommendation:** Option A (scroll sections) for this audience. Investors and hospital admins expect full-page content, not hidden tabs.

---

#### 5. Contact Page - Audience Selector

**Three Buttons:**
- Layout: 3 equal-width buttons in a row
- Default state: outlined, brand color border
- Hover: fill transitions in (200ms)
- Selected state: fully filled, checkmark icon appears, other buttons dim slightly
- Transition between selections: color crossfade (200ms)

**Form Reveal:**
- After audience selection, form slides down (300ms, ease-out)
- Fields stagger in (100ms each)
- If switching audience type: form crossfades (no jarring jump)

**Form Field Interactions:**
- Focus: border color transitions to primary (150ms), subtle glow
- Filled state: label floats above field (or stays above if using top-label pattern)
- Validation error: field border turns red, error text slides in below (200ms)
- Submit button: loading state with spinner, disabled during submission

**Success State:**
- Form fades out, success message fades in
- Checkmark icon draws itself (SVG animation, 500ms)
- Confetti is NOT appropriate for this brand (too casual)
- Simple, clean confirmation with next-steps text

---

#### 6. Navigation

**Desktop:**
- Sticky header, appears on scroll-up, hides on scroll-down (smart hide)
- Background transitions from transparent (on hero) to white (on scroll)
- Transition: 300ms
- Active page indicator: underline slides to current item

**Mobile:**
- Hamburger icon: animates to X on open (200ms)
- Menu slides in from right (300ms, ease-out)
- Background overlay fades in
- Menu items stagger in (50ms each)
- CTA button at bottom of mobile menu

---

#### 7. Footer

- No special animations needed
- Links: color transition on hover (150ms)
- Subtle top border or gradient separator from content

---

### Global Interaction Patterns

| Pattern | Spec |
|---------|------|
| Scroll reveal | IntersectionObserver, threshold 0.15, fade+slide up 400ms |
| Button hover | Background darken 10%, translateY -1px, 150ms ease |
| Button active | translateY 0px, darken 15% |
| Link hover | Color transition, 150ms |
| Card hover | translateY -4px, shadow-lg, 200ms ease |
| Page transitions | Crossfade 200ms (Next.js app router) |
| Loading states | Skeleton screens (not spinners) for content |

---

### Performance Guidelines for Animations

- Use CSS transforms and opacity only (GPU-accelerated)
- No layout-triggering animations (no width/height/top/left)
- Respect `prefers-reduced-motion` media query (disable animations)
- Keep total animation JS < 10KB (Framer Motion tree-shaken)
- No animations on first contentful paint (defer to after load)

---

### Widget: Modalities Diagram (Key Interactive Element)

```
Layout Concept:

          [ Breath: VocxiHealth ]
                  |
                  |
[ Blood: Oncodea ] --- [ PERSON HEALTH OS ] --- [ AI: RealBusiness.AI ]
                  |
                  |
        [ Lab: Molecular Testing Labs ]

- Center node is larger, brand-colored
- Connecting lines animate on scroll-reveal
- Each outer node has an icon + label
- Hover on any node: highlights its connection line
- Mobile: vertical stack with connecting line down the center
```
