# Resttoken

**Idea: donate your leftover AI subscription capacity to open source.**

Most of us pay for Claude, ChatGPT or similar and never hit the weekly limit.
That unused capacity simply expires, which is effectively a gift to the AI company.
Resttoken is a proposal for a small local tool that puts it to use for open-source
projects you choose instead.

> Status: **idea / RFC.** No code yet. Feedback wanted, see the Discussions tab.

## Concept

- Runs **locally** with **your own** login or API key. No credential sharing, no pooled accounts.
- You keep a **allowlist** of repositories that explicitly welcome AI contributions
  (for example via an `AI-CONTRIBUTIONS.md`), or vibe-coded open-source projects.
- You set **limits and a window**: for example only the last 12 hours before your weekly
  reset, and never above a usage percentage you define.
- It picks open tasks (`good first issue`, `help wanted`), runs the project's tests and
  lint, and opens a **clearly labeled AI-assisted pull request**.
- **Human in the loop:** by default nothing is sent without your approval.
- **Maintainer protection:** per-project cap on open PRs, quality gate before submitting,
  instant opt-out for any repo.

## Open questions

1. **Terms of service.** Subscription plans are meant for personal use. Is automated use
   on your own account allowed? Using your own API key with a budget cap is the safe path.
2. **Maintainer acceptance.** Many projects reject AI PRs. The opt-in list is the core of
   the idea, not a detail.
3. **Real value instead of noise.** How do we make sure contributions are useful?
   (tests must pass, small scope, reviewed by the donor)
4. **Opt-in format** for repos: `AI-CONTRIBUTIONS.md`, a topic tag, something else?
5. **Beyond PRs:** triage, docs, test coverage, dependency updates, security review.

## Roadmap (if there is interest)

1. Collect feedback in Discussions.
2. Minimal CLI prototype: allowlist, usage window, dry-run mode that only drafts PRs.
3. Opt-in spec for repositories.

## License

Apache-2.0, see [LICENSE](LICENSE).
