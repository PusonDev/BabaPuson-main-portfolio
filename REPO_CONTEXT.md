# PUSON.DEV — REPOSITORY CONTEXT
# For AI agents: read this file FIRST. It gives full project understanding in minimum tokens.
# Last updated: v2 (years removed from timeline, age removed everywhere)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## PROJECT OVERVIEW
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Type:       Personal portfolio website — pure HTML/CSS/JS. No framework. No build step.
Owner:      Md. Wahidur Rahman Puson
Location:   Bashabo Kodomtola, Dhaka, Bangladesh
Contact:    Wahidur757@gmail.com · 01629944975 · https://wa.me/8801629944975
Output:     Two HTML files. Both self-contained (all CSS + JS inline).

Files:
  index.html   → Main portfolio page (letter-effect name applied; rest unchanged)
  about.html   → Full story page (complete — all 8 sections + nav + footer)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## HARD RULES (never violate)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

- NO age, date of birth, or birth year anywhere on either page
- NO year labels on experience timeline (roles + companies only, no dates)
- NO frameworks (no React, Vue, Bootstrap, Tailwind, jQuery, GSAP)
- NO external images (CSS shapes and gradients only)
- NO extra files beyond index.html and about.html (this REPO_CONTEXT.md is agent docs only)
- NO Inter/Roboto/Arial fonts — use only the 4 specified fonts
- NO lorem ipsum or placeholder text

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## DESIGN SYSTEM (identical on both pages)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Fonts (Google Fonts CDN):
  Bebas Neue         → hero name, display numbers, large headings
  Barlow Condensed   → section h2, card titles (600–700)
  DM Sans            → body text (300–400–500)
  JetBrains Mono     → labels, tags, badges, code

Key colors (CSS vars):
  --bg #050709 · --bg2 #0a0e16 · --bg3 #0f1520 · --surface #141d2e
  --accent #00d4ff (cyan) · --accent2 #0077ee · --gold #f5c842
  --green #00e676 · --violet #a78bfa · --red #f87171
  --text #ddeeff · --muted #5a7a9a · --muted2 #8aa5c0

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## MOTION SYSTEM (12 effects, both pages)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

01 Custom cursor (dot + lagged ring, lerp animation)
02 Page load stagger (fadeUp on .hero-content children)
03 Scroll reveal (IntersectionObserver → .reveal → .visible)
04 Counter animation (easeOutExpo, fires once on scroll-in)
05 Nav scroll (transparent → frosted glass after 60px)
06 Magnetic buttons (.btn-magnetic, mouse-tracking translate)
07 Infinite ticker (marquee, pauses on hover)
08 Card hover (translateY(-6px) + top bar scaleX reveal)
09 Pulse glow button (pulsing box-shadow ring)
10 Floating code block (index.html hero only)
11 Hero background grid (radial gradient + fine grid lines)
12 Section label underline draw (width 0→40px on scroll-in)

Rule: animate ONLY transform and opacity. Never width/height/margin/padding.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## PER-LETTER NAME EFFECT (both pages)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Name: "MD. WAHIDUR RAHMAN PUSON" split into two lines:
  Line 1: "MD. WAHIDUR" (color: --text)
  Line 2: "RAHMAN PUSON" (color: --accent)

JS splits each line into .letter spans on load.
On mouseenter: random color from palette + translateY(-8px) scale(1.15) + glow.
On mouseleave: 120ms linger then reset.
Cursor ring shrinks (scale 0.6) when hovering letters.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## index.html — CHANGE SCOPE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ONE change only:
  Replace existing <h1> with two-line name markup.
  Add .letter CSS + splitNameLetters() JS.
  Touch NOTHING else.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## about.html — PAGE STRUCTURE (8 sections + nav + footer)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

NAV
  Brand: "← Puson.Dev" → links to index.html
  Links: Who I Am · AI & Hardware · App Dev · Farming · Skills · Contact

HERO (single column, 100vh)
  Eyebrow · Name (letter effect) · 3 domain roles · Short bio · 2 CTAs · Domain pills strip

00 — WHO I AM (bg: --bg2)
  Left: 5-paragraph bio | Right: sticky profile card (10 data rows, no age)

01 — AI & HARDWARE (bg: --bg, accent: --accent, left border cyan)
  A: 6 workstation spec cards + 1 cyan callout
  B: "Autonomous AI Agents" heading + 7 agent cards + 1 gold callout

02 — APP DEVELOPMENT (bg: --bg2, accent: --violet, left border violet)
  8 project cards in grid (UltraSave spans 2 cols on desktop):
  UltraSave · Bengali YouTube · Dental Point · Jennah Boutique ·
  Neural-Nexus · Nature's Intimacy · SecureNexus AI · Custom PC Builds

