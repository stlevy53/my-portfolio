# Portfolio Site — Build Plan & Copy Deck

**Owner:** Stephen Levy
**Purpose:** One-page portfolio site supplementing the resume for a VP-level product search (Netflix, Epic, Valve, Discord, Pinterest tier).
**Audience:** Recruiters, hiring managers, and execs who spend <90 seconds on first pass. The site must earn a second pass.
**This document contains everything a builder (human or AI) needs: final copy, design system, technical spec, hosting steps, and a ready-to-paste build prompt.**

---

## How to use this document (for Stephen)

1. Start a new chat with your builder model and attach or paste this entire file
2. Send the build prompt from Section 7 as your message
3. Review the output at 375px and 1280px widths before committing
4. Follow Section 5 to publish on GitHub Pages

**Builder note:** Only Section 2 contains page content, rendered verbatim. Sections 1, 3, and 4 are specifications. Sections 5, 6, and 8 are reference for Stephen only — nothing in them appears on the site. Section 6 in particular contains non-public information that must never be rendered.

---

## 1. Positioning

One through-line across 25 years: **Stephen builds the platforms and systems that power great games** — from Xbox 360 launch operations to Guild Wars 2 publishing to Twitch Prime growth to Unity multiplayer to Zynga's developer platforms and AI tooling.

The site is not a resume reprint. It's a narrative with proof:

1. **Hero** — who he is in one line, with the strongest numbers up front
2. **Career narrative** — the arc, in 3 short paragraphs
3. **Selected work** — 4 case studies with outcomes
4. **Career timeline** — the full 25-year strip, compressed
5. **How I work** — operating principles, not a skills word-cloud
6. **Contact** — email + LinkedIn

Tone: executive register. Confident, compressed, outcome-framed. No buzzwords, no filler, no "passionate about synergies." Every claim carries a number or a name.

---

## 2. Copy Deck (final copy — paste as-is)

### 2.1 Hero

**Headline:** I build the platforms that power great games.

**Subhead:** Product leader with 25+ years across Microsoft, NCsoft, Amazon, Unity, and Zynga — shipping developer platforms, live services, and AI systems that studios and millions of players depend on.

**Proof strip (3 stats, displayed as large numbers):**

- **300%** Twitch Prime membership growth — #2 acquisition driver for Amazon Prime
- **90%** reduction in deployment lead time across Zynga studios
- **3M** Guild Wars 2 units sold in six months as Global Director of Publishing

**CTA buttons:** [View selected work] (anchor scroll) · [Get in touch] (anchor scroll)

### 2.2 Career narrative ("The through-line")

**Section title:** The through-line

Every role I've held comes down to the same job: take a complex system — a console launch, an MMO publishing operation, a multiplayer platform, a build pipeline — and turn it into something teams can actually use to ship great games.

I started at Microsoft owning operational launch for Xbox 360, built NCsoft West's publishing function for Guild Wars 2, and grew Twitch Prime into Amazon Prime's second-largest acquisition channel. Then I went deep on the developer side: multiplayer services at Unity, fintech tooling for studios at Sanlo, and now Zynga's Systems organization — the platform team behind build pipelines, cloud infrastructure, and AI-powered developer tools for every Zynga studio.

Along the way I co-founded a hardware startup and drove its Kickstarter to 640% of goal, and built and sold Washington's largest indoor golf business. I like hard, ambiguous problems, small teams with big mandates, and measurable outcomes. That hasn't changed in 25 years.

### 2.3 Case studies ("Selected work")

**Section title:** Selected work
**Format:** 4 cards. Each card shows title + one-line outcome; clicking/tapping expands to the full case study (accordion or modal — accordion recommended). Each case study follows Context → What I did → Results.

---

#### Case study 1 — Zynga: Platform transformation, then a turnaround

**Card summary:** Rebuilt Zynga's developer platforms (90% faster deployments, 80%+ cost reduction), then was asked to take over a struggling Tools organization and get it shipping.

**Context.** I joined Zynga as Director of Product Management leading the Systems team — the internal platform organization behind build pipelines, cloud infrastructure, and AI-powered developer tools for every studio. In early 2026, leadership asked me to move to the Tools organization: three product pods that were struggling to execute and needed to get back on track.

**Chapter 1 — Systems: replatforming how studios build games.**

- Unified core developer platforms — CI/CD, Kubernetes, GitHub Enterprise, Artifactory — into a shared foundation, cutting deployment lead time **90%** and reaching **85% cross-studio adoption**
- Replaced **30 manual DevOps processes** with automated, self-service workflows — build cycle time down **25%**, build costs down **more than 80%**
- Built an AI-powered knowledge base synthesizing meeting transcripts, Slack, and Jira into a unified customer view — **300+ signals captured in three months, adopted by 18 PMs and expanding to 38 more** — and trained the PM org on AI-augmented workflows for market analysis, requirements, and prototyping

