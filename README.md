# fancy-chat-prism

> **Retired, never built or published** (owner, 2026-11-16).

It was planned as the one TypeScript chat package allowed to import Prism, the
"optional addon" of a provider-neutral core. That reading of the CC-fancy-0042
ruling was wrong: the Fancy agent chat is built on the Prism ecosystem, and only the
extras (prism-graph, prism-memory, the browser) are optional. So there is no
separate adapter package:

- `@particle-academy/fancy-chat-ui` reads prism-graph's own types directly
  (`./knowledge`).
- Prism Harness runs on the server: `particle-academy/fancy-chat-php` 0.2.0 today, and
  a Node twin on `@particle-academy/prism-harness` and `@particle-academy/prism-acp`
  next, both implementing the `@particle-academy/fancy-chat-js` contract.

Design: `.ai/plans/agent-chat-on-prism.md` in the Fancy envelope.
