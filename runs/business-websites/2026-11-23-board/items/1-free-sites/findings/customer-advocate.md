## Customer advocate

Agenda item 1: free sites for a dozen or so well-networked business owners, in return for referrals. Round 1 and round 2, 2026-11-23.

### Bottom line

No owner has asked for a free site, and the one real referral (I-165) came from a free demo, so I would make "free" something every owner can earn: $250, and "two neighbours who buy and yours is free". I would also pay $50 to anyone outside the buying business, let owners pay once the site is live, and keep giveaways to community groups. If the board still wants free business sites, nobody already quoted $250 should get one, and a neighbour should never find out about a free site that wasn't stated publicly and couldn't also be earned.

### What customers have said

All of this comes from Tom's logged interactions, 2026-11-18 to 11-21, as the secretary summarised them in current-state.md section 8. These are Tom's notes in his own words, not owners' words. There are no verbatim owner quotes, no paying customers and no reviews.

- **Madison Hart, Still Fly Studios:** "liked the site but said it isn't her branding" (I-159). Tom recreated her logo and redesigned the demo (I-177). She **may introduce Tom to the Skittlez Ink owner**, whose shop is being built out (I-165). This is the only owner-to-owner referral in the pack. It came after a free demo, with no free site and no cash offered. Whether Tom asked for it is not recorded. Under today's rule she would get nothing for it, because the $50 goes only to owners whose paid site is live (onboarding SKILL.md step 6).
- **Judy, Lobanton (OPP-31, the only deal at proposal):** "Their branding is different from the demo" (I-153). She asked for the v2 demo by email (I-157) and was quoted "$250 flat, one-time" (I-158). She has not replied since. The follow-up has been overdue since 11-20, and the preview is set to come down 11-27/28.
- **Executive Cuts / Impulse Hair Designs:** two stylists said they would pass both demo links to the owner, and one mentioned "the person who did their web work" (I-173, I-174). So an incumbent web person exists in that network.
- **Congress Tavern:** the bartender who runs the place day to day declined the demo link for now. The owners are "not very involved" (I-171).
- **Downtown law office:** "staff at the door said they were all set" (I-167).
- **Ale House Cigar Bar:** sent an email with the "$250 price" (I-168, I-169). No reply is logged.
- **Golden Ridge Stables (Catherine and Jeff Behrens), Salon Persia (Nicholas):** reached at Touch 1 (I-179, I-166). No response is logged.
- **Price:** "No logged objection to the $250 price; no logged acceptance either" (current-state.md section 8).
- **$50 referral offer:** no owner has seen it. It goes out only in the launch email after a paid site, and there are 0 won deals.
- **Free sites:** no owner has asked for one. The pack has no record that free, discount or "can't afford it" ever came up.

**Public owner sentiment on free websites** (not PVD Sites customers; I use it only to show how "free" tends to read):
- UK Business Forums, on a designer offering free small-business sites: "it looks like you are offering 'only pay if you use it' rather than an actual free site?" (Mark T Jones). Another poster warned that owners got sites "without realising they couldn't do anything without the developer" (Paul Kelly ICHYB). The reply that suggested what to ask for in return proposed "a reduced first-project rate in exchange for a written testimonial and permission to case-study the build" (john_brown).
- Brighton Chamber of Commerce advice to members: "There is usually a reason why people offer their services for free and more often than not, it's quality that suffers." And: "If you don't own your own website you could end up losing it."
- A search summary of a Reddit r/webdevelopment thread (I could not load the thread itself) gave the common suspicion as: a free build, then "lock you into expensive hosting", and "you typically won't own your domain". Treat this as secondhand.

What these show (inferred): owners read "free" as a sign of hidden lock-in or lower quality. Tom's model already answers both: the client owns the domain and hosting, and there is no monthly fee. That only helps if the answer is written into the offer.

### Customer effect of each motion

I tested four options against four groups: the free-site recipient, the friends they refer, owners who were quoted $250, and community groups.

