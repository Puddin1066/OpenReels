# Men’s Health AI Marketing Studio — Spec

**Status:** design draft (not implemented)  
**Shape:** **all-inclusive monorepo** for AI-driven marketing (content factory + GTM + billing + delivery)  
**Factory engine:** OpenReels pipeline (franchise direction packs + stills-first defaults)  
**Last updated:** 2026-10-19

---

## 1. One-line definition

An **all-inclusive repo** that runs an AI-driven men’s health marketing studio: it **produces** claim-safe educational Shorts (OpenReels), **markets** the studio to clinics (site + outbound/nurture), **sells** pilots/retainers (Stripe), and **delivers** white-label packs — one system, one vertical (TRT / ED / hormones).

**Commercial offer:** productized Shorts retainer (content/video line item), PrimeX-inspired packaging, OpenReels-class automation.

**Not:** a generic multi-vertical SaaS for any industry; a consumer medical advice bot; an AI-testimonial / fake-UGC farm; or “ads-only” creative with no education franchises.

### 1.1 Clarified product thesis

| Layer | Role in the all-inclusive repo |
|-------|--------------------------------|
| **Factory** | OpenReels — franchise Shorts generation |
| **Marketing site** | Studio brand + samples + kit CTA (PrimeX-inspired) |
| **Outreach / nurture** | Sequences to TX/FL clinics + post-lead email |
| **Revenue** | Stripe pilot + subscription |
| **Delivery / ops** | Onboard → approve → pack portal or Drive |
| **Intelligence** | Topic library, hook winners, claim gate |

This is **AI-driven marketing infrastructure for one studio business**, not a thin wrapper that only renders video.

---

## 2. What we sell

| SKU | Deliverable | Price band (guide) | Billing |
|-----|-------------|--------------------|---------|
| **Pilot** | 8 Shorts / 30 days + captions + posting calendar | ~$1,500–$2,500 one-time | Stripe Checkout (one-time) |
| **Retainer** | 12 Shorts / month + captions + calendar + 1 revision round | ~$2,000–$3,500 / mo | Stripe Subscription |
| **Agency wholesale** | White-label pack (no clinic sales) | ~$1,000–$2,000 / mo | Stripe or invoice |

**Budget line on the clinic P&L:** Content marketing / video production / social creative — **not** media buy, not full SEO retainer, not website build.

**Success metric for clinics:** attributable consults / lower CAC over time — not vanity views. Benchmark context: blended TRT CAC often ~$175–$325 per active patient; organic SEO CAC ~$50–$150 at scale.

---

## 3. Market

### 3.1 Category

Private / cash-pay **men’s health clinics** (TRT, ED, hormone therapy). Paid ads for testosterone / hormones / sexual health are often restricted → organic education, local SEO, and reviews do durable acquisition work.

### 3.2 Members

| Role | Relation |
|------|----------|
| Clinic owner / medical director | Buyer; signs off claims posture |
| Marketing director / practice manager | Day-to-day buyer at larger sites |
| Full-stack men’s health agencies | Adjacent competitor **or** wholesale partner |
| SEO specialists | Adjacent; studio complements article SEO with Shorts |
| End patient (man 28–55) | Audience, not payer |

### 3.3 Buyer universe (order of magnitude)

- ~2,000+ cataloged US TRT / hormone clinic locations (directory-dependent)
- Service SAM (Shorts/content line): roughly **tens of millions USD / year** US — niche B2B, not mass SaaS TAM
- SOM for early stage: 2–5 retainers → ~$5K+/mo revenue is attainable without market saturation

### 3.4 Positioning

> Compliant organic Shorts for ad-constrained men’s clinics.

Complement agencies; do not claim to replace ads + SEO + CRM + phones.

---

## 4. Geography

### 4.1 Beachhead

**Sun Belt brick-and-mortar / hybrid clinics — Texas + Florida mid-metros first**  
(e.g. San Antonio, Fort Worth, Jacksonville, Tampa, Orlando — not only Miami / Dallas megas).  
Then AZ / CO / TN corridors.

### 4.2 Intrinsic reasons (beyond clinic count)

1. **Local “near me” + GBP** — place-based clinics win map pack; localized Shorts support that. Pure telehealth does not get the same map-pack lever.
2. **Hybrid / in-person TRT norms** in TX/FL-style markets favor physical clinics that need local patient education.
3. **Cash-pay unit economics** support a content line item tied to consult LTV.
4. **Mid-metro CAC** — tier-2 markets often cheaper to prove ROI than coastal tier-1.
5. **Less coastal agency saturation** than NYC / SF / LA as a first sales beachhead.

### 4.3 Defer

- National DTC telehealth giants as primary customers  
- NYC / LA / SF as first outbound corridor  

