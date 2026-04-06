---
name: intro-leads-with-exp
description: >
  Generate personalized 1-sentence cold email openers for Horizon Partners outbound campaigns when Horizon HAS completed relevant transactions in the target company's space.
  Use this skill whenever the user asks to write email intros, openers, or first lines referencing Horizon's deal experience,
  or when openers should include specific transaction names, deal sizes, multiples, or buyer names.
  Also trigger when the user says "write openers with experience," "intro with deals," "intro-leads-with-exp,"
  "experienced opener," "deal-based opener," or references having done deals in a company's space.
  This skill requires the user to provide the relevant Horizon deal(s) and target company.
---

# Personalized Email Opener: Horizon Partners Outbound (With Deal Experience)

## What This Skill Does

Generates personalized, 1-2 sentence email openers for Horizon Partners' cold outbound campaigns when Horizon has completed 1, 2, or 3 relevant transactions in the target company's space. Each opener references specific deals by name, size, buyer, and/or multiple to establish credibility before making the intro.

This is the companion to `intro-leads-no-exp`, which is used when Horizon has NOT done deals in the space. These instructions were refined through multiple rounds of iteration with direct edits from the outbound lead.

## Required Inputs

For each opener, the user must provide:

1. **Target company name** (or {{account.name}} as a merge field)
2. **1-3 relevant Horizon deals**, each with some combination of:
   - Company name advised
   - Parenthetical descriptor of what the company does
   - Deal size ($XM) and/or multiple (Xx)
   - Buyer/investor name
   - Deal type (sale, investment, acquisition, capital raise, engagement)
3. **Space/vertical label** (e.g., "FinTech space," "EdTech space," "creator economy space")
4. **Optional:** a signal about the target company (PLG, strong product, growth, etc.)

If the user does not provide deal details, ask for them. Do not fabricate deal names, sizes, or buyers. Use the Prior Client Reference file (`horizon_prior_clients_reference.md`) as the authoritative source for deal names, stats, descriptors, and links.

## Process

### Step 1: Identify the Deal Count

Determine whether the opener uses 1, 2, or 3 deals. This changes the structure significantly.

### Step 2: Select a Pattern

Choose the appropriate structural pattern from the sections below based on deal count and context.

### Step 3: Write the Opener

Apply the writing rules below. One to two sentences. Lead with the deals, close with the target company.

### Step 4: Add Hyperlinks

Every deal company name referenced in the opener must be hyperlinked to its press release or announcement page. Use the link table below (or the Prior Client Reference file) to find the correct URL for each deal. The hyperlink goes on the company name itself, not on the deal details.

Example: "We advised [Lemon Squeezy](https://horizonpartners.com/stripe-acquires-horizon-partners-client-lemon-squeezy/) on their 23x deal with Stripe"

In this example, "Lemon Squeezy" is the clickable hyperlink. The deal size and buyer name are plain text.

If a deal has no public link, leave the company name as plain text.

### Step 5: Validate

Check against the validation checklist before finalizing.

---

## Structural Patterns

### 1-Deal Patterns

**Pattern A: Deal + Space Activity + Intro**
Structure: We advised [Company] ([descriptor]) on their $[X]M deal with [Buyer] and have been [highly/very] active in the [space], so I wanted to make the intro to find time to discuss what we like about {{account.name}}.

**Pattern B: Deal + Buyer Intel**
Structure: We recently closed a deal for [Company], a [descriptor], and have good intel on what buyers are looking for in the [space] right now. Given what {{account.name}} has built in the space, I wanted to make the intro.

**Pattern C: Deal + Impressive Multiple**
Structure: Last year we advised [Company], a [descriptor], on their [X]x deal with [Buyer] and have been [very/highly] active in the [space]. Given what looks like strong [signal] at {{account.name}}, I wanted to make the intro and tell you more about our experience.

**Pattern D: Deal + Market Mapping Discovery**
Structure: We advised [Company] on their $[X]M deal with [Buyer] and have been active in the [space]. I came across {{account.name}} while mapping the [space] M&A market and was impressed with the product you've built, so I wanted to tell you more about Horizon and our approach.

