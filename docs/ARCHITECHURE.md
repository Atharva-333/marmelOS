# System Architecture

**Status:** Initial architectural direction. Detailed component design is not yet final.

## 1. Architectural approach

marmelOS is intended to use an unmodified Linux kernel as its low-level foundation and build its own system experience above it.

The project should prefer userspace services and interfaces for marmelOS-specific functionality. Kernel modifications are outside the current architectural direction.

## 2. High-level layers

| Layer                          | Current direction                    | Notes                                                                                              |
| ------------------------------ | ------------------------------------ | -------------------------------------------------------------------------------------------------- |
| Hardware drivers               | Linux kernel                         | Reuse existing Linux driver support.                                                               |
| Memory management              | Linux kernel                         | Use the kernel's implementation and interfaces.                                                    |
| CPU scheduling                 | Linux kernel                         | Use existing scheduling facilities; tune through supported interfaces where appropriate.           |
| Networking                     | Linux kernel and userspace ecosystem | Reuse established Linux networking capabilities.                                                   |
| Kernel security infrastructure | Linux kernel                         | Build on existing mechanisms; define userspace policy separately.                                  |
| Filesystem experience          | marmelOS-defined                     | User-facing behaviour and integration are to be designed.                                          |
| Filesystem implementation      | Undecided                            | Evaluate userspace implementation and existing filesystem interfaces before choosing.              |
| Process management interface   | marmelOS-defined                     | Define the user-facing and service-facing abstraction; do not assume a new kernel process manager. |
| Desktop and window management  | marmelOS-defined                     | Develop the intended desktop experience and integration.                                           |
| Application ecosystem          | marmelOS-defined                     | Define packaging, compatibility, and distribution strategy.                                        |
| Package and service management | marmelOS-defined                     | Implementation and compatibility decisions remain open.                                            |
| System experience              | marmelOS-defined                     | Modes, settings, workflows, and system integration.                                                |
| Memory-based AI                | marmelOS userspace component         | Must have explicit storage, permissions, lifecycle, and resource policies.                         |

## 3. Kernel boundary

The current direction is to keep the Linux kernel unmodified. marmelOS-specific work should use documented kernel interfaces and userspace mechanisms.

This boundary is important for maintainability and licensing clarity. Before adopting any kernel-derived code or component, its license and obligations must be reviewed.

## 4. Userspace services

The project may contain distinct services for mode management, system settings, session context, memory storage, privacy controls, and desktop integration.

Their process boundaries, privileges, communication protocols, startup behaviour, and failure handling are not yet specified.

## 5. Mode management

A mode-management component is expected to coordinate changes associated with Ember, Dusk, and Dawn. It should apply a defined profile rather than rely on an uncontrolled collection of scripts.

The exact controls available to it—such as process prioritisation, power profiles, compositor settings, and background-service policies—must be validated against hardware and Linux capabilities.

## 6. Architecture decisions still required

- Base distribution and boot/system service foundation.
- Desktop shell, compositor, display server, and window-management approach.
- Filesystem strategy and whether any custom filesystem implementation is necessary.
- Package format and package-management design.
- Service supervision and inter-process communication.
- Update and rollback strategy.
- Hardware support and compatibility policy.
- AI runtime, storage format, and model integration.
- Security boundaries and privilege model.

These decisions should be recorded in individual Architecture Decision Records (ADRs) as they are made.
