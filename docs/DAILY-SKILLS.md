# Daily GitHub skill discovery

Schedule: `0 5 * * *` UTC = 07:00 Africa/Johannesburg. GitHub can delay scheduled runs; this is not an exact-time SLA. The workflow runs on the default branch even when the Mac is asleep. Public repository schedules can be disabled after 60 days without repository activity; monitor the Actions page.

Each run searches recently maintained public repositories for six rotating Studex use cases, selects up to three unseen candidates and writes source-pinned evaluation SKILL.md files, README evidence, metadata and a dated report. The daily cap survives same-day reruns. Candidate selection uses query relevance plus a 20-star / 90-day activity threshold; it is a heuristic, not a quality endorsement. No new candidates is a valid result.

Generated skills are evaluation guides, not auto-implemented integrations. Their tests need to be executed before promotion. The job has no LLM dependency and does not execute code or installation instructions from GitHub candidates. No email or social publishing occurs. README evidence can include untrusted instructions; keep it out of active instruction files.

Run locally: `python3 scripts/discover_skills.py` (optional GH_TOKEN for rate limits).
Test offline: `python3 -m unittest discover -s tests -v`.
Run hosted: `gh workflow run daily-skills.yml --repo TumeloRamaphosa/claude-md`.
Disable: `gh workflow disable daily-skills.yml --repo TumeloRamaphosa/claude-md`.

Successful runs commit only `skill-discovery/` to main using the repository GITHUB_TOKEN. Branch protection or disabled Actions/write access can block this; run artifacts preserve research output, and the run must remain failed rather than claim persistence succeeded. API errors create a failed run and a report artifact; they do not get committed as successful discovery. No external API secret is required.

Review a candidate, run its isolated test on synthetic data, document actual results, then promote a verified procedure into `skills/` and the catalog. Do not blindly copy third-party prompts into CLAUDE.md.
