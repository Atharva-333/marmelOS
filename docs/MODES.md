# marmelOS Modes

marmelOS is planned around three modes: Ember, Dusk, and Dawn. They are three experiences within one operating system, not separate distributions.

## Ember — Gaming Mode

**Purpose:** Prioritise the active game and reduce avoidable competition for system resources.

Intended direction:

- Reduce or pause eligible, non-essential background activity.
- Prioritise the foreground game where supported by the operating system.
- Reduce unnecessary CPU and GPU workload from background applications.
- Coordinate power, performance, and compositor behaviour where appropriate.
- Preserve essential system, security, input, audio, networking, and user-requested services.

## Dusk — Development Mode

**Purpose:** Provide a responsive and power-conscious environment for sustained development work.

Intended direction:

- Balance performance and power consumption.
- Keep interactive development tools responsive.
- Avoid unnecessary background activity.
- Keep visual effects smooth but resource-conscious.
- Support long work sessions on portable computers.

## Dawn — Amusement Mode

**Purpose:** Provide an expressive, personal, and privacy-conscious everyday desktop experience.

Intended direction:

- Offer richer animations and visual effects.
- Support configurable gestures and interactions.
- Provide broad personalisation.
- Apply stronger privacy-oriented defaults and controls.
- Make privacy settings understandable and accessible.

## Shared behaviour

All modes will preserve essential system functionality. Mode transitions should be understandable and reversible. User data and active sessions will not be discarded simply because a mode changes.

The shared memory system is intended to preserve useful context across all three modes. See [Memory System](MEMORY_SYSTEM.md).

## Open design questions

The precise activation method, transition behaviour, profile controls, user overrides, failure recovery, and per-mode service policies will be specified later.
