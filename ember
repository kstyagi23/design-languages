# EMBER — UI Design Language Document
### A Complete Design System for Dark-Native, Orange-Accented Product Interfaces

> *"Everything that does not serve clarity must disappear. Everything that remains must earn its presence."*

---

## 1. Purpose of the Document

### What This Document Is For

This document defines the **complete visual and interaction language** for product interfaces built under the VOID/EMBER design system — a dark-native, high-contrast UI language built around restraint, precision, and a single dominant accent.

It exists to:
- Eliminate design ambiguity across multi-screen, multi-product surfaces
- Ensure visual and behavioral consistency from the first pixel to the last interaction
- Give engineers, designers, and AI systems a single source of truth to build from
- Preserve the emotional intent of the design as the product scales

### Who Should Use It

| Role | Usage |
|------|-------|
| Product Designers | Component design, screen composition, spacing, hierarchy |
| Frontend Engineers | Token consumption, component states, interaction behavior |
| AI/Agentic Systems | Generating UI consistent with this language |
| Product Managers | Evaluating whether proposed UI decisions align with system intent |

### What This Document Standardizes

- Color, typography, spacing, elevation, and motion foundations
- Component definitions, variants, and states
- Interaction language and gesture vocabulary
- Emotional intent per screen type and state
- Copy tone and system communication patterns

### What It Does NOT Cover

- Backend logic or API contracts
- Platform-specific native component libraries (UIKit, Jetpack Compose) unless overriding them
- Marketing, landing pages, or brand identity outside of product UI
- Content strategy or information architecture beyond component-level copy

---

## 2. Product Context

### What These Products Do

The VOID/EMBER language is built for **high-utility mobile-first applications** — products where the user is *doing something*, not just reading. The reference products across which this language is extracted include:

- Temporal/calendar tools (date awareness, schedule density)
- Mobility and ride/logistics apps (spatial, action-heavy)
- Smart device ecosystems (IoT, real-time status, control surfaces)
- Activity tracking and performance monitoring

What unites them: **dense information presented cleanly**, with **action at the center** of every screen.

### Target Users

- Digitally fluent, mobile-native users aged 18–40
- Users operating with divided attention (in motion, multitasking)
- Power users who want control without clutter
- Users who associate dark UI with premium, focused experience

### Usage Environments

- Mobile-first (iOS and Android primary targets)
- Low-ambient-light conditions: vehicles, evenings, outdoor use
- One-thumb reachable interaction zones expected
- Performance environments: outdoors, active use, glance-and-act

### Key User Goals

1. Get information instantly, without parsing visual noise
2. Take action with minimal steps
3. Trust the system to be accurate and responsive
4. Feel in control of a smart, capable product

### Constraints

- Dark OLED screens demand true blacks and careful layering to avoid grayness
- High-motion use requires typography legibility at glance-speed
- Single-accent-color constraint is a deliberate philosophical choice, not a limitation
- Touch target minimums must be respected at all times (44px minimum)

---

## 3. Design Philosophy

### Core Philosophy Statement

> **"One background. One accent. Zero compromise."**

The interface disappears. Only the content, the action, and the moment remain. Dark is not a mood — it is a substrate. Orange is not decoration — it is a signal.

### 5 Guiding Principles

**1. Purposeful Restraint**
Every element on screen must justify its existence. Decoration is subtracted until only function remains. When in doubt, remove it.

**2. Accent as Signal**
Orange appears *only* where the user should look, act, or attend. It never decorates. If orange is everywhere, orange means nothing.

**3. Depth Through Darkness**
Hierarchy is built through layered darkness, not color proliferation. Backgrounds, cards, and surfaces are distinguished through subtle value shifts within the same dark family.

**4. Typography as Structure**
Type carries layout weight. Bold numbers and headings anchor screens. Type size alone communicates hierarchy — no need for color or icon noise to support it.

**5. Motion Serves State, Not Style**
Animations exist to communicate transitions between states — not to impress. If removing an animation breaks comprehension, it belongs. If it doesn't, cut it.

### What the UI Must Avoid

- Multiple competing accent colors
- Light-mode components embedded in dark surfaces
- Decorative gradients or glow effects not tied to a functional element
- Typography used at more than 4 distinct sizes per screen
- Rounded corners that compete with each other (multiple radii per screen)
- Empty space filled for its own sake

---

## 4. Brand Personality → UI Translation

### Personality Traits

| Trait | UI Expression |
|-------|--------------|
| Confident | Bold type scales, minimal hesitation in layout, no hedging UI patterns |
| Precise | 8pt grid adherence, exact radius values, no approximate spacing |
| Focused | Single accent, high signal-to-noise, distraction-free surfaces |
| Capable | Dense information without overwhelm, controls that feel powerful |
| Premium | True blacks, orange over gold, no cheap pastels, weight in type |

### Tone Spectrum

```
Formal ←————————————————————→ Casual
          ████████░░░
              ↑
         Slightly formal. Direct. No fluff.

Human ←————————————————————→ Machine
           ░░████████░
                  ↑
         Competent but not cold. Efficient but not robotic.
```

### Energy Level

**Controlled intensity.** Not quiet, not loud. The UI breathes with purpose. Orange punctuates silence — it doesn't fill it.

### Premium vs. Accessible Balance

Premium in aesthetic, accessible in behavior. The dark palette reads expensive. The interaction patterns must read *obvious*. These are not in conflict.

### Trust vs. Excitement Balance

Trust-dominant with excitement reserved for achievement/action moments. The system should feel *reliable at rest* and *alive when needed*.

---

## 5. Emotional Design System

### First Impression Emotion
**Focused confidence.** The screen should feel like the cockpit of something capable. Not intimidating — oriented. The user knows where they are immediately.

### Everyday Usage Emotion
**Efficient calm.** Interactions are fast. The system responds before doubt forms. There is no cognitive friction — just flow.

