### Korean indie hacker · building in public

Gym + code, daily. I build small, honest developer tools and validate
before I monetize — evidence over guesses.

**Currently building**

- **[agentproof-scan](https://github.com/ghkfuddl1327-wq/agentproof)** — a
  pre-deployment security scanner for self-hosted AI agents. Fires prompt-injection
  probes and checks whether the agent leaks its system prompt or API keys — including
  in its reasoning trace, where a leak hides even when the answer looks clean. Two-stage
  detection (leak vs prompt-disclosure), scan your own HTTP agent or gate CI, plus a
  paste-ready handoff block via --handoff. `pip install agentproof-scan` · Detect it, prove it.

**How I got here**

Each tool taught me the limit that pushed me to the next:

- **[preship](https://github.com/ghkfuddl1327-wq/preship)** — contract checks for
  FastAPI apps (500 crashes, undocumented status codes, schema mismatches). Learned that
  contract validation alone can't catch LLM-specific leaks.
- **[rojaprove](https://github.com/ghkfuddl1327-wq/rojaprove)** — a red-team CLI for LLM
  apps that detects system-prompt leakage (OWASP LLM07). Learned that watching only the
  answer channel misses leaks in the reasoning trace — which pointed me to agentproof.

**How I work**

Solo, local-zero, build-in-public. I'd rather ship a narrow tool that's
actually deterministic than a broad one that quietly guesses.

🛠 Python · ⚡ FastAPI · 🤖 LLM / agent security 📌 X @OHS1327


⚠️ Responsible Disclosure & Safety Notice

This work follows responsible disclosure principles. The goal is detection, not offense — knowing what leaks before you ship an AI agent, so you can prevent it.

- To prevent misuse, the exact bypass-prompt strings used in testing are masked/generalized.
- All tests run only against intentionally-vulnerable, self-controlled demo targets — never against external services or anyone else's systems.
- What's shared is where defenses shift the leak rate and where they don't, not a runnable recipe for how to attack.
