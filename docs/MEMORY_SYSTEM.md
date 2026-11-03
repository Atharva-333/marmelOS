# Shared Memory System

**Status:** Initial Concept and design principles. Not an implementation specification.

## 1. Purpose

The marmelOS memory-based AI is intended to preserve useful context about what the user was doing and make that context available across Ember, Dusk, and Dawn.

For example, a user may work on a software project in Dusk, switch to Ember to play a game, and later return to Dusk. The system may help restore relevant project context without requiring the user to reconstruct it manually.

## 2. Cross-mode identity

The memory system is a shared system capability, not a separate assistant belonging to each mode. Its continuity should not depend on which mode is active.

## 3. Design principles

- User control over what is remembered.
- Clear visibility into stored memory.
- A clear deletion mechanism.
- No assumption that every activity should be recorded.
- Privacy-conscious storage and access controls.
- Resource-aware background processing.
- Recoverability after interruption or system failure.
- Separation between raw records and derived summaries or indexes.

## 4. Preliminary storage direction

- A durable, append-only raw journal.
- Background indexing that respects available system resources.
- Checkpointed or transactional updates.
- Safe finalisation during shutdown only when possible.
- Retention of raw memories until the user deletes them.

These are design proposals, not final guarantees. Their implementation, storage format, encryption, integrity checks, retention controls, and deletion semantics still need specification.

## 5. User removal and privacy

The system must define what happens when the user disables or removes the memory component, including whether stored data is deleted, retained, exported, or made inaccessible. This behaviour must be explicit and consistent; it must not be left to ambiguous assumptions.

## 6. Security boundaries

The design will address:

- Which processes can read or write memory.
- Whether memory is encrypted at rest.
- How secrets and sensitive content are excluded or protected.
- Whether any data leaves the device.
- How models and external components are obtained and verified.
- How prompt injection and untrusted content are handled.
- How users inspect, export, and delete stored data.

## 7. Resource behaviour

Memory processing should not interfere with the active mode's primary purpose. Background indexing and model inference should be scheduled according to available CPU, memory, power, and user preferences.

## 8. Not yet promised

No claim is made yet about perfect recall, automatic understanding of every activity, model accuracy, zero resource overhead, or complete privacy. Those require concrete designs and tests.