### Error State Emotion
**Controlled, non-alarming clarity.** Errors are surfaced without drama. The system acknowledges the problem, owns it briefly, and moves the user toward resolution. Orange stays out of errors — that is the domain of red, used sparingly.

### Success State Emotion
**Quiet satisfaction.** Success is acknowledged, not celebrated loudly. A brief state change, perhaps a subtle orange confirmation, then back to neutral. The product doesn't clap for itself.

### Loading/Waiting Emotion
**Active patience.** The system is visibly working. Loading indicators are minimal but present. The user should never feel abandoned during latency.

### AI Interaction Emotion
**Intelligence in service.** AI surfaces feel like a quiet collaborator — confident in output, transparent about uncertainty, non-intrusive in placement.

### Emotional Keywords

`precise` · `focused` · `capable` · `direct` · `uncluttered` · `alive` · `dark-confident` · `signal-clear`

---

## 6. Visual Language (Foundations)

### 6.1 Color System

#### Base Palette

| Token | Hex | Usage |
|-------|-----|-------|
| `--color-bg-base` | `#0A0A0A` | True base, OLED black, primary background |
| `--color-bg-surface` | `#141414` | Cards, elevated containers |
| `--color-bg-raised` | `#1E1E1E` | Input fields, secondary surfaces |
| `--color-bg-overlay` | `#252525` | Modals, overlays, popovers |
| `--color-bg-subtle` | `#2E2E2E` | Hover states, inactive toggles |

#### Accent System

| Token | Hex | Usage |
|-------|-----|-------|
| `--color-accent` | `#FF6B00` | **THE** accent. Primary CTAs, current state, live indicators |
| `--color-accent-hover` | `#FF8C33` | Hover/pressed state of accent elements |
| `--color-accent-muted` | `#FF6B001A` | Accent at 10% opacity — backgrounds for accent-labeled content |
| `--color-accent-dim` | `#7A3300` | Subdued accent for deep-layer emphasis |

> **Rule:** Orange appears in no more than **2 places per screen** simultaneously. If a third element requires emphasis, reconsider the hierarchy.

#### Text Palette

| Token | Hex | Usage |
|-------|-----|-------|
| `--color-text-primary` | `#F0F0F0` | Headlines, primary content |
| `--color-text-secondary` | `#A0A0A0` | Secondary labels, metadata |
| `--color-text-tertiary` | `#606060` | Disabled, placeholder, ghost text |
| `--color-text-accent` | `#FF6B00` | Accent-colored text, labels on active states |
| `--color-text-inverse` | `#0A0A0A` | Text on orange surfaces |

#### Semantic Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `--color-success` | `#2ECC71` | Positive states, confirmations |
| `--color-success-bg` | `#2ECC711A` | Success backgrounds |
| `--color-error` | `#E74C3C` | Errors, destructive warnings |
| `--color-error-bg` | `#E74C3C1A` | Error backgrounds |
| `--color-warning` | `#F39C12` | Caution, near-orange but visually distinct |
| `--color-info` | `#3498DB` | Informational, neutral attention |

#### Color Usage Rules

1. **Never use two accents on one screen.** Orange is the only warm color in the active palette.
2. **Never lighten black with blue.** All neutrals gray toward white, not blue.
3. **Transparency over separate colors.** Build surface hierarchy with opacity stacks, not distinct palette entries.
4. **Text on orange must be `--color-text-inverse`.** Never white-on-orange at small sizes.
5. **Semantic colors (error, success) are rare.** They appear only on state indicators — never for decoration.

#### Contrast Standards

| Context | Minimum Ratio |
|---------|--------------|
| Body text on surface | 7:1 |
| Secondary text | 4.5:1 |
| Large text (18px+) | 3:1 |
| Interactive elements | 3:1 against background |
| Accent orange on base black | Confirmed: ~5.1:1 ✓ |

---

### 6.2 Typography System

#### Font Families

| Role | Family | Rationale |
|------|--------|-----------|
| Display / Numbers | `DM Serif Display` or `Syne` | Commanding, structured weight for large numerals |
| UI / Body | `DM Sans` or `Outfit` | Clean, legible, slightly humanist — not sterile |
| Monospace (data) | `JetBrains Mono` | Tabular data, timestamps, coordinates |

> Avoid Inter, Roboto, and SF Pro as primary choices. Use system fonts only as deep fallbacks.

#### Type Scale

| Step | Size | Weight | Line Height | Usage |
|------|------|--------|-------------|-------|
| `--type-display` | 56px | 700 | 1.0 | Hero numbers (date, metric, headline) |
| `--type-h1` | 32px | 700 | 1.1 | Screen titles |
| `--type-h2` | 24px | 600 | 1.2 | Section headers |
| `--type-h3` | 18px | 600 | 1.3 | Card titles |
| `--type-body` | 15px | 400 | 1.5 | Primary content |
| `--type-body-sm` | 13px | 400 | 1.5 | Secondary content |
| `--type-caption` | 11px | 500 | 1.4 | Labels, metadata, tags |
| `--type-overline` | 10px | 600 | 1.6 | Category labels (uppercase tracked) |

#### Font Weight Usage

- **700+** — Numbers, headlines, CTAs. Anchor points.
- **600** — Sub-headers, active labels, emphasized metadata.
- **400** — Body content, passive labels.
- **Never 300 or lighter** — Thin type disappears on dark backgrounds.

#### Readability Rules

- Minimum body size: **13px**
- Maximum line length: **60 characters** for reading content, unconstrained for labels/data
- Letter spacing on overlines/caps: `+0.08em`
- **Never center-align body text.** Left-align always except hero numbers.
- **Tabular numbers** required for all numeric data that changes dynamically.

---

### 6.3 Spacing System

