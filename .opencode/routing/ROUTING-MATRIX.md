# V4 Adaptive Routing Matrix

## Tier 0 — combo-free
Use when:
- low risk
- simple
- read-only
- no architecture/security decision

Agents:
- cheap-worker

Examples:
- find relevant files
- summarize existing tests
- inspect repository structure
- documentation lookup

## Tier 1 — combo-gemini
Use for evidence-heavy analysis and QA:
- requirements analysis
- QA planning
- test design
- API testing
- UI testing
- failure classification
- flaky test investigation

Agents:
- planner
- qa-lead
- test-designer
- api-tester
- ui-tester
- failure-analyzer
- flaky-test-analyzer
- router

## Tier 2 — combo-sonnet
Use for normal engineering coordination and implementation:
- orchestrator
- normal developer
- automation engineer
- medium-risk coordination

Agents:
- orchestrator
- developer-standard
- automation-engineer

## Tier 3 — combo-opus
Use for high complexity/risk:
- architecture
- adversarial design
- complex implementation
- debugging
- security
- performance
- independent review
- release gate

Agents:
- architect
- debater
- developer
- debugger
- performance-reviewer
- code-reviewer
- security-reviewer
- release-gate

## Escalation rules

1. Low/simple + read-only -> Tier 0.
2. Any QA/evidence task -> Tier 1.
3. Medium implementation -> Tier 2.
4. High risk OR complex -> Tier 3.
5. Security-sensitive -> Tier 3 security-reviewer.
6. Production-impacting -> Tier 3 code-reviewer + release-gate.
7. Database migration -> architect + developer + QA + code-reviewer.
8. Authentication/authorization -> security-reviewer.
9. Payment/financial flow -> architect + security-reviewer + code-reviewer + release-gate.
10. Repeated failure after 2 repairs -> escalate to Tier 3 debugger.
11. Three failed repairs -> HUMAN_REQUIRED.