**Chapter 2 — Tools: the turnaround mandate.**

The Tools portfolio spans three product pods: customer support tooling, player engagement and cross-game messaging, and game operations — including the localization platform serving Zynga's entire portfolio of live games.

- Shipped the localization platform's GA on schedule within **ten weeks** of taking over — after a two-year development history — by resetting scope, timeline discipline, and stakeholder trust
- Instituted decision hygiene the teams lacked: documented build-vs-buy frameworks, requirements sign-off before engineering evaluation, one-pagers with business rationale at kickoff
- Reset roadmaps and priorities across all three pods, replacing analysis paralysis with clear decision deadlines
- Built AI-driven machine translation into the localization pipeline, materially reducing translation costs across the portfolio
- Own the messaging platform handling **96% of all player engagement messages** across the Zynga portfolio

---

#### Case study 2 — Amazon: Making Twitch Prime a growth engine

**Card summary:** Grew Twitch Prime membership 300%, making it the #2 acquisition driver for Amazon Prime.

**Context.** Twitch Prime (now Prime Gaming) was a young benefit inside the Amazon Prime ecosystem. I owned member experience — every feature designed to acquire and retain members.

**What I did.**

- Built the member experience roadmap from data-driven insight loops: instrument, learn, ship, repeat
- Launched **Free Games with Prime**, the program that gave the benefit a recurring, tangible hook
- Aligned product, marketing, and partnerships across two large organizations (Amazon and Twitch) with different cultures and metrics

**Results.**

- **300%** membership growth; Twitch Prime became the **#2 acquisition channel** for the entire Prime program
- Free Games with Prime drove **+300 bps** in member conversion and **+250 bps** in retention

---

#### Case study 3 — Unity: Multiplayer as a platform product

**Card summary:** Scaled Unity's multiplayer platform past 100 partner teams and cut studio integration time 30%.

**Context.** Multiplayer is one of the hardest things a game team builds. At Unity I owned product strategy and roadmap for Multiplayer Services — matchmaking, lobby, and relationship APIs — plus AI-driven LiveOps analytics.

**What I did.**

- Delivered major upgrades to matchmaking, lobby, and relationship APIs with developer workflow as the first-class requirement: simpler setup, testing, and deployment
- Ran targeted betas and developer engagement programs to grow platform adoption
- Launched a Trust & Safety initiative using AI/ML to combat toxicity in games and online communities
- Drove the Sentis AI product through rapid iteration with **2,000+ beta users**

**Results.**

- Platform adoption grew past **100 partner teams**
- Studio integration time down **30%**
- New LiveOps analytics shipped, giving teams real-time insight into player behavior and retention

---

#### Case study 4 — NCsoft: Publishing Guild Wars 2

**Card summary:** Built NCsoft West's publishing function and launched Guild Wars 2 — 3M units in six months, $50M in presales.

**Context.** NCsoft West was newly formed and had no publishing function. Guild Wars 2 — one of the most anticipated MMOs ever — needed release management, QA, customer support, ecommerce, and monetization built from scratch.

**What I did.**

- Created the publishing organization: release management, quality assurance, and customer support for new MMORPG titles
- Owned the ecommerce platform and first-party digital sales targets, including payment provider strategy
- Developed the presale strategy and monetization model for launch, building on the playbook that generated $20M in presales for Aion

**Results.**

- **$50M** in gross presales before launch
- **3M+ units** sold in the first six months; Best PC MMORPG of 2012
- Publishing function became the operating model for NCsoft West titles

---

**Alternate case study — NOT in the v1 build. Kept here in case Stephen swaps it in later:**

#### Coros: Zero to one, hardware edition

**Card summary:** Co-founded a hardware startup — Kickstarter funded at 640% of goal, top 1% of all-time funded projects.

**Context.** Co-founded Coros Wearables as COO & Head of Product, owning all product and business operations for the launch of the LINX smart cycling helmet.

**What I did.** Drove product definition across hardware, mobile app, and platform; built logistics, supply chain, and customer support from nothing; adapted strategy in real time against live crowdfunding performance.

**Results.** Kickstarter funded at **640% of goal** (top 1% all-time); Interbike **"Gear of the Show"** — one of five awards among 1,400 brands; featured by GeekWire and Triathlete.

---

### 2.4 Career timeline

**Section title:** 25 years, one arc
**Format:** Compact vertical timeline or horizontal strip. One line per role. No bullets under each — the case studies carry the depth.