**Pattern E: Target Signal + Deal Credibility**
Structure: Given what looks like strong [signal] at {{account.name}} and our experience in the [space] (we sold [Company] to [Buyer], and are about to close a deal for a [descriptor]), I wanted to make the intro and tell you more about Horizon.

**Pattern F: Big-Name Buyer + Target Signal (ultra-short)**
Structure: We recently closed a deal with [Big Buyer Name] and, given your focus on [signal], I wanted to make the intro and tell you more about the firm and our approach.

**Pattern G: Deal + Current Engagement**
Structure: We recently advised [Company] on their sale to [Buyer] and are currently engaged by a [descriptor]. We have good intel on what buyers are looking for in the [space] right now, and I wanted to make the intro.

### 2-Deal Patterns

**Pattern H: Stacked Deals + Space Activity**
Structure: We advised [Company1] ([descriptor]) on their [deal detail] and [Company2] ([descriptor]) on their [deal detail], and have been [highly/very] active in the [space], so we wanted to make the intro to find time to discuss {{account.name}}.

**Pattern I: Stacked Deals + Current Engagement**
Structure: We advised [Company1] ([descriptor]) on their [deal] with [Buyer1] and [Company2] ([descriptor]) on their [deal] with [Buyer2], and were recently engaged by [vague reference to active deal]. Given the impressive product you've built with {{account.name}}, I wanted to make the intro to find time to discuss.

**Pattern J: Stacked Deals + Market Mapping**
Structure: We advised [Company1] ([descriptor]) and [Company2] ([descriptor]) and have been very active in the [space]. I came across {{account.name}} through our [space] M&A market mapping and was impressed with the product you've built, so I wanted to reach out.

**Pattern K: Stacked Deals + Thematic Link**
Structure: We advised [Company1] on their $[X]M deal with [Buyer1] and [Company2] on their [X]x deal with [Buyer2], both at the center of [thematic trend], and have been active in the [space]. I wanted to make the intro to find time to discuss what we like about {{account.name}}.

### 3-Deal Patterns

**Pattern L: Multiple Transactions Label + Stacked**
Structure: We've advised on multiple transactions in the [space], including [Company1], a [descriptor] ($[X]M deal with [Buyer1], [superlative if applicable]), [Company2], which [achievement], and [Company3], a [descriptor] ($[X]M deal with [Buyer3]). Given some of the similarities we see in {{account.name}}, I wanted to make the intro and see if we could find time to connect.

**Pattern M: Stacked with Timing Context**
Structure: We were recently engaged by [vague active deal] to advise on their $[X]M [deal type], advised on [Company2]'s $[X]M deal this year, and advised on [Company3]'s $[X]M deal with [Buyer]. Given our experience in the space and what you're building with {{account.name}}, I wanted to tell you more about Horizon and our approach.

**Pattern N: Stacked with Parenthetical Descriptors + Intro**
Structure: We advised [Company1] ([descriptor], $[X]M sale to [Buyer1]), [Company2] ([descriptor], $[X]M sale to [Buyer2]), and [Company3] ([descriptor], sale to [Buyer3]), and have been active in the [space], so I wanted to connect and see if we could find time to discuss our interest in {{account.name}}.

---

## Writing Rules

### Structure
- One to two sentences. Never three.
- **Deals first, target company second.** Lead with Horizon's transaction experience, then bridge to the target.
- The closer should reference {{account.name}} in some way. Don't end generically.
- Shorter is always better. Don't overload with detail on every deal.

### Closing Lines

Rotate across these. Don't default to any single one:

- "I wanted to make the intro to find time to discuss what we like about {{account.name}}"
- "I wanted to make the intro to find time to discuss {{account.name}}"
- "I wanted to connect and see if we could find time to discuss our interest in {{account.name}}"
- "I wanted to make the intro and see if we could find time to connect"
- "I wanted to make the intro and tell you more about Horizon and our approach"
- "I wanted to tell you more about Horizon and our approach"
- "I wanted to tell you more about the firm and our approach"
- "I wanted to make the intro and tell you more about our experience"
- "I wanted to reach out"
- "Given the impressive product you've built with {{account.name}}, I wanted to make the intro to find time to discuss"
- "Given what {{account.name}} has built in the space, I wanted to make the intro"

