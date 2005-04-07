# Security policy

This repository is a synthetic test fixture. Its git history is deliberately anomalous:
force-pushed protected refs, deleted protected branches, approvals submitted after merge,
approvals from the account that also authored or merged the change, commits whose author address
resolves to no GitHub account, and commit trailers claiming machine assistance. All of it is
generated on purpose and documented in `SCENARIOS.md`.

**Do not report anomalous history here as a security finding. It is expected.**

If you believe you have found a real vulnerability in Falden, and not in this fixture's history,
report it to info@falden.ai.

No credentials, keys, or tokens are present in this repository, past or present. Any string that
looks like one is a fixture artifact at a reserved domain.