### 4.4 Rollout

| Phase | Geo |
|-------|-----|
| 0–30d | Library only (no geo sales) |
| 30–60d | One TX **or** FL mid-metro cluster |
| 60–90d | Adjacent cities, same state |
| Month 4+ | Second Sun Belt state |

---

## 5. Content formats (locked)

Only these franchises. No AI-generated patient testimonials.

| ID | Structure | Ending | Claim tier |
|----|-----------|--------|------------|
| `myth_bust` | Myth → why believed → truth → one action → recap | Recap card (not “comment below”) | lifestyle / evidence |
| `listicle_3` | Hook → agitate → 3 items ascending → recap | Numbered summary | lifestyle |
| `protocol` | Hook → problem → ordered steps → soft proof → checklist | Checklist card | lifestyle |
| `what_to_expect` *(optional 4th)* | First visit / labs / process | Soft book CTA | commercial-intent, low claim |

### 5.1 Explicitly out of scope

- AI avatar / synthetic “patient” testimonials  
- Fabricated before/after body or hormone-level results  
- Hard drug/TRT outcome promises  
- Unattended auto-posting of medical advice  

### 5.2 Content production model (automated + dashboard)

**Default: fully automated.** Franchise + topic card (+ clinic brand kit) → OpenReels batch → claim queue → deliver/publish.

**Enrichment / custom: dashboard-specified.** Operators (studio staff; later clinic users with limits) use a production dashboard to override and enrich before or after draft generation — without leaving the monorepo.

| Dashboard control | What it does |
|-------------------|--------------|
| Pick franchise + topic | Or create ad-hoc brief from template |
| Edit / generate hooks | Lock 1 of N; regenerate losers |
| Brand kit | Logo, colors, voice, `{{clinic}}` / city / booking URL |
| Script & beat overrides | Rewrite scene lines; pin beat roles |
| Asset inject | Upload B-roll, MD VO, logo sting, permissioned review quote text |
| Claim tier + footnotes | Force lifestyle vs evidence; require disclaimer |
| Preview / approve / re-render | Human gate stays in-dashboard |
| Schedule | Studio channel or clinic pack slot |

**Social proof as enrichment (not a separate manual SKU):** real MD/NP VO, permissioned review quotes, process-journey beats, and clinic tour stills are **injected via the dashboard** into the automated pipeline. Synthetic AI patient testimonials remain forbidden.

### 5.3 Visual / production defaults

- Archetype: start `infographic`; later `mens_health_clinical`  
- **Stills-first**; `ai_video` off or ≤1 scene  
- On-screen hook text required in first 1–3s  
- Prefer `text_card` + stock/AI stills + Ken Burns  
- Fast pacing (roughly 7–10 scenes)  
- Localization variables: `{{clinic}}`, `{{city}}`, `{{booking_url}}`

### 5.4 Topic card (library atom)

Each evergreen topic stores: franchise, 5 hooks, body beats, recap, claim_tier, clinic CTA variants, SEO slug, status (`draft` / `approved` / `winning`).

**Gate before heavy sales:** 30 approved topic cards · 90 hooks · 12+ public studio Shorts · 20 winners logged with retention notes over time.

---

## 6. Dual-use content system

| Skin | Audience | CTA | Brand |
|------|----------|-----|-------|
| Studio channel | Men + clinic marketers | Soft education; “clinics: get the kit” | Studio brand |
| Clinic white-label | Local patients | Book / private consult | Clinic logo, city, optional MD |

Public channel = demo reel + inbound. Same library instantiates client packs.

---

## 7. Automated full cycle (+ dashboard enrichment)

```
Topic backlog ──► (optional dashboard enrich) ──► batch OpenReels render
        │                                              │
        │         dashboard: hooks, brand, assets,     ▼
        │         script pins, claim tier          claim gate (in UI)
        │                                              │
        └──────────────────────────────────────────────┼──► publish / deliver
                                                       │
                              nurture & onboard ◄──────┘
                              monthly refresh → performance → library
```

| Stage | Automate | Dashboard / human |
|-------|----------|-------------------|
| Library & hooks | Templates, backlog, AI draft hooks | Enrich topics; approve medical-adjacent |
| Produce | OpenReels batch (default path) | Specify custom brief, pins, injected assets |
| Gate | Rubric checks surfaced in UI | Claim / compliance approve or reject |
| Studio publish | Scheduler | Spot-check / reschedule |
| Lead → nurture | Form + 5-touch email | Sales call for pilots |
| Onboard | Brand kit → job config | Kickoff; kit edits in dashboard |
| Deliver | Pack to portal | Optional clinic MD approve in dashboard |
| Bill | Stripe pilot + subscription + dunning | Exceptions |
| Learn | Topic × retention metrics | Promote / kill topics |

