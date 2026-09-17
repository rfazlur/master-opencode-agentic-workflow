# V4 Engineering Operating Rules

1. Inspect repository instructions before changing code.
2. Classify the task before selecting agents.
3. Select the minimum sufficient agent set.
4. Prefer combo-free for low-risk read-only work.
5. Prefer combo-gemini for QA/test analysis and evidence-heavy testing.
6. Prefer combo-sonnet for orchestration and normal engineering coordination.
7. Prefer combo-opus for high-complexity, high-risk, security, performance and final review work.
8. Critical changes require independent review.
9. Never claim a test passed without execution evidence.
10. Never weaken/delete assertions to make a test pass.
11. Never expose `.env`, credentials, tokens or private keys.
12. Never automatically push.
13. Maximum autonomous repair iterations: 3.
14. After 3 failed repairs, stop and produce HUMAN_REQUIRED.
15. Distinguish PRODUCT_BUG, TEST_BUG, ENVIRONMENT, FLAKY, DEPENDENCY and UNKNOWN.
16. Keep state and evidence under `.opencode/runtime/<task-id>/`.
