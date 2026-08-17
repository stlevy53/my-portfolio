# Mobile Redesign Plan — Portfolio Site

**Owner:** Stephen Levy
**Goal:** Make the live portfolio site work properly on mobile screens while keeping the desktop design pixel-equivalent to the current site.
**Companion doc:** `PORTFOLIO_SITE_PLAN.md` (original content plan). **Copy source of truth is the current `index.html`** — it contains content updates newer than the plan doc.

---

## How to use this document (for Stephen)

1. Start a new chat with your builder model; attach this file AND the current `index.html`
2. Send the build prompt from Section 6
3. Test the output per Section 7 before replacing `index.html` in GitHub

---

## 1. Diagnosis — why the site breaks on mobile

The current `index.html` is a bundler export with four structural problems:

1. **No viewport meta tag.** Mobile browsers render the page at ~980px virtual width and zoom out — everything looks miniaturized. This is the single biggest cause.
2. **Zero media queries.** Nothing adapts at any screen size.
3. **All styling is inline** (189 `style` attributes) with fixed desktop values — `padding: 80px 56px`, fixed `font-size: 54px` headlines, fixed grid columns. Inline styles cannot be targeted by media queries, so the layout physically cannot respond without restructuring.
4. **Rigid grids:** hero is `1fr 300px`, stat strip is `repeat(3,1fr)`, timeline rows are `96px 1fr`, How I work is `1fr 1fr` — none collapse on narrow screens.

Also broken (fix in the same pass): page `<title>` is "Bundled Page", and there is no meta description, OG tags, or favicon — the SEO spec from the original plan was never implemented. File weight is 1.1MB of bundler scaffolding for what should be a <100KB page.

**Decision: rebuild clean, don't patch.** Converting 189 inline styles inside JS template strings is more work and more error-prone than regenerating a clean, class-based single file with identical content and visuals.

---

## 2. Hard constraints

1. **Desktop appearance is already approved — do not redesign it.** At ≥1024px the rebuilt site must look the same as the current site: same colors, fonts, spacing, section order, copy.
2. **Copy comes from the current `index.html` verbatim** — extract every text string as-is. Do not use older copy from `PORTFOLIO_SITE_PLAN.md` where it differs; the HTML is newer.
3. Single file, no frameworks, no build step, no localStorage. Only external request: Google Fonts.

### Design tokens (as built — keep these, not the teal palette in the original plan)

| Token | Value | Use |
|---|---|---|
| `--bg` | `#0D0C0B` | Page background |
| `--surface` | `#141310` | Cards, expanded case studies |
| `--border` | `rgba(255,255,255,.09)` | Hairlines (also `.08`/`.1` variants — normalize to one) |
| `--text` | `#ECEAE3` | Primary text |
| `--text-body` | `#C6C0B5` | Body copy |
| `--text-muted` | `#9A9488` | Captions, secondary |
| `--accent` | `#F5B841` | Stats, links, chapter labels, emphasis |

Fonts: **Space Grotesk** (headings), **IBM Plex Mono** (labels/dates/chapter tags), body font as currently used. Sticky nav keeps `backdrop-filter: blur(10px)` translucent treatment.

---

## 3. Responsive architecture

- Add `<meta name="viewport" content="width=device-width, initial-scale=1">` — non-negotiable, first fix
- All styles move to one `<style>` block with classes; zero inline styles
- **Mobile-first CSS** with two breakpoints: base (mobile, ≤767px), `@media (min-width: 768px)` (tablet), `@media (min-width: 1024px)` (desktop = current design)
- **Fluid type via clamp()** so text scales between breakpoints instead of jumping. Targets: hero headline `clamp(2rem, 8vw, 3.4rem)` (54px desktop → ~32px mobile); section titles `clamp(1.5rem, 5vw, 2.1rem)`; stats `clamp(1.8rem, 6vw, 2.9rem)`; body stays 16px minimum on mobile (never below — iOS zooms inputs and readability dies)
- Horizontal padding: `56px` desktop → `20px` mobile (use a `--pad-x` variable)
- No horizontal scroll at any width ≥320px: `overflow-x` must never appear