Built on an **8pt base grid** with 4pt subdivisions for fine-tuning.

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | 4px | Fine-grained internal padding, icon gaps |
| `--space-2` | 8px | Compact component internals |
| `--space-3` | 12px | Default internal component padding |
| `--space-4` | 16px | Standard component padding, list item gaps |
| `--space-5` | 20px | Card internal padding |
| `--space-6` | 24px | Section gaps, card-to-card |
| `--space-8` | 32px | Major section separation |
| `--space-10` | 40px | Screen top padding, hero spacing |
| `--space-12` | 48px | Inter-section breathing room |
| `--space-16` | 64px | Full screen section partitions |

#### Padding Rules

- Cards: `--space-5` (20px) horizontal, `--space-4` (16px) vertical minimum
- Screen edge margins: `--space-5` (20px) — consistent rail
- Bottom bar clearance: **24px above** nav bar (accounts for gesture zones)
- Top of screen content: **60px** minimum (below status bar region)

#### Density Levels

| Level | Description | When |
|-------|-------------|------|
| Compact | `--space-3` internals, `--space-4` between items | Data-dense lists, activity logs |
| Standard | `--space-4`–`--space-5` internals, `--space-6` between | Default product screens |
| Relaxed | `--space-6`+ internals, `--space-8` between | Onboarding, hero moments, empty states |

---

### 6.4 Shape & Geometry