**Option A: a dozen free sites to well-networked business owners, as the agenda puts it.**
- *Recipient:* pleased, but it reads as a catch unless the scope is in writing. The obvious question is "what do I owe you?" If the expected referrals go unsaid, they are a hidden string. If they are said, some owners will find it awkward to be told to sell to their friends (inferred). "Free" is also not free to them. They still create a Cloudflare account and pay their own domain renewal, roughly $10 to $15 a year for a .com. That figure is my guess; the pack records no domain cost. Tom would need to tell them: they own it, there is no monthly fee, the domain costs them about $X a year, here is exactly what is included, and nothing is asked in return except that, if they like it, they tell people. Under D-1975 the deal must not ask for reviews.
  - Would they thank Tom or leave? They would thank him. Whether they refer anyone is unknown, and the pack has no evidence either way.
- *Friends they refer:* they hear "Tom did mine for free" and anchor at $0. Then Tom quotes $250. Some will ask for the same deal, and some will feel they were brought in as paying customers after the friend got the gift (inferred). To avoid that, the recipient needs a line to repeat ("he did a few free to get started; it's $250 now") and the printed leave-behind card with the price on it. The card already uses `OFFER_PRICE` (CLAUDE.reference.md line 30).
- *Owners quoted $250:* this is my main objection. Tom prospects by cluster on purpose: strip malls, The Arcade, Regency Plaza, main streets (D-2002). The same closeness that makes referrals spread also makes two prices visible. Judy at Lobanton has been quoted $250 in The Arcade, and Ale House has been emailed $250. Every one of the 85 live demos opens its popup with "$250, done, yours." (helpers.mjs). A neighbour who gets the site free would leave those owners in one of three places:
  - asking why they pay;
  - waiting to see whether they get it free too;
  - if they have already paid, asking for their money back or telling neighbours about it.
  - Would they thank Tom or leave? Owners who paid would feel cheated. Those mid-pitch would stall.
- *Who notices first:* the neighbours of whoever gets the free site, and Lauren, who is working a 29-prospect call list (I-176) on the $250 offer.

**Option B: free sites to community groups only (the existing docs/free-sites.md idea).**
- *Recipient (for example the Greenfield Girls Softball League, Friends of India Point Park):* reads as generous. A volunteer group has no budget, so "free" has an obvious reason and does not look like a catch. They still need the written scope: who owns the domain, who updates the site after delivery, and what happens when the volunteer contact changes (inferred; volunteer groups turn over).
- *Friends they refer:* the people who see it are sponsors and members. For the softball league that is about 10 sponsoring businesses, including **Descavich Plumbing, which also has a live $250 demo (OPP-126)**. I don't think a sponsor resents a free site for the kids' league, and it may make Tom look like part of the community (inferred).
- *Owners quoted $250:* no price conflict, because a nonprofit is a different kind of customer. Descavich would see Tom's work on a site he already cares about.
- *Catch to fix:* the "Site by PVD Sites" credit cannot ship through the production build as coded (scripts/check-production.mjs line 148). Without the credit, the sponsors never learn who built it.

**Option C: no free business sites. Pay $50 to anyone who introduces a buyer, and tell owners that five buyers repay their site.**
- *Recipient (any owner who refers):* the "free site" is earned, the same rule applies to everyone, and nothing has to be explained. Madison Hart's introduction (I-165) would count today. Under the current rule it does not, which is unfair to the one owner actually referring.
- *Friends they refer:* the price is the same for everyone, so nothing about it surprises them. They hear "he's good, it's $250" from someone they trust.
- *Owners quoted $250:* no conflict, and they get a way to earn their money back.
- Would they thank Tom or leave? They would thank him. The cost is $50 per closed sale, paid only when there is revenue.

**Option D: a named, public, written "first sites in town" offer, as a discount for a testimonial and permission to show the site (the john_brown suggestion above).**
- Recipients are not suspicious, because the reason is stated and the offer is public. It is still a second price inside clusters. It also costs Tom his evidence: with 0 paid sites and the trial ending 2027-01-01, discounted closes would not show whether owners pay $250 (inferred). Better than A, worse than C.

**Round 2: teammates' plans tested against owners**

