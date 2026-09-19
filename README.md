# falden-fixture-sdlc

**This repository is a test fixture. Every commit in it is synthetic. None of it is real work, none of it runs, and its git history is deliberately anomalous.**

It exists to answer one question with evidence instead of assertion: when a tool claims to tell you whether a merged code change was approved by someone independent of its author, is it right?

You cannot answer that against a real repository, because nobody knows the true answer there. So this one was built backwards. Each scenario was constructed to a written specification, the expected verdict was recorded before any tool looked at it, and the tool is graded against the written answer.

## The answers are in a separate repository

This repository is the **history**. The expected answers, the frozen evidence, and the grader live in **[falden-fixture-pack](https://github.com/falden-fixtures/falden-fixture-pack)**.

```bash
git clone https://github.com/falden-fixtures/falden-fixture-pack
cd falden-fixture-pack
sha256sum -c MANIFEST.sha256
bin/fixpack verify
```

They are split on purpose. This repository is sealed: the pack carries frozen captures of every API response the evaluator reads, and a later commit here would add a change those captures do not contain. Two repositories keep the record and the evidence about the record from drifting apart.

## Read this if you found this repository by accident

Nothing here is a vulnerability, a mistake, or an incident. The history contains, on purpose:

- commits pushed directly to a protected branch, bypassing a rule that was active at the time
- pull requests merged with no approval, and with fewer approvals than the rule required
- approvals submitted after the merge they supposedly gated
- a branch rewritten after it was approved
- a commit signed by a key that belongs to no account
- a commit whose author address is at a reserved domain and resolves to nobody
- an approval whose written remark was replaced after the change had already merged
- configuration relaxed and restored inside a measured window

Every one of those is the point. Do not copy any pattern from this repository into anything real.

Every commit body carries the line `FIXTURE: synthetic commit in falden-fixture-sdlc. Not real work. See README.` There is exactly one exception, and it is documented: the merge commit produced by GitHub's merge queue, because `enqueuePullRequest` accepts no commit-body input and the queue writes its own message.

## What is in this repository

An inert source tree under `src/`, a code-owner definition under `docs/`, and one dispatch-only workflow under `.github/`. Nothing here compiles, runs, or is imported by anything. Each file exists only so that a commit had something to touch.

The interesting content is not the files. It is the shape of the history: who approved what, when, under which configuration, and by which mechanism.

## Email addresses

Every address in this history is either a GitHub `noreply` address or an address at a domain reserved by RFC 2606 and RFC 6761 (`.invalid`). None is deliverable and none identifies anyone.

## No license

Deliberate. GitHub's Terms of Service already grant every user the right to view and fork a public repository, which is everything needed to verify the work. No further permission to copy, modify or redistribute is granted.

Security policy: [SECURITY.md](SECURITY.md).