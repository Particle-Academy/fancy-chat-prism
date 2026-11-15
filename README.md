# fancy-chat-prism

**OPTIONAL** Prism adapters for the Fancy agent-chat framework (council change
CC-fancy-0042). **Not started; nothing here is published.**

The chat framework's core (`@particle-academy/fancy-chat-js`,
`@particle-academy/fancy-chat-ui`, `particle-academy/fancy-chat-php`) is
provider-neutral and works with any agent backend, or none. The whole Prism
ecosystem is an optional addon, and this package is where its TypeScript half
lives:

| Entry | Maps |
|---|---|
| `./harness` | prism-harness run lifecycle + Prism core stream events onto the neutral run, turn, part and HITL events |
| `./acp` | `@particle-academy/prism-acp` session updates, turn outcomes, permission requests, commands and plans |
| `./graph` | prism-graph `ScopedGraph` reads onto a `KnowledgeAdapter`, from an app-bound scope only |
| `./memory` | prism-memory, scope to be agreed with Prism |

The adapters use Prism's own types and stream events; nothing Prism already does
is rewritten here.

This is the only TypeScript chat package allowed to import Prism, and it is the
negative control of the core packages' no-Prism packaging test.

Design: `.ai/plans/agent-chat-framework.md` in the Fancy envelope.