#### Border Radius System

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-sm` | 8px | Small chips, badges, compact inputs |
| `--radius-md` | 12px | Standard cards, buttons, inputs |
| `--radius-lg` | 16px | Feature cards, panels |
| `--radius-xl` | 20px | Modal sheets, large containers |
| `--radius-2xl` | 28px | Bottom sheets, full-height panels |
| `--radius-full` | 9999px | Circular indicators, avatar containers, pills |

#### Shape Philosophy

- **Circles are status, not decoration.** The circular dot-calendar, the circular status indicators — these are communicating state, not applying visual style.
- **All primary containers share one radius.** A screen should not contain more than 2 distinct radius values among visible elements.
- **Sharp edges signal data.** If a container holds structured tabular data (timestamps, coordinates, stats), use `--radius-sm`. Softer containers hold narrative or interactive content.
- **No pure rectangles** — 0px radius exists only for full-bleed backgrounds.

---

### 6.5 Elevation & Depth

Depth is achieved through **value layering** (darker to lighter within the dark palette), NOT through traditional box shadows. Shadows are subtle and dark-tinted, never blue or cool-colored.

#### Layer Hierarchy

| Layer | Surface Token | Typical Elements |
|-------|--------------|-----------------|
| 0 — Ground | `--color-bg-base` | Screen background |
| 1 — Floor | `--color-bg-surface` | Persistent cards, list containers |
| 2 — Stage | `--color-bg-raised` | Inputs, secondary cards, inactive tabs |
| 3 — Float | `--color-bg-overlay` | Modals, active popovers |
| 4 — Accent Surface | `--color-accent` | Active/selected states, primary CTAs |

#### Shadow Tokens

```css
--shadow-sm: 0 2px 8px rgba(0, 0, 0, 0.4);
--shadow-md: 0 4px 16px rgba(0, 0, 0, 0.5);
--shadow-lg: 0 8px 32px rgba(0, 0, 0, 0.6);
--shadow-accent: 0 4px 20px rgba(255, 107, 0, 0.25);  /* For CTAs only */
```

#### Elevation Rules

- **Shadows are dark-tinted only.** Never cool/blue shadows — they kill the dark aesthetic.
- **Accent glow (`--shadow-accent`) is used only on the primary CTA button** — maximum one per screen.
- **Cards float through surface color, not box-shadow.** `--color-bg-surface` on `--color-bg-base` creates sufficient visual separation.

---

### 6.6 Motion & Animation

#### Motion Philosophy
> *"Motion should feel inevitable, not decorative."*

The system is not slow and ceremonious. It is responsive and direct. Motion communicates: "this happened" — nothing more.

#### Duration Standards

| Context | Duration | Easing |
|---------|----------|--------|
| Micro (feedback, icon swap) | 100–150ms | `ease-out` |
| Standard (state transition) | 200–250ms | `ease-in-out` |
| Navigation (screen entry) | 280–350ms | `cubic-bezier(0.4, 0, 0.2, 1)` |
| Modal/Sheet entry | 350–400ms | `cubic-bezier(0.16, 1, 0.3, 1)` — spring-like |
| Data loading | 400–600ms | Continuous loop, linear |

#### Transition Patterns

- **Screen entry:** Translate Y +16px → 0 + fade in. Minimal, directional.
- **Sheet/Modal:** Translate Y +100% → 0. Feels physical.
- **Card press:** Scale 0.97 → 1.0 at release. Tactile acknowledgment.
- **Toggle activation:** Thumb translates, background color transitions simultaneously.
- **Accent pulse:** Subtle `box-shadow` expand at 0.3s on confirmed action — accent glow only.

#### When Motion Must NOT Be Used

- On data that updates in real-time (don't animate every numeric tick)
- On disabled states
- In list scrolling (no parallax, no scroll-linked animations)
- When system `prefers-reduced-motion` is active — honor it fully

---

## 7. Layout System

### Grid System

| Context | Grid | Columns | Gutter |
|---------|------|---------|--------|
| Mobile default | Fluid | 4 | 16px |
| 2-column content | Fixed | 2×equal | 12px |
| Feature card grid | Fixed | 2×equal | 12px |
| Full-width card | Span all | 4 | — |

### Column Rules

- Feature/category grids: **2 columns always**, equal width, square or near-square cards
- List items: **full width**, left-rail icon, right-rail indicator
- Stats/metrics: **2 columns**, contrasting fills (one orange, one white/dark)
- Navigation: **bottom tab bar**, 3–5 items only

### Alignment Rules

- **Left-align all text in cards.** Right-align only metadata or chevrons.
- **Vertically center icons with their associated label** at all times.
- **Never float elements** — use flex or grid exclusively.
- **Screen title** sits at top-left on content screens, centered only on modal/overlay screens.

### Content Hierarchy Rules

1. **One primary action per screen** — visually dominant (orange fill, large, sticky)
2. **One primary display value per screen** — the "hero number/stat"
3. Secondary content follows without competing
4. Destructive or administrative actions are visually demoted

---

## 8. Component System

### 8.1 Buttons

#### Primary Button
- **Background:** `--color-accent`
- **Text:** `--color-text-inverse` (black), `--type-body` weight 600
- **Radius:** `--radius-full` (pill) or `--radius-md` depending on context
- **Height:** 52px touch target minimum
- **State — Hover:** `--color-accent-hover`, scale 1.01
- **State — Pressed:** Scale 0.97, slight shadow collapse
- **State — Disabled:** `--color-bg-raised`, `--color-text-tertiary`, no orange
- **Accent glow:** `--shadow-accent` on default state only

#### Secondary Button
- **Background:** `--color-bg-raised`
- **Text:** `--color-text-primary`
- **Border:** 1px `--color-bg-subtle`
- **No orange unless it has a specific accent-labeled role**

#### Icon Button
- **Size:** 44×44px minimum touch area, 36×36px visual
- **Background:** `--color-bg-raised`
- **Radius:** `--radius-full`
- **Active state:** Orange background, inverse icon

#### Destructive Button
- **Background:** `--color-error-bg`
- **Text:** `--color-error`
- **No orange involvement**

---

### 8.2 Inputs

- **Background:** `--color-bg-raised`
- **Radius:** `--radius-md`
- **Height:** 52px
- **Placeholder:** `--color-text-tertiary`
- **Border default:** None (surface color carries separation)
- **Border focus:** 1.5px solid `--color-accent`
- **Text:** `--color-text-primary`
- **Label:** `--type-caption`, `--color-text-secondary`, above the input
- **Error state:** 1.5px solid `--color-error`, error message below in `--color-error`

---

### 8.3 Toggles

- **Track inactive:** `--color-bg-subtle`
- **Track active:** `--color-accent`
- **Thumb:** White circle, `--shadow-sm`
- **Animation:** 200ms `ease-in-out` translation + simultaneous track color
- **Size:** 50×30px track minimum

---

### 8.4 Cards

Cards are the primary content containers. All cards follow the same DNA.

**Standard Card**
- Background: `--color-bg-surface`
- Radius: `--radius-lg`
- Padding: `--space-5`
- No border, no shadow by default
- Tap: Scale 0.97 feedback

**Feature Card (2-col grid)**
- Square-ish aspect ratio (1:1 to 4:3)
- Icon centered or top-left
- Label at bottom-left
- Optional badge (orange pill) top-right for promo/status

**Data Card (stats)**
- Two-tone: one card `--color-accent`, one card `--color-bg-surface`
- Large number `--type-display` dominates
- Label below in `--type-caption`
- Tap indicator: arrow icon top-right `--radius-full`

**Map/Media Card**
- Full-bleed image/map in upper portion
- Content overlay: gradient from transparent → `--color-bg-surface` at bottom
- Text laid over gradient

---

### 8.5 Navigation (Bottom Tab Bar)

- **Background:** `--color-bg-surface` with top border `--color-bg-raised`
- **Height:** 80px (includes safe area on iOS)
- **Icons:** 24px, line style, `--color-text-tertiary` inactive
- **Active icon:** `--color-accent`, filled variant if applicable
- **Active label:** `--type-caption`, `--color-accent`
- **Inactive label:** Hidden or `--type-caption`, `--color-text-tertiary`
- **Maximum 5 items**

---

### 8.6 List Items

- **Height:** 64px minimum
- **Leading element:** Icon (32px in `--color-bg-raised` container) or Avatar
- **Primary text:** `--type-body`, `--color-text-primary`
- **Secondary text:** `--type-body-sm`, `--color-text-secondary`
- **Trailing element:** Chevron (`>`) in `--color-text-tertiary` or metadata right-aligned
- **Divider:** 1px `--color-bg-subtle` at bottom, inset to content area (not full-bleed)

---

### 8.7 Status Indicators / Circular Dots

As seen in the calendar reference — a core VOID/EMBER pattern.

- **Active/past:** `--color-bg-overlay` (dark filled circle)
- **Current/today:** `--color-accent` (orange filled circle)
- **Future/inactive:** `--color-bg-raised` at 50% opacity (ghost circle)
- **Size:** 32px for calendar, 12px for inline status, 8px for compact indicators

---

### 8.8 Badges and Tags

- **Default badge:** `--color-bg-raised`, `--color-text-secondary`, `--radius-sm`
- **Accent badge:** `--color-accent`, `--color-text-inverse`, `--radius-full`
- **Semantic badge:** Background from semantic color family
- **Size:** `--type-caption`, 6px vertical padding, 10px horizontal

---

### 8.9 Sliders (Brightness, Volume, etc.)

- **Track:** `--color-bg-subtle` or gradient from dark to light
- **Fill:** Gradient toward `--color-accent` or white for neutral
- **Thumb:** White circle, 28px, `--shadow-md`
- **Height:** 8px track

---

### 8.10 Modals and Bottom Sheets

- **Background:** `--color-bg-overlay`
- **Handle:** 4px × 36px, `--color-bg-subtle`, centered at top
- **Radius:** `--radius-2xl` top-left and top-right only
- **Backdrop:** `rgba(0, 0, 0, 0.75)` blur optional
- **Max content height:** 90vh
- **Animation:** Slide up from bottom, `--shadow-lg`

---

### 8.11 AI-Specific Components

**AI Command Input**
- Pill-shaped input, `--color-bg-raised`
- Placeholder: "Command with AI..." in `--color-text-tertiary`
- Trailing: Waveform/voice icon in `--color-accent` container
- On focus: Accent border activates

**AI Suggestion Chips**
- Horizontal scrolling row
- `--color-bg-surface` chips, `--radius-full`
- Leading icon in `--color-accent`

**AI Confidence Indicator**
- Subtle — a thin orange underline or a small dot
- Never intrusive; the answer is the product, not the confidence display

---

## 9. Interaction Language

### Tap/Click Behavior

- **Cards:** Scale to 0.97 on press, release to 1.0 — haptic feedback where supported
- **Buttons:** Immediate visual response (<50ms). Press = scale down. Release = navigate or confirm.
- **List items:** Highlight background to `--color-bg-raised` on press, back on release
- **Icons:** Scale + color shift to `--color-accent` on press

### Hover (Web/Desktop contexts)

- Background shift: +1 layer (e.g., `--color-bg-surface` → `--color-bg-raised`)
- Cursor: `pointer` for interactive, `default` for display
- No underlines except on explicit hyperlinks

### Focus Behavior

- **Focus ring:** 2px solid `--color-accent`, 2px offset
- Never remove focus indicators — restyle instead
- Focus follows logical DOM order

### Gesture Vocabulary

| Gesture | Behavior |
|---------|----------|
| Swipe left on list item | Reveal destructive action (red zone) |
| Swipe right on list item | Reveal quick action (orange zone) |
| Pull to refresh | Spinner in `--color-accent`, threshold at 60px |
| Long press on card | Context menu appears (bottom sheet) |
| Pinch (map/media) | Standard zoom behavior |

### Response Time Expectations

| Action | Response |
|--------|----------|
| Button tap | < 50ms visual feedback |
| Screen navigation | < 300ms transition |
| Data load | Skeleton screen within 100ms |
| API failure | Error state within 5s, not indefinite spinner |

---

## 10. State System

### Complete State Definitions

| State | Visual Treatment |
|-------|-----------------|
| **Default** | Base styling as defined per component |
| **Hover** | +1 surface layer, cursor pointer |
| **Active/Pressed** | Scale 0.97, surface lightens slightly |
| **Focus** | 2px accent outline, offset 2px |
| **Disabled** | `--color-text-tertiary` text, `--color-bg-raised` bg, 40% opacity, no interaction |
| **Loading** | Skeleton shimmer (dark → slightly lighter dark), `--radius-md` shapes |
| **Success** | Brief accent pulse, then green checkmark, then return to default |
| **Error** | Red border, error message below, error icon leading |
| **Warning** | Yellow/amber indicator, non-blocking |
| **Empty** | Centered icon (ghost style), heading, subtext, optional CTA |
| **Offline** | Persistent banner top of screen, `--color-bg-overlay`, offline icon |
| **Partial data** | Show available data, loading skeleton where missing |
| **Destructive confirmation** | Requires a second deliberate tap, red CTA, "Are you sure?" pattern |

### Skeleton Loading Pattern

```
Background: --color-bg-surface
Shimmer gradient: linear-gradient(90deg, 
  --color-bg-surface → --color-bg-raised → --color-bg-surface)