- **Customer experience: about 12 in-person "founding sites", with a per-lead popup that hides the $250** (customer-experience.md, refinements 1 to 10).
  - Much of the journey is right for owners, and I back it:
    - Launch at the counter.
    - Ask by recognition ("do you know any of these owners?") rather than recall.
    - Name the referrer in the friend's first touch.
    - Tell the referrer when their friend goes live.

    That last point fixes the thing a referrer is most likely to resent: silence.
  - Twelve is the problem. At one per cluster, almost every cluster (about 15 in the pack) ends up with a "he did mine for free" story. That is the widest possible spread of a $0 anchor among exactly the neighbours who hold $250 demos.
  - The popup flag is not deception in itself. Showing "no charge" on the recipient's own link is more honest than showing $250 to someone who has been told it's free. But demo links do travel: staff pass them to owners (I-173, I-174). So the flag is acceptable only if the founding offer is also stated publicly ("one of my first sites, no charge"), and never inside a cluster where $250 has been quoted.
  - Cx's own guardrail (only owners never sent a link or price) is right. Because the popup opens by itself at about 20 seconds, it in practice rules out anyone who has opened a demo.
- **Pricing: 4 anchors chosen by network score, plus "two neighbours who buy and yours is free" for every buyer** (pricing-gtm.md, sections 2 and 3).
  - The universal earn-back is the best owner-facing idea on the board. It is one sentence at the counter, it applies to everyone, and nobody has to be told a secret. "Two" is within an owner's reach; my round-1 "five buyers repay it" was not. I'm withdrawing my version and joining this one.
  - It also answers the friend-anchoring problem. The referred friend gets the same chance to earn theirs back, so "he did mine for free" becomes "he did mine, and you can get yours free the same way".
  - The anchors are the weak part for owners. Pricing places them on Greenfield and Keene Main Street precisely because 7 neighbours there already hold demos, and every one of those popups says $250. That is tolerable only if the earn-back is in force first, so an anchor's free site reads as "he was first", not "he got a deal you can't".
  - Conflict with legal: pricing's first-ten plan says "Each stylist gets $50 if their owner buys" (I-173, I-174). Legal row 6 says that may be commercial bribery in RI and MA. It is also a fair grievance for the owner: an owner who finds out Tom paid their staff to push his site would feel worked on (inferred). Legal should win this one.
- **Ops: 3-site pilot, written terms, outside active clusters** (ops-risk.md, Option B, M1).
  - For owners this is the safest form of a business giveaway: a small number, written terms and away from neighbours holding $250 quotes.
  - Its weakness is the mirror of pricing's. Outside the clusters, the recipient's network is not the neighbours Tom has built demos for, so the referral value is lower (inferred).
  - Ops's warm sequence for referred businesses (M7) is a clear owner win. A friend who was sent by someone they trust should not get the cold 5-touch sequence and a takedown clock, because that embarrasses the referrer.
- **Contrarian: pay-when-live** (contrarian.md, motion 2).
  - This answers the top unaddressed ask in my round-1 file. Owners would get their own branding on the site before paying, because assets follow a written yes instead of payment. The two owners closest to buying both raised branding (I-153, I-159).
  - It also removes the one "catch" the paid offer has: Venmo $250 to a stranger before anything exists. No owner has logged that objection, but no owner has been asked to pay yet either.
  - The owners would thank Tom for it. The risk is Tom's hours on a site that never gets paid for. Tom doesn't host, so nothing costs him money afterwards.
- **Legal: no $50 to the buying business's employees without the owner's written knowledge** (legal-regulatory.md, row 6 and motion 4).
  - Checked against my round-1 motion 1 ("pay the $50 to anyone"): it needs that limit.
    - Madison Hart introducing Skittlez Ink is fine. She owns a different business (I-165).
    - The Executive Cuts and Impulse stylists (I-173, I-174) are the case legal flags, if they are employees of the salon that would buy.
  - Many stylists rent their chair and are their own business. That is inferred and not in the pack, so Tom needs to know which these are.
  - From the owner's side I would go one step further than legal: Tom should not offer cash to staff at the door at all. He should thank staff another way, by telling the owner who passed the link on. The owner-consent route legal allows means asking an owner "may I pay your stylist?", which is an awkward first conversation with a buyer.
