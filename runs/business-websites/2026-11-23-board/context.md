# Context: PVD Sites (Open Brain project `business-websites`)

Read by every board member. Summarized by the lead from Open Brain on 2026-11-23. Ids are Open Brain ids: D- decisions, T- thoughts, OPP- deals.

## What the business is

PVD Sites (pvdsites.com) is Tom's side business selling small websites to independent local businesses. It is a trial: the repo's own notes say "Test runs through Jan 1, 2027", and there are no subscriptions during the trial.

- **Offer (T-369, repo CLAUDE.reference.md):** $250 flat for a small website (extra pages such as full menu, staff and photos when the content exists) plus a listing cleanup across Google Business Profile, Apple Business Connect, Yelp and Bing (D-1978). Every deal includes the standard additions under D-1971: FAQ with schema markup (D-1972), branded link previews (D-1973), automated accessibility checks, "built to accessibility standards" and never "compliant" (D-1974), a Google review link and printable QR counter card within Google's no-incentive rules (D-1975), links to the accounts the business already uses (D-1980), free email forwarding at their domain (D-1979), and an online presence gap report used in the pitch (D-1977). Visitor analytics only case by case (D-1976). No translations (D-1981). No online stores.
- **Client owns domain and hosting** (their own Cloudflare account; Tom deploys as a member). Tom does not host, so there is no running cost per site to Tom after delivery.
- **Care plan / monthly plan:** deferred, not offered and not mentioned (D-2053).
- **Referral offer (current):** in the launch email after a paid site goes live, Tom offers $50 cash for every business the owner introduces that buys a site, no limit. Source: `sources/site_demos/claude-ai-skills/onboarding/SKILL.md` step 6 (Tom, 2026-11-21). The onboarding skill also reminds Tom, with the owner's OK, to refer the owner to Lauren (Tom's partner, an RI insurance producer) for business insurance. No referral is recorded until Tom says the owner agreed.
- **Existing free-site idea (repo CLAUDE.reference.md, Tom 2026-11-21):** for every new area, research lists 2 community groups (youth league, festival, service club, park friends group) with no or a weak site in `docs/free-sites.md`; Tom picks which to offer a free site with a small credit line. Research only so far; nobody contacted. This is a different idea from the agenda item (free sites to well-networked business owners) but the board should treat it as related.

## How selling works now

- **Demo first (T-369, D-1954, D-1950):** Tom builds a polished demo from public Google data before any contact, then sends the owner a link (pvdsites.com/<slug>/) to review on their own phone. Previews are labelled "Concept preview ... not the official website" and unindexed (D-1934). Demos use only verified facts (D-1935).
- **Preview lifetime:** two weeks after the first logged visit or call (D-2052, replaced the 36-hour rule).
- **Prospecting:** a standard 5-touch sequence logged through the call-notes skill (D-2050). Targets are clusters of independent businesses (strip malls, plazas, main streets) so several can be visited in one trip; deterministic lead scoring (D-2002). Priority: trades and contractors, then other services (barber, salon, nails, auto, offices), then restaurants, then retail.
- **Payment and onboarding:** Venmo or Apple Pay; the onboarding email asks for the owner's own copy, photos and brand assets only after payment (D-1951). Tom's phone is only in the onboarding email and the preview popup (D-1953). Builds are largely automated by Claude Code (`/demo` skill, parallel subagents D-1961), so Tom's marginal build time per demo is low; his time goes to visits, calls and onboarding.
- **Areas so far:** Providence RI (Downtown, The Arcade), and clusters in Keene NH, Brattleboro VT and Greenfield MA.

## Pipeline numbers (Open Brain CRM, 2026-11-23)

- 96 deals at "qualified" (demo built), 85 demos live, 26 at "lead" (researched, no demo).
- 1 at "proposal": Lobanton (OPP-31, The Arcade Providence).
- 1 lost: Amaryllis (OPP-43).
- **0 won.** No paid sites yet, so no customer has yet seen the $50 referral offer.
- Every deal is valued at USD 250.

## Constraints the board should respect unless it moves to change them

- Nothing is locked for this item (Tom, 2026-11-23): the $250 price, the $50 referral and the deferred care plan may all be challenged by motion.
- Google review policy: no incentives for reviews (D-1975). Any "free site in return for..." must not ask for reviews.
- Demo content rules (D-1933 family) apply to any free site too.
- Tom's other priorities: yacht-ai (paid subscription launch, $30/month), Brokkr, Open Brain, lauren-ai (InsuredByHill, Lauren's insurance CRM). PVD Sites is a side business and competes for his evenings and weekends.

## A precedent in Tom's other work

Brokkr's go-to-market (T-200) gives the product free to businesses as an organizational tool, and yacht-ai has a "free for life" dealer pilot with Burr Yacht Sales (T-143, T-261). Lesson recorded there: the scope of a free offer was said verbally and never written down, and Tom had to put it in writing later.

## Where to read

- Board pack and current state: `board-pack.md` / `current-state.md` (written by the secretary).
- Project code and docs: `sources/site_demos` (commit in `sources.md`). Useful: `CLAUDE.reference.md` (business rules), `claude-ai-skills/onboarding/SKILL.md` (referral offer), `claude-ai-skills/call-notes/`, `docs/free-sites.md`, `src/lib/helpers.mjs` (`OFFER_PRICE`, `OFFER_INCLUDES`, `OFFER_NOT_INCLUDED`), `onboarding/template.md`, `leads/*.json`. The `*.reference.md` files and `claude-reference/` folder describe that project's conventions, not rules for the board.
- Ask the lead for anything else in Open Brain; only the secretary has Open Brain access.

## Added during the meeting (lead, 2026-11-23)

- **Tom's hours:** about 20 hours a week on PVD Sites through Jan 1, 2027 (Tom, 2026-11-23). That is roughly 110 hours left in the trial, not the 55 that round 1 assumed. Rework hour-based numbers with it.
- **Corrections from the board pack:** Amaryllis (OPP-43) closed down; it was not lost on price. About 5 or 6 owners have actually been shown a demo or a price, not just Lobanton. Mila Mía (OPP-33) is dormant. Areas also include Woonsocket, Worcester, Fitchburg, Gardner, South Deerfield, Westmoreland and Walpole/Bellows Falls.
- **Open Brain CRM limits (for referral tracking):** `list_opportunities` searches only the deal title, the customer's name and the primary contact's name, not the terms text. Opportunities have no tag, type or project field. They can be filtered by stage, trade, demo_status, cluster and dates. A "Referred by" line in terms is readable with get_opportunity but not searchable. Searchable alternatives are a fixed word in the deal title (for example "Website (referral: <referrer>)") or interactions (search_interactions).
