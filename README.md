# OpenCode Agentic Workflow V4
## OpenCode 1.18.9 + 9Router adaptive model routing

V4 adds adaptive routing instead of assigning every task to the most expensive model.

Known models:
- 9router/combo-opus
- 9router/combo-sonnet
- 9router/combo-gemini
- 9router/combo-free

Core idea:

REQUEST -> CLASSIFY -> ROUTE -> EXECUTE -> VERIFY -> REPAIR -> REVIEW -> GATE

Routing dimensions:
- task type
- risk
- complexity
- affected layer
- required evidence
- iteration count
- failure classification

### Commands

/feature <request>
/bug <problem>
/qa <scope>
/automation <scope>
/review <scope>
/release <scope>
/route <request>

### Routing policy

FREE:
- simple documentation
- repository discovery
- low-risk summaries
- repetitive read-only tasks

GEMINI:
- requirements
- QA strategy
- test design
- API/UI testing
- failure classification
- flaky-test analysis

SONNET:
- orchestration
- normal implementation coordination
- test automation
- medium-risk engineering

OPUS:
- architecture
- complex implementation
- debugging
- security
- performance
- independent code review
- release gate
- critical/high-risk decisions

V4 does not automatically push changes. Critical/high-risk work requires independent review.
