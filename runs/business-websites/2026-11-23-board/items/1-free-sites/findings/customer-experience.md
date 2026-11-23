## Customer experience lead

### Bottom line
Up to 4 free business sites, not a dozen: 2 first, then 2 more only if the first two produce named introductions. Optionally, a community-group site counts inside that cap. Each is run in person: Tom signs the owner up at one visit, launches the site at the owner's counter, and at launch asks about neighbours he has already built demos for. Every other owner hears one rule instead of a second price: "$250, done, yours. Send me two neighbours who buy and yours is free." (Round 1 said a dozen, with a credit on every site. I changed both after team review; see below.)

### Customer journey (numbered moments with drop-off risks)

Whose words I used: the **owner's** words come from Tom's logged visits in the board pack, section 8: "liked the site but said it isn't her branding", "pass both demo links to the owner", "the person who did their web work", "all set". Owners talk about a *person* who does their website ("the person who did their web work"), not a studio. They say "my Google", not "listing". Tom's internal words ("listing cleanup", "presence gaps", "credit line", "D-1971 additions") stay off anything an owner reads. "Founding site" is my label for the board. To an owner, Tom says "one of my first few sites in town, no charge".

**Journey A: the founding-site owner (the free recipient)**

1. **Tom picks them.** They are owners who stand in front of other owners: a chair-side trade, a contractor who sponsors a league (Descavich Plumbing sponsors a Greenfield Girls Softball League team, per docs/free-sites.md), or an association officer (pricing's network score). *Drop-off risk (Tom's side):* he picks someone who has already seen "$250, done, yours." The popup on every demo opens by itself about 20 seconds in (src/contact.js line 128; src/lib/helpers.mjs line 311). Inside a cluster, that sets up two prices among neighbours who talk to each other (customer advocate; ops R5).
2. **The invitation, in person, with the demo on Tom's phone.** *Drop-off risk: "what's the catch".* One firm shut its free-website offer because many people thought it "was a scam" (Solveita). Tom should not lead with "free". He leads with the site they are already looking at. The popup will say $250, and he lets it: "Normally $250. I'm doing a few in town at no charge, and I'll ask you to introduce me to people." The $250 anchors the value. (This replaces my round 1 idea of changing the popup; see Changed after team review.)
3. **What they agree to: a one-page note, accepted by email reply.** Legal's item list and ops's terms cover it. Introductions are a hope, not a quota. Tom asks for no review of PVD Sites on any platform, not even an honest one (legal, row 2). *Drop-off risk:* vagueness. The Burr Yacht Sales pilot is the precedent (current-state.md section 9).
4. **Onboarding with no payment step.** Today the paid flow sends a 14-section email that says "$250" twice (onboarding/template.md). **This is the biggest drop-off in Journey A.** An owner who has paid nothing has no reason to work through that email (inferred). The fix is one sign-up visit. Tom takes the photos. The owner creates their Cloudflare account and buys the domain on their own card. The owner invites Tom as a Google Business Profile manager from their phone. Tom writes down the contractor registration number where the business needs one (legal, row 11). They set a launch date. Ops's 14-day asset deadline then has almost nothing left to wait on.
5. **Content.** Tom's own photos are allowed (CLAUDE.reference.md line 106), so the owner's photos can't stall the launch. Low risk after step 4.
6. **Preview approval.** The existing "1 to 10, what would make it a 10" question (call-notes step 7) works unchanged.
7. **Launch, at the counter.** Tom opens Google Maps on the owner's phone, searches the business and taps Website, and their own site opens. Then he hands over the review cards. *Drop-off risk today:* the launch is an email, so nobody is there for the reaction.
8. **The ask for referrals, made at that moment.** Today the launch email asks the open "Who else nearby would you introduce me to?" (onboarding SKILL step 6). Most people can't come up with names when asked cold, but they recognise names they're shown. So Tom brings 3 to 5 neighbours he has already built demos for and asks "do you know any of these owners? Mind if I say you sent me?" Pricing reached the same ask on its own. Tom also leaves a few of his cards with "Sent by <business>" written on the back.
9. **Second use: the owner shares their link.** The branded link preview (D-1973) shows their name and photo. Friends ask "who did that?" A business anchor's site carries no credit (see Changed), so this step depends on the owner remembering Tom. The cards from step 8 are what bridges it.
10. **Third use, about 30 days later.** Tom sends one text with the site's visit count (analytics on, per pricing M2) and asks again. Ops's timed asks at 14, 45 and 90 days set the cadence.