- **CFO: earn-back limited to 3 founders.** The mechanism is the same as pricing's, but limiting it to 3 hand-picked owners recreates the favouritism problem. I prefer pricing's version for every buyer.
- **Hours (context.md: 20 h/week, about 110 h left).** This weakens the capacity objections from CFO, ops and contrarian. It does not touch my objection, which rests on what neighbours see, not on Tom's hours.

**Is "free for a networked owner" generous or a catch?** To the recipient, it is generous if written down and a catch if unwritten. To that owner's neighbours who were quoted $250, it looks like favouritism either way. To friends who are referred, it is an anchor at $0. Free for a volunteer group reads as generous to everyone.

### Unaddressed customer asks

1. **Seeing their own branding before deciding.** The two owners closest to buying both raised it: Madison Hart (I-159) and Judy at Lobanton (I-153). D-1951 asks for brand assets only after payment, and Lobanton's brand-asset ask already departs from it (current-state.md section 8). No option on the agenda addresses this, and it is the objection I would expect to block a close, more than price.
2. **A reward for a referral that is already happening.** Madison Hart's possible introduction of the Skittlez Ink owner (I-165) has no reward and no record. She is not a paying customer, and there is no referral tracking (current-state.md section 4). The first owner who refers should not be the first one to go unthanked.
3. **The website help Tom may owe Gail Ahlers, The Empowerment Factory (nonprofit, referred by Lauren, I-55, T-209).** It is an open question with no recorded outcome. If the board approves free community sites, she is an existing ask that should come before cold-picked groups.

**After round 2:** ask 1 is now covered by contrarian's motion 2 (pay-when-live, with assets after a written yes), and ask 2 by CFO's motion 2 and pricing's motion 5 ($50 to anyone). These three asks remain uncovered:

1. **Gail Ahlers / The Empowerment Factory (T-209).** No teammate picked it up. It is an existing request that came through Lauren, and it should be settled before Tom cold-approaches a new group.
2. **A legal way to thank staff who pass links on.** The stylists at Executive Cuts and Impulse (I-173, I-174) are doing the introducing, and legal's rule takes cash off the table for them if they are employees. Nothing yet gives them a thank-you that is allowed.
3. **Owners who are never there.** Five or more stops found the owner out or busy (I-162 to I-164, I-168, I-175), and at Congress Tavern the owners are "not very involved" (I-171). Every referral motion assumes an owner in conversation. None of them gives staff something for the absent owner to see, beyond the existing leave-behind card.

Also time-sensitive: Lobanton's preview comes down 11-27/28 while Judy's follow-up is 3 days overdue. Under D-2052 it could run through 12-02 (current-state.md section 8). That is the only live proposal.

### Evidence

- current-state.md section 8: interactions I-153, I-156 to I-159, I-162 to I-177, I-179; pipeline counts; "No logged objection to the $250 price".
- current-state.md sections 4 and 5: $50 offer terms, no tracking, community free-site list, Descavich in the softball league, Gail Ahlers (I-55, T-209).
- sources/site_demos/claude-ai-skills/onboarding/SKILL.md step 6: $50 only in the launch email after a paid site; "for every business that buys, not just one, with no limit".
- sources/site_demos/CLAUDE.reference.md lines 6 to 15 and 30: offer, cluster targeting, the price shown first on every popup and on the leave-behind card.
- sources/site_demos/docs/free-sites.md: credit line, group picks, softball league sponsors.
- context.md: Burr Yacht Sales lesson (T-143, T-261), where the scope of a free offer was said aloud and had to be written later.
- Public: UK Business Forums thread; Brighton Chamber article; search summary of a Reddit r/webdevelopment thread (could not load directly).

### Confidence and gaps