Animation: translate X 200% over 1.5s, linear, infinite
```

### State Transitions

- Default → Hover: 150ms
- Default → Active: Immediate (haptic)
- Active → Success: 200ms color shift
- Any state → Error: 250ms, shake animation optional (5px horizontal, 3 cycles, 80ms)
- Any state → Loading: Replace content with skeleton immediately

---

## 11. Feedback & System Communication

### Loading Indicators

- **Page/screen load:** Full skeleton — never a centered spinner for primary content
- **Action processing:** Button transforms to loader (orange circular spinner replaces label)
- **Background sync:** Subtle activity indicator top-right, not full-screen

### Progress Feedback

- **Determinate:** Orange progress bar, `--radius-full`, 4px height
- **Indeterminate:** Orange dot pulse or waveform
- **Step progress:** Orange filled circles for completed steps, ghost for future

### Confirmation Patterns

- **Non-destructive:** Inline success state, no modal
- **Destructive:** Bottom sheet confirmation with explicit red CTA
- **Copy/share:** Toast notification (bottom of screen, 3s auto-dismiss)

### Error Recovery Patterns

- Show what went wrong in plain language
- Provide a specific action ("Retry", "Check connection", "Update")
- Never show raw error codes to users
- Persist errors until resolved — don't auto-dismiss failures

### Toast Notifications

- Position: Bottom of screen, above nav bar, 16px margin
- Background: `--color-bg-overlay`
- Radius: `--radius-md`
- Max width: Screen width minus 32px
- Duration: 3s for info, 5s for error, manual dismiss for warning
- Leading icon: Semantic color dot

---

## 12. Copy & Tone Guidelines

### Tone Profile

**Direct. Capable. Human but not warm-fuzzy.**

The system treats users as intelligent adults. No hand-holding language. No exclamation points in system messages.

### Button Text Style

- Action verbs only: "Confirm", "Scan", "Lock", "Add", "Set Schedule"
- Never: "Click here", "Please confirm", "Submit form"
- Maximum 3 words. Prefer 1–2.
- Title Case for CTAs. Sentence case for secondary.

### Error Message Style

| ❌ Avoid | ✓ Preferred |
|---------|------------|
| "Oops! Something went wrong." | "Couldn't load trips. Check your connection." |
| "Error 404: Resource not found" | "This page doesn't exist." |
| "Please try again later." | "Try again in a moment." |
| "Your session has expired." | "You've been signed out. Sign in to continue." |

### Helper Text Style

- Brief, factual, lowercase (sentence case)
- Placed below the input, not above
- Never repeat what the label already says
- Example: *"Code expires in 10 minutes"* not *"Please note that your verification code will expire."*

### Empty State Messaging

1. **Headline:** Describe what's missing, not the error. "No trips yet."
2. **Subtext:** One sentence suggesting the action. "Your rides will show up here."
3. **CTA (optional):** Primary action if actionable. "Book your first ride"

### AI Response Tone

- First person, no attribution ("Here's what I found" not "The AI has determined")
- Acknowledge uncertainty factually: "Based on recent activity..." not "I think maybe..."
- Never apologize for limitations — redirect instead

---

## 13. Accessibility Standards

### Contrast Ratios

| Element | Minimum | Target |
|---------|---------|--------|
| Body text | 4.5:1 | 7:1 |
| Large text (18px+) | 3:1 | 4.5:1 |
| Interactive elements | 3:1 | 4.5:1 |
| Orange accent on black | Confirmed ~5:1 ✓ | — |

### Text Sizing

- Minimum body: 13px / 0.813rem
- Support OS dynamic type scaling (iOS) and font scale (Android)
- No text locked to fixed px in body content

### Keyboard Navigation (Web)

- Tab order follows visual flow, left-to-right, top-to-bottom
- All interactive elements reachable via Tab
- Enter/Space activates buttons and toggles
- Escape closes modals and sheets
- Arrow keys navigate within menus and list items

### Screen Reader Compatibility

- All icons have `aria-label` when interactive, `aria-hidden` when decorative
- Status indicators include text equivalents (not just color)
- Dynamic content changes announced via `aria-live` regions
- Cards have descriptive accessible names beyond "Card"

### Color Independence

- Never rely on orange alone to communicate state — always pair with shape, text, or icon
- Error states use icon + text + color (not color alone)
- Active/inactive tab states use position + text + color

### Motion Reduction

```css
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