| Years | Company | Role | One-liner |
|---|---|---|---|
| 2024– | **Zynga** | Director of Product Management | Rebuilt developer platforms; now leading a multi-pod Tools org turnaround |
| 2024 | **Sanlo** | Head of Product, Gaming | Series A fintech; webshop margins +30% |
| 2021–24 | **Unity** | Senior Manager, Product Management | Multiplayer Services; 100+ partner teams |
| 2021 | **Age of Learning** | Director of Product Management | Education gaming portfolio |
| 2019–20 | **Big Fish Games** | Director of Product Management | $30M+/month mobile game portfolio |
| 2017–19 | **Amazon** | Senior PM, Twitch Prime | 300% growth; #2 Prime acquisition driver |
| 2016 | **Coros** | Co-founder, COO & Head of Product | Kickstarter at 640% of goal; Gear of the Show |
| 2013–19 | **Clubhouse Golf Center** | Owner | Built and sold WA's largest indoor golf business |
| 2012–13 | **Meteor Entertainment** | Chief Publishing Officer | Publishing org for Hawken F2P launch |
| 2009–12 | **NCsoft** | Global Director of Publishing | Guild Wars 2: 3M units, $50M presales |
| 2001–09 | **Microsoft** | Senior Product Manager | Xbox 360 launch ops; first B2C hardware business (Zune) |

**Footer line under timeline:** Before tech: US Army and Army Reserves (honorable discharge) · Snohomish Fire Department, Firefighter/EMT. B.A. Psychology & Business Administration, Western Washington University. PMP certified.

### 2.5 How I work

**Section title:** How I work
**Format:** 4 short principles, prose-first, no icons needed.

**Outcomes over output.** Every roadmap item traces to a business result. If we can't measure it, we haven't defined it yet.

**Platforms are products.** Internal developer tools deserve the same discovery, design, and iteration rigor as anything customer-facing. Developer experience is the multiplier on everything a studio ships.

**AI is a workflow, not a feature.** I've built AI product strategy from both sides — shipping AI-powered products and transforming how teams work with AI. The teams that win treat it as an operating model change. Most recently: an AI knowledge base that turns meeting transcripts, Slack, and Jira into a single customer view my PM org works from daily.

**Narrative first.** Strategy that can't be told as a story won't survive contact with an exec team. I write the press release before the roadmap.

### 2.6 Contact

**Section title:** Get in touch

Open to conversations with leaders and teams shaping the future of game development and technology.

- **Email:** slevy53@live.com (mailto link)
- **LinkedIn:** linkedin.com/in/stephenlevy (opens new tab)

No phone number. No contact form (avoids backend/spam).

### 2.7 Meta / SEO

- `<title>`: Stephen Levy — Product Leader | Game Platforms, Developer Tools & AI
- Meta description: "Product leader with 25+ years building the platforms that power great games — Microsoft, NCsoft, Amazon, Unity, Zynga. Developer platforms, live services, AI systems."
- OG tags: same title/description; og:type website. OG image optional v1 (can add a simple branded card later).
- Favicon: simple "SL" monogram SVG, inline data URI is fine.

---

## 3. Design System — "Executive minimal, dark accent"

**Feel:** Confident, typography-led, quiet gaming undertone. Think senior-exec personal site, not agency portfolio. Nothing neon, nothing animated for its own sake.

### Colors

| Token | Value | Use |
|---|---|---|
| `--bg` | `#0E1116` | Page background (near-black, slightly blue) |
| `--surface` | `#161B22` | Cards, timeline rows, expanded case studies |
| `--border` | `#262D37` | Hairline borders, dividers |
| `--text` | `#E6EAF0` | Primary text |
| `--text-muted` | `#98A2B3` | Secondary text, dates, captions |
| `--accent` | `#4FD1C5` | Stats, links, hover states, section markers (teal — distinctive without being gamer-neon) |
| `--accent-dim` | `#2C7A73` | Accent hover/pressed |

### Typography

- **Headings:** Inter (Google Fonts), weights 600/700, tight letter-spacing (-0.02em). Hero headline ~clamp(2.2rem, 5vw, 3.5rem).
- **Body:** Inter 400/500, 1.05rem, line-height 1.65, max-width 68ch.
- **Stats/numbers:** Inter 700, oversized (2.5–3rem), accent color.
- One font family total. No serif, no display font.

### Layout & behavior

- Single column, max-width 1040px, generous vertical rhythm (96–128px between sections).
- Sticky top nav: name left, anchor links right (Work · Timeline · About · Contact). Collapses to nothing fancy on mobile — just the name; the page is one scroll.
- Case studies: accordion cards. Summary row always visible (title + one-line outcome + expand chevron). Expand animates height; only one open at a time.
- Subtle entrance: sections fade/translate up 12px on first scroll into view (IntersectionObserver, `prefers-reduced-motion` respected).
- Fully responsive; test at 375px, 768px, 1280px.
- Accessibility: semantic landmarks, buttons for accordions with `aria-expanded`, contrast AA minimum, keyboard navigable.

---

## 4. Technical Spec

