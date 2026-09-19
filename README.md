# Esther Maina

**QA Automation Engineer in Training** · Nairobi, Kenya

Software Engineering diploma graduate building a specialization in QA automation.
Currently progressing through a structured 6-month roadmap covering manual testing
foundations, API testing, Playwright automation, and CI/CD pipeline integration.

---

## Featured Project

**[CareerMate](https://entry.esthermaina.com)**
AI-powered resume analysis and interview practice tool. Built with TypeScript
and the Anthropic API. Live at entry.esthermaina.com.

---

## 🛠️ Tech Stack

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=database&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white)
---

## QA Roadmap — August 2026

## MONTH 1: Test craft (the part everyone skips and then gets exposed on)
Automation without test design is just automating bad tests. This month is short but non-negotiable.
Learn
● SDLC and STLC, where QA sits, Agile ceremonies, definition of done, what a sprint actually feels like.
● Test design techniques, properly: equivalence partitioning, boundary value analysis, decision tables, state transition testing,
pairwise/combinatorial testing, error guessing.
● Test levels: unit, integration, system, acceptance. Test types: functional, regression, smoke, sanity, UAT.
● Severity vs priority, and how to defend your call to a PM who disagrees.
● Bug anatomy: title, environment, preconditions, steps, expected, actual, evidence, severity, impact.
● Exploratory testing with charters and session notes. This is a real skill, not "clicking around".
● Risk-based testing: how to decide what NOT to test.
● Browser DevTools deeply: network tab, console, application/storage, throttling, device emulation. Half of "is this a frontend or backend
bug" is answered here.
## Tools
● Jira (free tier) for the workflow. Qase or TestRail trial for test case management.
● Git and GitHub: commit, branch, PR, review. Non-negotiable from day 1.
● Markdown for documentation.
Milestone artifact (portfolio piece 1) Pick two real live products (one web app, one mobile app). Produce:
● A test plan and test strategy document for one of them.
● 30 to 40 test cases covering a critical flow, using named design techniques.
● 10 real bug reports with video, console logs, and network evidence.
● A one-page risk assessment: what would you test first with only 2 hours before a release, and why.
Gate (she must pass before month 2)
● Explain the difference between severity and priority using a bug she actually found.
● Take one of her test cases and justify why the specific boundary values were chosen.
● Given a feature spec cold, produce 10 test cases in 20 minutes without help.
● Reproduce one of her own bugs live, from her own report, without improvising steps.

## MONTH 2: Code and APIs (where the money starts)
API testing is the highest value-per-hour testing there is. It is faster, more stable, and catches deeper bugs than UI testing. In Kenya
specifically, most of the interesting bugs live in integrations: payments, M-Pesa callbacks, SMS, third party APIs, reconciliation.
Learn: just enough JavaScript/TypeScript Variables and types, functions, arrow functions, arrays and objects, destructuring, loops, promises
and async/await, modules, npm and package.json, error handling. That is it. She does not need a full JS bootcamp. She needs to read and
write code confidently.
# Learn: HTTP and APIs properly
● Methods, status codes (and what a 401 vs 403 vs 422 actually implies), headers, query params vs path params vs body.
● REST semantics, JSON, JSON Schema.
● Auth: Basic, API keys, Bearer/JWT (decode one, understand claims and expiry), OAuth2 flows at a conceptual level.
● Idempotency, retries, timeouts, rate limits, pagination, webhooks and callbacks.
● Why a callback-based payment flow is the single most bug-prone thing in African fintech.
# Tools
● Postman: collections, environments, variables, pre-request scripts, test scripts, chaining requests, running collections in Newman from
the CLI.
● Bruno as the open source alternative worth knowing.
● Code-level API testing: Playwright's request fixture, or supertest, or pytest + requests if going Python.
● Schema validation with zod or ajv.
Milestone artifact (portfolio piece 2) An automated API test suite in code (not just Postman) against a real public API plus one deliberately
messy target. Must include:
● Happy path, negative cases, auth failure cases, boundary cases.
● Response schema validation.
● Data setup and teardown.
● A README explaining what each test protects against. Bonus that will make her stand out locally: build a mock payment flow (initiate,
pending, callback, reconcile) and write tests for double-callback, late callback, and failed callback scenarios.
Gate
● Given a failing API test, correctly classify it: product bug, test bug, data issue, or environment issue. Explain how she knows.
● Explain what happens if the same payment callback is delivered twice, and write the test that catches it.
● Write a test for an endpoint she has never seen, using only its docs.