### Touch Targets

- Minimum: 44×44px for all interactive elements
- Preferred: 48×48px
- Spacing between adjacent targets: Minimum 8px

---

## 14. Iconography & Imagery

### Icon Style

- **Primary style:** Line icons with consistent 1.5px stroke
- **Active state:** Filled variant of same icon (not a different metaphor)
- **Grid:** 24×24px standard, 20px compact, 32px feature
- **Padding within container:** 4px internal padding minimum
- **Color:** `--color-text-secondary` inactive, `--color-accent` active, `--color-text-primary` for neutral-active

### Stroke Width

- **24px icon:** 1.5px stroke
- **20px icon:** 1.5px stroke
- **32px icon:** 2px stroke
- **Never mix stroke weights on the same screen**

### Metaphor Consistency

- Navigation: home, grid/menu, activity, profile — never swap metaphors between versions
- Actions: directional arrows always mean "go", circular arrows always mean "refresh"
- Status: lock = security, shield = protection, bolt = quick action — hold consistent

### Imagery (Maps, Product Shots)

- Maps: **Dark tile base** always (`rgba(0,0,0)` background, dark cartography)
- Route lines: `--color-accent` exclusively
- Location pins: White for origin, orange for destination
- Product shots (hardware): Dark background, product center-frame, slight glow/reflection
- No stock lifestyle photography in UI — illustration or product shots only

### Avatar Guidelines

- Shape: Circle, `--radius-full`
- Size: 32px list, 48px detail, 64px profile
- Fallback: Initial letter on `--color-bg-raised` background, `--color-text-primary` text

---

## 15. Data Visualization

### Chart Types

| Data Type | Chart |
|-----------|-------|
| Time-series activity | Bar chart (vertical) |
| Progress toward goal | Linear progress bar |
| Proportion | Arc/donut (minimal) |
| Geospatial | Dark-tile map with accent overlays |
| Comparative two-item | Side-by-side metric cards |

### Color Usage in Charts

- Primary series: `--color-accent`
- Secondary series: `--color-text-secondary`
- Background bars (total/scale): `--color-bg-raised`
- **Never** rainbow multi-color series — monochromatic with accent highlight

### Labeling Rules

- Axis labels: `--type-caption`, `--color-text-tertiary`
- Data labels (on bars): Only on selected/highlighted bar
- Tooltips: Dark overlay, `--radius-sm`, timestamp + value

### Emphasis Rules

- Highlight the current period's bar in `--color-accent`
- Past bars: `--color-bg-raised`
- Incomplete/future bars: `--color-bg-subtle`

---

## 16. AI Interaction Design

### AI Personality in UI

The AI exists as **infrastructure, not character**. It has no name visible in standard flows. It surfaces through capability, not through anthropomorphized personality.

- No "Hi there! I'm your AI assistant."
- No conversational filler in UI components
- Intelligent defaults over explicit AI promotion

### Confidence Display

| Confidence Level | UI Treatment |
|-----------------|--------------|
| High | No indicator — just the answer |
| Medium | Subtle label: "Based on recent data" |
| Low | Explicit framing: "Estimated — confirm before acting" |

### Uncertainty Handling

- Use hedging language *in copy*, not through UI complexity
- Don't surface confidence bars or percentage scores in default UI
- When uncertain: prompt user for confirmation, don't silently proceed

### Autonomy vs. Control Balance

- **AI acts, user reviews** — not the reverse
- Proactive suggestions surface as dismissible chips, not forced screens
- User override is always one tap away
- Destructive AI actions require manual confirmation (never autonomous)

### AI Interaction States

- **Listening:** Waveform animation in `--color-accent`
- **Processing:** Subtle pulse on input area, 3-dot ellipsis in accent color
- **Responding:** Text streams in — fade-in per line preferred
- **Complete:** State resets to default, no ceremony

---

## 17. Empty States & Edge Cases

### No Data States

**Structure:**
1. Ghost icon (line style, `--color-text-tertiary`, 48px)
2. Headline: "No [content] yet" — direct
3. Subtext: One sentence on what to do (optional)
4. CTA: Primary button if action resolves the empty state

**Never:** Sad-face illustrations, apology copy, dense instructions.

### First-Time Use

- Spotlight the primary action with accent emphasis
- Suppress secondary content areas until populated
- Onboarding hints: inline text, not modal overlays

### Network Issues