**Journey B: the referred friend**

1. **How they hear.** In person from the anchor ("talk to my website guy"), from the anchor's card, or from seeing the site. *Drop-off risk:* Tom's name gets lost between owners. The written card is the fix.
2. **Tom's first touch.** The demo-first flow suits a warm referral better than a cold one. Tom builds the friend's demo first, then opens with: "Madison at Still Fly said you were opening. I put this together for Skittlez." The talk point "Mention <name> sent you" comes from ops (no code needed). *Drop-off risk:* a cold 5-touch sequence and a 2-week takedown clock embarrass the referrer. Ops's warm sequence (M7) fixes this.
3. **What they see.** The banner and the popup ("I'm Tom. I made this preview so people who look up X find ...", then "$250, done, yours.") are fine for a warm friend. **Drop-off risk: the price clash.** The friend heard "he did mine for free." The fix is one line both the anchor and Tom say: "he did a few free to get started; it's $250 now, and if you send him two neighbours who buy, yours is free too." The rule that applies to everyone is what makes the clash survivable (pricing M4 and M5; advocate M2).
4. **They buy.** Payment, then the normal paid onboarding. Low risk.
5. **The referrer is credited and hears back.** *Drop-off risk: silence.* Someone who passes along a name and hears nothing doesn't pass along a second one. Ops's tracking runbook records the referral and the payout. My addition is that the referrer hears back within 2 days of the friend's **first** touch, not only when the friend buys.

### Refinements by version