## MONTH 3: UI automation done properly (Playwright)
Primary tool: Playwright. Fastest path to professional competence, best debugging story, strongest momentum in the market.
Also needed: Selenium literacy. A lot of Kenyan enterprise and banking shops still run Selenium with Java or Python. She does not need to
be an expert, but she must be able to answer Selenium questions in an interview and read an existing suite. Give it one weekend.
# Learn deeply:
● Locator strategy: role-based and accessibility-first locators, getByRole, getByLabel, test IDs. Why CSS chains and XPath are
technical debt.
● Auto-waiting and web-first assertions. Why sleep(3000) is the mark of an amateur and what to do instead.
● Fixtures, hooks, test isolation, parallel execution.
● Page Object Model, and just as importantly when POM is overkill.
● Test data strategy: seed via API, never via the UI. Reset state between tests. Never depend on test execution order.
● Authentication with storageState so you log in once, not 200 times.
● Trace viewer, videos, screenshots on failure.
● Flakiness: root causes (timing, shared state, network, animation, test order) and how to actually fix them rather than adding retries.
● Visual regression basics.
● Mobile: pick one, Appium (industry standard, painful) or Maestro (much easier, growing fast). Maestro is the better use of time for a first
pass.
# Milestone artifact (portfolio piece 3) An end-to-end suite against a real application with:
● At least 25 tests covering signup, login, a core transaction flow, and edge cases.
● Runs in parallel, under 5 minutes, zero flaky tests over 10 consecutive runs.
● API-based test data setup.
● Tagged smoke vs regression subsets.
● A written flakiness postmortem: one test that was flaky, the root cause, and the fix.
Gate
● Hand her a deliberately flaky test. She must diagnose the real cause and fix it without adding a sleep or a retry.
● Explain why she chose the locators she chose.
● Run her suite 10 times in a row live. If it is not 10 for 10, she is not through the gate.

## MONTH 4: The engineering layer (this is the junior-to-mid jump)
This is the month that separates "tester who can write scripts" from "quality engineer". It is where the salary bump lives.
# CI/CD with GitHub Actions
● Run the suite on every PR, on merge, and on a nightly schedule.
● Matrix runs across browsers, sharding for parallelism.
● Uploading artifacts: traces, videos, HTML reports.
● Publishing reports (GitHub Pages, or Allure).
● Secrets and environment configuration.
● Failing the build correctly, and quarantine strategy for known-flaky tests.
● Awareness of GitLab CI and Jenkins, since plenty of Kenyan enterprises run Jenkins.
# Environments and infra
● Docker basics: run the app and a database in containers so tests have a clean environment.
● Awareness of Testcontainers.
● Test environments, config management, seeding, why "it works on staging" is a real problem.
Test strategy as a discipline
● Test pyramid vs testing trophy, and what to automate vs leave manual.
● Why code coverage percentage is a vanity metric, and what mutation testing (Stryker, PITest) proves instead.
● Shift-left: testing in PRs, reviewing requirements for testability, contract testing awareness (Pact).
● Shift-right: monitoring, feature flags, canary releases, synthetic monitoring, observability. QA increasingly overlaps with observability,
and saying so in an interview lands well.
● Quality metrics: escaped defect rate, defect density, MTTD, flake rate, cycle time.
Non-functional testing
● Performance with k6: smoke, load, stress and soak tests. Understand p95 vs average, thresholds, and how to write a performance
report that a CTO reads.
● Security basics: OWASP Top 10, testing authentication and authorisation, IDOR, broken access control, injection. Tools: OWASP ZAP,
Burp Suite Community. Security-aware test coverage is one of the weakest areas across the whole industry, so this is cheap
differentiation.
● Accessibility: axe-core, WCAG basics, keyboard navigation, screen reader smoke checks. Quietly a hiring differentiator, especially for
international and remote roles.
# Milestone artifact (portfolio piece 4)
● The month 3 suite running in a full GitHub Actions pipeline, with published reports, tagged runs and artifacts on failure.
● A k6 load test with defined thresholds plus a written performance report with a recommendation.
● A security test pass against a deliberately vulnerable app (OWASP Juice Shop) with a written findings report.
Gate
● Break her pipeline on purpose. She has to diagnose it from the logs alone.
● Ask: "we have 4 hours of manual regression before each release. Give me a plan to get it to 20 minutes." She should answer with a
strategy, not a tool list.
● Have her defend one thing she chose NOT to automate.

