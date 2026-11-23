# Board pack: PVD Sites (`business-websites`), 2026-11-23

Prepared by the board secretary from Open Brain (read 2026-11-23) and the repo copy `sources/site_demos` at commit 892a68d (2026-11-21). Ids: D- decisions, T- thoughts, OPP- deals, I- interactions, Q- open questions. Anything marked *inferred* is the secretary's reading, not a recorded fact.

Agenda item 1: free sites for a dozen or so well-networked business owners, in return for referrals.

## 1. What the project is

- PVD Sites (pvdsites.com) sells small websites to independent local businesses. Trial: "Test runs through Jan 1, 2027" (CLAUDE.reference.md line 3). No subscriptions during the trial (CLAUDE.reference.md line 6; D-1976 context, Tom 2026-11-18).
- Open Brain registers 82 decisions for the project (77 active or deferred, 4 superseded, 1 proposed) and 2 thoughts (T-368, T-369). The project's registry description is still "Auto-registered via capture_thought" (list_projects).
- Who it serves: owner-run independent businesses that are well reviewed, have no or a weak website and do not already pay a designer. Priority order: trades and contractors, then other services (barber, salon, nails, auto, offices), then restaurants, then retail; at most 2 of one trade per 5-lead batch; chains, franchises and businesses already paying a designer are skipped (CLAUDE.reference.md line 11; claude-reference/agents/lead-researcher.md lines 11 and 33-35; scoring D-2002).

## 2. What is built and shipped

- Demo pipeline: `/demo` skill (D-1954) builds a themed demo per lead from public data (D-1951), with parallel subagents (D-1961), design standards (D-1933 and 21 live children), labelled and unindexed previews (D-1934), verified facts only (D-1935). Previews deploy from `main` on Cloudflare's free plan (D-1955; CLAUDE.reference.md line 117: "Nothing is charged").
- Every preview carries a "Questions about this site?" popup (D-2046) that opens with the price: `OFFER_PRICE = '$250, done, yours.'` and a six-line `OFFER_INCLUDES` list; `OFFER_NOT_INCLUDED = 'Not included: an online store or translated pages.'` (src/lib/helpers.mjs lines 311-320).
- Production build for paid sites: `npm run production` with strict checks (D-2005), AEOTester advisory (D-2033), launch checklist (docs/launch-checklist.md). **Fact relevant to the item:** the production check fails any page that carries the studio name: "the studio name ... is on the page; the only studio credit was the preview wording" (scripts/check-production.mjs line 148; test at scripts/production.test.mjs line 166, "Site by Fixture Studio"). A "Site by PVD Sites" credit line, as docs/free-sites.md proposes for free sites, cannot ship through the production build as coded today.
- Claude skills for call notes (1.4.0) and onboarding (1.3.0) (claude-ai-skills/release.json; D-1959).
- Repo copy holds 94 lead files and 86 onboarding emails (`ls leads`, `ls onboarding`).
- No paid site has been built or delivered (no deal is `won`).

## 3. Pricing and money

- Price: $250 flat, one time, for the site plus a listing cleanup across Google Business Profile, Apple Business Connect, Yelp and Bing (D-1978; T-369; helpers.mjs). Every deal carries the D-1971 additions (D-1972 to D-1981). Client owns domain and hosting in their own Cloudflare account; Tom does not host (CLAUDE.reference.md line 14).
- **The $250 price has no decision of its own in Open Brain.** It appears in T-369 (reference thought), in D-1978's title and text ("The $250 Google listing cleanup is widened ..."), in every deal's value (USD 250) and in the repo. No list_decisions hit for components `pricing` or `referral`.
- Payment: Venmo or Apple Pay (CLAUDE.reference.md line 13; docs/ob-changes.md adds cash).
- Running cost per site to Tom after delivery: none stated beyond his time (Tom does not host; Cloudflare free plan for previews). Cost of a domain Tom buys for a client and transfers: not recorded anywhere (gap).
- Revenue to date: $0 (no `won` deal).
- Care plan / monthly plan: **D-2053, deferred.** Full text: "Care plan: not offered and not mentioned to customers. The draft (sales-methods G doc) is kept for later." Context: Tom, 2026-11-21: "Care plan is deferred till we decide how viable the whole plan is". Trigger: "Tom decides the whole PVD Sites plan is viable". Component `offer`. Parent: D-2050 (the prospecting protocol). The onboarding skill also forbids mentioning a monthly plan (SKILL.md steps 5 and 6.3). D-1976 says free analytics on paid sites exist partly "to help validate a future monthly plan".