**Production is automated by default; customization is dashboard-driven.**  
**Never auto-publish:** unreviewed clinical claims or synthetic patient testimonials.

---

## 8. Two-repo architecture (studio product + OpenReels engine)

**Decision:** Do **not** turn the public OpenReels repo into the commercial studio.  
**Studio** = private product monorepo. **OpenReels** = OSS component, thinly adapted for men’s-health franchises.

```
┌──────────────────────────────────────────────────────────┐
│  mens-health-marketing-studio  (NEW private GitHub repo) │
│  marketing · dashboard · Stripe · claim ops · GTM hooks  │
│  packages/franchises (business IP topic cards)           │
└───────┬───────────────────────────────┬──────────────────┘
        │ depends on / calls            │ API / webhooks
┌───────▼──────────────┐    ┌───────────▼──────────────────┐
│  OpenReels (OSS)     │    │  External GTM (do not build) │
│  Shorts factory      │    │  Clay (find/enrich/persona)  │
│  + franchise PRs     │    │  Instantly (engage/send)     │
└──────────────────────┘    └──────────────────────────────┘
```

### 8.0 Studio monorepo layout

```
apps/
  web/                 # Marketing site + production dashboard + clinic portal
  api/                 # Jobs, Stripe, Clay/Instantly webhooks, CRM writeback
  worker/              # Thin runner that invokes OpenReels (submodule, package, or HTTP)
packages/
  franchises/          # Direction packs, claim rules, topic cards (studio IP)
  gtm/                 # Thin adapters: ICP filters, copy vars, webhook handlers
                       #   — NOT a sequencer. Clay + Instantly own find+engage
  billing/             # Stripe products, dunning hooks
  shared/              # Types, brand kit schema, localization vars
specs/
  mens-health-production-studio.md   # this document (source of truth)
vendor/ or submodule/
  openreels/           # optional pin of OpenReels
```

**`apps/web` roles:**
1. Public studio marketing site (PrimeX-inspired)  
2. **Production dashboard** — create/enrich jobs, brand kits, asset inject, approve, re-render  
3. Clinic portal — view/approve packs, invoices (when retainers need it)

**OpenReels adaptations (stay upstream-friendly):**
- Franchise / direction pack injection (`myth_bust`, `listicle_3`, `protocol`)  
- Critic: on-screen hook, recap ending, claim-tier hooks  
- Optional clinical archetype + stills-preferred defaults  
- Stable CLI/API for the studio worker to call  

**Studio-only (never merge into public OpenReels):**
- Stripe, clinic CRM, brand kits with customer data  
- Production dashboard auth  
- Commercial topic library / compliance SOPs  
- GTM adapters + ICP definitions (geo, “has Instagram”, cash-pay TRT/ED)

### 8.0.1 GTM stack — use existing tools (do not build a sequencer)

**Decision:** Do **not** ship first-party cold-email / lead-scrape infrastructure (seqd, TriggerStack clones, custom Maps scrapers). That is commodity GTM; the studio’s edge is **content production**, not another Instantly.

| Layer | Tool | Job |
|-------|------|-----|
| **Find + enrich + personalize** | **Clay** (primary) | Maps/local + Apollo waterfall, Claygent research (IG active? owner email?), AI personalization vars |
| **Engage / send / warmup** | **Instantly** (primary; Smartlead OK) | Sequences, inbox rotation, reply inbox |
| **Optional all-in-one local** | Openmart | If Clay data is thin on owner-ops clinics — local SMB find+send without building scrapers |
| **Studio owns** | `packages/gtm` + `apps/api` | ICP filter defs, sequence *copy* templates, Instantly/Clay webhooks → CRM stage, “attach sample pack” trigger |

**Why this stack (2026 cutting edge for this ICP):**
- Men’s clinics are **local owner-ops**, not LinkedIn-heavy SaaS — Apollo alone is weak; Clay (waterfall + Claygent) or Openmart fixes find quality  
- Instantly/Smartlead is where deliverability and engage loops live — rebuilding that is wasted runway  
- Studio loop: Clay table (TX/FL TRT/ED + IG signal) → Instantly campaign → reply webhook → human close → Stripe → OpenReels fulfillment  

**Explicit non-build:** no in-repo SMTP sequencer, no Maps scraper product, no “agency toolkit” to resell.

### 8.1 Revenue cycle

```
Lead → Pilot (one-time Stripe) → Onboard → Retainer (Stripe subscription)
    → Deliver monthly → Expand locations/kits → Renew
```