- **One file:** `index.html`. All CSS in a `<style>` block, all JS in a `<script>` block. Only external request: Google Fonts (Inter). No frameworks, no build step, no analytics v1.
- **No** localStorage, no forms, no backend.
- JS scope: accordion toggle, smooth anchor scrolling, IntersectionObserver entrance animation. ~60 lines max.
- Semantic HTML: `header`, `main`, `section` with `id`s matching nav anchors, `footer`.
- Total page weight target: <100KB excluding fonts.

---

## 5. Hosting Recommendation — GitHub Pages (free)

**Why:** Free, no ads, custom-domain capable, versioned, zero maintenance, and hosting your portfolio in your own GitHub account is itself a small credibility signal. Alternatives (Cloudflare Pages, Netlify free tier) are equally good but add an account; GitHub Pages uses what you have.

**Launch steps:**

1. Create a public repo named `stephenlevy.github.io` (this exact name makes the site the account root: `https://stephenlevy.github.io` — adjust to your actual GitHub username)
2. Commit `index.html` to `main`
3. Repo Settings → Pages → Source: `main` branch, root folder → Save
4. Site is live at `https://<username>.github.io` within ~2 minutes
5. **Optional custom domain (recommended for a VP search):** buy `stephenlevy.com` or similar (~$10/yr, Cloudflare Registrar or Namecheap), add it in Pages settings, create the CNAME/A records the settings page specifies. HTTPS is automatic.
6. Add the URL to LinkedIn (Contact info + Featured section) and the resume header.

---

## 6. Verification Log — all items resolved (July 3, 2026)

**PRIVATE — none of this section appears on the site.** The resume and LinkedIn disagreed on several numbers. All resolved with Stephen; log kept for reference:

1. ~~**Coros:**~~ RESOLVED (revised Jul 2026) — 640% of goal; Co-founder, COO & Head of Product per updated resume. Update LinkedIn to match (currently 600%, Head of Product & Business Ops, no co-founder).
2. ~~**Presales:**~~ RESOLVED — both are real. GW2 did $50M, Aion did $20M; copy now references both.
3. ~~**Clubhouse Golf:**~~ RESOLVED — numberless. Reconcile the $1.2M vs $3M discrepancy between resume and LinkedIn separately.
4. ~~**Big Fish dates:**~~ RESOLVED — 2019–20, consistent with both sources.
5. ~~**Zynga internal tool names:**~~ RESOLVED — all internal names (LaunchPad, Mercury, LocManager) and internal metrics removed. Pods described by function only. Keep specifics for interviews, not the public site.
6. ~~**LocManager GA:**~~ RESOLVED — shipped on time, June 2026. Copy claims "ten weeks" without naming the tool. Full story is interview material.
7. ~~**Messaging and customer-support pods:**~~ RESOLVED — added "96% of all player engagement messages" bullet (cleared by Stephen). Held back for interviews only: 86M messages/day across six channels — do not publish without clearance.
8. ~~**Age of Learning:**~~ RESOLVED — keep in timeline. Consider adding it to the resume for consistency.

---

## 7. Build Prompt (paste this to the builder model along with sections 2–4)

> Build a single-file `index.html` personal portfolio site exactly per the attached plan document. Use the copy in Section 2 verbatim — do not rewrite, expand, or "improve" it. Include exactly 4 case studies (Zynga, Amazon, Unity, NCsoft); omit the optional Coros case study — Coros appears only in the timeline and narrative. Render nothing from Sections 1, 5, 6, 7, or 8 — they are instructions and private reference, not page content. Implement the design system in Section 3 exactly (colors as CSS variables, Inter from Google Fonts, spacing and layout as specified). Follow the technical spec in Section 4: no frameworks, no build step, no localStorage, all CSS/JS inline. Sections in order: sticky nav, hero with 3-stat proof strip, "The through-line," "Selected work" (4 accordion case studies, one open at a time, aria-expanded on buttons), "25 years, one arc" timeline, "How I work," "Get in touch," minimal footer ("© 2026 Stephen Levy"). Bold markdown (**text**) in the copy becomes emphasized/accent-colored text, not literal asterisks; the timeline markdown table becomes styled HTML (or stacked rows on mobile), not a raw table dump. Smooth anchor scrolling and IntersectionObserver fade-in entrances respecting prefers-reduced-motion. Fully responsive at 375/768/1280px, semantic HTML, AA contrast. Include the meta/OG tags from Section 2.7 and an inline SVG "SL" favicon. Output the complete file.

---

## 8. Post-Launch (later, not v1)

- OG share image (1200×630 branded card) — improves LinkedIn link previews
- Custom domain (Section 5, step 5)
- Optional "Writing" section if LinkedIn thought-leadership content grows
- Lightweight analytics (GoatCounter or Cloudflare Web Analytics, both free, no cookies) if you want traffic visibility
