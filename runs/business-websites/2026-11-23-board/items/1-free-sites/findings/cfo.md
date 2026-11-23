## CFO

### Bottom line
Give at most 4 free sites during the trial, in two batches of 2, as pricing proposes. The second batch goes out only if the first passes its gate and at least one paid site has been delivered and timed. Carry pricing's tiered referral ($125, $125, then $50), not my separate founding-client earn-back: it is the same money, applied to every buyer. At 20 hours a week, the 4-site plan costs about 10-26 of Tom's roughly 110 remaining hours and less than $350 cash. The 12-site founding plan costs about 75-80 hours, which leaves too little for the paid pipeline the trial exists to test.

### Money picture
All figures are from the run folder unless marked *estimate* or *inferred*.

| Item | Figure | Source |
|---|---|---|
| Revenue to date | $0 (0 deals won) | current-state.md s.3, s.8 |
| Price | $250 flat, one time; no subscriptions in the trial | CLAUDE.reference.md l.6; helpers.mjs `OFFER_PRICE` |
| Payment fee | About $0 on personal Venmo; about $4.85 a sale on a Venmo business profile (1.9% + $0.10, unchecked) | pricing-gtm.md unit economics; legal row 16 |
| Pipeline (face value) | 96 qualified x $250 = $24,000. Only about 5-6 owners have actually been pitched. | current-state.md s.8 |
| Cash spend to date | **Not recorded.** Still open with the lead. | gap |
| Monthly cash burn | About $0 in direct cost (Cloudflare free plan, no hosting); Claude and the domain are shared or fixed costs (*inferred*) | CLAUDE.reference.md l.10, l.117 |
| Running cost per delivered site | $0 to Tom after delivery | context.md |
| **Tom's hours left in the trial** | **About 110 (20 h/week through Jan 1, 2027)** | context.md, "Added during the meeting" (Tom, 2026-11-23) |
| Optional lawyer review | About $300-750, one time | legal-regulatory.md (their guess) |

**Hours per delivered site (*estimate*; no site has been delivered).**
- Full paid scope: about 6.5 h (range 4-10). Ops estimates 5-7 h and pricing 3-5 h.
- Trimmed free scope, without the Apple, Yelp and Bing cleanup or the presence report (pricing and cx both cut these): about 5 h.
- Cx's in-person version, with a sign-up visit and a launch at the counter: about 6 h in Providence and 7-8 h out of area, because it takes two trips.
- I use 5-6 h for a free site and 6.5 h for a paid one.

**How the 110 hours would be spent (*estimate*).** The paid path needs about 60-70 hours:
- warm follow-ups on the 5-6 pitched owners plus new prospecting touches under D-2050: about 30-40 h;
- delivering about 5 paid sites, pricing's pass mark: about 32 h.

That leaves about **40-50 hours** for any free-site programme. That is the budget each plan below is measured against.

The cheapest money on the table is still Lobanton (OPP-31). Its follow-up is overdue, and the preview should run to about 12-02 under D-2052 (current-state.md s.8). Closing it also gives the first measured delivery time.

### Financial effect of each motion
**Break-even method (unchanged from round 1; *estimate*).**
- A free site brings in $0 and costs about 6 h.
- Each paid site it leads to brings in $250 minus the referral paid (r), for about 6.5 h of selling and delivery.
- The free site pays off only if its revenue per hour beats cold selling, which earns $250 per (5.5 h + A), where A is the hours of cold prospecting per sale won.
- A is unknown: 85 demos and 5-6 pitches have produced 0 wins.

| Hours of cold prospecting per sale (A) | Cold-selling $/h | Paid sites each free site must yield (r = $50) | Same, if the free recipient's first referrals pay $0 |
|---|---|---|---|
| 4 h (cold works well) | $26 | ~6 | ~2 |
| 10 h (middle guess) | $16 | ~1.1 | ~0.7 |
| 20 h (cold works badly) | $10 | ~0.5 | ~0.3 |

Even with endless referrals, free sites top out at about $31-38 per hour. On cash alone, one referred sale (about $195 net) covers the cash cost of about six free sites. **Hours are the constraint; cash is not.**