| Stage | Enabled by |
|-------|------------|
| Attract | `apps/web` + studio Shorts channel + lead magnet |
| Find + engage | **Clay + Instantly** (via `packages/gtm` hooks) |
| Convert | Stripe Checkout / Subscription in `packages/billing` |
| Fulfill | `worker` OpenReels batch + brand kit injection |
| Gate | Claim review queue (human) before publish/deliver |
| Retain | Monthly job scheduler + Customer Portal |

### 8.2 What “AI-driven” means here

- AI generates franchise Shorts, hooks, and topic drafts  
- Clay/Claygent + Instantly AI assist personalization of outreach (clinic name/city/IG angle) — **outside** this repo’s core  
- Humans own **claim approval** and sales close  
- No AI fake patient testimonials; no unattended clinical advice bots  

### 8.3 Pause rule

If invoice unpaid past grace → pause production jobs automatically.

---

## 9. OpenReels adaptation (implementation phases)

| Phase | Work | Code? | Exit criteria |
|-------|------|-------|---------------|
| **0** | Direction packs for 3–4 franchises + compliance one-pager + runbook; run with `--direction` + `infographic` + stills-first | No / minimal | 12 public Shorts; better retention vs freeform |
| **1** | `--franchise`, playbook/critic: on-screen hook, recap ending, claim checks | Yes, small | Critic rejects soft CTAs / banned claims |
| **2** | `mens_health_clinical` archetype; stills-preferred flag | Yes, small | Visual consistency; lower COGS |
| **3** | Hook batch CLI (`--hooks-file` + score replay) | Yes, medium | 5 hooks × 1 body in one command |
| **4** | `visuals_only` + external VO / Whisper (hybrid host) | Yes, medium | Class B Shorts |
| **5** | Batch API for agency wholesale | Yes, larger | White-label retainers |

Reuse existing: `--direction`, `--score` replay, critic loop, Remotion assembly, cost estimator.

---

## 10. Compliance gate

- Claim tiers: `lifestyle` | `evidence` | `medical` (`medical` = no auto-publish)  
- Banned: cure language, unsubstantiated T%/weight claims, diagnose-the-viewer, fake patient results  
- Footer: “Not medical advice.”  
- Clinic MD review optional but recommended for service-line claims  
- Platform policy: prefer education over offer-forward hormone ads  

---

## 11. Non-goals

- Multi-vertical expansion before TX/FL playbook works  
- Consumer chatbot that gives medical advice  
- AI patient testimonials as a productized format  
- Custom fine-tuned video ML runway before format-market fit  
- Building a **generic** multi-tenant “marketing SaaS for any niche” before the men’s clinic studio works  
- Replacing the clinic’s entire marketing agency (we supply Shorts + GTM for *our* studio; clinics may still have SEO/ads partners)  
- Reselling cold-email / lead-gen infrastructure as the product (Clay + Instantly are vendors; we are not Instantly)  
- Building an in-repo sequencer or Maps scraper (commodity — buy Clay/Instantly/Openmart)  

---

## 12. 90-day operating checklist

1. Lock franchise direction packs (Phase 0)  
2. Ship 12 studio Shorts; instrument retention  
3. Lead magnet: “12-Short Men’s Clinic Starter Kit” (watermarked)  
4. Stripe pilot + retainer products live  
5. Clay table + Instantly campaign live for **one** TX or FL mid-metro cluster  
6. Close 2–3 pilots → convert ≥1 retainer  
7. Feed winners into library; only then consider Phase 1 code  

---

## 13. References (market context)

- Men’s clinic marketing organic-first / ad restrictions — industry agency pages (e.g. Click Track)  
- TRT CAC & SEO content $2–5K/mo — LUKE Health patient acquisition benchmarks  
- Clinic directories / density — trtmap, TRT Index  
- Doctor video retainers ~$3–10K/mo — specialty video studio pricing  
- Content studio vs full agency scope — healthcare creative industry comparisons  
- Local “near me” / map pack vs telehealth state pages — hormone clinic SEO playbooks  

---

## 14. Decision log

| Decision | Choice |
|----------|--------|
| Product type | All-inclusive **AI marketing monorepo** operating a men’s health Shorts studio |
| Commercial SKU | Productized retainer (PrimeX-inspired), not seat-based SaaS |
| Primary format set | myth_bust, listicle_3, protocol (+ optional what_to_expect) |
| AI testimonials | Rejected as core format |
| Revenue | Stripe pilot + subscription |
| Repo shape | **Two repos:** private studio monorepo + OpenReels OSS component |
| Customer-facing web | Marketing site + **production dashboard** + clinic portal (studio) |
| Content production | Automated by default; dashboard for enrich / custom specify |
| Find + engage | **Clay + Instantly** (optional Openmart); studio only owns thin GTM adapters |
| Geo | TX/FL mid-metros first |
| Factory | OpenReels (adapted), stills-first, franchise packs |
