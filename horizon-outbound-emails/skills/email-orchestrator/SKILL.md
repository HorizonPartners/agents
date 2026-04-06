---
name: email-orchestrator
description: >
  Assembles complete outbound emails for Horizon Partners Lead-PF campaigns by combining 4 components in order:
  static intro, dynamic personalized intro (skill-based), dynamic body (skill-based), and static closing.
  Use this skill when generating full outbound emails for the 533-account Lead-PF campaign.
  Trigger on "write email," "full email," "assemble email," "email-orchestrator," or when the user wants a complete outbound email composed from modular components.
---

# Email Orchestrator: Horizon Partners Outbound

## What This Skill Does

Assembles complete outbound emails from 4 modular components, applied in this exact order:

1. **Static Intro** (select one variant below)
2. **Dynamic Intro** (use `intro-leads-with-exp` or `intro-leads-no-exp` skill)
3. **Dynamic Body** (use `body-problem-first`, `body-philosophy-first`, or `body-proof-first` skill)
4. **Static Closing** (select one variant below)

Each component is independent and interchangeable. The static intro and closing variants live in this file. The dynamic intro and body variants are generated or pulled from their respective skills.

---

## Component 1: Static Intro

Copy one variant verbatim. Replace merge fields before sending.

### Merge Fields

- `{{first_name}}` -- recipient's first name
- `{{sender.first_name}}` -- sender's first name
- `{{today}}` -- current day of the week (e.g., "Monday," "Tuesday")

### Hyperlink Requirement

"Horizon Partners" MUST be hyperlinked to https://www.horizonpartners.com in every static intro variant. This link must persist in rich text when exported to Gmail or Apollo.

### Static Intro Variant A (Warm + Day Reference)

Hi {{first_name}}, hope you're doing well and are having a great {{today}}.

I'm {{sender.first_name}} with [Horizon Partners](https://www.horizonpartners.com), a boutique investment bank specialized in M&A advisory for product-first software companies.

### Static Intro Variant B (Direct)

Hi {{first_name}},

I'm Patrick with [Horizon Partners](https://www.horizonpartners.com), a boutique investment bank specialized in M&A advisory for product-first software companies.

### Static Intro Variant C (Warm + Compact)

Hi {{first_name}},

Hope you're doing well. I'm {{sender.first_name}} with [Horizon Partners](https://www.horizonpartners.com), a boutique investment bank specialized in M&A advisory for product-first software companies.

---

## Component 2: Dynamic Intro (Skill-Based)

Select the appropriate skill based on whether Horizon has completed a relevant deal in the target company's space.

**Decision logic:**

1. Check the target company's sector/vertical against `horizon_prior_clients_reference.md`
2. If a high-fidelity match exists: use `intro-leads-with-exp`
3. If no match exists: use `intro-leads-no-exp`

The dynamic intro is separated from the static intro by one blank line. It is the personalized, company-specific opening line.

---

## Component 3: Dynamic Body (Skill-Based)

Select one body theme skill. Each skill contains 3 static variants to choose from.

- `body-problem-first` -- leads with the problem traditional M&A processes create for product-first founders
- `body-philosophy-first` -- leads with Horizon's ethos, values, and approach
- `body-proof-first` -- leads with Horizon's track record, multiples, and buyer names

The body paragraph(s) follow the dynamic intro. Copy the selected variant verbatim from the skill.

---

## Component 4: Static Closing

Copy one variant verbatim. Replace merge fields before sending.

### Merge Fields

- `{{account.name}}` -- target company name

### Static Closing Variant A (Simple Ask)

Do you have some time in the coming weeks for an intro call?

### Static Closing Variant B (Situational + Warm)

If you're considering a capital raise, secondary liquidity, or a strategic sale for {{account.name}}, we would love the opportunity to connect and get on your radar!

Thank you

### Static Closing Variant C (Short Ask)

Are you available in the coming weeks to connect on a short call?

---

## Assembly Rules

1. Every component is separated by one blank line. The greeting line, the Horizon Partners introduction line, the dynamic intro, the body, and the closing each get their own paragraph with a blank line between them.
2. Do not add any text, transitions, or filler between components.
3. Do not modify the text of any static variant. Copy verbatim.
4. Replace all merge fields (`{{first_name}}`, `{{sender.first_name}}`, `{{today}}`, `{{account.name}}`) with actual values before final output.
5. The dynamic intro (Component 2) and dynamic body (Component 3) follow their own skill instructions exactly.

## Example Assembly

> Hi Sarah, hope you're doing well and are having a great Tuesday.
>
> I'm Patrick with [Horizon Partners](https://www.horizonpartners.com), a boutique investment bank specialized in M&A advisory for product-first software companies.
>
> [Dynamic intro sentence from skill goes here.]
>
> [Bo