---

## 4. Per-section mobile behavior

**Sticky nav.** Desktop: name left, anchor links right (as now). Mobile: keep it a single row — name left, and either compress the four anchor links into smaller text in one row if they fit at 375px, or show name only. No hamburger menu; the page is one scroll and a hamburger is overhead.

**Hero (`1fr 300px` grid).** Stack to one column on mobile; the 300px right column content moves below the headline block. Reduce top padding from 80px to 40px. CTA buttons go full-width, stacked, 48px min height.

**Stat strip (`repeat(3,1fr)`).** On mobile: single column, stacked with hairline separators (or keep 3-across only if numbers + captions fit at 320px without wrapping awkwardly — they won't; stack them).

**Case study accordions.** Keep the accordion pattern. Mobile adjustments: summary row padding 24px→16px, chevron stays right-aligned, title wraps to two lines cleanly; entire summary row is the tap target (min 48px height). Expanded content: bullets keep 16px text, list padding-left reduced to 18px.

**Timeline (`96px 1fr` rows).** At mobile the 96px year column wastes a quarter of the screen. Stack each row: year as a small mono label above the company line, hairline between entries. Tablet+: restore the two-column grid.

**How I work (`1fr 1fr`).** Single column on mobile, `1fr 1fr` at 768px+.

**Contact.** Buttons/links full-width tap targets, stacked.

**Touch/interaction rules.** All interactive elements ≥44px tap target; accordion animation stays but respects `prefers-reduced-motion`; `IntersectionObserver` reveal animations keep working on mobile (they're cheap) but the initial-hidden state must not leave blank sections if JS fails — content visible by default, JS adds the animation class.

---

## 5. Fix in the same pass (from the original spec, never implemented)

1. `<title>`: Stephen Levy — Product Leader | Game Platforms, Developer Tools & AI
2. Meta description: "Product leader with 25+ years building the platforms that power great games — Microsoft, NCsoft, Amazon, Unity, Zynga. Developer platforms, live services, AI systems."
3. OG tags (og:title, og:description, og:type=website)
4. Inline SVG "SL" monogram favicon
5. Strip all bundler scaffolding — target file weight <100KB excluding fonts

---

## 6. Build prompt (paste to the builder model with this file + current index.html attached)

> Rebuild the attached `index.html` portfolio site as a clean, responsive, single-file `index.html`, following the attached MOBILE_REDESIGN_PLAN.md exactly. Extract ALL text content verbatim from the attached current index.html — the copy is final; do not rewrite a single sentence. Recreate the current desktop design exactly (Section 2 design tokens, same section order, same visual treatment) — at 1024px+ the rebuilt page should be visually indistinguishable from the original. Implement the responsive architecture in Section 3 (viewport meta, mobile-first classes in one `<style>` block, zero inline styles, clamp() fluid type, breakpoints at 768/1024px) and the per-section mobile behaviors in Section 4. Apply the Section 5 fixes (title, meta description, OG tags, SVG favicon, no bundler scaffolding). No frameworks, no build tools, no localStorage; only external request is Google Fonts (Space Grotesk, IBM Plex Mono + current body font). JS limited to: accordion (one open at a time, aria-expanded), smooth anchor scroll, IntersectionObserver reveals that respect prefers-reduced-motion and degrade to visible content without JS. No horizontal scroll at any width from 320px up. Output the complete file.

---

## 7. Acceptance checklist (test before replacing the live file)

- [ ] 375px (iPhone SE/13 mini class): no horizontal scroll, headline readable, stats stacked, timeline stacked, accordions tappable
- [ ] 320px: nothing overflows
- [ ] 768px: two-column How I work, timeline two-column returns
- [ ] 1280px: side-by-side with the old site — visually equivalent
- [ ] Tap every accordion on a phone: opens, closes, only one open
- [ ] All copy diff-checked against old file (extract text from both, compare — zero content changes)
- [ ] Browser tab shows correct title, not "Bundled Page"
- [ ] File size <100KB
- [ ] Then: replace `index.html` in the GitHub repo, commit, hard-refresh the live site on a phone
