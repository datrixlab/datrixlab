## Dat Nguyen

Backend and infrastructure work, mostly in Python and TypeScript. I spend most of
my open-source time on the unglamorous parts of self-hosted tooling: request
routing, credential handling, auth boundaries, and the code paths that only run
when something has already gone wrong.

### How I work

I try to send patches that a maintainer can verify without trusting me:

- **Prove the bug is reachable, not just present.** A helper that misbehaves in
  isolation is a curiosity; a helper that misbehaves on a value the production
  path actually hands it is a bug. I trace it end to end before writing a fix.
- **Every fix comes with a test that fails without it.** I revert the patch and
  re-run to confirm the test actually pins the behaviour — including a test that
  goes through the real call site, not only the helper in isolation.
- **Report what I ran, including what I could not run.** If a suite is red before
  my change, I say which tests and why, by name.
- **Say what I rejected.** Fixes I tried and dropped usually explain the shape of
  the one I kept.

### Interests

Credential redaction and log hygiene · auth and owner-scope boundaries ·
prompt-injection surfaces in LLM tooling · HTTP/SSE protocol translation ·
regression tests for bugs that only appear under retry or concurrency.

### Elsewhere

Contributions are listed on the activity tab as they land. This account is new —
I would rather it be judged on the diffs than on a summary written here.
