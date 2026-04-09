# VOID — UI/UX Design Language Document
### Version 1.0 | Dark Interface System for Intelligent Products

---

> *"Subtract until it breaks. Then subtract one more thing."*

---

## 1. Purpose of This Document

### What This Is
This document defines the complete visual, interaction, and emotional design language for products that operate within the **VOID design system** — a dark-native, data-forward, brutally minimal UI framework extracted from high-fidelity autonomous/intelligent product interfaces.

This is not a mood board. It is an engineering contract for aesthetics.

### Who Should Use It
- **Product Designers** — for screen composition, component design, and flow design
- **Frontend Engineers** — for token implementation, component behavior, and state management
- **AI/ML Product Teams** — for AI interaction surfaces, confidence UI, and agent feedback design
- **Brand Teams** — for ensuring UI expressions remain consistent with brand personality

### What It Standardizes
- Every pixel-level decision: color, type, spacing, radius, shadow
- Every interaction: tap, hover, focus, drag, swipe
- Every state: loading, error, empty, success, partial data
- Every AI-specific surface: agent output, confidence, memory, tool feedback

### What It Does NOT Cover
- Marketing/landing page design (separate document)
- Hardware industrial design
- Physical print materials
- Third-party integrations that cannot be reskinned

---

## 2. Product Context

### What These Products Do
Products built on VOID are **ambient intelligence interfaces** — systems that do heavy cognitive lifting on behalf of the user. Autonomous vehicles, AI agents, command dashboards, real-time data environments. The UI is not the product. The UI is the **skin on top of intelligence**.

### Target Users
- Technically literate, high-agency individuals
- Users who distrust decorative UI — they want signal, not noise
- Power users who interact with data continuously, not episodically
- Early adopters comfortable operating in sparse, trust-first environments

### Usage Environments
- Mobile-primary (OLED screens where true black is critical)
- Low-ambient-light settings (vehicles, offices at night, embedded hardware)
- Always-on, low-interaction-frequency contexts (check and dismiss, not browse)
- Occasionally: enterprise desktop dashboards

### Key User Goals
1. **Situational awareness** — know what's happening right now, instantly
2. **Frictionless action** — act on information with minimal steps
3. **Confident trust** — believe the system is operating correctly without constant validation
4. **Environmental integration** — the UI disappears; the world remains

### Constraints
- Performance: 60fps mandatory, 120fps where hardware supports
- OLED-first rendering: true `#000000` blacks are a feature, not a default
- Accessibility must not compromise aesthetic integrity — solve it architecturally
- No external font loading latency — fonts must be bundled or system-matched
- No unnecessary network calls for UI state

---

## 3. Design Philosophy

### Core Philosophy Statement
> **The interface should feel like it was always there — not designed, but discovered. Information surfaces when needed. Everything else is silence.**

### Guiding Principles

**1. Negative Space is the Primary Element**
Whitespace (here, blackspace) is not the absence of design. It is the design. Every element earns its existence by being irreplaceable.

**2. Data Over Decoration**
Numbers, labels, and status indicators are the UI. No illustrations, no hero imagery, no gradients masquerading as depth. If it doesn't carry information, it doesn't exist.

**3. Hierarchy Through Weight, Not Color**
Typography weight and size create hierarchy. Color is reserved for semantic meaning and critical state changes only. Never use color to "make it look nice."

**4. States Are First-Class Citizens**
Every element must be designed in all its states before it is considered complete. Loading is not an afterthought. Error is not an afterthought. Empty is not an afterthought.

**5. The System Speaks Only When It Has Something To Say**
Notifications, feedback, and system communication are earned interactions. No unnecessary toasts, no celebratory animations for routine actions, no confirmations that ask the user to confirm what they already intended.

### What the UI Prioritizes
- Speed of comprehension over richness of presentation
- Confidence over cleverness
- Consistency over expressiveness
- Trust over excitement

### What the UI Must Avoid
- Gradients used decoratively (only semantic gradients permitted)
- Rounded corners beyond the defined radius scale
- Shadows that simulate skeuomorphism
- Animations that exist for delight without serving function
- Color that draws attention without carrying meaning
- Typography that performs personality
- Any element that requires explanation to understand

---

## 4. Brand Personality → UI Translation

### Personality Traits

| Trait | UI Expression |
|---|---|
| **Precise** | Monospaced numerals, consistent grid alignment, exact spacing tokens |
| **Calm** | Low contrast backgrounds, no pulsing animations, muted accent palette |
| **Intelligent** | Information hierarchy that anticipates user need, progressive disclosure |
| **Unshowable** | No decorative elements, no brand colors in UI chrome |
| **Confident** | No disclaimers in UI copy, no excessive confirmation dialogs |
| **Premium** | Restraint, not luxury — what is removed signals quality |

### Tone Spectrum

```
FORMAL ──────────────────────────────── CASUAL
         ▲
         VOID sits here — precise, direct, unsentimental

HUMAN ─────────────────────────────── MACHINE
                              ▲
                              VOID sits here — functional, legible, not cold

QUIET ──────────────────────────────── EXPRESSIVE
   ▲
   VOID sits here — silence is the loudest statement
```

### Energy Level
**Quiet with latent intensity.** Resting state is near-silent. When something needs attention, it commands it — a single accent color, a single typographic weight change, a single motion beat. Not fireworks. A single flare.

### Premium vs Accessible
Premium through **subtraction**. Accessible through **architecture**. These are not in conflict in this system — the cleaner the UI, the more accessible it becomes. Every accessibility requirement is solved at the system level, never at the element level.

### Trust vs Excitement Balance
**9:1 toward trust.** Excitement is reserved for genuinely exciting moments — a route being completed, a first use, a major state transition. Routine usage is calm, unsurprising, and steady.

---

## 5. Emotional Design System

### First Impression Emotion
**"I can see everything I need. Nothing I don't."**
The emotional response is relief. Not awe, not delight — relief. The user should feel immediately capable, not overwhelmed or under-informed.

### Everyday Usage Emotion
**"This thing just works."**
Invisible competence. The system should feel like a trusted tool — a good mechanical watch, not a smartwatch. It does what it does, exactly as expected, without fanfare.

### Error State Emotion
**"I know what went wrong. I know what to do next."**
Never anxiety, never confusion. Error states in VOID are precise, non-dramatic, and recovery-forward. The system acknowledges the problem and immediately provides the path out.

### Success State Emotion
**"Done."**
Not celebration. Completion. Success states are brief, typographic, and immediate. They do not linger.

### Loading/Waiting Emotion
**"Something intelligent is happening."**
Loading is not dead time. The system communicates that processing is occurring — a subtle pulse, a progress indicator — without anxiety-inducing spinners or vague "please wait" messages.

### AI Interaction Emotion
**"The system understood me."**
Confidence without arrogance. AI surfaces should feel like a knowledgeable colleague — precise, efficient, and ready to be questioned. Never sycophantic, never uncertain without cause.

