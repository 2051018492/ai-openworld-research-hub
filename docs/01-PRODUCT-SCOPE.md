# AI Open World — Public Product Scope

**Status: Product direction confirmed at a high level; technical implementation remains undecided.**

## 1. Two independently usable modes

### Character-card chat

Users can import or create character cards and begin chatting without creating an entire world. Lorebooks, memory, visualization, typed fields, group chat and branches are optional.

### Open-world simulation

Users may create a truly blank world or import a content pack. A world can track stable NPC identity, time, locations, relationships, facts and event history. NPCs may act according to their own circumstances. Simulation must respect bounded inference and compute budgets.

## 2. A neutral, configurable engine

The runtime should not hardcode particular cities, NPCs, phones, quests, combat, money, affinity scores or social networks. These can be configured through content, schema, plugins or optional modules. Users may define and disable arbitrary status fields.

## 3. What visualization means

A visual status panel should read actual persisted state; numbers printed by the model inside chat are not the authoritative record. Valid interactions should have observable, attributable consequences in the state display, character detail, world scene, memory or other permitted surfaces. Narration, fact and private knowledge must not be conflated.

## 4. Candidate logical layers (discussion only)

1. World definitions, character cards and content packages.
2. Entity identities, typed fields and authoritative world state.
3. Events, history and state transitions.
4. Validation, permissions, idempotency, rollback and versioning.
5. AI decisions, context filtering, knowledge boundaries and bounded scheduling.
6. User interaction and visual presentation.

These are **logical responsibilities, not a mandate to deploy six microservices**.

## 5. Research questions

- What is the smallest shared abstraction for character-only and world simulation modes?
- How do structured changes from AI become verified persistent facts?
- How should rejected events be corrected before they become false narration?
- What are the consequences of regeneration, deletion, swipes and story branches for event histories?
- Can different NPCs consistently have private knowledge?
- Which existing SillyTavern modules can be directly reused or legally adapted?
- Does a hybrid architecture cost less to maintain than replacing the original platform?

**Not authorized:** changing the private application, publishing private assets, deploying a service or migrating the base architecture.