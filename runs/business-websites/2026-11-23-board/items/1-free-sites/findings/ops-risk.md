## Operations and risk officer

Round 2, 2026-11-23. Agenda item 1: free sites for well-networked business owners in return for referrals. Updated after reading the cfo, contrarian, customer-advocate, customer-experience, pricing-gtm and legal-regulatory findings, and the lead's additions to context.md.

### Bottom line
If the board gives free sites at all, Tom's roughly 110 remaining trial hours can carry about 4: pricing's 2-then-2 gated pilot, delivered with cx's in-person sign-up and launch visits. The dozen cannot be carried, by email or in person. Before the first invitation, four things need to be written down: a trigger for collecting assets when nobody pays (D-1951/D-1953), referral tracking that Open Brain can actually search (a fixed word in the deal title, with interactions as the ledger), legal's agreement and referral terms, and the contractor registration field. The credit line needs a tested change to the production checks before the first launch, though not before the first invitation.

### Who runs it

**What is the same whatever the board picks.** Only Tom can do the visits, get the yes, approve a client production deploy (CLAUDE.reference.md line 31), hand over referral cash and appear at an in-person launch. Agents can do research and shortlists, builds, draft emails, CRM writes, the monthly referral reconcile and monthly live checks. There is no backup for Tom's part.

**Tom's capacity (corrected).** He has about 20 hours a week through Jan 1, 2027, so roughly 110 hours (Tom via the lead, context.md "Added during the meeting"). Those hours must also cover the 5 or 6 warm owners already pitched, the Lobanton follow-up (3 days overdue), new prospecting, and delivering any paid close.

**Delivery effort per free site.** All of these are guesses; no site has been delivered.
- Using cx's in-person flow and leaving out the Apple, Yelp and Bing cleanup, I estimate about 6 Tom-hours per site:
  - agreement: 0.5 h
  - 30-minute sign-up visit, with the owner's Cloudflare account, domain and Google manager invite done there: 0.5 to 1 h
  - production review and approval: 0.5 to 1 h
  - launch checklist: 1 h
  - Google listing work only: 0.5 to 1 h
  - in-person launch and the walk past neighbours with built demos: 1 to 1.5 h
  - follow-ups: 0.5 h
- Travel comes on top. It is close to 0 when a visit falls on a prospecting day in that cluster. A dedicated round trip from Providence to Greenfield, Keene or Brattleboro is about 3 to 4 hours (a guess).
- The CFO's 6.5 h (range 4 to 10) and pricing's 2 to 4 h plus 1 h are in the same range.