### Emotional Keyword Lexicon
- `calm` — resting state of every surface
- `confident` — how data is presented
- `responsive` — how interactions feel
- `precise` — how information is structured
- `intelligent` — how the system anticipates
- `non-intrusive` — how notifications behave
- `resolved` — how errors communicate
- `earned` — how success feels

---

## 6. Visual Language (Foundations)

### 6.1 Color System

#### Core Philosophy
**True black is sacred. Accent color is a weapon. Use it once.**

VOID is built on OLED-native true blacks with layered dark grays creating depth through luminosity, not shadow. The accent palette is surgical — one semantic color per meaning, used once per screen.

#### Full Palette

```
── BACKGROUND LAYERS ──────────────────────────────────

void-black          #000000    Surface 0 — screen background (OLED true black)
void-depth-1        #0A0A0A    Surface 1 — primary card/panel background
void-depth-2        #111111    Surface 2 — nested containers, input fields
void-depth-3        #181818    Surface 3 — hover states, subtle elevation
void-depth-4        #222222    Surface 4 — borders, dividers, separators

── FOREGROUND / TEXT ───────────────────────────────────

void-white          #FFFFFF    Primary text — headings, critical data
void-text-primary   #F2F2F2    Body text — standard readability
void-text-secondary #8A8A8A    Secondary labels — descriptors, captions
void-text-tertiary  #4A4A4A    Tertiary — placeholder, disabled, ghost

── ACCENT COLORS (SEMANTIC) ────────────────────────────

void-route-blue     #2D6CFF    Navigation routes, active paths, progress
void-alert-red      #FF3B3B    Warnings, critical states, brake indicators
void-success-green  #1DB954    Completion, confirmed, system healthy
void-warm-amber     #FF9500    Caution states, attention (non-critical)

── DATA ACCENT (NEUTRAL) ───────────────────────────────

void-data-line      #3A3A3A    Chart lines, dividers within data
void-data-dim       #2A2A2A    Background of data zones

── BRAND ACCENT (ChainGPT-style reference) ─────────────

void-brand-orange   #FF7920    Primary brand CTA, logo accent
void-brand-amber    #FF6001    Secondary brand CTA, interactive elements

── OVERLAY ─────────────────────────────────────────────

void-overlay-40     rgba(0,0,0,0.40)    Light overlay on map/imagery
void-overlay-70     rgba(0,0,0,0.70)    Heavy overlay — modal backdrops
void-overlay-scrim  rgba(0,0,0,0.85)    Full content scrim

── SEMANTIC COLORS ─────────────────────────────────────

success             #1DB954
error               #FF3B3B
warning             #FF9500
info                #2D6CFF
```

#### Color Usage Rules
1. **Backgrounds only use `void-black` through `void-depth-4`.** Never use accent colors as backgrounds except in full-bleed state transitions.
2. **Accent colors appear at most once per semantic meaning per screen.** Two red elements on one screen means one of them is wrong.
3. **`void-route-blue` is exclusively for paths, progress, and navigation.** It does not mean "link" in this system.
4. **Text uses only the foreground stack.** Colored text is reserved for inline states (error message inline, success confirmation inline).
5. **`void-brand-orange` appears only on interactive CTAs and the logotype.** It is not a highlight color.
6. **Transparency is a tool for map overlays only.** Do not use rgba for panel backgrounds — use the solid depth stack.

#### Contrast Standards
- Primary text on `void-black`: minimum 15:1 (exceeds WCAG AAA)
- Secondary text on `void-depth-1`: minimum 7:1 (WCAG AA)
- Accent colors on dark backgrounds: minimum 4.5:1
- Interactive elements: 3:1 against adjacent non-interactive

---

### 6.2 Typography System

#### Font Families

```
Display / Headings:    Monospace system — IBM Plex Mono, or equivalent geometric monospace
Data / Numerals:       Tabular numerals enabled — always. Use `font-variant-numeric: tabular-nums`
Body / Labels:         SF Pro Text (iOS) / Roboto (Android) / system-ui fallback
Captions / Meta:       Same as body, reduced weight and size
Brand Display:         Custom geometric (AT Amiga variant or equivalent) — headings only in brand contexts
```

#### Font Weights

| Token | Weight | Usage |
|---|---|---|
| `weight-regular` | 400 | Body copy, labels, descriptors |
| `weight-medium` | 500 | Secondary headings, active states |
| `weight-semibold` | 600 | Data values, primary info |
| `weight-bold` | 700 | Critical numbers, primary headings |
| `weight-light` | 300 | Ghost/placeholder, tertiary captions |

#### Type Scale

```
── DISPLAY ─────────────────────────────────────────────
display-xl      48px / 52px line-height / weight-bold
display-lg      36px / 42px line-height / weight-bold
display-md      28px / 34px line-height / weight-semibold

── HEADING ─────────────────────────────────────────────
heading-lg      22px / 28px line-height / weight-semibold
heading-md      18px / 24px line-height / weight-semibold
heading-sm      16px / 22px line-height / weight-medium

── BODY ────────────────────────────────────────────────
body-lg         16px / 24px line-height / weight-regular
body-md         14px / 20px line-height / weight-regular
body-sm         13px / 18px line-height / weight-regular

── DATA (MONOSPACE) ────────────────────────────────────
data-xl         48px / 1.0 line-height / weight-bold     (primary metric)
data-lg         32px / 1.0 line-height / weight-bold     (secondary metric)
data-md         22px / 1.1 line-height / weight-semibold (inline data)
data-sm         14px / 1.1 line-height / weight-regular  (micro data)

── CAPTION / LABEL ─────────────────────────────────────
label-md        12px / 16px line-height / weight-medium  / letter-spacing: 0.04em / UPPERCASE
label-sm        10px / 14px line-height / weight-medium  / letter-spacing: 0.06em / UPPERCASE
caption         11px / 14px line-height / weight-regular
```

#### Critical Rules
1. **Data values always use monospace.** `68°`, `3.1 mi`, `6:15 pm` — these are data, not prose.
2. **Uppercase labels use tracked letter-spacing** (0.04–0.08em). Never uppercase without tracking.
3. **Line height for data is tight (1.0–1.1).** Data is not prose — it does not need breathing room.
4. **Never mix more than 2 font families on one screen.**
5. **Descriptor labels (`Climate →`, `Capacity →`) are always smaller, lighter, and secondary to the value they describe.**
6. **Arrow `→` after interactive labels is a system-wide convention for "tap to expand/navigate."**

---

### 6.3 Spacing System

#### Base Unit: 4px

All spacing is a multiple of 4px. 8pt grid applies to all layouts.

```
space-1    4px
space-2    8px
space-3    12px
space-4    16px
space-5    20px
space-6    24px
space-8    32px
space-10   40px
space-12   48px
space-16   64px
space-20   80px
space-24   96px
```

