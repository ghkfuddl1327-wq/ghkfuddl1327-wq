### Korean indie hacker · building in public

Gym + code, daily. I build small, honest developer tools and validate
before I monetize — evidence over guesses.

**Currently building**

- **[preship](https://github.com/ghkfuddl1327-wq/preship)**preship** — a pre-launch reliability check for FastAPI apps.
- Point it at a staging URL; it finds what breaks the contract (500 crashes, undocumented status codes, schema mismatches)
- and hands you a copy-paste fix prompt per pattern. Not a security scanner — it does one job and is honest about the edges. No API key required.

- **[rojaprove](https://github.com/ghkfuddl1327-wq/rojaprove)** — a pre-launch
  red-team CLI for LLM apps. Plant a canary, send leak probes, get a
  deterministic red/green verdict with evidence and a paste-ready fix.
  v0.1 detects system-prompt leakage (OWASP LLM07). *Find it, prove it, fix it.*

* [agentproof-scan](https://github.com/ghkfuddl1327-wq/agentproof) —  a pre-deployment security scanner for self-hosted AI agents (demo targets today; bring-your-own in progress). Fires prompt-injection probes and checks if the agent leaks its system prompt or API keys — two-stage detection (leak vs prompt-disclosure) plus a paste-ready fix via --handoff. Grew out of my earlier red-team work. Find it, prove it, fix it.

**How I work**

Solo, local-zero, build-in-public. I'd rather ship a narrow tool that's
actually deterministic than a broad one that quietly guesses.

🛠 Python · ⚡ FastAPI · 🤖 LLM / agent security 📌 X @OHS1327


⚠️ Responsible Disclosure & Safety Notice

This work follows responsible disclosure principles. The goal is defense, not offense — knowing what leaks before you ship an AI agent, so you can prevent it.

- To prevent misuse, the exact bypass-prompt strings used in testing are masked/generalized.
- All tests run only against intentionally-vulnerable, self-controlled demo targets — never against external services or anyone else's systems.
- What's shared is which defenses work, not a runnable recipe for how to attack.