- Persistent banner (not modal) at top
- Cached content visible, labeled as potentially stale
- Retry: Single tap CTA in banner

### Permissions Issues

- Explain what the permission enables (not what it is)
- Primary CTA: "Allow [Capability]"
- Secondary: "Not now" (never "Deny" — user might re-engage later)

---

## 18. Microinteractions

### Button Feedback

- Press: 0.97 scale, 100ms — physical feel
- Release with action: Ripple origin at touch point, `--color-accent` at 20% opacity, 200ms expand

### Input Validation Feedback

- Valid on blur: Subtle green indicator (left border line or checkmark icon)
- Invalid on blur: Red border + shake (3-cycle, 80ms, ±4px horizontal)
- Real-time: Only after first blur — not while typing

### Hover Effects (Web)

- Card hover: `--color-bg-raised` background, 150ms ease
- Icon hover: `--color-accent` at 70%, 100ms
- Tab hover: Underline in `--color-accent` at 40%, 100ms

### Toggle Animation

Thumb translates 20px, track color fills simultaneously over 200ms. No bounce. Smooth and confident.

### Progress Completions

- On 100%: Brief scale pulse (1.0 → 1.05 → 1.0, 300ms)
- Color stays orange — no confetti, no celebratory state change unless milestone

---

## 19. Do / Don't Guidelines

### Color

| ✅ Do | ❌ Don't |
|-------|---------|
| Use orange for exactly one focal point per screen | Use orange as a background fill for large areas |
| Use dark surface progression for depth | Add blue tints to grays |
| Use semantic colors for status only | Use semantic colors decoratively |
| Pair orange CTA with dark background | Put orange text on orange background |

### Typography

| ✅ Do | ❌ Don't |
|-------|---------|
| Use bold display numbers to anchor screens | Use more than 4 type sizes per screen |
| Left-align body content | Center-align paragraphs |
| Let type scale establish hierarchy | Use color as the only hierarchy differentiator |
| Use tabular numbers for changing data | Use proportional numbers in aligned columns |

### Layout

| ✅ Do | ❌ Don't |
|-------|---------|
| One primary action per screen | Multiple orange CTAs competing |
| Consistent 20px screen rail | Vary margins between screens |
| 2-column feature card grids | 3+ column grids on mobile |
| Full-width list items | Card-within-card patterns |

### Cards

| ✅ Do | ❌ Don't |
|-------|---------|
| Single radius value per screen | Mix --radius-md and --radius-xl on same screen |
| Float cards through surface color | Add visible borders to dark cards |
| Use 20px internal card padding | Pad cards asymmetrically |

### Anti-Patterns

- **Glassmorphism** — frosted glass effects break the dark language
- **Gradient backgrounds** — the background must stay flat dark
- **Color-only status** — always pair color with icon or text
- **Crowded bottom bars** — max 5 items, prefer 4
- **Orange decorations** — if it's orange, it must be actionable or the current state

---

## 20. Decision Framework

### When to prioritize speed vs. clarity

> If the user is in motion or time-pressured → **Speed.** Fewer taps, bigger targets, primary action above the fold.

> If the action is irreversible → **Clarity.** Add the confirmation step. The friction is worth it.

### When to add friction

Add deliberate friction when:
- Action is destructive (delete, unlock, transfer)
- Action has financial consequence
- Action affects other users
- First-time performing a critical action

Never add friction to:
- Browsing or exploration
- Reading content
- Navigation between tabs
- Search

### When to simplify UI

Simplify when:
- More than 3 visual elements compete for attention at once
- The user has to read instructions to use a screen
- The error rate for a particular action is measurably high
- The same information appears in 2+ places

### When to expose complexity

Expose complexity when:
- Power users need fine-grained control
- Safety requires confirmation
- Legal/compliance requires explicit acknowledgment
- The default choice could be wrong for a significant user segment

### When to automate vs. ask user

| Automate when... | Ask user when... |
|-----------------|-----------------|
| Default is correct >90% of the time | Preference is highly personal |
| Reversal is easy | Reversal is difficult or impossible |
| Speed is the product value | Accuracy is the product value |
| Accumulated behavior predicts preference | This is first-time context |

---

## 21. Example Screens

### Home Screen

```
[Status bar — transparent]
[Screen rail: 20px]

GREETING                    [Avatar 32px]
"Hi, [Name]"

[2×2 Feature Card Grid — 12px gap]
[Ride ⟨PROMO badge⟩] [Delivery]
[Travel]               [Food]

[Full-width search input — 52px]
  🔍 "Where to?"         [Now ▾]

[Recent destinations — list]
  [Icon] Address primary
         Address secondary    [Clock icon]
  ─────────────────────────────
  [Icon] Address primary
         Address secondary    [Clock icon]

[Bottom tab bar]
  🏠(active/orange)  ☰  👤
```

---

### Activity / Log Screen

```
[Back <] Activity [settings ⋯]

PAST

[Map card — full width, dark tiles, 180px height]
  Comfort
  Aug 24, 7:10 PM
  ⛔ Cancelled

[List items — compact]
[Car icon] Address              >
           Date · Price
  ───────────────────────────────
[Car icon] Address              >
           Date · Price
```

---

### Profile / Settings Screen

```
Hi there 👋
[Name]                      [Avatar 48px]

[3-col quick action row]
[?] Help   [💳] Wallet   [🕐] Trips

[Settings list]
  [📨] Messages    •(indicator)    >
  ───────────────────────────────
  [⚙️] Settings                    >
  ───────────────────────────────
  [👤] Earn by driving              >
  ───────────────────────────────
  [ℹ️] Legal                        >

[Version number — bottom, caption, tertiary]
```

---

### IoT Control Screen (Smart Device)