| Plan | Tom-hours (guess) | Share of ~110 h | Who does the weekly work | Does the capacity exist? |
|---|---|---|---|---|
| 0. Status quo, with $50 open to anyone (CFO M2, advocate M1) | About 0 extra; the referral logging is done through the skills | 0% | Tom: touches. Agents: CRM and reconcile. | Yes. Operationally this is the lightest. |
| CFO's founding-client earn-back (up to 3 pay $250, refunds on referrals) | Same as paid sales | n/a; it is sales time | As a paid sale | Yes. Payment fires D-1951/D-1953 as they stand, so no rule change and no free branch in the skill. |
| **Pricing: 4 anchors, 2 then 2, gated** | About 25 to 32 h, including some travel | About 23 to 29% | Tom: 2 visits per site, combined with prospecting days in Greenfield and Keene. Agents: network-score shortlist, builds, agreement drafts, reconcile. | **Yes**, provided each visit is paired with prospecting in that cluster. |
| CX: about 12 founding sites, in person, at most one per cluster | About 75 to 115 h. "One per cluster" spreads 12 sites across 12 clusters in 4 states, at 2 trips each. | About 70 to 100%+ | Tom alone, about 24 trips | **No.** It would use up the warm follow-ups and all December selling. |
| The agenda's 12 by the existing email flow | About 60 to 85 h, plus stalls | About 55 to 77% | Tom alone | No. It also has the worst stall risk (cx A4). |
| One community-group site (CFO M4, advocate M4, contrarian M4) | About 8 h (CFO's guess) | About 7% | Tom, plus a volunteer contact | Yes. GGSL timing fits; Winter Carnival realistically lands after Jan 1. |

**Timing of pricing's gate (my reading).** Batch 1 sign-ups fall in the week of Nov 30, with launches around Dec 14, so the week-3 gate falls before or at launch. That works only if the 3 named introductions are asked for at sign-up, which pricing's ask allows, and not only at launch. Batch 2 would start around Dec 21, so its launches fall in January. That needs Tom's answer on extending the trial (pricing Q4; same as my Q2).

**Referral tracking in Open Brain as it actually works.** The lead's correction: `list_opportunities` searches only the deal title, the customer name and the primary contact's name. There is no tag or type field, and terms text cannot be searched. So the `referrer` relation in pricing M7 and contrarian M4 cannot be used for lookups, and neither can my round-1 "Referred by:" line in the terms. Revised scheme:
1. **Founding deal.** Title "<Business> website (founding)", value 0. A search for "(founding)" lists every free site. Excluding it gives the paid close rate (CFO M5's "own stage"; there is no custom stage, so the title tag stands in for it). The stage moves to `won` at launch, with an `outcome_note` of "Founding site, no charge, agreement I-<id>". The agreement text goes in the terms so it can be read, even though it cannot be searched.
2. **Referred deal.** Title "<Business> website (ref: <Referrer name or business>)". A search for "ref:" lists every referred deal, and a search for "ref: Still Fly" lists one referrer's deals, which is also how a tier is counted if pricing's $125/$50 tiers pass. If the referred business already has a deal, rename it, after checking the attribution rule (R10).
3. **The ledger of record is interactions**, because they are append-only and the repo never rewrites them (`search_interactions`). Fixed subjects:
   - "Referral given: <Referred business>", logged on the referrer's deal, or on the referred deal with the referrer as a participant when the referrer has no deal (non-customers such as stylists or association staff).
   - "Referral paid $<amount> <cash|Venmo>: <Referred business>". The body carries the tier, "Employee of buyer: no" or "Employee of buyer: yes, owner's written OK I-<id>" (legal row 6), and the receipt.

   *Inferred:* `search_interactions` matches subjects. I have not confirmed that; the lead can check.
4. **Payout trigger.** When a deal with "(ref:" in its title is won, the onboarding skill adds the next action "Pay <referrer> $<amount> for <Business>", due within 7 days. It is not marked done until the "Referral paid" interaction exists. Following cx M8, it also adds "Tell <referrer> <Business> is live".
5. **Monthly reconcile (agent, about 10 minutes).** Count won deals with "ref:" in the title against "Referral paid" interactions, and report what is owed, the tier counts, any payee close to the $1,000 W-9 point (legal row 7), and payouts missing the employee line.
6. **In the site_demos repo.** The referred lead's `why_candidate` starts "Introduced by <name>", with a talk point "Mention <name> sent you". These are existing fields, so no code change is needed.
7. **Guarding the title tags.** crm-brief prints `title: "<Business> website"` and `value_amount: 250` for every deal (scripts/crm-brief.mjs lines 358-359), and the demo skill lists both alongside the fields it writes "every time" (claude-reference/skills/demo/SKILL.md line 94). *Inferred:* a demo revision could reset "(ref: ...)" or "(founding)" and put a $0 deal back to $250. Fix: make title and value new-deal-only, like `stage_if_new`. Interactions keep the ledger safe even if this is missed.

### Risk register (risk, likelihood, impact, owner, mitigation, early signal)

| # | Risk | Likelihood | Impact | Owner | Mitigation | Early signal |
|---|---|---|---|---|---|---|
| R1 | Free-site work crowds out selling and delivering paid sites before the trial ends | High at 12 (any flow); low to medium at 4 staged | High | Tom | Pricing's 2+2 with the gate. No more than 2 in onboarding at once. Each visit paired with a prospecting day. | Touch next actions on warm deals go overdue (Lobanton already has) |
| R2 | A free owner goes quiet before launch | Medium with cx's sign-up visit; high with the email flow (cx A4) | Medium | Tom | The sign-up visit does the owner's setup on the spot. Tom takes the photos. Assets due within 14 days, or the offer lapses, in writing. | The 2-day "onboarding reply" action passes twice |
| R3 | The owner is happy but never refers | Medium to high (contrarian: about 70% of people who say they will refer never do) | Medium | Tom | Named introductions from Tom's list of neighbours with built demos (cx row 6, pricing), asked at sign-up as well as at launch. Pricing's gate stops batch 2 if this fails. | Fewer than 6 named introductions by the week-3 gate |
| R4 | Scope creep, with no paid path (D-2053) | High | Medium | Tom | One revision round, a 30-day change window, then a quote or no (legal agreement item 2) | More than 2 "Requested changes" lines after launch |
| R5 | Two prices in one cluster | Medium to high in clusters; low with pricing's gate rules (met in person, not in a paid conversation, not already quoted) | High | Tom | Anchors only where no price has been quoted; cx's one per cluster, applied to 4 not 12. Never send a founding owner the pvdsites.com link before the agreement, because the popup opens by itself showing "$250, done, yours." (cx A1). | An owner says "you gave X theirs free" |
| R6 | The credit line fails production: studio name (check-production.mjs line 148), "pvdsites.com" anywhere in the output (lines 104-111), and, for cx's mailto credit, Tom's email on a paid page (scripts/contact.test.mjs line 63) | Certain unless the code changes | Medium: launch is blocked, or someone is tempted to hand-edit the output | Tom; an agent builds it | Allow one exact, opt-in, nofollow, owner-removable credit string, with tests for allowed, not flagged and altered. Tom approves, because this loosens the strictest build. | A production build fails with "studio name", "preview domain" or a contact test failure |
| R7 | D-1951/D-1953 have no trigger without payment | Certain | Medium | Tom | Motion F2 | Assets requested before a written yes is logged |
| R8 | The onboarding skill, run unchanged, logs "Paid $250" and drafts "The $250 covers..." | High | Medium | Agent edits; Tom re-uploads | A founding branch in the skill (cx A4) | A "(founding)" deal with value 250 |
| R9 | A referral is not recorded, or is paid twice or at the wrong tier | High without the tracking scheme; low with it | Medium | Tom; agent reconciles | Title tags, the interaction ledger, the payout next action, the monthly reconcile | A won "(ref:" deal with no "Referral paid" interaction after 7 days |
| R10 | Attribution dispute, or an introduction to a business already in the CRM (122 deals at lead or qualified) | Medium | Low to medium | Tom | First introducer wins (legal M4), within 90 days, ties to the referrer (pricing M7). Check `account_brief` before renaming a deal. | An introduction names an existing deal |
| R11 | Referred businesses get the cold 5-touch sequence and the expiry clock | Medium | Medium | Tom | Motion F11 | A referred owner declines after touch 3 |
| R12 | The open-ended "no limit" promise outlives the trial | Medium | Low to medium | Tom | Motion F7 | Program still open at the trial review |
| R13 | Cash payouts leave no record | Medium | Low ($2,000 1099-NEC threshold for 2026) | Tom | The "Referral paid" interaction with a receipt. W-9 at $1,000 (legal). | A payout without an interaction |
| R14 | Personal Venmo used for business payments breaks Venmo's terms (now with $125 refunds under pricing's tiers) | Low to medium | Medium | Tom; CFO and legal | Business profile, or goods-and-services tagging (legal row 16) | A hold notice |
| R15 | A delivered site breaks later and the complaint travels through exactly the network the program targets | Low to medium | High | Agent checks; Tom fixes | Monthly live check (F10). A "what you own" sheet at handover. | Live check fails, or the domain expires within 30 days |
| R16 | Tom pays for domains | Low with the sign-up visit (owner's card, owner's account) | Low | Tom | The owner buys the domain on the visit (cx, legal row 13) | A domain registered to Tom on a $0 deal |
| R17 | Lauren's insurance referral gets entangled with free sites | Low to medium | Medium (it lands on Lauren's licence, legal row 9) | Tom; legal | Joins legal M5 | Insurance mentioned in a free-site conversation |
| R18 | December slips batch 2 into January | High | Medium | Tom | Decide on a trial extension now (Q2). Prefer trades and services as anchors. | Batch 1 launches later than Dec 18 |
| R19 | **New:** a $50 is paid to an employee of the buying business (the Executive Cuts and Impulse stylists, I-173/I-174, are exactly the people pricing would pay) | Medium | Medium (commercial-bribery statutes, legal row 6) | Tom | The payout cannot close without the "Employee of buyer" line, and the owner's written OK if yes | A payout to someone whose deal participant role is staff |
| R20 | **New:** a contractor site launches without the state registration number, or says "licence" where the business is only "registered" | High for contractor anchors (Descavich Plumbing is pricing's top candidate; there is no business-level field; `licenseLabel` prints "<ST> license", src/lib/helpers.mjs line 164) | Medium (the client is fined and blames Tom) | Agent builds; Tom verifies in the state lookup | A business-level registration field with a registered-or-licensed label, an onboarding ask in trades.mjs, and a production check for contractor trades (joins legal M6). Until it ships, no contractor anchor launches. | A contractor-trade lead reaches production with no number |
| R21 | **New:** loosening the production checks for the credit lets other residue through | Low | Medium | Agent; Tom reviews | Exempt one exact string only, with tests that reject any other studio text, preview-domain text or email | Any change to `residue`, `studioRe` or contact.test beyond the exact string |
| R22 | **New:** a demo revision rewrites a deal's title or value and loses "(ref:" or "(founding)" | Medium (inferred) | Medium | Agent | Title and value become new-deal-only in crm-brief and the demo skill. Interactions stay the ledger. | A "(founding)" or "(ref:" deal shows up under its plain title |
| R23 | **New:** cx's per-lead popup "no charge" line is shown on a preview link that can be shared (pvdsites.com previews are noindexed but can be passed around), so the free offer travels by link | Medium if adopted | Medium (R5) | Tom | Don't adopt it in v1. Founding owners see the demo on Tom's phone, then review the build in person. The offer stays verbal plus the written agreement. | A founding demo link forwarded to a neighbour |

### Single points of failure
- **Tom.** Only he can do sign-up visits, in-person launches, production approvals, cash payouts, and answer the phone in the popup. CX's in-person design adds to this: a sick week now postpones launches. The fallback is the existing email launch, with the walk past neighbours done on the next prospecting trip.
- **Open Brain.** It is the only CRM and the only referral ledger. Its search is limited to titles and interactions, so the tracking depends on two naming conventions that agents must follow exactly. The monthly reconcile report is the backup copy.
- **crm-brief and the demo skill as deal writers.** One writer controls deal titles and values for every deal (R22).
- **tom@brokkr.co.** All agreements, acceptances and emails. It is the evidence in any referral dispute.
- **Cloudflare.**
  - Previews run on the free plan's build minutes.
  - Each client account has Tom as a member, and legal row 13 says Tom removes himself at handoff. After that, fixes need the owner to re-invite him. That's correct, but the monthly live check can only report a problem, not fix it.
- **`main` is live**, for every preview link an anchor might pass on.
- **The AEOTester plugin.** Every production launch depends on it (CLAUDE.reference.md lines 67 and 123).
- **claude.ai skill uploads.** The founding branch, referral steps and phone fix only take effect after a version bump and re-upload.
- **Venmo or Apple Pay in, cash out.** There is no second channel, and pricing's $125 refunds go back through Venmo.

### Needed before it ships
Before the first invitation:
1. **Legal's one-page agreement**, with my additions:
   - the owner's Cloudflare account, domain and Google manager invite are done at the sign-up visit, before Tom starts the production build
   - assets are due within 14 days or the offer lapses
   - Tom may take the photos himself
2. **The asset and phone trigger decision** (D-1951/D-1953).
3. **Written referral terms**: legal M4, pricing M7's attribution window, and an end date.
4. **The tracking runbook** in the call-notes and onboarding skills (version bumps and re-upload). Also make title and value new-deal-only in scripts/crm-brief.mjs and the demo skill.
5. **The founding branch in the onboarding skill**: value 0, no "$250" lines, no presence-gap section (cx), and the sign-up visit in place of the 14-section email.
6. **A network-score shortlist (pricing M9)**, produced by an agent. Tom picks 2.

Before the first launch:

7. **The credit change**, if approved: an exact string, tests, and Tom's yes.
8. **The contractor registration field**, if any anchor is a contractor.
9. **Fix the phone contradiction.** claude-ai-skills/voice.md line 12 says "No other email includes his phone number", but onboarding SKILL.md step 6.3.4 signs the launch email "with his phone" (cx found it). The owner already has the number from the onboarding email, so D-1953 is not broken. I recommend keeping the phone in the launch email and amending voice.md.
10. **A monthly live check** scheduled for delivered sites (F10).
11. **Hours logged** on the first delivery, step by step (CFO M5, Q5). That turns every hour figure in this file from a guess into a number.

### Evidence
- Lead's additions: Tom's 20 h a week, Open Brain search limits (context.md "Added during the meeting").
- Production guards:
  - scripts/check-production.mjs line 148 (studio name) and lines 104-111 (preview domain and preview wording in any text file)
  - scripts/contact.test.mjs line 63 (Tom's email and phone never on a paid page)
  - scripts/check.mjs line 293 (`askProblems` requires the "$250" price block on every preview, which is what cx's popup variant would have to get past)
- Deal title and value writer: scripts/crm-brief.mjs lines 358-359; claude-reference/skills/demo/SKILL.md line 94.
- No business-level registration field: src/lib/fields.mjs line 24 (licence only on staff entries). The label "<ST> license" comes from src/lib/helpers.mjs line 164.
- Phone contradiction: claude-ai-skills/voice.md line 12 against claude-ai-skills/onboarding/SKILL.md step 6.3.4.
- Teammates' figures and proposals, from items/1-free-sites/findings/:
  - cfo.md: 6.5 h per site; M1 to M5
  - pricing-gtm.md: 4 anchors 2+2, gate, tiers, M1 to M9
  - customer-experience.md: about 12 in person, popup variant, credit, M1 to M10
  - legal-regulatory.md: rows 6, 11, 12, 13; M1 to M7
  - contrarian.md: M1 to M5
  - customer-advocate.md: M1 to M6
- Round-1 evidence stands: the launch checklist, onboarding skill, call-notes skill, docs/ob-changes.md lines 151-169, and the 1099 and Venmo sources: [Sovos](https://sovos.com/regulatory-updates/trr/one-big-beautiful-bill-raises-1099-reporting-thresholds/), [Patriot Software](https://www.patriotsoftware.com/blog/accounting/1099-reporting-threshold/), [Venmo terms](https://www.venmo.com/legal/terms).
- Guesses, labelled as such: every hour figure, the travel times, the domain cost.

### Confidence and gaps
- **High confidence:**
  - the credit is blocked by three guards
  - the payment trigger is missing
  - the dozen does not fit 110 h alongside selling
  - the original terms-based tracking could not be searched
- **Medium confidence:**
  - the title-tag scheme (it depends on agents following two conventions)
  - the risk likelihoods
- **Low confidence:** all hour figures.
- **Unknown:**
  - whether `search_interactions` matches subjects (inferred yes)
  - whether a demo revision actually rewrites titles today (R22, inferred from the brief and the skill text)
  - the current text of Venmo's terms

### Questions for Tom
1. Which 2 owners would you pick for batch 1, and can you visit them on days when you are prospecting in that cluster anyway?
2. If batch 2 launches in January, will you extend the trial for the pilot only?
3. Do free-site owners also get referral cash? The CFO says not for the first two referrals; legal needs the agreement to say which.
4. Does an introduction to a business you have already pitched earn the reward?
5. Will you take the photos yourself at the sign-up visit?
6. Are you willing to approve a change that loosens the production check for one exact credit string?

### Changed after team review
- **Capacity.** Tom has about 20 h a week, so about 110 h left (lead, context.md). Round 1 assumed 45 to 55 h. Effect: the pilot is now comfortable at 4 sites instead of tight at 3, so I moved from my own 3-site cap to **joining pricing's 4 sites given 2 then 2 with the gate**. A dozen is still out: 70 to 100%+ of the hours in cx's in-person form, 55 to 77% by email.
- **Referral tracking redesigned.** `list_opportunities` cannot search terms, and there is no tag or type field (lead). I dropped the "Referred by:" terms line as the lookup key. The lookup is now the title tags "(founding)" and "(ref: <referrer>)", with interactions as the ledger of record. This also replaces the `referrer` relation that pricing M7 and contrarian M4 rely on.
- **New R22** (a demo revision may overwrite title and value), found while checking whether title tags would survive (scripts/crm-brief.mjs lines 358-359).
- **Adopted cx's in-person mechanics** for the anchors: sign-up visit, owner's card and account for the domain, Tom's photos, in-person launch, a recognition list of neighbours with built demos, and "Sent by" cards. They cut R2 and R16 more than any written rule could (customer-experience.md refinements 4 to 6).
- **CX's credit is harder than cx's one-line estimate assumes.** Besides check-production.mjs line 148, "pvdsites.com" fails the preview-domain residue check (lines 104-111), and a mailto to Tom fails contact.test.mjs line 63. I added R6 and R21 detail. I still support the credit, with conditions (F8).
- **I do not support cx's per-lead popup variant (cx M4) for v1.** It publishes "no charge" on a shareable preview link (R23). The popup wording changes only on Tom's word (CLAUDE.reference.md lines 29-30), and the in-person invitation makes it unnecessary.
- **Legal's employee-payment rule** (legal-regulatory.md row 6) collides with pricing's plan to pay the Executive Cuts and Impulse stylists (pricing-gtm.md, first ten customers, segment 2). I added R19, and the payout ledger now needs an "Employee of buyer" line before a payout can close.
- **Legal's contractor registration rule** (row 11) is a code change, not a wording change: there is no business-level field, and the existing label says "license". It blocks a contractor anchor such as Descavich Plumbing (pricing's top candidate) until it ships (R20).
- **Operations is neutral to positive on the CFO's earn-back.** It needs no trigger change and no free branch in the skill, which makes it the cheapest option to run. Whether free sites are worth giving at all is for the board to decide on the CFO, contrarian and advocate arguments. My motions set how to run them if they are approved.

### Final motions for the secretary
Proposer is "ops" unless the motion joins another member's. Each makes one change. Money figures are guesses unless stated.

- **F1. Cap and stage free business sites.** Joins **pricing's motion 1**: at most 4 during the trial, 2 then 2, batch 2 only after 6 or more named introductions within 3 weeks. Ops addition for the secretary to record with it: no more than 2 in onboarding at once, and each visit paired with a prospecting day in that cluster. D-ids: new, under D-2050. Money: about 25 to 32 Tom-hours, against about 75 to 115 for cx's 12. Risk: lowers R1, R2 and R5.
- **F2. Asset and phone trigger for no-payment deals.** Proposer: ops. Restates D-1951 and D-1953 to fire on "payment, or the owner's written acceptance of the free-site agreement". The same change sits inside cx M5, pricing M3 and contrarian M2; I offer it as a single change so it is recorded once. D-ids: D-1951, D-1953. Money: $0. Risk: removes R7.
- **F3. Written agreement before any free build.** Joins **legal's motion 1**. Ops asks that its contents add: the owner's Cloudflare account, domain and Google manager invite done at the sign-up visit before the production build; a 14-day asset deadline after which the offer lapses; Tom may take the photos. D-ids: new; relates to D-1971 and D-1979. Money: $0, plus an optional lawyer review of about $300 to $750 (legal's guess). Risk: lowers R2, R4 and R16.
- **F4. Founding-site scope.** Joins **cx's motion 2** (Google work only; no Apple, Yelp or Bing; no presence report; the demo plus one page). Ops reason: it removes the slowest steps that wait on the owner to verify, and saves about 1 h per site. D-ids: D-1971, D-1975, D-1977, D-1978. Money: saves about 1 h per site. Risk: lowers R1 and R2.
- **F5. Searchable referral and founding tracking in Open Brain.** Proposer: ops.
  - Deal titles carry "(founding)" or "(ref: <referrer>)"; founding deals are valued at 0.
  - Interactions "Referral given: ..." and "Referral paid $n ...: ..." are the ledger of record.
  - When a "(ref:" deal is won, a payout next action is due within 7 days.
  - An agent reconciles monthly.
  - The call-notes and onboarding skills are updated and re-uploaded.
  - crm-brief and the demo skill write title and value only on new deals.

  Replaces the `referrer`-relation mechanism in pricing M7 and contrarian M4, which Open Brain cannot search, and provides the mechanism for CFO M5's "log the referrer" and "free sites kept apart at $0". D-ids: D-2050, D-1969 (pending Mark paid), D-1963 to D-1967 (CRM mapping), open-brain D-1962. Money: $0; about 10 agent-minutes a month and about 2 Tom-minutes per referral (guess). Risk: removes R9 and R22.
- **F6. Written referral terms.** Joins **legal's motion 4** (paid after the referred business pays and its site is live, first introducer, the employee rule, a receipt, W-9 and 1099 points). Ops asks the secretary to attach pricing M7's 90-day attribution window and tie rule, so the terms carry a single attribution rule. D-ids: new referral decision; relates to D-2050. Money: as set by pricing or the CFO ($50 per referred sale, or the tiers). Risk: removes R10, R13 and R19.
- **F7. End date for the referral offer.** Proposer: ops. Whatever the amount, the offer runs through a stated date (I suggest the trial review, or June 30, 2027), and rewards already earned are always paid. D-ids: the new referral decision from F6. Money: caps an open-ended liability. Risk: removes R12.
- **F8. Opt-in credit line on live sites.** Joins **cx's motion 7**, with these ops conditions:
  - one exact string, opt-in by lead flag
  - `rel="nofollow"` and removable by the owner (legal row 12)
  - the studio-name check (check-production.mjs line 148), the preview-domain residue check (lines 104-111) and, if a mailto is kept, contact.test.mjs line 63 are each relaxed for that exact string only, with tests for allowed, not flagged and altered
  - Tom's yes before merging, because it loosens the strictest build
  - built before the first credited launch, not before the first invitation

  D-ids: D-2005; the community free-site rule (no D-id). Money: about 1 agent-day plus about 1 Tom-hour of review (guess). Risk: R6 and R21 controlled.
- **F9. Contractor registration numbers.** Joins **legal's motion 6**. Ops note for the record: this needs a new business-level owner-only field, a registered-or-licensed label (today's `licenseLabel` prints "license"), an onboarding ask in trades.mjs, and a production check for contractor trades. No contractor anchor launches before it ships. D-ids: new child of D-1935; relates to D-1971. Money: about half an agent-day plus about 30 Tom-minutes of state lookup per contractor (guess). Risk: removes R20.
- **F10. Monthly live check of delivered sites.** Proposer: ops. Each month an agent runs `npm run aeo -- <slug> --live` (or a plain fetch) on every delivered site, paid or free, and reports failures and domain renewals due within 60 days. D-ids: D-2033. Money: $0; about 10 agent-minutes per site per month. Risk: lowers R15.
- **F11. Warm sequence for referred businesses.** Proposer: ops. Touch 1 names the referrer and arrives with the demo already built; at most 3 touches; the 2-week expiry is mentioned once, with an offer to extend (cx refinement 12). D-ids: D-2050, D-2052. Money: $0; saves 2 touches per referred lead. Risk: lowers R11.
- **F12. Clear Lobanton first.** Joins **contrarian's motion 5**: preview_until to 2026-12-02 under D-2052, and close the overdue follow-up before any free-site invitation goes out. D-ids: D-2052. Money: $0. Risk: lowers R1 (it is the live overload signal).
- **F13. Keep Lauren's referral separate.** Joins **legal's motion 5**. D-ids: new; relates to D-2050. Money: $0. Risk: lowers R17.
- **F14. Log delivery hours and keep free sites out of the close rate.** Joins **CFO's motion 5**, using F5's "(founding)" title tag and value 0 in place of a separate stage, which Open Brain does not have. D-ids: D-2050, open-brain D-1962. Money: $0. Risk: turns every hour guess in this file into a measured figure after the first delivery.

**Not supported by ops:**
- cx's motion 4 (the per-lead popup variant), because of R23 and because the in-person invitation makes it unnecessary.
- cx's count of about 12 founding sites, because of R1: 70 to 100%+ of Tom's remaining hours.