- **Low confidence on whether networked owners refer at all.** The evidence is one possible introduction (I-165), from 5 to 6 owners pitched, with no paying customers. Nobody has been asked whether a free site, $50 or anything else would get them to refer.
- **High confidence that two prices in one cluster will be noticed.** This is inferred from how clusters are targeted (D-2002), not observed. No free site exists yet.
- **No verbatim owner words.** Every owner line is Tom's note as summarised by the secretary. I have not read the raw interaction bodies; the lead can fetch them from Open Brain.
- **The quickest way to get evidence (about a week, during touches Tom is already logging under D-2050):** ask Madison Hart, Judy, the Behrenses, Nicholas at Salon Persia and Ale House three questions:
  1. "Is $250 fair?"
  2. "Who would you send to me?"
  3. "Would $50 cash, or your site paid back after five, make you more likely to?"

  Log the answers through call-notes. The first paid launch email is the first real test of the $50 offer.

### Questions for Tom

1. Did Madison Hart offer the Skittlez Ink introduction on her own, or did you ask? What would she want for it?
2. Do you have the dozen names in mind? Are any of them in a cluster where you have already quoted or shown $250 (The Arcade, Regency Plaza, Keene, Greenfield)?
3. Would you be comfortable with every recipient's neighbours knowing their site was free? If not, it is a secret, and secrets leak in strip malls.
4. Has any owner said $250 is too much, or asked for a deal, without it being logged?
5. Do you owe Gail Ahlers website help (T-209)?
6. Are the Executive Cuts and Impulse stylists (I-173, I-174) employees of the salon, or do they rent their chairs? Legal's employee rule turns on it.

### Changed after team review

1. **I withdrew "five referred buyers repay the site" and joined pricing's two-tier earn-back** ($125 back on each of the first two referred sales, then $50; pricing-gtm.md motion 4). Two buyers is reachable for an owner and five is not, and it lets the referred friend earn the same deal. Source: pricing-gtm.md, section 3.
2. **I narrowed "$50 to anyone" to anyone outside the buying business**, following legal's commercial-bribery flag (legal-regulatory.md row 6). Staff of the buying business are paid only with the owner's written knowledge. My owner-side preference is not to offer cash to staff at all.
3. **My brand-match motion now joins contrarian's pay-when-live motion** (contrarian.md motion 2). It delivers the same thing, assets before payment, and more.
4. **I moved from "no free business sites, full stop" to "no free business sites in the trial, plus fallback conditions if the board approves some anyway".** The conditions:
   - the universal earn-back is already in force;
   - the recipient has never been sent a link or price;
   - at most one per cluster;
   - the offer is stated publicly.

   Why: cx's "first sites, no charge" framing and pricing's universal earn-back answer most of the favouritism problem, and no owner has yet paid $250 in reliance on the price. Sources: customer-experience.md refinements 1 to 3; pricing-gtm.md section 3. My preference is unchanged.
5. **The unaddressed asks are updated** (see that section). Two of my three round-1 asks are now covered by teammates' motions.
6. **Hours (context.md, 20 h/week):** no change to my position. My objections were never about Tom's hours.
7. **Flag for the lead and pricing:** pricing's first-ten plan pays the stylists $50, which conflicts with legal row 6. I could not message pricing, so it is recorded here.

### Motions I would propose (round 1, superseded by "Final motions for the secretary" below)

These were my round-1 motions, one change each.