## 4. The referral offers in force

- **$50 cash referral (no D-id).** Source: claude-ai-skills/onboarding/SKILL.md step 6, Tom 2026-11-21: "I want to make sure that after payment is made and the site is delivered that we mention the referral fee we offer." Terms as written: the owner passes along another business owner's information and lets Tom mention them; Tom brings $50 cash once that business buys a site; "for every business that buys, not just one, with no limit". The launch email asks: "Who else nearby would you introduce me to?" A next action "Ask <Business> about referrals in person" follows about two weeks later.
  - The offer reaches an owner only in the launch email after a paid site is live. With 0 won deals, no owner has received it.
  - **No tracking exists.** Open Brain has no referral field or decision for business-to-business referrals; the CRM's relation types include `referrer` (manage_open_questions schema), but nothing in the onboarding or call-notes skills records who referred whom or when $50 is owed (inferred from the skill texts and docs/ob-changes.md).
- **Lauren insurance referral (no D-id).** After a close, with the owner's OK, Tom may refer the owner to Lauren for business insurance (CLAUDE.reference.md line 15). Never mentioned in any email (claude-ai-skills/voice.md line 11). Proposed field `referred_to_lauren` on the opportunity: "not yet" built (docs/ob-changes.md line 166).
- Precedent elsewhere: yacht-ai has a built referral system with attributed invites (D-810, D-812) and deferred referral payouts (D-857, deferred "until real credit-usage data is available").

## 5. The existing free-site idea (community groups)

- Rule (no D-id): CLAUDE.reference.md line 12, Tom 2026-11-21: for every new area list 2 community groups with no or a weak site in docs/free-sites.md; "Tom picks which to offer a free site with a small credit line. Research only: contact nobody."
- docs/free-sites.md: credit line "Site by PVD Sites". Eight groups researched, one pick per area:
  - Providence: Friends of India Point Park (pick), Pete & Andy's Food Pantry.
  - Greenfield: Greenfield Girls Softball League (pick; "Strongest match in the whole search"; 10 teams each sponsored by a local business, including **Descavich Plumbing**, which is also OPP-126, a qualified deal with a live demo), Greenfield Bee Fest (tied to the Greenfield Business Association).
  - Brattleboro: Winter Carnival (pick; planning for February 2027), Kiwanis Club ("members are typically local business people").
  - Keene/Westmoreland: Keene Crush Youth Lacrosse (pick), Westmoreland Old Home Days (town committee; Selectboard may need to approve).
- Status: research only; nobody contacted (docs/free-sites.md line 3). No Open Brain record of any group.
- Earlier unpaid website help: Gail Ahlers, The Empowerment Factory (nonprofit), referred to Tom by Lauren in September 2026 (I-55, E-72210; T-209 asked whether Tom owes Gail website help). Outcome not recorded.

## 6. Decisions in force that bear on the item

