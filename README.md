# GBP Lead Scraper Skill for Claude Code

**The most aggressive Google Business Profile lead generation engine ever built for Claude Code.**

Discovers unoptimized local service businesses across the entire US, audits their GBP on 18 weighted signals, maps each lead to a service tier with pricing, generates conversion-ready outreach, and logs everything to your CRM — automatically.

Built by [ClearOps AI](https://getclearops.io) — AI-Managed Growth Infrastructure for Local Service Businesses.

---

## What It Does

This Claude Code skill turns Claude into an autonomous GBP prospecting machine that:

1. **Searches** 20 high-value verticals across 200+ US cities
2. 2. **Audits** every GBP found on 18 weighted optimization signals (28-point scoring system)
   3. 3. **Categorizes** each lead as CRITICAL, POOR, or MODERATE based on their score
      4. 4. **Maps** each lead to a recommended service package with pricing
         5. 5. **Generates** personalized outreach messages and AI agent handoff scripts
            6. 6. **Logs** everything to a spreadsheet CRM with 24-column schema
               7. 7. **Reports** daily execution summaries with revenue projections
                 
                  8. ---
                 
                  9. ## Target Verticals (20 Industries)
                 
                  10. HVAC · Plumbing · Personal Injury Law · Dental / DSO · Med Spas · Property Management · Real Estate Brokerages · Immigration Law · Home Inspection · Luxury Auto Dealers · Franchise Systems · General Contractors · Locksmiths · Door Repair / Security · Speech Therapy / Healthcare · Roofing · Electrical · Pest Control · Landscaping · Auto Body / Collision
                 
                  11. ---
                 
                  12. ## Coverage
                 
                  13. - **Tier 1:** 25 top US metros — scraped weekly
                      - - **Tier 2:** 50 mid-size metros — scraped bi-weekly
                        - - **Tier 3:** 125+ remaining metros (100K+ population) — scraped monthly
                          - - **Total combinations:** 4,000+ vertical × city pairings
                           
                            - ---

                            ## 18-Signal GBP Audit System

                            Every business is scored on a 28-point weighted scale:

                            | Signal | Weight |
                            |--------|--------|
                            | Business description (100+ chars) | 2x |
                            | Categories set | 1x |
                            | Business hours | 1x |
                            | Website URL present | 2x |
                            | Website mobile-friendly | 2x |
                            | Phone number | 1x |
                            | 5+ photos | 1x |
                            | Recent photos (90 days) | 1x |
                            | Google Posts active (30 days) | 3x |
                            | 20+ reviews | 2x |
                            | Rating 4.5+ | 1x |
                            | Owner responds to reviews | 3x |
                            | Services section filled | 2x |
                            | Booking link | 1x |
                            | Q&A activity | 1x |
                            | Products listed | 1x |
                            | Attributes filled | 1x |
                            | Multi-location consistency | 1x |

                            **Scoring:** 0-8 = CRITICAL · 9-16 = POOR · 17-22 = MODERATE · 23-28 = SKIP

                            ---

                            ## Service Tier Mapping

                            Each lead is automatically matched to a recommended package:

                            | Score | Category | Recommended Package | Price Range |
                            |-------|----------|-------------------|-------------|
                            | 0-8 | CRITICAL | Growth OS or Full OS | $1,800 - $5,000/mo |
                            | 9-16 | POOR | Growth OS | $1,800/mo |
                            | 17-22 | MODERATE | Local Presence or Starter | $399 - $700/mo |

                            Plus vertical-specific add-ons: AI voice agents, dispatch automation, appointment booking, CRM integration ($300-$500/mo each).

                            ---

                            ## Installation

                            ### Option 1: Clone and install

                            ```bash
                            git clone https://github.com/ori-ai/gbp-lead-scraper-skill.git
                            cp gbp-lead-scraper-skill/CLAUDE.md ~/.config/claude-code/skills/gbp_lead_scraper.md
                            mkdir -p ~/.config/claude-code/skills/data/gbp_scraper_reports
                            ```

                            ### Option 2: Direct copy

                            Copy the contents of `CLAUDE.md` into `~/.config/claude-code/skills/gbp_lead_scraper.md`

                            ---

                            ## Usage

                            Open Claude Code and use any of these commands:

                            ```
                            scrape gbp leads                                    # Run next cycle in rotation
                            scrape gbp leads --vertical=hvac --city=houston      # Target specific combo
                            find unoptimized gbps                                # Same as scrape gbp leads
                            run lead scraper --report                            # Daily summary
                            gbp prospecting --status                             # Progress tracker
                            ```

                            ---

                            ## CRM Output Schema (24 Columns)

                            Every lead is logged with: Date · Business Name · Vertical · City · State · Phone · Website · Maps Link · Reviews · Rating · GBP Score · Category · Top Issues · Package · Price · Upsell · Upsell Price · Outreach Message · Agent Notes · Status · Source · Assigned To · Follow-up Date · Notes

                            ---

                            ## How It Fits Into Your Stack

                            This skill is designed to integrate with:

                            - **AI Voice Agents** — Leads get warm-transferred with full context
                            - - **n8n Workflows** — Webhook triggers for automated lead routing
                              - - **Google Sheets CRM** — Direct logging to your existing pipeline
                                - - **Content Engines** — Audit data becomes social proof content
                                  - - **Self-Optimization** — Tracks which verticals and cities convert best
                                   
                                    - ---

                                    ## Quality Rules

                                    - Only logs businesses scoring 22 or below (out of 28)
                                    - - Verifies businesses are operational
                                      - - De-duplicates by phone number across all runs
                                        - - Flags high-review businesses with low scores as HIGH VALUE
                                          - - Never fabricates data — unknown signals are excluded from scoring
                                           
                                            - ---

                                            ## Built With

                                            - [Claude Code](https://docs.anthropic.com/en/docs/claude-code) — Anthropic's agentic coding tool
                                            - - [ClearOps AI](https://getclearops.io) — AI-Managed Growth Infrastructure
                                             
                                              - ---

                                              ## License

                                              MIT

                                              ---

                                              **Star this repo if you want to see more Claude Code skills for agency lead generation.**
