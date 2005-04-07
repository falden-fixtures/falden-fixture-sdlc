# falden-fixture-sdlc

**A test fixture. Not real work. The code does nothing.**

Every commit, pull request, review, and branch ruleset in this repository was generated
deliberately. The history is anomalous on purpose: force-pushed protected refs, approvals
submitted after merge, approvals from people who wrote the code they approved, commits whose
author address resolves to no GitHub account, and commit trailers claiming machine assistance.
That is the product, not a compromise.

It exists so that Falden's collector can be run against live GitHub data and its output checked
against a known expected answer, rather than only against unit tests. Anyone may clone this
repository and re-run that check themselves.

Every expected answer is checked in under `fixtures/expected/`. Run the commands in
`SCENARIOS.md` and compare. Nothing here says anything about how any real project is developed.

## No license

Deliberate. GitHub's Terms of Service already grant every user the right to view and fork a
public repository, which is all you need to verify Falden's output against this fixture
yourself. No further copy or redistribution rights are granted, because this is not software
anyone should reuse.