```
< Main light           [⋯]

[Temperature tabs: Warm | Neutral | Cold(active)]

[Product shot — centered, full width]

[Brightness slider]
  [⏻]  ────────●────────  [☀️]
       50%

Schedule
  Sun   08:00 AM – 10:00 PM   [toggle: ON/orange]
  Mon   07:00 AM – 10:00 PM   [toggle: OFF]
  Tue   07:00 AM – ...        [toggle: ON/orange]
```

---

## 22. Implementation Guidelines

### Token Naming Convention

```css
/* Pattern: --[category]-[subcategory]-[variant] */

--color-bg-base
--color-bg-surface
--color-text-primary
--color-accent
--space-4
--radius-md
--shadow-sm
--type-body
--duration-standard
```

### CSS Custom Properties (Root)

```css
:root {
  /* Colors */
  --color-bg-base: #0A0A0A;
  --color-bg-surface: #141414;
  --color-bg-raised: #1E1E1E;
  --color-bg-overlay: #252525;
  --color-bg-subtle: #2E2E2E;

  --color-accent: #FF6B00;
  --color-accent-hover: #FF8C33;
  --color-accent-muted: rgba(255, 107, 0, 0.10);
  --color-accent-dim: #7A3300;

  --color-text-primary: #F0F0F0;
  --color-text-secondary: #A0A0A0;
  --color-text-tertiary: #606060;
  --color-text-inverse: #0A0A0A;

  --color-success: #2ECC71;
  --color-error: #E74C3C;
  --color-warning: #F39C12;

  /* Spacing */
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 20px;
  --space-6: 24px;
  --space-8: 32px;
  --space-10: 40px;
  --space-12: 48px;
  --space-16: 64px;

  /* Radii */
  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-xl: 20px;
  --radius-2xl: 28px;
  --radius-full: 9999px;

  /* Shadows */
  --shadow-sm: 0 2px 8px rgba(0, 0, 0, 0.4);
  --shadow-md: 0 4px 16px rgba(0, 0, 0, 0.5);
  --shadow-lg: 0 8px 32px rgba(0, 0, 0, 0.6);
  --shadow-accent: 0 4px 20px rgba(255, 107, 0, 0.25);

  /* Motion */
  --duration-micro: 120ms;
  --duration-standard: 220ms;
  --duration-navigation: 320ms;
  --duration-sheet: 380ms;
  --easing-standard: cubic-bezier(0.4, 0, 0.2, 1);
  --easing-spring: cubic-bezier(0.16, 1, 0.3, 1);
}
```

### Component Structure Rules

- **Atomic:** Token-consuming primitives (Button, Input, Badge)
- **Molecular:** Composed patterns (ListItem, FeatureCard, StatCard)
- **Organisms:** Screen sections (NavBar, ActivityFeed, ControlPanel)
- **Templates:** Screen-level compositions

### Reusability Rules

- No hardcoded hex values in components — tokens only
- No hardcoded spacing in components — tokens only
- Component accepts `variant`, `size`, and `state` props
- Dark theme is the only theme — no light mode toggle required

### Performance Considerations

- SVG icons over icon fonts
- `will-change: transform` on animated cards during active animation, removed after
- No layout-triggering properties in transitions (no width, height, top, left — only transform, opacity)
- Images: WebP, lazy loaded below fold
- Skeleton screens preempt layout shift

---

## 23. Design System Governance

### Ownership

| Role | Responsibility |
|------|---------------|
| Design Lead | Token decisions, component ratification, philosophy enforcement |
| Lead Engineer | Implementation standards, token consumption, performance review |
| Product Lead | Use-case validation, exception requests |

### Contribution Process

1. **Propose** — Raise a component/token request with use-case and mock
2. **Review** — Design Lead + Lead Engineer assess against system philosophy
3. **Prototype** — Build in isolation, no production merge
4. **Ratify** — Cross-team review, edge case documentation
5. **Publish** — Added to system with changelog entry

### Update Process

- Breaking changes: **Version bump** (v1 → v2), migration guide required
- Additive changes: **Minor bump** (v1.0 → v1.1), no migration needed
- Fixes: **Patch bump** (v1.0.0 → v1.0.1)

### Versioning System

Semantic versioning: `MAJOR.MINOR.PATCH`

- Major: Breaking token or component changes
- Minor: New tokens, new components, non-breaking additions
- Patch: Bug fixes, documentation corrections, accessibility fixes

### Deprecation Rules

- Deprecated components marked with `@deprecated` and removal version
- 2-version grace period before removal
- Migration path documented in component notes

---

## 24. Future Evolution

### Scalability Considerations

- The accent system (single orange) scales cleanly to multi-product contexts by swapping `--color-accent` at the product theme level — the rest of the system is color-agnostic
- The dark-native approach is inherently OLED-optimized, future-proofed for foldables and wearables
- Spacing tokens scale to tablet/desktop by introducing breakpoint-aware overrides, not parallel token sets

### Platform Expansion Rules

- **Tablet:** Same tokens, 2-column layout, increased density permitted
- **Desktop/Web:** Same dark language, mouse hover states added, sidebar navigation replaces tab bar
- **Wearable:** Subset of tokens — display type scale only, accent-only color, circular layouts
- **TV/Large Display:** Display type scale dominant, remote-navigation focus rings must be larger

### AI Evolution Considerations

- As AI capability grows, expose progressive disclosure — more AI surfaces without changing base UI language
- The "Command with AI" input pattern scales to become a universal control plane
- Confidence levels and tool usage indicators can expand without breaking existing screens
- Memory/context UI should remain opt-in and subtle — never mandatory on primary surfaces

### Design Debt Tracking

Maintain a living `DEBT.md` alongside this document:

- Log each known deviation from this system with component, date, reason
- Assign severity: `P1` (breaks system philosophy), `P2` (visual inconsistency), `P3` (minor token drift)
- Review quarterly, resolve P1s in current cycle, P2s in next

---

*VOID/EMBER Design Language — v1.0*
*Last revised: 2026*
*Maintained by: Design System Team*