| D-id | Status | What it says (verbatim or close) | Bearing on free sites |
|---|---|---|---|
| D-1971 | active, n/a | Every deal includes the low-effort, high-value additions (children D-1972 to D-1981). Tom approved 2026-11-18. | Defines what a "site" includes; a free site must say which of these it carries. |
| D-1975 | active, n/a | Review button on every site and a printable QR card for each paying client; "Neither may ask customers to name staff, offer incentives, or act as an in-store review kiosk." Context: Google's April 2026 review policy. | A free site cannot be given in return for reviews; the QR card is written as a paying-client deliverable. |
| D-1976 | active, n/a | Free visitor analytics on paying clients' live sites, situationally; numbers help validate a future monthly plan. | A free site's traffic could serve the same proof (inferred). |
| D-1978 | active, n/a | $250 covers a four-platform listing cleanup. | The only decision that names the $250 figure. |
| D-1979 | active, n/a | Free Cloudflare email forwarding during onboarding. | Part of what a free site would or would not include. |
| D-1934 / D-1935 | active | Previews labelled and unindexed; real verified content only. | Apply to any free-site demo. |
| D-1951 | active | Owner's copy, photos and brand assets requested only after payment. | A free site has no payment event; the trigger for asset collection would need restating (inferred). |
| D-1953 | active | Tom's phone only after payment (onboarding email) and in the preview popup. | Same: no payment event for a free site. |
| D-2050 | active, n/a | 5-touch prospecting protocol; each touch logged "Touch <n> of 5: <method>"; "No cold texts". Children D-2051, D-2052, D-2053. | Any free-site approach would be logged through this protocol. |
| D-2051 / D-2054 | active (conflict: candidate between them) | No Google listing photos on new demos after 2026-11-21 (stock or Tom's photos); 62 existing demos keep theirs. | A free site built now uses stock or Tom's photos until the owner supplies their own. |
| D-2052 | active | Preview stays up 2 weeks after the first logged visit or call; replaced the 36-hour rule (D-1952, superseded). | |
| D-2053 | deferred | Care plan not offered or mentioned. | A free site that later converts to a paid plan would need D-2053 revisited. |

Note: D-2053 (care plan) sits under D-2050 (prospecting protocol) as parent, although its component is `offer` and it is not a prospecting rule (inferred: a filing choice worth noting, not a conflict).

## 7. Open questions

- manage_open_questions (list, newest 50, open): all are owner-facing deal questions (hours, photos, logos, owner names) from Q-656 to Q-705; none concerns pricing, referrals or free sites. Lobanton alone has 11 open (Q-19 to Q-23, Q-37, Q-39, Q-40, Q-88 to Q-90, Q-269).
- No proposed decision touches the item (only D-2030, a massage trade definition, is `proposed`).

## 8. Pipeline and what is known about customers

Counts from list_opportunities, 2026-11-23:

| Stage | Count | Note |
|---|---|---|
| lead (researched) | 26 | |
| qualified | 96 | about a dozen of these have no live demo (chamber-directory clusters) |
| proposal | 1 | OPP-31 Lobanton |
| dormant | 1 | OPP-33 Mila Mía (not in context.md) |
| lost | 1 | OPP-43 Amaryllis |
| won | 0 | |

Demos live: 85. Every website deal is valued at USD 250.

**Stage labels under-record contact (inferred).** T-369 defines proposal as "link sent"; CLAUDE.reference.md line 16 defines it as "pitched". Logged interactions show demo links or prices sent to several owners whose deals still read `qualified`: Ale House Cigar Bar (I-168, I-169, email with "$250 price"), Still Fly Studios (Madison Hart, I-159, I-177, redesigned demo sent), Golden Ridge Stables (I-179, "Touch 1 of 5", co-owners Catherine and Jeff Behrens), Salon Persia (I-166, text to Nicholas). So "1 at proposal" understates how many owners have been pitched; it is roughly 5 to 6 owners reached with a demo (secretary's count from I-153 to I-179).

**OPP-31 Lobanton (the only proposal).** Restaurant in The Arcade Providence, 4.9 from 111 Google reviews, no website, orders only through DoorDash (and possibly Uber Eats). Owner Judy confirmed in person 2026-11-18 (I-153); "Their branding is different from the demo"; plan: send the demo, collect brand assets, send an updated preview. Demo link and brand-asset ask emailed 11-18 (I-156); second visit 11-19 (I-157, speaker not confirmed as Judy); v2 preview emailed 11-19 quoting "$250 flat, one-time" (I-158). Version 1 retired 11-20; current design on the original link. Next action "follow up with Judy for brand assets" was due 2026-11-20 and is **3 days overdue**; demo set to go offline **2026-11-27** (preview expires 2026-11-28 05:00 UTC). No reply from Judy is logged. Note: the 11-27 date was set under the old rule; under D-2052 (2 weeks after the first logged visit on 11-18) it would run through 2026-12-02 (inferred). Note also that asking for brand assets before payment departs from D-1951 (inferred; the terms record it as Tom's plan).

**OPP-43 Amaryllis (lost): why.** Not lost on price or offer. Research found the downtown BYOB restaurant's Instagram bio reads "Permanently Closed" and its listed website amaryllisri.com "Website Expired". Terms: "Researched only, no demo, never contacted." Closed 2026-11-18. It tells the board nothing about owner demand.

**OPP-33 Mila Mía (dormant).** Boutique in The Arcade, 5.0 from 38 reviews; looked closed on Tom's 11-18 visit; "Parked until confirmed." Demo offline.

**What owners have said (logged interactions, 11-18 to 11-21):**
- Lobanton: asked for the v2 demo by email (I-157). No decision logged.
- Still Fly Studios: Madison Hart "liked the site but said it isn't her branding" (I-159); Tom recreated her logo and redesigned; she was asked to review (I-177). She may introduce Tom to the Skittlez Ink owner, a shop being built out (I-165): an informal referral already in motion.
- Executive Cuts / Impulse Hair Designs: two stylists said they would pass both demo links to the owner; one mentioned the person who did their web work (I-173, I-174).
- Congress Tavern: the bartender who runs day to day declined the demo link for now; owners "not very involved" (I-171).
- A downtown law office: "staff at the door said they were all set" (I-167).
- Several stops with the owner out or busy (I-162, I-163, I-164, I-168, I-175).
- No logged objection to the $250 price; no logged acceptance either.
- Lauren received a call list of 29 prospects across Woonsocket, Worcester, Fitchburg, Gardner, Keene, Brattleboro and Bellows Falls (I-176, 2026-11-20).

**Areas covered.** Open Brain clusters go wider than context.md lists: Providence (Downtown, The Arcade, Thayer Street/College Hill, Providence Place, Regency Plaza), Woonsocket RI, Worcester Canal District, Fitchburg and Gardner MA, Greenfield and South Deerfield MA, Keene, Westmoreland and Walpole NH, Brattleboro and Bellows Falls VT.

## 9. Related projects and precedents

- yacht-ai, Burr Yacht Sales "free for life" dealer pilot (T-143, T-261): the scope was said verbally only; AJ Longmaid had not heard the offer; Tom ruled the written message must state the offer and scope together. Lesson: write a free offer's scope down before anyone repeats it.
- yacht-ai OPP-16, Apparent Winds: free membership for SV Resilience "in exchange for product feedback", aimed at a first influencer partner. Free-for-reach, written into deal terms; still at `proposal` since 2026-10-14.
- Brokkr go-to-market (T-200): given to businesses free as an organizational tool.
- yacht-ai referral system (D-810, D-812 active; payouts deferred, D-857).
- Lauren (lauren-ai, InsuredByHill): source of one earlier website-help referral (I-55).

## 10. Repo state

- Copy at commit 892a68d, 2026-11-21 ("Live demos keep their Google photos ..."). Recent work: chamber demos for Keene, Greenfield, South Deerfield, Brattleboro (5008143, 2444d6d); stock photos and 2-week previews (4cc721a); "Price first on every demo popup, what $250 includes, likely-buyer lead criteria, free-site groups, skills 1.3.0" (ea55768).
- Nothing in `src/` or `scripts/` implements free sites, referral codes or referral tracking (grep for "referr", "free site", "$50").
- docs/ob-changes.md lists Open Brain fields still "not yet" built, including `live_url`, `domain` and `referred_to_lauren` (under open-brain D-1962).
- Secret files were not read (none needed).

## 11. Gaps the board should know

1. The three anchors of the item (the $250 price, the $50 referral, the community free-site idea) live in the repo and thoughts, not as decisions. Any motion on them will create, not amend, decisions.
2. There is no referral tracking in Open Brain or the repo.
3. A credited free site cannot pass the production build as coded.
4. Zero paid sites: no evidence yet on close rate, delivery time per site or whether owners refer.
5. CRM stages understate contact made; pipeline figures are an inventory of demos, not of conversations.