"v1" means before the trial ends on Jan 1, 2027 (about 110 of Tom's hours left, per context.md), with each item buildable in days or done without a build. "v2" means after Tom rules the plan viable (the D-2053 trigger).

| # | Drop-off it fixes | Refinement | Version |
|---|---|---|---|
| 1 | A1 (two prices among neighbours) | Anchors come only from owners never sent a demo link or a price, in a cluster where nobody has been quoted $250. At most 4 in the trial, 2 at a time. | v1, no build |
| 2 | A2, A3 (catch, vagueness) | Invite in person with the demo on Tom's phone. Leave the one-page agreement; the owner accepts it by email reply. Never lead with "free". | v1, writing only |
| 3 | A4, A5 (onboarding stall) | One sign-up visit replaces the long email (photos, Cloudflare account, domain, Google invite, contractor number, launch date). A short confirmation email follows with no "$250" lines and no Lauren reminder. | v1, onboarding skill branch |
| 4 | A7, A8 (launch with nobody there, recall question) | Launch at the counter, then the named-neighbour ask and the "Sent by" cards. The launch email becomes the written record. | v1, no build |
| 5 | A9 (community-group site has no credit) | On the community-group site only, a plain-text credit, "Website by Tom at PVD Sites", with a mailto link whose subject is "Saw the <group> site". It contains no pvdsites.com and no followed link. It needs a tested allow-list at check-production.mjs line 148. Business anchors get no credit. | v1 if a community site is in the cap |
| 6 | B2 (cold touch on a warm lead) | The warm sequence: touch 1 names the referrer, at most 3 touches, a soft expiry (ops M7). | v1, skill text |
| 7 | B3 (price clash) | The line everyone hears, "two who buy and yours is free", said at the pitch and printed on the leave-behind card. | v1, card wording on Tom's word |
| 8 | B5 (silence) | A next action, "Tell <referrer> I've been to see <friend>", due 2 days after the friend's first touch. The payout next action and the reconcile come from ops M5. | v1, skill text |
| 9 | A10 (no third use) | Analytics on, and a day-30 text with the visit count plus the second ask. | v1 |
| 10 | Proof for the friend | "Sites I've made" on the studio page, listing live sites with the owner's OK (permission is in the agreement). | v1, after the first launch |
| 11 | Scale | Referral codes and links, a dashboard, automated payouts. | v2 at the earliest |

**Leave out of v1:** the Apple, Yelp and Bing cleanup on free sites; the presence-gap report; Tom buying domains; any review request, even for an honest one; a referral quota; a credit on business anchors; a changed popup; referral software; and changes beyond a 30-day error-fix window.

**What the free site includes** (the work is the advertisement): the full site as the paid version would be, with Tom's or the owner's photos; the branded link preview (D-1973); FAQ schema and the automated accessibility checks; the review button and QR card (D-1975, card wording unchanged); email forwarding (D-1979); the Google Business Profile website field; the contractor number where one applies; and analytics.

**Review card:** keep the wording exactly as it is (scripts/review-card.mjs). Restate "for paying clients" as "every delivered site". Put nothing about PVD Sites or referrals on it.

**Launch email:** for anchors, it becomes a written record of the counter launch: the live address, what was done, the neighbours they agreed Tom may name, and the line they can repeat. Voice.md line 12 says the phone number goes only in the onboarding email, but SKILL step 6.3.4 signs the launch email with it. Ops should reconcile the two.

### The moment worth telling a friend about

- **For the founding owner:** at the counter, they tap Website on their own Google listing and their site opens, with their photos and their hours, and staff come over to look. Then the review cards come out. That is when they'll show it off, and it is when Tom asks about named neighbours. v1 delivers this with no build, only the decision to launch in person (refinement 4). Tom should change the Google website field at the sign-up visit so it is showing by launch day (inferred lag, not checked).
- **For the referred friend:** "Madison sent me, and I already built yours." It is the demo-first flow played on a warm lead. v1 delivers it by building the friend's demo before the first touch and naming the referrer in touch 1 (refinement 6).

### Evidence

- Popup wording and timing: src/contact.js lines 31 to 33 and 128; src/lib/helpers.mjs lines 311 to 320; src/templates/sections.mjs lines 53 to 58.
- Production checks: scripts/check-production.mjs line 148 rejects the studio name, and lines 104 to 111 reject the preview domain (pvdsites.com) in any text file. Both read this round, confirming ops.
- Onboarding email length and its "$250" lines: claude-ai-skills/onboarding/email-template.md. Launch email and the $50: claude-ai-skills/onboarding/SKILL.md step 6. The phone contradiction: claude-ai-skills/voice.md line 12.
- Review card: scripts/review-card.mjs lines 1 to 4 and 15. Studio page with no real work shown: src/templates/studio.mjs lines 42 to 48 and 100 to 138.
- Teammates, round 1:
  - cfo.md: about 6.5 hours per site (a guess), 12 sites about 78 hours.
  - customer-advocate.md: two prices in a cluster; no owner has asked for free.
  - contrarian.md: about 6 owners actually pitched; referrals rewarded on the friend's side; Madison Hart referring unpaid.
  - ops-risk.md: tracking runbook, R5 price leak, R6 credit blocked, R8 skill run unchanged on a free site, R11 warm sequence.
  - pricing-gtm.md: cap of 4, the neighbours-list ask, the two-tier referral.
  - legal-regulatory.md: no reviews at all, a nofollow or plain credit, contractor numbers, keep Lauren apart, employee payouts.
- context.md (added during the meeting): about 110 hours left; Open Brain cannot search deal terms, but it can search a fixed word in the deal title or interactions.
- Outside, anecdotal: [Solveita closed free-site offer](https://tally.so/r/wvA8qg) ("thinking it was a scam"); [UK Business Forums thread](https://www.ukbusinessforums.co.uk/threads/looking-to-help-a-few-small-businesses-with-a-free-website.430754/).

### Confidence and gaps

- **Medium** on the drop-off points, which come from reading the actual flow. **Low** on whether anchors will refer: 0 paid sites, and one unpaid introduction in motion (I-165).
- **Hours.** At the CFO's 6.5 hours a site (a guess), 4 sites take about 26 of the roughly 110 hours left (24%). 12 would take about 78 (71%) and crowd out selling to the 96 qualified deals. The in-person visits roughly replace the email back-and-forth and the follow-up hours the CFO counted (my inference), but only when they fall on a trip Tom is already making. A dedicated trip to Greenfield, Keene or Brattleboro adds the CFO's $130 to $160 and half a day.
- **Credit allow-list.** The size of that change (about a day) is my inference; dev is not seated.
- **Not checked:** how fast Google shows a changed website field.

### Questions for Tom

1. Can you name 2 owners who have never been sent a demo link or a price, in a cluster you already visit, who sit on an association or sponsor list?
2. Will you do both the sign-up and the launch at the counter, on trips you are already making?
3. Free anchors already have their site free, so the first two referrals that would earn a paying owner $125 each don't apply to them. Is it $50 cash from their first referral on (my preference: one sentence), or nothing until their third (the CFO's preference)?
4. Is there a community group (the Greenfield Girls Softball League, or a group tied to a business association) worth one of the 4 slots, with a plain-text credit?

### Changed after team review

1. **A dozen down to at most 4, given 2 then 2 (pricing's cap and gate).** With 110 hours left, 12 sites take about 71% of Tom's time before any sale (CFO). Pricing's staging gives the referral question an answer at 2 sites. I had no counter-evidence to the hours case.
2. **No credit on business anchors. On a community site, a plain-text credit with a mailto link.** Ops showed the production build rejects "pvdsites.com" anywhere in the output (check-production.mjs lines 104 to 111) as well as the studio name (line 148). I confirmed both. Legal flagged footer credit links as possible link spam, and the advocate and ops showed a credit puts the free deal on public display. A mailto credit with no domain needs one allow-list change, and it is not a followed link. My round 1 credit, "Website by Tom · pvdsites.com", is withdrawn.
3. **Withdrew the popup change.** A popup saying "no charge" on a public link, which neighbours can forward, would broadcast the second price (advocate; ops R5). Leaving "$250, done, yours." in place anchors the value, and Tom explains the exception out loud.
4. **The price clash for the friend is handled by one rule everyone hears.** "Two neighbours who buy and yours is free" (pricing M4 and M5; advocate M2; CFO M3) gives every owner a path to the same outcome. That makes the anchors' free sites survivable inside a cluster. It replaces my give-or-get idea. The benefit for the referred business I now support is the contrarian's (M3), on the Gershon, Cryder and John finding that rewarding the person referred moves results.
5. **Legal's points adopted.** No review of PVD Sites from anchors at all. Introductions are a hope, not a quota: pricing M3's "3 named introductions within 30 days" should be worded as Tom's request, or it becomes the barter-income and "free with strings" problem legal raised in row 8. The contractor number is collected at the sign-up visit. Lauren never comes up in the free-site flow: the free-site onboarding branch drops the skill's Lauren reminder. Under the referral rule, an employee who refers their own employer is paid only with the owner's written knowledge.
6. **Tracking uses Open Brain as it is.** I drop the "Referred by:" line as the searchable record, because terms text is not searchable (context.md, added during the meeting). I join ops's runbook, using the title form the lead gives ("Website (referral: <referrer>)") or interactions. The "Sent by" cards stay as the physical cue, not the record.
7. **Anchor selection tightened.** Never anyone sent a link or a price. Never in a cluster where $250 has been quoted (advocate M5). Pricing's network score picks among those who are left.

### Final motions for the secretary

Proposer for each: customer experience lead. Each motion makes one change. "Joins" means I back another member's motion rather than adding a duplicate.

1. **Cap free business sites at 4 in the trial, given 2 then 2, with the gate on named introductions.** Joins pricing-gtm M1. A community-group site counts inside the cap. Touches: new decision under D-2050. Money: about 26 hours (a guess, at 6.5 each) instead of about 78, and $0 revenue from the anchors themselves. Risk: lower; Tom keeps about 84 hours for the pipeline.
2. **Anchor selection filter.** Anchors come only from owners never sent a demo link or a price, in a cluster where no owner has been quoted $250, chosen by pricing's network score (pricing M9). Joins customer-advocate M5 on the cluster rule. Touches: D-2002 (a filter on top), D-2050. Money: $0. Risk: removes most of the two-price leak (ops R5), but may leave few candidates; Tom has to name 2.
3. **Written one-page agreement, accepted by email reply, before any free build.** Joins legal-regulatory M1 (same as ops M4, pricing M3 in part). Touches: D-1971, D-1979, D-2053. Money: $0, plus an optional lawyer review at $300 to $750 (legal's guess). Risk: closes the verbal-scope gap (T-143).
4. **What "in return" may and may not be.** Allowed: voluntary introductions, portfolio use, a labelled quote. Never: a review, an insurance purchase, a quota. Joins legal-regulatory M2. Touches: D-1975. Money: $0. Risk: removes review-removal and barter risk. Pricing M3's introductions ask should be reworded as a request.
5. **Free-site scope.** The full site with the D-1971 additions and the Google Business Profile website field; no Apple, Yelp or Bing cleanup; the owner pays for the domain; a 30-day error-fix window; analytics on. Joins pricing-gtm M2. Touches: D-1971, D-1975, D-1978, D-1976. Money: saves about 1 to 1.5 hours a site (the CFO's listing-cleanup line). Risk: low.
6. **Assets and Tom's phone are triggered by written acceptance when there is no payment.** Joins ops-risk M2. Touches: D-1951, D-1953. Money: $0. Risk: removes a certain rule conflict.
7. **A free-site branch in the onboarding skill: one sign-up visit instead of the 14-section email.** At the visit: Tom's photos, the owner's own Cloudflare account and domain, the Google manager invite, the contractor number, a launch date. Afterwards, a short confirmation email with no "$250" lines and no Lauren reminder; the deal is logged at value 0 (ops R8). Proposer: me. Touches: D-1951, D-1953 (through motion 6); onboarding skill 1.3.0 to 1.4.0 (no D-id). Money: about neutral in hours against email chasing on an existing trip (inferred); $130 to $160 per dedicated trip otherwise (CFO). Risk: the main stall in Journey A drops sharply; it depends on Tom being on site.
8. **Launch free sites at the counter, and ask about named neighbours there.** Tom brings 3 to 5 neighbours with built demos and leaves cards marked "Sent by <business>". The launch email becomes the record. Proposer: me; the neighbours-list ask joins pricing-gtm M3. Touches: onboarding SKILL step 6 (no D-id), D-2050. Money: about 0.5 hours on an existing trip. Risk: an open recall question becomes recognition of names on a list; it depends on Tom's presence.
9. **Credit only on a community-group site, as plain text with a mailto link.** "Website by Tom at PVD Sites" with the subject "Saw the <group> site": no pvdsites.com, no followed link, removable by the owner. It needs an allow-list for that one string at check-production.mjs line 148, with a test. No credit on business anchors. Joins ops-risk M3 (no credit on business sites); the form follows legal's row 12. Touches: D-2005; the community free-site rule (CLAUDE.reference.md line 12, no D-id). Money: about a day of dev time (inferred). Risk: gives the sponsor audience a way to reach Tom with no link-spam exposure.
10. **Referral tracking runbook in Open Brain as it is.** The referral goes in the deal title ("Website (referral: <referrer>)") or an interaction, with a payout next action and a monthly reconcile. Joins ops-risk M5 (and pricing M7 on the rules). Touches: D-2050, D-1962 (open-brain). Money: $0. Risk: no double or missed payouts (ops R9).
11. **The referrer hears back.** A next action, "Tell <referrer> I've been to see <friend>", due 2 days after the friend's first touch, as well as the payout when the friend buys. Proposer: me. Touches: D-2050; call-notes skill (no D-id). Money: a 2-minute text per referral. Risk: referrers who never hear back stop referring; this makes a second referral more likely.
12. **Warm sequence for referred businesses.** Touch 1 names the referrer, at most 3 touches, a soft expiry. Joins ops-risk M7. Touches: D-2050, D-2052. Money: fewer touches per referred lead. Risk: protects the referrer's standing.
13. **The referral offer goes to anyone and is said at the pitch.** "$250, done, yours. Two neighbours who buy and yours is free", then $50 each, and $50 to anyone who is not a customer. An employee who refers their own employer is paid only with the owner's written knowledge. Joins pricing-gtm M4 and M5 (also customer-advocate M1, cfo M2, and legal M4 for the terms). Touches: new referral decision (no D-id today); the OFFER_* constants and card, on Tom's word. Money: $125 net per referred sale on the first two tier, $200 net after (pricing). Risk: one rule removes most of the friend's price clash.
14. **A benefit for the referred business.** Joins contrarian M3. Touches: the new referral decision. Money: $25 to $50 less margin per referred sale. Risk: low; this is the half of the referral the research says moves results.
15. **Contractor registration numbers on every contractor site, collected at the sign-up visit.** Joins legal-regulatory M6. Touches: D-1935, D-1971. Money: $0. Risk: removes a fine risk for the client.
16. **Keep Lauren's referral out of anything free.** Joins legal-regulatory M5; motion 7 removes the reminder from the free-site branch. Touches: new decision, D-2050. Money: $0. Risk: protects Lauren's license.
17. **"Sites I've made" on the studio page.** Live sites only, with the owner's OK from the agreement, added after the first launch. Proposer: me. Touches: none (src/templates/studio.mjs; the rule that the studio page never links to previews stands). Money: about an hour of build (inferred). Risk: gives a referred friend who looks Tom up something real to see; the mock "Your business" page is all there is today.
18. **Day-30 text with the visit count, plus the second introductions ask.** Proposer: me; analytics-on joins pricing-gtm M2, and the timing fits inside ops's 14, 45 and 90 day asks. Touches: D-1976. Money: about 5 minutes per site. Risk: gives the owner a reason to come back and something to brag about.

**Withdrawn from round 1:** the founding-offer popup variant (it would broadcast the second price) and the "Website by Tom · pvdsites.com" credit on business sites (the build blocks it, it risks link spam, and it puts the free deal on display). The give-or-get referral is replaced by joining contrarian M3.