#### Padding Rules

| Context | Horizontal | Vertical |
|---|---|---|
| Screen edge (mobile) | 20px | 24px |
| Card inner | 16px | 14px |
| Data cell | 12px | 10px |
| Button | 20px | 14px |
| Input field | 16px | 12px |
| Modal | 24px | 28px |

#### Density Levels

```
compact     — Data dashboards, real-time feeds. Reduce all padding by 25%.
standard    — Default. All tokens as defined.
relaxed     — Onboarding, long-form content. Increase vertical padding by 50%.
```

#### Section Spacing
- Between major sections on a screen: `space-8` (32px)
- Between related elements in a group: `space-4` (16px)
- Between a label and its value: `space-1` (4px) — they are a pair
- Between unrelated data cells: thin divider line + `space-4`

---

### 6.4 Shape & Geometry

#### Border Radius Scale

```
radius-none     0px      — Data cells, map containers, full-bleed elements
radius-xs       2px      — Tags, status pills, micro-elements
radius-sm       4px      — Inputs, small buttons
radius-md       8px      — Cards, panels, dropdowns
radius-lg       12px     — Bottom sheets, modals
radius-xl       16px     — Large cards, media containers
radius-full     9999px   — Pills, avatars, toggle tracks
```

#### Philosophy
**Geometry is not decoration — it signals function.**
- Sharp corners (0–2px) = data, system, machine
- Moderate radius (4–8px) = interactive, approachable
- Large radius (12–16px) = containment, modal depth
- Full radius = pills and toggles only

The interfaces in this system lean toward **low radius** — the world is not soft. Containers are mostly `radius-md` (8px) or flat. Never use large radius on data containers.

#### Edge Treatment
- Borders: 1px solid `void-depth-4` — used only to separate sibling elements, never to frame a standalone element
- No drop shadows on cards — depth is achieved through background layer differentiation
- Map containers are always edge-to-edge (full bleed) — no radius, no border

---

### 6.5 Elevation & Depth

#### Layer System

```
Layer 0 — void-black        Screen base, map backgrounds
Layer 1 — void-depth-1      Primary content panels
Layer 2 — void-depth-2      Input fields, nested containers
Layer 3 — void-depth-3      Hover states, popovers
Layer 4 — void-depth-4      Borders, dividers
Layer 5 — overlay           Scrim, blur backgrounds
```