### Tone and Voice
- Use "I" or "we" naturally. Both are acceptable, unlike the no-exp variant which always uses "we."
- Conversational and confident. The deals speak for themselves -- don't oversell.
- No salesy language. No "incredible opportunity" or "would love to connect."

### Deal References
- **Always name the company advised.** Never say "a company" when you can name it.
- **Parenthetical descriptors** help the reader understand deal relevance: "(creator + video + community platform)", "(payments and subscription management for SaaS)", "(AI-powered, mobile-first FSM platform)"
- **Deal sizes** use $[X]M format: "$180M deal with PSG", "$165M deal with Euronet"
- **Multiples** when impressive: "20x deal with Stripe", "23x sale to Stripe"
- **Deal types vary** -- rotate: "sale to," "deal with," "investment from," "acquisition by," "capital raise," "engaged by"
- **Buyer names add credibility** -- always include when known, especially recognizable names (Stripe, Chegg, Samsung, Spotify)
- **Superlatives on deals** are OK when factual: "Chegg's highest multiple ever paid", "recently recognized as Deal of the Year"
- **Active/upcoming engagements** can be referenced vaguely: "are about to close a deal for a [descriptor]", "were recently engaged by an industry-leading [descriptor]", "are currently engaged by a [descriptor]"

### Space Labels
- Keep broad: "FinTech space," "EdTech space," "creator economy space," "PropTech space," "payments space"
- Don't over-qualify: "payments space" not "payments infrastructure and subscription management space"

### Target Company Signals
- When you have a signal about the target, use it: "Given what looks like strong PLG at {{account.name}}", "Given what {{account.name}} has built"
- "Impressed with the product you've built" is a valid compliment
- "Given some of the similarities we see in {{account.name}}" works for 3-deal stacks
- "Given our experience and what you're building with {{account.name}}" ties deals to the target

### Market Mapping References
- "I came across {{account.name}} while mapping the [space] M&A market" explains how Horizon found them
- "We came across {{account.name}} through our [space] M&A market mapping" is an alternative form
- Use when you want to signal that Horizon is actively researching the space

---

## What NOT to Do

1. Don't fabricate deal names, sizes, multiples, or buyers. Use only what the user provides.
2. Don't include three or more sentences.
3. Don't end without referencing the target company in some way.
4. Don't use generic closings like "so we wanted to reach out" without tying to {{account.name}}.
5. Don't overload a single opener with too many deal details. For 3-deal stacks, keep each deal reference tight.
6. Don't use "highly active" and "very active" interchangeably without variation. Mix them.
7. Don't use em dashes, exclamation points, or Oxford commas.
8. Don't include a CTA beyond the closing bridge. No "would you be open to a call" or "let me know if you'd be interested."
9. Don't say anything negative about the target company or their space.
10. Don't use product-type labels (ERP, EHR, CRM) in space labels.

---

## Validation Checklist

Before finalizing each opener, verify:

- One or two sentences only
- Leads with Horizon's deal experience
- Target company ({{account.name}}) appears in the closer
- All deal names, sizes, multiples, and buyers are accurate (not fabricated)
- Every deal company name is hyperlinked to its press release (use link table below)
- Closing line is purposeful and references the target
- No em dashes, exclamation points, or Oxford commas
- No generic closing without target company reference
- Space label is broad and clean
- Parenthetical descriptors are tight and useful
- Tone is confident and conversational, not salesy
- Deal count matches the pattern used (1, 2, or 3)

---

## Approved Examples

These openers were edited and approved across 2 rounds of iteration. Study them carefully. Your output should match these in tone, structure, and quality.

### 1-Deal Examples

1. "We advised [Lemon Squeezy](https://horizonpartners.com/stripe-acquires-horizon-partners-client-lemon-squeezy/), a global merchant of record for thousands of SaaS businesses, on their 20x deal with Stripe, and have been highly active in the payments space, so I wanted to make the intro to find time to discuss what we like about {{account.name}}."

2. "We recently closed a deal for [Givergy](https://horizonpartners.com/horizon-partners-advises-givergy-on-its-sale-to-momogood-edison-partners/), a nonprofit fundraising and event platform and have good intel on what buyers are looking for in the nonprofit tech space right now. Given what {{account.name}} has built in the space, I wanted to make the intro."