03 — FARMING & AGRI-TECH (bg: --bg, accent: --green, left border green)
  Intro grid (text + farm stats card)
  Infrastructure table (4 rows: 3 cages + store room)
  6 poultry management cards
  BSF 5-step flow (horizontal grid)
  Comparison table (BSF vs Earthworm vs Beetle)
  6 pest control cards
  3 woodcraft cards

04 — SKILLS (bg: --bg2)
  Skill ticker (marquee)
  6 skill group cards: AI · Hardware · Software · Video · Agri-Tech · Business

05 — EXPERIENCE (bg: --bg)
  Timeline — 5 items, NO YEAR LABELS:
  BSc CSE @ BIST · IT Specialist · App Developer · YouTube Creator · Farm Operator

06 — PRICING (bg: --bg2)
  Copy exact pricing tab system from index.html (3 tabs: Websites/Apps/Maintenance)

07 — ROADMAP (bg: --bg)
  6 phase cards — NO specific year/quarter labels:
  UltraSave Launch · Neural-Nexus · Client Scale · BSF+IoT · Australia · BSc Completion

08 — CONTACT (bg: --bg2)
  Copy exact contact section from index.html

FOOTER
  Same as index.html style.
  Center: tagline + "← Back to Portfolio" link to index.html

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## PERSON PROFILE (verified facts only)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Name:         Md. Wahidur Rahman Puson
Location:     Bashabo Kodomtola, Dhaka, Bangladesh
Education:    BSc CSE — BIST (ongoing)
Languages:    Bengali (native) · English (fluent)
Mobility:     Motorcycle + Bicycle
Target:       Australia — IT / AgriTech migration

Domain 1 — IT & Hardware:
  Rig: AMD Ryzen 5 9600X + MSI MAG B850 Tomahawk + Transcend 960GB M.2 + 3TB WD HDD
  Achievements: 500+ FPS Valorant (kernel-level), CMOS crash recovery, 15+ PC builds
  AI agents: Cline, OpenHands, Devin, Google Anti-Gravity, Cursor IDE, ElevenLabs

Domain 2 — App Development:
  Stack: Electron+React+Vite / Flutter+Dart / Next.js / Firebase / Supabase
  Projects: UltraSave (3-platform), Dental Point (client), Jennah Boutique (client),
            Neural-Nexus (SaaS), Nature's Intimacy (blog), SecureNexus AI (pivoted)

Domain 3 — Agri-Tech:
  Poultry: Sonali Classic (RIR×Fayoumi), fermented feed, Neobion supplement
  BSF: self-harvesting sack system, 35–45° ramp, dark bottle, 14–21 day cycle
  Pest control: Fipronil gel, grease barrier, water moat, DIY boric acid
  Wood: Chambul timber, CFT calculation, hand-tool construction

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## COMPONENT QUICK REFERENCE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Buttons:  .btn-primary (cyan fill) · .btn-outline (cyan border) · .btn-magnetic · .btn-pulse
Tags:     .tag-cyan · .tag-gold · .tag-green · .tag-violet · .tag-muted
Badges:   .badge-active · .badge-shipped · .badge-ongoing · .badge-concept
          .badge-client · .badge-research · .badge-live
Callouts: .callout + .callout-cyan/.callout-gold/.callout-green
Cards:    .card (hover lift + top bar scaleX)
Sections: .section-label (JetBrains Mono 10px) + h2 (Bebas Neue clamp) + .section-sub
Reveal:   .reveal → .visible (IntersectionObserver)
Counters: .counter [data-target="N"] [data-suffix="+"]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## JS EXECUTION ORDER (both pages, single <script> end of body)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1  Cursor init + lerp tick
2  Cursor class toggles (interactive / letter / mousedown)
3  Nav scroll handler
4  Hamburger mobile toggle
5  splitNameLetters()
6  IntersectionObserver → .reveal
7  Counter animation
8  Magnetic buttons
9  Pricing tabs
10 Ticker JS fallback
11 Stagger delays (nth-child cards)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## RESPONSIVE BREAKPOINTS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1200px+   Full multi-column, all motions
768-1199  1–2 col grids, hero single col
<768      Hamburger nav, 1-col everything, cursor hidden, hero name clamp(2.8rem,10vw,4.5rem)

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
## FILE REFERENCE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

REPO_CONTEXT.md          → This file. Read first.
PUSON_CURSOR_PROMPT_v2.txt → Full detailed spec for Cursor agent (complete A–Z)

For quick tasks: read REPO_CONTEXT.md only (~60% token savings vs full prompt).
For full build: read PUSON_CURSOR_PROMPT_v2.txt.
