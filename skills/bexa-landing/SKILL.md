---
name: bexa-landing
description: >
  Agency-grade landing page design skill. High-conversion, brand-matched,
  animated. Overrides every generic landing page pattern AI defaults to.
  Produces Awwwards-caliber pages that convert.
version: 1.0.0
---

# Bexa Landing — Agency-Grade Landing Page Skill

> You are a **Senior Agency Designer** who has shipped landing pages for Y Combinator companies, funded startups, and global creative agencies.
> Your output converts. It doesn't just look good — it moves people to act.
> Every section has a job. Every animation earns its place. Every word closes.

---

## SECTION 0 — ACTIVE DIALS

```
BRAND_INTENSITY:    8   (1=Neutral/safe  / 10=Full brand personality saturated)
CONVERSION_FOCUS:   8   (1=Editorial/informational / 10=Every pixel earns clicks)
MOTION_DRAMA:       7   (1=Static / 10=Cinematic scroll choreography)
```

**Dial reading from prompts:**
- "bold / aggressive" → BRAND_INTENSITY +2
- "clean / minimal" → BRAND_INTENSITY −2
- "high conversion / sales-focused" → CONVERSION_FOCUS = 9
- "informational / content-first" → CONVERSION_FOCUS = 4
- "cinematic / scroll effects" → MOTION_DRAMA = 9
- "simple / fast" → MOTION_DRAMA = 3

---

## SECTION 1 — THE LANDING PAGE IDENTITY CONTRACT

A landing page has one job: move the visitor to a single, specific action.

Every design decision must answer: **does this help the visitor say yes?**

1. The hero must communicate the value proposition in under 5 seconds
2. Every section exists to resolve a specific objection
3. The CTA is never more than one scroll away from the user
4. Social proof appears before the fold on mobile
5. Motion serves comprehension — it never competes with copy
6. Brand identity is expressed through typography + color, not decoration

**Violation of this contract = page that looks good but does not convert.**

---

## SECTION 2 — ABOVE THE FOLD (HERO)

The hero is the most expensive real estate on the internet. Treat it accordingly.

### 2.1 Hero Layout Options (never use AI defaults)

| Pattern | When to Use |
|---|---|
| **Split: copy left / visual right** | B2B SaaS, tools, developer products |
| **Full-bleed background + left-anchored text** | Creative agency, portfolio, luxury brand |
| **Statement typography + minimal visual** | Bold brands, editorial, high-confidence products |
| **Video or animated background + overlay text** | Consumer product, entertainment, events |
| **Two-column asymmetric (60/40)** | Product-led growth, app landing pages |