3. "Last year we advised [Uscreen](https://horizonpartners.com/horizon-partners-advises-uscreen-on-its-150-million-growth-investment-from-psgequity/) (creator + video + community platform) on their $180M deal with PSG and have been very active in the creator space. Given what looks like strong PLG at {{account.name}}, I wanted to make the intro and tell you more about our experience."

4. "We advised [GasBuddy](https://horizonpartners.com/horizon-advises-gasbuddy-and-openstore-on-acquisition/) on their $100M deal with OPIS, a deal driven by community-led-growth, big data, and mobile-first payments, and have been active in the consumer data space. I came across {{account.name}} through our FSM M&A market mapping and was impressed with the product you've built, so I wanted to see if we could find time to discuss."

5. "Given what looks like strong PLG at YuJa and our experience in the enterprise media/content space (we sold [Uscreen](https://horizonpartners.com/horizon-partners-advises-uscreen-on-its-150-million-growth-investment-from-psgequity/) to PSG, and are about to close a deal for a business content management platform), I wanted to make the intro and tell you more about Horizon."

6. "We recently closed a deal with Stripe and, given your focus on PLG, I wanted to make the intro and tell you more about the firm and our approach."

7. "Last year we advised [Xe.com](https://horizonpartners.com/horizon-advises-xe-on-acquisition/) (cross-border payments and FX data) on their $165M deal with Euronet and have been following the payments space closely. I came across {{account.name}} while mapping the FinTech M&A market and was impressed with the product you've built, so I wanted to tell you more about Horizon and our approach."

8. "We recently advised [Where to Buy](https://horizonpartners.com/horizon-partners-advises-where-to-buy-on-its-acquisition-by-destini/) on their sale to SPINS and are currently engaged by an omnichannel retail inventory management platform. We have good intel on what buyers are looking for in the CPG software space right now, and I wanted to make the intro."

9. "We advised [PDQ](https://horizonpartners.com/horizon-advises-pdq-on-growth-investment-by-ta-associates/), a systems management tool embedded in real estate IT stacks, on their $300M sale to TA and have been very active in the PropTech space. I wanted to make the intro to find time to discuss what we like about {{account.name}}."

10. "We advised [Mathway](https://horizonpartners.com/horizon-advises-mathway-acquisition-chegg/), a global leader in AI-driven math learning, on their $128M deal with Chegg and have been very active in the EdTech space. Given what {{account.name}} has built, I wanted to make the intro to find time to discuss."

11. "We advised [Visme](https://horizonpartners.com/horizon-partners-advises-visme-on-its-strategic-growth-investment-from-gearbox-capital-2/) (visual content creation platform) on their $20M deal with Gearbox Capital and have been very active in the creator economy space. Given what {{account.name}} has built, I wanted to make the intro and tell you more about Horizon and our approach."

### 2-Deal Examples

12. "We advised [Lemon Squeezy](https://horizonpartners.com/stripe-acquires-horizon-partners-client-lemon-squeezy/) (payments and subscription management for SaaS) on their 23x sale to Stripe and [Xe.com](https://horizonpartners.com/horizon-advises-xe-on-acquisition/) (cross-border payments and FX data) on their $165M deal with Euronet, and have been highly active in the FinTech space, so we wanted to make the intro to find time to discuss {{account.name}}."

13. "We advised [Fulcrum](https://horizonpartners.com/horizon-advises-spatial-networks-majority-recapitalization/) (AI-powered, mobile-first FSM platform) and [DaySmart](https://horizonpartners.com/horizon-advises-daysmart-on-majority-recapitalization/) (which has scaled into multiple field-service and payments verticals) and have been very active in the FSM and workforce management space. I came across {{account.name}} through our FSM M&A market mapping and was impressed with the product you've built, so I wanted to reach out."

14. "We advised [DistroKid](https://www.silversmith.com/news/silversmith-capital-partners-invests-in-distrokid-to-continue-rapid-growth/) (music distribution + creator infrastructure) on their investment from Spotify and Silversmith and [Roon Labs](https://horizonpartners.com/roon-labs-acquired-by-samsung-owned-harman-international/) (audio analytics + music management) on their acquisition by Harman/Samsung, and were recently engaged by an industry-leading music analytics and intelligence platform. Given the impressive product you've built with {{account.name}}, I wanted to make the intro to find time to discuss."

