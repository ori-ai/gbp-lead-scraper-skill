# SKILL: GBP Local Service Lead Scraper

## Every lead generation run MUST follow ALL phases below. This is non-negotiable.

This skill discovers unoptimized Google Business Profiles for local service businesses across the US, audits them on 18 weighted optimization signals, maps them to service tiers with pricing, generates conversion-ready outreach with AI agent handoff scripts, and logs everything to CRM.

Built by ClearOps AI (getclearops.io) — AI-Managed Growth Infrastructure for Local Service Businesses.

---

## PHASE 1: TARGET SELECTION

Each run targets ONE vertical in ONE city. Cycle through all combinations systematically.

### Target Verticals (Priority Order)

1. HVAC companies
2. Plumbing companies
3. Personal injury law firms
4. Dental practices and DSO groups
5. Med spas and aesthetics clinics
6. Property management companies
7. Real estate brokerages
8. Immigration law firms
9. Home inspection companies
10. Luxury auto dealerships
11. Franchise systems (any vertical)
12. General contractors and builders
13. Locksmith services
14. Door repair and security companies
15. Speech therapy and healthcare practices
16. Roofing companies
17. Electrical contractors
18. Pest control companies
19. Landscaping and hardscaping companies
20. Auto body and collision repair shops

### US City Tiers

**Tier 1 — Top 25 metros (run weekly, highest volume):**
New York, Los Angeles, Chicago, Houston, Phoenix, Philadelphia, San Antonio, San Diego, Dallas, Austin, Jacksonville, San Jose, Fort Worth, Columbus, Charlotte, Indianapolis, San Francisco, Seattle, Denver, Nashville, Washington DC, Oklahoma City, El Paso, Boston, Portland

**Tier 2 — Next 50 metros (run bi-weekly):**
Las Vegas, Memphis, Louisville, Baltimore, Milwaukee, Albuquerque, Tucson, Fresno, Mesa, Sacramento, Atlanta, Kansas City, Omaha, Colorado Springs, Raleigh, Long Beach, Virginia Beach, Miami, Oakland, Minneapolis, Tampa, Tulsa, Arlington, New Orleans, Wichita, Cleveland, Bakersfield, Aurora, Anaheim, Honolulu, Santa Ana, Riverside, Corpus Christi, Lexington, Pittsburgh, St Louis, Cincinnati, Anchorage, Henderson, Greensboro, Plano, Newark, Lincoln, Orlando, Irvine, Toledo, Jersey City, Chula Vista, Durham, Laredo

**Tier 3 — All remaining US metros with population 100K+ (run monthly):**
Generate dynamically using search patterns.

### Rotation Logic

Track progress in a local JSON file. Pick the next unrun vertical+city combo. After all Tier 1 combos are exhausted, move to Tier 2, then Tier 3, then restart the cycle.

---

## PHASE 2: SEARCH AND SCRAPE

For the selected vertical + city, run these search queries:

- `{vertical} {city} {state}` on Google Maps
- `{vertical} near {city}` via web search
- `best {vertical} in {city} reviews`
- `{vertical} {city} Google Business Profile`

For each business found, extract:
- Business name
- Full address
- Phone number
- Website URL (or mark NO WEBSITE)
- Google Maps link
- Total review count
- Average star rating
- Listed GBP categories
- Whether GBP appears claimed or verified

**Target: 15-30 businesses per run. De-duplicate by phone number across all runs.**

---

## PHASE 3: 18-SIGNAL GBP AUDIT

Score each business 0 or 1 on these signals with the following weights:

| # | Signal | Weight |
|---|--------|--------|
| 1 | Business description present and over 100 characters | 2x |
| 2 | Primary plus secondary categories set | 1x |
| 3 | Business hours listed | 1x |
| 4 | Website URL present | 2x |
| 5 | Website loads and is mobile-friendly | 2x |
| 6 | Phone number present | 1x |
| 7 | Five or more photos uploaded | 1x |
| 8 | Recent photos within last 90 days | 1x |
| 9 | Google Posts active within last 30 days | 3x |
| 10 | Twenty or more reviews | 2x |
| 11 | Average rating 4.5 or above | 1x |
| 12 | Owner responds to reviews | 3x |
| 13 | Services or menu section filled | 2x |
| 14 | Appointment or booking link present | 1x |
| 15 | Q and A section has activity | 1x |
| 16 | Products listed if applicable | 1x |
| 17 | Business attributes filled | 1x |
| 18 | Multi-location consistency if chain | 1x |

**Total possible: 28 points (weighted)**

### Scoring Categories

- **0-8 = CRITICAL** — Immediate high-value opportunity
- **9-16 = POOR** — Strong opportunity
- **17-22 = MODERATE** — Entry-level opportunity
- **23-28 = GOOD** — Skip. Already optimized.

**ONLY log businesses scoring 22 or below.**

---

## PHASE 4: SERVICE TIER MAPPING AND PRICING

### CRITICAL Leads (Score 0-8)

Recommended package: Growth OS at $1,800/mo or Full OS at $3,000/mo. For businesses doing $1M+ revenue: recommend CEO Agent at $3,000-5,000/mo.

Pitch angle: "Your Google presence is essentially invisible. You are losing leads every day to competitors who show up. We deploy a complete system including GBP management, AI voice agent, local SEO, and CRM in under 10 days. Fully managed. You never touch a dashboard."

