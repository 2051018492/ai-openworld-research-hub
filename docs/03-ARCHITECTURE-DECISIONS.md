# Architecture Decision Ledger — Public Research Scope

All entries describe **product intentions or discussions**, not permission to code or deploy.

| Topic | Status | Next evidence |
|---|---|---|
| Open-world as core long-term product experience | Confirmed product goal | End-to-end realistic behavior |
| Character-card chat without mandatory world setup | Confirmed product goal | Session/identity design |
| World content and fields fully configurable | Confirmed product goal | Schema and UX proof of concept |
| Persistent state backing visible indicators | Proposed architecture | Event and real-model tests |
| Separating validated facts from model narration | Proposed architecture | Rejected-proposal experiments |
| NPC autonomy with bounded catch-up and private knowledge | In design | Behavior/cost tests |
| A: SillyTavern as primary application base | Undecided | Code audit, PoC, license |
| B: Independent engine + selected component reuse | Undecided | Dependency/migration estimate |
| C: SillyTavern interface + independent world service | Undecided | Bridge prototype |
| Public multi-user deployment | Not approved | Security and operations review |

## Proposed state-change protocol (not yet approved)

- Typed fields have stable namespaced identities and explicit owners.
- User-authored world definitions are separate from individual persistent world instances.
- AI may propose actions and changes; validation checks schema, permissions, preconditions, version and idempotency.
- Accepted events and state updates are committed atomically; rejected proposals never silently change the database.
- Narration, UI and memory reflect only committed world facts and explicitly labeled uncertainty.
- Display is filtered by observer access and character knowledge.
- Swipes, regeneration and branching need branch-aware facts rather than a single mutable chat state.

## Decision authority

Use `proposed` → `discussed` → `approved` → `implementing` → `verified` with dated evidence. Main-brain + user choose product architecture. An agent's research recommendation is not an implementation approval.