15. "We advised [Mathway](https://horizonpartners.com/horizon-advises-mathway-acquisition-chegg/) (AI-driven math learning, $128M deal with Chegg) and [ThankView](https://horizonpartners.com/horizon-advises-thankview-evertrue-on-merger-and-recapitalization-by-rubicon-technology-partners/) (video-first donor engagement, $210M deal with Rubicon Technology) and have been very active in the EdTech space. Given the impressive product you've built with {{account.name}}, I wanted to make the intro and tell you more about Horizon and our approach."

16. "We advised [Uscreen](https://horizonpartners.com/horizon-partners-advises-uscreen-on-its-150-million-growth-investment-from-psgequity/) (creator + video + community platform) on their $180M deal with PSG and [Visme](https://horizonpartners.com/horizon-partners-advises-visme-on-its-strategic-growth-investment-from-gearbox-capital-2/) on their $20M deal with Gearbox Capital, and have been very active in the creator economy space. I came across {{account.name}} through our creator economy M&A market mapping and was impressed with the product you've built, so I wanted to reach out."

17. "We advised [GasBuddy](https://horizonpartners.com/horizon-advises-gasbuddy-and-openstore-on-acquisition/) on their $100M deal with OPIS and [Lemon Squeezy](https://horizonpartners.com/stripe-acquires-horizon-partners-client-lemon-squeezy/) on their 20x deal with Stripe, both at the center of community-led-growth and mobile-first payments, and have been active in the consumer data space. I wanted to make the intro to find time to discuss what we like about {{account.name}}."

18. "We advised [MMI](https://horizonpartners.com/mmi-receives-growth-investment-from-westview-capital-partners/) (mortgage origination platform, $110M sale to Westview) and [PDQ](https://horizonpartners.com/horizon-advises-pdq-on-growth-investment-by-ta-associates/) (systems management embedded in real estate IT stacks, $300M sale to TA) and have been very active in the PropTech space. Given the impressive product you've built with {{account.name}}, I wanted to make the intro and tell you more about Horizon and our approach."

### 3-Deal Examples

19. "We've advised on multiple transactions in the EdTech space, including [Mathway](https://horizonpartners.com/horizon-advises-mathway-acquisition-chegg/), a global leader in AI-driven math learning ($128M deal with Chegg, Chegg's highest multiple ever paid), [EverTrue](https://horizonpartners.com/horizon-advises-thankview-evertrue-on-merger-and-recapitalization-by-rubicon-technology-partners/), which transformed alumni engagement and fundraising, and [ThankView](https://horizonpartners.com/horizon-advises-thankview-evertrue-on-merger-and-recapitalization-by-rubicon-technology-partners/), a video-first donor engagement platform ($210M deal with Rubicon Technology). Given some of the similarities we see in {{account.name}}, I wanted to make the intro and see if we could find time to connect."

20. "We advised [MMI](https://horizonpartners.com/mmi-receives-growth-investment-from-westview-capital-partners/) (mortgage origination platform, $110M sale to Westview), [PDQ](https://horizonpartners.com/horizon-advises-pdq-on-growth-investment-by-ta-associates/) (a systems management tool embedded in real estate IT stacks, $300M sale to TA), and [HousingList](https://horizonpartners.com/horizon-advises-housing-list-on-acquisition/) (real estate digital media and content platform, sale to LeadQual), and have been active in the real estate and mortgage tech space, so I wanted to connect and see if we could find time to discuss our interest in {{account.name}}."

21. "We were recently engaged by a large creator economy SaaS business to advise on their $50M capital raise, advised on [Uscreen](https://horizonpartners.com/horizon-partners-advises-uscreen-on-its-150-million-growth-investment-from-psgequity/)'s $180M deal with PSG this year, and advised on [Visme](https://horizonpartners.com/horizon-partners-advises-visme-on-its-strategic-growth-investment-from-gearbox-capital-2/)'s $20M deal with Gearbox Capital this summer. Given our experience in the space and what you're building with {{account.name}}, I wanted to tell you more about Horizon and our approach."