## MONTH 5: AI (the differentiator)
This is what makes a 6-month candidate beat a 3-year candidate in 2026. Two tracks, and she needs both.
Track A: Using AI to do QA faster
● Using Claude Code, Copilot or Cursor to scaffold tests from a spec or a ticket.
● Generating test data: Faker for structure, LLMs for realistic edge case data, synthetic PII-safe data.
● Converting a bug report or a screen recording into a reproducible automated test.
● Failure triage: feeding traces and logs to an LLM to get to root cause faster.
● Reviewing PRs for testability.
● Self-healing locators and AI-augmented tools: Testim, mabl, Meticulous. Know what they do and their limits.
The discipline that matters more than the tools:
● AI writes the first draft. A human adds the edge cases, business rules and the assertions that actually matter.
● Verify AI-generated tests actually catch faults. High coverage from generated tests does not mean fault detection. Prove it with mutation
testing.
● AI generates happy paths by default. Security, authorisation and edge cases have to be asked for explicitly.
● She must be able to say in an interview: "AI made my suite 3x faster to write, and here is exactly where I stopped trusting it."
Track B: Testing AI features (the scarce skill)
This is where the premium sits. Companies are shipping AI features and have nobody who knows how to test them.
● Why non-determinism breaks traditional assertions, and what replaces exact-match assertions.
● Evals: golden datasets, rubric scoring, LLM-as-judge, pass thresholds, regression on prompt changes.
● RAG evaluation: faithfulness, answer relevancy, context precision and recall, hallucination detection.
● Adversarial testing: prompt injection, jailbreaks, data exfiltration through prompts, red-teaming.
● Safety and compliance checks: toxicity, bias, PII leakage.
● Operational criteria as test criteria: latency budgets, token cost per request, timeout and fallback behaviour.
● Tools: promptfoo, DeepEval, RAGAS, LangSmith, Braintrust, Giskard.
Milestone artifact (portfolio piece 5, the headline one) Build a small LLM feature (a support chatbot answering over a set of docs is enough)
and then build the eval suite around it:
● A golden dataset of 50+ question/expected-answer pairs.
● Automated scoring with LLM-as-judge plus deterministic checks.
● A prompt injection and jailbreak test set that must be fully blocked.
● Hallucination and PII leakage checks.
● The whole thing running in CI with a pass threshold, so a prompt change that degrades quality fails the build.
● A README explaining the methodology.
Almost nobody applying for junior QA roles in this market has this. It is worth more than any certificate.
Gate
● "How do you test something that gives a different answer every time?" She must answer confidently and with specifics.
● Show her an AI-generated test suite with a subtle flaw (an assertion that always passes). She must catch it.
● Demonstrate the injection test set actually blocking an attack live.

---

## Contact

📧 mainagathigia0725@gmail.com
🌐 [entry.esthermaina.com](https://entry.esthermaina.com)
💼 [LinkedIn](https://www.linkedin.com/in/esther-maina-808478424)

