# Plan: GuT Mayoral Candidate Landing Page

## Concept & Vision

A **cheerful, optimistic, and welcoming** landing page for a mayoral candidate affiliated with the "GuT" voter group. The design evokes **sunshine, community warmth, and progressive energy** — feeling like a breath of fresh air rather than typical political propaganda. Think "European civic engagement meets modern editorial design." The predominantly bright/light base with yellow and blue as intentional accent colors creates a sense of optimism and accessibility.

## Design Language

### Aesthetic Direction
**"Warm Civic Optimism"** — A bright, editorial-inspired design with playful geometric accents. Not corporate or sterile, but warm and approachable like a community gathering space. Slight retro influences mixed with modern clarity.

### Color Palette
- **Background**: Warm off-white `#FFFBF5` (cream white)
- **Primary Accent**: Sunny Yellow `#F5C518` (mustard-inspired optimism)
- **Secondary Accent**: Municipal Blue `#1E5FA8` (trustworthy, civic)
- **Text Primary**: Deep Charcoal `#2D2A26`
- **Text Secondary**: Warm Gray `#6B6560`
- **Highlight/CTA**: Golden Yellow `#FFD700` → gradient to `#F5C518`

### Typography
- **Display/Headlines**: "Fraunces" (Google Font) — a soft serif with character and warmth
- **Body/Navigation**: "DM Sans" (Google Font) — clean, friendly, highly legible
- **Fallback**: Georgia, system-ui

### Spatial System
- Base unit: 8px
- Section padding: 80px vertical (desktop), 48px (mobile)
- Container max-width: 1200px
- Generous whitespace to let content breathe

### Motion Philosophy
- **Page load**: Staggered fade-up entrance (elements reveal sequentially with 100ms delays)
- **Scroll interactions**: Subtle parallax on hero, elements fade in on scroll-into-view
- **Hover states**: Gentle scale (1.02-1.05) with color transitions, 200ms ease-out
- **Navigation**: Smooth scroll to sections
- **Decorative elements**: Floating/breathing ambient motion on geometric shapes

### Visual Assets
- Abstract geometric patterns (circles, waves) in yellow/blue as decorative accents
- Wave/curve dividers between sections
- Soft drop shadows for depth
- Possibly abstract blob shapes or gradient meshes

## Layout & Structure

### Navigation (Fixed Top)
- Transparent → slightly frosted on scroll
- Logo/candidate name on left
- Menu items: "About Me" | "My Positions" (smooth scroll anchors)
- Right side: Legal Notice | Privacy Policy links (smaller, muted)

### Hero Section
- Large headline with candidate name
- Tagline referencing GuT voter group
- Abstract geometric background pattern (yellow/blue)
- Primary CTA button to learn more
- Asymmetric layout with decorative elements

### About Me Section
- Photo placeholder area (stylized geometric frame)
- Biography text with personal story
- Key accomplishments or credentials
- Warm, personal tone

### My Positions Section
- Card-based layout for different policy areas
- Each card: icon, title, brief description
- Grid of 3-4 position cards
- Clean, scannable format

### Footer
- Contact information
- Social links (placeholder)
- Copyright and legal links repeated
- Wave/curve transition from content

## Features & Interactions

### Navigation
- Smooth scroll to sections on click
- Active state highlights current section
- Mobile: hamburger menu with slide-out drawer

### Hero CTA
- Hover: scale up + shadow increase
- Click: smooth scroll to About Me

### Position Cards
- Hover: lift effect (translateY -4px + shadow)
- Subtle background color shift

### Legal/Privacy Links
- Footer links open in same tab (anchor pages)

## Component Inventory

1. **Header/Navigation Bar** — Fixed, semi-transparent, responsive
2. **Hero Banner** — Full-width, asymmetric, with decorative shapes
3. **Section Divider** — Wave/curve SVG or CSS
4. **About Card** — Photo + bio text layout
5. **Position Card** — Icon + title + description, hover states
6. **Footer** — Multi-column layout with links
7. **Decorative Elements** — Floating circles/blobs, gradient meshes

## Technical Approach

- **Single HTML file** with embedded CSS and minimal JS
- **CSS Custom Properties** for theming
- **Vanilla JavaScript** for:
  - Smooth scroll navigation
  - Scroll-triggered animations (IntersectionObserver)
  - Mobile menu toggle
- **Google Fonts**: Fraunces + DM Sans via CDN
- **Responsive**: Mobile-first, breakpoints at 768px and 1024px
- **No build step required** — runs directly in browser

## File Structure

```
gut-bm-website/
├── index.html          (main landing page)
├── legal-notice.html   (legal notice page)
├── privacy-policy.html (privacy policy page)
└── .kilo/
    └── plans/
        └── [this plan file]
```