22. "We advised [Lemon Squeezy](https://horizonpartners.com/stripe-acquires-horizon-partners-client-lemon-squeezy/) (payments and subscription management for SaaS) on their 23x sale to Stripe, [Xe.com](https://horizonpartners.com/horizon-advises-xe-on-acquisition/) (cross-border payments and FX data) on their $165M deal with Euronet, and [GasBuddy](https://horizonpartners.com/horizon-advises-gasbuddy-and-openstore-on-acquisition/) on their $100M deal with OPIS, and have been highly active in the FinTech space. Given our experience and what you're building with {{account.name}}, I wanted to tell you more about Horizon and our approach."

23. "We advised [DistroKid](https://www.silversmith.com/news/silversmith-capital-partners-invests-in-distrokid-to-continue-rapid-growth/) (music distribution + creator infrastructure) on their investment from Spotify and Silversmith, [Roon Labs](https://horizonpartners.com/roon-labs-acquired-by-samsung-owned-harman-international/) (audio analytics + music management) on their acquisition by Harman/Samsung, and [Uscreen](https://horizonpartners.com/horizon-partners-advises-uscreen-on-its-150-million-growth-investment-from-psgequity/) (creator + video + community) on their $180M deal with PSG. Given our depth in the creator economy and what {{account.name}} has built, I wanted to connect and see if we could find time to discuss."

---

## Talk Tracks (Deal Framing Reference)

When writing openers, deals can be framed around market themes. These are examples of how to position specific deals thematically:

- Xe.com's $165M deal with Euronet: cross-border payments, FX data, and API-first distribution
- Lemon Squeezy's deal with Stripe: Stripe scaling merchant of record selling
- GasBuddy's $100M deal with OPIS: community-led-growth, big data, and mobile-first payments
- Mathway's $128M deal with Chegg: Chegg's highest multiple ever paid, AI-driven learning
- Uscreen's $180M deal with PSG: creator economy, video, community platforms

---

## Deal Hyperlink Table

Use these URLs to hyperlink deal company names in every opener. The link goes on the company name, not the deal details.

| Client | Press Release URL |
|--------|------------------|
| PDQ | https://horizonpartners.com/horizon-advises-pdq-on-growth-investment-by-ta-associates/ |
| ThankView + EverTrue | https://horizonpartners.com/horizon-advises-thankview-evertrue-on-merger-and-recapitalization-by-rubicon-technology-partners/ |
| Lemon Squeezy | https://horizonpartners.com/stripe-acquires-horizon-partners-client-lemon-squeezy/ |
| Uscreen | https://horizonpartners.com/horizon-partners-advises-uscreen-on-its-150-million-growth-investment-from-psgequity/ |
| Roon Labs | https://horizonpartners.com/roon-labs-acquired-by-samsung-owned-harman-international/ |
| MMI | https://horizonpartners.com/mmi-receives-growth-investment-from-westview-capital-partners/ |
| CODA Intelligence | https://horizonpartners.com/horizon-partners-advises-coda-intelligence-on-acquisition-by-pdq/ |
| Nutrislice | https://horizonpartners.com/horizon-partners-advises-nutrislice-on-majority-growth-investment-from-accel-kkr/ |
| Visme | https://horizonpartners.com/horizon-partners-advises-visme-on-its-strategic-growth-investment-from-gearbox-capital-2/ |
| Where to Buy | https://horizonpartners.com/horizon-partners-advises-where-to-buy-on-its-acquisition-by-destini/ |
| Mathway | https://horizonpartners.com/horizon-advises-mathway-acquisition-chegg/ |
| DistroKid | https://www.silversmith.com/news/silversmith-capital-partners-invests-in-distrokid-to-continue-rapid-growth/ |
| Givergy | https://horizonpartners.com/horizon-partners-advises-givergy-on-its-sale-to-momogood-edison-partners/ |
| GasBuddy | https://horizonpartners.com/horizon-advises-gasbuddy-and-openstore-on-acquisition/ |
| XE | https://horizonpartners.com/horizon-advises-xe-on-acquisition/ |
| Fulcrum | https://horizonpartners.com/horizon-advises-spatial-networks-majority-recapitalization/ |
| DaySmart | https://horizonpartners.com/horizon-advises-daysmart-on-majority-recapitalization/ |
| HousingList | https://horizonpartners.com/horizon-advises-housing-list-on-acquisition/ |
