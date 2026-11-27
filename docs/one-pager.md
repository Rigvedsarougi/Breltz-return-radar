# Breltz Bags: Return Radar (process one-pager)

## The client
Bengaluru backpack brand, 38 cr revenue (+40% YoY): 55% website, 25% Amazon, 12% Myntra. Contribution margin fell from 22% to 9%. The CEO blames returns (30% on the dashboard, which includes RTO). Goals: know why people return (by product, channel, ad, customer type), get website customer-initiated returns below 12% and margin to 18%+, without cutting growth.

## What I think the real problem is
Returns are mostly a marketing and information problem, not a quality problem. Breltz pays to create expectation gaps and has no signal telling it so.

**Evidence from the call**
- **Not quality:** 75-80% of Commuter returns are QC grade A; transit damage is 4-5%; stricter vendor QC moved nothing.
- **Best ads over-promise:** the 5x Riya video shows a petite creator with (probably) a 13" Air; tickets say "mine doesn't fit like that". The carousel says "Fits up to 16-inch" but spec is 15.6" (copy changed in March; returns rose in April). The new 28L is slimmer than the old 30L.
- **Colour is a creative issue:** studio photos are accurate, filtered reels (Ananya's Goa sunset) run as ads; tickets say Dusty Rose "looks brown". Sage and Dusty Rose have the highest return rates.
- **Listings are stale:** Myntra (31% returns) still shows old photos and "30L". Amazon (13-14%) has size-comparison imagery, reviews and customer photos; the website has cm dimensions in a Specifications tab.
- **Incentives amplify it:** free prepaid returns since last Diwali (+18% conversion, return impact never analysed) invite two-colour bracketing.
- **Optimisation is blind:** Meta gets the purchase at order time and never hears about returns, so "scale above 3x" pushes hardest on ads that cause returns. Nobody checks ad copy against the spec.
- **No shared data:** the dropdown is useless, tickets are unlinked to returns, order IDs don't exist in Meta, four tools hold one order's story.

Caveats: RTO (17-18% of COD) is a separate COD problem and should be reported separately. The causal story is a strong hypothesis from one call, to be confirmed by the data join.

## Options considered
- **Return-reason survey only:** cheap, but WhatsApp reason requests got no replies and it only measures the symptom.
- **Tighten return policy / COD fee:** fast, but the COD fee already hurt conversion and the CEO ruled out shrinking growth.
- **Size guide or listing fixes alone:** right direction but one-off; the next creative can reintroduce the gap.
- **Chosen: Return Radar:** addresses the cause (expectation gap), the incentive (scaling the wrong ads) and the blindness (no joined data) together, and ships in stages.

## Prototype screens
1. Ads after returns: net ROAS per creative; the ranking flips.
2. Promise vs product: specific claims to fix.
3. Orders at risk: duplicate-colour orders, fit/colour tickets, high-risk creative, suggested save message.
4. Return reason capture: two taps, order ID attached.

## Rollout
- **Weeks 1-2 (no engineering):** fix Myntra listing and the 16" copy; join Shopify, returns sheet, Freshdesk and Meta exports in a spreadsheet; first return rates by SKU, colour, channel, new vs repeat, creative.
- **Weeks 3-6:** net-ROAS dashboard; claim check before creatives go live; new return-reason flow; website size-comparison image.
- **Weeks 6-12:** at-risk triggers on WhatsApp; return/refund events to Meta via CAPI; test exchange-first for bracketing.

## What I would measure
- **Outcome:** website customer-initiated return rate (under 12% in two quarters, RTO excluded); contribution margin (18%+).
- **Diagnosis:** share of returns with a structured reason; share of orders joined to an ad (about 40% have a source today); return rate by creative, colour, new vs repeat.
- **Marketing:** gap between Meta ROAS and net ROAS; share of spend on creatives with net ROAS above 2.8x.
- **Guardrails:** conversion and revenue growth; stock locked in reverse transit.
- **Experiments:** corrected vs old creative; fit tip vs holdout; with/without size-comparison image.

## Risks and open questions
- Attribution is partial, so net ROAS is directional; use creative IDs in UTMs and ad names; treat WhatsApp-assisted COD orders separately.
- Creators may resist disclaimers; offer a second creator with a larger laptop instead.
- Verify the Riya laptop model and real fit data before blaming specific ads.