#### Shadow Philosophy
**No decorative shadows. Zero.**
Depth is communicated through background color stepping, not shadows. When a panel appears "above" the background, it is because its background is `void-depth-1` (#0A0A0A) against `void-black` (#000000) — not because it has a drop shadow.

The only exception: **a focused interactive element** may use a very subtle glow (`box-shadow: 0 0 0 2px rgba(45, 108, 255, 0.4)`) to indicate keyboard focus without relying on color alone.

---

### 6.6 Motion & Animation

#### Motion Philosophy
**Motion communicates state change. It does not perform.**

When an element enters, it should feel like it was always about to be there. When it leaves, it dissolves rather than flies away. Motion should be felt, not watched.

#### Duration Standards

```
instant         0ms         — State changes that are logically immediate (toggle flip)
micro           80ms        — Hover feedback, button press response
fast            150ms       — Input focus, dropdown open
standard        250ms       — Panel enter/exit, modal appear
deliberate      400ms       — Route line draw, map zoom, page transition
slow            600ms       — First-load sequence, significant state change
cinematic       800–1200ms  — Onboarding, full-screen transitions (use sparingly)
```

#### Easing Curves

```
ease-snap       cubic-bezier(0.2, 0, 0, 1)        — UI elements appearing (fast in, slow settle)
ease-exit       cubic-bezier(0.3, 0, 1, 0.8)       — Elements leaving (slow start, fast exit)
ease-spring     cubic-bezier(0.34, 1.56, 0.64, 1)  — Interactive feedback (slight overshoot)
ease-data       cubic-bezier(0.4, 0, 0.2, 1)       — Data updates, number changes
ease-linear     linear                              — Progress bars, countdowns
```

#### Transition Patterns

| Transition | Duration | Easing | Notes |
|---|---|---|---|
| Screen enter | 250ms | ease-snap | Fade + slight upward translate (8px → 0px) |
| Screen exit | 200ms | ease-exit | Fade out only — no translation on exit |
| Panel expand | 250ms | ease-snap | Height expansion + fade in |
| Route line draw | 600ms | ease-linear | Stroke-dashoffset animation |
| Number update | 150ms | ease-data | Cross-fade between values |
| Modal enter | 300ms | ease-snap | Scale from 0.96 + fade |
| Toast enter | 200ms | ease-spring | Slide from bottom + slight bounce |
| Map zoom | 400ms | ease-snap | System-native map animation |

#### When Motion Must NOT Be Used
- Between individual data cell updates in a live feed (too distracting)
- On button states beyond micro feedback (hover, press — no animation)
- For purely decorative "loading art"
- When `prefers-reduced-motion` is active — all transitions collapse to instant or 80ms crossfade

---

## 7. Layout System

### Grid System

**Mobile (primary):**
- 4-column grid
- Column width: fluid
- Gutter: 16px
- Screen margins: 20px

**Tablet:**
- 8-column grid
- Gutter: 24px
- Screen margins: 32px

**Desktop:**
- 12-column grid
- Max content width: 1200px
- Gutter: 24px
- Screen margins: 48px

### Layout Anatomy (Mobile)

```
┌─────────────────────────────────┐
│ STATUS BAR (system)             │ ← system-owned
├─────────────────────────────────┤
│ MAP / HERO ZONE (full bleed)    │ ← 45-55% of screen height
│ — always edge-to-edge           │
│ — overlaid content uses scrim   │
│ — no padding applied            │
├─────────────────────────────────┤
│ CONTENT PANEL                   │ ← starts mid-screen
│  Padded: 20px horizontal        │
│  Primary heading                │
│  ─────────────────────────────  │
│  DATA GRID (2-col)              │
│  [Value] [Descriptor]  [Value]  │
│  ─────────────────────────────  │
│  SECONDARY SECTION              │
│  ─────────────────────────────  │
│  MEDIA / CONTEXTUAL BLOCK       │
├─────────────────────────────────┤
│ HOME INDICATOR (system)         │ ← system-owned
└─────────────────────────────────┘
```

### Data Grid Pattern
The 2-column data grid is the primary information layout primitive in VOID. It follows this structure:

```
[Large Value]    [Descriptor →]    |    [Large Value]    [Descriptor →]
────────────────────────────────────────────────────────────────────────
[Large Value]    [Descriptor →]    |    [Large Value]    [Descriptor →]
```

- Values are left-aligned within their cell
- Descriptor labels are directly below the value, reduced weight, with `→` for tappable rows
- Thin horizontal dividers separate rows — 1px `void-depth-4`
- Vertical divider between columns: none by default (implied separation from spacing)

### Alignment Rules
- **All text: left-aligned.** Center alignment only in empty states and single-line full-screen messages.
- **Numbers: left-aligned** within their data cell. Never right-aligned in this system.
- **Icons: vertically centered** with their associated label, 8px gap
- **Dividers: full bleed** to screen edges, not inset

### Content Hierarchy Rules
1. Critical state info is at the **top of the content panel**, immediately after the map zone
2. Primary data (destination, arrival time, main value) is at `heading-lg` or `data-lg`
3. Secondary data (sub-values, metrics) occupies the data grid at `data-md`
4. Actionable items (controls, settings entries) follow secondary data
5. CTAs and cancel/dismiss actions are always **pinned to bottom** of screen

---

## 8. Component System

### 8.1 Buttons

#### Variants

**Primary (CTA)**
```
Background:     void-depth-3 (#181818)
Text:           void-white / body-lg / weight-medium
Height:         54px (mobile) / 44px (desktop)
Radius:         radius-md (8px)
Padding:        20px horizontal
Border:         none
```

**Destructive**
```
Background:     rgba(255, 59, 59, 0.12)
Text:           void-alert-red / body-lg / weight-medium
Border:         1px solid rgba(255, 59, 59, 0.3)
```

**Ghost / Secondary**
```
Background:     transparent
Text:           void-text-secondary / body-md / weight-regular
Border:         1px solid void-depth-4
```

**Icon Button**
```
Size:           40x40px
Background:     void-depth-2
Icon:           24px / void-text-secondary
Radius:         radius-sm
```

#### Button States
| State | Visual Change |
|---|---|
| Default | As defined |
| Hover | Background +1 depth level |
| Pressed | Background +2 depth levels, scale 0.97 |
| Disabled | Opacity 0.35, not interactive |
| Loading | Replace label with 3-dot pulse animation |

#### Rules
- **Button labels use sentence case. Never all-caps for CTAs.** (Label tags use all-caps — buttons do not.)
- One primary CTA per screen. One.
- Destructive buttons never appear as primary CTAs. They must require an explicit secondary interaction.

---

### 8.2 Text Inputs

```
Height:         48px
Background:     void-depth-2
Border:         1px solid void-depth-4
Border-focus:   1px solid void-route-blue
Text:           void-text-primary / body-md
Placeholder:    void-text-tertiary / body-md
Radius:         radius-sm (4px)
Padding:        16px horizontal
```

**States:**
- `default` — as above
- `focus` — border becomes `void-route-blue`, subtle glow: `0 0 0 3px rgba(45,108,255,0.15)`
- `error` — border becomes `void-alert-red`, inline error message below at `caption` scale in `void-alert-red`
- `success` — border becomes `void-success-green`, check icon trailing
- `disabled` — opacity 0.4, no interaction

---

### 8.3 Data Cells (Core Primitive)

The data cell is the most frequently used component in VOID. It renders a single metric with its descriptor.

```
Structure:
  [Value]         — data-xl or data-lg / void-white
  [Descriptor →]  — label-sm / void-text-secondary / uppercase / tracked
  [Divider line]  — 2px wide / void-route-blue or void-alert-red / semantic

Rules:
  — Value and descriptor are always vertically stacked, never inline
  — The short colored divider line under the value is the only decoration permitted
  — Tappable cells include `→` in the descriptor
  — Non-tappable cells have no arrow
```

**Divider line semantics:**
- `void-route-blue` — navigation, position, distance data
- `void-alert-red` — critical system state (speed, brake, alert)
- `void-warm-amber` — caution, attention-required
- `void-success-green` — confirmed, healthy
- `void-text-tertiary` (default gray) — neutral data

---

### 8.4 Navigation & App Bar

```
Height:         0px visible chrome

VOID products have NO traditional navbar or app bar.
Navigation is achieved through contextual bottom sheets,
inline tappable states, and full-screen transitions.

The status bar is system-owned and untouched.
The first UI element is the map or hero zone.
```

There is intentionally no persistent navigation chrome. The product knows where the user is. It does not ask them to navigate.

---

### 8.5 Bottom Sheets

```
Background:         void-depth-1
Border-top:         1px solid void-depth-4
Border-radius:      radius-lg radius-lg 0 0 (top corners only)
Drag handle:        4px × 36px pill / void-depth-4 / centered / 8px below top edge
Padding:            24px top (after handle) / 20px horizontal / 34px bottom (safe area)
```

**Variants:**
- `peek` — 30% screen height. Shows summary data. Drag up to expand.
- `half` — 55% screen height. Primary interaction surface.
- `full` — 90% screen height. Configuration, full data views.

---

### 8.6 Dividers

```
Thickness:  1px
Color:      void-depth-4 (#222222)
Style:      solid
Margin:     0 (full bleed to screen edges)
```

Never use dotted or dashed dividers. Never use dividers with padding — they must touch the screen edge.

---

### 8.7 Media Player Component

```
Album art:          72×72px / radius-md / positioned left
Track info:         Track name: body-md / weight-semibold / void-white
                    Artist: body-sm / void-text-secondary
Controls:           3 icons (prev, play/pause, next) centered
                    Icon size: 28px / void-white
                    Gap between icons: 40px
Background:         void-depth-1
Divider:            1px void-depth-4 above component
```

---

### 8.8 Modals

```
Background:         void-depth-1
Backdrop:           void-overlay-70 blur(8px)
Radius:             radius-lg
Padding:            28px
Max-width (mobile): screen width - 40px (20px margins)
Animation:          scale(0.95) → scale(1) + fade / 300ms ease-snap
```

---

### 8.9 AI-Specific Components

#### Agent Status Indicator
```
A 6px dot adjacent to the AI's label.
  Idle:        void-text-tertiary / no animation
  Processing:  void-route-blue / slow pulse (2s loop)
  Error:       void-alert-red / no animation
  Complete:    void-success-green / fades out after 2s
```

#### AI Response Surface
```
Background:         void-depth-2
Left border:        3px solid void-route-blue
Padding:            16px
Border-radius:      0 radius-sm radius-sm 0
Typography:         body-md / void-text-primary
```

#### Confidence Display
```
Do not display percentage confidence as a number.
Use a 3-segment indicator:
  [●●●] High confidence — 3 segments lit in void-route-blue
  [●●○] Medium — 2 segments lit
  [●○○] Low — 1 segment lit / void-warm-amber
Segments: 6px × 20px / radius-xs / 4px gap
```

#### Uncertainty State
When AI output is uncertain, do not hide it. Display with:
- Reduced text opacity (void-text-secondary instead of void-white)
- Confidence indicator at 1-segment
- Optional inline label at `label-sm`: "ESTIMATED"

---

## 9. Interaction Language

### Tap / Click
- Feedback: immediate press state (background +2 depth levels, scale 0.97, 80ms)
- No ripple effects. No material design tap circles.
- Release triggers action, not press (tap-up, not tap-down)

### Hover (Desktop/Cursor)
- Background: shift one depth level up
- Cursor: `pointer` for interactive, `default` for data display
- No underlines for links in this system — links are styled differently (weight change + arrow)
- Hover transitions: 150ms / ease-snap

### Focus (Keyboard)
- Focus ring: `0 0 0 2px void-route-blue` — this is the ONLY decorative glow permitted in the system
- Focus must be visible at all times — no suppressing focus outlines
- Tab order follows visual reading order (top-to-bottom, left-to-right)

### Swipe / Gesture (Mobile)
- Bottom sheets: drag up/down with momentum physics
- Cards: horizontal swipe for dismiss (where applicable) — 60% of card width to trigger
- Map: system-native pan/zoom gestures; do not interfere
- Pull-to-refresh: not used — data refreshes automatically

### Keyboard Navigation
- All interactive elements reachable by Tab
- Modal traps focus until dismissed
- Escape closes modals, bottom sheets, and dropdowns
- Arrow keys navigate within data grids and lists

### Response Time Expectations

| Interaction | Expected Response | Tolerance |
|---|---|---|
| Button press | Visual feedback | < 80ms |
| Data load | Skeleton state | < 200ms |
| Screen transition | Begin animation | < 100ms |
| AI response start | Show typing state | < 300ms |
| Map load | Show placeholder | < 150ms |

---

## 10. State System

### Full State Reference

| State | Background | Text | Border | Icon | Notes |
|---|---|---|---|---|---|
| Default | void-depth-1 | void-white | void-depth-4 | void-text-secondary | Resting state |
| Hover | void-depth-3 | void-white | void-depth-4 | void-text-primary | Desktop only |
| Active/Pressed | void-depth-4 | void-white | void-depth-4 | void-white | scale(0.97) |
| Focus | void-depth-1 | void-white | void-route-blue | void-white | Focus glow |
| Disabled | void-depth-1 | void-text-tertiary | void-depth-3 | void-text-tertiary | opacity 0.4, no cursor pointer |
| Loading | void-depth-1 | — | void-depth-4 | — | Skeleton shimmer |
| Success | void-depth-1 | void-success-green | void-success-green | void-success-green | Fades to default after 2s |
| Error | void-depth-1 | void-alert-red | void-alert-red | void-alert-red | Persists until resolved |
| Warning | void-depth-1 | void-warm-amber | void-warm-amber | void-warm-amber | Persists until acknowledged |
| Empty | void-depth-1 | void-text-tertiary | void-depth-3 | void-text-tertiary | See §17 |
| Offline | void-depth-1 | void-warm-amber | void-depth-4 | void-warm-amber | System-level banner |
| Destructive | rgba(255,59,59,0.1) | void-alert-red | rgba(255,59,59,0.3) | void-alert-red | Requires confirmation |

### Skeleton Loading Pattern

```
Background:     void-depth-2
Animation:      shimmer sweep — left to right — 1.5s loop
Gradient:       linear-gradient(90deg, void-depth-2, void-depth-3, void-depth-2)
Border-radius:  match element it replaces
```

Skeletons match the exact dimensions and layout of the content they represent. Never use spinner-only loading for content areas.

### State Transitions
- Default → Hover: 150ms ease-snap
- Default → Loading: 100ms fade
- Loading → Success: 250ms fade through brief green flash
- Loading → Error: 200ms
- Any → Disabled: 150ms opacity fade
- Error → Default (on retry): 200ms

---

## 11. Feedback & System Communication

### Loading Indicators

| Context | Pattern |
|---|---|
| Full screen | Full-screen skeleton layout |
| Data cell | Shimmer on exact cell dimensions |
| Button | 3-dot pulse in place of label |
| Map | Native map loading behavior (not overridden) |
| AI processing | Dots animation + "Processing" at label-sm |

### Progress Feedback
- Route progress: animated stroke on the route line (live position marker)
- Task progress: thin linear bar — `void-route-blue` on `void-depth-2` background — pinned to top of panel
- Completion: bar fills to 100% → fades out in 400ms

### Confirmation Patterns
- **Routine actions: no confirmation.** The system acts.
- **Irreversible actions** (delete, cancel trip): bottom sheet confirmation with explicit destructive button
- **System-critical actions** (software update, hardware command): full-screen modal with typed confirmation where appropriate

### Error Recovery
- Error messages: always include **one specific next action** — not just "something went wrong"
- Format: `[What happened]. [What to do.]` — two sentences maximum
- Retry buttons: always present for network errors. Auto-retry after 5s with visible countdown.

### Undo Pattern
- Undo surfaces as a toast for up to 5 seconds after a destructive action
- Toast contains: `[Action label]` + `Undo` link in `void-route-blue`
- After 5 seconds, action is committed and toast auto-dismisses

---

## 12. Copy & Tone Guidelines

### Tone
**Precise. Declarative. Never apologetic.**
The system does not say "Oops!" It says what happened. It does not say "We're having trouble." It says "Connection lost. Reconnecting."

### Rules

| Context | Style | Example |
|---|---|---|
| Button labels | Verb + noun, sentence case | "Cancel ride" not "CANCEL" |
| Error messages | Past tense + next action | "Route unavailable. Try again." |
| Empty states | Present tense, neutral | "No trips scheduled." |
| Confirmations | Direct question | "Cancel this trip?" |
| Success states | Simple past | "Arrived." / "Saved." |
| Loading states | Present progressive | "Finding your route." |
| Descriptor labels | Noun only, uppercase | "CLIMATE" "CAPACITY" |
| AI responses | First person, present tense | "I've updated your route." |

### What Copy Must Avoid
- Exclamation marks in system UI (marketing copy excepted)
- Passive voice in error messages
- Vague language: "something went wrong", "an error occurred"
- Sycophantic AI responses: "Great question!", "Absolutely!"
- Anthropomorphizing the system unnecessarily ("I'm thinking...")
- Emoji in system UI. Zero.

---

## 13. Accessibility Standards

### Contrast Ratios
- Normal text (< 18px): minimum 4.5:1 (WCAG AA), target 7:1
- Large text (≥ 18px bold or ≥ 24px): minimum 3:1
- Interactive elements vs background: minimum 3:1
- Focus indicator vs adjacent background: minimum 3:1

### Text Sizing
- Minimum body text: 13px
- Minimum label text: 10px (uppercase tracked only)
- Never use `px` alone — pair with `rem` in implementation for system font scaling
- Support Dynamic Type (iOS) / Font Size (Android) — layout must not break at 150% text scale

### Keyboard Navigation
- Every interactive element must be tab-focusable
- Tab order follows DOM order (which follows visual order)
- Skip-to-content link on desktop web
- Modal and bottom sheet must trap focus
- No keyboard traps outside of modal contexts

### Screen Reader Compatibility
- All icons must have `aria-label` or adjacent visible text
- Data cells: `aria-label` must include both value and descriptor ("68 degrees, Climate settings")
- Map zones: `aria-label="Map showing current location and route"`
- Dynamic content: `aria-live="polite"` for data updates, `aria-live="assertive"` for critical alerts
- Loading states: `aria-busy="true"` on loading containers

### Focus Indicators
- Never remove focus outlines. Ever.
- Custom focus ring: `outline: 2px solid #2D6CFF; outline-offset: 2px`
- Focus state is always visible against all background layers

### Color Independence
- Never convey information through color alone
- Error states use both red color AND an error icon AND error text
- Route lines use both color AND a distinct stroke pattern (where contextually appropriate)
- Data cell semantic lines use color AND position — they are never the sole indicator

### Motion Reduction
```css
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```
All animations collapse. All transitions become instant crossfades at maximum 80ms.

---

## 14. Iconography & Imagery

### Icon Style
**Line icons. Single weight. No fill.**
- Stroke width: 1.5px at 24px size; 1px at 16px size
- Corner treatment: `round` linecap and linejoin
- Visual weight: optically balanced with the typography system
- No duotone. No gradient on icons. No decorative detail.

### Size System

```
icon-xs    16px — inline with body text, breadcrumbs
icon-sm    20px — compact UI, data cells
icon-md    24px — standard UI, navigation, controls
icon-lg    32px — empty states, feature icons
icon-xl    48px — onboarding, full-screen states
```

### Metaphor Rules
- Icons must be universally understood — no invented metaphors
- Prefer established iOS/Android conventions for navigation (back = chevron-left, settings = gear)
- AI-specific icons: use circuit/node motifs, not robot faces
- Arrow `→` is used as a text character, not an SVG icon, for descriptor links

### Avatar Guidelines
```
Shape:          Circle (radius-full)
Size:           40px standard / 28px compact / 56px large
Border:         none in default state
                2px void-route-blue in active/selected state
Fallback:       Monogram initials — 2 chars — body-md / weight-semibold
Background:     void-depth-3 for fallback
```

### Illustration Style
**None.** VOID does not use illustrations.
The exception is onboarding, where simple single-weight line art (matching icon style) may be used, maximum 160×160px, `void-text-tertiary` color.

---

## 15. Data Visualization

### Chart Types (Permitted)
- Line charts (time series) — primary chart type
- Bar charts (comparison) — horizontal only
- Minimal area charts (sparklines within data cells)
- No pie charts. No donut charts. No radar charts.

### Color Usage in Charts
- Primary series: `void-route-blue`
- Secondary series: `void-text-secondary`
- Alert threshold: `void-alert-red`
- Reference lines: `void-depth-4` (barely visible — they frame, not shout)
- Never more than 3 data series on a single chart

### Labeling Rules
- Axis labels: `label-sm` / `void-text-tertiary` / no background
- Data point labels: only on hover/focus, never always-on
- Chart title: `label-md` / `void-text-secondary` / above the chart

### Emphasis Rules
- The most critical data point gets `void-route-blue` emphasis
- Everything else is `void-text-secondary` or dimmer
- Do not use bold weight in charts — use color/brightness contrast instead

### Interaction Behavior
- Hover reveals tooltip with exact value: `data-sm` / `void-depth-3` background / `radius-xs`
- No click-to-drill on mobile charts unless explicitly required
- Touch target on mobile data points: minimum 44×44px hit zone

### Handling Uncertainty
- Uncertain data ranges: dashed line (4px dash / 4px gap) in same color at 50% opacity
- Projected/estimated values: `label-sm` "ESTIMATED" tag above affected zone
- Missing data: gap in line, never interpolated

---

## 16. AI Interaction Design

### AI Personality in UI
The AI in VOID-based products is a **specialist, not an assistant**. It knows its domain completely and speaks only from that domain. It does not chitchat. It does not hedge unnecessarily. It does not explain its reasoning unless asked.

### Confidence Display
See §8.9 — 3-segment indicator. Rules:
- High (80–100%): 3 segments / `void-route-blue`
- Medium (50–79%): 2 segments / `void-route-blue` at 60% opacity
- Low (<50%): 1 segment / `void-warm-amber`
- Never show raw percentage numbers to end users in consumer interfaces

### Uncertainty Handling
- AI must surface uncertainty. Silent overconfidence is a bug.
- Uncertain values are shown at `void-text-secondary` opacity (not hidden)
- "ESTIMATED" label appears inline at `label-sm`
- The AI must offer an alternative or next action alongside an uncertain result

### Clarification Behavior
- AI asks one clarifying question maximum per interaction
- Clarification is asked before action, not after
- Clarification surfaces as a bottom sheet option, not an inline chat bubble
- If the AI can take a safe default action, it acts and informs — it does not ask

### Autonomy vs Control
```
LOW STAKES:     AI acts, informs passively (toast notification)
MEDIUM STAKES:  AI acts, offers undo (5s toast with undo)
HIGH STAKES:    AI proposes, user confirms (bottom sheet)
CRITICAL:       User always initiates, AI never auto-acts
```

### Memory Representation
- Memory is not a visible UI concept in most VOID surfaces
- When memory is surfaced: it appears as a pre-populated context chip above the input field
- Chip format: `[Context label] ×` — tappable to remove
- Memory stored: indicated by brief system toast "Noted." — no icon, no fanfare

### Tool Usage Feedback
When AI is using tools (searching, fetching, calculating):
```
Show:     Agent Status Indicator (processing state)
Label:    verb-noun format at label-sm — "FETCHING ROUTE" / "CALCULATING" / "READING CALENDAR"
Duration: if >3s, add estimated time "~5s"
On complete: indicator snaps to complete state, fades in result
```

---

## 17. Empty States & Edge Cases

### No Data State
```
Icon:       icon-lg / void-text-tertiary
Headline:   heading-sm / void-text-secondary — direct statement of what's missing
Subtext:    body-sm / void-text-tertiary — one line explaining why or what to do
CTA:        ghost button if an action can help. None if there is nothing to do.
```

Example: No trips scheduled. → "Your calendar has no upcoming trips." → [Connect Calendar]

### First-Time Use
- No splash screens
- No animated walkthroughs
- Required permissions are requested contextually (when the feature is first used)
- The first experience is the real experience. Trust the design.

### Error States (Screen-level)
```
Icon:       icon-xl / void-alert-red (if critical) or void-text-tertiary (if recoverable)
Headline:   What happened — plain language, no code
Subtext:    What to do next — always present
CTA:        Primary action (Retry / Go Back / Contact Support)
```

### Network Issues
- Offline banner: 40px full-width / `void-warm-amber` text on `void-depth-1` background / pinned to top
- Copy: "Offline. Last updated [time]."
- Data from cache displays at reduced opacity (0.65) to indicate staleness
- Auto-reconnect is silent; success is announced by banner disappearing + brief green flash

### Permissions Issues
- Requested contextually, not upfront
- When denied: empty state with specific explanation ("Location access needed to show your route") and system settings deeplink

### Incomplete Workflows
- Progress is auto-saved silently. Never lose user input.
- Re-entry into an incomplete flow: bottom sheet asks "Continue where you left off?" with brief summary
- Option to start fresh is always present

---

## 18. Microinteractions

### Button Feedback
- Press: scale(0.97) + background +2 depth levels / 80ms / ease-spring
- Release: scale(1.0) + return to hover state / 120ms / ease-snap

### Input Validation Feedback
- Real-time validation (after first blur or after 800ms typing pause)
- Valid: border snaps to `void-success-green` / checkmark icon appears
- Invalid: border snaps to `void-alert-red` / inline error below field slides in from top (4px translate, 150ms)
- Error text: never shifts layout — it occupies reserved space (collapsed to 0 height when no error)

### Hover Effects
- Backgrounds shift one depth level: 150ms / ease-snap
- No scaling on hover. No glow. No shadow.
- Tappable rows: full-width background shift to `void-depth-3`

### Subtle Animations
- Data value updates: cross-fade 150ms (old value fades out, new value fades in)
- Route line: draws progressively on load (stroke-dashoffset animation, 600ms)
- Position marker (vehicle): smooth interpolation, not teleport, between coordinate updates
- ETA countdown: silent number update, no animation unless value changes by >2 minutes

### Sound
Not in scope for this version of the design system. When implemented, sound design follows the same principle: **functional, not decorative.** Alert sounds only for critical system states.

---

## 19. Do / Don't Guidelines

### Typography

✅ DO
- Use monospace for all data values
- Use `→` for interactive descriptors
- Use uppercase + tracking for labels
- Let whitespace create hierarchy

❌ DON'T
- Mix serif and sans-serif on one screen
- Use colored text for non-semantic purposes
- Use font size as the only differentiator between hierarchy levels
- Justify text

---

### Color

✅ DO
- Use `void-route-blue` exclusively for navigation/progress
- Use accent colors semantically and sparingly
- Achieve depth through background layer stepping

❌ DON'T
- Use gradients on backgrounds decoratively
- Apply `void-brand-orange` to anything other than CTAs and logotype
- Use more than one accent color per data cell
- Place colored text on colored backgrounds

---

### Layout

✅ DO
- Allow the map zone to be full-bleed
- Pin CTAs to the bottom
- Use the data grid primitive for multiple metrics
- Let negative space do the work

❌ DON'T
- Pad the map zone
- Stack more than 4 metrics in a single data grid
- Use centered alignment for data-heavy screens
- Add chrome that exists only to fill empty space

---

### Motion

✅ DO
- Use motion to communicate state change
- Keep animations under 400ms for UI elements
- Provide instant feedback on interaction

❌ DON'T
- Loop animations unnecessarily
- Animate for decoration
- Add transitions where instant state change is more appropriate
- Override `prefers-reduced-motion`

---

### Copy

✅ DO
- Be direct and declarative
- Always provide next action in error states
- Use sentence case for buttons

❌ DON'T
- Use exclamation marks in system UI
- Apologize in error messages
- Use passive voice
- Write more than 2 sentences for any system message

---

### Anti-Patterns (Never Do)

| Anti-Pattern | Why It's Wrong |
|---|---|
| Tooltip on every icon | VOID icons are self-evident or have adjacent labels |
| Celebratory confetti animation | Routine completion is not a party |
| Gradient button backgrounds | Breaks flat depth system |
| Multiple CTAs of equal weight | One primary CTA per screen — always |
| Full-screen loading spinner (spinner only) | Show skeleton — never just spin |
| Status bar recoloring | System-owned — never touched |
| "Are you sure?" confirmation for reversible actions | Undo pattern handles this |
| Sidebar navigation on mobile | Not this system's navigation model |

---

## 20. Decision Framework

### Speed vs Clarity
```
IF information changes in real-time AND user is actively monitoring:
  → prioritize speed (instant updates, no animation)
IF information is being presented for the first time:
  → prioritize clarity (controlled reveal, hierarchy)
IF action has irreversible consequences:
  → add deliberate friction (confirmation bottom sheet)
```

### When to Add Friction
- Friction is added **only** for destructive, irreversible, or high-stakes actions
- Friction is **never** added to make UI feel more substantial or "serious"
- Friction is implemented as a **confirmation surface**, not a multi-step form

### When to Simplify UI
- When more than 5 data points compete for attention on one screen — restructure into hierarchy
- When a user has completed onboarding — remove guidance, trust them
- When data is predictable — pre-fill, pre-select, and get out of the way

### When to Expose Complexity
- When the user has explicitly navigated to a settings/configuration surface
- When a professional user needs fine-grained control (expose via progressive disclosure)
- When hiding complexity creates confusion about what the system is doing (e.g., AI actions)

### When to Automate vs Ask
```
AUTOMATE when:
  — Action is reversible
  — Default is correct >95% of the time
  — Asking creates more cognitive load than acting

ASK when:
  — Action is irreversible
  — Personal data or system state will be permanently modified
  — The user has previously expressed a preference to be asked
```

---

## 21. Example Screens

### Screen A: Approach State (Vehicle En Route to Pickup)
```
Zone 1 — MAP (full bleed, 50% height)
  Dark 3D isometric map view
  Vehicle model lit from below (white light cone)
  Dotted approach path from vehicle to pickup pin
  Pickup pin: square icon with location label

Zone 2 — CONTENT PANEL
  "[N] minutes away"   — heading-lg / void-white
  "Model Y"            — body-md / void-text-secondary
  ──────────────────────────────────────────
  [68°]              | [4]   Passengers Max
  [Climate →]        | [Capacity →]
  ──────────────────────────────────────────
  Destination via Calendar
  "Stanford Shopping Center  →"   — heading-sm / void-white
  ──────────────────────────────────────────
Zone 3 — PINNED BOTTOM
  [Cancel]   — Primary button / full-width
```

### Screen B: In-Ride State
```
Zone 1 — MAP (full bleed, 45% height)
  Route line: void-route-blue animated stroke
  Vehicle: live position marker
  Destination pin at end of route

Zone 2 — CONTENT PANEL
  "Going to"           — label-sm / void-text-tertiary / uppercase
  "Stanford Shopping Center  ⋮"  — heading-md / void-white
  ──────────────────────────────────────────
  [6:15 pm]      [15 min]      [3.1 mi]
  — Inline tricolumn, data-md, no labels (self-evident)
  ──────────────────────────────────────────
  [68°]     | [3/10]     | [Auto]
  [Climate] | [Volume →] | [Seat →]
  ──────────────────────────────────────────
  [Album art 72px]   Track name — body-md
                     Artist — body-sm / void-text-secondary
                     [◀◀]    [▶]    [▶▶]
```

### Screen C: Error State
```
Zone 1 — FULL SCREEN
  (no map)
  icon-xl: signal-lost / void-alert-red
  "Route unavailable."      — heading-md / void-white
  "GPS signal lost."        — body-md / void-text-secondary
  ────────────────────────
  [Try Again]               — Primary button
  [Contact Support →]       — Ghost button
```

### Screen D: Empty State (No Trips)
```
icon-lg: calendar-empty / void-text-tertiary
"No upcoming trips."    — heading-sm / void-text-secondary
"Connect your calendar to see scheduled trips."
                        — body-sm / void-text-tertiary
[Connect Calendar]      — Ghost CTA
```

---

## 22. Implementation Guidelines

### Token Naming Convention
```
Category:
  color-{layer}-{variant}    e.g. color-background-depth1
  color-text-{priority}      e.g. color-text-primary
  color-accent-{semantic}    e.g. color-accent-route
  color-semantic-{state}     e.g. color-semantic-error

  space-{n}                  e.g. space-4, space-8
  radius-{size}              e.g. radius-sm, radius-md
  font-size-{context}-{size} e.g. font-size-data-xl
  font-weight-{name}         e.g. font-weight-semibold
  duration-{name}            e.g. duration-standard
  ease-{name}                e.g. ease-snap
```

### CSS Custom Properties (Root)

```css
:root {
  /* Backgrounds */
  --color-bg-base:        #000000;
  --color-bg-depth-1:     #0A0A0A;
  --color-bg-depth-2:     #111111;
  --color-bg-depth-3:     #181818;
  --color-bg-depth-4:     #222222;

  /* Text */
  --color-text-primary:   #F2F2F2;
  --color-text-secondary: #8A8A8A;
  --color-text-tertiary:  #4A4A4A;

  /* Accents */
  --color-accent-route:   #2D6CFF;
  --color-accent-error:   #FF3B3B;
  --color-accent-success: #1DB954;
  --color-accent-warning: #FF9500;
  --color-brand-primary:  #FF7920;

  /* Spacing */
  --space-1: 4px;   --space-2: 8px;   --space-3: 12px;
  --space-4: 16px;  --space-5: 20px;  --space-6: 24px;
  --space-8: 32px;  --space-10: 40px; --space-12: 48px;
  --space-16: 64px;

  /* Radius */
  --radius-none: 0;     --radius-xs: 2px;  --radius-sm: 4px;
  --radius-md: 8px;     --radius-lg: 12px; --radius-xl: 16px;
  --radius-full: 9999px;

  /* Duration */
  --dur-micro:      80ms;
  --dur-fast:       150ms;
  --dur-standard:   250ms;
  --dur-deliberate: 400ms;
  --dur-slow:       600ms;

  /* Easing */
  --ease-snap:   cubic-bezier(0.2, 0, 0, 1);
  --ease-exit:   cubic-bezier(0.3, 0, 1, 0.8);
  --ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);
  --ease-data:   cubic-bezier(0.4, 0, 0.2, 1);
}
```

### Component Structure Rules
- Components are atomic — no component depends on another component's internal styles
- Variants are implemented via CSS custom property overrides or class modifiers, not duplicated stylesheets
- State classes: `.is-loading`, `.is-error`, `.is-disabled`, `.is-active` — applied to the component root
- Never inline `style=` except for dynamic values (e.g., route line length, progress bar width)

### Reusability Rules
- Every token must be defined before it is used
- No magic numbers in component code — always reference a token
- Components export a props interface (or equivalent) — all variants and states are declarable from outside

### Performance Considerations
- No layout-triggering CSS properties in animations (`width`, `height`, `top`, `left`) — use `transform` and `opacity` only
- Map rendering is always hardware-accelerated (`will-change: transform` on map container)
- Skeleton screens must not cause layout shifts when real content loads — same dimensions
- Font loading: preload critical weight (400, 600) — other weights lazy-loaded
- Image assets: WebP with AVIF fallback, lazy-loaded below the fold

---

## 23. Design System Governance

### Ownership
- **Design System Lead**: owns this document and all token definitions
- **Component owners**: assigned per component — one designer, one engineer
- **Product teams**: consumers — can propose changes, cannot unilaterally modify tokens

### Contribution Process
1. Open a proposal (ticket/PR) with: what, why, evidence (user feedback, usage data, or design rationale)
2. Design System Lead reviews within 5 business days
3. If approved: design spec produced, engineering implementation follows
4. Component ships behind a version tag — consuming teams opt in

### Update Process
- Breaking changes: major version bump (1.0 → 2.0)
- New components: minor version bump (1.0 → 1.1)
- Bug fixes and token adjustments: patch version (1.0 → 1.0.1)
- All changes documented in CHANGELOG.md with migration notes

### Deprecation Rules
- Deprecated components get a `[DEPRECATED]` tag in documentation
- Minimum 2-release cycle before removal
- Migration guide is required before a component can be deprecated
- Engineers are notified via automated lint warnings in their codebase

---

## 24. Future Evolution

### Scalability Considerations
- All tokens are platform-agnostic — the same token system maps to iOS, Android, web, and embedded
- Component library must support dark mode as the default, with a future light mode variant behind a flag
- Layout system scales from 320px to 2560px without component-level breakpoints — layout is handled at the system level

### Platform Expansion Rules
- When expanding to a new platform (watchOS, embedded HMI, XR), derive tokens from this document — do not fork
- Platform-specific tokens (e.g., watchOS crown interaction, HMI knob input) are additive, not substitutive
- Brand identity (colors, type, philosophy) remains constant across all platforms

### AI Evolution Considerations
As AI capabilities expand, new UI patterns will be needed for:
- **Proactive AI surfaces** — system-initiated suggestions without user prompt (must follow autonomy-vs-control framework in §16)
- **Multimodal input** — voice, gesture, and environment-aware input surfaces
- **AI memory visualization** — when persistent memory becomes user-visible, it follows the chip pattern defined in §16 with a dedicated memory management surface
- **Confidence evolution** — as AI improves, confidence UI may shift from 3-segment to more nuanced representations — but must never become a raw percentage in consumer contexts

### Design Debt Tracking
- All known debt is logged as `[DEBT]` tagged items in the design system backlog
- Debt is reviewed quarterly and prioritized by: user impact, engineering cost, design consistency risk
- A component with known debt may not be promoted to "stable" status until debt is resolved

---

*VOID Design Language Document — v1.0*
*For internal design and engineering use.*
*Do not distribute externally without redaction of product-specific details.*

---