### POOR Leads (Score 9-16)

Recommended package: Growth OS at $1,800/mo.

Pitch angle: "Your GBP has the basics but you are leaving money on the table. No posts, weak review management, no SEO strategy. We automate all of it. You approve content with one tap from your phone."

### MODERATE Leads (Score 17-22)

Recommended package: Local Presence at $700/mo or Starter Automation at $399/mo. Upsell path: start at $700, upgrade to $1,800 within 90 days.

Pitch angle: "You have a decent foundation. Let us take it from good to dominant. Three posts per week, every review responded to within the hour, monthly performance reporting. Zero effort from you."

### Vertical-Specific Add-Ons

| Vertical | Add-On Service | Price |
|----------|---------------|-------|
| Law firms | AI intake and qualification agent | +$499/mo |
| HVAC and Plumbing | Dispatch AI plus CRM | +$500/mo |
| Med spas and Dental | Appointment booking agent | +$499/mo |
| Property management | Tenant inquiry agent | +$499/mo |
| Contractors | Job dispatch plus estimate routing | +$500/mo |
| Franchise | Multi-location GBP management | +$300/location/mo |
| Auto dealers | Lead qualification agent | +$499/mo |

---

## PHASE 5: CONVERSION ASSET GENERATION

For every CRITICAL and POOR lead, generate three items:

### A. Audit Summary (2-3 sentences)

Template: "{Business Name} in {City} has a GBP optimization score of {Score}/28. Key issues: {top 3 missing signals}. Estimated monthly leads being lost to competitors: {15-40 based on vertical}."

### B. Outreach Message (Email or SMS ready)

Template:
```
Hi,

I was looking at {Business Name}'s Google listing in {City} and noticed {specific issue}.

For {vertical} businesses in {City}, that typically means you are showing up below competitors who post weekly and respond to every review.

We manage Google presence for {vertical} businesses across the US — three posts per week, every review responded to within the hour, and monthly ranking reports. Fully managed. You never touch a dashboard.

Worth a quick call? Our AI receptionist can schedule one: (917) 540-3962

Or reply here.

— ClearOps AI
getclearops.io
```

### C. AI Agent Handoff Notes

Template: "LEAD SOURCE: GBP Scraper | BUSINESS: {name} | VERTICAL: {category} | CITY: {city} | SCORE: {x}/28 | RECOMMENDED: {package} at ${price}/mo | PAIN POINTS: {top 3 issues} | QUALIFY ON: annual revenue, team size, current marketing spend, biggest frustration with online presence"

---

## PHASE 6: CRM LOGGING

Log each qualified lead to a spreadsheet with this column schema:

| Column | Field |
|--------|-------|
| A | Date Found (YYYY-MM-DD) |
| B | Business Name |
| C | Vertical |
| D | City |
| E | State |
| F | Phone |
| G | Website |
| H | Google Maps Link |
| I | Review Count |
| J | Avg Rating |
| K | GBP Score (x/28) |
| L | Score Category |
| M | Top 3 Issues |
| N | Recommended Package |
| O | Monthly Price |
| P | Upsell Package |
| Q | Upsell Price |
| R | Outreach Message |
| S | Agent Handoff Notes |
| T | Outreach Status (default PENDING) |
| U | Lead Source (GBP Scraper v1) |
| V | Assigned To |
| W | Follow-up Date (date plus 3 days) |
| X | Notes |

---

## PHASE 7: DAILY EXECUTION REPORT

After each run, output:

```
=== GBP LEAD SCRAPER — DAILY REPORT ===
Date: {date}
Vertical: {vertical}
Cities Covered: {list}
Businesses Scanned: {count}
Leads Logged (score 22 or below): {count}
  CRITICAL (0-8): {count}
    POOR (9-16): {count}
      MODERATE (17-22): {count}
      Revenue Potential if All Close:
        Conservative 10%: ${amount}/mo
          Moderate 20%: ${amount}/mo
            Aggressive 30%: ${amount}/mo
            Top Opportunity: {name} — {city} — Score {x}/28 — {package}
            Next Run: {next vertical} + {next city}
            ===
            ```

            ---

            ## QUALITY RULES

            1. Never log businesses scoring 23 or above
            2. Verify business is operational and not permanently or temporarily closed
            3. Skip any existing clients already in the CRM
            4. Prioritize businesses with 10-100 reviews (established but not enterprise)
            5. Flag businesses with 100+ reviews AND score below 16 as HIGH VALUE
            6. De-duplicate using phone number as unique key across all runs
            7. For multi-location businesses log the parent company once with location count
            8. Never fabricate data. If a signal cannot be verified, mark as unknown and do not count it toward the score

            ---

            ## INSTALLATION

            ```
            Skills directory: ~/.config/claude-code/skills/gbp_lead_scraper.md
            Progress tracker: ~/.config/claude-code/skills/data/gbp_scraper_progress.json
            Reports: ~/.config/claude-code/skills/data/gbp_scraper_reports/
            ```

            ## TRIGGER COMMANDS

            - `scrape gbp leads` — Run one cycle (next vertical x city in rotation)
            - `scrape gbp leads --vertical=hvac --city=houston` — Target specific combo
            - `find unoptimized gbps` — Same as scrape gbp leads
            - `run lead scraper --report` — Generate daily summary
            - `gbp prospecting --status` — Show progress across all verticals and cities
