# marmelOS

> An operating system shaped around the way people use their computers.

**marmelOS** is an independent operating-system project being built on the Linux kernel, with its own system experience, desktop environment, user-facing interfaces, services, and application ecosystem.

The project explores a simple idea: the operating system should adapt its behaviour to the user's activity without taking control away from the user.

marmelOS is currently in its early Requirements Analysis and Planning stage. Its architecture, requirements, features, and release scope are being documented before implementation commitments are made.

## The three experiences

marmelOS is organised around three proposed operating modes:

| Mode      | Purpose     | Direction                                                                                            |
| --------- | ----------- | ---------------------------------------------------------------------------------------------------- |
| **Ember** | Gaming      | Prioritise the active game and reduce unnecessary resource competition.                              |
| **Dusk**  | Development | Balance responsiveness, sustained performance, and power efficiency for focused work.                |
| **Dawn**  | Amusement   | Offer a more expressive, customisable desktop experience with stronger privacy-oriented protections. |

These modes are intended to change system behaviour and presentation, not create three separate operating systems.

## A shared memory system

A memory-based AI concept runs across the three modes. Its purpose is to preserve useful user context when the user changes activities or modes—for example, helping someone return to the project they were working on.

The intended design is user-controlled and privacy-conscious. Its data lifecycle, deletion behaviour, storage model, resource use, and security boundaries will be specified before implementation.

## Technical foundation

marmelOS uses the Linux kernel as its low-level foundation for now. The current architectural direction is to keep the kernel unmodified and build marmelOS-specific functionality in userspace.

The project intends to create its own system experience and major user-facing components. The exact implementation boundaries for areas such as filesystem services, process interfaces, package management, and desktop infrastructure will be documented in the architecture decisions.

## Project principles

- **User agency:** the system should adapt to the user, not unnecessarily dictate how they work.
- **Purposeful modes:** Ember, Dusk, and Dawn should have distinct goals and measurable behaviour.
- **Privacy by design:** personal data and memory features should have clear controls and boundaries.
- **Visible source, defined permissions:** users should be able to inspect the source under the project's published terms.
- **A distinct identity:** marmelOS should be more than a reskinned desktop.
- **Honest engineering:** performance, privacy, compatibility, and security claims must be tested rather than assumed.

## Project status

**Status:** Early-stage project / foundation documentation.

This repository currently establishes the project's identity and documentation structure. It is not a statement that the proposed features are already implemented or production-ready.

## Documentation

Start here:

- [Project overview](docs/PROJECT_OVERVIEW.md)
- [Project philosophy](docs/PHILOSOPHY.md)
- [System architecture](docs/ARCHITECTURE.md)
- [Operating modes](docs/MODES.md)
- [Memory system concept](docs/MEMORY_SYSTEM.md)
- [Source visibility and permissions](docs/LICENSING_AND_PERMISSIONS.md)
- [Contribution policy](docs/CONTRIBUTING.md)
- [Governance and decision-making](docs/GOVERNANCE.md)
- [Security and privacy principles](docs/SECURITY_AND_PRIVACY.md)
- [Documentation status](docs/DOCUMENTATION_STATUS.md)

Requirements, goals, feature specifications, milestones, and timelines will be added as separate documents after the foundation is reviewed.

## Name and identity

The name **marmelOS** is inspired by _Aegle marmelos_ (the bael tree). The tree's trifoliate leaf provides a reference for the project's visual identity.

The final logo, visual system, and naming conventions will be documented separately.

## Copyright

Copyright (c) 2026 Atharva Lohar. All rights reserved.

The project's source-visibility and usage permissions are intended to be governed by a separate license that will be published before the first public release. This README is not a substitute for that license.
