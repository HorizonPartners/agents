# Horizon Outbound Emails

Modular email assembly system for Horizon Partners Lead-PF outbound campaigns targeting founder-led software companies.

## How It Works

Emails are assembled from 4 independent, interchangeable components:

1. **Static Intro** -- greeting + Horizon Partners introduction (3 variants)
2. **Dynamic Intro** -- personalized opener referencing the target company (2 skills: with or without deal experience)
3. **Dynamic Body** -- value proposition paragraph(s) (3 theme skills, 3 variants each)
4. **Static Closing** -- call-to-action (3 variants)

The **email-orchestrator** skill ties everything together, routing to the correct intro skill based on whether Horizon has relevant deal experience in the target company's space.

## Skills

| Skill | Purpose |
|-------|---------|
| `email-orchestrator` | Main assembly skill. Contains static intros/closings and routes to dynamic skills. |
| `intro-leads-no-exp` | Generates thesis-first personalized openers when Horizon has no relevant deal experience. |
| `intro-leads-with-exp` | Generates deal-first personalized openers referencing Horizon's prior transactions. |
| `body-problem-first` | 3 static body variants leading with the problem traditional M&A creates for product-first founders. |
| `body-philosophy-first` | 3 static body variants leading with Horizon's ethos, values, and approach. |
| `body-proof-first` | 3 static body variants leading with Horizon's track record and results. |

## Reference Data

The `intro-leads-with-exp` skill includes `references/horizon_prior_clients_reference.md`, a structured database of Horizon's prior deals with sector labels for matching target companies to relevant transactions.

## Usage

Say "write an email for [company]" or "assemble email" to trigger the orchestrator. You can also invoke individual components directly (e.g., "write an opener for [company]" or "use the proof-first body").
