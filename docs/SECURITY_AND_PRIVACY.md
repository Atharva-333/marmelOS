# Security and Privacy Principles

**Status:** Initial principles; not a security specification or audit.

## 1. Security posture

marmelOS intends to build on established Linux security facilities and add clearly scoped userspace protections where appropriate.

The project must not claim that a mode is "the most secure" or that the operating system is secure by default until the relevant controls are implemented, tested, and documented.

## 2. Least privilege

System services should receive only the permissions they need. User-facing applications and background components should not receive broad system access without a defined reason.

## 3. Privacy

The project should document:

- What data is collected or generated.
- Where data is stored.
- Which components can access it.
- Whether data is transmitted outside the device.
- How long data is retained.
- How users inspect, export, and delete it.

## 4. Memory system

The memory-based AI requires special care because it may process activity context and personal information. Its data access, storage, deletion, model execution, and network behaviour must be explicit and user-controllable.

## 5. Updates and vulnerabilities

Before public release, the project needs a documented update process, a way to receive vulnerability reports, a severity assessment process, and a realistic policy for communicating fixes.

No response-time or support-duration guarantee is made in this foundation document.

## 6. Security reporting

A dedicated security contact and private reporting channel should be established before public release. Do not publish sensitive exploit details before a coordinated response has been considered.

## 7. Claims and verification

Security claims should identify the protection, threat model, limitations, and evidence. A privacy-focused interface or a security setting alone does not establish that the entire system is secure.