1. **Pay the $50 referral to any owner who introduces a business that buys, paid customer or not, and record the referrer when the introduction is made.** Touches D-2050, since call-notes logs the introduction as a touch; it creates the first referral decision, because the $50 has no D-id today. Why: Madison Hart (I-165) is referring now and is not eligible. Money: $50 per closed $250 sale, paid only out of revenue. Risk: low.
2. **Say plainly in the launch email and on the leave-behind card that five referred buyers repay the owner's $250.** This creates a decision under the new referral decision; the wording of `OFFER_*` changes only on Tom's word. Why: it gives the "free site" Tom wants to offer to every owner on the same rule, with no second price. Money: the same as motion 1. Risk: the owner reads it as a sales pitch. Keep it to one line.
3. **No free sites to for-profit businesses during the trial (through 2027-01-01). Revisit once 3 paid sites have launched.** Creates a decision; leaves the $250 untouched. Why: two prices in the same clusters (D-2002) where 85 demos and at least two direct quotes say $250. Money: nothing given up, since no revenue exists yet. Risk: Tom loses a possible fast route to referrals that the evidence neither supports nor rules out.
4. **Free sites go to community groups only: one per area, Gail Ahlers first if help is owed, then the softball league, with the scope written down before any offer.** The scope states that the group owns the domain, that the site is the D-1971 package except the review QR card and listing cleanup (D-1975, D-1978), that there is no monthly fee and no care plan (D-2053), what Tom does after delivery, and that nothing is asked in return. Touches D-1971, D-1975, D-2053, plus the build's studio-credit check. Why: it reads as generous to everyone, and sponsors such as Descavich see the work. Risk: Tom's hours (CFO); the credit line needs a code change.
5. **If the board does approve free business sites:** a one-page written scope before anyone is approved, never inside a cluster where $250 has been quoted, and a stated line for recipients to repeat ("it's $250 now"). Touches D-1971, D-1975, D-1951 and D-1953 (asset collection and Tom's phone need a trigger other than payment). Why: the Burr Yacht Sales lesson (T-143, T-261), and the "what's the catch" reading. Risk: still a second price.
6. **Brand match before payment, within D-1935's verified-content rule: when an owner shares their logo or colours, the next preview uses them.** Amends D-1951. Why: the top unaddressed ask (I-153, I-159). It is outside this item, so it may go to a later agenda.

Sources:
- [UK Business Forums: Looking to help a few small businesses with a free website](https://www.ukbusinessforums.co.uk/threads/looking-to-help-a-few-small-businesses-with-a-free-website.430754/)
- [Brighton Chamber: 5 things to consider before accepting a free website](https://www.brightonchamber.co.uk/blog/5-things-consider-accepting-free-website)
- [Reddit r/webdevelopment thread, via search summary only](https://axebps-redlib.hf.space/r/webdevelopment/comments/1jqrmfg/i_need_a_website_and_people_keep_offering_to_make)

### Final motions for the secretary

One change each. Where a teammate proposed the same change, I join theirs rather than duplicate it. Cash and hour figures come from the named teammate's file, and every hour figure is a guess (no site has been delivered).

1. **Hold free sites for individual business owners until after the trial** (none before 2027-01-01; revisit once 3 paid sites have been delivered). **Joins CFO's motion 1.**
   - D-ids: creates a new decision; no existing D-id.
   - Money: no revenue is given up, because there is none yet. It avoids up to about 12 deliveries of Tom's time (CFO estimate, about 78 h).
   - Risk, owner side: it removes the two-price problem in clusters where 85 demos and at least two direct quotes (I-158, I-168/169) say $250. It costs a possibly faster route to referrals, which the evidence neither supports nor rules out.
2. **Fallback, only if motion 1 fails: the conditions on any free business site.** Proposer: customer advocate; conditions (b) and (c) join cx's motion 3.
   - The conditions:
     - (a) The universal earn-back (motion 4) is already in force, so every neighbour can earn the same thing.
     - (b) The recipient has never been sent a demo link or a price.
     - (c) At most one per cluster.
     - (d) It is stated openly as "one of my first sites, no charge", with a line the recipient can repeat to friends ("it's $250 now, and two who buy makes yours free").
     - (e) The count is capped as ops's M1 sets it (3), not 12.
   - D-ids: new decision; touches D-2002 (it filters on top of scoring) and D-2050.
   - Money: about 5 to 7 h per site (ops guess), $0 cash.
   - Risk: it is still a second price. The conditions keep it public and reachable, so a neighbour sees "he was first", not favouritism.
3. **$50 to anyone who introduces a business that buys, not only to paying customers, said at the pitch and on the leave-behind card.** **Joins CFO's motion 2** (the same change as pricing's motion 5), subject to motion 5 below.
   - D-ids: creates the first referral decision; touches D-2050.
   - Money: $0 up front, about $200 net per referred sale.
   - Risk: low. Madison Hart's introduction (I-165) qualifies immediately.
4. **Two-tier earn-back for every buyer: $125 back on each of the first two referred sales, then $50 cash, with no limit.** **Joins pricing's motion 4.** I prefer this for every buyer, not CFO's motion 3, which limits it to 3 founders.
   - D-ids: new decision under the referral decision; changes onboarding SKILL step 6.
   - Money: never negative on cash. It costs $150 more per buyer than flat $50, and only after $500 of referred sales.
   - Risk: an owner may read it as a sales pitch. Keep it to one line.
   - My round-1 "five buyers repay it" is withdrawn.
5. **No $50 to staff of the buying business without the owner's written knowledge; one payout per buying business, to the first introducer; every payout logged.** **Joins legal's motion 4.**
   - D-ids: new decision (the referral terms); relates to D-2050.
   - Money: none. The rule governs who gets the existing $50.
   - Risk: it removes the commercial-bribery exposure (RI §11-7-4, Mass. c.271 §39) and the grievance an owner would have on finding their staff had been paid.
   - Owner-side note for the secretary: I would rather Tom not offer cash to staff at all, and thank them by telling the owner who passed the link on. Pricing's plan to pay the I-173/I-174 stylists conflicts with this rule.
6. **Pay-when-live option: an owner may pay once the site is live at their address, and assets, brand and Tom's phone follow a written yes rather than payment.** **Joins contrarian's motion 2.** It covers my round-1 brand-match motion; ops's M2 makes the same trigger change for free sites.
   - D-ids: amends D-1951 and D-1953.
   - Money: revenue arrives later, and some sites may go unpaid. There is no hosting cost to Tom.
   - Risk: Tom's hours on unpaid sites, which a small cap bounds.
   - It answers the branding ask both near-buyers raised (I-153, I-159).
7. **Referred businesses get a warm sequence: touch 1 names the referrer, at most 3 touches, a soft expiry, nothing negative reported back.** **Joins ops's M7.**
   - D-ids: touches D-2050 and D-2052.
   - Money: none.
   - Risk: removes the embarrassment a referrer would feel if their friend got the cold 5-touch sequence and a takedown clock.
8. **Close the loop with the referrer: a "Referred by:" line, a "Tell <referrer> <friend> is live" action within 2 days, and the payout within 7 days.** **Joins cx's motion 8** (the tracking mechanics are ops's M5).
   - D-ids: touches D-2050.
   - Money: none.
   - Risk: low. Silence is what stops a second referral.
9. **A written agreement before any free site, accepted by email reply.** **Joins legal's motion 1** (the same as ops's M4 and cx's motion 1).
   - From the owner side it must say plainly that the owner pays their own domain renewal, and that nothing is owed (no review, no quota, no insurance).
   - D-ids: new; relates to D-1971, D-1975, D-1979 and D-2053.
   - Money: $0, plus an optional $300 to $750 lawyer review (legal's guess).
   - Risk: removes the "what's the catch" reading and repeats none of the Burr Yacht Sales mistake (T-143, T-261).
10. **Community giveaway as a capped, written pilot: 2 or 3 sites, private nonprofits only, the Greenfield Girls Softball League first.** **Joins contrarian's motion 4**, with **legal's motion 7** (no town committees).
    - D-ids: new decision for the free-site rule (none exists); touches D-1971 and D-1975, plus the studio-credit check in the build.
    - Money: about 8 h per site (CFO guess), $0 to $15 cash, plus a small code change for the credit.
    - Risk: volunteer groups are slow to supply content. It reads as generous to everyone, and sponsors such as Descavich Plumbing (OPP-126) see the work.
11. **Resolve T-209 first: if Tom owes Gail Ahlers (The Empowerment Factory, I-55) website help, she takes the first community slot, ahead of any cold-picked group.** Proposer: customer advocate.
    - D-ids: none (it settles open thought T-209); it orders the slots under motion 10.
    - Money: about one community site's hours, inside motion 10's cap.
    - Risk: it honours an existing ask that came through Lauren rather than leaving it hanging.
12. **Lobanton: move its preview end to 2026-12-02 under D-2052 and clear the overdue follow-up before any new programme.** **Joins contrarian's motion 5.**
    - D-ids: D-2052 (enforcing it, not changing it).
    - Money: protects the only $250 at proposal.
    - Risk: none.
13. **Record $250 flat, one time, as the price through the trial.** **Joins pricing's motion 6.**
    - D-ids: new; touches D-1978.
    - Money: none.
    - Risk: none. It protects what Judy, Ale House and 85 popups have already been told.
