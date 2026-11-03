# Project Overview

**Project:** marmelOS  
**Project type:** Independent operating-system project  
**Kernel foundation:** Linux  
**Project stage:** Early-stage planning and architecture  
**Maintainer:** Atharva Lohaer
**Last updated:** 2026-11-03

## 1. What is marmelOS?

marmelOS is an independent operating-system project built on the Linux kernel. It aims to provide a distinct system experience through its own user-facing environment, system services, interfaces, and application ecosystem.

It is organised around three activity-oriented modes—Ember, Dusk, and Dawn—and a shared memory-based AI concept intended to preserve useful context across those modes.

## 2. Why does it exist?

The project explores whether one operating system can provide meaningfully different experiences for gaming, development, and everyday personal use without fragmenting the user's environment.

The goal is not simply to change a wallpaper, theme, or power profile. Each mode should eventually have clearly defined system-level behaviour appropriate to its purpose.

## 3. Who is it for?

The intended audiences include:

- People who play games on their computers.
- Developers and technical users.
- People who value personalisation and control over their desktop experience.
- Users interested in a distinct, privacy-conscious computing environment.

These are intended audiences, not a promise of compatibility with every device or workflow.

## 4. Product shape

marmelOS is conceived as one operating system with multiple modes:

- **Ember:** gaming-oriented resource prioritisation.
- **Dusk:** development-oriented efficiency and responsiveness.
- **Dawn:** expressive personal computing and stronger privacy-oriented protections.
- **Shared memory system:** continuity of useful context across modes.

## 5. Technical direction

The current direction is to use an unmodified Linux kernel and implement marmelOS-specific functionality in userspace. The project will rely on existing Linux kernel capabilities where appropriate while developing its own higher-level system experience.

Specific implementation choices remain subject to architecture decisions and feasibility testing.

## 6. Project boundaries

marmelOS is not currently claiming to:

- Be a new kernel.
- Replace every existing Linux subsystem.
- Support every hardware configuration.
- Guarantee higher frame rates in every game.
- Guarantee that every workload uses less power.
- Provide a fully autonomous AI that can safely infer every user intention.
- Be production-ready or security-audited.

## 7. Current status

This document describes project intent. It does not define a release commitment. Requirements, goals, features, compatibility targets, milestones, and timelines will be documented separately after the foundation is reviewed.