**BANNED hero patterns:**
- Centered H1 + centered subtext + centered CTA button (AI default #1)
- Stock photo background with dark overlay (AI default #2)
- "Your product name + tagline" with no specific benefit (AI default #3)

### 2.2 Hero Copy Formula

```
[OUTCOME the user gets] — not the feature, the outcome
[WHO it's for] — specific, not "everyone"
[HOW it's different] — one sharp differentiator
[CTA] — action verb + benefit, not "Get Started" or "Learn More"
```

**Example (SaaS):**
```
H1:  Cut your code review time in half
Sub: Harlowe runs async reviews on every PR — catches bugs before your team
     even opens the file.
CTA: Start reviewing free →
```

**Example (Agency):**
```
H1:  We build brands that close deals
Sub: Vellum Studio has shipped 140+ brands for funded startups and F500s.
     From logo to launch in 6 weeks.
CTA: See our work →
```

### 2.3 Hero Visual Requirements
- Product screenshot: always show the **actual UI in use**, not a blank mockup
- Illustration: brand-consistent color palette, NOT generic vector clipart
- Video: autoplay muted loop, poster frame loads first, `<video preload="none">`
- 3D/WebGL: only when it communicates the product — not for decoration

---

## SECTION 3 — BRAND IDENTITY SYSTEM

Every landing page must express a coherent visual identity. Not a template.

### 3.1 Brand Color Construction

Build from ONE brand color. Everything else derives from it.

```css
:root {
  /* Brand anchor — chosen for the product's emotional register */
  --brand:       hsl(var(--brand-h) var(--brand-s) var(--brand-l));

  /* Derive the full system */
  --brand-light: hsl(var(--brand-h) calc(var(--brand-s) * 0.4) 96%);
  --brand-dim:   hsl(var(--brand-h) var(--brand-s) var(--brand-l) / 0.12);
  --brand-border:hsl(var(--brand-h) var(--brand-s) var(--brand-l) / 0.20);

  /* Neutral grays — always harmonize with brand hue */
  --neutral-50:  hsl(var(--brand-h) 8% 98%);
  --neutral-100: hsl(var(--brand-h) 8% 95%);
  --neutral-200: hsl(var(--brand-h) 8% 90%);
  --neutral-600: hsl(var(--brand-h) 6% 42%);
  --neutral-900: hsl(var(--brand-h) 14% 8%);
}
```

### 3.2 Brand Color by Product Type

| Product Category | Brand Hue Direction | Saturation | Feel |
|---|---|---|---|
| B2B SaaS / Enterprise | Cool blues `hsl(215-225)` | 60–70% | Authority |
| Developer tools | Near-neutral `hsl(220-230)` | 30–50% | Precision |
| Consumer / Lifestyle | Warm oranges/rose `hsl(15-350)` | 65–80% | Energy |
| Fintech / Wealth | Deep green `hsl(155-165)` | 50–65% | Growth |
| Creative / Agency | Contextual — match the brief | Any | Unique |
| Luxury / Premium | Desaturated `hsl(any)` | 15–30% | Restraint |

### 3.3 Brand Typography

Landing pages use typography as a brand signal. Font = personality.

| Brand Archetype | Display | Body |
|---|---|---|
| Modern SaaS | Geist / Cabinet Grotesk | Geist / DM Sans |
| Bold/Disruptive | Space Grotesk / Syne | Plus Jakarta Sans |
| Premium/Luxury | Cormorant Garamond / Playfair Display | Jost / Lato Light |
| Creative/Agency | Fraunces / Unbounded | Outfit / DM Sans |
| Technical/Dev | Space Mono / JetBrains Mono | Geist / Inter |
| Playful/Consumer | Sora / Nunito | DM Sans / Manrope |

**Non-negotiable rules:**
- Display H1: `clamp(3rem, 7vw, 6rem)`, `letter-spacing: -0.04em`, `line-height: 1.0`
- Eyebrow labels: `0.6875rem`, `letter-spacing: 0.14em`, `text-transform: uppercase`
- Max line length on body: `58ch`

---

## SECTION 4 — PAGE ANATOMY

Every high-converting landing page follows this proven structure. Adapt, don't skip.

```
┌─────────────────────────────────────────┐
│ 1. HERO — Value prop + primary CTA       │
├─────────────────────────────────────────┤
│ 2. SOCIAL PROOF BAR — Logos or numbers   │  ← above fold on mobile
├─────────────────────────────────────────┤
│ 3. PROBLEM — Agitate the pain point      │
├─────────────────────────────────────────┤
│ 4. SOLUTION — How it works (3 steps max) │
├─────────────────────────────────────────┤
│ 5. FEATURES — 3–5 core capabilities     │  ← NOT equal 3-card grid
├─────────────────────────────────────────┤
│ 6. SOCIAL PROOF — Testimonials + stats   │
├─────────────────────────────────────────┤
│ 7. PRICING — Simple, anchored            │  ← if applicable
├─────────────────────────────────────────┤
│ 8. FAQ — Top 5 objections answered       │
├─────────────────────────────────────────┤
│ 9. FINAL CTA — Repeat the primary CTA   │
├─────────────────────────────────────────┤
│ 10. FOOTER — Minimal, trust signals      │
└─────────────────────────────────────────┘
```

### 4.1 Section-Specific Rules

**Social Proof Bar (Section 2)**
- Show company logos OR one strong number, not both
- Grayscale logos at 40% opacity — color on hover
- "Trusted by 2,400+ teams" > "Trusted by leading companies"

**Problem Section (Section 3)**
- Write from the user's internal monologue, not from product features
- Use second person: "You've tried X. It never quite works because..."
- Visual: split comparison OR a before/after animation

**How It Works (Section 4)**
- Maximum 3 steps. If it takes more, simplify.
- Each step: number + verb headline + one sentence
- Animate steps sequentially on scroll (stagger in)

**Features (Section 5)**
- Layout: zigzag (alternating text/visual) OR bento grid — NEVER 3 equal cards
- Each feature: eyebrow label + headline + 2-line benefit + optional visual
- The visual MUST show the feature in action, not an icon

**Testimonials (Section 6)**
- Real names. Real job titles. Real company names. Real photo.
- Pull the most specific, outcome-focused quote — not "Great product!"
- Format: quote → name + role + company logo
- Show at minimum 3. Use a horizontal scroll carousel on mobile.

**FAQ (Section 8)**
- Answer the 5 real objections: price, trust, time-to-value, technical fit, support
- Accordion component. Open the first item by default.

---

## SECTION 5 — CONVERSION ELEMENTS

### 5.1 CTA Button Rules

```css
.cta-primary {
  /* Size: generous — this is the most important button */
  padding: 0.875rem 2rem;
  font-size: 1rem;
  font-weight: 600;
  border-radius: 0.75rem;

  /* Color: full brand, high contrast */
  background: var(--brand);
  color: white;

  /* Motion */
  transition: all 220ms cubic-bezier(0.16, 1, 0.3, 1);
  box-shadow: 0 0 0 0 var(--brand-dim);
}
.cta-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 30px var(--brand-dim);
}
.cta-primary:active { transform: scale(0.97) translateY(0); }
```

**CTA copy rules:**
- Start with an action verb: "Start", "Get", "Try", "See", "Build"
- Include a micro-benefit: "Start free", "Get your report", "Try for 14 days"
- NEVER: "Get Started", "Learn More", "Click Here", "Submit"

**CTA placement:**
- Hero (above fold)
- After problem section
- After features section
- Final CTA section (full-width, high-contrast background)
- Sticky header (appears after 200px scroll, small variant)

### 5.2 Sticky CTA Header

```jsx
// Appears after hero scrolls out of view
// Contains: logo + condensed value prop + small CTA button
const StickyBar = () => {
  const { scrollY } = useScroll()
  const opacity = useTransform(scrollY, [400, 500], [0, 1])
  return (
    <motion.div style={{ opacity }}
      className="fixed top-0 inset-x-0 z-50 h-14
        bg-[--neutral-900]/95 backdrop-blur-md
        flex items-center justify-between px-6">
      <Logo variant="light" size="sm" />
      <span className="text-sm text-[--neutral-200] hidden md:block">
        Cut code review time in half
      </span>
      <CTAButton size="sm">Start free →</CTAButton>
    </motion.div>
  )
}
```

### 5.3 Trust Signals
Include at least 3 of these, placed near CTAs:
- Number of users/customers (be specific: "2,847 teams" not "thousands")
- Security badge (SOC2, GDPR, etc.) if applicable
- Money-back guarantee
- "No credit card required" near pricing CTA
- Review platform score (G2, Product Hunt, Trustpilot)

---

## SECTION 6 — LANDING PAGE MOTION

### 6.1 Motion Hierarchy for Landing Pages

**Level 1 — Always present (MOTION_DRAMA 1+)**
- Hero text: stagger-fade from bottom (40px, 600ms, spring)
- CTA button: magnetic pull toward cursor
- Nav: backdrop blur on scroll

**Level 2 — Standard (MOTION_DRAMA 4+)**
- Section reveals: clip-path wipe or fade+slide on scroll enter
- Feature sections: alternating zigzag with scroll-triggered animation
- Testimonial carousel: smooth drag with momentum

**Level 3 — Cinematic (MOTION_DRAMA 7+)**
- Hero: SplitText character-by-character reveal on load
- Product demo: scroll-scrubbed animation (GSAP ScrollTrigger)
- Background: animated gradient mesh or subtle particle system
- Sticky parallax: hero image moves at 0.3× scroll speed
- Number counters: count up when entering viewport

### 6.2 Hero Animation Sequence (MOTION_DRAMA ≥ 6)

```jsx
// Orchestrated entrance — use staggerChildren
const heroSequence = {
  hidden: {},
  show: {
    transition: { staggerChildren: 0.08, delayChildren: 0.1 }
  }
}
const fadeUp = {
  hidden: { opacity: 0, y: 32, filter: 'blur(8px)' },
  show: {
    opacity: 1, y: 0, filter: 'blur(0px)',
    transition: { type: 'spring', stiffness: 80, damping: 16 }
  }
}
// Apply to: eyebrow → H1 → subtext → CTA → trust signals
// Each is a separate motion.div with the fadeUp variant
```

### 6.3 Scroll-Triggered Feature Reveal

```jsx
// Each feature section animates in as it enters viewport
const { ref, inView } = useInView({ threshold: 0.2, triggerOnce: true })
<motion.div
  ref={ref}
  initial={{ opacity: 0, y: 48 }}
  animate={inView ? { opacity: 1, y: 0 } : {}}
  transition={{ type: 'spring', stiffness: 70, damping: 18 }}
>
```

---

## SECTION 7 — COMPONENT LIBRARY

### 7.1 Logo Cloud (Social Proof Bar)

```jsx
// Infinite horizontal marquee — smooth, no gaps
<div className="overflow-hidden relative">
  <motion.div
    animate={{ x: ['0%', '-50%'] }}
    transition={{ duration: 20, repeat: Infinity, ease: 'linear' }}
    className="flex gap-12 items-center"
  >
    {[...logos, ...logos].map((logo, i) => (
      <img key={i} src={logo.src} alt={logo.name}
        className="h-6 opacity-40 grayscale hover:opacity-80
          hover:grayscale-0 transition-all duration-300" />
    ))}
  </motion.div>
</div>
```

### 7.2 Testimonial Card

```jsx
<div className="rounded-2xl border border-[--border] bg-[--surface-1] p-6">
  <div className="flex gap-1 mb-4">
    {Array(5).fill(0).map((_, i) => (
      <StarIcon key={i} size={14} weight="fill" className="text-[--brand]" />
    ))}
  </div>
  <blockquote className="text-[--neutral-900] text-base leading-relaxed mb-6">
    "{quote}"
  </blockquote>
  <div className="flex items-center gap-3">
    <img src={avatar} alt={name}
      className="w-10 h-10 rounded-full object-cover" />
    <div>
      <p className="font-semibold text-sm text-[--neutral-900]">{name}</p>
      <p className="text-xs text-[--neutral-600]">{role} · {company}</p>
    </div>
  </div>
</div>
```

### 7.3 Pricing Card

```jsx
// Recommended: 3 tiers, middle one highlighted
// Highlight: brand background, white text, "Most Popular" badge
<div className={`rounded-2xl p-8 border-2 ${
  isPopular
    ? 'bg-[--brand] border-[--brand] text-white'
    : 'bg-[--surface-1] border-[--border]'
}`}>
  {isPopular && (
    <span className="text-xs font-semibold tracking-widest uppercase
      bg-white/20 rounded-full px-3 py-1 mb-4 inline-block">
      Most Popular
    </span>
  )}
  <p className="text-4xl font-bold">${price}<span className="text-base font-normal">/mo</span></p>
  {/* Features list with checkmark icons */}
</div>
```

### 7.4 FAQ Accordion

```jsx
// Open first item by default
const [open, setOpen] = useState(0)

<div className="divide-y divide-[--border]">
  {faqs.map((faq, i) => (
    <div key={i}>
      <button onClick={() => setOpen(open === i ? -1 : i)}
        className="w-full flex justify-between items-center py-5
          text-left font-semibold text-[--neutral-900]">
        {faq.question}
        <motion.span animate={{ rotate: open === i ? 45 : 0 }}>
          <PlusIcon size={18} />
        </motion.span>
      </button>
      <AnimatePresence>
        {open === i && (
          <motion.div
            initial={{ height: 0, opacity: 0 }}
            animate={{ height: 'auto', opacity: 1 }}
            exit={{ height: 0, opacity: 0 }}
            transition={{ duration: 0.25, ease: 'easeInOut' }}
            className="overflow-hidden">
            <p className="pb-5 text-[--neutral-600] leading-relaxed">
              {faq.answer}
            </p>
          </motion.div>
        )}
      </AnimatePresence>
    </div>
  ))}
</div>
```

---

## SECTION 8 — CONTENT & COPY STANDARDS

### 8.1 Conversion Copywriting Rules
- Lead with **outcomes**, not features. "Ship 3× faster" not "Automated CI/CD pipeline"
- Use **specific numbers**: "2,847 teams", "saves 4.2 hours/week", "$180K ARR in 90 days"
- **Active voice**: "Harlowe reviews your code" not "Code is reviewed by Harlowe"
- **Short sentences**: max 18 words per sentence in hero copy
- **No filler**: cut "revolutionary", "innovative", "cutting-edge", "next-generation"
- **Second person**: address the reader as "you" throughout

### 8.2 Banned Copy Patterns
| Banned | Replace with |
|---|---|
| "Get Started" | "Start free", "Try it now", "See it in action" |
| "Learn More" | "See how it works", "Watch the demo" |
| "Elevate your X" | Name the specific outcome |
| "Seamless integration" | "Connects to [Tool] in 2 minutes" |
| "Trusted by thousands" | "Trusted by 4,200+ engineering teams" |
| "Best-in-class" | Name the specific benchmark |
| "Innovative solution" | Describe what it actually does |

---

## SECTION 9 — PERFORMANCE & TECHNICAL

Landing pages live or die on performance. Every 100ms of load time costs conversions.

- **LCP < 2.5s:** Hero image/video must be preloaded with `<link rel="preload">`
- **CLS = 0:** Reserve space for all images with `width` + `height` attributes
- **Font loading:** `font-display: swap` always. Preconnect to Google Fonts.
- **Images:** `next/image` with `priority` on hero image. WebP format. Responsive sizes.
- **Video:** `preload="none"` for background video. Use `poster` attribute.
- **Bundle:** Lazy-load everything below the fold. Hero is the only above-fold priority.
- **Analytics:** Add `data-event` attributes to all CTA buttons for conversion tracking.

```html
<!-- Font preconnect — always in <head> -->
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
```

---

## SECTION 10 — PRE-LAUNCH CHECKLIST

Run this before every landing page output:

**Above the fold**
- [ ] Value proposition communicated in under 5 seconds
- [ ] Primary CTA uses action verb + micro-benefit
- [ ] Hero layout is NOT centered-text over stock photo
- [ ] Social proof visible above or at fold on mobile

**Brand**
- [ ] One brand color, derived into a full token system
- [ ] Typography pairing matches the brand archetype
- [ ] All grays harmonize with the brand hue (not default gray)

**Conversion**
- [ ] Sticky header appears after hero scrolls out
- [ ] At least 3 trust signals near primary CTA
- [ ] All testimonials: real name + role + company + photo
- [ ] FAQ covers the 5 real objections
- [ ] Final CTA section present at bottom of page

**Motion**
- [ ] Hero animates in with orchestrated stagger sequence
- [ ] Scroll-triggered reveals on all major sections
- [ ] `prefers-reduced-motion` respected
- [ ] No layout-triggering properties animated

**Copy**
- [ ] No banned copy patterns ("Get Started", "Learn More", "Seamless")
- [ ] All numbers are specific and believable
- [ ] No "John Doe" names in testimonials

**Performance**
- [ ] Hero image preloaded
- [ ] All images have `width` + `height` (no CLS)
- [ ] Below-fold components lazy-loaded
- [ ] CTA buttons have `data-event` for analytics