**Option A: no business giveaway, community groups only (the advocate's position).**
- Hours: about 8 h per community site (*estimate*). Cash: $0-15 per site.
- Adds a small code change for the credit line (scripts/check-production.mjs l.148).
- Affordable. It avoids the two-price risk entirely. But it produces no business-owner connector test before Jan 1, because Winter Carnival and the Greenfield Girls Softball League (GGSL) are spring or February calendars.

**Option B: about 12 "founding sites", handled in person (cx's plan).**

| What | Figure (*estimate*) |
|---|---|
| Delivery | 12 x ~6 h = ~72 h (range 54-108) |
| Plus | Referral follow-ups ~3 h, plus Tom's review of the popup-flag and footer-credit builds ~2-3 h (cx estimates about 1 day of build each) |
| **Total hours** | **~78 h, about 70% of the 110 left (range 55-100%)** |
| Cash | Cards ~$60. Mileage for two trips per site: ~$100-400, cheap if all 12 are in Providence. Domains on the owners' cards: $0. **Total ~$200-500.** |
| Break-even (middle case) | ~13 referred paid sales, about $3,250 gross |
| Expected referred sales by Jan 1 | 0-3. The contrarian's vendor figure of about 18% of recipients converting gives about 2. Launches land mid-to-late December. |
| Net cash in the trial | About -$500 to +$250 |

- **Not affordable alongside the paid path.** It leaves about 32 hours for Lobanton, the warm owners and any sales the referrals produce. Five referred sales alone would use all 32 hours in delivery.
- **Flag: it commits about 70% of the remaining trial before any market result,** and it replaces the trial's question (do owners pay $250?) with a different one (do gifted owners refer?).
- Cx's in-person mechanics are good value at small scale and should be used for the anchors: the launch at the counter, the named-neighbour ask, and the "Sent by" cards.

**Option C: 4 anchors, 2 then 2, gated at week 3 on at least 6 named introductions (pricing's plan, which folds the community and partner picks into the same cap).**

| | Batch 1 (2 sites) | Batch 2 (2 sites, if the gate passes) | Whole plan |
|---|---|---|---|
| Hours | ~10-13 h | ~10-13 h | **~10-26 h, 9-24% of the 110 hours** |
| Cash | | | ~$20-60 in cards, plus ~$140 per dedicated Greenfield or Keene round trip at ~$0.70/mile. Marginal if Tom is already going there to prospect. **Under ~$350 in total.** |
| Break-even (middle case) | ~2-3 referred sales | | ~4-5 referred sales |

At pricing's pass mark (5 paid sites by week 6: at least 3 from anchor or partner introductions and at least 1 referred by a paying customer):

| | Figure (*estimate*) |
|---|---|
| Revenue | 5 x $250 = $1,250 |
| Payouts | ~$125-175 (one $125 tier payment, possibly one $50). Anchors' first two referrals pay $0 under my motion F4. |
| Venmo business fees | ~$24 |
| **Net cash** | **~+$1,050** |
| Hours | ~26 (anchors) + ~32 (paid deliveries) + selling, which fits within 110 |

- If the gate fails, the downside is capped at 2 sites, about 10-13 hours.
- **Affordable now.** I recommend it, with one amendment: batch 2 also waits until at least one paid site has been delivered and timed. That way willingness-to-pay data, and a real hours figure, exist before more is given away.

**Option D: 3 free sites, offered by Dec 5 and live by Dec 31 (ops's plan).**
- About 15-20 h and about $90.
- Affordable. It is close to C, but without C's stop after the first two sites.
- I prefer C's 2-then-2 because it caps the downside at 2.

**Option E: pricing's tiered referral ($125 back on each of a buyer's first two referred sales, then $50 each, no limit) versus my round-1 founding-client earn-back.**
- The money is identical. Mine limited it to 3 hand-picked owners; pricing's offers it to every buyer, at every pitch.
- **Carry pricing's version.** It is one rule for everyone, so there is no second price (the advocate's main concern). It is easier to say at the counter, and it tests whether owners will pay $250 because the buyer pays first.
- Cost: it is never cash-negative. Each of a buyer's first two referred sales nets $125 instead of $200. The extra exposure is at most $150 per buyer, and only out of referral revenue (*arithmetic*).
- Risk: the contrarian cites Gershon, Cryder and John (2020), who found that rewarding the referrer adds little. Pricing's own v2 trigger answers this: keep the $125 tier only if referred sales are at least 30% of closes.

**Option F: open the $50 to anyone who introduces a buyer (pricing, the advocate and cx all propose this).**
- Costs $0 upfront and about +$200 net per referred sale. Affordable now.
- Legal's commercial-bribery point (RI §§ 11-7-3/4, Mass. c. 271 § 39) costs nothing to fix: never pay an employee of the buying business without the owner's written knowledge.
- A cheaper and cleaner alternative for staff introducers such as the Executive Cuts and Impulse stylists (I-173, I-174): give the $50 to the buying business as $50 off, following cx's give-or-get idea. The cash is the same, there is no payment to an employee, and the contrarian's research suggests a benefit to the referred business converts better. The pricing and legal leads should confirm this.

**Option G: pay-on-launch (the contrarian's motion 2).**
- Revenue arrives later. The exposure is about 6.5 h per owner who doesn't pay after delivery.
- Affordable if capped at about 3 unpaid launches at a time (exposure about 20 h). This is mostly outside this item.

**How the $50 and the $250 fit.**
- At $250, the $50 is 20% of revenue, and the $125 tier is 50% of the first two referred sales.
- Neither ever pays out before the money comes in. The $250 holds (pricing's motion 6 records it).
- A free anchor should not also get cash for its first two referred sales. A paying buyer gets $250 back over two referrals, and an anchor has already received the $250 site. Paying both would pay twice for the same referrals (motion F4).

**Lawyer review ($300-750, legal's guess).**
- This is the only cash commitment on the table.
- Defer it until 3 paid sites have closed or the trial is extended. Tom can draft the one-page agreement himself from legal's 11-point list for $0.
- Hold the employee-payment question until the lawyer review by simply not paying employees (the carve-out above).

### Cheaper ways to the same answer
1. **Close what is already warm ($0).**
   - Lobanton's follow-up and preview date (joins the contrarian's motion 5).
   - Touches 2-5 on the 5-6 pitched owners.
2. **Work the referrals already moving ($0 until a sale).**
   - Madison Hart's Skittlez Ink introduction (I-165).
   - The Executive Cuts and Impulse stylists, with the $50 offered as $50 off for their owner (I-173, I-174).
3. **Say the tiered referral at every pitch ($0 upfront).** "Two neighbours who buy and yours is free" makes the site free for the buyer without giving it away.
4. **Give 2 anchors, not 12 (~10-13 h),** with the week-3 gate.
5. **Ask associations for one-to-many introductions** (pricing's partner deal), counted inside the 4-site cap.

### Evidence
- **Tom's hours:** 20 h/week, about 110 h left (context.md, "Added during the meeting").
- **Pricing's plan:** 4 anchors in two batches, a week-3 gate of 6 named introductions, the $125/$125/$50 tier, the week-6 pass mark and partner deals (pricing-gtm.md, motions 1, 4, 5, 6 and 8, and the market test).
- **Cx's plan:** 12 in-person founding sites, a popup flag and footer credit (about 1 day each, inferred), and a trimmed scope (customer-experience.md, motions 1-10).
- **Ops:** 5-7 h per site, a 3-site cap, referral tracking with value-0 free deals, and the first free site serving as a dry run that records delivery time (ops-risk.md, M1, M5, "Needed before it ships" item 8).
- **Contrarian:** the 2-3 site gate, pay-on-launch, Lobanton, Gershon et al. 2020, and the vendor's 18% conversion figure (contrarian.md).
- **Advocate:** no business giveaway, the two-price risk inside clusters, Madison Hart's unpaid referral (customer-advocate.md).
- **Legal:** commercial bribery (row 6), the 1099-NEC threshold of $2,000 (row 7), the lawyer review at $300-750 (a guess), the Venmo business profile (row 16) (legal-regulatory.md).
- **Round-1 sources still used:** CLAUDE.reference.md l.3, 6, 10, 12, 117; onboarding SKILL.md step 6; docs/launch-checklist.md; docs/free-sites.md; current-state.md s.2, s.8, s.9.
- **Everything marked *estimate* is mine,** including the per-site hours, the 60-70 hour paid-path load, mileage and referral lag.

### Confidence and gaps
- **Medium-high:** a 2-then-2 cap fits the hours at 20 h/week, and 12 does not leave room for the paid path.
- **Low:** every break-even count. Hours per delivery and cold-prospecting hours per sale are still unmeasured. The first paid or anchor delivery should be timed step by step, as ops proposes.
- **Missing:**
  - Cash spent to date.
  - Whether Claude usage is a flat subscription.
  - Whether Tom would extend the trial if the week-6 result lands after Jan 1 (pricing asks the same question).
  - Whether Tom receives payments on personal Venmo or a business profile, which decides the ~2% fee.

### Questions for Tom
1. Will you extend the trial to about Jan 4-15 so pricing's 6-week test can finish?
2. Are you willing to say "two neighbours who buy and yours is free" at the counter, and to refund $125 by Venmo?
3. Should anchors receive no cash for their first two referred sales and $50 from the third, the mirror of the buyer's $125 tier?
4. Will you log your hours on the first delivery step by step?
5. What have you spent so far (domain, travel, tools)?

### Changed after team review
- **Hours budget roughly doubled.** Tom's answer (context.md) raises the capacity from my assumed 55 h to about 110 h. My round-1 verdict that even 2-3 free sites should wait for the first paid delivery no longer holds: 2 anchors take about 10-13 h, about 10% of the remaining hours. I moved from "no free site before the first paid delivery" to **support pricing's 2-then-2 cap**, adding the first paid delivery as a condition for batch 2 only.
- **12 sites recosted.** At 110 h, cx's 12 founding sites (about 78 h) is no longer more than Tom has, but it is about 70% of it. It would leave too little for the paid pipeline. I still oppose 12, now for that reason rather than plain unaffordability.
- **Earn-back merged into pricing's tier.** My founding-client earn-back for 3 owners has the same money structure as pricing's tiered referral for every buyer. I withdraw mine and join pricing's, because a single rule avoids a second price (customer-advocate.md).
- **Employee carve-out added (from legal-regulatory.md row 6).** Payments to anyone now exclude employees of the buying business unless the owner knows in writing. I added the $50-off alternative, taken from cx's give-or-get (customer-experience.md motion 9) and the contrarian's recipient-reward evidence (contrarian.md).
- **New cash line: the lawyer review ($300-750, from legal).** I recommend deferring it until 3 paid sites or a trial extension.
- **Community sites count toward the same 4-site cap** (pricing's motion 8), not as a separate programme.

### Final motions for the secretary
Proposer: CFO. Each makes one change. "Joins" means I back another member's motion rather than duplicate it.

**F1. Cap free sites at 4 during the trial, given 2 then 2.**
- Joins pricing's motion 1 (ops's M1 sets a cap of 3; the contrarian's motion 4 sets 2-3).
- Amendment proposed by the CFO: batch 2 also requires at least one paid site delivered with Tom's hours logged.
- Touches: new decision under D-2050.
- Money: ~10-26 h of ~110; under $350 cash; downside capped at ~10-13 h if the gate fails.
- Risk: misses the upside of 12 if connectors turn out to refer strongly. Mitigation: revisit after Jan 1 with data.

**F2. Do not adopt the 12 free business sites in the trial.**
- Joins the advocate's motion 3 in effect: it rejects the agenda's 12 and cx's founding programme at that size. It is distinct from F1 only if the board votes the number separately.
- Touches: new decision.
- Money: avoids ~78 h (~70% of the remaining trial) and ~$200-500 cash.
- Risk: as F1.

**F3. Tiered referral: $125 back on each of a buyer's first two referred sales, then $50 each, no limit.**
- Joins pricing's motion 4. Replaces my round-1 founding-client earn-back.
- Touches: new referral decision (the $50 has no D-id); onboarding SKILL step 6.
- Money: never cash-negative; at most $150 extra per buyer, paid only from referral revenue. Review at v2: keep the $125 tier only if referred sales are at least 30% of closes.
- Risk: research says rewards to the referrer add little; bounded cost.

**F4. Free anchors earn no cash on their first two referred sales and $50 from the third.**
- New; CFO.
- Touches: the new referral decision from F3 and the free-site agreement (legal's motion 1, ops's M4).
- Money: saves $100 per anchor and keeps anchors and buyers on the same "free after two" footing.
- Risk: an anchor may find it stingy (cx Q5). Legal says either way is lawful if written.

**F5. Open the $50 to anyone who introduces a buyer, said at the pitch.**
- Joins pricing's motion 5 and the advocate's motion 1.
- Touches: new referral decision; D-2050; the OFFER_* constants and card wording, only on Tom's word.
- Money: $0 upfront; +$200 net per referred sale.
- Risk: commercial bribery if paid to staff of the buying business. Covered by F6.

**F6. No referral payment to an employee of the buying business without the owner's written knowledge.**
- Joins legal's motion 4 (written $50 referral terms), which already contains this rule.
- CFO addition for the board to consider: for staff introducers, offer the $50 as $50 off for the buying business instead.
- Touches: the new referral decision; D-2050.
- Money: $0 change in cost.
- Risk: removes the RI §§ 11-7-3/4 and Mass. c. 271 § 39 exposure.

**F7. Log Tom's hours on every delivered site, paid or free, as an interaction on the deal. Free deals carry value 0 and stay out of paid "won" totals.**
- New for the hours log, joining ops's M5 (tracking runbook, value-0 free deals).
- Touches: D-2050; open-brain D-1962 (fields still to build); ops's M5.
- Money: $0. It produces the numbers every break-even above depends on.
- Risk: none.

**F8. Defer any paid lawyer review ($300-750) until 3 paid sites have closed or the trial is extended. Tom drafts the agreement from legal's list until then.**
- New; CFO. Modifies legal's motion 1 only as to its optional spend.
- Touches: legal's motion 1.
- Money: avoids up to $750 before any revenue.
- Risk: an unreviewed agreement for 2-4 free sites. Low, since no money changes hands on free sites.

**F9. Bring Lobanton's preview into line with D-2052 (through about 12-02) and clear the overdue follow-up before any new programme starts.**
- Joins the contrarian's motion 5.
- Touches: D-2052.
- Money: $250, the only live proposal.
- Risk: none.
