# ADR-0004: Licence

Status: accepted
Date: 2026-11-14

## Context

Perigee is a free, open-source desktop app for spaceflight fans. Free Windows signing through SignPath Foundation requires an OSI-approved licence. Most Rust crates use the same dual licence. The licence choice must support both needs.

## Decision

Use the dual licence "MIT OR Apache-2.0". The user selects one of the two licences when the user reuses the code.

## Alternatives

- MIT only. It is short. It has no patent clause.
- Apache-2.0 only. It has an explicit patent grant. Its text is longer.
- GPL-3.0. It is a copyleft licence. Changed versions must publish the source. Reuse of the code becomes more difficult.

## Consequences

Positive:
- Users have maximum freedom.
- The licence agrees with the Rust ecosystem.
- The project can apply for free Windows signing through SignPath Foundation.

Negative:
- Closed forks are permitted.

## Review trigger

Closed forks become a problem for the project.
