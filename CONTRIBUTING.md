# Contributing to KyPost Site

KyPost Site is the landing page for the KyPost email ecosystem — a self-hosted mail server and clients. Contributions keep the site accurate, accessible, and self-contained, and must not misrepresent KyPost's security posture.

## Before contributing

Read [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) and [SECURITY.md](SECURITY.md),
the [README](README.md), and any AGENTS.md in the subtree you are about to
touch. Open an issue before proposing a feature larger than a bug fix or
documentation change.

Keep changes small, reuse existing code, and fix the shared root cause rather
than the reported symptom. New non-trivial logic ships with a runnable test or
self-check.

## Security requirements

- The site is public-facing; do not add trackers, analytics, or third-party calls the project has not chosen.
- Claims about KyPost's security must match KyPost's actual behavior and its SECURITY policy.
- Keep pages accessible (WCAG AA contrast) and self-contained.
- Do not add telemetry, phone-home, analytics, or unconfigured third-party
  services.
- Do not add silent security fallbacks; fail closed with a readable error and a
  remediation step.
- Name and document any security trade-off in [SECURITY.md](SECURITY.md) before
  it merges.

## Verification

Fix valid compiler/linter warnings, or document why a warning is a false positive
in the relevant source or check configuration. Do not silently ignore warnings.

Run `python3 -m unittest discover -s tests -v`. Add automated regression checks
with major new functionality, and update [CHANGELOG.md](CHANGELOG.md) for
user-visible or security-related changes.

Validate Markdown and HTML links and asset paths, and run any site build or
lint before opening the pull request. Record the exact commands and results in
the pull request.

## AI attribution

AI-assisted contributions are welcome; undisclosed ones are not. Disclose
material AI assistance in the pull request — the tool, what it changed, and what
you personally ran, read, and verified — and add a commit trailer naming any
tool that materially contributed. You are the author of the code you submit for
every purpose, regardless of how it was produced.

## Pull requests

Branch off `main` with a focused name, and use a Conventional Commit subject
(`fix:`, `feat:`, `docs:`, `refactor:`, `test:`, or `chore:`). The pull request
explains why the change exists, the verification performed, the security impact,
and any known limitations.

Every pull request gets an adversarial review pass; see
[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md#hostile-reviews-are-about-code-never-people)
for what that is and the boundary it keeps.

## Licence

KyPost Site is licensed under the MIT License. See [LICENSE.txt](LICENSE.txt).

